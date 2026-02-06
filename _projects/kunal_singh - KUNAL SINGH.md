---
layout: projects/projects-individual
title: "Bias Detection in Book Reviews: Understanding LLM-Based Bias Detection and Finding Objective Reviews"
advisor: "Prof. Lipika Dey"
students: "Kunal Singh, Kenisha Chandak"
abstract: "This project investigates seven types of biases—gender, genre, rating, author, popularity, and cultural—in book reviews across multiple datasets using an ensemble of local LLMs (LLaMA, Mistral, Phi, Qwen, and Gemma). The project begins with data collection through web scraping and aims to understand how LLM-based bias detection can surface objective reviews and support fairer recommendation systems."
categories: ["Machine Learning", "Natural Language Processing"]
---

## Project Description

This capstone project explores the presence and detection of bias in book reviews, with a particular emphasis on Indian literature and how biased user-generated content can distort recommendation systems. Reviews on platforms such as Goodreads significantly influence what books are surfaced to readers, yet they often contain subjective judgments shaped by genre stereotypes, cultural misunderstandings, personal preferences, and preconceived notions about authors. These biases, when aggregated, can propagate into algorithmic pipelines and undermine the fairness and reliability of recommendations.

The project addresses this problem using a multi-model Large Language Model (LLM) ensemble designed to identify seven types of bias: cultural, gender, confirmation, genre, rating, recency, and writing/author bias. A multi-step pipeline was developed that includes web scraping data from Goodreads, conducting structured data cleaning, creating engineered features, and preparing four distinct datasets—ranging from curated Indian literature to large-scale Western-dominant corpora. Each dataset enables analysis of how bias manifests differently across cultural contexts.

Prompt engineering played a crucial role, as multiple prompting strategies were designed and evaluated to test how instruction detail influences LLM outputs. Results showed that models exhibit variability and prompt sensitivity, with some models aggressively over-detecting bias while others remain conservative. To address this, a weighted voting ensemble was introduced, incorporating internal consistency checks and model-specific weighting to produce stable, validated bias classifications.

In addition, the project includes manual annotation of a subset of reviews to evaluate the accuracy of LLM predictions, revealing complementary strengths across models and justifying the ensemble approach. Key findings demonstrate that genre and rating biases are most commonly detected, while cultural and confirmation biases emerge more prominently in Indian literature datasets. Recency bias remains particularly difficult for LLMs to detect across all models.

Ultimately, the project contributes a full LLM-based evaluation framework, insights into prompt–model interactions, and recommendations for integrating bias detection into real-world review platforms and recommendation systems.

## Objectives

- Detect multiple forms of bias in book reviews using open-source LLMs.
- Build a structured multi-dataset evaluation pipeline for bias analysis.
- Develop and test multiple prompting strategies for consistent bias detection.
- Construct a weighted ensemble voting system to increase robustness.
- Conduct manual annotation to validate model performance.

## Methodology

- Web-scraping Goodreads book reviews focused on Indian literature and global datasets.
- Cleaning, preprocessing, and feature engineering to develop review datasets.
- Detailed prompt engineering across four prompt templates.
- Evaluation of multiple open-source LLMs (Mistral, Phi, Qwen, Gemma).
- Weighted ensemble voting combining per-run and per-model consistency.
- Ground-truth validation through manual annotation and F1-score analysis.

## Results

- Genre and rating biases were the most consistently detected across datasets.
- Cultural and confirmation biases appeared more prominently in Indian datasets.
- Recency bias showed near-zero true positives across all LLMs.
- Weighted ensemble significantly improved reliability over single-model outputs.
- Prompt detail strongly influenced detection behavior and stability.

## Conclusion

This project demonstrates that while LLMs show strong potential for bias detection in literary reviews, their performance varies widely depending on prompt design, dataset characteristics, and model architecture. A voting-based ensemble approach offers improved stability and accuracy, making LLM-driven bias detection a promising tool for enhancing fairness in recommendation systems.

