Job Advertisement Preprocessing and Analysis

This project demonstrates the preprocessing and analysis of job advertisements using Python, including tokenization, stopword removal, frequency-based filtering, vocabulary creation, and representation generation using Bag-of-Words and pre-trained word embeddings.

Project Structure

Setup

Installs necessary packages like spacy and downloads the English language model.

Handles file uploads and extracts job advertisements from a ZIP archive.

Preprocessing

Text Tokenization: Extracts words using regular expressions, converts them to lowercase, and removes short words.

Stopword Removal: Removes common stopwords using a predefined list.

Frequency Filtering: Removes low-frequency and high-frequency words.

Vocabulary Building

Constructs a vocabulary from the preprocessed tokens and saves it to a file.

Feature Representation

Generates Bag-of-Words vectors for each job description.

Saves count vectors to a file.

Word Embeddings

Loads pre-trained GloVe word embeddings.

Computes unweighted vector representations for job descriptions using GloVe embeddings.

Prerequisites

Libraries

Python 3.x

spacy

pandas

numpy

External Files

Job advertisements in text format within a ZIP file.

Stopword list (stopwords_en.txt).

Pre-trained GloVe embeddings (glove.6B.zip).

Tools

Google Colab (preferred for running the notebook).

Usage Instructions

1. Setup Environment

Install Required Libraries

!pip install -U pip setuptools wheel
!pip install -U spacy
!python -m spacy download en_core_web_sm

Upload Job Ads
Use the Colab file upload interface to upload the ZIP file containing job advertisements.

Extract Job Ads
Uploaded files are extracted to /content/data.

2. Preprocessing

Tokenization

Extract words using regex patterns.

Convert to lowercase.

Filter words with length > 1.

Stopword Removal

Load stopwords from stopwords_en.txt.

Remove stopwords from tokens.

Frequency Filtering

Remove low-frequency and high-frequency words.

Exclude the top 50 most frequent words.

3. Vocabulary Creation

Build a sorted vocabulary from filtered tokens.

Save vocabulary to vocab.txt.

4. Feature Representation

Bag-of-Words (BoW)

Represent job ads as count vectors using the vocabulary.

Save count vectors to count_vectors.txt.

Word Embeddings

Load pre-trained GloVe embeddings.

Compute unweighted word vector representations for job ads.

5. Save Results

Save preprocessed job ads to preprocessed_job_ads.csv.

Save vocabulary and count vectors for further analysis.

Output Files

Preprocessed Job Ads: preprocessed_job_ads.csv

Vocabulary: vocab.txt

Count Vectors: count_vectors.txt

Notes

Ensure the directory structure is consistent when running the script.

Modify file paths if running locally instead of Google Colab.

For GloVe embeddings, download the appropriate dimensions as needed (e.g., 50d, 100d, 300d).

Future Improvements

Add support for more advanced text preprocessing techniques (e.g., lemmatization).

Explore additional feature representations like TF-IDF.

Extend compatibility to handle various file formats (e.g., PDF, DOCX).

Integrate clustering or classification methods for job ad analysis.

Contact

For further assistance, please reach out to email:tahseenislamian900@gmail.com