FROM httpd:2.4

ENV VERSION=1.0.0
ENV AUTHOR="Jorge Rubiano"
ENV USERNAME=chatgpt

WORKDIR /var/www/html

COPY ./web .

CMD [ "apachectl", "-D", "FOREGROUND" ]