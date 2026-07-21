# Run Renovate Bot locally

## Execute command

```shell
docker run --rm \
  -v "/home/jbordat/Documents/projects/infrastructure/helm/renovate-bot/test/config.json:/usr/src/app/config.json" \
  -e "LOG_LEVEL=debug" \
  -e "RENOVATE_CONFIG_FILE=/usr/src/app/config.json" \
  renovate/renovate:41.97.7
```
