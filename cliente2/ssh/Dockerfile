FROM ubuntu:latest

RUN apt-get update && apt-get install -y openssh-server
RUN mkdir /var/run/sshd

RUN useradd -m tiago
RUN echo 'tiago:tiago' | chpasswd

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]