FROM alpine
MAINTAINER anorpi "5262122@gmail.com"

RUN apk --no-cache add ttf-dejavu
RUN apk --no-cache add openjdk8
RUN apk --no-cache add wget
RUN wget -q -c http://mirrors.jenkins-ci.org/war-stable/latest/jenkins.war

EXPOSE 8080
CMD ["java","-jar","jenkins.war"]

