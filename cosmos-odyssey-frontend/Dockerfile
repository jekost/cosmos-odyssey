# Use an official Node.js image as a build stage
FROM node:18 AS build

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# Copy the rest of the application
COPY . .

# Build the React app
RUN npm run build

# Use nginx for serving static files
FROM nginx:alpine

# Copy built files from the previous step
COPY --from=build /app/dist /usr/share/nginx/html

# Expose the port
EXPOSE 5173

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
#RUN npm run dev
