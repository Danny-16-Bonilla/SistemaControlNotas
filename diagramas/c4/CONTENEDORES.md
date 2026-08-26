# Nivel 2: Modelo de Contenedores

## Descripción

En el **Nivel 2 – Modelo de Contenedores** se muestra cómo está organizado internamente el **Sistema de Información TIC** y cuáles son sus principales unidades tecnológicas.

A diferencia del Nivel 1, donde el sistema se representa como una sola unidad, en este nivel se muestran sus principales partes internas y la forma en que se comunican entre sí.

Los principales contenedores son:

- **Aplicación Web Frontend**
- **API Backend**
- **Base de Datos**

El **Usuario / Cliente** interactúa directamente con la **Aplicación Web Frontend**, que corresponde a la parte visual del sistema. Esta puede desarrollarse utilizando tecnologías como **React, Angular, HTML, CSS y JavaScript**.

La **Aplicación Web Frontend** se comunica con la **API Backend** para enviar solicitudes y recibir información. Esta comunicación puede realizarse mediante **HTTPS**, utilizando formatos como **JSON** para intercambiar datos.

La **API Backend** procesa las solicitudes recibidas, ejecuta la lógica del sistema y realiza las operaciones necesarias.

Finalmente, el **Backend** se comunica con la **Base de Datos** para almacenar, consultar, modificar o eliminar la información utilizada por el sistema. Como ejemplos de tecnologías se pueden utilizar **SQL Server** o **PostgreSQL**.

---

## Contenedores principales

| Contenedor | Descripción | Tecnologías posibles |
|---|---|---|
| Aplicación Web Frontend | Proporciona la interfaz visual mediante la cual el usuario interactúa con el sistema. | React, Angular, HTML, CSS y JavaScript |
| API Backend | Recibe y procesa solicitudes, ejecuta la lógica del sistema y comunica el frontend con la base de datos. | Node.js, .NET, Spring Boot |
| Base de Datos | Almacena y permite consultar la información utilizada por el sistema. | SQL Server, PostgreSQL |

---

## Flujo de funcionamiento

El funcionamiento general puede entenderse de la siguiente manera:

1. El **Usuario / Cliente** utiliza la interfaz del sistema.
2. La **Aplicación Web Frontend** recibe las acciones del usuario.
3. El **Frontend** envía las solicitudes a la **API Backend** mediante HTTPS y puede utilizar JSON para intercambiar información.
4. La **API Backend** procesa la solicitud y ejecuta la lógica correspondiente.
5. Cuando es necesario, el **Backend** consulta o modifica la **Base de Datos**.
6. La respuesta regresa desde el Backend hacia el Frontend y finalmente se muestra al usuario.

En forma resumida:

> **Usuario → Frontend → Backend → Base de Datos**

Y la respuesta sigue el camino inverso:

> **Base de Datos → Backend → Frontend → Usuario**

---

## Límite del Sistema

El rectángulo denominado **"Límite del Sistema"** permite identificar cuáles elementos forman parte directamente del **Sistema de Información TIC**.

Dentro de este límite se encuentran:

- **Aplicación Web Frontend**
- **API Backend**
- **Base de Datos**

El **Usuario / Cliente** se encuentra fuera del límite porque representa una persona que utiliza el sistema, pero no forma parte de su arquitectura interna.

El límite permite diferenciar claramente entre **los elementos que pertenecen al sistema** y **las personas externas que interactúan con él**.

---

## ¿Por qué se utilizan estos tres contenedores?

### Aplicación Web Frontend

Se encarga de la **interfaz de usuario**, es decir, de mostrar la información y permitir que el usuario interactúe con el sistema.

### API Backend

Se encarga de la **lógica del sistema**. Recibe solicitudes del Frontend, procesa la información y determina qué operaciones deben realizarse.

### Base de Datos

Se encarga de **almacenar y proporcionar los datos** que necesita el sistema para funcionar.

Esta separación permite que cada contenedor tenga una responsabilidad específica y facilita el mantenimiento y evolución del sistema.

---

## Relación entre los contenedores

### Usuario → Frontend

**Relación:** `Interactúa con la interfaz`

El usuario utiliza la aplicación web para realizar las operaciones disponibles.

### Frontend → Backend

**Relación:** `Consume servicios vía HTTPS/JSON`

El Frontend envía solicitudes al Backend y recibe las respuestas correspondientes.

### Backend → Base de Datos

**Relación:** `Persiste y consulta datos`

El Backend solicita información a la base de datos o guarda los cambios realizados por los usuarios.

---

## Diferencia con el Nivel 1

En el **Nivel 1 – Contexto**, el sistema se muestra como una sola unidad para identificar a los usuarios y sistemas externos relacionados.

En el **Nivel 2 – Contenedores**, ese sistema se descompone para mostrar sus principales partes internas.

Por lo tanto:

> **Nivel 1:** ¿Quién utiliza el sistema y con qué se relaciona?

> **Nivel 2:** ¿Cómo está organizado internamente el sistema?

---

```mermaid
graph TD

    UserCont["Usuario / Cliente"]

    subgraph SistemaTIC["Límite del Sistema"]
        WebApp["Aplicación Web Frontend<br/>React / Angular / HTML-CSS-JavaScript"]
        API["API Backend<br/>Node.js / .NET / Spring Boot"]
        DB[("Base de Datos<br/>SQL Server / PostgreSQL")]
    end

    UserCont -->|Interactúa con la interfaz| WebApp
    WebApp -->|Consume servicios vía HTTPS/JSON| API
    API -->|Persiste y consulta datos| DB

    classDef azulOscuro fill:#08427B,stroke:#032F55,color:#fff;
    classDef contenedor fill:#438DD5,stroke:#2B659B,color:#fff;

    class UserCont azulOscuro;
    class WebApp,API,DB contenedor;
