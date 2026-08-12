# Registros de Decisión de Arquitectura (ADR) Julian Brenes

\# Registros de Decisión de Arquitectura (ADR)



Responsable: Julián Brenes



Este directorio contiene las decisiones arquitectónicas del proyecto SGCE.



| ADR | Título | Estado |

|-----|--------|--------|

| \[0001](0001-eleccion-de-arquitectura-frontend.md) | Elección de tecnología frontend | Aceptado |

| \[0002](0002-eleccion-de-tecnologia-backend.md) | Elección de tecnología backend | Aceptado |

| \[0003](0003-eleccion-de-base-de-datos.md) | Elección de base de datos | Aceptado |

| \[0004](0004-eleccion-de-arquitectura-general.md) | Elección de arquitectura general | Aceptado |

# Registros de Decisión de Arquitectura (ADR)

Responsable: Julián Brenes

Este directorio contiene las decisiones arquitectónicas del proyecto SGCE.

| ADR | Título | Estado |
| --- | --- | --- |
| [0001](0001-eleccion-de-arquitectura-frontend.md) | Elección de tecnología frontend | Aceptado |
| [0002](0002-eleccion-de-tecnologia-backend.md) | Elección de tecnología backend | Aceptado |
| [0003](0003-eleccion-de-base-de-datos.md) | Elección de base de datos | Aceptado |
| [0004](0004-eleccion-de-arquitectura-general.md) | Elección de arquitectura general | Aceptado |

---

## Resumen del Stack Tecnológico

### [ADR-0001: Elección de Tecnología Frontend](0001-eleccion-de-arquitectura-frontend.md)
* **Decisión:** React[cite: 5].
* **Alternativas consideradas:** Angular, HTML/CSS puro[cite: 5].
* **Justificación:** Desarrollo ágil mediante componentes reutilizables y amplio soporte comunitario[cite: 5].

### [ADR-0002: Elección de Tecnología Backend](0002-eleccion-de-tecnologia-backend.md)
* **Decisión:** Node.js[cite: 4].
* **Alternativas consideradas:** .NET, Spring Boot[cite: 4].
* **Justificación:** Permite unificar JavaScript/TypeScript en todo el stack y aprovecha el ecosistema `npm`[cite: 4].

### [ADR-0003: Elección de Base de Datos](0003-eleccion-de-base-de-datos.md)
* **Decisión:** PostgreSQL[cite: 3].
* **Alternativas consideradas:** SQL Server[cite: 3].
* **Justificación:** Motor relacional robusto, de código abierto (sin costos de licencia) y con alta integridad de datos[cite: 3].

### [ADR-0004: Elección de Arquitectura General](0004-eleccion-de-arquitectura-general.md)
* **Decisión:** Cliente-Servidor de 3 Capas[cite: 2].
* **Alternativas consideradas:** Monolito de escritorio, Microservicios[cite: 2].
* **Justificación:** Mantenimiento y despliegue simple, ideal para el alcance del equipo y la centralización de datos[cite: 2].
