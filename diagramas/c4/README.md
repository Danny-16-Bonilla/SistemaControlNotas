# Modelado C4
Espacio para los diagramas C4 Model de Freisser Arce.

---

## 1. Modelo C4 - Contexto (Nivel 1)

```mermaid
graph TD
    User[Usuario / Cliente]
    Admin[Administrador del Sistema]
    System[Sistema de Información TIC]
    ExtSystem[Servicios / APIs de Terceros]

    User -->|Usa el sistema para| System
    Admin -->|Gestiona y configura| System
    System -->|Consulta / Envía datos a| ExtSystem

    classDef azulOscuro fill:#08427B,stroke:#032F55,color:#fff;
    classDef azulClaro fill:#1168BD,stroke:#0B4E8F,color:#fff;
    classDef gris fill:#999999,stroke:#666666,color:#fff;
    class User,Admin azulOscuro;
    class System azulClaro;
    class ExtSystem gris;
