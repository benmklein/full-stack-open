
```mermaid
sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: the HTML Document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the CSS File
    deactivate server


    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: the JS File
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: The JSON objects
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes
    
```
    [![](https://mermaid.ink/img/pako:eNq1VE1P3DAQ_SuWz5B0d9sFcuBSaKuqhUrZYyQ0sSeJIbFTe7yAVvvfOyHZlSpUEB_NwbLfjN57nnFmI5XTKDMZ8HdEq_DMQO2hK6zgrwdPRpkeLInSu9uA_nGAwfUOH9cp9fD0dIxl4tdlvhINUR-yNA0UtcGQqJA02AZjb0xSmRTvoOtbhL5PLd5eWUc40oEiswbCv5Q0PoL_Jf71_EXarBueEB73h8w_KWWCGhTfVj9_iDOnYoeW_rPFDozl8Ctcfs5z8cW0-ITBd7R4_QqH3581OAQuuEnCm7oh4SqxJ1gxwXQQgfiNBoF3qCIZW4_ssIZcedOTGN49Y0CiQlINhkn-8kJU3nUPp_dtmwYCromzL6vKamfLldeoKLy9NGNNphsraNsS1I2oomVGZ8eieLQa_Zjy8EvIA9mh575qnhabQauQHOywkBlvNVYQWypkYbecCpFcfm-VzMhHPJCx59vvhovMKmjDHj3Xhpzfg60DVpbZRtJ9P4ym2gRiSuVsZeoBj75leFf4IZzUhppYJsp1aTC64dY365Nlupwvj2G-wOXRAj4tFlqVs5Pjav5xVumjD7M5yO12-wed7cAO?type=png)](https://mermaid.live/edit#pako:eNq1VE1P3DAQ_SuWz5B0d9sFcuBSaKuqhUrZYyQ0sSeJIbFTe7yAVvvfOyHZlSpUEB_NwbLfjN57nnFmI5XTKDMZ8HdEq_DMQO2hK6zgrwdPRpkeLInSu9uA_nGAwfUOH9cp9fD0dIxl4tdlvhINUR-yNA0UtcGQqJA02AZjb0xSmRTvoOtbhL5PLd5eWUc40oEiswbCv5Q0PoL_Jf71_EXarBueEB73h8w_KWWCGhTfVj9_iDOnYoeW_rPFDozl8Ctcfs5z8cW0-ITBd7R4_QqH3581OAQuuEnCm7oh4SqxJ1gxwXQQgfiNBoF3qCIZW4_ssIZcedOTGN49Y0CiQlINhkn-8kJU3nUPp_dtmwYCromzL6vKamfLldeoKLy9NGNNphsraNsS1I2oomVGZ8eieLQa_Zjy8EvIA9mh575qnhabQauQHOywkBlvNVYQWypkYbecCpFcfm-VzMhHPJCx59vvhovMKmjDHj3Xhpzfg60DVpbZRtJ9P4ym2gRiSuVsZeoBj75leFf4IZzUhppYJsp1aTC64dY365Nlupwvj2G-wOXRAj4tFlqVs5Pjav5xVumjD7M5yO12-wed7cAO)
