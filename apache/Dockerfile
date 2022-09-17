FROM httpd:2.4.32-alpine

RUN apk update; \
    apk upgrade;

COPY bastion.conf /usr/local/apache2/conf/bastion.conf
COPY bastion-ssl.conf /usr/local/apache2/conf/bastion-ssl.conf
RUN echo "Include /usr/local/apache2/conf/bastion.conf" \
    >> /usr/local/apache2/conf/httpd.conf
RUN echo "Include /usr/local/apache2/conf/bastion-ssl.conf" \
    >> /usr/local/apache2/conf/httpd.conf
