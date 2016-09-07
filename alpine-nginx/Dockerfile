FROM alpine
MAINTAINER anorpi "5262122@gmail.com"

#If no nginx.pid in the path, will can not apk add nginx, maybe a bug.
RUN mkdir -p /run/nginx/
RUN cd  /run/nginx/
RUN touch nginx.pid
RUN apk add --no-cache nginx
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
#Default root web document: /var/lib/nginx/html/
#You can use:'nginx -V' see more details
