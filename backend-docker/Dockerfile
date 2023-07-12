# Use the official Golang image as the base image
FROM golang:1.19

# Set the working directory inside the container
WORKDIR /app

# Copy the backend folder into the container
COPY backend/ .

# Install dependencies
RUN go get ./...

#Set Environment Variables
ARG db_host
ENV DB_HOST $db_host
ARG db_user
ENV DB_USER $db_user
ARG db_password
ENV DB_PASSWORD $db_password
ARG db_name
ENV DB_NAME $db_name
ARG db_port
ENV DB_PORT $db_port
ARG origins
ENV ALLOWED_ORIGINS $origins

# Expose the port on which the backend server runs
EXPOSE 8080

# Run the backend application
CMD ["go", "run", "main.go"]
