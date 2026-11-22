---
name: Docker والنشر المستمر
description: النشر والتشغيل: Docker، Dockerfile، docker compose، CI/CD، GitHub Actions، الخوادم، النشر التلقائي، الاستضافة، المراقبة. docker dockerfile compose container containers kubernetes k8s ci cd pipeline actions deploy deployment devops nginx vps linux hosting دوكر حاويات استضافة النشر نشر التلقائي
version: 1.0.0
category: coding
---
Use this for containers, CI/CD pipelines and deploying services.
1. Dockerfile: an official slim base image pinned to a version; a multi-stage build (tools in the build stage, only the output in the runtime stage); copy dependency manifests and install before copying source so layers cache; run as a non-root user; set production mode; add a HEALTHCHECK; never bake credentials into the image, inject them at runtime.
2. A .dockerignore that excludes dependency folders, build output, logs and local credential files.
3. docker compose for local stacks: app, database and cache with named volumes, health-based depends_on, and ports bound to localhost.
4. CI on every pull request: install from the lock file, lint, type-check, unit tests, build, then integration tests against service containers; cache dependencies; keep it under about ten minutes.
5. CD: build once, tag the image with the commit hash, deploy the same image to staging and then production, run migrations as a separate step, keep a one-command rollback to the previous tag.
6. Credentials live in the CI or host secret store and arrive as environment variables; scope them to the minimum and rotate them.
7. Production basics: TLS at a reverse proxy or the platform, restart policies, resource limits, central logs, uptime and error alerts, automated database backups with a tested restore.
8. Zero-downtime deploys need health checks and backward-compatible database changes.
Answer shape: complete files (Dockerfile, compose or workflow YAML), then the commands to build, test and deploy.
