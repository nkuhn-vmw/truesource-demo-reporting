# truesource-demo-reporting

Demo finance reporting for [TrueSource Viewer](https://github.com/nkuhn-vmw/truesource-viewer-hub-edition).

**Intentionally vulnerable demo. Do not deploy it, do not install from it.** It contains only
manifests and lock files, written by hand: the lock files have no integrity hashes, and the
versions named below are pinned on purpose so that the viewer has something to find.

A Django reporting site with Celery jobs, versions locked with Pipenv.

| File | Pins | What the viewer should report |
|---|---|---|
| `Pipfile.lock` | `django` 3.2.0 | Django 3.2 is past its end of life, with many known vulnerabilities |
| `Pipfile.lock` | `urllib3` 1.26.4, `cryptography` 3.3.1, `celery` 5.0.5, `sqlparse` 0.4.1, `gunicorn` 20.0.4 | Known vulnerabilities |
| `Dockerfile` | `python:3.9.7-slim` | An old Python 3.9 image |
| `compose.yaml` | `bitnami/postgresql:12.9.0`, `bitnami/redis:6.2.6` | PostgreSQL 12 is past its end of life |
