
# Use the official Node.js image as the base image
FROM node:18.16

# Set the working directory inside the container
WORKDIR /app

# Copy the frontend folder into the container
COPY frontend/packages*.json ./

# Remove and Install dependencies
# RUN rm -rf node_modules package-lock.json
RUN npm install 

COPY . .
# Expose the port on which the frontend server runs
EXPOSE 3000

# Run the frontend application
CMD ["npm", "start"]
