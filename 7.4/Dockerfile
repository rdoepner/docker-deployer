FROM wodby/php:7.4

ARG DEPLOYER_VERSION_6=v6.9.0
ARG DEPLOYER_VERSION_7=v7.1.1

USER root

RUN set -ex; \
    wget -qO /usr/local/bin/deployer https://github.com/deployphp/deployer/releases/download/${DEPLOYER_VERSION_7}/deployer.phar; \
    chmod +x /usr/local/bin/deployer

RUN set -ex; \
    wget -qO /usr/local/bin/deployer6 https://deployer.org/releases/${DEPLOYER_VERSION_6}/deployer.phar; \
    chmod +x /usr/local/bin/deployer6

USER wodby
