FROM centos:6.8
MAINTAINER anorpi "5262122@gmail.com"

RUN echo "[nginx]">/etc/yum.repos.d/nginx.repo
RUN echo "name=nginx repo">>/etc/yum.repos.d/nginx.repo
RUN echo "baseurl=http://nginx.org/packages/centos/\$releasever/\$basearch/">>/etc/yum.repos.d/nginx.repo
RUN echo "gpgcheck=0">>/etc/yum.repos.d/nginx.repo
RUN echo "enabled=1">>/etc/yum.repos.d/nginx.repo
RUN yum update -y && yum install nginx -y
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
	&& ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80 443
CMD ["nginx", "-g", "daemon off;"]
