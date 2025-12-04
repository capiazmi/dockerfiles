# Style and Conventions
- Encoding/newlines: UTF-8, LF, final newline enforced via .editorconfig.
- Indentation: YAML uses 2-space indent; Makefiles use tabs; other files unspecified (follow existing style: shell scripts are POSIX sh with `set -eu`).
- Shell: `scripts/init.sh` uses portable /bin/sh, exits on error/undef vars; prefer the same style for new scripts.
- PHP/App config: Config files live under `debian/php` and `debian/nginx`; keep permissions/ownership consistent for app/public/storage as in init script.
- Images/build: Dockerfile relies on ARG PHP (default 8.4) and URL to released Invoice Ninja tarball; avoid hardcoding architecture-specific paths beyond current chrome/chromium logic.