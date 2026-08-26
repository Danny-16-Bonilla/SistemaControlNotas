Manual del Sistema de Control de Notas Estudiantiles

 1. Manual Técnico del Sistema

1.1. Arquitectura y Componentes

El Sistema de Control de Notas Estudiantiles utiliza una arquitectura cliente-servidor desacoplada, dividida en tres capas principales:

**Capa de Presentación (Frontend):**
Interfaz Web/Móvil interactiva para Administradores, Docentes y Estudiantes.

**Capa de Negocio (Backend / API REST):**
Controladores y servicios encargados del procesamiento de datos, validación de permisos y aplicación de reglas de negocio, como el cálculo de promedios, porcentajes de evaluación y estados de aprobación o reprobación.

**Capa de Persistencia (Base de Datos):**
Base de datos relacional PostgreSQL o MySQL que almacena usuarios, cursos, asignaciones, calificaciones y bitácoras.

 1.2. Especificaciones de Servidor y Entorno

**Entorno de ejecución:** Node.js v18 LTS o superior / Python 3.10 o superior.

**Base de Datos:** PostgreSQL 14 o superior / MySQL 8.0 o superior.

**Requisitos mínimos del servidor:**

* 2 vCPU
* 4 GB de RAM
* 10 GB de almacenamiento SSD

---

# 2. Manual de Instalación y Despliegue

## Paso 1: Clonar el Repositorio

```bash
git clone https://github.com/Danny-16-Bonilla/SistemaControlNotas.git
cd SistemaControlNotas
```

Paso 2: Configuración de Variables de Entorno

Crear un archivo `.env` en la raíz del proyecto basándose en la plantilla `.env.example`:

```env
PORT=8080
DB_HOST=localhost
DB_PORT=5432
DB_NAME=sistema_notas_db
DB_USER=admin_notas
DB_PASSWORD=TuPasswordSeguro123!
JWT_SECRET=ClaveSecretaJWT2026
```

 Paso 3: Instalación de Dependencias

Ejecutar el siguiente comando:

```bash
npm install
```

## Paso 4: Ejecución de Migraciones de Base de Datos

Ejecutar:

```bash
npm run db:migrate
npm run db:seed
```

 Paso 5: Despliegue y Ejecución del Servidor

Entorno de Desarrollo

```bash
npm run dev
```

 Entorno de Producción

```bash
npm run build
npm start
```

---

3. Manual de Usuario

3.1. Funcionalidades por Rol

 Administrador

* Crear y gestionar usuarios.
* Registrar profesores y estudiantes.
* Asignar docentes a materias y grupos.
* Configurar periodos lectivos.
* Administrar la información general del sistema.

 Docente

* Crear rubros de evaluación del curso, como parciales, tareas y proyectos.
* Registrar y actualizar calificaciones.
* Consultar las notas de los estudiantes.
* Cerrar actas de notas finales.

Estudiante

* Consultar las calificaciones por materia.
* Visualizar el desglose de las evaluaciones.
* Consultar el promedio acumulado.
* Visualizar el estado final de la asignatura.

3.2. Paso a Paso para el Registro de Notas — Rol Docente

1. Iniciar sesión en la plataforma con las credenciales asignadas.
2. Dirigirse a la sección **"Mis Cursos"** en el menú principal.
3. Seleccionar la asignatura y el grupo correspondiente.
4. Hacer clic en **"Gestión de Calificaciones"**.
5. Seleccionar la evaluación que se desea calificar, por ejemplo, **"Examen Parcial I"**.
6. Ingresar las notas de los estudiantes en una escala de **0 a 100**.
7. Presionar **"Guardar Cambios"** para registrar y actualizar las calificaciones en el historial académico.
