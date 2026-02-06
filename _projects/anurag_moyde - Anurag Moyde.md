---
layout: projects/projects-individual
title: "Expert-in-the-Loop IVF Clinical Document Digitization: A DocVQA-Driven Approach"
advisor: "Dr. Rintu Kutum"
students: "Anurag Moyde"
abstract: "This project designs and evaluates an expert-in-the-loop clinical document digitization platform for IVF medical records in the Indian healthcare context. The system integrates Document Visual Question Answering principles with structured annotation workflows to convert heterogeneous, unstructured IVF documents into schema-validated, research-ready datasets while preserving clinical provenance and auditability."
categories: ["Artificial Intelligence", "Healthcare"]
---

## Project Description

In vitro fertilization clinics across India generate large volumes of clinical documentation across treatment cycles, including laboratory reports, ultrasound measurements, hormone assays, embryology records, and stimulation protocols. Despite their clinical and research value, these records largely remain locked in unstructured formats such as scanned PDFs, printed reports, and handwritten notes. The lack of structured digitization prevents large-scale retrospective analysis, quality monitoring, and the development of AI-driven decision support systems for reproductive medicine.

This capstone project addresses this gap by designing and implementing an expert-in-the-loop clinical document digitization platform tailored specifically for IVF medical records. Rather than relying on fully automated extraction pipelines that risk clinically unsafe errors, the system combines machine-assisted OCR and DocVQA-inspired techniques with structured human verification. Clinical experts interactively review OCR-extracted text overlaid as bounding boxes on document images, correct transcription errors, and map extracted values to IVF-specific clinical fields.

A central contribution of the project is the use of a schema-first approach through LinkML-based clinical data models. All annotations are validated against predefined schemas, ensuring semantic consistency, completeness, and downstream interoperability. Each extracted field retains full provenance information, including page number, bounding box coordinates, and annotator metadata, making the resulting datasets auditable and suitable for clinical research.

The platform follows a modular service-oriented architecture with a React-based frontend for visual annotation and a Flask backend orchestrating OCR extraction, schema validation, and structured export. By reframing digitization from manual data entry to semantic validation, the system reduces expert burden while significantly improving data quality. The project demonstrates how hybrid human-machine workflows can reliably transform legacy IVF documents into FAIR-compliant datasets, laying the foundation for future AI research in IVF outcome prediction, treatment optimization, and personalized reproductive medicine.

## Objectives

- Design a clinically trustworthy digitization workflow for heterogeneous IVF medical documents.
- Integrate OCR and DocVQA-inspired techniques with expert-in-the-loop verification.
- Develop a schema-driven annotation framework using LinkML for IVF clinical fields.
- Ensure complete provenance, auditability, and schema compliance for all extracted data.
- Enable generation of research-ready structured datasets from legacy clinical records.

## Methodology

The system employs a hybrid digitization pipeline combining automated OCR extraction with structured human validation. Uploaded IVF documents are processed into page-level images, from which OCR generates text tokens with spatial bounding boxes. These tokens are rendered in an interactive annotation interface where experts correct errors, assign clinical labels, and validate values in real time.

A LinkML-based schema enforces data types, units, and required fields, providing immediate feedback on missing or inconsistent annotations. All edits are versioned and logged to preserve provenance. Once validated, the curated annotations are exported as schema-compliant JSON or CSV files suitable for downstream analytics and machine learning workflows.

## Key Outcomes

- A working expert-in-the-loop IVF document digitization platform with full-stack implementation.
- Schema-validated, provenance-rich structured datasets derived from unstructured clinical records.
- Demonstrated reduction in transcription errors and annotation burden compared to manual workflows.
- A reusable foundation for building high-quality IVF datasets for future AI and clinical research.
