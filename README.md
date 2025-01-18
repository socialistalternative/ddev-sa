# ddev-sa

Opinionated DDEV config for our Drupal/CiviCRM installations.

## Installation

```sh
ddev add-on get socialist-alternative/ddev-sa
```

## Setup

Add hooks to `.ddev/config.yaml`:

```yaml
hooks:
  post-import-db:
    - exec: "drush cr"
  post-start:
    - exec: ".ddev/bin/setup"
```

To support building a theme, define the theme name in `.ddev/.env`:

```env
THEME=my_theme
```

To support Vite for theme development, expose ports in `.ddev/config.yaml`:

```yaml
web_extra_exposed_ports:
  - name: vite
    container_port: 5173
    http_port: 5172
    https_port: 5173
```
