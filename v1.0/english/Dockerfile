FROM openjdk:8-jre-alpine

MAINTAINER  DBpedia Spotlight Team <dbp-spotlight-developers@lists.sourceforge.net>

ENV RELEASE_SERVER    sourceforge.net/projects/dbpedia-spotlight/files
ENV RELEASE_FILENAME  dbpedia-spotlight-1.0.0.jar 
ENV LANGUAGE_MODEL    en.tar.gz

RUN mkdir -p /opt/spotlight && \
    cd /opt/spotlight && \
    wget https://sourceforge.net/projects/dbpedia-spotlight/files/2016-10/en/model/en.tar.gz && \
    wget https://sourceforge.net/projects/dbpedia-spotlight/files/spotlight/dbpedia-spotlight-1.0.0.jar && \
    tar -xvzf en.tar.gz  && \

ADD spotlight.sh /bin/spotlight.sh
RUN chmod +x /bin/spotlight.sh

EXPOSE 80
