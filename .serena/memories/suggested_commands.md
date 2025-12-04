# Suggested Commands
- Repo inspection: `ls`, `rg --files`, `rg <pattern>`.
- Compose lifecycle: `cd debian && docker compose up -d`, `docker compose down`, `docker compose ps`, `docker compose logs -f app`.
- Build/pull images: `cd debian && docker compose build` (rebuild app image), `docker compose pull && docker compose up -d` (upgrade).
- Artisan/app maintenance: `docker compose exec app php artisan key:generate --show`, `docker compose exec app php artisan migrate --force`, `docker compose exec app php artisan cache:clear`, `docker compose exec app php artisan ninja:design-update`, `docker compose exec app php artisan optimize`.
- One-off key gen without running stack: `docker run --rm -it invoiceninja/invoiceninja-debian php artisan key:generate --show`.
- Database/redis connectivity (via containers): `docker compose exec mysql mysql -u$MYSQL_USER -p$MYSQL_PASSWORD`, `docker compose exec redis redis-cli ping`.
- Generic Linux utils available: `cat`, `cp`, `mv`, `find`, `grep`, `sed`, `awk` (use `rg` for fast search).