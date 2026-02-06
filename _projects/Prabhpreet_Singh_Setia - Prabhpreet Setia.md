---
layout: projects/projects-individual
title: "Robust Vision Transformers via Lipschitz Certification and Attention Regularization"
advisor: "Prof. Aalok Thakkar"
students: "Prabhpreet Singh Setia, Pranav Jayanandan"
abstract: "Transformer architectures have become foundational across computer vision and multimodal learning, yet they remain highly vulnerable to adversarial perturbations. This project integrates global Lipschitz certification with local Jacobian-based attention regularization to improve robustness in Vision Transformers. By combining CertViT’s architecture-level Lipschitz constraints with JaSMin’s softmax Jacobian smoothing, the work demonstrates improved empirical robustness while preserving competitive clean accuracy, particularly on MNIST and partially on CIFAR-10."
categories: ["Machine Learning", "Computer Vision"]
---

## Project Description

Transformer-based models, particularly Vision Transformers (ViTs), have rapidly become central to modern machine learning systems due to their expressive power and scalability. However, this success has been accompanied by a growing concern: Transformers are especially vulnerable to adversarial perturbations. Small, carefully crafted input changes can lead to large and unpredictable shifts in model predictions, raising serious concerns for safety-critical and security-sensitive applications.

This capstone project investigates robustness in Vision Transformers through the lens of both certified and empirical defenses. Certified robustness methods aim to provide formal guarantees that a model’s prediction cannot change under bounded perturbations, while empirical methods focus on improving resistance to specific attack strategies. Unfortunately, most certified approaches struggle to scale to Transformers because attention mechanisms—particularly dot-product attention combined with softmax—exhibit highly non-Lipschitz behavior. On the other hand, empirical defenses such as adversarial training provide strong practical robustness but lack worst-case guarantees.

The core objective of this project is to bridge this gap by integrating two complementary frameworks: CertViT and JaSMin. CertViT enforces global Lipschitz continuity in Vision Transformers through architectural modifications, spectral norm constraints, and Douglas–Rachford projection, enabling formal robustness certification. JaSMin, in contrast, targets local instability by regularizing the Jacobian of the softmax attention mechanism, discouraging overly sharp or degenerate attention distributions.

By unifying these approaches, the project proposes a hybrid framework that simultaneously controls global smoothness and local attention dynamics. Extensive experiments on MNIST demonstrate a substantial improvement in adversarial robustness, measured via PGD attacks, while maintaining high clean accuracy. Preliminary CIFAR-10 results, although limited by computational constraints, indicate stable scaling behavior and consistent robustness trends. Overall, this work provides evidence that global Lipschitz constraints and local Jacobian smoothing act synergistically, offering a promising path toward more reliable and certifiable Transformer-based vision models. fileciteturn0file0

## Objectives

- Study the sources of adversarial vulnerability in Vision Transformers.
- Implement and analyze CertViT for global Lipschitz-based robustness certification.
- Integrate JaSMin softmax Jacobian regularization into a Lipschitz-constrained Transformer architecture.
- Evaluate the combined framework on standard vision benchmarks.
- Analyze the relationship between global Lipschitz bounds and empirical robustness.

## Methodology

The project adopts the CertViT architecture, which modifies standard Vision Transformers to admit analytic Lipschitz bounds through spectral normalization of linear layers and an alternative L2-based attention mechanism. Douglas–Rachford splitting is used during training to enforce spectral constraints while preserving optimization stability.

On top of this architecture, the JaSMin regularizer is integrated into the training objective. JaSMin penalizes the spectral norm of the softmax Jacobian, encouraging smoother and more stable attention distributions. The final loss function combines standard cross-entropy with a weighted Jacobian regularization term.

All experiments are implemented in PyTorch. Due to CPU-only computational constraints, MNIST is used as a proof-of-concept benchmark, while CIFAR-10 serves as a limited scaling and stability test. Robustness is evaluated using projected gradient descent (PGD) attacks, alongside clean and certified accuracy metrics.

## Results and Contributions

- Demonstrated a significant improvement in empirical adversarial robustness on MNIST (+21% PGD accuracy) when combining CertViT with JaSMin.
- Showed that local Jacobian smoothing can improve robustness even when global Lipschitz bounds become looser.
- Validated stable integration of Jacobian regularization into a Lipschitz-constrained Transformer architecture.
- Provided insights into the complementary roles of global and local smoothness in robust Transformer design.

## References

- CertViT: Certified Vision Transformers via Lipschitz Regularization
- JaSMin: Jacobian Smoothing of Softmax for Robust Attention
- Related literature on certified robustness, Lipschitz neural networks, and adversarial machine learning
