```mermaid
classDiagram
  direction LR
  class Client
  class Facade {
    -linksToSubsystemObjects
    -optionalAdditionalFacade
    +subsystemOperation()
  }
  class AdditionalFacade {
    +anotherOperation()
  }
  Client --> Facade
  Facade --> AdditionalFacade
```