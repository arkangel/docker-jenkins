FROM oberthur/jenkins-slave-base:2.0

ENV MAVEN_VERSION=3.3.3 \
    MAVEN_HOME=/usr/share/maven \
    PATH=${DOCKER_HOME:-/usr/bin/docker-1.7.1}:$PATH

RUN curl -fsSL http://archive.apache.org/dist/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz | tar xzf - -C /usr/share \
  && mv /usr/share/apache-maven-$MAVEN_VERSION /usr/share/maven \
  && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn


RUN mkdir /usr/bin/docker-1.7.1 \
    && mkdir /usr/bin/docker-1.8.2 \ 
    && wget -O /usr/bin/docker-1.7.1/docker "https://get.docker.com/builds/Linux/x86_64/docker-1.7.1" \
    && chmod +x /usr/bin/docker-1.7.1/docker \
    && wget -O /usr/bin/docker-1.8.2/docker "https://get.docker.com/builds/Linux/x86_64/docker-1.8.2" \
    && chmod +x /usr/bin/docker-1.8.2/docker



