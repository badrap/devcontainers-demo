FROM node:22-alpine
RUN apk add --no-cache \
  chromium \
  git \
  openssh \
  ripgrep
RUN mkdir -p /workspace && chown node:node /workspace

USER node
# Create directories before (anonymous or named) volumes are be mounted
# to them, so that the ownership will be correct.
RUN mkdir -p /workspace/node_modules /workspace/dist ~/.vscode-server
# Allow `npm install -g` without sudo.
RUN mkdir ~/.npm-global \
  && npm config set -L user prefix ~/.npm-global
ENV PATH="$PATH:/home/node/.npm-global/bin"
