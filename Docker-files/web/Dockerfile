# Use the official NGINX image as the base image
FROM nginx

# Set labels to provide information about the project and author
LABEL "Project"="Vprofile"
LABEL "Author"="Chidi"

# Remove the default NGINX configuration file
RUN rm -f /etc/nginx/conf.d/default.conf

# Copy your custom NGINX configuration file to the container
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
