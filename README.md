# Text_Mining_-_Search

Amazon Fine Food Reviews: Text Mining & Latent Semantic Analysis
Text Mining Research Project | Master's Degree
This project processes over 500k consumer reviews to transform raw text into meaningful numerical representations. It compares Bag-of-Words (BoW) and TF-IDF vectorization techniques while evaluating dimensionality reduction via Truncated SVD.

## 1. Dataset Overview
The project utilizes the Amazon Fine Food Reviews dataset (Kaggle), spanning from 1999 to 2012.
Total Reviews: ~568,454
Core Features Utilized:
Time: Temporal analysis of reviews.
Score: Rating scale (1-5) used as a sentiment proxy.
Text: The raw corpus of consumer feedback.

## 2. Natural Language Preprocessing (NLP)
To clean the noise from consumer-generated content, a three-step normalization pipeline was implemented:

* Normalization: Converting text to lowercase and removing special characters/punctuation.

* Tokenization & Stop Word Removal: Segmenting sentences into individual words and filtering out common non-informative words (e.g., "the", "and").

* Stemming: Reducing words to their root form (e.g., "eating" and "eaten" to "eat") to reduce vocabulary size.

## 3. Text Representation & Dimensionality Reduction
The core of the research involves converting text into high-dimensional vectors and analyzing their variance.

* Vectorization Techniques: Bag of Words (BoW): Counting word frequencies to create a sparse matrix, TF-IDF (Term Frequency-Inverse Document Frequency): Weighting words by their importance and rarity across the corpus to better capture semantic significance.
*Latent Semantic Analysis (LSA)
* To handle the "curse of dimensionality," we employed Truncated SVD (Singular Value Decomposition). This allows us to:

Identify latent patterns (topics) within the reviews.

Analyze the Explained Variance to determine how many components are required to capture the majority of the information in the dataset.

## 4. Technical Stack
Environment: Google Colab (GPU/TPU acceleration for SVD computation).

Libraries: NLTK (Preprocessing), Scikit-Learn (Vectorization, Truncated SVD), Pandas, Matplotlib.
