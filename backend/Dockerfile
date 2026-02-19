<<<<<<< HEAD
FROM node:lts-alpine

RUN mkdir -p /app
WORKDIR /app
COPY package*.json ./
RUN apk --no-cache add --virtual builds-deps build-base python3 git
RUN npm install
COPY . .
ENV NODE_ENV prod
ENV NODE_ICU_DATA=node_modules/full-icu
ENTRYPOINT ["npm", "start"]
=======
# Use a stable Node.js version
FROM node:24-bullseye

# Set working directory inside container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies including connect-mongo
RUN npm install

# Copy the rest of the backend source code
COPY . .

# Expose backend port
EXPOSE 4242

# Start the backend
CMD ["npm", "start"]
>>>>>>> 1c6e04d (sso setup from pwndoc-ng to pwndoc)
