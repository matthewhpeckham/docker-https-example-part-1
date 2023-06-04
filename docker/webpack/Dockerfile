FROM node:lts-bullseye-slim

USER node
WORKDIR /usr/src/app

COPY --chown=node:node package-lock.json package.json ./

RUN npm ci

COPY --chown=node:node docker/webpack/entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]