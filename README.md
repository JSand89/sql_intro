# Comandos Básicos de SQL
## DDL (Data Definition Language)
- CREATE DATABASE: Crear una base de datos.
- CREATE TABLE: Crear una tabla.
- ALTER TABLE: Modificar una tabla.
- DROP TABLE: Eliminar una tabla.
Ahora vamos a crear las tablas de uno de los juegos favoritos de su formador.

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
```
CREATE TABLE Magias (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    tipo VARCHAR(20),
    poder INT,
    descripcion TEXT
);
```
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
