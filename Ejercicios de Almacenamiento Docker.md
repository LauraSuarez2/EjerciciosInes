# Ejercicios de Almacenamiento en Docker



[TOC]

> Realizado por: Laura Suárez
>
> Realizado: Alberto Vicente



## Ejercicios volúmenes

1. Crea un volumen docker que se llame miweb.

   ```bash
   $ docker volume create miweb
   ```

   ![image-20240202092540052](./Ejercicios%20de%20Almacenamiento%20Docker.assets/image-20240202092540052.png)

   

2. Crea un contenedor desde la imagen php:7.4-apache donde montes en el directorio /var/www/html (que sabemos que es el DocumentRoot del servidor que nos ofrece esa imagen) el volumen docker que has creado.

   ```bash
   $ docker run -d --name mi-php -v miweb:/var/www/html -p 8080:80 php:7.4-apache
   ```

   ![image-20240202102418617](./Ejercicios%20de%20Almacenamiento%20Docker.assets/image-20240202102418617.png)

3. Utiliza el comando docker cp para copiar un fichero index.html en el directorio /var/www/html.

   ![image-20240205100038725](./Ejercicios%20de%20Almacenamiento%20Docker.assets/image-20240205100038725.png)

   ![image-20240205100703178](./Ejercicios%20de%20Almacenamiento%20Docker.assets/image-20240205100703178.png)

   ![image-20240205101434190](./Ejercicios%20de%20Almacenamiento%20Docker.assets/image-20240205101434190.png)

4. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero index.html.

   -

5. th

6. rth

7. rth



## Ejercicios Bind Mount

<u>Vamos a trabajr con **bind mount** :</u>

1. Crea un directorio en tu host y dentro crea un fichero `index.html`.
2. Crea un contenedor desde la imagen `php.7.4-apache` donde montes en el directorio `/var/www/html` el directorio que has creado por medio de `bind mount`.
3. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html.`
4. Modifica el contenido del fichero `index.html` en tu host y comprueba que al refrescar la página ofrecida por el contenedor, el contenido ha cambiado.
5. Borra el contenedor.
6. Crea un nuevo contenedor y monta el mismo directorio como en el ejricico anterior.
7. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html`. ¿Se sigue viendo contenido?.