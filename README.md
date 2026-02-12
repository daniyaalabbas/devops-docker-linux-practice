# Docker Nginx Static App – DevOps Practice

This project demonstrates how to deploy a static HTML application using Docker and Nginx.

By Abbas Ali .....

## Tech Used
- Docker
- Nginx
- Ubuntu (WSL)
- GitHub

## Steps Performed

1. Created a custom `index.html`
2. Wrote a Dockerfile using nginx base image
3. Built a Docker image
4. Ran a container with port mapping
5. Accessed the app on browser using `localhost:8080`

## Dockerfile

```dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html

