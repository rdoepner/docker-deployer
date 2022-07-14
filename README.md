# PHP Deployer

Docker image for Deployer and Composer

Base image: [wodby/php](https://github.com/wodby/php)

## Usage

**Run Deployer**

```bash
docker run --rm -v $PWD:/app -w /app rdoepner/docker-deployer deployer
```

**Run Composer**

```bash
docker run --rm -v $PWD:/app -w /app rdoepner/docker-deployer composer
```

## User

Name  | UID  | GID
----- | ---- | ---
wodby | 1000 | 1000

## Build arguments

Argument           | Default Version
------------------ | ---------------
DEPLOYER_VERSION_7 | v7.0.0-rc.8
DEPLOYER_VERSION_6 | v6.8.0
