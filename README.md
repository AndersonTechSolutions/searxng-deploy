# searxng-deploy

Deployment for **AndersonTech Search** — a self-hosted [SearXNG](https://github.com/searxng/searxng)
privacy-respecting metasearch instance, managed by Komodo on the Docker host.

- Image: `searxng/searxng:latest` (Komodo `poll_for_updates` tracks new releases)
- Compose: [`deploy/compose.searxng.yml`](deploy/compose.searxng.yml)
- Host config: `/opt/searxng/settings.yml` (JSON API enabled; not in this repo)
- Secret: injected via the Komodo Variable `SEARXNG_SECRET` (never committed)
- Exposure: internal only, bound to `10.10.0.162:8095`

Used as a company search portal and as a JSON search API (web + image search)
for automation and AI tooling.
