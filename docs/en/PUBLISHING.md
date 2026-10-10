# Classification & Multi-Platform Publishing

## Classification Is Central

Tel-News is designed around category-aware publishing. Classification is not merely a display label; it can control downstream routing.

Examples include:

- Sports
- Politics
- General
- Additional configurable categories

## Category-to-Destination Routing

A category can be mapped to one or more destinations. Different categories can therefore be published independently to specialized channels.

```text
Sports   -> Sports destination(s)
Politics -> Political destination(s)
General  -> General destination(s)
```

## Multi-Platform Design

Publishing is separated behind output adapters. This allows the same processed news object to be delivered to different supported platforms without rebuilding the ingestion/analysis pipeline.

Telegram is currently an important operational output and management surface, while the architecture is intentionally broader and can accommodate other messaging/social publishing destinations.

## Benefits

- One ingestion pipeline for many destinations
- Category-specific editorial channels
- Platform-independent core processing
- Easier addition of new output platforms
- Consistent classification and quality rules across destinations
