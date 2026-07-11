FROM node:26-alpine


RUN apk update && apk upgrade --no-cache

WORKDIR /app

COPY package*.json ./

RUN npm ci --ignore-scripts --omit=dev

COPY . .

USER node

EXPOSE 3001

CMD ["node", "server.js"]