\# ADR-0004: Elección de arquitectura general (cliente-servidor)



\## Estado

Aceptado



\## Contexto

El sistema debe centralizar el registro, seguimiento y reporte de

calificaciones para múltiples tipos de usuario (estudiantes, docentes,

administradores), evitando los problemas actuales de registros

descentralizados en hojas de cálculo o papel.



\## Decisión

Se adopta una arquitectura cliente-servidor de tres capas

(presentación - lógica de negocio - datos), en lugar de un enfoque

monolítico de escritorio o una arquitectura de microservicios.



\## Alternativas consideradas

\- Cliente-servidor de 3 capas: separa claramente la interfaz (React),

&#x20; la API (Node.js) y la base de datos (PostgreSQL); adecuada para el tamaño

&#x20; y alcance del proyecto.

\- Microservicios: mayor escalabilidad, pero complejidad de

&#x20; infraestructura innecesaria para el alcance actual del proyecto.

\- Aplicación de escritorio monolítica: descartada porque no cumple con

&#x20; el requisito de acceso remoto desde cualquier dispositivo.



\## Consecuencias

\### Positivas

\- Arquitectura simple de mantener y desplegar para el tamaño del equipo.

\- Facilita la trazabilidad y centralización de la información.



\### Negativas / riesgos

\- Menor escalabilidad horizontal comparado con microservicios (aceptable

&#x20; para el alcance actual del proyecto).



\## Referencias

\- Documento Avance #1, sección "Contexto del Proyecto".

