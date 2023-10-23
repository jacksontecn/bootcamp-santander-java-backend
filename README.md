# Bootcamp Santander Java Backend
Java RESTful API criada para o bootcamp santander java backend 2023

## Diagrama de classes

```mermaid
classDiagram
  class User {
    -id: Long
    -name: String
    -account: Account
    -features: Feature[]
    -card: Card
    -news: News[]
  }
  class Account {
    -id: Long
    -Number: String
    -Agency: String
    -Balance: BigDecimal
    -Limit: BigDecimal
  }
  class Feature {
    -id: Long
    -icon: String
    -description: String
  }
  class Card {
    -id: Long
    -Number: String
    -Limit: BigDecimal
  }
  class News {
    -id: Long
    -icon: String
    -description: String
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News
```
