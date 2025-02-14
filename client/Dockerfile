FROM debian:bookworm-slim

RUN apt-get -y update && \
        apt install -y net-tools iputils-ping netcat-traditional curl && \
        rm -rf /var/lib/apt/lists

WORKDIR /

COPY ./wstunnel /usr/bin

CMD ["sh", "-c", "tail -f /dev/null"]