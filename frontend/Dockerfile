# Pin specific version of node to avoid breaking changes
FROM node:18.15

# Specify working directory
WORKDIR /frontend

# Copy package.json and package-lock.json
COPY package*.json ./
# Install dependencies
RUN npm install

# Install ping
RUN apt-get update
RUN apt-get install inetutils-ping

# Copy source code
COPY ./src ./src
# Copy public folder
COPY ./public ./public

# Run frontend
CMD ["npm", "start"]
#CMD ["ls", "-la"]
