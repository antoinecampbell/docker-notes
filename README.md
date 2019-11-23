# docker-notes

## Portainer
```bash
docker pull portainer/portainer
```

```bash
docker volume create portainer
```

```bash
docker create --name portainer \
    -p 9000:9000 \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer:/data portainer/portainer \
    portainer/portainer \
    --no-auth
```

```bash
docker start portainer
```
