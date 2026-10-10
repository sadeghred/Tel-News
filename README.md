# Tel-News

**Multi-Source AI-Powered News Intelligence, Classification & Multi-Platform Publishing System**

[فارسی](README.fa.md) · [Architecture](docs/en/ARCHITECTURE.md) · [Pipeline](docs/en/PIPELINE.md) · [Publishing](docs/en/PUBLISHING.md) · [Security](docs/en/SECURITY.md)

> **Public repository scope:** project presentation and documentation only. Private source code, production credentials, deployable packages, databases, and application downloads are not published here.

## Overview

Tel-News is not merely a Telegram bot. It is a programmable **news intelligence and publishing platform** designed to collect information from multiple source types, normalize and analyze it, classify news by subject, reduce duplicates, prepare publication-ready content, and route different categories to different destinations across multiple platforms.

Telegram is one supported source, administration interface, and publishing channel — not the architectural boundary of the project.

## Core Capabilities

- Multi-source news ingestion
- Website, Telegram and YouTube-oriented source architecture
- Text/transcript normalization
- AI-assisted event and relevance analysis
- Semantic processing and clustering
- Deduplication before publication
- Persian news rewriting and presentation
- Quality-control stages
- Metadata and hashtag generation
- Database-backed processing state
- Administrative review and monitoring
- **Automatic news classification by category**
- **Independent routing of each news category to different channels/destinations**
- **Multi-platform publishing architecture**
- Central AI integration through AI-Hub

## The Key Idea: Classify Once, Publish Anywhere

A central design goal is to separate **what a news item is** from **where it should be published**.

```text
News Sources
     ↓
Ingestion / Normalization
     ↓
Event + Relevance Analysis
     ↓
Clustering / Deduplication
     ↓
News Classification
     ├── Sports
     ├── Politics
     ├── General
     └── Other configured categories
     ↓
Writing / Quality / Metadata
     ↓
Destination Routing
     ├── Category-specific Telegram channels
     ├── Other messaging/social platforms
     └── Future publishing destinations
```

This means one processing engine can support multiple editorial channels and platforms without duplicating the ingestion and AI pipeline for each destination.

## Sources

The architecture is designed to ingest news from heterogeneous sources. Current/project source work includes:

- Telegram channels
- Websites
- YouTube/video-derived textual content
- Extensible future source adapters

Each source type is normalized before entering the common processing pipeline.

## AI Architecture

Tel-News integrates with the central **AI-Hub** instead of hard-coding every AI provider into the news application. AI-oriented stages can include event extraction, relevance filtering, semantic processing, translation, rewriting, quality review, and other task-based operations depending on deployment configuration.

## Telegram Capability

Telegram remains an important part of the project:

- source monitoring
- category/channel management
- administrative controls
- status and reporting
- user/contact workflows
- publishing to configured Telegram destinations

However, the project itself is a broader news-processing and multi-platform publishing system.

## Current Operational Features

The current administration architecture includes independent management of news sources, categories, advertising-related functions, reporting, user messages, and overall status. Telegram source management is database-backed and supports per-source activation/deactivation and configuration.

## Security

The public repository intentionally excludes API keys, Telegram credentials, AI-provider secrets, server addresses, production databases, authentication secrets, private logs, and deployable private source code.

## Status

Tel-News is an active evolving project. Its ingestion, processing, AI integration, administration, and publishing architecture are being developed incrementally while preserving already working components.

## Contact

- Telegram: [@Sadeghred](https://t.me/Sadeghred)
- Email: [sadeghred@gmail.com](mailto:sadeghred@gmail.com)

---
© 2026 Tel-News Project
