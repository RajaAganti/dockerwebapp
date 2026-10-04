FROM mysql:5.7.25

# App database and user (read from build args or runtime env)
ENV MYSQL_ROOT_PASSWORD="devopspassword"
ENV MYSQL_DATABASE="accounts"

# Seed data — runs only on first init of an empty data dir
ADD Docker_db/db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql

EXPOSE 3306

# Official image already has a sane CMD; no need to override
