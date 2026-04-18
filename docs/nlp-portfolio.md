# NLP Portfolio: Web Mining and Applied NLP

**Author:** Kiruthikaa NS
**Date:** 18th April, 2026

## Overview

This portfolio shows the work I completed in Web Mining and Applied NLP during this course. Across the modules, I worked with text preprocessing, corpus exploration, API data, web documents, and full NLP pipelines. My strongest project was Module 6, where I customized an EVTAL pipeline to analyze a different arXiv research paper by changing the source URL and creating my own config, validate, transform, analyze, and pipeline files.

Through these projects, I learned how to collect data from APIs and websites, clean and process text using Python, create useful outputs like charts and CSV files, and organize everything into a repeatable workflow. One of the biggest takeaways for me was seeing how small changes in one stage of a pipeline can improve the final results.

---

## 1. NLP Techniques Implemented

During this course, I used several NLP techniques across different projects.

- **Tokenization:** Split text into words or tokens for analysis.
- **Text Cleaning:** Converted text to lowercase, removed punctuation, extra spaces, and common stopwords.
- **Frequency Analysis:** Counted common words using `Counter()` and displayed results in charts.
- **N-grams / Bigrams:** Explored common word pairs to identify phrase patterns.
- **Web Scraping / HTML Extraction:** Used BeautifulSoup to collect titles, abstracts, and metadata from web pages.
- **API Text Analysis:** Worked with JSON API data and converted it into structured tables.
- **Feature Engineering:** Added derived columns such as `word_count`, `title_word_count`, `token_count`, and `type_token_ratio`.
- **Visualization:** Generated top token bar charts and word clouds.
- **Pipeline Design:** Used EVTL / EVTAL stages (Extract, Validate, Transform, Analyze, Load).

In Module 6, I modified the analyze stage by reducing the top token chart from 20 words to 10 words, which made the output cleaner and easier to read.

---

## 2. Systems and Data Sources

I worked with different types of text data during this course.

- **HTML Web Pages:** Used arXiv research paper pages and other websites.
- **JSON API Data:** Used structured API responses in Module 4.
- **Plain Text Files:** Used text corpora in earlier modules for preprocessing and exploration.

For Module 6, I changed the source URL to a different arXiv paper and used the pipeline to extract the title, abstract, and other metadata fields.

For Module 5, I tested the pipeline on the **GPT-4 Technical Report** from arXiv and confirmed the pipeline still worked correctly with a new source.

Some data sources were clean and structured, while others needed extra checks. I handled messy data by validating required fields, checking HTML structure, removing unwanted symbols, and making sure the correct values were extracted before analysis.

---

## 3. Pipeline Structure (EVTAL)

My projects followed a staged workflow.

### Extract
Collected raw data from websites or APIs using Python requests.

**Examples:**
- `stage01_extract.py`
- `pipeline_web_html_kiruthikaa_project.py`
- `pipeline_api_json.py`

### Validate
Checked whether required keys, tags, and content were available before processing.

**Examples:**
- `stage02_validate_kiruthikaa.py`

In Module 4, I added required-key checks for:

- `userId`
- `id`
- `title`
- `body`

In Module 5, I added a validation check to confirm the abstract text length was sufficient.

### Transform
Cleaned text and created new derived fields.

**Examples:**
- `stage03_transform_kiruthikaa.py`

Fields I added across projects:

- `word_count`
- `title_word_count`
- `token_count`
- `unique_token_count`

### Analyze
Created charts, token summaries, and observed patterns.

**Examples:**
- `stage04_analyze_kiruthikaa.py`

### Load
Saved outputs such as CSV files, raw files, and charts for future use.

This workflow helped me understand how each stage connects to the next.

---

## 4. Signals and Analysis Methods

I computed several useful signals from text data.

- **Word Frequency:** Identified the most common words in documents.
- **Bigrams / Context:** Found common word pairs and nearby word relationships.
- **Token Counts:** Measured total and unique words.
- **Type-Token Ratio:** Used to estimate vocabulary variety.
- **Title Length:** Used `title_word_count` to compare paper titles.
- **Metadata Signals:** Used titles, dates, IDs, and author counts.
- **Visual Signals:** Used charts and word clouds to quickly see patterns.

