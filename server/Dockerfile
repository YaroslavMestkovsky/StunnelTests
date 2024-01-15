FROM ubuntu:latest

LABEL authors="Y"

RUN apt-get update && apt-get install -y stunnel4

COPY configs/stunnel-server.conf /etc/stunnel/
COPY rsa/certificate.pem /etc/stunnel/

CMD ["stunnel", "/etc/stunnel/stunnel-server.conf"]

ENTRYPOINT ["top", "-b"]