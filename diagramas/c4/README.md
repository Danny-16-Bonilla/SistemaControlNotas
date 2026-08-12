# Modelo C4

## Descripción

El modelo **C4** es una metodología utilizada para representar la arquitectura de un sistema mediante diferentes niveles de abstracción.

Cada nivel permite observar el sistema desde una perspectiva diferente, comenzando por una visión general y avanzando progresivamente hacia los componentes internos.

Los principales niveles del modelo C4 son:

1. **Contexto del sistema**
2. **Contenedores**
3. **Componentes**
4. **Código**

---

## Nivel 1: Contexto del Sistema

El **Nivel 1 – Contexto** proporciona una visión general del sistema y permite identificar las personas, organizaciones o sistemas externos que interactúan con él.

En este nivel no se muestran detalles internos como bases de datos, APIs internas, servidores o componentes del software.

El objetivo principal es responder:

> **¿Quién utiliza el sistema y con qué sistemas externos se relaciona?**

---

## Elementos principales

| Elemento | Tipo | Descripción |
|---|---|---|
| Usuario / Cliente | Persona | Utiliza el sistema para realizar las operaciones disponibles. |
| Administrador del Sistema | Persona | Gestiona y configura diferentes aspectos del sistema. |
| Sistema de Información TIC | Sistema | Representa el sistema principal que se está desarrollando. |
| Servicios / APIs de Terceros | Sistema externo | Representa servicios externos con los que el sistema intercambia información. |

---

## Relaciones entre los elementos

### Usuario / Cliente → Sistema

El **Usuario / Cliente** interactúa directamente con el **Sistema de Información TIC** para utilizar las funcionalidades disponibles.

**Relación:** `Usa el sistema para`

### Administrador → Sistema

El **Administrador del Sistema** interactúa con el sistema para realizar tareas de gestión, configuración y administración.

**Relación:** `Gestiona y configura`

### Sistema → Servicios / APIs de Terceros

El **Sistema de Información TIC** se comunica con servicios externos para consultar información o enviar datos cuando las funcionalidades del sistema lo requieren.

**Relación:** `Consulta / Envía datos a`

---

## Interpretación del diagrama

El diagrama presenta al **Sistema de Información TIC** como el elemento central de la arquitectura.

Los usuarios y administradores interactúan con el sistema de acuerdo con sus responsabilidades, mientras que el sistema puede comunicarse con servicios o APIs externas para obtener o enviar información.

De esta manera, el diagrama permite identificar claramente:

- Los usuarios que interactúan con el sistema.
- El sistema principal.
- Las funciones generales de interacción.
- Los sistemas externos relacionados.
- El intercambio de información con servicios de terceros.

---

## Alcance del Nivel 1

El diagrama de contexto se mantiene en un nivel de abstracción alto. Por esta razón, **no se representan detalles técnicos internos** del sistema.

Los siguientes elementos corresponden a niveles posteriores del modelo C4:

- Aplicación Web Frontend.
- API Backend.
- Base de datos.
- Servicios internos.
- Componentes de software.
- Clases y código fuente.

Estos elementos serán detallados principalmente en el **Nivel 2 – Contenedores** y en los niveles posteriores.

---

## Próximo nivel

El siguiente nivel corresponde al **Nivel 2 – Contenedores**.

En este nivel se descompone el **Sistema de Información TIC** en sus principales contenedores tecnológicos, mostrando cómo se relacionan entre sí la aplicación web, el backend, la base de datos y los servicios externos.

---

## Código del diagrama

El siguiente código Mermaid permite generar el diagrama C4 de contexto:

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
