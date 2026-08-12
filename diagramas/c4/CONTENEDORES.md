# Modelo C4 — Nivel 2: Contenedores

## Visión General

El **Sistema de Información TIC** se compone de tres contenedores principales organizados en una arquitectura cliente-servidor de tres capas.

```mermaid
graph TD
    UserCont["Usuario / Cliente"]

    subgraph SistemaTIC["Sistema de Información TIC"]
        WebApp["Aplicación Web Frontend<br>(React / Angular)"]
        API["API Backend<br>(Node.js / .NET / Spring Boot)"]
        DB[("Base de Datos<br>(SQL Server / PostgreSQL)")]
    end

    UserCont -->|"HTTPS"| WebApp
    WebApp -->|"HTTPS / JSON"| API
    API -->|"SQL / TCP"| DB

    classDef actor fill:#08427B,stroke:#032F55,color:#fff;
    classDef container fill:#438DD5,stroke:#2B659B,color:#fff;

    class UserCont actor;
    class WebApp,API,DB container;
