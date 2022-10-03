## Diseños UML
### Estructura del patron
```mermaid
graph TD;
	Controlador -- Inicia --> Vista;
	Controlador -- Modifica --> Modelo;
	Modelo --> cheathelper.py;
	Vista --> card.py;
	Vista --> Inicio.py;
	Vista --> Not_found.py;
	Vista --> Resultados.py;
	Vista --> Error_Serv.py;
```
### Diagrama de estados
```mermaid
stateDiagram-v2
[*] --> Buscar
Buscar --> Error: No funciona
Buscar --> Encontrado: Funciona
Encontrado --> Resultados: SI
Encontrado --> ErrorBusqueda: NO
ErrorBusqueda --> Buscar
Resultados --> Ampliar
Ampliar --> Buscar
Resultados --> Buscar
Error --> [*]
ErrorBusqueda --> [*]
Resultados --> [*]
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
