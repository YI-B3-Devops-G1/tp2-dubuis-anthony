FROM node:13.3-alpine
ENV PORT 36301
ENV DB_USER postgres
ENV DB_PASSWORD postgres
ENV DB_NAME postgres
ENV DB_HOST postgres

WORKDIR /home/node/app
RUN chown -R node:node /home/node/app
USER node

COPY package*.json ./
RUN yarn install
COPY . .

EXPOSE 36301
CMD ["yarn", "start"]