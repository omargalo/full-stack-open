# New note in Single page app diagram

```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    Note over User, Browser: User is on the SPA version of the notes app

    User->>Browser: Input note and click Save
    activate Browser
    Note right of Browser: Browser captures note data

    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Note over Browser, Server: Request contains note data

    activate Server
    Note left of Server: Server processes and saves the new note

    Server-->>Browser: Confirmation response with note data
    deactivate Server

    Note right of Browser: Browser updates the notes list dynamically

    deactivate Browser
```
