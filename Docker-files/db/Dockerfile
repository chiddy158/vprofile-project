# Use the MySQL 8.0.33 base image
FROM mysql:8.0.33

# Set labels to provide information about the project and author
LABEL "Project"="Vprofile"
LABEL "Author"="Chidi"

# Set environment variables
ENV MYSQL_DATABASE="accounts"
ENV MYSQL_ROOT_PASSWORD="vprodbpass"

# Copy the SQL backup script to the initdb.d directory
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
