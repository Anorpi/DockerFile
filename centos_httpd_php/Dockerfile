FROM centos:6.8
MAINTAINER anorpi "5262122@gmail.com"

RUN yum update -y
RUN yum install httpd -y
RUN yum install php -y
RUN yum install php-mysql -y
RUN sed -ri -e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' -e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' /etc/httpd/conf/httpd.conf

EXPOSE 80 443
CMD ["httpd","-DFOREGROUND"]
