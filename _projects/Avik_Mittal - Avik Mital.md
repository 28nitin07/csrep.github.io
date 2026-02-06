---
layout: projects/projects-individual
title: "vid2kg: Recipe Curation from YouTube Videos"
advisor: "Ms. Lipika Dey"
students: "Aryan Verma, Avik Mittal"
abstract: "vid2kg is an end-to-end automated system that extracts structured recipe information from unstructured, multilingual Indian cooking videos on YouTube. The project focuses on converting informal spoken recipes into machine-readable formats suitable for food knowledge graphs, search, and downstream analytics."
categories: ["Machine Learning", "Natural Language Processing"]
---

## Project Description

vid2kg (Video to Knowledge Graph) is a capstone project that addresses the growing challenge of extracting structured knowledge from unstructured video content, with a specific focus on Indian cooking videos available on YouTube. While traditional recipes are often documented in text-based formats, a vast and culturally rich corpus of culinary knowledge exists exclusively in video form—particularly from rural and regional Indian creators. These videos are multilingual, informal, and often recorded in noisy environments, making them difficult to process using conventional natural language processing techniques.

The primary objective of vid2kg is to transform these videos into structured, machine-readable recipe representations that can be integrated into food knowledge graphs and other downstream systems. The project implements a robust, offline-first pipeline that begins with audio extraction from YouTube videos and progresses through speech-to-text transcription, translation to English, transcription error correction, large language model (LLM)–based recipe extraction, and unit normalization. Each stage produces intermediate artifacts to ensure transparency, reproducibility, and ease of debugging.

A key contribution of the project lies in its handling of multilingual and noisy data. Indian cooking videos frequently involve code-mixing (such as Hinglish or Tanglish), strong regional accents, and vague measurements like “pinch” or “handful.” vid2kg addresses these challenges using a combination of fuzzy string matching, domain-specific error dictionaries, and LLM-driven reasoning. The system was evaluated using both automatic metrics and manual human evaluation, including a detailed case study on a Dal Fry recipe. Results demonstrate that vid2kg can achieve high accuracy in ingredient and step extraction while maintaining robustness across multiple Indian languages.

## Motivation

A large portion of traditional Indian culinary knowledge is shared orally through video platforms rather than written recipes. This makes such knowledge difficult to search, analyze, preserve, or integrate with modern food-tech applications such as nutrition analysis, meal planning, and recommendation systems. Existing recipe extraction tools are largely English-centric and designed for clean, text-based inputs, leaving a significant gap for multilingual video content. vid2kg was motivated by the need to bridge this gap and enable structured access to culturally important culinary data.

## Methodology

The system follows a six-stage modular pipeline: audio extraction using yt-dlp with caching, multilingual speech-to-text transcription using Faster-Whisper, translation to English via Google Translate, fuzzy matching–based error correction, LLM-powered recipe extraction using Google Gemini Flash Lite, and unit normalization to metric standards. The pipeline is orchestrated through a command-line interface and designed to be reproducible and extensible.

## Results and Contributions

vid2kg successfully processed a dataset of Indian cooking videos across multiple languages, achieving significant reductions in transcription errors and producing consistent structured recipe outputs. The project demonstrates the feasibility of combining traditional NLP techniques with modern LLMs for knowledge extraction from informal spoken content.

## Future Work

Future extensions include direct export to food knowledge graph formats, integration with nutrition databases, support for multi-speaker videos, and incorporation of visual cues from video frames to enhance extraction accuracy.
