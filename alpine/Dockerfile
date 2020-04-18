FROM alpine:3.11@sha256:b276d875eeed9c7d3f1cfa7edb06b22ed22b14219a7d67c52c56612330348239

ENV AWS_CLI_VERSION 1.18.41

RUN apk add -v --update --no-cache python groff less && \
  apk add -v --update --no-cache --virtual .build-deps py-pip && \
  pip install --no-cache-dir --upgrade pip awscli==${AWS_CLI_VERSION} && \
  apk del -v .build-deps

ENTRYPOINT [ "aws" ]
