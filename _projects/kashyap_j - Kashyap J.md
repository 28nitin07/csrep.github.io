---
abstract: This project develops India-specific AI safety benchmarks and
  risk databases focused on education and financial lending. It
  constructs domain-specific AI Safety Risk Databases and a unified
  ontology grounded in real-world Indian deployments. In addition, it
  introduces an education-focused bias benchmark evaluating large
  language models across caste, religion, and linguistic identity using
  ambiguous and disambiguated question formats. Together, these
  contributions provide a structured, empirically grounded foundation
  for AI safety assessment and governance in the Indian context.
advisor: Professor Anirban Sen, Professor Debayan Gupta, Professor Aalok
  Thakkar
categories:
- AI Safety
- Responsible AI
layout: projects/projects-individual
students: Ananya Basotia, Kashyap J
title: Developing AI Safety Benchmarks and Databases in the Indian
  Context
---

## Project Description

This capstone project addresses a major gap in AI safety research: the
lack of structured, India-specific understanding of how AI risks
manifest in real socio-technical contexts. While global AI safety
frameworks exist, they are largely designed around Western assumptions
and often overlook Indian realities such as caste hierarchies,
linguistic diversity, infrastructural constraints, and uneven digital
access. As AI systems become embedded in India's Digital Public
Infrastructure and Digital Public Goods, failures in these systems can
have wide-ranging social consequences.

The project focuses on two high-impact domains: school education and
financial lending. The first objective was to systematically identify
and document AI-related harms in these sectors. Using academic
literature, policy reports, and investigative journalism, the authors
compiled a large corpus of risk instances. These were organized into two
domain-specific AI Safety Risk Databases, each structured into clear
categories and sub-categories such as bias and exclusion, hallucination
and incorrect output, situational awareness failures, toxicity, and
security and privacy risks.

Building on these databases, the project develops a unified,
domain-agnostic AI safety ontology. This ontology captures shared
structures and causal patterns across domains, enabling a more general
understanding of how AI risks arise in India. A causal characterization
framework further classifies risks by stage of occurrence, stakeholder
involvement, and intent, helping clarify where accountability and
interventions may lie.

The second major contribution is an India-specific education bias
benchmark for large language models. Inspired by BBQ and BharatBBQ, the
benchmark centers on realistic Indian classroom scenarios and evaluates
model behavior across caste, religion, and linguistic identity. The
dataset includes around 21,000 question--answer pairs, with both
ambiguous and disambiguated formats. Established metrics such as
Ambiguous Accuracy, Disambiguated Accuracy, and multiple bias scores are
used to measure abstention, correctness, and stereotype alignment.

Evaluation results show that bias patterns differ across identity axes,
with particularly strong stereotype alignment in explicit reasoning
tasks for caste and religion, and weak performance on linguistic
identity. Overall, the project provides both conceptual tools
(taxonomies and ontology) and empirical tools (benchmark and metrics)
that can support future auditing, research, and governance efforts for
safer and more inclusive AI in India.
