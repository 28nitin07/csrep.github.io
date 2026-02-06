---
layout: projects/projects-individual
title: "The Psychological Underpinnings of Misinformation Perception"
advisor: "Dr. Anirban Sen and Dr. Dipanjan Chakraborty"
students: "Ansh Madan and Anagha Bhavsar"
abstract: "This capstone develops and validates a psychologically grounded framework for understanding why misinformation is persuasive. Rather than focusing only on surface linguistic cues, the project operationalises the Elaboration Likelihood Model (central vs. peripheral routes) alongside key cognitive biases (availability bias, naturalness bias, and illusory correlation). Using large language models, the authors generate and annotate synthetic misinformation-style headlines in health and technology, then empirically test how topic and psychological framing influence believability ratings in human surveys."
categories: ["Misinformation", "Computational Social Science"]
---

## Project Description

Misinformation spreads rapidly in modern digital environments, often outpacing fact-checking efforts and undermining trust in public discourse. While computational approaches to misinformation detection have advanced significantly, many systems rely heavily on superficial linguistic patterns or domain-specific cues, which limits their ability to generalise across topics and, crucially, fails to explain *why* certain false claims are persuasive.

This capstone project investigates the psychological mechanisms underlying misinformation perception. The work proposes a unified framework grounded in established theories from cognitive psychology and persuasion research. Specifically, the project operationalises the Elaboration Likelihood Model (ELM), distinguishing between central-route persuasion (evidence-based or technical framing) and peripheral-route persuasion (heuristic cues such as emotion, authority, or anecdote). In parallel, it incorporates three cognitive biases frequently implicated in misinformation belief: availability bias, naturalness bias, and illusory correlation.

The methodology follows a two-stage empirical pipeline. First, a Level 0 topic pre-test survey identifies domains that are both engaging and shared across participant cohorts, selecting health and technology as focal areas. Second, a Level 1 believability study uses Gemini Pro to generate and annotate misinformation-style headlines constrained by the psychological framework. A balanced pool of 40 stimuli is constructed and evaluated through online surveys measuring believability on a Likert scale.

Key outcomes include the creation of a psychologically annotated synthetic headline dataset, evidence of topic-level differences in believability, qualitative validation of LLM-generated labels, and the development of a DistilBERT-based multi-label classifier to predict persuasive mechanisms in misinformation. Overall, the project demonstrates how computational misinformation research can be strengthened by integrating psychological theory, enabling more interpretable and mechanism-aware approaches to detection and intervention.

## Objectives

- Develop a unified psychological framework for classifying misinformation persuasiveness mechanisms.
- Operationalise ELM routes and cognitive bias constructs into usable annotation labels.
- Generate and annotate synthetic misinformation headlines in high-impact domains.
- Empirically evaluate how psychological framing influences believability ratings.
- Establish infrastructure for future annotation of real-world misinformation corpora.

## Methodology / Approach

- **L0 Topic Pre-Test:** Surveyed participants across cohorts to select common and engaging misinformation domains.
- **Framework-Guided Generation:** Used Gemini Pro to create misinformation-style headlines aligned with specific psychological mechanisms.
- **LLM Annotation Pipeline:** Cross-annotated headlines with complementary framework labels and rationales.
- **Balanced Stimulus Construction:** Sampled a constrained 40-headline pool with equal topic representation.
- **Believability Survey:** Conducted two survey blocks measuring perceived believability on a 5-point scale.
- **Classifier Development:** Fine-tuned DistilBERT for multi-label prediction of psychological mechanisms.

## Key Outcomes / Contributions

- A validated, psychologically grounded taxonomy for misinformation mechanisms.
- Synthetic dataset of framework-labelled misinformation headlines in health and technology.
- Empirical findings on believability patterns by topic and persuasion route.
- DistilBERT multi-label classifier baseline for mechanism-aware misinformation analysis.
- Clear pathway for extending annotations to real-world datasets such as FakeNewsNet and MuMiN.

## Links

- GitHub (project artefacts and code): *Included in appendix of report*
- Related datasets for future extension: FakeNewsNet, MuMiN, IFND, TruthSeeker2023

## References

- Vosoughi, Aral & Roy (2018) – False news spreads faster than truth.
- Wardle (2018) – Taxonomy of misinformation and disinformation.
- Broda & Strömbäck (2024) – Systematic review of misinformation research.
