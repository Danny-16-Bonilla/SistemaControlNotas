```text
## 2. Modelo C4 - Diagrama de Contenedores (Nivel 2)

```mermaid
graph TD
    UserCont[Usuario / Cliente]

    subgraph Sistema TIC [Límite del Sistema]
        WebApp[Aplicación Web Frontend<br>React / Angular / HTML-CSS]
        API[API Backend<br>Node.js / .NET / Spring Boot]
        DB[(Base de Datos<br>SQL Server / PostgreSQL)]
    end

    UserCont -->|Interactúa con la interfaz| WebApp
    WebApp -->|Consume servicios vía HTTPS/JSON| API
    API -->|Persiste y consulta datos| DB

    classDef azulOscuro fill:#08427B,stroke:#032F55,color:#fff;
    classDef contenedor fill:#438DD5,stroke:#2B659B,color:#fff;
    class UserCont azulOscuro;
    class WebApp,API,DB contenedor;
