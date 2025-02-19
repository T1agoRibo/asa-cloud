FROM nginx:latest

RUN mkdir -p /etc/nginx/ssl
COPY ./certs /etc/nginx/ssl
#RUN openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/ssl/certificate.key -out /etc/nginx/ssl/certificate.crt -days 1024 -nodes \
  #  -subj "/C=US/ST=State/L=City/O=Organization/OU=Unit/CN=praiadoamor.com.br"
#COPY index.html /usr/share/nginx/html

#RUN apt install certbot python3-certbot-nginx -y
COPY default.conf /etc/nginx/conf.d
EXPOSE 443