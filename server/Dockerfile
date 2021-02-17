FROM node
ENV NODE_ENV=development
WORKDIR /app/server
COPY package*.json ./
RUN npm install
CMD [ "node", 'index.js']
EXPOSE 3000