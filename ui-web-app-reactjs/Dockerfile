FROM node:13.12.0-alpine
RUN mkdir /app
WORKDIR /app
COPY package*.json /app
RUN npm install
COPY . /app
RUN npm run build
EXPOSE 8080
CMD [ "node", "server.js" ]
