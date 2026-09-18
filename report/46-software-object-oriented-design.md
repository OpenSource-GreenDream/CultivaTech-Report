## 4.7. Software Object-Oriented Design.

## 4.7.1. Class Diagrams.

```plantuml
@startuml
skinparam backgroundColor #FFFFFF
skinparam defaultFontColor #333333
skinparam classFontColor #1A1A1A
skinparam classAttributeFontColor #555555
skinparam class {
    BackgroundColor #F8F9FA
    BorderColor #DEE2E6
    HeaderBackgroundColor #E9ECEF
    HeaderFontColor #0066CC
    FontColor #1A1A1A
}

skinparam arrow {
    Color #6C757D
    FontColor #495057
    Thickness 1
}

skinparam package {
    BackgroundColor #F8F9FA
    BorderColor #ADB5BD
    FontColor #0066CC
}

title <color:#0066CC><size:18>AgroTech IoT - Class Diagram</size></color>

hide empty members

' ==================== SHARED KERNEL ====================
package "Shared Kernel" {
    interface IAuditableEntity {
        + CreatedAt : DateTimeOffset?
        + UpdatedAt : DateTimeOffset?
    }
    interface IBaseRepository<T> {
        + AddAsync(T) : Task
        + FindByIdAsync(int) : Task<T?>
        + Update(T) : void
        + Remove(T) : void
        + ListAsync() : Task<IEnumerable<T>>
    }
    interface IUnitOfWork {
        + CompleteAsync() : Task
    }
}

' ==================== IAM ====================
package "IAM" {
    class User {
        + Id : int
        + Email : Email
        - PasswordHash : string
    }
    class Email <<ValueObject>> {
        + Value : string
    }
}

' ==================== PROFILE ====================
package "Profile" {
    class Profile {
        + Id : int
        + UserId : int
        + FundoName : string
        + ContactPhone : string
        + MoistureThreshold : double
        + TempThreshold : double
    }
}

' ==================== MONITORING ====================
package "Monitoring" {
    class Field {
        + Id : int
        + ProfileId : int
        + Name : string
        + SizeM2 : double
        + SoilType : string
        + Latitude : double
        + Longitude : double
    }
    class Device {
        + Id : int
        + FieldId : int
        + MacAddress : string
        + Status : string
        + LastSync : DateTimeOffset
    }
}

' ==================== COMMERCIAL ====================
package "Commercial" {
    class Order {
        + Id : int
        + ProfileId : string
        + ProductId : int
        + Quantity : int
        + TotalAmount : decimal
        + Status : OrderStatus
        + PaymentMethod : PaymentMethod
    }
    class Product {
        + Id : int
        + Name : string
        + Description : string
        + Price : decimal
        + Type : string
    }
    enum OrderStatus {
        Pending
        Validated
        Paid
        Completed
        Cancelled
    }
    enum PaymentMethod {
        CreditCard
        DebitCard
        PayPal
        BankTransfer
    }
}

' ==================== STOCK ====================
package "Stock" {
    class Inventory {
        + Id : int
        + ProductId : int
        + StockQuantity : int
        + WarehouseLocation : string
    }
}

' ==================== NOTIFICATION ====================
package "Notification" {
    class Notification {
        + Id : int
        + ProfileId : int
        + Title : string
        + Message : string
        + IsRead : bool
        + IsAlert : bool
    }
}

' ==================== COMMUNITY ====================
package "Community" {
    class CommunityProfile {
        + Id : int
        + ProfileId : string
        + Nickname : string
        + ReputationScore : int
        + PublicBio : string
        + VisibilityStatus : VisibilityStatus
    }
    class Comment {
        + Id : int
        + AuthorProfileId : string
        + TargetProfileId : string
        + Content : string
        + Rating : int
    }
    enum VisibilityStatus {
        Public
        Private
        Hidden
    }
}

' ==================== ANALYTICS ====================
package "Analytics" {
    class Report {
        + Id : int
        + DeviceId : int
        + GeneratedAt : DateTimeOffset
        + MeanValue : double
        + Variance : double
        + StandardDeviation : double
        + TechnicalInterpretation : string
    }
}

' ==================== RELATIONSHIPS ===================
User --> Email
User ..|> IAuditableEntity
User --> Profile

Profile ..|> IAuditableEntity
Profile --> Field
Profile --> Order
Profile --> Notification
Profile --> CommunityProfile

Field ..|> IAuditableEntity
Device ..|> IAuditableEntity
Field --> Device

Order ..|> IAuditableEntity
Product ..|> IAuditableEntity
Order --> OrderStatus
Order --> PaymentMethod
Product --> Order
Product --> Inventory

Inventory ..|> IAuditableEntity

Notification ..|> IAuditableEntity

CommunityProfile ..|> IAuditableEntity
Comment ..|> IAuditableEntity
CommunityProfile --> VisibilityStatus
CommunityProfile --> Comment

Report ..|> IAuditableEntity
Device --> Report

@enduml
```