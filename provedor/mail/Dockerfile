FROM ubuntu:latest

RUN apt update --fix-missing -y

RUN apt upgrade -y

RUN apt install postfix dovecot-imapd dovecot-pop3d -y

RUN apt install -q -y syslog-ng

# Copiar o arquivo de configuração
COPY main.cf /etc/postfix

# Copiar arquivo de autenticacao do Dovecot
COPY ./dovecot/10-auth.conf /etc/dovecot/conf.d
COPY ./dovecot/10-master.conf /etc/dovecot/conf.d
COPY ./dovecot/10-mail.conf /etc/dovecot/conf.d


RUN echo "camurupim.com.br" > /etc/mailname


# Add User
# Add User
RUN useradd -m tiago
RUN useradd -m henrique

# Set user passord
RUN echo "tiago:tiago"|chpasswd
RUN echo "henrique:tiago"|chpasswd

CMD ["sh", "-c", "service syslog-ng start ; service postfix start ; service dovecot start; tail -F /var/log/mail.log"]