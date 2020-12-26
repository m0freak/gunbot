FROM ubuntu:20.04
  
RUN apt update && \
  apt install --no-install-recommends --no-install-suggests -y unzip wget ca-certificates && \
  wget -O /tmp/lin.zip https://github.com/GuntharDeNiro/BTCT/releases/download/2100/lin_v14.zip && \
  cd /tmp && \
  unzip -q lin.zip && \
  rm -rf lin.zip && \
  mv lin* /lin && \
  apt-get remove --purge --auto-remove -y unzip && \
  rm -rf /var/lib/apt/lists/*

EXPOSE 5000
  
WORKDIR /lin

ENTRYPOINT ["./gunthy-linux"]

