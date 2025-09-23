# A Docker container that contains WordPress with php-fpm 
# (it must be installed and configured) only, without nginx.
# A volume that contains your WordPress database.
# A second volume that contains your WordPress website files.

FROM debian:bullseye

RUN apt update && apt install -y --no-install-recommends \
    wget \
    curl \
    gnupg2 \
    lsb-release \
    && rm -rf /var/lib/apt/lists/*



