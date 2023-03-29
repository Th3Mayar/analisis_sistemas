# Proyecto final de analisis y diseño de sistemas

#### Nombre:
+ ##### Jose Francisco H.

#### Matrícula:
+ ##### 2022 - 0115

#### Fecha: 
+ ##### 29/03/2023

#### Materia: 
+ ##### Análisis de sistemas

#### Descripción: 
+ #### Proyecto final de la asignatura, app con react y js

---

## Descripcion general

##### <p style="text-align:justify;">Este project consta de varias parte una de ellas es la parte del cliente y otra del servidor o api, en la parte del cliente se ejecuta la app que es basicamente una app que permite calcular apartir de un numero digitado calcular el Fibonacci de ese numero y la parte del servidor que crea una base de datos llamada values y almacena los valores previamente digitados por teclado en el input para posteriormente ser utilizados para calcular el indice. La parte del server consta de varias partes tambien, estas son la del container de nginx, redis, postgres y api que son los containers de las base de datos y los containers del api donde se realizan las respectivas conexiones a las base de datos porque se utilizan 2 en este caso, la base de datos de redis es la que se encarga de recopilar los datos y la base de datos de postgres es la que almacena los valores introducidos previamente almacenados por redis. Y la parte del cliente es lo que se visualiza en pantalla al usuario.</p>

<hr>

## Marco Teórico

+ #### nginx

    ##### Es un servidor web/proxy inverso ligero de alto rendimiento y un proxy para protocolos de correo electrónico. Sirve como puente, para conectar los demas servidores en solo un puerto. <i style="color:red;">En el project escucha en el puerto 80 especificamente el 3050 y este se conecta al cliente/server en el puerto 3000 y la parte de server en el 5000 del api. Ademas, configura que la localizacion /api te mande directamente al contenedor del api, el cual se encuentra en el puerto 5000.</i>

+ #### Worker

    ##### Es un servidor web/proxy inverso ligero de alto rendimiento y un proxy para protocolos de correo electrónico. <i style="color:red;">En el project escucha en el puerto 80 especificamente el 3050 y este se conecta al cliente/server en el puerto 3000 y la parte de server en el 5000 del api. Ademas, configura que la localizacion /api te mande directamente al contenedor del api, el cual se encuentra en el puerto 5000.</i>