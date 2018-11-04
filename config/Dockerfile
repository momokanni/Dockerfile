FROM java:8
LABEL maintainer="sunchongan@sina.com"
COPY config.jar /usr/local/sunlin/
COPY config.sh /usr/local/sunlin/
VOLUME /usr/local/sunlin/basedir/
WORKDIR /usr/local/sunlin/
EXPOSE 8763
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/.urandom","-jar","config.jar"]
