ARG RELEASE_TAG=latest

FROM atlassian/jira-software:${RELEASE_TAG}-jdk11

RUN apt-get update && apt-get install wget

RUN wget -P /tmp https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j-8.0.32.tar.gz

RUN tar \
    --extract \
    --verbose \
    --strip-components=1 \
    --file=/tmp/mysql-connector-j-8.0.32.tar.gz \
    -C /opt/atlassian/jira/lib mysql-connector-j-8.0.32/mysql-connector-j-8.0.32.jar