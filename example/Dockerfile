FROM node

# Set the working directory
WORKDIR /api

RUN apt update && apt install -y dnsutils && apt install -y net-tools

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port
EXPOSE 3000

# Start the application
CMD ["node", "app.js"]
