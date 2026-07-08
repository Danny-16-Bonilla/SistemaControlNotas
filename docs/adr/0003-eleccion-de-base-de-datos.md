\# ADR-0003: Elección de base de datos



\## Estado

Aceptado



\## Contexto

La información académica (calificaciones, usuarios, cursos) es sensible y

requiere trazabilidad ante modificaciones (RNF-02, RNF-03 del documento de

requisitos). El diagrama C4 plantea dos alternativas: SQL Server o

PostgreSQL.



\## Decisión

Se selecciona PostgreSQL como motor de base de datos.



\## Alternativas consideradas

\- PostgreSQL: sistema de gestión de bases de datos relacional, de código

&#x20; abierto y sin costo de licenciamiento, con soporte robusto para

&#x20; integridad referencial y transacciones.

\- SQL Server: motor robusto y con buena integración en entornos

&#x20; Microsoft/.NET, pero con costos de licenciamiento para uso institucional.



\## Consecuencias

\### Positivas

\- Sin costos de licencia, ideal para un proyecto universitario.

\- Amplio soporte de la comunidad y compatibilidad con Node.js.

\- Cumple con los requisitos de integridad y consistencia de datos.



\### Negativas / riesgos

\- El equipo debe familiarizarse con las herramientas de administración de

&#x20; PostgreSQL si no las ha usado antes (pgAdmin, psql).



\## Referencias

\- Documento de requisitos, RNF-02 y RNF-03.

\- https://www.postgresql.org/

