FROM php:7.2

ARG COMPOSER_VERSION=1.8.6
ARG DEPLOYER_VERSION=6.4.3

ARG APP_USER=rdoepner
ARG APP_UID=1000
ARG APP_GROUP=rdoepner
ARG APP_GID=1000

# Create app user
RUN set -ex; \
    addgroup --gid $APP_GID $APP_GROUP; \
    adduser --uid $APP_UID --gid $APP_GID --disabled-password --gecos "" $APP_USER

# Install system requirements
RUN set -ex; \
    apt-get update && apt-get install --yes \
        rsync \
        wget \
        curl \
        git \
        unzip \
        mysql-client \
        openssh-client \
        zlib1g-dev; \
    \
    rm -rf /var/lib/apt/lists/*

# Install extensions
RUN set -ex; \
    docker-php-ext-install zip

# Install composer
RUN set -ex; \
    wget -qO - https://getcomposer.org/installer | php -- \
        --install-dir=/usr/local/bin \
        --filename=composer \
        --version=$COMPOSER_VERSION

# Install deployer
RUN set -ex; \
    wget -qO /usr/local/bin/deployer \
        https://deployer.org/releases/v$DEPLOYER_VERSION/deployer.phar; \
    \
    chmod +x /usr/local/bin/deployer
