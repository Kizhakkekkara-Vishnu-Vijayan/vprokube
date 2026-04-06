FROM mysql:8.0.33

LABEL "Project"="Vprofile"
LABEL "Author"="Vishnu"

# Basic DB setup
ENV MYSQL_ROOT_PASSWORD=vprodbpass
ENV MYSQL_DATABASE=accounts
ENV MYSQL_ROOT_HOST=%

# Copy DB init script
COPY db_backup.sql /docker-entrypoint-initdb.d/

# 🔥 Correct CMD format (single line OR properly closed array)
CMD ["mysqld","--innodb-buffer-pool-size=64M","--innodb-log-buffer-size=8M","--max_connections=50","--performance-schema=OFF"]
