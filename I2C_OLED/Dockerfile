FROM ghcr.io/home-assistant/base:latest

ENV LANG C.UTF-8
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Install requirements for add-on
RUN apk add --no-cache \
  python3 \
  py3-pip \
  py3-pillow \
  py3-smbus

# Copy data for add-on
COPY src/ /I2C_OLED/
COPY run.sh /

WORKDIR /data
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
