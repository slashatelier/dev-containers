FROM gitpod/workspace-full:latest

USER gitpod
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

ENV GLOBAL_MAKEFILE_LIBRARY="/srv/makelib"
COPY rootfs/ /

RUN \
    brew install terraform-docs && \
    brew install tfenv && \
    brew install tflint && \
    brew install tfsec && \
    brew install awscli && \
    brew install conftest && \
    brew install --ignore-dependencies cdktf && \
    brew cleanup
RUN tfenv install latest && tfenv use latest

RUN curl "https://s3.amazonaws.com/session-manager-downloads/plugin/latest/ubuntu_64bit/session-manager-plugin.deb" -o "session-manager-plugin.deb" && \
    sudo dpkg -i session-manager-plugin.deb && \
    rm session-manager-plugin.deb

USER root
SHELL ["/bin/sh", "-c"]
