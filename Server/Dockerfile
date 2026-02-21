FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# build dist/index.js if build script exists, skip if not
RUN npm run build --if-present

EXPOSE 5000

CMD ["npm", "start"]
