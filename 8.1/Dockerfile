FROM wodby/php:8.1

ARG DEPLOYER_VERSION_7=v7.0.1

USER root

RUN set -ex; \
    wget -qO /usr/local/bin/deployer https://github.com/deployphp/deployer/releases/download/${DEPLOYER_VERSION_7}/deployer.phar; \
    chmod +x /usr/local/bin/deployer

USER wodby
