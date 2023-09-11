# ddev-sa

## Installation

```sh
ddev get socialist-alternative/ddev-sa
ddev restart
```

## Required configuration

Add the following to `.ddev/config.yaml`:

```yaml
hooks:
  post-import-db:
    - exec: "drush cr"
  post-start:
    - exec: ".ddev/bin/setup"
```

## Configuration for theme development

```yaml
web_extra_exposed_ports:
  - name: vite
    container_port: 5173
    http_port: 5172
    https_port: 5173
hooks:
  post-import-db:
    - exec: "drush cr"
  post-start:
    - exec: "THEME=sa .ddev/bin/setup"
```
