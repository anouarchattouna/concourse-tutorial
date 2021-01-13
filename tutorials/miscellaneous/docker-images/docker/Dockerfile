# syntax = docker/dockerfile:1.0-experimental
FROM alpine:3.12

RUN --mount=type=secret,id=mycoolsecret \
  MY_SECRET=$(cat /run/secrets/mycoolsecret) && \
  export MY_SECRET && \
  echo "MY_SECRET=\"${MY_SECRET}\"" >> /etc/os-release && \
  apk update && apk add --no-cache --upgrade

ENV PS1='[\u@\h \W]\$'

CMD ["bash"]
