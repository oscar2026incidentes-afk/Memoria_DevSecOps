# 1. Partir de una imagen oficial de PHP con servidor web (Apache)
FROM php:8.2-apache

# 2. Establecer el directorio de trabajo dentro del contenedor
WORKDIR /var/www/html

# 3. Copiar la aplicación PHP desde el anfitrión al contenedor
#    (el directorio 'app' del anfitrión se copia al WORKDIR del contenedor)
COPY app/ /var/www/html/

# 4. (Opcional) Dar permisos adecuados, si hiciera falta
# RUN chown -R www-data:www-data /var/www/html

# 5. Exponer el puerto 80 (el de Apache)
EXPOSE 80
