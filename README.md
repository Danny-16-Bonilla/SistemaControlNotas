# 🎓 Sistema de Gestión y Control de Notas Estudiantiles (SGCE)

<p align="center">
  <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExdHQ4djJydmhjNjQzdHF3Y24yMGh2OTIwbGl4dmpkdTZhZGY1aTNxdiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/H03PuVdwREB21ANkLX/giphy.gif" alt="Developer Coding GIF" width="550">
</p>


Bienvenido al repositorio oficial del proyecto **SGCE**. Este sistema web está diseñado para optimizar, automatizar y auditar la gestión, control y consulta de calificaciones académicas en instituciones de educación superior, sustituyendo los procesos manuales por una solución centralizada, trazable y segura.

---

## 📌 Contexto del Proyecto

El **SGCE** busca erradicar las deficiencias de los métodos tradicionales (hojas de cálculo y registros físicos) que generan inconsistencias, pérdidas de información y retrasos en la publicación de notas.

* **Objetivo General:** Desarrollar e implementar un Sistema Integral de Gestión y Control de Notas Estudiantiles mediante una plataforma web centralizada y de alta seguridad, garantizando la trazabilidad absoluta y optimizando la toma de decisiones institucionales.
* **Estado del Entregable:** Fase II - Especificación de Arquitectura, Modelado C4/UML y Manuales Operativos.

---

## 🗂️ Índice del Expediente Documental

El proyecto está organizado de forma modular. Utilice la siguiente tabla para navegar a las distintas secciones del expediente:

### 1. Documentación Conceptual, Análisis y Operación

| Sección / Entregable | Descripción | Enlace Directo |
| :--- | :--- | :--- |
| **Centro de Documentación** | Índice principal y mapa de documentos | [📂 `docs/`](./docs/) |
| **Requisitos del Sistema** | Requisitos Funcionales (`RF-01` a `17`) y No Funcionales (`RNF-01` a `10`) | [📋 `docs/requisitos/`](./docs/requisitos/) |
| **Historias de Usuario** | Especificación ágil de funcionalidades (`HU-01` a `10`) | [📖 `docs/historias_usuario/`](./docs/historias_usuario/) |
| **Registros ADR** | Decisiones de Arquitectura de Software | [🏛️ `docs/adr/`](./docs/adr/) |
| **Manual de Usuario** | Guía paso a paso para estudiantes y docentes | [📘 `docs/MANUAL_USUARIO.md`](./docs/MANUAL_USUARIO.md) |
| **Manual de Administración** | Gestión de usuarios, roles, catálogos y seguridad | [📕 `docs/MANUAL_ADMINISTRACION.md`](./docs/MANUAL_ADMINISTRACION.md) |
| **Despliegue y Servidor** | Requisitos, instalación y plan de rollback | [🚀 `docs/DESPLIEGUE.md`](./docs/DESPLIEGUE.md) |
| **Respaldo y Recuperación** | Políticas de backup, frecuencia y procedimiento | [💾 `docs/RESPALDO_Y_RECUPERACION.md`](./docs/RESPALDO_Y_RECUPERACION.md) |
| **Notas de Versión** | Historial de entregas, cambios y correcciones | [📋 `docs/NOTAS_DE_VERSION.md`](./docs/NOTAS_DE_VERSION.md) |

---

### 2. Diagramación y Arquitectura Visual

| Sección | Modelos / Contenido | Enlace Directo |
| :--- | :--- | :--- |
| **Diagramas UML** | Casos de uso, diagramas de actividades y clases | [📊 `diagramas/uml/`](./diagramas/uml/) |
| **Modelado C4** | Nivel 1 (Contexto), Nivel 2 (Contenedores) y Nivel 3 (Componentes) | [🏗️ `diagramas/c4/`](./diagramas/c4/) |

---

## 🔗 Matriz de Trazabilidad del Proyecto

| Objetivo Específico | Req. Funcionales | Historias de Usuario | Req. No Funcionales |
| :--- | :--- | :--- | :--- |
| **OE-01:** Roles y Permisos | `RF-01`, `RF-02`, `RF-03`, `RF-04` | `HU-01`, `HU-02`, `HU-09` | `RNF-03`, `RNF-04` |
| **OE-02:** Períodos y Cursos | `RF-05`, `RF-06`, `RF-07` | `HU-08` | `RNF-02`, `RNF-07` |
| **OE-03:** Componentes Evaluativos | `RF-08` | `HU-03` | `RNF-01`, `RNF-08` |
| **OE-04:** Registro y Cálculo | `RF-09`, `RF-10`, `RF-11`, `RF-12` | `HU-04`, `HU-05` | `RNF-01`, `RNF-09` |
| **OE-05:** Consulta de Calificaciones | `RF-13`, `RF-14` | `HU-06` | `RNF-01`, `RNF-04`, `RNF-05` |
| **OE-06:** Solicitud de Revisión | `RF-17` | `HU-07` | `RNF-04`, `RNF-09` |
| **OE-07:** Reportes Exportables | `RF-15`, `RF-16` | `HU-10` | `RNF-01`, `RNF-04` |
| **OE-08:** Calidad y Seguridad | `RF-02`, `RF-04`, `RF-12` | `HU-01`, `HU-09` | `RNF-01` a `RNF-10` |

---

## 👥 Equipo de Trabajo y Responsabilidades

| Integrante | Rol en el Proyecto | Usuario GitHub |
| :--- | :--- | :--- |
| **Dany Bonilla** | Coordinador de Repositorio y Despliegue | [@Danny-16-Bonilla](https://github.com/Danny-16-Bonilla) |
| **Nelson Alvarez** | Diagramación y Modelado UML | [@Nelsonalvarez15](https://github.com/Nelsonalvarez15) |
| **Freisser Arce** | Diseñador de Arquitectura C4 | [@Freiss5r](https://github.com/Freiss5r) |
| **Julian Brenes** | Arquitectura y Registros Decisiones (ADR) | [@brenesyulian67-a11y](https://github.com/brenesyulian67-a11y) |
| **Sharon Zuñiga** | Especificación de Requisitos e Historias de Usuario | *Colaboradora* |

---

## 🛠️ Tecnologías y Metodología

* **Control de Versiones:** Git & GitHub
* **Estándar Documental:** Markdown (`.md`)
* **Arquitectura de Software:** Cliente-Servidor (SPA Web + REST API)
* **Modelado Visual:** UML 2.5 y C4 Model
- **Modelado Visual**: UML y C4 Model
