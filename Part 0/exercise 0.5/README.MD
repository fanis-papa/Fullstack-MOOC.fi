Exercise 0.5
Create a similar diagram depicting the situation where the user creates a new note on the page https://studies.cs.helsinki.fi/exampleapp/notes by writing something into the text field and clicking the Save button.

If necessary, show operations on the browser or on the server as comments on the diagram.



[![](https://mermaid.ink/img/pako:eNqtVE1v2zAM_SuEroudNAmKQYeeWmwY2u6QnDrtwFl0rDWWXIlOOwT576WjrNiwBWiA-CKLfI96_JC2qgqWlFaJnnryFV07XEVsjQf5fsTwnCgWV1cfZNlQ1PDpZgkNc5f0eJy4t45SWaWyoXVy_tGVtRvTC7bdmrDrxqnDHAkrdhtkghwnG_N_IeGLw0kaPi_vbuE6VH1LnjPM0j_sM8lr0XlxpxM1_k07Ku98NSx_nirxT9J_BRp_H8QQ3aphCDW8MZcN_d5AYoycgF6o6tn5FbA4v-AGF1V0HcMwO2JDPhqtJq4aSpm4-HoPdQztfnfmVlrkIePgTyzUGw--bY1cBs_D3CkNRonKROAlsVSWpXQ9Bk9GjcQlLMqg6WQ6LybzYjpfXlzq2Uc9uygvJ7MHo2A3goH3_WgX8pC8ow-5AYcyRrIRnwdWgrr3ElTEcxC7t4IVSAuDRaAdrsh4NVItRRlaK_d8Oxy7z609ZGAxPhpl_E5w2HNY_PKV0hx7Gqm-GzI9vAlK17hOYiXrOMS7_HDs34_dK0Tdenk?type=png)](https://mermaid.live/edit#pako:eNqtVE1v2zAM_SuEroudNAmKQYeeWmwY2u6QnDrtwFl0rDWWXIlOOwT576WjrNiwBWiA-CKLfI96_JC2qgqWlFaJnnryFV07XEVsjQf5fsTwnCgWV1cfZNlQ1PDpZgkNc5f0eJy4t45SWaWyoXVy_tGVtRvTC7bdmrDrxqnDHAkrdhtkghwnG_N_IeGLw0kaPi_vbuE6VH1LnjPM0j_sM8lr0XlxpxM1_k07Ku98NSx_nirxT9J_BRp_H8QQ3aphCDW8MZcN_d5AYoycgF6o6tn5FbA4v-AGF1V0HcMwO2JDPhqtJq4aSpm4-HoPdQztfnfmVlrkIePgTyzUGw--bY1cBs_D3CkNRonKROAlsVSWpXQ9Bk9GjcQlLMqg6WQ6LybzYjpfXlzq2Uc9uygvJ7MHo2A3goH3_WgX8pC8ow-5AYcyRrIRnwdWgrr3ElTEcxC7t4IVSAuDRaAdrsh4NVItRRlaK_d8Oxy7z609ZGAxPhpl_E5w2HNY_PKV0hx7Gqm-GzI9vAlK17hOYiXrOMS7_HDs34_dK0Tdenk)


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

    %%{`The browser starts executing the JavaScript code that fetches the JSON from the server`}%%
    

    browser->>+server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>-browser: data.json [{"content": "these notes... marone", "date": "2024-04-24T16:38:31.603Z" }, ... ]
    deactivate server
    
    %%{`The browser executes the redrawNotes function to render them on the page`}%%
   
