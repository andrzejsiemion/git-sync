# File Sync - Docker Image

## Disclaimer

This project is complete overengineering – although it is fully functional, it was more about learning Docker and GitHub than delivering optimal value.

## Overview

This Docker image push file from local folder to remote repository.

### Features:

- push file from local folder to remote repository

## How to Use

### Pull the Image

To pull the latest version of the Docker image:

```sh
docker pull ghcr.io/andrzejsiemion/file-sync:latest
```

Or pull a specific version:

```sh
docker pull ghcr.io/andrzejsiemion/file-sync:0.0.5
```

### Run the Container

```sh
docker run -d --name file-sync \
  -e GIT_REPO=name_of_remote_repository \
  -e GIT_BRANCH=main \
  -e GIT_EMAIL=user@example.com \
  -e GIT_NAME=robot \
  -e CRON_SCHEDULE="*/2 * * * *" \
  -e TZ=Europe/Warsaw \
  ghcr.io/andrzejsiemion/git-sync:latest
```
