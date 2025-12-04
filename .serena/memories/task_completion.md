# Task Completion Checklist
- If you changed Docker build or configs, run `cd debian && docker compose build` (and `docker compose up -d` to apply) to ensure image builds and services start.
- If environment changes, update `debian/.env` and ensure sensitive values are set (APP_KEY, IN_USER_EMAIL/PASSWORD for first run, DB creds).
- Validate stack health: `docker compose ps`, `docker compose logs -f app` (look for init/migrate output), ensure nginx serves via exposed port 80.
- No automated tests detected in repo; consider manual verification inside running containers (artisan commands, ping db/redis) when relevant.
- Keep permissions/ownership for `/var/www/html/public` and `/var/www/html/storage` aligned with init script expectations.