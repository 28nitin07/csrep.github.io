---
layout: projects/projects-individual
title: "From Structured ICU Data to Discharge-Style Narratives: A Modular, View-Wise LLM Framework"
advisor: "Dr. Lipika Dey, Dr. Mayank Garg"
students: "Himangi Parekh, Soham Shah"
abstract: "Electronic health records (EHRs) contain rich information about a patient’s intensive care unit (ICU) course, but this information is spread across multiple structured tables and is difficult to interpret quickly. This project investigates whether large language models (LLMs) can generate discharge-style ICU summaries directly from structured EHR data, without access to original clinical notes. We propose a modular, view-wise framework that transforms MIMIC-IV ICU data into coherent narrative summaries through structured aggregation, linearisation, and controlled prompt-based summarisation. The framework is evaluated using both quantitative and qualitative metrics, revealing model-specific trade-offs between conciseness, coverage, and clinical faithfulness."
categories: ["Natural Language Processing", "Healthcare AI"]
---

## Project Description

Electronic health records (EHRs) capture detailed, high-frequency clinical data across the course of a patient’s hospital stay, particularly in intensive care units (ICUs). While these structured data streams—such as laboratory results, medication administrations, physiological measurements, procedures, and outputs—are comprehensive, they are fragmented across multiple relational tables and lack narrative form. Clinicians must manually integrate this information into discharge summaries, a process that is time-consuming, cognitively demanding, and prone to inconsistency. This project explores whether large language models (LLMs) can reliably generate discharge-style ICU summaries using structured EHR data alone, without relying on clinician-authored notes.

The project proposes a modular, view-wise summarisation framework built on the MIMIC-IV ICU database. Raw structured tables are first cleaned and reorganised into patient-centric ICU episodes anchored around stay identifiers. These episodes are then decomposed into clinically meaningful “views,” including admissions, diagnoses and procedures, laboratory tests, medications, physiological measurements, and outputs. Each view is aggregated and linearised into compact textual blocks that preserve factual grounding while remaining interpretable to language models.

Summarisation is performed in stages using view-specific prompts followed by a global synthesis prompt, allowing fine-grained control over model behaviour and reducing the risk of hallucination. Two contrasting models—FLAN-T5, a general-purpose instruction-tuned model, and Meditron-7B, a clinically specialised biomedical model—are evaluated on a curated cohort of 250 ICU stays. Outputs are compared against clinician-authored discharge summaries using BERTScore precision, embedding similarity, medical term density, stylistic measures, and qualitative assessment of faithfulness, coherence, and safety.

The results demonstrate that structured ICU data alone can support the generation of clinically flavoured narratives, while also highlighting important trade-offs between conciseness, coverage, and verbosity across models. The project contributes a reproducible architecture, a task-specific evaluation framework, and a critical analysis of the current limitations of LLM-based clinical summarisation.

## Methodology

The methodology follows a multi-stage pipeline: (i) data cleaning and cohort construction from MIMIC-IV, (ii) episode building by linking key ICU tables, (iii) view-level aggregation across major clinical domains, (iv) linearisation of structured data into text blocks, and (v) controlled summarisation using view-specific and global prompts. Two LLMs are deployed within this pipeline to compare general-purpose and clinical domain-adapted behaviour.

## Results and Contributions

The framework achieves high lexical alignment with reference discharge summaries (BERTScore ≈ 0.8) and produces realistic sentence structure and medical terminology. FLAN-T5 generates concise, well-grounded summaries but omits some information, while Meditron-7B provides broader coverage with increased verbosity and occasional speculative detail. Key contributions include a schema-agnostic summarisation architecture, a multi-dimensional evaluation strategy, and empirical insights into model-specific trade-offs in structured-data clinical summarisation.
