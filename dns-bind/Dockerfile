FROM debian:bookworm-slim
RUN apt update && \
    apt install -y bind9 bind9utils && \
    rm -rf /var/lib/apt/lists/*

COPY named.conf /etc/bind/named.conf
COPY ngin.db /etc/bind/data/

CMD ["named", "-g", "-c", "/etc/bind/named.conf"]
