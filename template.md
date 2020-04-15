# Especificación de requisitos 
## Del proyecto Musync

Versión 0.1  
Generada por Rubén Castro Ruiz  
Musync  
12/04/2020  

Índice
=================
* [Versiones](#versiones)
* 1 [Introducción](#1-introducción)
  * 1.1 [Objetivo del documento](#11-objetivo-del-documento)
  * 1.2 [Ámbito del proyecto](#12-ámbito-del-proyecto)
  * 1.3 [Resumen del documento](#15-resumen-del-documento)
* 2 [Vista general del producto](#2-vista-general-del-producto)
  * 2.1 [Perspectiva del producto](#21-perspectiva-del-producto)
  * 2.2 [Funciones del producto](#22-funciones-del-producto)
  * 2.3 [Restricciones del producto](#23-restricciones-del-producto)
  * 2.4 [Perfiles de usuario](#24-perfiles-de-usuario)
  * 2.5 [Suposiciones y dependencias](#25-suposiciones-y-dependencias)
* 3 [Interfaces externas](#3-interfaces-externas)
    * 3.1 [Interfaces con el Usuario](#31-interfaces-con-el-usuario)
    * 3.2 [Interfaces con el Hardware](#32-interfaces-con-el-hardware)
    * 3.3 [Interfaces con el Software](#33-interfaces-con-el-software)
* 4 [Requisitos](#4-requisitos)
  * 4.1 [Precedencia y prioridad](#41-precedencia-y-prioridad) 
  * 4.2 [Funcionales](#42-funcionales)
  * 4.3 [Calidad de Servicio](#43-calidad-de-servicio)
    * 4.3.1 [Rendimiento](#431-rendimiento)
    * 4.3.2 [Seguridad](#432-seguridad)
    * 4.3.3 [Fiabilidad](#433-fiabilidad)
  * 4.5 [Diseño e implementación](#45-diseño-e-implementación)
    * 4.5.1 [Instalación](#451-instalación)
    * 4.5.3 [Mantenimiento](#453-mantenimiento)
    * 4.5.6 [Coste](#456-coste)
    * 4.5.7 [Fecha de Entrega](#457-fecha-de-entrega)
* 5 [Verificación](#5-verificación)
## Versiones
| Name   |    Date    | Reason For Changes                 | Version |
| ------ | :--------: | ---------------------------------- | ------: |
| Musync | 12/04/2020 | Empezar el diseño de la aplicación |   0.1.0 |

## 1. Introducción
### 1.1 Objetivo del documento
En este documento se pretende exponer los requisitos del proyecto para la asignatura, llamado Musync.

### 1.2 Ámbito del proyecto
El proyecto consta de una aplicación web progresiva que gracias al framework en el que esta desarrollada, podrá ser usada además de en navegadores web, en sistemas operativos Android e iOS.

Gráficamente seria un sistema de publicaciones de anuncios, a los cuales pues acceder sin registro previo para visualizarlos. Una vez te registras también puedes crear, editar y eliminar tus propios anuncios. El objetivo es tener una buena base en cuanto al sistema de usuarios y anuncios y posteriormente si es posible implementar mensajería interna para aumentar el ámbito del sistema.

En esta aplicación los músicos podrán ofrecerse para tocar en alguna banda o buscar miembros para su banda, mediante un sistema de búsqueda de anuncios y búsqueda de músicos.

### 1.3 Resumen del documento
Este documento contiene los requisitos que necesita el sistema para funcionar y los casos de uso y funcionalidades que realizan la aplicación.

## 2. Vista general del producto
### 2.1 Perspectiva del producto
El sistema surge con la idea de un compañero, el cual es músico y al que le gustaría que existiese esta aplicación porque se la imagina muchas veces cuando toca en una banda y falta alguien, porque se pone malo, se rompe el instrumento o cualquier momento.
Ese problema se podría solucionar con esta app que le envía una notificación al usuario que esta en su casa con ganas de tocar un instrumento pero no tiene grupo donde tocar.

### 2.2 Funciones del producto
Las funciones de las que dispone la aplicación son la administración de usuarios, soporte para administradores y usabilidad para los músicos.

​	Administración de usuarios: 
Los usuarios podrán registrarse, iniciar sesión, cerrar la sesión y editar su usuario. En la edición del usuario entran el nombre de usuario, la contraseña, la imagen de perfil, la descripción y los instrumentos que tocan. Además si no desean pertenecer mas a Musync, eliminar su usuario.

​	Soporte para administradores:
Los administradores sol usuarios que pueden reportar usuarios y publicaciones, si un usuarios ha sido reportado reiteradas veces, también se podrá eliminar la cuenta por completo. Cuentan con un visor de reportes, que los músicos notifican, pero son los administradores los que toman la decisión.

​	Músicos:
Los músicos son usuarios del sistema que pueden listar, crear, editar y eliminar anuncios en el sistema, además de notificar a los administradores de infracciones de usuarios o publicaciones cuentan con un sistema de calificación entre ellos en el que se evalúan mediante la relección que mantienen.

### 2.3 Restricciones del producto
Las restricciones que se podrían tener en el proyecto es la falta de tiempo y el despliegue puede tener, ya que no disponemos de capital para su necesaria publicidad y el ámbito de clientes es solo músicos, por lo que cerramos abanico en ese aspecto. Si se diese ese caso, podríamos abrirla más y crear secciones para deportistas, por ejemplo, que busquen un jugador para sus equipos o jugadores que busquen un equipo donde jugar etc. De este modo abriríamos el abanico a más público.

### 2.4 Perfiles de usuario
Como ya se ha comentado antes existen los usuarios administradores y los usuarios músicos. Además contamos con otro tipo de usuario, el cual no esta registrado en el sistema, "Músico no registrado" este solo puede ver los anuncios que hay en la aplicación y hacer consultas. Si desea hacer algo más deberá registrarse, para conseguir las funciones del usuario músico. El usuario músico, además, tiene permiso para crear, editar y eliminar sus publicaciones, además, reportar publicaciones y músicos, para que el usuario administrador quede notificado y proceda a eliminar o reportar.

### 2.5 Suposiciones y dependencias
Las dependencias son los framework que usamos, estamos sujetos a ellos, un mal soporto o que dejen de da soporte podría ser un gran riesgo.
También estamos a disposición del gusto de los usuarios, existen mas aplicaciones para músicos y aunque la nuestra sea la mejor app del mundo esta sujeta a la moda y a la comunidad haya.

### 3 Interfaces externas
#### 3.1 Interfaces con el usuario 

Las interfaces con las que contamos serán:

​	Tablón de anuncios:
Sera el index de la app, es donde aparecerán los anuncios mas nuevos del sistema.

​	Búsqueda de anuncios:
Se podrá buscar los anuncios en dos partes, búsqueda de músicos y búsqueda de bandas. Con filtros para buscar por instrumento, por fecha o por lugar

​	Anuncio:
Cuando vemos un anuncio podemos acceder a el para verlo mas detalladamente.

​	Búsqueda de músicos:
Se podrá buscar músicos con filtro por instrumentos y lugares.

​	Músico:
Cuando encuentras un músico en una busqueda o clicas en el musico de un anuncio podrás acceder a su perfil de usuario.

​	Perfil propio:
Puedes acceder a tu perfil para modifícalo y para ver, crear, editar o modificar tus anuncios.

​	Reportes:
Es una sección del administrador, donde puede ver los reportes de los músicos y hacer sus reportares

#### 3.2 Interfaces con el Hardware
A la aplicación se podrá acceder mediante un navegador web, por lo cual abre mucho terreno a muchos sistemas operativos que dispongan de navegador e internet.

En dispositivos Android e iOS, será instalable gracias a framework con que trabajamos.

#### 3.3 Interfaces con el Software
La aplicación usará protocolo HTTP y HTTPS mediante el framework ionic y angular, de esta forma se comunicará la aplicación. La base de datos también usa estos protocolos puesto que disponemos de firebase, un sistema de datos NoSQL de Google, que nos retorna objetos JSON.


## 4. Requisitos
### 4.1 Precedencia y prioridad
| Id   | Nombre                  | Descripción                                                  | Prioridad   | Precedencia | Tipo         |
| ---- | ----------------------- | ------------------------------------------------------------ | ----------- | ----------- | ------------ |
| R1   | Buscar anuncios         | Un músico sin registro previo puede hacer consultas en la app para buscar anuncios. | Fundamental |             | Funcional    |
| R2   | Ver anuncio             | Seleccionando un anuncio puedes acceder a el y verlo de forma mas detallada. También se puede acceder mediante su link HTTP GET | Fundamental |             | Funcional    |
| R3   | Acceso                  | En esta sección de la aplicación los usuarios pueden registrarse e iniciar sesión. | Fundamental |             | Funcional    |
| R4   | Registrarse             | El usuario debe introducir el nombre de usuario, el correo electrónico y la contraseña. Para poder tener acceso a la web como usuario. | Fundamental | R3          | Funcional    |
| R5   | Iniciar sesión          | El usuario ya registrado en el sistema puede iniciar sesión para entrar a la app. | Fundamental | R3          | Funcional    |
| R6   | Tablón de anuncios      | Cuando el usuario accede a la aplicación se muestran todos los anuncios que se han creado ordenados por fecha de creación. | Fundamental | R5          | Funcional    |
| R7   | Ver mi perfil           | Puedes acceder a tu usuario en el cual aparecen tus publicaciones y tus datos los cuales puedes editar con un botón. | Fundamental | R5          | Funcional    |
| R8   | Editar usuario          | Esta sección te permite cambiar tu nombre de usuario, correo electrónico, imagen de perfil, descripción, instrumentos que tocas y localidad | Fundamental | R7          | Funcional    |
| R9   | Crear publicación       | En tu perfil te da la opción de crear una publicación, en la que especifica si buscas banda o músico, que instrumento, tocar, en que lugar y para que fecha | Fundamental | R7          | Funcional    |
| R10  | Editar publicación      | Cuando tiene una publicación, te aparece un botón en ella, para editarla, si clicas sobre él, puedes modificar los datos ya creados. | Fundamental | R7          | Funcional    |
| R11  | Eliminar publicación    | Cuando tienes una publicación creada, te aparece un botón para borrarla | Fundamental | R7          | Funcional    |
| R12  | Reportar publicación    | Cuando ves algo poco ético en algún anuncio, puedes darle al botón de reportar y describir por que lo has hecho. Los administradores lo verán | Deseable    | R2          | Funcional    |
| R13  | Búsqueda de usuarios    | Puedes buscar usuarios, por nombres o instrumentos           | Fundamental | R5          | Funcional    |
| R14  | Ver otro perfil         | Cuando haces una busque de usuarios o ves un usuario en algún anuncio, puedes clicar en su nombre y acceder a su perfil. | Fundamental |             | Funcional    |
| R15  | Reportar músico         | Cuando ves algo poco ético en algún perfil, puedes darle al botón de reportar y describir por que lo has hecho. Los administradores lo verán | Deseable    | R14         | Funcional    |
| R16  | Sistema de mensajería   | Cuando accedes a un perfil puedes pulsar el botón enviar mensaje, donde podrás escribirte con otro musico para hablar sobre un anuncio. | Opcional    | R14         | Funcional    |
| R17  | Puntuar músico          | Un músico puede puntuar a otro músico con una valoración de 5 estrellas | Deseable    | R14         | Funcional    |
| R18  | Reportar anuncio        | Si un administrador recibe una notificación o encuentra un anuncio poco ético puede reportarlo, eliminándolo de las publicaciones | Deseable    | R12         | Funcional    |
| R19  | Reportar músico         | Si un administrador recibe una notificación o encuentra un musico poco ético puede reportarlo, cerrando su usuario por un tiempo limitado. | Deseable    | R15         | Funcional    |
| R20  | Eliminar usuario        | Si un administrador ve repetidas conductas negativas en un músico, puede eliminarlo del sistema para que no vuelva a molestar | Deseable    | R19         | Funcional    |
| R21  | Control de calidad      | La aplicación la probaran usuarios sin experiencia para comprobar cuales son los porcentajes de facilidad de experiencia de usuario que tiene el sistema. Se espera un 75% | Deseable    |             | No funcional |
| R22  | Testing                 | Se harán pruebas de testing para que el sistema sea eficiente y no haya fallos de ejecución. | Deseable    |             | No funcional |
| R23  | Velocidad de consultas  | El sistema debe ser rápido para que el usuario no se canse de esperar y salga de la aplicación. | Deseable    |             | No funcional |
| R24  | Mantenimiento           | La aplicación tendrá mantenimiento por ingenieros que la mantendrán actualizada y a prueba de errores | Fundamental |             | No funcional |
| R25  | Acceso premium          | Cuando la aplicación tenga todas las características esperadas, se hará un acceso premium, será un pago único el cual proporcionará funcionalidades extra como poder crear mas publicaciones y no tener anuncios de empresas en la app. | Opcional    |             | No funcional |
| R26  | Coste del producto      | El coste de crear el sistema                                 | Fundamental |             | No funcional |
| R27  | Comunicación HTTPS      | La conexión de la aplicación será por HTTPS, lo cual hace que la comunicación sea segura porque viaja cifrada. | Deseable    |             | No funcional |
| R28  | Contraseñas encriptadas | Las contraseñas en el servidor serán encriptadas, como defensa a ataques a la base de datos | Deseable    |             | No funcional |
|      |                         |                                                              |             |             |              |



### 4.2 Funcionales

![Diagrama de casos de uso](C:\Users\ruben\Documents\MEGA\Estudios\Universidad\Asignaturas\2Curso\2Cuatrimestre\Introduccion_a_la_Ingenieria_de_Software\trabajos\5_Casos_de_uso_Y_requisitos\requisitos\Diagrama de casos de uso.svg)

Como ya se han especificado y descrito en el apartado anterior los requisitos tipo funcionales, aquí se puede observar un diagrama de los casos de uso donde se pueden ver como los actores pueden interactuar con el sistema.

Tenemos el usuario sin registrar, el cual solo puede Visualizar perfiles, buscar publicaciones y ver publicaciones en detalle.

Cuando ya te registras puede realizar mas funciones de usuario como es iniciar sesión, cerrar sesión, editar tu perfil, eliminarlo y hacer consultas de perfiles

Una vez estás registrado, desarrollas un rol que puede ser de administrador o músico.

Si eres músico, se te permite crear, editar y eliminar rus publicaciones, acceder al sistema de mensajería y hacer reportes, tanto de músicos como de anuncios.

Si eres un administrador, puedes acceder a los reportes de músicos y decidir reportar perfiles y músicos.



Requisitos funcionales:

### R1 - Buscar anuncios.

#### 	Descripción:

Un usuario cualquiera sin registro previo debe poder accede a esta función de buscar y filtrar anuncios mediante campos como instrumento, fecha o lugar. Es importante para que cualquiera que la vea pueda hacer un uso "beta" de ella y si le gusta, ya podría registrarse, incluso poder compartir enlaces de anuncios con amigos que no tendrán que registrarse tampoco para poder verlos y poder que también se registren si les gusta.

#### 	Dependencias:

No Tiene.

#### 	Prioridad:

Fundamental.

#### 	Justificación:

Una interfaz necesaria.



### R2 - Ver anuncio

#### 	Descripción:

Cuando un usuario hace búsquedas de anuncios recibe un montón de anuncios resumidos, esta funcionalidad es importante, para poder ver en detalle cada anuncio y poder compartirlo como se menciona en el requisito anterior.

#### 	Dependencias:

No tiene.

#### 	Prioridad:

Fundamental

#### 	Justificación:

Una interfaz necesaria.



### R3 - Acceso  

#### 	Descripción:

Esta funcionalidad es importante para que los usuarios puedan acceder a sus perfiles o registrarse si no lo están.

#### 	Dependencias:

No tiene

#### 	Prioridad:

Fundamental

#### 	Justificación:

Una interfaz necesaria



### R4 - Registrarse 

#### 	Descripción:

Funcionalidad importante para que los usuarios no registrados puedan registrarse y tener acceso a las funcionalidades de músico. Deben introducir Su nombre de usuario, correo electrónico y la contraseña.

#### 	Dependencias:

R3

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R5 - Iniciar sesión

#### 	Descripción:

Funcionalidad importante para que los usuarios del sistema puedan acceder, deben introducir su nombre de usuario y contraseña.

#### 	Dependencias:

R3

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R6 - Tablón de anuncios

#### 	Descripción:

Esta funcionalidad es importante para que el usuario pueda ver los nuevos anuncios que se han creado en la app, recién iniciar sesión.

#### 	Dependencias:

R5

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R7 - Ver mi perfil

#### 	Descripción:

Interfaz necesaria para poder editar tu usuario, crear anuncios, editarlos y eliminarlos.

#### 	Dependencias:

R5

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R8 - Editar usuario

#### 	Descripción:

Funcionalidad importante para poder tener acceso a cambiar imagen de perfil, cambiar contraseña, cambiar nombre de usuario, editar descripción, editar instrumentos que tocas y eliminar usuario. Pedirá confirmación.

#### 	Dependencias:

R7

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria



### R9 - Crear publicación

#### 	Descripción:

Funcionalidad importante para que los músicos puedan crear anuncios y dar sentido al sistema.

#### 	Dependencias:

R7

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R10 - Editar publicación

#### 	Descripción:

Funcionalidad importante para que los usuarios puedan modificar las publicaciones en caso de erratas, pedirá confinación.

#### 	Dependencias:

R7

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria.



### R11 - Eliminar publicación

#### 	Descripción:

Funcionalidad importante para cuando el usuario haya conseguido lo que pedía en el anuncio poder eliminar ese anuncio. Pedirá confinación.

#### 	Dependencias:

R7

#### 	Prioridad:

Fundamental.

#### 	Justificación:

Interfaz necesaria.



### R12 - Reportar publicación

#### 	Descripción:

Funcionalidad necesaria para que el el sistema sea pacífico, pedirá una descripción y confirmación.

#### 	Dependencias:

R2

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria.



### R13 - Búsqueda de usuarios

#### 	Descripción:

Funcionalidad importante para que un usuario pueda encontrar a otros usuarios por su nombre o instrumentos que toca.

#### 	Dependencias:

R5

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R14 - Ver otro perfil

#### 	Descripción:

Funcionalidad importante para poder ver en detalle un músico, puedes hacerlo sin usuario registrado para ver su valoración si estas viendo anuncios.

#### 	Dependencias:

No tiene

#### 	Prioridad:

Fundamental

#### 	Justificación:

Interfaz necesaria



### R15 - Reportar músico

#### 	Descripción:

Funcionalidad importante para los usuarios puedan reportar a los músicos si hacen algo malo, pide descripción y confirmación. Luego pasa a manos del administrador.

#### 	Dependencias:

R14

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria



### R16 - Sistema de mensajería

#### 	Descripción:

Funcionalidad importante para que los músicos puedan tener más comunicación en el sistema y tratar los anuncios sin tener que dar datos sensibles como numero de teléfonos o correos electrónicos.

#### 	Dependencias:

R14

#### 	Prioridad:

Opcional

#### 	Justificación:

Interfaz necesaria



### R17 - Puntuar músico

#### 	Descripción:

Funcionalidad importante, para ver si un músico de un anuncio es de fiar, si accedes a su perfil puedes ver la puntuación que tiene y puntuar con hasta 5 estrellas, si es que ya has tenido relección con el, sino podría reportarte por mal uso de la puntuación.

#### 	Dependencias:

R14

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria



### R18 - Reportar anuncios

#### 	Descripción:

Funcionalidad importante para que el administrador pueda reportar los anuncios indeseable. Los anuncios se eliminarán. Pide confirmación.

#### 	Dependencias:

R12

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria



### R19 - Reportar músico

#### 	Descripción:

Funcionalidad importante para que el administrador pueda cerrar la sesión a un músico si comete una fechoría por un tiempo limitado. Pide confirmación.

#### 	Dependencias:

R15

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria



### R20 - Eliminar usuario

#### 	Descripción:

El administrador puede eliminar la cuenta a un músico si ha sido reportado varias veces y no escarmienta.

#### 	Dependencias:

R19

#### 	Prioridad:

Deseable

#### 	Justificación:

Interfaz necesaria



### 4.3 Calidad de Servicio
#### 4.3.1 Rendimiento

El rendimiento es importante en una aplicación como esta, es para sacar de apuros a un grupo a que se le ha podido ir un miembro y necesitan buscar otro, si pierden el tiempo esperando, acaban saliendo de la app y eso implica desinstalarla y perder miembros.

### R23 - Velocidad de consultas:

####		Descripción:

La base de datos debe de ser rápida para que no tarde mas de 1 segundo en responder.

#### 	Dependencias: 

No hay

#### 	Prioridad: 

Deseable.

#### 	Justificación:

El usuario no debe abandonar la aplicación por perdida de tiempo en respuestas de la aplicación



#### 4.3.2 Seguridad
La aplicación utilizará HTTPS, en la cual toda la comunicación irá cifrada.
La contraseña de un usuario en el servidor ira encriptada para que si la base de datos es hackeada, no haga robos de cuentas.

### R27 - Comunicación HTTPS:

####		Descripción:

La conexión esta cifrada por lo que no pueden obtener nada haciendo MITM capturando paquetes, porque esos datos no son útiles.

#### 	Dependencias: 

No hay

#### 	Prioridad: 

Deseable.

#### 	Justificación:

Los usuarios no pueden sufrir suplantaciones de identidad



### R28 - Contraseñas encriptadas:

####		Descripción:

Las contraseñas estarás en la base de datos encriptadas mediante salt, para que no puedan obtener nada si los crackers acceden a la base de datos. La contraseña entrará como texto plano por el formulario de inicio de sesión (que mediante la encriptación HTTPS no podrán obtener), el lenguaje de programación la encriptará y comparará con la contraseña encriptada de la base de datos.

#### 	Dependencias: 

No hay.

#### 	Prioridad: 

Deseable.

#### 	Justificación:

Los usuarios no pueden sufrir suplantaciones de identidad.



#### 4.3.3 Fiabilidad
Es importante que la aplicación sea fiable, gracias a estos requisitos y los de seguridad, la aplicación será fiable.

### R21 - Control de usabilidad:

####		Descripción:

La aplicación será probada por usuarios sin experiencia para comprobar el porcentaje de error que debe de ser mayor de 75%, 

#### 	Dependencias: 

No hay

#### 	Prioridad: 

Deseable.

#### 	Justificación:

Un riesgo podría ser que la aplicación no se entienda y la gente no la use, con este requisito lo solventaremos



### R22 - Testing:

####		Descripción:

Mientras los programadores implemente la aplicación, los tester, crearan pruebas según el diseño que se ha creado antes de la implementación, la aplicación deberá superar estos test para ser totalmente fiable.

#### 	Dependencias: 

No hay

#### 	Prioridad: 

Fundamental.

#### 	Justificación:

La aplicación no puede tener fallos, este requisito lo solventará



### 4.5 Diseño e implementación

#### 4.5.1 Instalación
Gracias al framework Angular la aplicación será una aplicación web progresiva por lo que no es necesario instalarla, se puede acceder desde el navegador web.

Y por otro lado, gracias a Ionic, se puede hacer instalable para sistemas operativos móviles como Android e iOS.



#### 4.5.3 Mantenimiento
### R24 - Mantenimiento:

####		Descripción:

La aplicación una vez este lista estará manteada y actualizada para el bueno uso de los usuarios, se hará balanceo de carga en caso de pico de usuarios, para que estos no sufran lentitud.

#### 	Dependencias:

Sin dependencias

#### 	Prioridad: 

Fundamental.

#### 	Justificación:

Si la aplicación no tiene mantenimiento podría ir a la deriva en cualquier momento porque depende de muchos servicios externos.



#### 4.5.6 Coste
El coste del proyecto se basa en el sueldo de los programadores, el coste del hosting, cuanta mas gente se registre en el sistema, mas servidores se deben alquilar y el mantenimiento de la aplicación cuando esté en marcha.

### R25 - Acceso premium:

####		Descripción:

Cuando estén todas las bases, para que la app funciones bien se implantara un sistema de pago único premium, el cual quitará anuncios comerciales y añadirá algunas funcionalidades como poder crear más anuncios etc.

#### Dependencias:

No hay

#### 	Prioridad: 

Opcional.

#### 	Justificación:

Es una forma común en muchas aplicaciones de quitarte los anuncios comerciales.



### R26 - Coste de producción:

####		Descripción:

Los costes de producción son los de hosting y salario de programadores.

#### 	Dependencias:

No hay

#### 	Prioridad: 

Fundamental.

#### 	Justificación:

Se debe invertir un poco de dinero para poder lanzarla y ya comenzar a ganar.



#### 4.5.7 Fecha de entrega
El producto tiene como fecha de entrega el día 05/06/2020, para ese día debe estar terminado.

## 5. Verificación
La verificación se realizará con usuarios que prueben la aplicación y no encuentren errores que ya hemos detectado. Es este paso ya deben estar todos los requisitos mínimos y solo queda solucionar errores.
