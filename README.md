# Comandos Básicos de SQL
## Objetivo
Vamos a desarrollar la base de datos de un video juego RPG en SQL, si estan interesados en como desarrollamos el backend no olviden seguirme para una proxima documentacíon.

## Crear Tablas
Lo primero es crear algunas de las tablas que vamos a estar usando.
los comandos son:

- CREATE DATABASE: Crear una base de datos.
- CREATE TABLE: Crear una tabla.
- ALTER TABLE: Modificar una tabla.
- DROP TABLE: Eliminar una tabla.


Ahora vamos a crear las tablas.

#### Tabla de personajes
```
CREATE TABLE Personajes (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    vida INT,
    fuerza INT,
    destreza INT,
    magia INT
);

```
#### Tabla de magias
```
CREATE TABLE Magias (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    tipo VARCHAR(20),
    poder INT,
    descripcion TEXT
);
```
#### Tablas de objetos
```
CREATE TABLE Objetos (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    tipo_objeto VARCHAR(20)
);

CREATE TABLE Armas (
    id INT PRIMARY KEY,
    objeto_id INT,
    tipo_arma VARCHAR(20),
    ataque INT,
    descripcion TEXT,
    FOREIGN KEY (objeto_id) REFERENCES Objetos(id)
);

CREATE TABLE ObjetosClave (
    id INT PRIMARY KEY,
    objeto_id INT,
    efecto VARCHAR(100),
    descripcion TEXT,
    FOREIGN KEY (objeto_id) REFERENCES Objetos(id)
);

CREATE TABLE Pociones (
    id INT PRIMARY KEY,
    objeto_id INT,
    tipo_pocion VARCHAR(20),
    efecto VARCHAR(100),
    descripcion TEXT,
    FOREIGN KEY (objeto_id) REFERENCES Objetos(id)
);
```
```

```
