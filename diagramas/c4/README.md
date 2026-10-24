erDiagram
    OFICINA {
        string codof PK
        string lugar
    }
    DEPARTAMENTO {
        string coddep PK
        string nombre
    }
    EMPLEADO {
        string cedula PK
        string nombre
        string apellido
        string codof FK
        string coddep FK
    }
    ROL {
        string codrol PK
        string rol
    }
    PROYECTO {
        string codpro PK
        string fechainicio
        string descripcion
    }
    EMPLEADO_ROL {
        string cedula PK,FK
        string codrol PK,FK
    }
    EMPLEADO_PROYECTO {
        string cedula PK,FK
        string codpro PK,FK
        date fechainicio
    }

    OFICINA ||--o{ EMPLEADO : "pertenece"
    DEPARTAMENTO ||--o{ EMPLEADO : "tiene"
    EMPLEADO ||--o{ EMPLEADO_ROL : ""
    ROL ||--o{ EMPLEADO_ROL : ""
    EMPLEADO ||--o{ EMPLEADO_PROYECTO : ""
    PROYECTO ||--o{ EMPLEADO_PROYECTO : ""
