FROM node:18-alpine3.17

LABEL org.opencontainers.image.description "The CxAppSecEng Platform API"
LABEL org.opencontainers.image.source https://github.com/cxappseceng/platform
LABEL org.opencontainers.image.documentation https://github.com/cxappseceng/platform#readme

ENV HOST="0.0.0.0"
ENV PORT="3000"

RUN addgroup -S platform && \
    adduser -S platform -G platform;

COPY ./dist/packages/platform-api/ /opt/app

WORKDIR /opt/app

RUN npm install --omit=dev

USER platform

EXPOSE 3000

CMD [ "node", "main.js" ] 
