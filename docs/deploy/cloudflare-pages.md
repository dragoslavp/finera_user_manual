# Cloudflare Pages

Ovaj projekat je pripremljen za objavu na **Cloudflare Pages**.

## Podešavanja projekta

Pri kreiranju Pages projekta koristite sledeće vrednosti:

- `Production branch`: `main`
- `Build command`: `mkdocs build --strict`
- `Build output directory`: `site`

## Environment variables

Dodajte sledeće environment variables:

- `PYTHON_VERSION=3.13`
- `SITE_URL=https://finera-user-manual.pages.dev/`

Primer:

```text
SITE_URL=https://finera-user-manual.pages.dev/
```

## Napomena

`SITE_URL` se koristi iz `mkdocs.yml`, tako da isti repo moze da se koristi i na drugim hosting platformama bez rucnog menjanja konfiguracije.