In Module 6, reducing the token chart to top 10 words helped remove clutter and made the results easier to understand.

---

## 5. Insights

My projects revealed several useful insights.

- Cleaning text greatly improves analysis results.
- Small visualization changes can make outputs easier to understand.
- Different data sources need different handling (HTML vs JSON vs text files).
- Pipelines are reusable when files are organized well.
- Validation is important because it catches issues before transformation.

From my Module 6 project, terms such as **metabolic**, **cells**, **volume**, and **rate** appeared often, showing the main research focus of the selected paper.

From Module 5, my output dataset increased from **8 columns to 9 columns** after I added the `title_word_count` field.

When I tested the GPT-4 Technical Report, the pipeline extracted:

- arXiv ID: `2303.08774`
- title word count: `3`
- abstract word count: `132`
- author count: `282`

From Module 4, after my validation changes, the terminal confirmed that **100 API records were validated successfully**, and the transformed preview showed shape **(5, 8)** with added columns.
I also connected the Module 4 API pipeline concepts to my real work environment, where structured EDI payloads are exchanged through APIs and require validation before use.

One great lessons I learned was that if custom files are not linked correctly, the pipeline may still run the default files. I ran into that issue and had to debug imports and terminal sessions carefully, almost all the 3 weeks I had that issue and fixed them later.

---

## 6. Representative Work

### Project 1: Module 6 Custom NLP Pipeline

Link: https://github.com/Kiruthikaa2512/nlp-06-nlp-pipeline

This was my strongest project. I customized the original pipeline files, changed the arXiv paper source, updated chart outputs, and successfully ran my own EVTAL pipeline.

Custom files used:

- `config_kiruthikaa.py`
- `pipeline_web_html_kiruthikaa_project.py`
- `stage02_validate_kiruthikaa.py`
- `stage03_transform_kiruthikaa.py`
- `stage04_analyze_kiruthikaa.py`

Key changes:

- Reduced top token chart from 20 to 10
- Updated output filenames
- Added bold chart title
- Added custom log message

---

### Project 2: Module 5 Web Documents Pipeline

Link: https://github.com/Kiruthikaa2512/nlp-05-web-documents

In this project, I customized the validation and transformation stages for a different arXiv paper source. I added a new derived field called `title_word_count` and an extra validation check for abstract length.

My output changed from **8 columns to 9 columns** after adding the new field.

This project helped me understand how targeted changes can improve a pipeline without breaking the workflow.

---

### Project 3: Module 4 API Text Data

Link: https://github.com/Kiruthikaa2512/nlp-04-api-text-data

This project focused on API JSON data. I created my own config, validate, and transform files, updated the pipeline imports, and added new fields such as `word_count` and `title_word_count`.

I also added required-key validation and logging that confirmed **100 records were validated successfully**.

This project helped me understand how structured API data can be cleaned and prepared for analysis.

---

### Project 4: Module 3 Text Exploration

Link: https://github.com/Kiruthikaa2512/nlp-03-text-exploration

This project focused on tokenization, frequency analysis, bigrams, and word relationships. It gave me the foundation for later NLP and pipeline projects.

---

## 7. Skills

Through these projects, I developed the following skills:

- Python data processing
- Text cleaning and preprocessing
- Tokenization and frequency analysis
- Working with HTML web pages
- Working with JSON APIs
- Web scraping using BeautifulSoup
- Creating derived analytical fields
- Building repeatable EVTL / EVTAL pipelines
- Handling messy or inconsistent data
- Debugging file paths, imports, and workflow issues
- Creating charts and visual summaries
- Organizing projects with GitHub
- Communicating technical results in Markdown

---

## Conclusion

This course helped me understand how raw text data can be turned into structured information and useful insights. Across multiple modules, I learned both foundational NLP skills and practical pipeline design.

My Module 6 customized pipeline was the best example of this growth because it combined extraction, validation, transformation, analysis, and presentation into one complete project. More importantly, I learned that small thoughtful changes in each stage can create much better final results.
