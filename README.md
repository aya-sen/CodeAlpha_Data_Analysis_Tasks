# CodeAlpha Data Analysis Tasks

This repository contains my data analytics submissions for the **CodeAlpha Internship**. Each project is organized programmatically into its respective task directory containing localized source files, datasets, and execution notes.

---

## 📁 Repository Structure

```text
CodeAlpha_Data_Analysis_Tasks/
│
├── .gitignore                      # Global git exclusions
├── README.md                       # Main repository documentation
│
└── Task 1 _ WEB SCRAPING/          # Task 1 Production Folder
    ├── main_scraper.ipynb          # Step-by-step Jupyter Notebook 
    ├── requirements.txt            # Python environment dependencies
    └── data/                       # Local structured data storage
        └── books.csv               # Extracted dataset (1,000 items)

```

---

## 🚀 Task 1: Programmatic Web Scraping Automation

### 📋 Project Overview

The objective of this task was to design and implement a custom web scraper that programmatically navigates through a multi-page web directory to compile a structured custom dataset.

Instead of extracting an isolated category with low data volume, the architecture was engineered to systematically loop through the entire catalog of an online bookstore to fetch **1,000 distinct items** across **50 consecutive web pages**—perfect for downstream analytics, predictive pricing models, or inventory data warehousing.

### 🛠️ Technical Stack & Frameworks

* **Python**: Core programming language.
* **Requests**: Executed programmatic HTTP client requests with explicit `utf-8` stream decoding to handle raw text symbols smoothly.
* **BeautifulSoup4**: Parsed and walked the complex nested HTML Document Object Model (DOM).
* **Pandas**: Structured raw dictionary matrices into an optimized, tabular Data Science format.
* **Time**: Managed throttling (1-second delay pauses) to respect server rate-limiting policies.

### 📊 Features Extracted

For every book entry captured, the scraper cleans and structures:

* **Title**: Full descriptive book name.
* **Price**: Cleaned decimal float value (currency signs programmatically removed).
* **Availability**: Real-time stock status flags.
* **Star Ratings**: Ordinal classification string extracted directly from the tag's layout classes.

---

## ⚡ Setup & Local Installation

To reproduce the data extraction locally, run the following commands in your terminal:

1. **Navigate to the Task folder:**
```
cd "Task 1 _ WEB SCRAPING"

```
2. **Install the required packages:**
```
pip install -r requirements.txt

```
3. **Execute the Notebook:**
Open `main_scraper.ipynb` using Jupyter or VS Code and run all cells sequentially to regenerate `data/books.csv`.

```

