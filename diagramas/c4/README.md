@startuml
skinparam linetype ortho

entity "Aviones" as Aviones {
  * Matricula : PK
  --
  Modelo
  Anhoinsc
}

entity "Pilotos" as Pilotos {
  * Pasaporte : PK
  --
  Nombre
  Nacionalidad
  Edad
  Correo
  Telefono
}

entity "Paquetes" as Paquetes {
  * Codigo : PK
  --
  Peso
  Descripcion
  Destino
}

entity "Receptores" as Receptores {
  * id : PK
  --
  Nombre
  Clave
  Correo
  Telefono
}

' Relaciones con cardinalidades
Aviones }|--|{ Pilotos : "tiene (N:N)"
Aviones ||--o{ Paquetes : "lleva (1:N)"
Receptores ||--o{ Paquetes : "tiene (1:N)"

@enduml
