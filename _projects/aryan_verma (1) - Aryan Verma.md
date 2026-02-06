---
layout: projects/projects-individual
title: "vid2kg: Recipe Curation from YouTube Videos"
advisor: "Ms. Lipika Dey"
students: "Aryan Verma, Avik Mittal"
abstract: "vid2kg is an end-to-end automated system for extracting structured recipe knowledge from multilingual Indian cooking videos on YouTube. The project converts unstructured, speech-driven video content into machine-readable formats suitable for knowledge graphs and downstream applications such as nutrition analysis, semantic recipe search, and cultural preservation."
categories: ["Natural Language Processing", "Knowledge Graphs"]
---

## Project Description

vid2kg (Video to Knowledge Graph) is a capstone project that addresses the challenge of extracting structured culinary knowledge from YouTube cooking videos, with a specific focus on Indian cuisine and multilingual content. A large proportion of traditional Indian recipes—especially those shared by rural or home-style creators—exist only in video form and are narrated informally in regional languages. These videos are unstructured, noisy, and often code-mixed, making them inaccessible to conventional recipe databases and food knowledge systems. The central objective of this project is to bridge this gap by transforming such unstructured video content into standardized, machine-readable recipe representations.

The system processes a YouTube video URL and outputs a structured JSON object containing recipe metadata such as title, cuisine, ingredients with quantities, preparation steps, cooking time, and difficulty level. vid2kg is designed as an offline-first, reproducible pipeline, where extracted audio is cached locally to avoid redundant downloads and ensure deterministic outputs across repeated runs. This design choice enables reliable evaluation and efficient experimentation.

Beyond technical feasibility, vid2kg demonstrates strong real-world relevance. The structured outputs produced by the system can be integrated into food knowledge graphs, enable semantic search across multilingual recipes, support automated nutrition analysis using Indian food databases, and contribute to the digital preservation of regional culinary knowledge. The pipeline was evaluated on 13 real-world cooking videos across multiple Indian languages and achieved high accuracy on ingredient extraction and step identification through both manual and automated validation.

## Methodology

The system follows a six-stage modular pipeline: (1) audio extraction and caching from YouTube videos using yt-dlp, (2) speech-to-text transcription with automatic language detection using Faster-Whisper, (3) translation of non-English transcripts into English while preserving code-mixed segments, (4) fuzzy matching–based error correction for ingredient names using RapidFuzz and a curated error dictionary, (5) large language model–based recipe extraction using Google Gemini Flash Lite with strict JSON output constraints, and (6) unit normalization that converts vague or region-specific measurements into standardized metric units using rule-based and context-aware estimation.

## Key Outcomes

The project achieved a 100% pipeline success rate across 13 multilingual videos. Manual evaluation on a representative Dal Fry video demonstrated approximately 90% accuracy on core recipe elements. The system showed robust multilingual support, effective reduction of transcription errors by 60–80%, and stable structured extraction suitable for downstream knowledge graph integration and future extensions.
