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
---
> * *¿Cuándo se debe utilizar JWT en Java, y cómo lo implementarías en un proyecto?*
---
---
> * *Realizar demostración de cómo debe ser explicado el patrón de diseño de MVC a un alumno*
---
---
> * *Crear un ejemplo guiado de serialización y deserialización usando Spring MVC y JSON* 
