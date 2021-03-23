FROM nextcloud

RUN apt update -y \
    && apt-get install software-properties-common -y \
    && apt install certbot -y \
    && apt install apache2 libapache2-mod-wsgi python-dev -y \
    && apt-get install python-certbot-apache -y \
    && a2enmod ssl \
    && certbot --apache -d przemekgorzynski.pl --non-interactive --agree-tos -m przeyslaw.gorzynski@protonmail.com \ 
    && certbot renew \
    && apt-get update -y \
    && apt-get clean \

EXPOSE 80
CMD ["apache2-foreground"]