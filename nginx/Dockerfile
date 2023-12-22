# Use the official Nginx base image
FROM nginx:latest

RUN apt-get update && apt-get install -y \
    vim \
    curl \
    wget \
    git \
    zip \
    unzip \
    && rm -rf /var/lib/apt/lists/*

# Copy the static HTML files to the Nginx document root
COPY ./default.conf /etc/nginx/conf.d/default.conf

# Expose port 80 for HTTP traffic
EXPOSE 80

# Start Nginx server
CMD ["nginx", "-g", "daemon off;"]