# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.163.1/containers/rust/.devcontainer/base.Dockerfile

# FROM mcr.microsoft.com/vscode/devcontainers/rust:0-1
FROM rust:1-slim

ENV PATH $PATH:~/.local/bin
# [Optional] Uncomment this section to install additional packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    # add git
    && apt-get -y install --no-install-recommends curl git \
    # add rustfmt
    && rustup component add rustfmt \
    # rust-analyzer-bin
    && mkdir -p ~/.local/bin \
    && curl -L https://github.com/rust-analyzer/rust-analyzer/releases/latest/download/rust-analyzer-linux -o ~/.local/bin/rust-analyzer \
    # &&  curl -L https://github.com/rust-analyzer/rust-analyzer/releases/download/nightly/rust-analyzer-linux -o ~/.local/bin/rust-analyzer \
    && chmod +x ~/.local/bin/rust-analyzer \
    ;
