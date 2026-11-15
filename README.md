# Sports News NLP: Information Extraction and Analysis

## Project Overview

This project explores Natural Language Processing (NLP) techniques using sports news articles from The Guardian.

Using Python and spaCy, the project analyses unstructured sports news text to identify linguistic structures, recognise named entities and extract information related to players, scoring events and disciplinary actions.

The project demonstrates how NLP techniques can be used to transform unstructured news articles into more structured and meaningful information.

## Dataset and Data Source

- **Data Source:** The Guardian
- **Number of Articles:** 5
- **Data Type:** Unstructured textual data
- **Data Collection Method:** Web scraping using Goose3

Five sports news articles were extracted from The Guardian, covering international rugby union and football matches.

**Original article URLs:**

1. https://www.theguardian.com/sport/2026/aug/08/australia-wallabies-japan-nations-championship-2026-match-report
2. https://www.theguardian.com/sport/2026/jul/18/argentina-england-nations-championship-rugby-union-match-report
3. https://www.theguardian.com/sport/2026/jul/04/south-africa-england-nations-championship-rugby-union-match-report
4. https://www.theguardian.com/sport/live/2026/jul/11/fiji-v-england-nations-championship-rugby-union-live
5. https://www.theguardian.com/football/2026/jul/19/spain-win-world-cup-ferran-torres-10-man-argentina-extra-time

*Note: The original articles are third-party content. This repository contains the code for extracting and analysing the text rather than redistributing the full articles.*

## Key Features and Methodologies

### 1. Web Scraping and Text Extraction

- Used Goose3 to extract article titles and main text content.
- Collected five sports news articles from The Guardian.
- Combined the extracted articles for further NLP processing.

### 2. Linguistic Analysis

Used spaCy to analyse the grammatical structure of the collected articles.

Techniques included:

- **Part-of-Speech (POS) Tagging:** Identified nouns, proper nouns and verbs.
- **Noun Chunk Extraction:** Extracted noun phrases from the articles.
- **Dependency Parsing:** Examined grammatical relationships between words.
- **Syntactic Analysis:** Identified subjects, direct objects and their associated verbs.
- **Tree Navigation:** Explored relationships between syntactic components.

### 3. Named Entity Recognition (NER)

Applied spaCy's Named Entity Recognition to identify people mentioned in the sports news articles.

The project also explored extracting player names using recognised entities and proper nouns.

### 4. Sports Scoring Event Extraction

Developed rule-based extraction logic to identify sentences containing scoring-related keywords, including:

- Try
- Tries
- Point
- Points
- Score
- Scored
- Scoring

The code attempts to identify player names and associated scoring references from the extracted sentences.

### 5. Disciplinary Event Extraction

Implemented rule-based text processing to identify disciplinary incidents, including:

- Yellow cards
- Red cards

The extraction logic searches for relevant keywords within sentences and attempts to associate the incidents with player names.

## Technologies and Libraries

- Python
- Goose3
- spaCy
- Pandas
- NLTK

## Learning Outcomes

Through this project, I gained practical experience in:

- Extracting unstructured text from online news articles.
- Understanding linguistic structures and grammatical relationships.
- Applying Part-of-Speech tagging and dependency parsing.
- Using Named Entity Recognition to identify people.
- Navigating syntactic dependency trees.
- Developing rule-based information extraction techniques.
- Exploring the conversion of unstructured sports news into structured information.

## Limitations

- The dataset contains only five sports news articles.
- Player identification relies on spaCy's NER and proper noun extraction, which may not always identify the correct player associated with an event.
- Scoring and disciplinary event extraction uses keyword-based rules and may produce incomplete or inaccurate results.
- The current implementation is an exploratory NLP exercise rather than a fully automated sports event recognition system.

## Future Improvements

- Expand the dataset with more sports news articles.
- Improve player identification using dependency parsing.
- Develop more accurate scoring event extraction rules.
- Convert extracted events into structured datasets using Pandas.
- Explore machine learning approaches for automated sports event classification.
