---
layout: projects/projects-individual
title: "Falcon Aadhaar: Post-Quantum Secure & Privacy-Preserving Age Proofs for Aadhaar via Incremental Falcon Verification"
advisor: "Mahabir Prasad Jhanwar, Saravanan Vijayakumaran"
students: "Aryan Nath"
abstract: "This project designs a post-quantum secure and privacy-preserving age proof system for India’s Aadhaar identity infrastructure. It replaces the classical RSA signature used in Aadhaar QR codes with the lattice-based Falcon signature scheme and integrates this verification into an incrementally verifiable computation framework. The construction enables users to prove that they are above a given age threshold without revealing any other personal information contained in their Aadhaar credential."
categories: ["Cryptography", "Zero-Knowledge Proofs", "Privacy"]
---

## Project Description

Know Your Customer (KYC) systems in India commonly rely on Aadhaar-based verification, which requires individuals to disclose their full identity credentials even when only a single attribute, such as age, is relevant. This approach creates significant privacy risks, as sensitive information like residential address, gender, and exact date of birth are unnecessarily shared with service providers. The goal of this project is to demonstrate that existing Aadhaar credentials can be used to generate privacy-preserving proofs, allowing individuals to selectively prove eligibility properties without exposing their underlying data.

This capstone project focuses on the design of a privacy-preserving age proof that is secure even against quantum adversaries. Prior Aadhaar-based age proof systems rely on RSA signatures embedded in Aadhaar QR codes, which are vulnerable in a post-quantum setting. To address this limitation, the project retrofits Aadhaar QR codes with Falcon, a lattice-based digital signature scheme believed to be secure against quantum attacks. The project further integrates Falcon signature verification into an incrementally verifiable computation (IVC) framework, enabling efficient zero-knowledge proofs over large computations.

The resulting system allows a prover to demonstrate that their Aadhaar credential was legitimately issued and that the encoded date of birth exceeds a required age threshold, while revealing nothing else about the credential. Importantly, the design preserves desirable properties such as intra-application linkability (to prevent proof sharing) and inter-application unlinkability (to prevent cross-service tracking). By combining post-quantum cryptography with modern zero-knowledge techniques, this project shows how national-scale identity systems can be upgraded to meet future security and privacy requirements without redesigning the entire infrastructure.

## Objectives

- Design a privacy-preserving age proof mechanism for Aadhaar-based verification.
- Achieve post-quantum security by replacing RSA signatures with Falcon signatures.
- Integrate signature verification into an incrementally verifiable computation framework.
- Preserve privacy properties such as minimal disclosure, unlinkability, and local proof generation.

## Methodology

The project begins by analyzing the structure of Aadhaar QR codes and existing zero-knowledge age proof systems. The RSA-based signature verification is replaced with Falcon-512, chosen for its relatively compact signatures and efficient verification. Falcon signature verification is then expressed as an incremental computation compatible with the Nova folding scheme for IVC.

The system models the age proof as an NP statement enforced through Rank-1 Constraint Systems (R1CS). SHAKE256 hashing, polynomial operations over NTRU lattices, and ℓ2-norm bounds required for Falcon verification are encoded into arithmetic circuits. Incremental verification allows the proof to be generated efficiently while maintaining strong soundness and privacy guarantees.

## Outcomes and Contributions

- A post-quantum secure age proof construction for Aadhaar QR codes.
- An incremental Falcon signature verification circuit suitable for zero-knowledge proofs.
- A detailed R1CS-based formulation of privacy-preserving age verification.
- A prototype implementation demonstrating feasibility and efficiency compared to prior work.

## Links

- GitHub Repository: https://github.com/natharyan/falcon-aadhaar
