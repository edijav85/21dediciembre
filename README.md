# DEBER DE TECNOLOGÍAS WEB CON JAVASCRIPT
-------------------------------------------
###Materia: Tecnologias Web con Java Script
###Tema: Introduccion a la Web
###Fecha: 21/12/2016
###Profesor:TANIA CALLE Y ADRIAN EGUEZ

#INDICE DE CONTENIDOS
-------------------------------------------
- <a href="#tema">Tema</a>
- <a href="#objetivos">Objetivos</a>
- <a href="#marco-teorico">Sails, Assets, Views, Pipelines, Controllers</a>
- <a href="#desarrollo">Desarrollo de la Práctica</a>
- <a href="#conrec">Conclusiones y Recomendaciones</a>

<a name="tema"></a>
## Tema
-Sails, Assets, Views, Pipelines, Controllers

<a name="objetivos"></a>
## Objetivos

- Dar a conocer las principales conceptos que infieren en el uso del framework SAILS JS.
- Dar a conocer los comandos basicos para la istalacion de SAILS

<a name="marco-teorico"></a>
## Marco Teorico
### SAILS
![alt text](http://sailsjs.com/images/logos/sails-logo_ltBg_ltBlue.png)

Es un framework o un Marco de Trabajo hecho en JavaScript en Nodejs con grandes y excelentes beneficios como aplicaciones en tiempo real, querys, modelos relacionales y no relacionales, sesiones y mucho más.
 * Comandos de instalación:
    - npm install -g sails
      + Instala sailsjs globalmente en nuestro sistema operativo

 * Comandos de sails:
    - sails new Aplicación
      + Crea una nueva aplicación en el directorio actual con nombre Aplicación.
    - sails generate controller NuevoControlador
      + Crea un nuevo controllador dentro de nuestra aplicación, llamado NuevoControlador. Internamente se agrega un archivo a la cartpeta     controllers, dentro de la carpeta Api.

### Assets
Los assets son una carpeta dentro del Framework la cual funciona como un servidor web de archivos estáticos, en donde cualquier tipo de archivos que coloquemos en esta carpeta será mostrada al público.  


### Views
Las vistas son las páginas que se va a mostrar al usuario dependiendo de la lógica que tenga nuestra aplicación de sailsjs.


### Rutas
Las rutas son a donde vamos a direccionar nuestro trafico dependiendo los métodos HTTP y el URL de nuestros recursos.
Link Documentación Oficial: Routes


### Controladores
Los controladores dentro de Sailsjs tienen como finalidad brindar los métodos CRUD de nuestros modelos, así también como exponer la lógica de negocio que se defina en la aplicación, como por ejemplo la autenticación.


### Pipeline
En el archivo pipeline.js dentro de la carpeta task se encuentran las diferentes configuraciones de GRUNT que es un automatizador de actividades con JavaScript. Dentro de este podemos configurar los assets que van a ser inyectados en TODAS las vistas de nuestra aplicación en Sailsjs.








###<a name="script_bdd">Script de la BDD</a>
