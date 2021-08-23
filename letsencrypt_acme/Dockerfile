ARG BUILD_FROM=homeassistant/armv7-base-python:3.7-alpine3.12
FROM $BUILD_FROM

# ARG BUILD_ARCH='armhf'
# # setup base
# ARG CERTBOT_DNS_IONOS_VERSION="0.0.7"
# ARG CERTBOT_VERSION=1.2.0
# #ENV PATH="~/.cargo/bin:${PATH}"


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

ENV LE_CONFIG_HOME /data/acme.sh
#Install
COPY ./ /install_acme.sh/
RUN cd /install_acme.sh && ([ -f /install_acme.sh/acme.sh ] && /install_acme.sh/acme.sh --install || curl https://get.acme.sh | sh) && rm -rf /install_acme.sh/

# RUN ln -s  /data/.acme.sh/acme.sh  /usr/local/bin/acme.sh && crontab -l | grep acme.sh | sed 's#> /dev/null##' | crontab -

# RUN printf "%b" '#!'"/usr/bin/env sh\n \
# if [ \"\$1\" = \"daemon\" ];  then \n \
#  trap \"echo stop && killall crond && exit 0\" SIGTERM SIGINT \n \
#  crond && while true; do sleep 1; done;\n \
# else \n \
#  exec -- \"\$@\"\n \
# fi" >/entry.sh && chmod +x /entry.sh

#         libffi \
#         musl \
#         openssl 
#     && apk add --no-cache --virtual .build-dependencies \
#         cargo \
#         g++ \
#         libffi-dev \
#         musl-dev \
#         openssl-dev \
#         rust \
#     && pip3 install --no-cache-dir --find-links \
#         "https://wheels.home-assistant.io/alpine-$(cut -d '.' -f 1-2 < /etc/alpine-release)/${BUILD_ARCH}/" \
#         certbot==${CERTBOT_VERSION} \
#         certbot-dns-ionos==${CERTBOT_DNS_IONOS_VERSION}\
#     && apk del .build-dependencies
# RUN pip3 install certbot-dns-ionos==${CERTBOT_DNS_IONOS_VERSION}

# Copy data
COPY rootfs /
