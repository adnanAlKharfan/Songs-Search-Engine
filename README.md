# Songs Search Engine

A Python-based project for crawling song lyrics from the web and building a search engine to query song lyrics efficiently.


## Introduction

The Songs Search Engine is designed to scrape song lyrics from the web and create a searchable database. This allows users to search for lyrics and receive ranked results based on their queries.

## Features

- Web Crawling: Scrapes song lyrics from specified URLs.
  
- Search Engine: Uses TF-IDF vectorization and positional indexing to search and rank song lyrics.
  
- Lemmatization and Tokenization: Processes lyrics to improve search accuracy.

## Installation

To install the necessary dependencies, run:

```bash
pip install -r requirements.txt
```

## Usage

1. Crawling Lyrics: Use the lyrics web crawler.ipynb notebook to scrape song lyrics.

2. Building the Search Engine: Use the irs project.ipynb notebook to process the lyrics and build the search engine.

3. Querying Lyrics: Execute search queries within the irs project.ipynb to find lyrics.

### Example

1. Crawling Lyrics:
   
```python
from lyrics_crawler import Crawler
crawler = Crawler(["https://www.lyrics.com/lyric/24488857/Pink+Floyd/Wish+You+Were+Here"])
crawler.run(100)  # Crawls up to 100 lyrics pages
```

2. Building the Search Engine:

```python
from search_engine import buildPostionalIndex, querySearch
buildPostionalIndex()
results = querySearch("wish you were here")
print(results)
```

## Project Structure

- irs project.ipynb: Jupyter notebook for processing lyrics and building the search engine.

- lyrics web crawler.ipynb: Jupyter notebook for scraping song lyrics.

- lyrics.json: JSON file containing the scraped song lyrics.

- requirements.txt: Dependencies required for the project.


## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

