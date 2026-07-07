# Running locally

Vestige is two pieces: this **web** front-end and a separate **API** (repo: `vestige-api`).

## API
```bash
# in the vestige-api repo
docker compose up -d                          # PostGIS on localhost:5433
.venv/bin/python -m etl.ingest                # load sample events
.venv/bin/uvicorn api.main:app --port 8000    # http://localhost:8000
```

## Web
```bash
# in this repo
python3 -m http.server 5173                   # http://localhost:5173
```

The front-end reads the API via `API_BASE` at the top of `index.html` (defaults to
`http://localhost:8000`). Point it at a deployed API for production.

## Docs
This site is built with MkDocs:
```bash
pip install mkdocs-material
mkdocs serve
```
