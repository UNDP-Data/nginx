# nginx

This is Dockerfile of nginx for geohub. It will build Docker image with customised nginx.conf

## register docker image to Github Pakcage's Container Registy

- create personal access token

see [here](https://github.com/settings/tokens)

select `read:packages`, `write:packages` and `delete:packages`

```bash
$export CR_PAT=YOUR_TOKEN
$echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
```

Build and push docker image to private Github package

```bash
$docker build -t ghcr.io/undp-data/nginx:latest .
$docker push ghcr.io/undp-data/nginx:latest
```
