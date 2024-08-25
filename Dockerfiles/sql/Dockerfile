FROM mysql:8.0.33
LABEL "Project" = "Docker-Local"
LABEL "Author" = "MSaqibBhatti"

ENV MYSQL_ROOT_PASSWORD = "sqlpass"
ENV MYSQL_DATABASE = "accounts"

ADD db-backup.sql docker-entrypoint-initdb.d/db_backup.sql