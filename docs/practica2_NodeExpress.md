# Práctica 3.2: Despliegue de aplicaciones con Node Express

## Introducción

En esta práctica vamos a realizar el despliegue de aplicaciones Node.js sobre un servidor Node Express. Lo curioso de este caso es que el despliegue aquí cambia un poco puesto que no se hace sobre el servidor, sino que la aplicación es el servidor.

!!! warning "Warning"

    Comprueba que el servidor Tomcat de prácticas anteriores no está corriendo o nos dará problemas:
    
    `sudo systemctl status tomcat9`
    
    Y en caso de salir activo, pararlo:
    
    `sudo systemctl stop tomcat9`

## Instalación de Node.js, Express y test de la primera aplicación

La primera parte de la práctica es muy sencilla. Consistirá en instalar sobre nuestra Debian 11 tanto Node.js como Express y tras ello crear un archivo `.js` de prueba para comprobar que nuestro primer despliegue funciona correctamente.

Para ello, os podéis apoyar [en este sencillo tutorial](https://web.archive.org/web/20240420163631/https://unixcop.com/how-to-install-expressjs-on-debian-11/) o [este otro](https://www.server-world.info/en/note?os=Debian_12&p=nodejs&f=1), y para Express:

En lugar de acceder a `http://localhost:3000`, debéis acceder desde vuestra máquina local a `http://IP-maq-virtual:3000`, utilizando la IP concreta de vuestra máquina virtual.

!!! warning "Recordatorio"

    Debéis añadir a vuestro grupo de seguridad el puerto que estéis utilizando para acceder a la aplicación (3000 u otro), permitiendo el tráfico de entrada hacia ese puerto TCP.

Recordad parar el servidor (CTRL+C) al acabar la práctica.

!!! info "Task"

    Documenta, incluyendo capturas de pantallas, el proceso que has seguido para realizar el despliegue de esta nueva aplicación, así como el resultado final.

## Despliegue de una nueva aplicación

Vamos ahora a realizar el despliegue de una aplicación de terceros para ver cómo es el proceso.

Se trata de un "prototipo" de una aplicación de predicción meteorológica que podéis encontrar en este [repositorio de Github](https://github.com/alexkowsik/react-weather-app).

Tal y como indican las instrucciones del propio repositorio, los pasos a seguir son, en primer lugar, clonar el repositorio a nuesta máquina:

`git clone https://github.com/MehedilslamRipon/Shopping-Cart-Application`

Movernos al nuevo directorio:

`cd Shopping-Cart-Application/`

Instalar las librerías necesarias (paciencia, este proceso puede tardar un buen rato):


`npm install`

Y, por último, iniciar la aplicación:

`npm run start`

Cuando sigáis el proceso necesario e intentéis iniciar la aplicación con Express, os dará un error del tipo:

`sh: 1: nodemon: not found`

!!! info "Tarea"

    Buscad cómo solucionar este problema y, tras ello, iniciad la aplicación sin problemas.

    ¿Qué comando habéis usado para solucionar el fallo anterior?¿Cuál es su cometido?¿Qué archivo se ha modificado al ejecutarlo? Documéntalo todo en el informe de la práctica.

!!! infor "Tarea"

    Documenta, incluyendo capturas de pantallas, el proceso que has seguido para realizar el despliegue de esta nueva aplicación, así como el resultado final.

## Cuestiones

Cuando ejecutáis el comando `npm run start`, lo que estáis haciendo es ejecutar un script:

* ¿Donde podemos ver que script se está ejecutando?
* ¿Qué comando está ejecutando?

Como ayuda, podéis consultar [esta información](https://www.freecodecamp.org/espanol/news/node-js-npm-tutorial/).

## Referencias

[How to install ExpressJS on Debian 11?](https://unixcop.com/how-to-install-expressjs-on-debian-11/)