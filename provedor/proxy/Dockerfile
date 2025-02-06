FROM nginx:latest

RUN mkdir -p /etc/nginx/ssl
RUN cd /etc/nginx/ssl
RUN openssl req -x509 -sha256 -newkey rsa:2048 -keyout /etc/nginx/ssl/certificate.key -out /etc/nginx/ssl/certificate.crt -days 1024 -nodes \
    -subj "/C=US/ST=State/L=City/O=Organization/OU=Unit/CN=localhost"
#COPY index.html /usr/share/nginx/html
