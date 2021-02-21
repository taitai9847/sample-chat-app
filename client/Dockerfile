FROM node
ENV NODE_ENV=development
WORKDIR /app/client
COPY package*.json ./
RUN npm install
CMD [ "npm", "run", "watch" ]
EXPOSE 8080