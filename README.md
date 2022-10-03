## Diseños UML
```mermaid
classDiagram
    class Modelo {
	}
	class Vista {
	}
	class Controlador {
	}
	Controlador ...> Vista;
	Controlador ...> Modelo;
	Vista ..> Gtk : << uses >>
	class Gtk
	<<package>> Gtk
```


# Documentacion
## Diseño
Para la creación de esta aplicación hemos escogido el **patrón MVC**, este patrón convierte el desarrollo de aplicaciones complejas en un proceso mucho más manejable. Permite a varios desarrolladores trabajar simultáneamente en la aplicación.
 Este patrón se basa en la división del desarrollo en tres partes:
- **Modelo:** Es el backend, contiene toda la lógica de la aplicación, en nuestro caso es el *cheathelper.py*
- **Vista:** Es el frontend o la interfaz gráfica del usuario, comunica al usuario con la aplicación y cambia continuamente, en nuestro caso la vista se encuentra implementada en los ficheros *insertar nombre de ficheros*
- **Controlador:** Es el cerebro de la aplicación, comunica el modelo con la vista, se encarga de realizar las peticiones, lanzar los errores y cambiar las pantallas, nuestro fichero controlador es *insertar nombre de fichero*
![Patron MVC](https://www.freecodecamp.org/espanol/news/content/images/size/w1600/2021/06/MVC3.png)
## Clases

> cheathelper.py
 
 modelo de la aplicacion, contiene los comandos de unix, proporcionado en el enunciado
 
> interfaz.py
 
  ficheros con la interfaz de la aplicación, juntos forman la vista, implementados en python usando GTK
  
> diseño-iu.pdf

 fichero con la interfaz estática de la aplicación, croquis inial de la misma
 
> controlador.py

 cerebro de la aplicación, comunica todos los ficheros entre sí, convirtiendo una interacción del usuario en una respuesta
