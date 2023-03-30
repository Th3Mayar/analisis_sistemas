# Proyecto final de analisis y diseño de sistemas

#### Nombre:
+ ###### Jose Francisco H.

#### Matrícula:
+ ###### 2022 - 0115

#### Fecha: 
+ ###### 29/03/2023

#### Materia: 
+ ###### Análisis de sistemas

#### Descripción: 
+ ###### Proyecto final de la asignatura, app con react y js

---

## Descripcion general

###### <p style="text-align:justify;">Este project consta de varias parte una de ellas es la parte del cliente y otra del servidor o api, en la parte del cliente se ejecuta la app que es basicamente una app que permite calcular apartir de un numero digitado calcular el Fibonacci de ese numero y la parte del servidor que crea una base de datos llamada values y almacena los valores previamente digitados por teclado en el input para posteriormente ser utilizados para calcular el indice. La parte del server consta de varias partes tambien, estas son la del container de nginx, redis, postgres y api que son los containers de las base de datos y los containers del api donde se realizan las respectivas conexiones a las base de datos porque se utilizan 2 en este caso, la base de datos de redis es la que se encarga de recopilar los datos y la base de datos de postgres es la que almacena los valores introducidos previamente almacenados por redis. Y la parte del cliente es lo que se visualiza en pantalla al usuario.</p>

<hr>

## Marco Teórico

###### Lo que uso el maestro para levantar el proyecto completo fueron diferentes lenguajes de programacion y tecnologias como librerias, base de datos, etc, estas son las siguientes.

+ #### React

    ###### Es una biblioteca Javascript de código abierto diseñada para crear interfaces de usuario con el objetivo de facilitar el desarrollo de aplicaciones en una sola página. Es mantenido por Facebook y la comunidad de software libre.

+ #### node.js

    ###### Node.js® is an open-source, cross-platform JavaScript runtime environment, que se encuentra en la parte del back-end, normalmente el javascript solo se encontraba en el front-end, pero resulta que lo modificaron y a partir de este crearon node.js, que se implementa ahora en la parte del servidor, en el caso de este proyecto, ahi es donde se implementa.


+ #### Api Rest

    ###### Esta parte del project es bastante interesante e importante, porque es la que hace las respectivas conexiones de los puertos ademas de crear la base de datos y almacenar los datos en ella mediante redis, tambien asi crea la conexion entre el usuario y el servidor, para que este se mantenga conectado a ambos, no a 1 a la vez.

+ #### Docker

    ###### Docker es una plataforma de código abierto para crear, implementar y gestionar aplicaciones en múltiples contenedores. Aprenda sobre los contenedores, cómo se comparan con las máquinas virtuales y por qué Docker es tan ampliamente adoptado y utilizado.

+ #### nginx

    ###### Es un servidor web/proxy inverso ligero de alto rendimiento y un proxy para protocolos de correo electrónico. Sirve como puente, para conectar los demas servidores en solo un puerto. <i style="color:red;">En el project escucha en el puerto 80 especificamente el 3050 y este se conecta al cliente/server en el puerto 3000 y la parte de server en el 5000 del api. Ademas, configura que la localizacion /api te mande directamente al contenedor del api, el cual se encuentra en el puerto 5000.</i>

+ #### Worker

    ###### Worker hace posible ejecutar una operación de secuencia de comandos en un subproceso de fondo separado del subproceso de ejecución principal de una aplicación web. La ventaja de esto es que el procesamiento laborioso se puede realizar en un subproceso separado, lo que permite que el subproceso principal (generalmente la interfaz de usuario) se ejecute sin bloquearse o ralentizarse.

+ #### Postgres

    ###### Es un sistema de gestión de bases de datos relacional orientado a objetos, en el project sirve para crear la base de datos mediante postgres y almacenar los datos dentro de ella mediante redis, para posteriormente ser solicitados por redis tambien.

+ #### Redis

    ###### Es un motor de base de datos en memoria, basado en el almacenamiento en tablas de hashes pero que opcionalmente puede ser usada como una base de datos durable o persistente, en el project, redis se encarga de almacenar los datos digitados por el usuario para luego ser almacenados directamente a la base de datos de postgres.

<hr>

## Video (Prueba de funcionamiento)

[Video de la prueba de funcionamiento]()

<hr>

## Conclusiones y mejoras:

#### Mejoras