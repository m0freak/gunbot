FROM alpine:3.12.3

RUN apk add --no-cache --virtual .deps zip wget && \
  wget -O /tmp/lin.zip https://github.com/GuntharDeNiro/BTCT/releases/download/2100/lin_v14.zip && \
  cd /tmp && \
  unzip -q lin.zip && \
  rm -rf lin.zip && \
  mv lin* /lin && \
  apk del .deps

EXPOSE 5000

WORKDIR /lin

ENTRYPOINT ["./gunthy-linux"]

