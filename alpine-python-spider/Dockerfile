FROM alpine
MAINTAINER anorpi "5262122@gmail.com"
RUN apk update 
RUN apk --no-cache add gcc
RUN apk --no-cache add python
RUN apk --no-cache add python-dev
RUN apk --no-cache add py-lxml
RUN apk add ca-certificates && update-ca-certificates && apk add openssl
RUN wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' && python2 /tmp/get-pip.py  && rm /tmp/get-pip.py
RUN pip install requests
RUN pip install bs4

ENTRYPOINT ["/usr/bin/python"]
#Usage:
#docker build -t="anorpi/alpine-python-spider:v1.0" .
#write the command in shell,<docker run --rm --name alpine-python-spider  -v $PWD:$PWD  anorpi/alpine-python-spider:v1.0 $PWD/$1>
