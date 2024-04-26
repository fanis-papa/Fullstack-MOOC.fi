Exercise 0.4: 

Create a similar diagram depicting the situation where the user creates a new note on the page https://studies.cs.helsinki.fi/exampleapp/notes by writing something into the text field and clicking the Save button.

If necessary, show operations on the browser or on the server as comments on the diagram.



[![](https://mermaid.ink/img/pako:eNq1lF1P2zAUhv_KkW_XpCWttCkXXIFAUwfT0t1ApungnDSmjZPZx4Wp6n_faZ0hTROaOiA3js_n49cfW6W7ilSuPP0IZDWdGVw6bEsL8t257sGTS05P38mwIZfD5-tiAQ1z7_Px2HOoDPlU-7ShtTd2ZdLajOkR235N2PdjSw_fbccU66Fms0EmiNWiMf4n0iQZ-uUwnWRQMHLw8PXLHBxVxpHmmFDRX3Wexb04P4pWSP2RqJeLT3M463Royf4L8JUwWzRW3MeS_pn2dioe-tz_F93983BRvyvZIXBm2TB0NTwlLxr6PQHP6NgDPZIObOwSWJwfcYOFdqZn2B94sSFDTawb8jGguL6C2nXtYfbKilTIKGvr7JGaPOXB7baUm2p5f8ZUDqWaI9yQNViqkcwkkKI9m2SzZDJLsuniZJZnWT75kE7fz25KBbsRpGkK314ucdR2UE7jen2HegV1sFJRYA_iOrIVuRgy3Cs1Ui052ehKHpztvl-pxN0O6BW6ValKu5M4DNwVP61WObtAIxX6_RKHxykad78Am_uhxw?type=png)](https://mermaid.live/edit#pako:eNq1lF1P2zAUhv_KkW_XpCWttCkXXIFAUwfT0t1ApungnDSmjZPZx4Wp6n_faZ0hTROaOiA3js_n49cfW6W7ilSuPP0IZDWdGVw6bEsL8t257sGTS05P38mwIZfD5-tiAQ1z7_Px2HOoDPlU-7ShtTd2ZdLajOkR235N2PdjSw_fbccU66Fms0EmiNWiMf4n0iQZ-uUwnWRQMHLw8PXLHBxVxpHmmFDRX3Wexb04P4pWSP2RqJeLT3M463Royf4L8JUwWzRW3MeS_pn2dioe-tz_F93983BRvyvZIXBm2TB0NTwlLxr6PQHP6NgDPZIObOwSWJwfcYOFdqZn2B94sSFDTawb8jGguL6C2nXtYfbKilTIKGvr7JGaPOXB7baUm2p5f8ZUDqWaI9yQNViqkcwkkKI9m2SzZDJLsuniZJZnWT75kE7fz25KBbsRpGkK314ucdR2UE7jen2HegV1sFJRYA_iOrIVuRgy3Cs1Ui052ehKHpztvl-pxN0O6BW6ValKu5M4DNwVP61WObtAIxX6_RKHxykad78Am_uhxw)



    browser->>+server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>-browser: 302 Status URL redirect
    deactivate server

    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>-browser: HTML Document
    deactivate server

    
    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>-browser: main.css
    deactivate server

    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>-browser: main.js
    deactivate server
    
    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>-browser: data.json [{"content": "La Zenia", "date": "2024-04-23T14:22:08.374Z" }, ... ]
    deactivate server
    
    Note right of browser: The browser executes the callback function that renders the notes
