FROM mariadb:10.1

# COPY ./initDatabase.sql /var/initDatabase.sql

COPY ./initDatabase.sql /docker-entrypoint-initdb.d/

# RUN mysql -u root -p mysql < /var/initDatabase.sql

