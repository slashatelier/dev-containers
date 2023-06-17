FROM gitpod/workspace-full:latest

USER gitpod
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN \
    brew install awscli && \
    brew cleanup

USER root
SHELL ["/bin/sh", "-c"]
