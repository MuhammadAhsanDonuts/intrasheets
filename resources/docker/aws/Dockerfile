FROM amazonlinux

ENV container docker

RUN yum update -y \
    && amazon-linux-extras install nginx1.12 -y

COPY localhost.conf /etc/nginx/conf.d

EXPOSE 80
EXPOSE 443

STOPSIGNAL SIGTERM

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
