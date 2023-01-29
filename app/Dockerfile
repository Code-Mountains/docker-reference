FROM node:18-alpine
WORKDIR /app
MAINTAINER Kiran Dangol "kiran_dan2009@Yahoo.com"
ENV HOSTNAME=todo-app
ENV HOST=web-app
ENV OS="Alpine Linux"
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
