# GitHub Pages napomena

Za objavu preko GitHub Pages potrebno je:

1. Repository `Settings` -> `Pages`
2. U delu `Build and deployment` izabrati `GitHub Actions`

Workflow `.github/workflows/github-pages.yml` zatim automatski gradi i objavljuje MkDocs sajt pri svakom `push` na `main` granu.

## Važno

Ako će konačni GitHub Pages URL biti drugačiji od:

`https://example.github.io/finera_user_manual/`

onda treba ažurirati polje `site_url` u `mkdocs.yml`.
