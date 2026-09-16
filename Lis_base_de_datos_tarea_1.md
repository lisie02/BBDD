# INSTALACIÓN DE UN SGBD

## Instituto Politécnico Nacional

### Escuela Superior de Cómputo (ESCOM)

**Docente:** Hurtado Avilés Gabriel

**Alumna:** Suarez Mendoza Lis Rosaura  
**Grupo:** 3BV1  
**Fecha:** 15 de septiembre de 2026

---

# Tarea #1
## Base de Datos

## Introducción

En esta actividad se llevará a cabo la instalación y configuración de un Sistema Gestor de Bases de Datos (SGBD) utilizando diferentes herramientas como Docker, Ubuntu, PostgreSQL y pgAdmin.

El objetivo principal es conocer de manera práctica cómo se puede preparar un entorno para trabajar con bases de datos y comprender la función que tiene cada una de estas herramientas dentro del proceso.

Durante la práctica se utilizará Docker para crear y levantar un contenedor donde se ejecutará PostgreSQL, mientras que pgAdmin permitirá administrar la base de datos mediante una interfaz gráfica. También se utilizará Ubuntu como parte del entorno de trabajo.

A través de este proceso podremos familiarizarnos con conceptos como contenedores, servidores, bases de datos y conexiones entre diferentes herramientas.

Esta actividad es importante porque, como estudiantes de Ingeniería en Inteligencia Artificial, no solo necesitamos aprender a programar, sino también entender cómo se almacenan, organizan y administran los datos que posteriormente pueden ser utilizados por diferentes aplicaciones y sistemas de inteligencia artificial.

Por medio de esta práctica se busca adquirir experiencia en la instalación y configuración de un entorno real de trabajo con bases de datos.

---

## Instalación de Docker

Docker nos permite ejecutar aplicaciones dentro de contenedores, permitiéndonos crear un contenedor para PostgreSQL. Sin embargo, para que Docker pueda funcionar en nuestro sistema Windows será necesario instalar Ubuntu, permitiendo utilizar Linux como sistema operativo.

Para la instalación de Docker es suficiente con ingresar al navegador, buscar la página oficial y descargar la versión más reciente.

### Verificación de Docker

Podemos verificar que Docker se ha instalado correctamente en la terminal de Ubuntu escribiendo:

```bash
docker --version
```

También será necesario instalar PostgreSQL y pgAdmin en sus versiones más recientes.

pgAdmin permitirá administrar y visualizar PostgreSQL mediante una interfaz gráfica.

---

## Crear un Contenedor

Podemos generar el contenedor desde la terminal de Ubuntu o desde CMD descargando la imagen oficial de PostgreSQL.

La imagen contiene todo lo necesario para crear el contenedor.

Ejemplo:

```bash
docker pull postgres
```

Crear un contenedor:

```bash
docker run --name postgres-db \
-e POSTGRES_PASSWORD=admin \
-p 5432:5432 \
-d postgres
```

Verificar contenedores:

```bash
docker ps
```

---

## Conclusión

En esta tarea fue muy importante conocer y aprender cómo crear un contenedor, ya que en la materia de Bases de Datos representa el primer paso para construir la estructura donde posteriormente se almacenarán los datos.

La práctica me permitió comprender de una manera más clara cómo se instala y configura un entorno para trabajar con bases de datos. El uso de Docker permitió crear y levantar un contenedor con PostgreSQL, mientras que pgAdmin facilitó la administración de la base de datos mediante una interfaz gráfica.

En general, la actividad me ayudó a familiarizarme con herramientas que pueden ser útiles durante mi formación en Ingeniería en Inteligencia Artificial y a entender mejor la importancia de gestionar correctamente los datos.

---

## Referencias

- Del Estado de Hidalgo, U. A. (s. f.). *Software libre (Ubuntu).* https://www.uaeh.edu.mx/scige/boletin/prepa4/n2/e4.html
- PostgreSQL Global Development Group. (s. f.). *PostgreSQL: The world’s most advanced open source database.*
- PostgreSQL Global Development Group. (s. f.). *PostgreSQL Documentation.*
- pgAdmin Development Team. (s. f.). *pgAdmin 4 Documentation.*