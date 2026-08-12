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
* **Justificación:** Se seleccionó React porque permite construir una interfaz web dinámica mediante componentes reutilizables, lo que agiliza el desarrollo y facilita el mantenimiento[cite: 5]. Frente a Angular, ofrece una curva de aprendizaje mucho menor para el equipo, y supera al HTML/CSS puro al permitir manejar eficientemente múltiples roles de usuario (estudiante, docente, administrador) e interfaces interactivas[cite: 5].

### [ADR-0002: Elección de Tecnología Backend](0002-eleccion-de-tecnologia-backend.md)
* **Decisión:** Node.js[cite: 4].
* **Alternativas consideradas:** .NET, Spring Boot[cite: 4].
* **Justificación:** Se optó por Node.js para unificar un solo lenguaje (JavaScript/TypeScript) en todo el stack, aprovechando los conocimientos del equipo y eliminando la curva de aprendizaje que requeriría aprender C# (.NET) o Java (Spring Boot)[cite: 4]. Además, cuenta con un ecosistema maduro (`npm`) para la creación rápida y ligera de APIs REST[cite: 4].

### [ADR-0003: Elección de Base de Datos](0003-eleccion-de-base-de-datos.md)
* **Decisión:** PostgreSQL[cite: 3].
* **Alternativas consideradas:** SQL Server[cite: 3].
* **Justificación:** Se eligió PostgreSQL por ser un motor relacional de código abierto que no genera costos de licenciamiento, siendo ideal para proyectos académicos[cite: 3]. Ofrece soporte robusto para transacciones ACID, integridad referencial y trazabilidad de notas sensibles, superando a SQL Server que implicaría costos operativos institucionales[cite: 3].

### [ADR-0004: Elección de Arquitectura General](0004-eleccion-de-arquitectura-general.md)
* **Decisión:** Cliente-Servidor de 3 Capas[cite: 2].
* **Alternativas consideradas:** Monolito de escritorio, Microservicios[cite: 2].
* **Justificación:** Se seleccionó este modelo para resolver la descentralización de notas (hojas de cálculo o papel) y garantizar el acceso remoto desde cualquier dispositivo[cite: 2]. Permite una clara separación de responsabilidades (Presentación, Lógica y Datos)[cite: 2]. Es mucho más simple de desplegar y mantener que una arquitectura de microservicios, y supera a la aplicación de escritorio al brindar acceso web continuo[cite: 2].

---

## Documentación Detallada de Decisiones (ADRs)

### ADR-0001: Elección de Tecnología Frontend
* **Estado:** Aceptado[cite: 5]
* **Contexto:** El Sistema de Gestión y Control de Notas Estudiantiles (SGCE) requiere una interfaz accesible vía web desde cualquier dispositivo para reducir la dependencia de equipos físicos[cite: 5].
* **Consecuencias Positivas:**
  * Desarrollo ágil e incremental mediante componentes reutilizables[cite: 5].
  * Gran ecosistema de librerías y amplio soporte de la comunidad[cite: 5].
* **Riesgos y Mitigaciones:**
  * Requiere configurar herramientas adicionales de empaquetado y estado, lo cual se mitiga usando configuraciones estándar del ecosistema[cite: 5].

### ADR-0002: Elección de Tecnología Backend
* **Estado:** Aceptado[cite: 4]
* **Contexto:** Se necesita una API backend que garantice la disponibilidad, consistencia e integridad en el registro y consulta de notas[cite: 4].
* **Consecuencias Positivas:**
  * Reducción significativa de la curva de aprendizaje al compartir lenguaje con el frontend[cite: 4].
  * Acceso a múltiples librerías para autenticación, validación y conexión a base de datos[cite: 4].
* **Riesgos y Mitigaciones:**
  * Al ser de tipado dinámico, se deben seguir buenas prácticas de validación de datos o incorporar TypeScript para evitar errores en tiempo de ejecución[cite: 4].

### ADR-0003: Elección de Base de Datos
* **Estado:** Aceptado[cite: 3]
* **Contexto:** La información de calificaciones es sensible y exige estricta trazabilidad e integridad ante modificaciones[cite: 3].
* **Consecuencias Positivas:**
  * Cero costos de licencia[cite: 3].
  * Integración nativa y fluida con entornos Node.js[cite: 3].
  * Excelente manejo de consistencia y transacciones concurrentes[cite: 3].
* **Riesgos y Mitigaciones:**
  * Curva de adaptación con herramientas como `pgAdmin` o `psql`, mitigada mediante el uso de ORMs o clientes SQL estándar[cite: 3].

### ADR-0004: Elección de Arquitectura General
* **Estado:** Aceptado[cite: 2]
* **Contexto:** Centralizar la gestión académica para estudiantes, docentes y administradores en una única plataforma[cite: 2].
* **Consecuencias Positivas:**
  * Estructura clara y mantenible para el tamaño del equipo[cite: 2].
  * Garantiza la centralización de los datos y facilita la trazabilidad de operaciones[cite: 2].
* **Riesgos y Mitigaciones:**
  * Posee menor escalabilidad horizontal frente a microservicios, lo cual es un riesgo aceptable dado el alcance actual del proyecto[cite: 2].