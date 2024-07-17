FROM node:20-alpine

WORKDIR /app

RUN npm install --quiet node-gyp typescript -gyp

RUN npm install -g @vue/cli

COPY . .

EXPOSE 8080

CMD [ "npm", "run", "serve"]