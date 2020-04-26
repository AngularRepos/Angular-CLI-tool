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

para verificar que coinciden en ambas respuestas la versión de Angular CLI instaladas.  

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

## Generar código con modelos

El comando *generate* nos permite crear código a partir de una serie de modelos. De esta forma, cuando comenzamos a escribir el código de nuestra aplicación, podemos utilizar CLI para crear compenentes, directivas, clases, etc... utilizando estos modelos mediante la instrucción `ng generate <modelo>`, o utilizar los alias correspondientes `ng g <m>`)

### Generar nuevos componentes

Para crear un nuevo componente para nuestra aplicación utilizaremos el comando  
`ng generate component <nombre del componente>`  
o usar `g`como alias de `generate` y usar `c`como alias de `component`
Algunos parámetros para este comando a tener en cuenta a la hora de crear un componente son los siguientes:

+ `--flat`: por defecto cuando se crea un nuevo compoente, se crea dentro de su propio directorio; con flat el componente se crea directamente el raíz que le hayamos indicado, sin crear un nuevo directorio;
+ `--inline-template` (o `-t`): permite indicar que el componente no tendrá un fichero externo para su template, sino que estará definido en el propio componente;
+ `--inline-style` (o `-s`): igual que el anterior, pero aplicado a los ficheros de estilo;
+ `--skipTests`: evita la creación de los ficheros individuales de test;
+ `--dry-run` (o `-d`): permite ver qué ficheros se van a crear, sin crearlos realmente.

Así, por ejemplo, el comando `ng g c customer` creará un nuevo componente llamado *customer* dentro del directorio raíz *app* de la aplicación. Por su parte, el comando `ng g c customer/customers-list -t -s --skipTests` creará un único fichero .ts en el directorio raíz *customer* para nuestro nuevo componente, que incluirá el template html y el fichero de estilo correspondiente.
