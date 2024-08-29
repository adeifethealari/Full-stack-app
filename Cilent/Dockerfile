FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build

# Install `serve`
RUN npm install -g serve

# Use `serve` to serve the built files
CMD ["serve", "-s", "dist", "-l", "5000"]

EXPOSE 5000

