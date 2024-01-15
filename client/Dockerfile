FROM ubuntu:latest

LABEL authors="Y"

RUN apt-get update && apt-get install -y stunnel4

COPY configs/stunnel-client.conf /etc/stunnel/
COPY rsa/certificate.pem /etc/stunnel/

CMD ["stunnel", "/etc/stunnel/stunnel-client.conf"]

ENTRYPOINT ["top", "-b"]