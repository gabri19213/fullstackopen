## Ejercicio 0.6
sequenceDiagram
    participant browser
    participant server

    Note right of browser: El usuario escribe una nota y presiona "Save"

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: El servidor recibe la nueva nota en formato JSON
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: El navegador actualiza la lista de notas sin recargar la página
