FROM alpine
MAINTAINER anorpi "5262122@gmail.com"

RUN apk --no-cache add python
RUN apk --no-cache add git
RUN git clone -b manyuser https://github.com/breakwa11/shadowsocks.git


EXPOSE 8388
ENTRYPOINT ["/usr/bin/python","/shadowsocks/shadowsocks/server.py","-p","8388","-m","aes-256-cfb","-k"]
#Usage:
#docker build -t="anorpi/alpine-ssr:v1" .
#docker run -p 8388:8388  --name alpinessr -d anorpi/alpine-ssr:v1 YOURPASSWORD
