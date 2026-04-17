# Finera User Manual

Osnovni kostur projekta za korisnicko uputstvo uradjen pomocu **Material for MkDocs**.

## Pokretanje lokalno

1. Instalirati zavisnosti:

```bash
pip install -r requirements.txt
```

2. Pokrenuti lokalni server:

```bash
mkdocs serve
```

3. Otvoriti adresu:

```text
http://127.0.0.1:8000
```

## Deploy

Repo je pripremljen za objavu na:

- GitHub Pages
- Cloudflare Pages
- Read the Docs

### GitHub Pages

Workflow za GitHub Pages je u:

`./.github/workflows/github-pages.yml`

Potrebno je samo da u GitHub repozitorijumu ukljucite:

`Settings -> Pages -> Build and deployment -> GitHub Actions`

### Cloudflare Pages

Pri povezivanju repoa u Cloudflare Pages koristite:

- Production branch: `main`
- Build command: `mkdocs build --strict`
- Build output directory: `site`

Dodajte i environment variable:

- `PYTHON_VERSION=3.13`
- `SITE_URL=https://<vas-pages-domen>/`

Ako koristite podrazumevani Pages domen, to ce biti nesto poput:

`https://finera-user-manual.pages.dev/`

### Read the Docs

Repo sadrzi konfiguraciju:

`./.readthedocs.yaml`

U Read the Docs je dovoljno:

1. importovati GitHub repo
2. potvrditi da koristi `.readthedocs.yaml`
3. pokrenuti prvi build

Na Read the Docs strani `site_url` se automatski preuzima iz promenljive:

`READTHEDOCS_CANONICAL_URL`
