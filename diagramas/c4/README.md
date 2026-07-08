```mermaid
graph TD

User[Usuario / Cliente]
Admin[Administrador]
System[Sistema de Información TIC]
ExtSystem[Servicios / APIs de Terceros]

User -->|Usa el sistema| System
Admin -->|Administra| System
System -->|Consulta APIs| ExtSystem

style User fill:#08427B,stroke:#032F55,color:#fff
style Admin fill:#08427B,stroke:#032F55,color:#fff
style System fill:#1168BD,stroke:#0B4E8F,color:#fff
style ExtSystem fill:#999999,stroke:#666666,color:#fff
```
