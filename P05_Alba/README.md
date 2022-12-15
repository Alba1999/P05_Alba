# P05 -  Despliegue de escenarios multicontenedor con Docker Compose


## Los user son: alba
## Las password son: 1234


1. Servidor Apache
 - Tomamos como base la imagen de Apache (httpd)
 - Cambiamos el `volumes` y le podemos la siguiente línea `C:/html:/var/www/html` que permite abrir y mostar la página de inicio de Apache.

2. Mediawiki
 - Tomamos como base la imagen Mediawiki 
 - Modificamos los datos (user, password y db)
 - Una vez accedido con los datos descargamos el archivo localsettings
 - Copiamos el archivo `LocalSettings.php` dentro de la carpeta onde tenemos el mediawiki.yml 
 - Hacemos un cp del `Local.Setting.php` en la ruta: `/var/www/html`
 - Desde la web de Mediawiki abrimos la guia  

3. Guestbook

4. Wordpress
- Tomamos como base la imagen de Wordpress
- Modificamos los datos de la bbdd 
- Añadimos los temas y pluggins en `volumes`

5. Adminer