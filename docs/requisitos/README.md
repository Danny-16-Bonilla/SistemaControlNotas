1. Manual Técnico del Sistema
1.1. Arquitectura y Componentes
El Sistema de Control de Notas Estudiantiles utiliza una arquitectura cliente-servidor desacoplada dividida en tres capas principales:
Capa de Presentación (Frontend): Interfaz Web/Móvil interactiva para Administradores, Docentes y Estudiantes.
Capa de Negocio (Backend / API REST): Controladores y servicios encargados del procesamiento de datos, validación de permisos, reglas de negocio (cálculo de promedios, porcentajes de evaluación, estados de aprobación/reprobación).
Capa de Persistencia (Base de Datos): Base de datos relacional (PostgreSQL / MySQL) que almacena usuarios, cursos, asignaciones, calificaciones y bitácoras.
1.2. Especificaciones de Servidor y Entorno
Entorno de ejecución: Node.js (v18 LTS o superior) / Python (3.10+).
Base de Datos: PostgreSQL 14+ / MySQL 8.0+.
Requisitos Mínimos de Servidor: 2 vCPU, 4 GB RAM, 10 GB de almacenamiento SSD.
2. Manual de Instalación y Despliegue
Paso 1: Clonar el Repositorio
git clone https://github.com/Danny-16-Bonilla/SistemaControlNotas.gitcd SistemaControlNotas
Paso 2: Configuración de Variables de Entorno
Crea un archivo .env en la raíz del proyecto basándote en la plantilla .env.example: PORT=8080 DB_HOST=localhost DB_PORT=5432 DB_NAME=sistema_notas_db DB_USER=admin_notas DB_PASSWORD=TuPasswordSeguro123! JWT_SECRET=ClaveSecretaJWT2026
Paso 3: Instalación de Dependencias
npm install
Paso 4: Ejecución de Migraciones de Base de Datos
npm run db:migrate npm run db:seed
Paso 5: Despliegue/Ejecución del Servidor
Entorno de Desarrollo: npm run dev
Entorno de Producción: npm run build && npm start
3. Manual de Usuario
3.1. Funcionalidades por Rol
Administrador: Crear y gestionar usuarios (profesores, estudiantes), asignar docentes a materias y grupos, y configurar periodos lectivos.
Docente: Crear los rubros de evaluación del curso (Parciales, Tareas, Proyectos), registrar y actualizar calificaciones, y cerrar actas de notas finales.
Estudiante: Consultar desglose de calificaciones por materia, y visualizar promedio acumulado y estado final de la asignatura.
3.2. Paso a Paso para Registro de Notas (Rol Docente)
Iniciar sesión en la plataforma con las credenciales asignadas.
Ir a la sección "Mis Cursos" en el menú principal.
Seleccionar la asignatura y el grupo correspondiente.
Hacer clic en "Gestión de Calificaciones".
Seleccionar la evaluación a calificar (ej. Examen Parcial I).
Ingresar las notas de los estudiantes (escala 0 a 100).
Presionar "Guardar Cambios" para actualizar el historial académico.
4. Reflexión sobre la Inteligencia Artificial en el Desarrollo
Ventajas y Aportes de la IA
Aceleración del desarrollo: Asistencia en la generación de estructuras iniciales (boilerplate code), esquemas de base de datos y endpoints para la API REST.
Calidad de código y pruebas: Apoyo en la identificación de casos borde (edge cases) en las validaciones de notas y la creación de datos de prueba mock.
Estructuración documental: Apoyo en la organización coherente y profesional del expediente documental de la Fase III.
Análisis Crítico y Responsabilidad Humana
A pesar de la agilidad que aportan las herramientas de IA, la supervisión humana fue imprescindible para refactorizar la arquitectura según los estándares del proyecto, garantizar la seguridad en la gestión de contraseñas y tokens de autenticación, y validar que la lógica de cálculo de promedios ponderados se ajustara a los reglamentos académicos reales.
5. Conclusiones
Integración Exitosa: Se consolidó la Fase III integrando todo el expediente documental, unificando el trabajo de análisis (Fase I) y diseño/desarrollo (Fase II).
Estructura Escalable: La separación por capas y el uso de patrones limpios garantizan que el sistema pueda escalar fácilmente a futuro.
Control de Versiones y Trazabilidad: El trabajo organizado mediante GitHub facilitó la colaboración en equipo y la trazabilidad de cambios en cada entrega.
6. Referencias Bibliográficas (APA 7ª ed.)
Bass, L., Clements, P., & Kazman, R. (2021). Software architecture in practice (4th ed.). Addison-Wesley Professional.
Pressman, R. S., & Maxim, B. R. (2019). Software engineering: A practitioner's approach (9th ed.). McGraw-Hill Education.
Sommerville, I. (2016). Software engineering (10th ed.). Pearson.
