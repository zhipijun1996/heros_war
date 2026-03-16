```mermaid
flowchart TB
    Start -->|"Request Token"| TokenService[Token Service]
    TokenService -->|"Generate Token"| TokenGenerated[Token Generated]
    TokenGenerated -->|"Token Valid?"| TokenValidation{Token Validation}
    TokenValidation -- Yes -->|"Proceed"| ActionService[Action Service]
    TokenValidation -- No -->|"Reject"| Rejection[Rejection]
    ActionService -->|"Finish Process"| End[End]
```
