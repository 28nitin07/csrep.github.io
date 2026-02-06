---
layout: projects/projects-individual
title: "From Structured ICU Data to Discharge-Style Narratives: A Modular, View-Wise LLM Framework"
advisor: "Dr. Lipika Dey & Dr. Mayank Garg     Department of Computer Science Ashoka University    Monsoon 2025"
students: "Himangi Parekh, Soham Shah  Advisors"
abstract: "Electronic health records (EHRs) contain rich information about a patient’s intensive care unit (ICU) course, but this information is spread across multiple structured tables and is difficult to interpret quickly. This thesis investigates whether large language models (LLMs) can generate discharge-style ICU summaries directly from structured EHR data, without access to the original clinical notes. I propose a modular, view-wise framework that transforms the MIMIC-IV ICU database into narrative summaries through a sequence of stages: (i) data cleaning and ICU cohort construction around stay identifiers; (ii) episode building that links key tables; (iii) view-level aggregation for major clinical domains (admissions, diagnoses and procedures, laboratory tests, medications, measurements, and outputs); (iv) linearisation of each view into compact textual “blocks”; and (v) view-specific and global prompts that drive LLM summarisation. Two models—a general-purpose instruction-tuned model (FLAN-T5) and a clinically specialised model (Meditron-7B)—are embedded into this pipeline and applied to a curated cohort of 250 ICU stays. Evaluation compares model summaries with clinician-authored discharge notes using BERTScore precision, document-level embedding similarity, average sentence length, and medical term density, complemented by qualitative assessment of coverage, faithfulness, coherence, conciseness, directional interpretation, and hallucination. The best version of the pipeline achieves high lexical alignment (BERTScore ≈ 0.8), realistic sentence structure, and improved medical term density across several views, demonstrating that structured data alone can support coherent, clinically flavoured narratives. The results reveal a consistent trade-off: FLAN-T5 produces concise, comparatively well-grounded summaries but omits non-trivial amounts of available information, whereas Meditron-7B offers broader coverage and richer clinical vocabulary at the cost of greater verbosity and occasional speculative elaboration. The thesis contributes (i) a detailed, schema-agnostic architecture for structured-data ICU summarisation, (ii) a multi-dimensional evaluation framework tailored to this task, and (iii) a critical analysis of model-specific trade-offs that delineates what is currently achievable—and what remains unsafe—when using LLMs to transform structured ICU data into discharge-style narratives."
categories: ["Healthcare", "Natural Language Processing"]
---

This capstone explores whether large language models (LLMs) can generate discharge-style ICU summaries directly from structured electronic health record (EHR) tables in the MIMIC-IV ICU database, without using the original clinician notes. It proposes a modular, view-wise pipeline that converts heterogeneous tables into clinically interpretable “views”, linearises each view into compact text blocks, and uses view-specific and global prompts to produce a coherent narrative summary.

## Project Description

Electronic health records store a patient’s ICU course across many structured tables—labs, medications, vitals, procedures, outputs, and administrative data. While these tables are detailed, they are hard to interpret quickly because clinically relevant context is fragmented across many sources and time granularities. This project asks a focused question: **can we generate discharge-style ICU narratives using only structured EHR data**, without access to the original clinical notes?

To answer this, the project develops a **modular, view-wise framework** for transforming the MIMIC-IV ICU database into narrative summaries. The pipeline begins by cleaning and restructuring raw tables around ICU stay identifiers, then builds a stay-level “episode” that links key domains. Next, it aggregates each domain into a clinically meaningful view (e.g., admissions context; diagnoses & procedures; laboratories; medications; measurements/vitals; and outputs). Each view is **linearised into a compact text block** with stable semantics, forming a clear interface between database engineering and language-model prompting. Using **view-specific prompts** followed by a **global synthesis prompt**, the system generates a discharge-style document that resembles the structure and tone of clinician-authored ICU summaries.

