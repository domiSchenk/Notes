---
id: xhto3wky6qxp78cpg6u7stq
title: Volumes
desc: ''
updated: 1646977210707
created: 1646977191417
---


# Docker Volumes
## Create external volume

```bash
docker volume create --driver local --opt type=none --opt device=/home/domischenk/share --opt o=bind <name>
```
