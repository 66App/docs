# 66App Docs

This repository contains the technical and user documentation for **66App** — a social content platform built with Flutter 3.24 (mobile) and Go 1.24 (backend).

## Contents

| Document | Description |
|---|---|
| [Architecture Overview](docs/66app_architecture_overview.html) | Full architecture map covering every layer of the stack: Flutter frontend, Go API server, PostgreSQL, Redis, MinIO/S3, and Meilisearch. |
| [Developer Manual](docs/dev-manual.html) | Step-by-step guide for setting up the development environment, coding conventions, and contribution workflows. |
| [User Manual](docs/user-manual.html) | End-user guide covering all app features and how to use them. |

## About 66App

66App is a social content platform with the following features:

- **Home feed** — personalised content feed
- **Shorts** — short-form video
- **Post creation** — images and video with captions and hashtags
- **Search** — full-text search across posts, hashtags, and users (Meilisearch)
- **User profiles** — follow/unfollow, bio, avatar
- **Notifications** — activity alerts
- **Affiliate programme** — HMAC-signed affiliate links with click and conversion tracking

### Tech stack

| Layer | Technology |
|---|---|
| Mobile client | Flutter 3.24 · Riverpod · GoRouter · Dio · PASETO |
| API server | Go 1.24 · Chi router · sqlc |
| Database | PostgreSQL (26 migrations, cursor-based pagination) |
| Cache | Redis 7 (feed cache, sessions, rate limiting) |
| Media storage | MinIO / AWS S3 (presigned upload flow) |
| Search | Meilisearch (posts, hashtags, users) |