Two LLMs are evaluated within the same framework: **FLAN-T5** (a general-purpose instruction-tuned model) and **Meditron-7B** (a clinically specialised model). Experiments are run on a curated cohort of **250 ICU stays**, and model outputs are compared to clinician-authored discharge notes using a mix of quantitative and qualitative measures. Quantitatively, the evaluation includes **BERTScore precision**, document embedding similarity, average sentence length, and medical term density. Qualitatively, the summaries are assessed for coverage, faithfulness, coherence, conciseness, directional interpretation, and hallucination. The strongest pipeline version achieves **high lexical alignment (BERTScore ≈ 0.8)** and produces stylistically realistic narratives, demonstrating that structured data alone can support coherent, clinically flavoured ICU summaries. At the same time, the project highlights a central trade-off: FLAN-T5 tends to be concise and comparatively well-grounded but can omit important information, while Meditron-7B provides broader coverage and richer clinical vocabulary at the cost of verbosity and occasional speculative elaboration.

## Objectives

- Design an end-to-end, modular pipeline that converts structured MIMIC-IV ICU data into discharge-style narrative summaries.
- Compare a general instruction-tuned model (FLAN-T5) with a clinically specialised model (Meditron-7B) under identical inputs and prompts.
- Develop a multi-dimensional evaluation approach (quantitative + qualitative) tailored to structured-data ICU summarisation.
- Characterise model-specific trade-offs and failure modes relevant to clinical safety (omissions vs. hallucination/speculation).

## Methodology / Approach

- **Data preparation & cohort construction:** Clean and standardise key MIMIC-IV ICU tables; construct ICU cohorts around stay identifiers; curate a working cohort of 250 stays.
- **Episode building:** Link relevant tables into a stay-level episode representation spanning major clinical domains.
- **View-wise aggregation:** Aggregate each domain into concise, clinically interpretable summaries (e.g., medians/ranges for labs and measurements; spans/quantities for medications).
- **Linearisation:** Convert each view into a compact textual block with stable semantics to serve as the LLM input interface.
- **Prompting strategy:** Use view-specific prompts to generate section-level summaries and a final global prompt to synthesise a discharge-style narrative.
- **Model inference & optimisation:** Run FLAN-T5 and Meditron-7B in the same pipeline; apply practical optimisation tactics (e.g., batching/quantisation where needed) to fit shared compute constraints.
- **Evaluation:** Compare outputs to clinician-authored discharge notes using BERTScore precision, embedding similarity, sentence length, medical term density, and structured qualitative review.

## Key Outcomes / Contributions

- Demonstrated that structured ICU tables alone can be transformed into coherent discharge-style narratives that resemble clinician-authored summaries.
- Achieved high lexical alignment with reference discharge notes in the strongest pipeline version (BERTScore ≈ 0.8), with realistic sentence structure and improved medical term density in multiple views.
- Identified consistent behavioural differences: FLAN-T5 is more concise and cautious (lower hallucination, more omissions), while Meditron-7B is richer and higher-coverage (more verbosity and occasional speculative elaboration).
- Contributed a schema-agnostic, view-wise architecture and a task-specific evaluation framework, along with an explicit taxonomy of common failure modes relevant to safety.

## Tools & Technologies

- Python; pandas; NumPy; scikit-learn
- Streamlit (demo/interface), Plotly, Matplotlib (analysis & visualisation)
- LLMs: FLAN-T5; Meditron-7B

## Links

- [MIMIC-IV ICU (PhysioNet)](https://physionet.org/content/mimiciv/)
- [FLAN-T5 model family (Google Research / Hugging Face)](https://huggingface.co/google/flan-t5-large)
- [Meditron-7B (Hugging Face)](https://huggingface.co/epfl-llm/meditron-7b)
- [BERTScore (paper)](https://arxiv.org/abs/1904.09675)

## References

- BERTScore: Evaluating Text Generation with BERT. (Zhang et al.)
- MIMIC-IV: A freely accessible critical care database (Johnson et al., PhysioNet).
- FLAN-T5: Instruction-tuned text-to-text Transformer models.
- Meditron: Clinically specialised large language model family.
