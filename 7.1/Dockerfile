FROM wodby/php:7.1

ARG DEPLOYER_VERSION=6.7.3

USER root

# Install deployer
RUN set -ex; \
    wget -qO /usr/local/bin/deployer \
        https://deployer.org/releases/v$DEPLOYER_VERSION/deployer.phar; \
    \
    chmod +x /usr/local/bin/deployer

USER wodby
