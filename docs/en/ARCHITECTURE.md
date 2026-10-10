# Architecture

## Architectural Goal

Tel-News separates source acquisition, news understanding, editorial preparation, classification, and destination publishing into distinct stages.

```text
Sources
  ↓
Source Adapters
  ↓
Normalization / Transcript
  ↓
Event & Relevance Processing
  ↓
Clustering / Deduplication
  ↓
Category Classification
  ↓
Writing / Quality / Metadata
  ↓
Review / Routing
  ↓
Platform Output Adapters
```

## Source Layer

Source-specific collectors handle Telegram, websites, YouTube-derived content, and future adapters. The goal is to normalize heterogeneous inputs before the common pipeline.

## Processing Layer

The processing pipeline performs local deterministic work where appropriate and delegates selected semantic tasks to AI-Hub.

## Classification Layer

Classification is a first-class architectural stage. A news item can be assigned to a configured subject such as sports, politics, general news, or future custom categories.

## Routing Layer

Category and destination are separate concepts. Routing rules can map different categories to different channels or platforms.

## Output Layer

Output adapters isolate platform-specific publishing behavior from the core news-processing engine. Telegram is one implementation; the architecture is intended to support additional destinations.

## Administration

Administrative tooling manages source state, categories, monitoring, reporting, publishing-related settings, and operational status without redefining the core processing pipeline.
