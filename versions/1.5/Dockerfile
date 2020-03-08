# Play framework v1.5
# docker run --rm pottava/play:1.5

FROM pottava/java:11

RUN apk --no-cache add --virtual build-dependencies curl unzip \
      && apk --no-cache add python \
      && curl --location -s https://downloads.typesafe.com/play/1.5.3/play-1.5.3.zip > /tmp/play-1.5.3.zip \
      && unzip -q /tmp/play-1.5.3.zip -d /opt \
      && rm -rf /tmp/play-1.5.3.zip \
            /opt/play-1.5.3/COPYING \
            /opt/play-1.5.3/documentation \
            /opt/play-1.5.3/framework/test-src \
            /opt/play-1.5.3/play.bat \
            /opt/play-1.5.3/python/*.dll \
            /opt/play-1.5.3/python/python.* \
            /opt/play-1.5.3/README.textile \
            /opt/play-1.5.3/samples-and-tests \
            /opt/play-1.5.3/support \
      && ln -sf /opt/play-1.5.3/play /usr/local/bin \
      && ln -sf /opt/play-1.5.3 /play-1.5.3 \
      && apk del --purge build-dependencies

CMD ["play"]
