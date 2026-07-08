\# ADR-0001: Elección de tecnología frontend



\## Estado

Aceptado



\## Contexto

El Sistema de Gestión y Control de Notas Estudiantiles (SGCE) requiere una

interfaz web accesible desde cualquier dispositivo con conexión a internet,

que reduzca la dependencia de equipos físicos y horarios de oficina

(ver Avance #1, sección "Justificación Tecnológica"). El diagrama de

contenedores (C4) plantea tres alternativas: React, Angular o HTML/CSS puro.



\## Decisión

Se selecciona React como tecnología de frontend.



\## Alternativas consideradas

\- React: biblioteca basada en componentes reutilizables, gran ecosistema

&#x20; y comunidad, curva de aprendizaje moderada para el equipo.

\- Angular: framework completo y opinado, robusto para proyectos grandes,

&#x20; pero con curva de aprendizaje más alta y mayor complejidad inicial.

\- HTML/CSS puro: rápido de implementar en prototipos pequeños, pero no

&#x20; escala bien para una aplicación con múltiples roles de usuarios

&#x20; (estudiante, docente, administrador) y estados dinámicos.



\## Consecuencias

\### Positivas

\- Desarrollo más ágil gracias a componentes reutilizables.

\- Amplia documentación y soporte de la comunidad.

\- Facilita el mantenimiento a largo plazo del sistema.



\### Negativas / riesgos

\- Requiere configurar herramientas adicionales (bundlers, gestión de estado).

\- El equipo debe familiarizarse con el ecosistema de React si no lo conoce.



\## Referencias

\- Documento Avance #1 del proyecto, sección "Justificación Tecnológica".

\- https://react.dev/



