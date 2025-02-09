FROM debian:bookworm-slim

RUN apt-get -y update && \
        apt install -y net-tools iputils-ping netcat-traditional && \
        rm -rf /var/lib/apt/lists

WORKDIR /

COPY ./wstunnel /usr/bin

ENV SERVER_PROTOCOL="ws"
ENV SERVER_LISTEN="0.0.0.0"
ENV SERVER_PORT="8080"

EXPOSE 8080

CMD ["/bin/sh", "-c", "exec /usr/bin/wstunnel server ${SERVER_PROTOCOL}://${SERVER_LISTEN}:${SERVER_PORT}"]