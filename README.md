# family-guard-healthcheck
Outside-Cloudflare backup check. Every ~30 min it calls the public `/health` endpoints (heartbeat ages only, no device data, no secrets). If something is stale or unreachable it opens or updates one `outage` issue, which GitHub emails to the owner. When things recover it closes the issue. Test with Actions > Run workflow > force_fail.
