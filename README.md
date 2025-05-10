# MUCS-IberLEF2025

# Handcrafted Features Fusion with Multilingual Models for Hope Speech Detection in Spanish and English

This project involves text classification using machine learning techniques to detect hope speech in social media texts. It includes preprocessing, feature extraction, and classification of text data in both English and Spanish.

## Table of Contents
- [Description](#description)
- [Features](#features)
- [Installation](#installation)


## Description
Hope speech detection in social media texts is essential for fostering supportive online communities and amplifying positive and motivational content. However, identifying this content manually is cumbersome due to the ever-growing amount of user-generated social media text. Further, the characteristics of user-generated text, particularly when the information is subtle or masked by sarcasm, make it more challenging.

To address these challenges, PolyHope at IberLEF 2025 shared task organized at IberLEF 2025 invites the research community to develop efficient models to detect hope speech tweets in Spanish and English languages. The shared task consists of two subtasks:
1. Binary Hope Speech detection to classify the given tweet as 'Hope' and 'Not Hope'.
2. Multiclass Hope Speech detection to classify the given tweet as 'Generalized Hope', 'Realistic Hope', 'Unrealistic Hope', 'Sarcasm', or 'Not Hope', in Spanish and English.

In this project, we - team MUCS, describe the proposed multilingual models submitted to the shared task. Instead of developing separate models for each language, we merge the train sets of English and Spanish, and build multilingual models using an ensemble of Machine Learning (ML) classifiers (Logistic Regression (LR), Multinomial Naive Bayes (MNB), and Support Vector Machine (SVM)). Ensemble models are trained with a fusion of selected handcrafted features (Term Frequency-Inverse Document Frequency (TF-IDF) vectors of words, character ngrams, and subwords) and their predictions are combined using Hard and Soft voting.

The best results obtained by our proposed models are:
- Weighted precision of 0.80 and 0.78 (Hard voting), for Binary Hope Speech detection in Spanish and English, respectively.
- Weighted precision of 0.64 and 0.62 (Hard voting), for Multiclass Hope Speech detection in Spanish and English, respectively.

This research contributes to the development of inclusive language technologies, provides insights into the psychological and linguistic dimensions of hope, and supports the creation of more positive and resilient online environments.

## Features
- Text preprocessing including tokenization, lemmatization, and stemming.
- Feature extraction using TF-IDF for words, characters, and BPE tokenized texts.
- Classification using Logistic Regression, Naive Bayes, and SVM.
- Voting classifiers for improved prediction accuracy.

## Installation
To run this project, you need to have Python installed along with the following libraries:
- pandas
- numpy
- seaborn
- nltk
- contractions
- scikit-learn
- tokenizers
- emoji
- num2words

You can install these libraries using pip:

```bash
pip install pandas numpy seaborn nltk contractions scikit-learn tokenizers emoji num2words
