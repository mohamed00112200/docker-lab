# Docker Lab Assignment

This repository contains solutions for Docker Lab tasks.

---

# Problem 1

## Run hello-world container

```bash
docker run hello-world
```

## Check all containers

```bash
docker ps -a
```

## Start stopped container

```bash
docker start CONTAINER_ID
```

## Remove container

```bash
docker rm CONTAINER_ID
```

## Remove image

```bash
docker rmi hello-world
```

---

# Problem 2

## Run ubuntu interactive container

```bash
docker run -it ubuntu bash
```

## Run echo command

```bash
echo docker
```

## Create file

```bash
touch hello-docker
```

## Exit container

```bash
exit
```

## Stop container

```bash
docker stop CONTAINER_ID
```

## Remove container

```bash
docker rm CONTAINER_ID
```

## Remove all stopped containers

```bash
docker container prune -f
```

### Comment

The file `hello-docker` is removed after deleting the container because containers are ephemeral.

---

# Problem 3

## Deploy MySQL database

```bash
docker run -d --name app-database -e MYSQL_ROOT_PASSWORD=P4sSw0rd0! -p 3306:3306 mysql:latest
```

## Check running containers

```bash
docker ps
```

## Show logs

```bash
docker logs app-database
```

## Access MySQL container

```bash
docker exec -it app-database bash
```

## Login to MySQL

```bash
mysql -u root -p
```

Password:

```text
P4sSw0rd0!
```

---

# Problem 4

## Run Nginx container

```bash
docker run -d -p 8080:80 --name mynginx nginx
```

## Copy HTML file

```bash
docker cp index.html mynginx:/usr/share/nginx/html/
```

## Commit container

```bash
docker commit mynginx IMAGE_NAME
```

---

# Problem 5

## Python App

### app.py

```python
print("Hello Docker")
```

---

## Dockerfile

```dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY . .

CMD ["python","app.py"]
```

---

## Build Image

```bash
docker build -t python-app .
```

---

## Run Container

```bash
docker run python-app
```

---

## Multi-stage Dockerfile

```dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY app.py .

CMD ["python","app.py"]
```

---

## Push to Docker Hub

```bash
docker login
```

```bash
docker tag python-app YOUR_USERNAME/python-app
```

```bash
docker push YOUR_USERNAME/python-app
```

---

# Docker Concepts Learned

- Docker Images
- Containers
- Dockerfile
- Interactive Mode
- Background Containers
- Environment Variables
- Port Mapping
- Docker Hub
- MySQL Containers
- Nginx Containers
- Python Containerization

---

# Author

Mohamed Lotfy Mohamed Atya