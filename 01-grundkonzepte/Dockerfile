FROM debian

RUN apt-get update
RUN apt-get install -y apache2
RUN mkdir /var/run/apache2

EXPOSE 80

CMD [ "sh", "-c", ". /etc/apache2/envvars && apache2 -D FOREGROUND" ]
