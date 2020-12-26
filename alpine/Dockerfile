FROM alpine:latest

RUN apk add --no-cache --virtual .deps zip wget && \
  wget -O /tmp/lin.zip https://github.com/GuntharDeNiro/BTCT/releases/download/2100/lin_v14.zip && \
  cd /tmp && \
  unzip -q lin.zip && \
  rm -rf lin.zip && \
  mv lin* /lin && \
  apk del .deps

#ADD https://github.com/GuntharDeNiro/BTCT/releases/download/2100/lin_v14.zip /tmp/

#WORKDIR /tmp

#RUN unzip -q /tmp/lin*.zip && rm -rf /tmp/lin*.zip

#RUN mv lin* /lin

WORKDIR /lin

ENTRYPOINT ["./gunthy-linux"]

