FROM ubuntu:20.04

RUN apt update && \
  apt install --no-install-recommends --no-install-suggests -y unzip wget ca-certificates dumb-init && \
  wget -O /tmp/lin.zip https://github.com/GuntharDeNiro/BTCT/releases/download/22/lin_v14.zip && \
  cd /tmp && \
  unzip -q lin.zip && \
  rm -rf lin.zip && \
  mv lin* /lin && \
  apt-get remove --purge --auto-remove -y unzip && \
  rm -rf /var/lib/apt/lists/*

RUN useradd -u 10001 gunbot

EXPOSE 5000

RUN chown -R gunbot:gunbot /lin

WORKDIR /lin

USER gunbot

ENTRYPOINT ["/usr/bin/dumb-init", "--"]

CMD ["./gunthy-linux"]

