ARG BUILD_FROM=homeassistant/armv7-base-python:3.7-alpine3.11
FROM $BUILD_FROM

# ARG BUILD_ARCH='armhf'
# # setup base
# ARG CERTBOT_DNS_IONOS_VERSION="0.0.7"
# ARG CERTBOT_VERSION=1.2.0
# #ENV PATH="~/.cargo/bin:${PATH}"


# RUN apk add --no-cache --update \
#         libffi \
#         musl \
#         openssl \
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
