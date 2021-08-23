ARG BUILD_FROM=homeassistant/armv7-base-python:3.7-alpine3.12
FROM $BUILD_FROM

 RUN apk add --no-cache --update \
                openssl \
                openssh-client \
                coreutils \
                bind-tools \
                curl \
                sed \
                socat \
                tzdata \
                oath-toolkit-oathtool \
                tar \
                libidn

ENV LE_CONFIG_HOME /acme.sh
#Install
COPY ./ /install_acme.sh/
RUN cd /install_acme.sh && ([ -f /install_acme.sh/acme.sh ] && /install_acme.sh/acme.sh --install || curl https://get.acme.sh | sh) && rm -rf /install_acme.sh/

VOLUME /acme.sh

# Copy data
COPY rootfs /
