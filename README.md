# Docker Deployer

PHP Docker image for Deployer and Composer

## Usage

**Run Deployer**

```bash
docker run --rm \
    -u rdoepner \
    -v $PWD:/app \
    -w /app \
    rdoepner/docker-deployer deployer
```

**Run Composer**

```bash
docker run --rm \
    -u rdoepner \
    -v $PWD:/app \
    -w /app \
    rdoepner/docker-deployer composer
```

## Build arguments

Argument         | Default value
---------------- | -------------
COMPOSER_VERSION | 1.8.3
DEPLOYER_VERSION | 6.4.3
APP_USER         | rdoepner
APP_UID          | 1000
APP_GROUP        | rdoepner
APP_GID          | 1000
