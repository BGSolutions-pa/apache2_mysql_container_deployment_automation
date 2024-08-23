FROM ubuntu
USER root
RUN apt-get update -y
RUN apt-get install apache2 -y
RUN echo "ServerName 127.0.0.1" >> /etc/apache2/apache2.conf
EXPOSE 80/TCP
EXPOSE 443/TCP
CMD ["apachectl", "-D", "FOREGROUND"]
