FROM gitpod/workspace-full:latest

USER gitpod
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

ENV GLOBAL_MAKEFILE_LIBRARY="/srv/makelib"
COPY rootfs/ /

RUN \
    brew install awscli && \
    brew cleanup

USER root
SHELL ["/bin/sh", "-c"]
