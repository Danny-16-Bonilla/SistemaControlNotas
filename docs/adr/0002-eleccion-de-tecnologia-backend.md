\# ADR-0002: Elección de tecnología backend



\## Estado

Aceptado



\## Contexto

El sistema necesita una API backend que garantice la integridad, consistencia

y disponibilidad de la información académica, permitiendo el registro,

consulta y modificación segura de calificaciones. El diagrama C4 plantea tres

alternativas: Node.js, .NET o Spring Boot.



\## Decisión

Se selecciona Node.js como tecnología de backend.



\## Alternativas consideradas

\- Node.js: mismo lenguaje (JavaScript/TypeScript) que el frontend en

&#x20; React, lo que facilita compartir conocimiento entre el equipo; ligero y

&#x20; con gran cantidad de librerías para APIs REST.

\- .NET: robusto y con tipado fuerte, buen rendimiento, pero requiere

&#x20; conocimientos de C# que el equipo no maneja actualmente.

\- Spring Boot: maduro y usado en entornos empresariales, pero con mayor

&#x20; complejidad de configuración inicial (Java + Spring).



\## Consecuencias

\### Positivas

\- Un solo lenguaje (JavaScript/TypeScript) en todo el stack, reduce la curva

&#x20; de aprendizaje del equipo.

\- Gran cantidad de paquetes disponibles (npm) para autenticación, validación

&#x20; y conexión a bases de datos.



\### Negativas / riesgos

\- Node.js es de tipado dinámico (a menos que se use TypeScript), lo que

&#x20; puede generar errores en tiempo de ejecución si no se valida bien.

\- Requiere buenas prácticas para manejar operaciones asíncronas.



\## Referencias

\- Documento Avance #1 del proyecto, sección "Justificación Administrativa".

\- https://nodejs.org/

