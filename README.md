# Agentic-AI-Crawler

Agentic AI Crawler is a smart web crawler that recursively extracts, summarizes, classifies, and embeds website content using Google's Gemini AI models.
It builds a structured tree of the website and enables semantic search using FAISS, allowing users to search meaningfully based on page content rather than keywords.

**Features**
->Dynamic web crawling with depth control

->Summarization of web page content using Gemini models

->Classification of pages (e.g., blog, product, login page)

->Semantic search through FAISS and Gemini embeddings

->Tree visualization of the website structure using Graphviz

->Support for analyzing screenshot-based pages using Gemini Vision API

->Streamlit UI for easy interaction

**Project Structure**
.
├── app.py               # Streamlit frontend application
├── crawler.py           # Crawling logic for extracting URLs and page content
├── summarizer.py        # Functions for summarization and content embeddings
├── search.py            # FAISS indexing and semantic search functionality
├── gemini_vision.py     # Analyze images/screenshots of web pages
├── utils.py             # Utility functions
├── requirements.txt     # List of dependencies
└── README.md            # Project documentation


**Tech Stack**

->Python
->Streamlit (for UI)
->Google Gemini API (text summarization, classification, embedding)
->FAISS (for semantic search)
->BeautifulSoup and Requests (for HTML parsing)
->Selenium (for handling dynamic websites and taking screenshots)
->Graphviz (for website tree visualization)


**How It Works**
1)The crawler extracts links starting from a given URL.

2)For each page, it generates a content summary and classifies the page type using Gemini.

3)It builds embeddings for each page using the Gemini embedding model.

4)All embeddings are stored in a FAISS index for fast semantic search.

5)Users can search for any query, and the crawler returns the most relevant pages based on meaning, not just keywords.

6)The website structure is visualized in a tree format for better understanding.
