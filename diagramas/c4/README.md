Modelo C4
Descripción

El modelo C4 es una metodología utilizada para representar y documentar la arquitectura de un sistema de software. Su objetivo es mostrar de manera clara cómo está compuesto el sistema, quién interactúa con él y cómo se relacionan sus diferentes elementos.

El modelo permite representar la arquitectura utilizando diferentes niveles de detalle, comenzando con una visión general del sistema y avanzando progresivamente hacia sus componentes internos.

Nivel 1: Modelo de Contexto
Descripción

El Nivel 1: Modelo de Contexto proporciona una visión general del sistema. En este nivel se identifican los principales usuarios que interactúan con el sistema y los sistemas o servicios externos que tienen alguna relación con él.

El objetivo principal es comprender qué personas utilizan el sistema, cuál es el sistema principal y con qué elementos externos se comunica.

Elementos principales
Usuario / Cliente: Persona que utiliza el sistema para realizar diferentes operaciones.
Administrador del Sistema: Persona encargada de gestionar, configurar y supervisar el sistema.
Sistema de Información TIC: Sistema principal que proporciona las funcionalidades necesarias para los usuarios.
Servicios / APIs de Terceros: Sistemas externos que pueden proporcionar información o servicios al sistema.
Relaciones

El Usuario / Cliente utiliza el Sistema de Información TIC para acceder a sus diferentes funcionalidades.

El Administrador del Sistema interactúa con el sistema para realizar tareas de gestión, configuración y administración.

El Sistema de Información TIC puede comunicarse con Servicios o APIs de Terceros para consultar información o enviar datos.

Comunicación

Las principales relaciones pueden resumirse de la siguiente manera:

Usuario → Sistema: utiliza las funcionalidades disponibles.
Administrador → Sistema: gestiona y configura el sistema.
Sistema → Servicios externos: consulta o envía información.
Interpretación

Este nivel permite comprender el sistema desde una perspectiva general, sin entrar todavía en detalles sobre su funcionamiento interno. Es útil para identificar los actores y elementos externos que forman parte del entorno del sistema.

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

