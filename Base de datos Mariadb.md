# Base de datos Mariadb
## Índice
1. ¿Por qué un SGBD como MariaDB? ¿Qué es?
2. Instalación de MariaDB

## 1. ¿Por qué un SGBD como MariaDB? ¿Qué es?

### ¿Qué es una base de datos?

Una base de datos en un conjunto de información guardada de forma ordenada para poder buscarla y usarla rápidamente, se organizan en tablas que tienen lo siguiente:

- columnas: el tipo de dato que se guarda (por ejemplo "título", "autor")
- Filas: cada elemento guardado (por ejemplo, cada entrada del blog)

| id | título | autor | fecha |
|---|---------|-------|-------|
| 1 | Hola mundo | admin | 2026-10-26 |
| 2 | Horario de matrícula | admin | 2026-10-27 |

### ¿Qué es un SGBD?

Un **SGBD** (Sistema Gestor de Bases de Datos) es el **programa que se encarga de manejar la base de datos**, los programas como WordPress no leen ni escriben los datos directamente en el disco sino que se lo piden al SGBD y este se encarga de:

- **Guardar** los datos de forma ordenada y segura.
- **Buscarlos rápido** cuando alguien los pide usando el lenguaje **SQL**.
- **Controlar quién accede** con usuarios, contraseñas y permisos.
- **Evitar errores** cuando muchas personas usan los datos a la vez (por ejemplo dos visitantes comentando al mismo tiempo).
- **Mantener la información coherente** aunque falle algo a mitad de una operación.
