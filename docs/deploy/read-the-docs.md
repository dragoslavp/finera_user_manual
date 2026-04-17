# Read the Docs

Ovaj projekat je pripremljen za objavu na **Read the Docs**.

## Konfiguracija u repou

U korenu projekta se nalazi fajl:

`/.readthedocs.yaml`

On definiše:

- `version: 2`
- `ubuntu-24.04`
- `python: 3.13`
- korišćenje `mkdocs.yml`
- instalaciju paketa iz `requirements.txt`

## Koraci

1. Povežite GitHub repo sa Read the Docs nalogom.
2. Importujte projekat.
3. Potvrdite build konfiguraciju iz `.readthedocs.yaml`.
4. Pokrenite prvi build.

## Canonical URL

Na Read the Docs platformi `site_url` se automatski preuzima iz promenljive:

`READTHEDOCS_CANONICAL_URL`

Zbog toga nije potrebno posebno menjati `mkdocs.yml` za RTD objavu.
