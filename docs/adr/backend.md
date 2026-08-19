# ADR-0002: Elección de tecnología backend

## Estado

Aceptado

## Contexto

El sistema necesita una API backend que garantice la integridad, consistencia

y disponibilidad de la información académica, permitiendo el registro,

consulta y modificación segura de calificaciones. El diagrama C4 plantea tres

alternativas: Node.js, .NET o Spring Boot.

## Decisión

Se selecciona Node.js como tecnología de backend.

## Alternativas consideradas

- Node.js: mismo lenguaje (JavaScript/TypeScript) que el frontend en

React, lo que facilita compartir conocimiento entre el equipo; ligero y

con gran cantidad de librerías para APIs REST.

- .NET: robusto y con tipado fuerte, buen rendimiento, pero requiere

conocimientos de C# que el equipo no maneja actualmente.

- Spring Boot: maduro y usado en entornos empresariales, pero con mayor

complejidad de configuración inicial (Java + Spring).

## Consecuencias

### Positivas

- Un solo lenguaje (JavaScript/TypeScript) en todo el stack, reduce la curva

de aprendizaje del equipo.

- Gran cantidad de paquetes disponibles (npm) para autenticación, validación

y conexión a bases de datos.

### Negativas / riesgos

- Node.js es de tipado dinámico (a menos que se use TypeScript), lo que

puede generar errores en tiempo de ejecución si no se valida bien.

- Requiere buenas prácticas para manejar operaciones asíncronas.

## Referencias

- Documento Avance #1 del proyecto, sección "Justificación Administrativa".

- https://nodejs.org/