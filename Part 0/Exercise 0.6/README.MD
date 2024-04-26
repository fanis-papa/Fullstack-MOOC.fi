exercise 0.6: 

New note in Single page app diagram
Create a diagram depicting the situation where the user creates a new note using the single-page version of the app.



[![](https://mermaid.ink/img/pako:eNp9U0tv1DAQ_isjn0Dsg_YYoUogDqiiLVKWW6Rq1p5szDq28Ti7VFX_O-M4rUCC5hJ77Pn8PexHpYMh1SimnxN5TZ8tHhKOnQf59imcmdL66uqd_E6UGvh21-5gyDlys91ynowl3mjeDOTY-qPd9HZLv3CMjjDGrafzvQ-Z7jkiVNBbmUKyhyFD6J-PaODTA2hn9dH6A3SqxRN1CvJAEDxP-9FmoBP5DJaht4kMnAerh-ZVzAvhm-Y2nqHOtIeIB4I-hRESuYBGznsV47KBlrxhwKo9FaM4Qw4zZPUFdPAZC_VSE9HwYZ-uoCgHZLhu727BYEZ4UzYKn1WZ0gr6kEbMbztfOaDO9iQLC2wt1vFaUli_sGp3H3ffW7h8f_EHeUf9zP05q7ZyM4G4UBHqHIMX52wepKqncWYi1v6YRJH1xmo5nCv5PGB-kTMrGUTKnsgDT1oT95NzEloi6TGAAmzz0uuCANngN7ATgHLFAB0HiMmWLBBGYi5BLC6KKxwc1WbxZC4aSc6FKApkFxMt98fQP136T3zXeELWyUYp-xl2WRI3vKHEf0lcVTklSFwilJUvu5uvQI6KXRu1UiNJaNbIq3ksZ3dKIEa5ro0MDaZjpzr_JPtwyqF98Fo1OU20UlMsoS8vTDW9WCJVMjaHdFOf4fwan34DyF8-Zw?type=png)](https://mermaid.live/edit#pako:eNp9U0tv1DAQ_isjn0Dsg_YYoUogDqiiLVKWW6Rq1p5szDq28Ti7VFX_O-M4rUCC5hJ77Pn8PexHpYMh1SimnxN5TZ8tHhKOnQf59imcmdL66uqd_E6UGvh21-5gyDlys91ynowl3mjeDOTY-qPd9HZLv3CMjjDGrafzvQ-Z7jkiVNBbmUKyhyFD6J-PaODTA2hn9dH6A3SqxRN1CvJAEDxP-9FmoBP5DJaht4kMnAerh-ZVzAvhm-Y2nqHOtIeIB4I-hRESuYBGznsV47KBlrxhwKo9FaM4Qw4zZPUFdPAZC_VSE9HwYZ-uoCgHZLhu727BYEZ4UzYKn1WZ0gr6kEbMbztfOaDO9iQLC2wt1vFaUli_sGp3H3ffW7h8f_EHeUf9zP05q7ZyM4G4UBHqHIMX52wepKqncWYi1v6YRJH1xmo5nCv5PGB-kTMrGUTKnsgDT1oT95NzEloi6TGAAmzz0uuCANngN7ATgHLFAB0HiMmWLBBGYi5BLC6KKxwc1WbxZC4aSc6FKApkFxMt98fQP136T3zXeELWyUYp-xl2WRI3vKHEf0lcVTklSFwilJUvu5uvQI6KXRu1UiNJaNbIq3ksZ3dKIEa5ro0MDaZjpzr_JPtwyqF98Fo1OU20UlMsoS8vTDW9WCJVMjaHdFOf4fwan34DyF8-Zw)


    browser->>+server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa 
    Note right of browser: By clicking "Save" the onsubmit event is fired which:
    Note right of browser: 1: Prevents the web page from reloading
    Note right of browser: 2: Sends a POST request to the server containg the new <br> note as JSON data (content, date, format)

    activate server
    server-->>-browser: STATUS 201
    Note left of server: Server does not respond with document, it just indicates <br> that the new note has been succesfully created and its <br> location. The code also prints a message to the console <br> for the developer to see 
    deactivate server
    Note right of browser: Javascript on the browser renders the new note, creating a <br> new HTML element.