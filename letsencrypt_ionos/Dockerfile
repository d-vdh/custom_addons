ARG BUILD_FROM="certbot/certbot:arm32v6-v1.18.0"
FROM $BUILD_FROM

# setup base
ARG CERTBOT_DNS_IONOS_VERSION="0.0.7"

RUN pip3 install certbot-dns-ionos==${CERTBOT_DNS_IONOS_VERSION} 
#RUN apk del .build-dependencies

# Copy data
COPY rootfs /
