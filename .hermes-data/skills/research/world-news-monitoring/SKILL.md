---
name: world-news-monitoring
description: "Monitor and summarize global and regional news using browser and search tools."
version: 1.0.0
author: Hermes
license: MIT
metadata:
  hermes:
    tags: [news, research, monitoring, summary, global, regional]
---

# World News Monitoring

This skill provides a structured approach to monitoring and summarizing latest news from various regions and domains.

## Workflow

1.  **Broad Search**: Use `browser_navigate` or `web_search` with date-specific queries (e.g., "latest news May 4 2026") to get a high-level overview.
2.  **Source Diversification**: Check multiple reputable international sources (e.g., The Guardian, SCMP, Reuters, AP) to avoid regional bias.
3.  **Targeted Queries**: When searching for specific regional news (e.g., "China news"), use localized search terms or visit regional sections of major news sites.
4.  **Categorized Summarization**: Group findings into logical categories like:
    *   International Dynamics
    *   Regional Focus
    *   Business & Economy
    *   Science & Technology
    *   Social & Culture
5.  **Offer Deep-Dives**: Always offer to perform a more detailed search on specific items of interest.

## Pitfalls

*   **Bot Detection**: Google Search can be aggressive with bot detection. If blocked, fallback to Bing, DuckDuckGo, or direct navigation to news homepages.
*   **Stale Results**: Always include the current date in search queries to ensure results are truly from "today".
*   **Language Barrier**: For non-English regions, searching in the local language (if possible) or visiting the English version of local outlets (e.g., SCMP for China) provides better depth.

## Verification

*   Check the timestamp of the articles to ensure they are recent.
*   Cross-reference major breaking news across at least two sources.
