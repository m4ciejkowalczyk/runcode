FROM prestashop/prestashop:1.7.8

# Kopiowanie źródeł
COPY ./src /var/www/html

RUN chown -R www-data:www-data /var/www/html

# Reszta Twoich komend (SSL itp.)
RUN apt-get update && apt-get install -y openssl \
    && openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    -keyout /etc/ssl/private/ssl-cert-snakeoil.key \
    -out /etc/ssl/certs/ssl-cert-snakeoil.pem \
    -subj "/C=PL/ST=Pomorskie/L=Gdansk/O=PG/OU=ETI/CN=localhost" \
    && a2enmod ssl \
    && a2ensite default-ssl
