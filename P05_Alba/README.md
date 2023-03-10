# P05 -  Despliegue de escenarios multicontenedor con Docker Compose

### :memo: Datos:
Los user son: alba (salvo en Adminer) :pushpin:\
Las password son: 1234 :pushpin:

### :bulb: Info usada:
- Los apuntes de clase
- https://hub.docker.com/_/mediawiki


### :one: Servidor Apache:
 Tomamos como base la imagen de Apache (httpd).\
 Cambiamos el `volumes` y le podemos la siguiente línea `.:/html:/var/www/html`.\
 Lo abrimos en el buscador que nos mostrará la página de inicio de Apache.\
 ![imagen it works](./imagenes/Apache.png)
 
### :two: Mediawiki:
Tomamos como base la imagen Mediawiki.\
Modificamos los datos (user, password y db).\
Lo abrimos en el buscador\
![imagen inicio mediawiki](./imagenes/1.png)\
![imagen conf mediawiki](./imagenes/2.png)\
![imagen conf2 mediawiki](./imagenes/3.png)

Una vez accedido con los datos descargamos el archivo localsettings.\
Copiamos el archivo `LocalSettings.php` dentro de la carpeta onde tenemos el mediawiki.yml.\
![imagen del php en carpeta](./imagenes/php.JPG)

Hacemos un cp del `Local.Setting.php` en la ruta: `/var/www/html`.\
Desde la web de Mediawiki abrimos la guia.


### :three: Guestbook:
Tomamos el código de DockerHub de Guestbook.\
Modificamos el código (container name).\
Lo abrimos en el buscador.
![imagen guestbook](./imagenes/Guestbook.png)

### :four: Wordpress:
Tomamos el código de DockerHub de Wordpress.\
Modificamos los datos de la bbdd (intentamos poner los pluggings pero creemos que eso daba incompatibilidad con la bbdd).\
Lo abrimos en el buscador.\
![imagen gadminer](./imagenes/Wordpress.png)

### :five: Adminer:
Tomamos el código de DockerHub de Adminer.\
Lo abrimos en el buscador.\
Cuando nos solicite el usuario ponemos root.\
![imagen gadminer](./imagenes/Adminer.png)
