FROM alpine:3.10

MAINTAINER <s.billon@linkbynet.com>

# Install postfix and supervisor
RUN apk add --no-cache \
        postfix \
        cyrus-sasl-plain \
        rsyslog \
        supervisor && \
        /usr/bin/newaliases

# Copy files into container
COPY . /

# SMTP port
EXPOSE 25

ENTRYPOINT [ "/entrypoint.sh" ]
