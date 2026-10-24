```mermaid
erDiagram
    OFICINA {
        codof PK
        lugar
    }
    DEPARTAMENTO {
        coddep PK
        nombre
    }
    EMPLEADO {
        cedula PK
        nombre
        apellido
        codof FK
        coddep FK
    }
    ROL {
        codrol PK
        rol
    }
    PROYECTO {
        codpro PK
        fechainicio
        descripcion
    }
    EMPLEADO_ROL {
        cedula PK_FK
        codrol PK_FK
    }
    EMPLEADO_PROYECTO {
        cedula PK_FK
        codpro PK_FK
        fechainicio
    }
    OFICINA ||--o{ EMPLEADO : ""
    DEPARTAMENTO ||--o{ EMPLEADO : ""
    EMPLEADO ||--o{ EMPLEADO_ROL : ""
    ROL ||--o{ EMPLEADO_ROL : ""
    EMPLEADO ||--o{ EMPLEADO_PROYECTO : ""
    PROYECTO ||--o{ EMPLEADO_PROYECTO : ""
