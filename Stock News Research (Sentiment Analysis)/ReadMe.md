# Stock News Research Project

## Project Overview

This project focuses on analyzing stock-related news articles to provide summarized insights into recent developments in the financial market. The aim is to use advanced natural language processing (NLP) techniques to extract relevant information from news articles about specific stock tickers, summarize the content, and assess the overall sentiment of these summaries.

## Technologies Used

- **NewsAPI**: For fetching news articles related to specific stock tickers.
- **Pegasus**: A state-of-the-art model for summarization, used here to condense news articles into meaningful summaries.
- **BeautifulSoup**: For parsing HTML content from news article URLs.
- **Requests**: For making HTTP requests to fetch article content.
- **Pandas**: For organizing and analyzing the results.

## Workflow

1. **Fetching Articles**: News articles related to monitored stock tickers are fetched using the NewsAPI.
2. **Article Extraction**: The content of each article is extracted using BeautifulSoup.
3. **Text Chunking**: Long articles are split into manageable chunks for summarization.
4. **Summarization**: Each chunk is summarized using the Pegasus model.
5. **Sentiment Analysis**: The sentiment of the summarized articles is assessed to understand the general sentiment towards each stock ticker.
6. **Results Compilation**: The summaries and sentiments are compiled into a DataFrame for analysis.

### Key Functions

- `fetch_article(url)`: Fetches and extracts text content from a given article URL.
- `split_text_into_chunks(text, max_chunk_size)`: Splits long text into smaller chunks suitable for summarization.
- `summarize_chunk(chunk, tokenizer, model)`: Summarizes a chunk of text using the Pegasus model.
- `summarize_article(url, tokenizer, model, max_chunk_size=500)`: Summarizes an entire article by fetching, chunking, and summarizing.
- `get_news_urls(ticker)`: Retrieves news article URLs and publication dates for a given stock ticker.

## Monitored Tickers

The following stock tickers are monitored for news articles:

- AMZN (Amazon)
- GOOGL (Google)
- META (Meta Platforms)
- NVDA (NVIDIA)
- BTC (Bitcoin)
- ETH (Ethereum)
- SPX (S&P 500)
- VOO (Vanguard 500 ETF)

## Results

The sentiment analysis of the summarized articles resulted in the following distribution:

- **Neutral**: 23 articles
- **Positive**: 14 articles
- **Negative**: 7 articles
