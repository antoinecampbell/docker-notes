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
    -v portainer:/data \
    portainer/portainer \
    --no-auth
```

```bash
docker start portainer
```

## Nexus OSS
```bash
docker pull sonatype/nexus3
```

```bash
docker volume nexus-data
```

```bash
docker create --name nexus \
    -p 8081:8081 \
    -v nexus-data:/nexus-data \
    sonatype/nexus3
```

```bash
docker start nexus
```

```bash
docker exec -it nexus /bin/bash -c "cat /nexus-data/admin.password"
```

## SonarQube
```bash
docker pull sonarqube:8-community
```

```bash
docker volume create sonarqube
```

```bash
docker create --name sonarqube \
    -p 9000:9000 \
    -v sonarqube:/opt/sonarqube \
    sonarqube:8-community
```

```bash
docker start sonarqube
```
