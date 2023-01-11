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
DEPLOYER_VERSION_7 | v7.1.1
DEPLOYER_VERSION_6 | v6.9.0

## Docker Hub

**Build images**

```bash
cd 7.4
docker build -t rdoepner/docker-deployer:7.4 .

cd 8.0
docker build -t rdoepner/docker-deployer:8.0 .

cd 8.1
docker build -t rdoepner/docker-deployer:8.1 .

cd 8.2
docker build -t rdoepner/docker-deployer:latest -t rdoepner/docker-deployer:8.2 .
```

**Push images**

```bash
docker push rdoepner/docker-deployer:7.4
docker push rdoepner/docker-deployer:8.0
docker push rdoepner/docker-deployer:8.1
docker push rdoepner/docker-deployer:8.2
docker push rdoepner/docker-deployer:latest
```
