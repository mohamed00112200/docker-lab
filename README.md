# Docker Lab

## Problem 1
Run hello-world container.

## Problem 2
Run ubuntu container in interactive mode.

## Problem 3
Deploy MySQL database container.

Command:
```bash
docker run -d --name app-database -e MYSQL_ROOT_PASSWORD=P4sSw0rd0! -p 3306:3306 mysql:latest
```

## Problem 4
Run nginx and add static HTML files.

## Problem 5
Containerize Python app using Dockerfile.

Build:
```bash
docker build -t python-app .
```

Run:
```bash
docker run python-app
```