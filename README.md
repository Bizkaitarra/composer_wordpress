# composer_wordpress

## Introducción
En este repositorio git es creará una instalación de Wordpress usando composer. Se asume que la instalación de composer se ha realizado.
Se instalará Wordpress 4.3 pero cualquier otra versión funcionaría igual.
Se deja también fuera del alcance la configuración de apache para correr Wordpress (creación de un Virtual Host) y la configuración de la base de datos al considerarse cosas triviales.

## Creación de fichero json
Se debe crear un fichero que indique a composer lo que debe instalar así como donde dejar cada uno de los diferentes ficheros y librerías instaladas.
Para ello se instala fancyguy/webroot-installer que permite elegir en qué directorios se quieren instalar las aplicaciones web, en este caso Wordpress.
Se requiere también composer/installers	para indicar donde se deben instalar los plugins y themes de Wordpress.
Se indica la versión de cada paquete a instalar indicando en primer lugar la primera versión del plugin.

## Instalación vía composer
Una vez que se tenga en raiz el fichero json únicamente se deberá hacer uso del siguiente comando
```
composer install
```

