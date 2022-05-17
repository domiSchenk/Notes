

# Docker Volumes
## Create external volume

```bash
docker volume create --driver local --opt type=none --opt device=/home/domischenk/share --opt o=bind <name>
```
