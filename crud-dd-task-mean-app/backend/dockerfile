FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --production

COPY . .

# If your backend uses another port, change this
EXPOSE 3000

# Uses "npm start" from package.json
CMD ["npm", "start"]
