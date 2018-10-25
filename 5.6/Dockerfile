FROM moodlehq/moodle-php-apache:5.6

RUN pecl install solr redis

VOLUME [ "/var/www/html" ]
VOLUME ["/var/www/moodledata"]

COPY php.ini /usr/local/etc/php/conf.d

RUN chmod -R 777 /var/www/moodledata

CMD ["apache2-foreground"]
