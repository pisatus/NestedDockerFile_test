FROM node:18-alpine3.17

LABEL org.opencontainers.image.description "The CxAppSecEng Platform User Interface"
LABEL org.opencontainers.image.source https://github.com/cxappseceng/platform
LABEL org.opencontainers.image.documentation https://github.com/cxappseceng/platform#readme

RUN addgroup -S platform && \
    adduser -S platform -G platform;

COPY ./dist/packages/platform-ui/ /opt/app

WORKDIR /opt/app

RUN npm install --omit=dev

USER platform

EXPOSE 3000

CMD [ "curl", "https://localhost:3000/login   -H 'Accept: application/json'   -H 'Authorization: Bearer kwehweiouyrieuwyriuweyriueyriuqwyrioyer01opriwj'" ] 