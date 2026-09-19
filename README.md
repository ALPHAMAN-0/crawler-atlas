# Crawler Atlas — code & data flow

Documentation and system-design explainers for **Crawler Atlas**, a polite,
incremental web crawler: give it a site, it visits on a schedule, notices what
changed, uses AI to pull the useful facts out of each page, and writes them as
rows in a table you own.

**Live page:** https://alphaman-0.github.io/crawler-atlas/

## Contents

- [`index.html`](index.html) — *How Google Crawls the Web*, a system-design
  explainer covering crawl budget, rendering, and indexing — background reading
  for anyone building or reasoning about a crawler. This is the page served
  live above.
- [`crawler-explained.md`](crawler-explained.md) — *The Crawler, Explained
  Simply*: a plain-language walkthrough of Crawler Atlas itself — jobs, runs,
  the incremental content-hash check, the recipe/LLM extraction split, the
  rules that protect existing data, and where everything lives in the codebase.

## Why two documents

`index.html` is general background on how crawling works at web scale (Google's
approach). `crawler-explained.md` is the specific design of this project's own
crawler, including its worker pools, database layout, and the ten rules it
never breaks.
