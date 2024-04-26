exercise 0.5: 

Single page app diagram

Create a diagram depicting the situation where the user goes to the single-page app version of the notes app at https://studies.cs.helsinki.fi/exampleapp/spa.



[![](https://mermaid.ink/img/pako:eNqtVMFuEzEQ_ZWRr2Q3aRJVyIeeikCIlkNyAnMY7NmsadZe7Nm0KMq_MxuHCgSViJS9eD1-b_zmeey9stGR0irT94GCpVuPm4SdCSDf1xQfM6Xq5uaVDDtKGt6-WUPL3Gc9nWYenKdc21y3tM0-PPi68VN6wq7fEvb9NPdYMqFlv0MmKHlKsPxXkr467aTh3fruA9xGO3QUuMAc_cW-kLwOfZDlfKbGP2kvyruch_W3cyX-TvqnQBPuowSS37QMsYFn5rqlXxPIjIkz0BPZgX3YAMvie9zhyibfM4y9IzFkaIhtS7kAVh_voUmxO84ufGQOeawshjMNeebB572Rpg889pfSYJSozARB7Mh1XcvpphjIqIksCYsKaD6bL6vZspov11fXevFaL67q69nik1FwmMDI-_Ki26UZ_sPvYvTJxkQu4ePIytAMQZKKeI4SD06wAulgjAi0xw2ZoCaqoyTN6eQ-78dtj7V1pwocpgejTDgIDgeOqx_BKs1poIka-rHS091XusFtlig5zzHdlQfi-E4cfgKMDXGI?type=png)](https://mermaid.live/edit#pako:eNqtVMFuEzEQ_ZWRr2Q3aRJVyIeeikCIlkNyAnMY7NmsadZe7Nm0KMq_MxuHCgSViJS9eD1-b_zmeey9stGR0irT94GCpVuPm4SdCSDf1xQfM6Xq5uaVDDtKGt6-WUPL3Gc9nWYenKdc21y3tM0-PPi68VN6wq7fEvb9NPdYMqFlv0MmKHlKsPxXkr467aTh3fruA9xGO3QUuMAc_cW-kLwOfZDlfKbGP2kvyruch_W3cyX-TvqnQBPuowSS37QMsYFn5rqlXxPIjIkz0BPZgX3YAMvie9zhyibfM4y9IzFkaIhtS7kAVh_voUmxO84ufGQOeawshjMNeebB572Rpg889pfSYJSozARB7Mh1XcvpphjIqIksCYsKaD6bL6vZspov11fXevFaL67q69nik1FwmMDI-_Ki26UZ_sPvYvTJxkQu4ePIytAMQZKKeI4SD06wAulgjAi0xw2ZoCaqoyTN6eQ-78dtj7V1pwocpgejTDgIDgeOqx_BKs1poIka-rHS091XusFtlig5zzHdlQfi-E4cfgKMDXGI)


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
   
