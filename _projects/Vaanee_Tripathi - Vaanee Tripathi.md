---
layout: projects/projects-individual
title: "Join the Dots: Real-Time Tactile Rendering of Classroom Diagrams for Students with Visual Impairments"
advisor: "Subhashish Bannerjee; Venkatesh Potluri"
students: "Vaanee Tripathi"
abstract: "This capstone explores the challenge of providing real-time accessibility to classroom diagrams for students with visual impairments, focusing specifically on flowcharts in computer science education. Through formative research, grammar design, and dual technical pipelines (traditional computer vision and vision-language models), the project investigates how hand-drawn instructional flowcharts can be automatically recognised and translated into structured representations suitable for accessible output modalities."
categories: ["Accessibility", "Computer Vision"]
---

## Project Description

Visual diagrams are central to STEM and computer science education, serving as cognitive tools that help students reason about algorithms, control flow, and system design. However, this visual reliance creates significant barriers for students with visual impairments, particularly in live classroom settings where diagrams are drawn and modified dynamically. Existing accessibility solutions primarily support asynchronous access through manually produced tactile graphics or expensive refreshable displays, but no widely available system enables real-time access to evolving instructional diagrams.

This capstone investigates the feasibility of real-time flowchart recognition and structured translation as a foundational step toward synchronous accessibility. The project began with a formative study analysing twelve hours of undergraduate lecture recordings to understand how diagrams are actually used in instructional practice. This study produced a taxonomy of visual content and revealed key challenges including temporal evolution of diagrams, implicit communication, spatial complexity, and instructor-specific drawing variation.

Based on these findings, the project defined a formal grammar for representing flowcharts, encoding nodes, edges, attributes, and metadata in a structured intermediate representation. This grammar serves as a bridge between raw visual input and downstream accessible outputs such as tactile renderings or audio descriptions.

Two technical pipelines were developed and evaluated. The first employs traditional computer vision techniques, including preprocessing, contour-based node detection, transformer-based OCR, multi-method edge detection, and structured export to Mermaid syntax. The second leverages a vision-language model to perform end-to-end recognition, generating both Mermaid representations and natural language explanations directly from images.

Empirical evaluation demonstrated that traditional computer vision provides high geometric precision and interpretability, while vision-language models offer stronger semantic understanding and multimodal explanation. Together, these findings establish technical feasibility and clarify architectural trade-offs, laying groundwork for future systems capable of enabling real-time accessible diagram interpretation in live educational contexts.

## Objectives

- Understand how flowcharts and visual diagrams are used in real classroom instruction.
- Define a structured grammar capable of representing flowchart semantics independent of visual appearance.
- Explore and compare traditional computer vision and vision-language model approaches to automated flowchart recognition.
- Generate structured outputs suitable for downstream accessible presentation modalities.

## Methodology

The project followed a three-stage methodology:

1. **Formative Study:** Qualitative analysis of ten undergraduate lecture videos to characterise diagram usage, temporal patterns, and instructional practices.
2. **Grammar Design:** Definition of a basic flowchart grammar capturing nodes, edges, attributes, and metadata, with conceptual extension toward a comprehensive multimodal grammar.
3. **Dual Pipeline Exploration:** Implementation of (a) a traditional computer vision pipeline using contour detection, OCR (TrOCR), and multi-method edge detection, and (b) a vision-language model pipeline generating Mermaid syntax and explanatory text.

## Key Outcomes

- Developed a taxonomy of visual content used in CS instruction.
- Defined a formal flowchart grammar for structured representation.
- Built and evaluated two recognition pipelines.
- Demonstrated complementary strengths of traditional CV and VLM-based approaches.
- Identified preprocessing mismatch effects on transformer-based vision models.
- Established groundwork for future real-time, multimodal accessible diagram systems.

## Future Directions

Future work includes real-time video processing, multimodal alignment with speech and gesture, improved shape vocabulary, expanded test datasets, and user-centred evaluation with visually impaired students to determine optimal presentation modalities.
