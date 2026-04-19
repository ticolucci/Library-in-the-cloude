# 📚 Library in the Cloude — Claude Code Context

This repo is Thiago’s personal audiobook library management system.
Three files are the source of truth — always read them before answering
questions about the library, queue, wishlist, or making recommendations.

## Data Files

|File              |Purpose                                      |
|------------------|---------------------------------------------|
|`library.yaml`    |Full audiobook library (~197 books)          |
|`wishlist.yaml`   |Books to read eventually (~73+ entries)      |
|`next-in-queue.md`|Immediate reading queue, ordered and reasoned|

## YAML Schemas

### library.yaml — per entry

```yaml
title:
author:
year:
series:
series_number:
universe:           # e.g. "Cosmere" for Sanderson books
rating:             # 1–10
status:             # read | dnf | dont-remember
date_read:
format:             # audiobook | ebook | physical
source:             # audible | apple-books | etc.
tags: []
reread:             # true | false
potential_reread:   # true | false
genre:
sub_genre:
audiobook_hours:
```

### wishlist.yaml — per entry

```yaml
title:
author:
year:
genre:
sub_genre:
series:
series_number:
tags: []
audiobook_hours:
priority:           # high | medium | low
reason:
source:             # how it was discovered
series_status:      # complete | ongoing
available_on_audible:
note:
```

### next-in-queue.md

Ordered Markdown list. Each entry includes: title, author, year, length,
genre, series, tags, Audible availability, and a “Why now” rationale.

## Reader Profile

Thiago’s tastes, for recommendations and wishlist curation:

**Loves:** LitRPG · humor · hard magic systems · progression fantasy ·
web-serial-origin fiction · epic fantasy · slice-of-life fantasy ·
apocalyptic · isekai · Cosmere

**Dislikes:** chosen-one tropes · cultivation without humor · novellas ·
classic fantasy without modern energy · Cradle-style cultivation ·
Murderbot-style AI fiction

**Key signals:**

- Every book over 30h has been rated 10/10 — epic length is a strong buy signal
- Non-fiction sweet spot: ~10h, punchy and idea-dense
- Top series by investment: Stormlight Archive (268h), HWFWM (219h),
  Wandering Inn (158h), Dungeon Crawler Carl (134h)
- DNF history: Wheel of Time, Red Rising, Cradle, Murderbot, Crescent City,
  Hyperion Cantos — these inform risk flags for similar books
- Unfinished series are a meaningful risk: Thiago has abandoned long series
  mid-way before; flag ongoing series in wishlist entries

**Wishlist curation rules:**

- Bar for adding is low; bar for skipping is high
- “Doesn’t fit reading pattern” is not a valid skip reason
- Only skip on genuine quality concerns or strong predicted dislike
- Maybes default to adding

## When Updating Files

- Edit files directly in the repo (that’s the point of using Claude Code)
- Never guess at field values — ask if unsure
- Don’t update dynamic stats (book counts, total hours) in this file —
  those live in the data files themselves
- Audible UK ratings are unreliable due to low volume; prefer Goodreads