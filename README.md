# Twitter Data Scraping & Analysis: "Sessiz İstila" (2021–2022)

An R-based analysis pipeline for historical Twitter data collection, text preprocessing, statistical analysis, and Social Network Analysis (SNA) focusing on the Turkish Twitter term **"sessiz istila"** (Silent Invasion).

## Project Overview

This repository contains the R scripts and code workflows used to scrape, process, and analyze historical Twitter data between **June 1, 2021** and **December 31, 2022**. The dataset captures the origin, spread, temporal spikes, and network characteristics of the phrase *"sessiz istila"* on Twitter prior to the Twitter API v2 access model changes.

### Key Highlights
* **Total Tweets Collected:** 47,024 tweets
  * **2021:** 1,502 tweets
  * **2022:** 45,522 tweets (30x volume increase compared to 2021)
* **First Notable Mention:** Tracked back to June 8, 2021, via [@KaracasuHande](https://twitter.com/KaracasuHande/status/1402203834668273665).
* **Peak Activity Day:** June 27, 2022, reaching **6,077 tweets** in a single day.

---

## Features & Analysis Workflow

1. **Data Scraping & Extraction:**
   * Historical Tweet collection using `academictwitteR` across specified temporal ranges.
   * Exporting raw data into `.json`, `.RData`, and `.xlsx` formats.

2. **Data Cleaning & Preprocessing:**
   * Text normalization: lowercase conversion, removing RT headers, handles, hashtags, URLs, emoticons, numbers, and extra whitespace.
   * Removal of Turkish stopwords using a custom stopword dictionary.

3. **Statistical Analysis & Visualization:**
   * Daily and monthly tweet volume summaries (means, medians, quartiles).
   * Time-series plotting with `ggplot2` to pinpoint discourse spikes and trend shifts across 2021 and 2022.
   * Word frequency analysis (top 40 terms), word clouds (`wordcloud`), and n-gram breakdowns (Bigrams, Trigrams, 4-grams).

4. **Social Network Analysis (SNA):**
   * Mentions and retweets network construction via `igraph`.
   * Exporting graph network files (`.gml`) for visualization in **Gephi**.

5. **Human Coding Preparation:**
   * Cleaning duplicate text entries and exporting randomized samples for manual sentiment and thematic coding.

---

## Required R Packages

Ensure you have the following packages installed before running the `.Rmd` script:

```R
install.packages(c(
  "academictwitteR",
  "writexl",
  "readxl",
  "dplyr",
  "lubridate",
  "ggplot2",
  "scales",
  "tm",
  "qdapRegex",
  "SnowballC",
  "tidytext",
  "wordcloud",
  "igraph"
))
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

