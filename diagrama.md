```mermaid
graph TD;
    A[Abrir la página de notas] -->|GET HTML| B((Navegador));
    B -->|HTML document| C((Navegador));
    B -->|GET main.css| D((Navegador));
    D -->|the css file| E((Navegador));
    B -->|GET main.js| F((Navegador));
    F -->|the JavaScript file| G((Navegador));
    G -->|GET data.json| H((Navegador));
    H -->|JSON data| I((Navegador));
    I -->|Render notas| J((Navegador));
    J -->|Usuario escribe nueva nota y hace clic en "Save"| K((Navegador));
    K -->|HTTP POST /new_note| L((Servidor));
    L -->|302 Redirect| M((Navegador));
    M -->|GET /notes| N((Navegador));
    N -->|HTML document| O((Navegador));
    M -->|GET main.css| P((Navegador));
    P -->|the css file| Q((Navegador));
    M -->|GET main.js| R((Navegador));
    R -->|the JavaScript file| S((Navegador));
    M -->|GET data.json| T((Navegador));
    T -->|Updated JSON data| U((Navegador));
    U -->|Render updated notas| V((Navegador));
```
