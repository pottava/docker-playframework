# Play framework v1.4.1
# docker run --rm pottava/play:1.4 

FROM alpine:3.3

RUN apk --no-cache add --virtual build-dependencies curl unzip \
      && apk --no-cache add python \
      && curl --location -s https://downloads.typesafe.com/play/1.4.1/play-1.4.1.zip > /tmp/play-1.4.1.zip \
      && unzip -q /tmp/play-1.4.1.zip -d /opt \
      && rm -rf /tmp/play-1.4.1.zip \
            /opt/play-1.4.1/COPYING \
            /opt/play-1.4.1/documentation \
            /opt/play-1.4.1/play.bat \
            /opt/play-1.4.1/support \
            /opt/play-1.4.1/README.textile \
            /opt/play-1.4.1/samples-and-tests \
      && ln -s /opt/play-1.4.1/play /usr/local/bin \
      && apk del build-dependencies

CMD ["play"]
