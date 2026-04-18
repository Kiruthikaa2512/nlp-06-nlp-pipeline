# NLP Portfolio: Web Mining and Applied NLP

**Author:** Kiruthikaa
**Date:** April 2026

## Overview

This portfolio shows the work I completed in Web Mining and Applied NLP during this course. Across the modules, I worked with text preprocessing, corpus exploration, APIs, web documents, and full NLP pipelines. My strongest project was Module 6, where I customized an EVTAL pipeline to analyze a different arXiv research paper by changing the source URL and creating my own config, validate, transform, and analyze files.

Through these projects, I learned how to collect text data from websites, clean and process text using Python, create useful outputs like charts and CSV files, and organize everything into a repeatable pipeline.

---

## 1. NLP Techniques Implemented

During this course, I used several NLP techniques across different projects.

- **Tokenization:** Split text into words or tokens for analysis.
- **Text Cleaning:** Converted text to lowercase, removed punctuation, extra spaces, and common stopwords.
- **Frequency Analysis:** Counted the most common words using `Counter()` and displayed results in charts.
- **N-grams / Bigrams:** Explored common word pairs to identify phrase patterns.
- **Web Scraping / HTML Extraction:** Used BeautifulSoup to collect text and metadata from web pages.
- **API Text Analysis:** Worked with JSON data and converted it into structured tables.
- **Feature Engineering:** Created columns such as token count, unique token count, and type-token ratio.
- **Visualization:** Generated outputs such as top token bar charts and word clouds.
- **Pipeline Design:** Used EVTAL stages (Extract, Validate, Transform, Analyze, Load) to organize workflows.

In Module 6, I also modified the analyze stage by reducing the top token chart from 20 words to 10 words, which made the chart easier to read.

---

## 2. Systems and Data Sources

I worked with different types of text data during this course.

- **HTML Web Pages:** Used website pages and arXiv research paper pages as data sources.
- **JSON API Data:** Worked with structured API data in earlier modules.
- **Plain Text Files:** Used text corpora for preprocessing, tokenization, and frequency analysis.

For my Module 6 project, I changed the source URL to a different arXiv research paper and used the pipeline to extract information such as the title, abstract, and other text fields.

Some data sources were clean and structured, while others needed extra cleaning. I handled messy data by checking the page structure, removing unwanted symbols, cleaning text, and making sure the correct fields were extracted before analysis.

---

## 3. Pipeline Structure (EVTAL)

My projects followed the EVTAL workflow.

### Extract
Collected raw data from websites or APIs using Python requests.

**Example files:**
- `stage01_extract.py`
- `pipeline_web_html_kiruthikaa_project.py`

### Validate
Checked that the required fields, tags, or content existed before processing.

**Example file:**
- `stage02_validate_kiruthikaa.py`

### Transform
Cleaned text, tokenized content, and created useful derived columns.

**Example file:**
- `stage03_transform_kiruthikaa.py`

### Analyze
Created charts, token frequency summaries, and text insights.

**Example file:**
- `stage04_analyze_kiruthikaa.py`

### Load
Saved final outputs such as processed CSV files and charts for reuse.

This structure made the projects easier to debug, reuse, and improve.

---

## 4. Signals and Analysis Methods

I computed several useful signals from text data.

- **Word Frequency:** Identified the most common words in documents.
- **Bigrams / Context:** Found common word pairs and nearby word relationships.
- **Token Counts:** Measured total and unique words.
- **Type-Token Ratio:** Used to estimate vocabulary variety.
- **Metadata Signals:** Used titles, dates, and other extracted fields.
- **Visual Signals:** Used bar charts and word clouds to quickly see patterns.

In Module 6, reducing the chart to top 10 tokens helped remove clutter and made the results easier to understand.

---

## 5. Insights

My projects revealed several useful insights.

- Cleaning text greatly improves analysis results.
- Small changes in visualization can make results clearer.
- Different sources require different handling (HTML vs JSON vs text files).
- Pipelines are reusable when files are organized well.
- The arXiv project showed that academic abstracts often contain repeated topic-specific terms.

From my custom Module 6 project, terms such as **metabolic**, **cells**, **volume**, and **rate** appeared often, showing the main research focus of the paper.

One of my biggest lessons was that checking imports and file names carefully matters, because the pipeline may run default files if custom files are not linked correctly.

---

## 6. Representative Work

### Project 1: Module 6 Custom NLP Pipeline

Link: https://github.com/Kiruthikaa2512/nlp-06-nlp-pipeline

This was my strongest project. I customized the original pipeline files, changed the arXiv paper source, updated chart outputs, and successfully ran my own EVTAL pipeline.

Custom files used:

- config_kiruthikaa.py
- pipeline_web_html_kiruthikaa_project.py
- stage02_validate_kiruthikaa.py
- stage03_transform_kiruthikaa.py
- stage04_analyze_kiruthikaa.py

### Project 2: Module 5 Web Documents Pipeline

Link: https://github.com/Kiruthikaa2512/nlp-05-web-documents

This project focused on extracting and processing text from HTML web pages. It helped me learn how website structures differ and how validation and transformation stages must be adjusted for new sources.

### Project 3: Module 4 API Text Data

Link: https://github.com/Kiruthikaa2512/nlp-04-api-text-data

This project used API JSON data and converted it into structured data for analysis. It helped me understand schemas, structured data, and handling different input formats.

### Project 4: Module 3 Text Exploration

Link: https://github.com/Kiruthikaa2512/nlp-03-text-exploration

This project focused on tokenization, frequency analysis, bigrams, and word relationships. It gave me the foundation for later NLP projects.

---

## 7. Skills

Through these projects, I developed the following skills:

- Python data processing
- Text cleaning and preprocessing
- Tokenization and frequency analysis
- Working with HTML web pages
- Working with JSON APIs
- Web scraping using BeautifulSoup
- Building repeatable EVTAL pipelines
- Handling messy or inconsistent data
- Creating charts and visual summaries
- Debugging file paths and imports
- Organizing projects with GitHub
- Communicating technical results in Markdown

---

## Conclusion

This course helped me understand how raw text data can be turned into structured information and useful insights. Across multiple modules, I learned both foundational NLP skills and practical pipeline design.

My Module 6 customized pipeline was the best example of this growth because it combined extraction, validation, transformation, analysis, and improved presentation into one complete project.
