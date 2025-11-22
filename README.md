
# News Research Tool Using LangChain and OpenAI LLM 

This is a user-friendly news research tool designed for effortless information retrieval. Users can input article URLs and ask questions to receive relevant insights from the stock market and financial domain.

![](dashboard.jpg)

## Features

- Load URLs or upload text files containing URLs to fetch article content.
- Process article content through LangChain's UnstructuredURL Loader
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (OpenAI) by inputting queries and receiving answers along with source URLs.


## Installation

1.Clone this repository to your local machine using:

```bash
  https://github.com/Supriya07-bit/news-research-tool.git
```
2.Create conda virtual env

```bash
  conda env create -f environment.yaml -p ./.venv
```

3.Download NLTK data packages

```bash
  import nltk
```
```bash
  nltk.download('all')
```

4.Set up your OpenAI API key by creating a .env file in the project root (Generate API key [here](https://platform.openai.com/api-keys))

```bash
  OPENAI_API_KEY='your_api_key_here'
```
## Usage/Examples

1. Run the Streamlit app by executing:
```bash
  streamlit run main.py
```

2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles
- Below are the example news articles
  - https://www.moneycontrol.com/news/business/tata-motors-mahindra-gain-certificates-for-production-linked-payouts-11281691.html
  - https://www.moneycontrol.com/news/business/tata-motors-launches-punch-icng-price-starts-at-rs-7-1-lakh-11098751.html
  - https://www.moneycontrol.com/news/business/stocks/buy-tata-motors-target-of-rs-743-kr-choksey-11080811.html

