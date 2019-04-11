# Test Desafío Latam

*A través de este repositorio se pretende dar respuesta a las preguntas solicitadas por Susana de Desafío Latam, de acuerdo al correo reproducido a continuación:*

> *De acuerdo a lo conversado con respecto a la creación de nuestra nueva carrera Desarrollo Full Stack Java, ésta se encuentra distribuida en módulos, los cuáles se tiene considerado*:
>
> __Módulo 1__: Fundamentos de Desarrollo Web 
> Contenidos: HTML, CSS, Bootstrap, Javascript, Terminal, Repositorios
>
> __Módulo 2__: Introducción a la programación con Java 
> Contenidos: Introducción a la programación, flujo, ciclos, métodos, orientación a objetos, api (colecciones), uml, junit
> 
> __Módulo 3__: Introducción a base de datos
> Contenidos: Oracle SQL Server, Modelo entidad-Relación.
> 
> __Módulo 4__: Desarrollo de aplicaciones web con Java
> Contenidos: Java Servlets, JavaServer Pages, Tomcat, Patrón de diseño MVC, Conexión a una BD mediante JBBD
> 
> __Módulo 5__: Spring Framework
> Contenidos: Spring MVC - Spring con maven, JDBCtemplate, AOP, RestTemplate, Spring Security, JPA con Spring, JSON web Token
> 
> __Módulo 6__: Proyecto Full Stack Java
> Aquí los alumnos desarrollarán un proyecto en el cual aplicarán todo lo aprendido en los 5 módulos anteriores.
>
> *Dado los contenidos indicados, se requiere un feedback de los módulos 4 y 5, en cuánto a qué necesita el alumno adquirir para obtener la certificación de Desarrollador Full Stack Java. (Puedes realizar los ajustes que estimes conveniente).*
> 
---
Considerando los contenidos de los módulos mi feedback es el siguiente:
### Para la carrera en general
Considerar una unidad que interiorice al alumno con algún entorno de desarrollo integrado (IDE), tal como eclipse o intellij, esto debido a que, a diferencia de ruby java es un lenguaje estático, fuertemente tipado y mucho más verboso por lo que el desarrollo sin este tipo de herramientas lo hace sumamente complicado, sobre todo considerando el background de los alumnos.

El uso de maven se podría considerar desde el módulo de introduccion a java o desde el 4, de forma en que se interioricen más con eso que se usa de manera prácticamente estándar dentro de la industria actualmente

### Para el módulo 4

Dado el punto anterior agregaría una unidad introductoria al IDE y las lecturas serían guíadas a través de las operaciones que permite este último. Por ejemplo: 
   * Crear en eclipse un nuevo proyect web dinámico
   * Seleccionar como servidor de aplicaciones tomcat
   * ...

Explicación del patron MVC a nivel teórico dado que la implementación de este en el lenguaje puede llevar a confusión
### Para el módulo 5
Es escencial que se considere spring Core (El contenedor IOC de spring), que quede claro para los alumnos el concepto de inyeccion de dependencias y como lo resuelve spring.

Considerar guiar el desarrollo utilizando [Springboot](https://spring.io/projects/spring-boot) y su [inicializador](https://start.spring.io/), de manera de concentrarse en todo lo que provee el framework que es bastante.

Considerar introducir el uso de un motor de plantillas como Thymeleaf, que permite una mejor y más fácil integración entre el html puro y el código Java en comparación a JSP.

---
> *Además, necesitamos que respondas las siguientes preguntas:*
>
> * *¿Qué es lo mínimo que debe adquirir el alumno para integrarse a un equipo de trabajo y desempeñarse como Desarrollador Full Stack Java?*
---
El alumno debe adquirir las siguientes habilidades para poder desempeñarse como desarrollador fullstack java
* Conocimiento sobre el lenguaje Java y Programación orientada a objetos.
* Conocimiento sobre HTML, CSS, Javascript. Dependiendo del caso podría ser necesario conocer sobre algun framework javascript en particular (React, Angular, Vue, etc).
* Entendimiento del ciclo de vida y los componentes y patrones escenciales de la arquitectura web para Java (Servlets, MVC, JSP)
* Conocimiento del framework Spring, principalmente de los módulos MVC, Core (IoC Container) y JPA
* Conocimiento sobre el uso de administradores de paquetes modernos en Java, Maven /Gradle principalmente

---
> * *¿Cuándo se debe utilizar JWT en Java, y cómo lo implementarías en un proyecto?*
---
JWT (Json Web Token) es un estándar para tokens de acceso a recursos, utilizado generalmente para transportar información básica del usuario y/o autorizar el acceso a algún recurso u operación web. Dentro del ecosistema Java su uso se da generalmente cuando queremos autorizar recursos y operaciones contra servicios Rest, ya que la aplicación cliente (App web con algún framework JS o aplicaciones móviles), envian el token JWT en los headers de cada peticion y los servicios rest, validan que el token sea válido y que cuente con los permisos necesarios para operar.

Una implementación sencilla consiste en lo siguiente:
1. Crear un servicio/endpoint especializado que permita validar un usuario y password el cual retorne un token JWT con información básica del cliente y los roles asociados al usuario. Utilizando la biblioteca de spring security respectiva para jwt (spring-security-jwt)
   * ```Ejemplo: login-service -> endpoint -> POST /login ```
2. Crear un servicio que acceda a alguna base de datos u obtenga información, el cual sea capaz de validar el token JWT obtenido con el servicio "login-service". Para esto se utiliza la misma biblioteca que login service solo que se solicita la autorización utilizando la anotacion ```@PreAutorize```
3. Las aplicaciones obtendran el token a través de login-service y enviaran dicho token en la cabecera ```Autorization```

---
> * *Realizar demostración de cómo debe ser explicado el patrón de diseño de MVC a un alumno*
---
##### Patron MVC

El patron MVC (Modelo Vista Controlador) es un patron compuesto que se utiliza principalmente para resolver uno de los problemas más comunes que tienen los desarrolladores web, el cual consiste en separar la lógica de presentación (Vista) de la lógica del negocio (Modelo).

![Patron MVC](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a9/ModelViewControllerDiagram_es.svg/220px-ModelViewControllerDiagram_es.svg.png)

Para ello el patron MVC consta de tres partes, tal cual su nombre lo indica sus partes son las siguientes
* Modelo: El modelo es el responsable de contener los datos y/o estado de un objeto que se desea mostrar en la Vista
* Vista: La vista es la responsable de representar, en este caso a través de una página web, los datos provistos por el "Modelo"
* Controlador: El controlador es el reponsable de coordinar que las acciones que se gatillan desde la vista (clicks, cargas, etc) se reflejen  en el modelo respectivo y que este sea a su vez enviado a la vista correspondiente.

* 
---
> * *Crear un ejemplo guiado de serialización y deserialización usando Spring MVC y JSON* 
---
//TODO
