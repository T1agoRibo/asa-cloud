FROM nginx:latest

RUN sudo mkdir -p /etc/nginx/ssl
RUN cd /etc/nginx/ssl
RUN sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
-keyout meu-certificado.key -out meu-certificado.crt


#COPY index.html /usr/share/nginx/html
