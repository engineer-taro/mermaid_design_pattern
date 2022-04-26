```mermaid
classDiagram
    direction BT
    class PrototypeRegistry{
        - Prototype[] items
        +addItem(id: string, p: Prototype)
        +getById(id: string) Prototype
        +getByColor(color: string) Prototype
    }

    class Prototype{
        <<interface>>
        +getColor() string
        +clone() Prototype
    }

    class Button{
        -x, y, color
        +Button(x, y, color)
        +Button(prototype)
        +getColor() string
        +clone() Prototype
    }

    class Client

    PrototypeRegistry o--> Prototype
    Button ..|> Prototype
    
    Client --> PrototypeRegistry : use 
```