# Proyecto final de analisis y diseño de sistemas

#### Nombre:
+ ###### Jose Francisco H.
+ ###### Felix Josue Lopez.
+ ###### Kaolanny Rufino Morel.

#### Matrícula:
+ ###### 2022 - 0115
+ ###### 2021 - 0116
+ ###### 2021 - 1089

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

[Video de la prueba de funcionamiento](https://drive.google.com/file/d/1yNd1l1tBnjhrsyk9LbsGYGdgn2KdwTML/view?usp=share_link)

<hr>

## Conclusiones y mejoras:

###### Este proyecto cuando tuve la oportunidad de analizarlo brevemente me di cuenta de que las cosas mas importantes se encuentran en la parte de nginx, server y worker, la parte del cliente es de solo diseño de ahí importante importante podríamos sacar el js que se llama fib.js que básicamente lo que hace es calcular el fibonacci de la serie de números que digitemos. Y los almacena como anteriormente he dicho en la base de datos de redis para posteriormente este archivo sacar los datos directamente desde redis y postgres, porque la data que pasa por redis termina almacenandose en postgres.

#### Mejoras

+ 1. ###### Me di cuenta de que en el input cuando le doy a enviar directamente no me hace nada, es decir que tengo que volver a recargar la página para que me haga el fibonacci de ese número que digité, y para corregirlo simplemente fui a la carpeta client.

    +  ###### Fui a la carpeta client.
    +  ###### Fui al archivo de fib.js
    +  ###### Fui a la linea 29 del codigo y le puse lo siguiente...
        + ###### this.fetchValues();
        + ###### this.fetchIndexes(); 

+ 2. ###### Le mejoraria un poco mas el diseño de la estructura front-end del código debido a que es un poco no atractible pero de igual forma tiene un excelente funcionamiento en el back-end.

+ 3. ###### A ciertas personas le causó error el hecho de que en los docker-file.dev no se encontraba el comando RUN npm install nodemon, y al parecer a computadoras sin permisos de usuario autorizados no le instalaba el express, pero nodemon fue un error debido a que simplemente no se puso el comando, a mi no me dio ningun error porque yo ya tenia nodemon en mi computadora y todos los packages requieridos, tambien de express, pero esa seria la otra modificacion que yo le realicé.