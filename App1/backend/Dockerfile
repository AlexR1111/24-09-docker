FROM node:22-alpine3.20

ENV DB_USER="postgres"
ENV DB_HOST="host.docker.internal"
ENV DB_NAME="my_to_do_app"
ENV DB_PASSWORD="1234"
ENV DB_PORT=5433

WORKDIR /backend
COPY package.json package-lock.json ./
RUN npm install --omit=dev

COPY . .

EXPOSE 3050

CMD ["node", "server.js"]