El modelo C4 es una metodología que permite representar un sistema mediante diferentes niveles de diagramas, comenzando desde una visión general y avanzando progresivamente hacia los componentes internos del sistema.

En este caso, el primer diagrama corresponde al C4 – Modelo de Contexto, Nivel 1. Su objetivo principal es mostrar el sistema desde una perspectiva general, identificando a las personas que interactúan con él y los sistemas externos con los que tiene comunicación.

En el diagrama se identifican cuatro elementos principales. El primero es el Usuario o Cliente, quien utiliza el sistema para realizar las diferentes funciones que este ofrece. El segundo es el Administrador del Sistema, encargado de gestionar, configurar y supervisar el funcionamiento del sistema.

El tercer elemento es el Sistema de Información TIC, que representa el sistema que se está desarrollando. Este constituye el elemento central del diagrama, ya que tanto los usuarios como los administradores interactúan directamente con él.

Finalmente, se encuentran los Servicios o APIs de Terceros. Estos representan sistemas externos que pueden proporcionar información o servicios que el sistema necesita. La comunicación entre el sistema y estos servicios puede consistir en consultar información o enviar datos.

Las flechas del diagrama representan las relaciones entre los diferentes elementos. Por ejemplo, la relación entre el Usuario y el Sistema indica que el usuario utiliza el sistema, mientras que la relación del Administrador representa las actividades de gestión y configuración. Por otro lado, la conexión entre el Sistema de Información TIC y los servicios externos representa el intercambio de información con otras plataformas.

El diagrama fue elaborado utilizando Mermaid, una herramienta que permite crear diagramas mediante código. Esto facilita que el diagrama pueda mantenerse y modificarse fácilmente dentro de plataformas como GitHub.

En conclusión, este primer nivel del modelo C4 permite obtener una visión general de la arquitectura del sistema, sin entrar todavía en detalles sobre cómo está programado internamente. Su función es identificar claramente quién utiliza el sistema, cuál es el sistema principal y con qué elementos externos se comunica

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

