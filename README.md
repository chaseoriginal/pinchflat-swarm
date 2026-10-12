# pinchflat-swarm

YouTube content downloader for Plex.

## Stack

- **Host**: ore-dock-110-1
- **Stack**: `pinchflat-swarm`
- **Image**: ghcr.io/kieraneglin/pinchflat:latest
- **Config**: named volume `pinchflat-swarm.config`
- **Downloads**: `/media/Multimedia/Incoming/pinchflat`

## Ports

| Port | Published | Protocol |
|------|----------|----------|
| 8945 | 8945 | TCP |

## Deploy

```bash
ssh ore-dock-110-1
cd /data/compose/pinchflat-swarm
set -a && source .env && docker stack deploy -c docker-compose.yml --with-registry-auth pinchflat-swarm && set +a
```
