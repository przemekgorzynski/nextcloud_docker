FROM nextcloud

RUN apt update -y \
    && apt-get install software-properties-common -y \
    && apt install certbot -y \
    && apt-get install python-certbot-apache \
    && apt-get update \
    && apt-get clean \

EXPOSE 80
ENTRYPOINT ["/entrypoint.sh"]
CMD ["apache2-foreground"]