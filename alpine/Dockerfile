FROM alpine:3.8@sha256:621c2f39f8133acb8e64023a94dbdf0d5ca81896102b9e57c0dc184cadaf5528

ENV AWS_CLI_VERSION 1.15.85

RUN apk add -v --update --no-cache python groff less && \
  apk add -v --update --no-cache --virtual .build-deps py-pip && \
  pip install --no-cache-dir --upgrade pip awscli==${AWS_CLI_VERSION} && \
  apk del -v .build-deps

ENTRYPOINT [ "aws" ]
