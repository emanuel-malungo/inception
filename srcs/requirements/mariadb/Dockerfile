# A Docker container that contains only MariaDB, without nginx.

FROM debian:bullseye

RUN apt update && apt install -y --no-install-recommends \
    mariadb-server \
    && rm -rf /var/lib/apt/lists/*