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

Para instalar la versión 2.0 se cambia el fichero json y se realiza un update.
```
composer update
```

## Resultado final

A continuación adjunto toda la traza de la instalación realizada
```
$ composer install
Loading composer repositories with package information
Updating dependencies (including require-dev)
Package operations: 4 installs, 0 updates, 0 removals
  - Installing fancyguy/webroot-installer (1.0.0): Loading from cache
  - Installing composer/installers (v1.0.16): Loading from cache
  - Installing wordpress (4.3): Loading from cache
  - Installing bizkaitarra/kaixowp (master v1.0): Cloning v1.0 from cache
Writing lock file
Generating autoload files

njgportatil@LAPTOP-9FBVPV79 MINGW64 ~/Desktop/ZeroXIII/UniServerZ/www/prueba/composer_wordpress (master)
$ composer update
Loading composer repositories with package information
Updating dependencies (including require-dev)
Package operations: 0 installs, 1 update, 0 removals
  - Updating bizkaitarra/kaixowp master (v1.0 => v2.0):  Checking out v2.0
Writing lock file
Generating autoload files

njgportatil@LAPTOP-9FBVPV79 MINGW64 ~/Desktop/ZeroXIII/UniServerZ/www/prueba/composer_wordpress (master)
```