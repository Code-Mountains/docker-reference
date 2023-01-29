FROM node:18-alpine
WORKDIR /app
ENV HOSTNAME=todo-app
ENV HOST=web-app
ENV OS="Alpine Linux"
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
