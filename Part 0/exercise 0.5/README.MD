    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>-browser: HTML Document
    deactivate server

    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>-browser: main.css
    deactivate server

    
    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->>-browser: spa.js
    deactivate server


    Note right of browser: The browser starts executing the JavaScript code that
    Note right of browser: fetches the JSON from the server

    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>-browser: data.json [{"content": "these notes... marone", "date": "2024-04-24T16:38:31.603Z" }, ... ]
    deactivate server
    
    Note right of browser: The browser executes the redrawNotes function to render them on the page
