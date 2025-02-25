# Tarea 12

Realiza una instalación limpia de una base de datos y mar
ca la opción de “Demo
data”. Posteriormente instala las aplicaciones de facturación y contactos.

## Apartado 1

Mediante la
herramienta PgAdmin u otro método que estimes oportuno, elabora y ejecuta una
sentencia que cree una tabla llamada “EmpresasFCT“con los siguientes campos:

    ● idEmpresa: autonumérico. Este campo será la clave primaria.
    ● nombre: Texto con tamaño máximo de 40 caracteres. -useChatgpt: booleano, por defecto a true
    ● quiereAlumnos: Booleano.
    ● numAlumnos: número entero.
    ● fechaContacto: tipo fecha.

```sql
CREATE TABLE EmpresasFCT (
    idEmpresa SERIAL PRIMARY KEY,
    nombre VARCHAR(40) NOT NULL ,
    useChatgpt BOOLEAN,
    quiereAlumnos BOOLEAN,
    numAlumnos INTEGER,
    fechaContacto DATE
);
```
![Screenshot_20250225_132854.png](img/Screenshot_20250225_132854.png)

## Apartado 2

Inserta 5 registros inventados en la tabla a través de una sentencia SQL.

```sql
INSERT INTO EmpresasFCT (nombre, quiereAlumnos, numAlumnos, fechaContacto)
VALUES
    ('Empresa1', TRUE, 5, '2025-01-25'),
    ('Empresa2', FALSE, 0, '2025-01-12'),
    ('Empresa3', TRUE, 3, '2025-01-01'),
    ('Empresa4', TRUE, 10, '2025-01-14'),
    ('Empresa5', TRUE, 7, '2025-01-20');
```
![Screenshot_20250225_133252.png](img/Screenshot_20250225_133252.png)

## Apartado 3

Realiza una consulta donde se muestren todos los datos de la tabla EmpresasFCT
ordenados por fechaContacto, de modo que en la primera fila salga el que tenga la
fecha más reciente.

```sql
SELECT * FROM EmpresasFCT ORDER BY fechaContacto DESC;
```
![Screenshot_20250225_133544.png](img/Screenshot_20250225_133544.png)

