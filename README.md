# DEBER DE TECNOLOGÍAS WEB CON JAVASCRIPT
-------------------------------------------
###Materia: Tecnologias Web con Java Script
###Tema: Introduccion a la Web
###Fecha: 21/12/2016
###Profesor:TANIA CALLE Y edison logacho

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
<div align="center"><img src="http://sailsjs.com/images/logos/sails-logo_ltBg_ltBlue.png"></div>

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

###<a name="#desarrollo">PRACTICA</a>

## Comandos Importantes

### Instalar sailsjs

Sailsjs es un servidor web que se conecta a bases de datos y puede funcionar con aplicaciones en tiempo real, ayudandonos a crear REST APIs.

´´´
> npm install -g sails
´´´

El -g nos deja utilizarlo globalmente.

### Crear un proyecto en Sailsjs

´´´
> sails new NombreProyecto
´´´

### Levantar el servidor

´´´
> sails lift
´´´


´´´
> node app.js
´´´

El sails les pide opciones si no estan definidas, las opciones son:

- 1: SAFE MODE no se va a alterar la base de datos
- 2: ALTER MODE se va a alterar la base de datos si nosotros hicimos cambios en los modelos por ejemplo
- 3: DELETE MODE borra todos los datos de la base y vuelve a crear los modelos

## Servidor Web de Sailsjs

El servidor web de sails se encuentra localizado en la carpeta **assets**


## Generar Controladores Sailsjs

´´´
> sails generate controller NombreControlador
´´´

## Generar Modelos en Sailsjs

´´´
> sails generate model NombreModelo
´´´

## Generar APIs en Sailsjs

´´´
> sails generate api NombreAPI
´´´

Un Api es la fusión de un **Controlador** y de un **Modelo**.

# API REST

## Modelo Usuario

### Crear Usuarios

URL:

´http://localhost:1337/Usuario´

Metodo HTTP:

´POST´

Datos:


´´´javascript
{
    nombre:'edison',
    apellido:'logacho',
    correo:'edison.logacho@epn.edu.ec'
}
´´´


### Buscar Usuarios

URL:

´http://localhost:1337/Usuario´

Metodo HTTP:

´GET´

Datos:


´´´javascript
[
  {
    "nombres": "edison",
    "apellidos": "logacho",
    "correo": "edison.logacho@epn.edu.ec",
    "createdAt": "2016-12-21T18:57:16.362Z",
    "updatedAt": "2016-12-21T18:57:16.362Z",
    "id": 1
  },
  {
    "nombress": "javier",
    "apellidoss": "iza",
    "correos": "javier.iza@epn.edu.ec",
    "correo": "correo@invalido.com",
    "createdAt": "2016-12-21T18:58:00.888Z",
    "updatedAt": "2016-12-21T19:06:31.603Z",
    "id": 2,
    "nombre": "Carlos",
    "casa": "Azul",
    "mouse": "negro"
  }
]
´´´

### Buscar Usuario por ID

URL:

´http://localhost:1337/Usuario/1´

Metodo HTTP:

´GET´

Datos:


´´´javascript
  {
    "nombres": "edison",
    "apellidos": "logacho",
    "correo": "edison.logacho@epn.edu.ec",
    "createdAt": "2016-12-21T18:57:16.362Z",
    "updatedAt": "2016-12-21T18:57:16.362Z",
    "id": 1
  }
´´´

### Borrar Usuarios

URL:

´http://localhost:1337/Usuario/1´

Metodo HTTP:

´DELETE´

Datos:


´´´javascript
  {
    "nombres": "edison",
    "apellidos": "logacho",
    "correo": "edison.logacho@epn.edu.ec",
    "createdAt": "2016-12-21T18:57:16.362Z",
    "updatedAt": "2016-12-21T18:57:16.362Z",
    "id": 1
  }
´´´

### Actualizar Usuarios

URL:

´http://localhost:1337/Usuario/1´

Metodo HTTP:

´PUT´

Datos:


´´´javascript
  {
    "nombres": "edison",
    "apellidos": "logacho",
    "correo": "edison.logacho@epn.edu.ec",
    "createdAt": "2016-12-21T18:57:16.362Z",
    "updatedAt": "2016-12-21T18:57:16.362Z",
    "id": 1
  }
´´´


## Blueprint API

### Shortcuts

Con los shortcuts tenemos la posibilidad de crear borrar y actualizar mediante solamente un URL en sails


´´´
http://localhost:1337/Usuario/create?nombres=edison&apellidos=Lucho

http://localhost:1337/Usuario/destroy/1

http://localhost:1337/Usuario/update/1?nombres=Fernando

´´´
