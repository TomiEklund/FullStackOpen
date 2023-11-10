```mermaid
sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Selain lähettää palvelimelle muistiinpanon JSON-muotoisena datana ja aikaleiman
    deactivate server
    
    browser->>server: https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created. Uusi muistiinpano on luotu.
    deactivate server
