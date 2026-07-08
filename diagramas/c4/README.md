# Modelado C4
Espacio para los diagramas C4 Model de Freisser Arce.

# Modelo C4 - Documentación Arquitectónica

Este módulo contiene la representación del sistema utilizando el Modelo C4 (Niveles 1 y 2) para describir el contexto y la distribución de contenedores.

---

## 1. Modelo C4 - Contexto (Nivel 1)
Este diagrama define los límites del sistema, mostrando cómo los actores principales y los servicios externos interactúan con la plataforma.

```mermaid
graph TD
    %% Definición de Nodos
    User[Usuario / Cliente]
    Admin[Administrador del Sistema]
    System[Sistema de Información TIC]
    ExtSystem[Servicios / APIs de Terceros]

    %% Relaciones
    User -->|Usa el sistema para| System
    Admin -->|Gestiona y configura| System
    System -->|Consulta / Envía datos a| ExtSystem

    %% Definición de Estilos (Clases)
    classDef azulOscuro fill:#08427B,stroke:#032F55,color:#fff;
    classDef azulClaro fill:#1168BD,stroke:#0B4E8F,color:#fff;
    classDef gris fill:#999999,stroke:#666666,color:#fff;

    %% Aplicación de Estilos
    class User,Admin azulOscuro;
    class System azulClaro;
    class ExtSystem gris;

graph TD
    %% Actores Externos
    UserCont[Usuario / Cliente]

    subgraph Sistema TIC [Límite del Sistema]
        WebApp[Aplicación Web Frontend<br>React / Angular / HTML-CSS]
        API[API Backend<br>Node.js / .NET / Spring Boot]
        DB[(Base de Datos<br>SQL Server / PostgreSQL)]
    end

    %% Relaciones de Flujo
    UserCont -->|Interactúa con la interfaz| WebApp
    WebApp -->|Consume servicios vía HTTPS/JSON| API
    API -->|Persiste y consulta datos| DB

    %% Definición de Estilos
    classDef azulOscuro fill:#08427B,stroke:#032F55,color:#fff;
    classDef contenedor fill:#438DD5,stroke:#2B659B,color:#fff;

    %% Aplicar Estilos
    class UserCont azulOscuro;
    class WebApp,API,DB contenedor;
