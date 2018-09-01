ARG FROM_IMAGE
FROM $FROM_IMAGE

ARG NAME
ARG VERSION
ARG MAINTAINER
LABEL Name=$NAME Version=$VERSION maintainer=$MAINTAINER

RUN apt-get update -y \
 && apt-get upgrade -y \
 && apt-get dist-upgrade -y \
 && apt-get install -y \
    wget \
    openssh-client \
    uuid-runtime \
    libxmuu1 \
    xauth\
    supervisor
RUN apt-get install -y openjdk-8-jdk 

ARG RUNDECK_INSTALL_PACKAGE
ARG RUNDECK_INSTALL_PACKAGE_URL
RUN wget $RUNDECK_INSTALL_PACKAGE_URL \
 && dpkg -i $RUNDECK_INSTALL_PACKAGE

ARG PORT
ENV PORT=$PORT
ARG HOST
ENV HOST=$HOST
CMD echo "export RDECK_HTTP_PORT=$PORT" > /etc/default/rundeckd \
 && sed -i "s/4440/$PORT/" etc/rundeck/framework.properties \
 && sed -i "s/4440/$PORT/" /etc/rundeck/rundeck-config.properties \
 && sed -i "s/localhost/$HOST/" /etc/rundeck/framework.properties \
 && sed -i "s/localhost/$HOST/" /etc/rundeck/rundeck-config.properties \
 && service rundeckd start \
 && exec /usr/bin/supervisord -n