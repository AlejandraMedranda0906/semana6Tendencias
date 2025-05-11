# TENDENCIAS TECNOLOGICAS

## 1. Titulo
TAS5 - hvfgcgvWordpres con docker
## 2. Tiempo de duración
El tiempo de duración fue de 5 horas aproximadamente para xkjsbdhcbdjn el desarrollo de la práctica.

## 3. Fundamentos:

En esta práctica se trabajó con contenedores Docker para levantar un entorno completo de gestión de contenidos con WordPress, incluyendo el sistema de gestión de bases de datos MySQL y la herramienta web de administración phpMyAdmin, todos interconectados en una red personalizada.

Docker permite crear entornos aislados mediante contenedores, lo que facilita la portabilidad, escalabilidad y configuración eficiente de servicios como servidores web, gestores de contenido y bases de datos (Docker Inc., 2024). A través de la creación de una red personalizada en Docker, es posible establecer una comunicación segura entre contenedores, por ejemplo, entre el servidor WordPress y el contenedor de base de datos MySQL.

WordPress es un sistema de gestión de contenidos (CMS) de código abierto ampliamente utilizado para la creación de sitios web y blogs. Su implementación en contenedores Docker permite un despliegue modular y replicable del sistema (WordPress.org, 2024).

MySQL, por su parte, es un sistema de gestión de bases de datos relacional que se encarga del almacenamiento y administración de datos estructurados (MySQL Documentation Team, 2024). En esta práctica se utiliza para alojar la base de datos de WordPress.

phpMyAdmin se incorpora como una interfaz web para gestionar MySQL de forma visual, permitiendo consultar, crear y modificar tablas y registros fácilmente (phpMyAdmin, 2024).

La práctica se enfoca en tres aspectos fundamentales:

Crear una red personalizada en Docker para interconectar contenedores.

Implementar WordPress como CMS utilizando contenedores Docker.

Conectar WordPress con MySQL y administrar la base de datos mediante phpMyAdmin.

Esta metodología permite a los estudiantes comprender los conceptos clave de redes, persistencia de datos y gestión de servicios web usando contenedores. Además, fomenta la autonomía en la configuración de entornos profesionales de desarrollo web (Nickoloff & Kuenzli, 2019; Miell & Sayers, 2019).

## 4. Conocimientos previos.

Para realizar esta practica el estudiante necesita tener claro los siguientes temas:
- Línea de comandos (CLI)
- Navegadores web
- Conceptos fundamentales de Docker (contenedores, volúmenes, redes)
- Configuración y uso de MySQL
- Uso de phpMyAdmin
- CMS WordPress.
- Base de datos para CMS
- Redes personalizadas en Docker 
- Gestionar volúmenes de Docker

## 5. Objetivos a alcanzar

- Configurar manualmente los contenedores necesarios para levantar un CMS WordPress utilizando solo comandos de Docker.
- Configurar variables de entorno en la creación de los contenedores para establecer parámetros esenciales como usuario, contraseña y nombre de la base de datos
- Implementar redes personalizadas en Docker para permitir la comunicación segura entre los contenedores de base de datos y WordPress.
- Gestionar volúmenes de Docker para asegurar la persistencia de datos tanto para la base de datos como para los archivos de WordPress.

## 6. Equipo necesario:

- Computadora con sistema operativo Windows/Linux/Mac
- Acceso a Docker Play o instalación local de Docker
- Terminal
- Navegador web para acceder a phpMyAdmin y WordPress


## 7. Material de apoyo.

- Documentación oficial de Docker
- Documentación oficial de MySQL
- Documentación oficial de phpMyAdmin
- Documentación oficial de WordPress
- Guía proporcionada en la asignatura


## 8. Procedimiento

## Parte 1: Crear los contenedores necesarios para un sitio WordPress, utilizando únicamente comandos de Docker.

### Paso 1:Crear una red 
Se crea una red personalizada de tipo bridge en Docker. Esta red permitirá que los contenedores puedan comunicarse entre sí de forma segura y controlada mediante nombres internos.

<img src="00.jpg" alt="Paso1" width="800">

### Paso 2:Crear un volumen para wordpress
Se genera un volumen persistente para almacenar los archivos del CMS WordPress. Este volumen asegura que los datos no se pierdan si el contenedor se reinicia o elimina.

<img src="2.jpg" alt="Paso2" width="800">

### Paso 3: Crear un volumen para mysql
Se crea un volumen dedicado para almacenar los datos de la base de datos MySQL. Este volumen garantiza la persistencia de las tablas, configuraciones y registros.

### Paso 4: Crear un contenedor para mysql
Se levanta un contenedor con la imagen oficial de MySQL y se asocian las variables de entorno necesarias para su configuración. También se vincula al volumen creado previamente y se conecta a la red personalizada.

<img src="4.jpg" alt="Paso4" width="800">

### Paso 5: Crear un contenedor para phpmyadmin
Se ejecuta un contenedor con phpMyAdmin para administrar gráficamente la base de datos MySQL desde el navegador. Este contenedor también se conecta a la red personalizada y se vincula con el contenedor de la base de datos.

<img src="5.jpg" alt="Paso5" width="800">

### Paso 6: Crear un contenedor de wordpress
Se levanta el contenedor que contiene WordPress y se configura para conectarse con la base de datos ya existente. El contenedor se une a la red, se le asigna un volumen para los archivos y se exponen los puertos necesarios para su acceso web.

<img src="5.jpg" alt="Paso6" width="800">

## 9. Resultados esperados:

- Los contenedores de WordPress, MySQL y phpMyAdmin estarán correctamente conectados mediante la red personalizada.
- Se podrá acceder a WordPress desde el navegador y completar su configuración inicial.
- Se podrá gestionar la base de datos WordPress desde phpMyAdmin.
- Se comprueba la persistencia de los datos en caso de reinicio de los contenedores gracias al uso de volúmenes.
- Se fortalece el entendimiento práctico de la implementación de servicios web usando Docker.

## 10. Bibliografía

-Docker Inc. (2024). Docker documentation. https://docs.docker.com

- Miell, I., & Sayers, A. (2019). Docker in practice (2nd ed.). Manning Publications.

- MySQL Documentation Team. (2024). MySQL 8.0 reference manual. https://dev.mysql.com/doc/

- Nickoloff, J., & Kuenzli, S. (2019). Docker in action (2nd ed.). Manning Publications.

- phpMyAdmin. (2024). phpMyAdmin documentation. https://docs.phpmyadmin.net/

- WordPress.org. (2024). WordPress documentation. https://wordpress.org/support/


