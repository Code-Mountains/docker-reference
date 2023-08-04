# Use the Nginx image from Docker Hub as a base
FROM nginx:alpine

# Remove the default Nginx configuration file
RUN rm /etc/nginx/conf.d/default.conf

# Replace with our own configuration file
COPY nginx.conf /etc/nginx/conf.d/

# Create a directory for our app
RUN mkdir -p /usr/share/nginx/html/app

# Copy the HTML file
COPY index.html /usr/share/nginx/html/app

# Expose port 80
EXPOSE 80

# Start Nginx when the container has provisioned.
CMD ["nginx", "-g", "daemon off;"]
