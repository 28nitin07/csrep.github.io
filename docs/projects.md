
---
layout: projects/projects-individual
title: "Early ICU Mortality Prediction from 48-Hour EHR Data"
advisor: "Prof. Lipika Dey, Dr. Mayank Garg"
students: "Anurav Singh"
abstract: "This project studies early ICU mortality prediction using the first 48 hours of electronic health record data from the MIMIC-IV dataset. It compares heterogeneous graph neural networks with autoencoder-based representation learning pipelines to determine which modeling paradigm better captures clinically relevant temporal structure under severe sparsity and class imbalance."
categories: ["Machine Learning", "Healthcare"]
---

## Project Description

Predicting early mortality in Intensive Care Units (ICUs) is a central challenge in clinical decision support, with significant implications for timely intervention and resource allocation. Modern ICUs generate dense streams of heterogeneous electronic health record (EHR) data, including vital signs, laboratory measurements, medications, procedures, and static demographics. However, these data are high-dimensional, irregularly sampled, sparse, and heavily imbalanced, making reliable early risk estimation difficult for both clinicians and machine learning models.

This project focuses on predicting early in-ICU mortality using only the first 48 hours of patient data following ICU admission. Early mortality is defined as death within seven days of admission or within forty-eight hours of discharge. Using the publicly available MIMIC-IV database, the study investigates whether clinically meaningful signals can be extracted from short-horizon ICU trajectories despite noise, missingness, and low outcome prevalence.

Two contrasting modeling paradigms are explored. The first uses a heterogeneous Graph Neural Network (GNN) to explicitly model patient–timeslice relationships by representing each ICU admission as a graph consisting of a patient node and 48 hourly timeslice nodes connected by temporal and semantic edges. The second approach compresses flattened 48-hour multivariate time series into compact latent representations using autoencoders, which are then used for downstream mortality classification.

Through a systematic comparison of these approaches, the project evaluates predictive performance, robustness under class imbalance, and interpretability. While neither approach achieves clinically actionable performance, the results demonstrate that compact latent representations learned through autoencoders provide improved precision–recall balance, more stable training, and clearer post-hoc explanations compared to graph-based message passing on sparse hourly graphs.

## Objectives

- Predict early ICU mortality using only the first 48 hours of EHR data  
- Compare graph-based and representation-learning approaches under severe sparsity  
- Evaluate performance trade-offs between discrimination, recall, and precision  
- Analyze interpretability of learned representations in a clinical context  

## Methodology

The dataset was constructed from MIMIC-IV ICU stays with length of stay of at least 48 hours and patient ages between 18 and 80. Chart events, input events, and procedure events were aggregated into hourly bins for the first 48 hours. Missing chart values were forward/backward filled, while procedures and inputs were zero-filled. Features were robust-scaled, and highly skewed variables were log-transformed.

The GNN approach modeled each ICU stay as a heterogeneous graph with patient and hourly timeslice nodes, using a single-layer GATv2-based architecture with edge-type-specific attention. Class imbalance was addressed using focal loss, weighted sampling, and undersampling strategies.

The autoencoder-based pipeline flattened each 48×117 hourly matrix into a single vector and trained a multilayer perceptron autoencoder to learn a 64-dimensional latent embedding. These embeddings were used to train LightGBM and MLP classifiers. Model interpretability was explored using SHAP values projected back to the original feature–hour space via decoder-based attribution.

## Key Outcomes

- GNN achieved ROC–AUC ≈ 0.78 but low F1 due to sparse hourly graphs  
- Autoencoder-based models achieved higher F1 and better precision–recall balance  
- Latent embeddings enabled stable training and improved interpretability  
- Early hours and physiologic markers such as arterial pH and creatinine were consistently influential  

## Links

- Dataset: https://physionet.org/content/mimiciv/
