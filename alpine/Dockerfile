FROM alpine:3.10@sha256:c19173c5ada610a5989151111163d28a67368362762534d8a8121ce95cf2bd5a

ENV AWS_CLI_VERSION 1.16.303

RUN apk add -v --update --no-cache python groff less && \
  apk add -v --update --no-cache --virtual .build-deps py-pip && \
  pip install --no-cache-dir --upgrade pip awscli==${AWS_CLI_VERSION} && \
  apk del -v .build-deps

ENTRYPOINT [ "aws" ]
