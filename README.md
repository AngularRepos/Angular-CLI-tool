# ANGULAR CLI

La idea principal que quía el desarrollo de Angular CLI es crear una herramienta que nos permita crear aplicaciones de angular que sigan los patrones de creación, buenas prácticas y estilo de Angular, así como testar el código y desplegarlo en un entorno de producción. Así podemos crear una nueva aplicación Angular con sólo unos pocos cómandos.  

## Instalación y verificación de Angular CLI

Para instalar Angular CLI debemos asegurarnos de tener instalado cualquier versión de [Node](https://nodejs.org/) superior
a la 8. Para ello, o bien procederemos a instalar Node, si no lo tenemos instalado, o comprobaremos qué versión tenemos instalada utilizando el comando `node -v`.  
A continuación, debemos verificar también qué versión de npm (el gestor de paquetes de Node) tenemos instalada para lo cual utilizamos el comando `npm -v`.  
Para más información, siempre podremos revisar la documentación de la [Guía de inicio de Angular](https://angular.io/guide/quickstart).  
Una vez verificados los requerimientos, podemos proceder a la instalación de Angular CLI con el comando:  

`npm install -g @angular/cli`

donde el parámetro `-g` indica que se instalará la herramienta y todas sus dependiencias de forma global en
nuestra máquina.
Finalizada la instalación podemos verificar la instalacion con los comandos

+ `npm list -g @angular/cli --depth=0`
+ `ng -v`

la que coinciden en ambas respuestas la versión de Angular CLI instaladas.  

## Generar nuevas aplicación de Angular

El comando principal para crear una nueva aplicación de angular es el siguiente:  
`ng new nombre-de-la-aplicación`
donde ng es la llamada a la propia CLI, new es la acción a realizar, es decir, indica que vamos a crear una nueva aplicación y nombre-de-la-aplicación será el nombre de nuestra aplicación. Este comando creará una nueva carpeta con todos los componentes de nuestra aplicación en el  directorio en el que nos encontremos cuando ejecutemos el comando.  
Algunos parámetros para este comando son los siguientes:

+ `--dry-run`: indica qué ficheros van a crearse, pero sin llegar a crearlos.
+ `--skip-install`: genera toda la estructura del proyecto, creando todos los ficheros necesarios, pero sin llegar a ejecutar la instalación, lo que conlleva descargar e instalar todas los módulos y dependencias, proceso que puede ser un poco lento. No obstante, si no lo hacemos en el momento de la creación, tendremos que hacer esa instalación tarde o temprano.  

Con el comando`ng new --help` podemos ver la documentación sobre los diferentes parámetros existentes y su funcionamiento.  

Una vez finalizada la instalación de nuestra aplicación, podemos verificar que se ha creado correctamente utilizando el comando  
`ng lint`
que se encarga de analizar el código TypeScript de la apliación para ver que es correcto. Añadiendo el parámetro `--help` podremos ver los parámetros que nos permiten personalizar la ejecución de este comando.
