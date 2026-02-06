---
layout: projects/projects-individual
title: "Accessible Security Interfaces for Security Protocol Verification"
advisor: "Aalok Thakkar"
students: "Kudakwashe Mavis Chakanyuka"
abstract: "This project explores how Human–Computer Interaction (HCI) principles can be applied to improve the usability and accessibility of security protocol verification. Formal verification tools provide strong guarantees about properties such as secrecy and authentication, but their outputs are often difficult for learners and practitioners to interpret. The project presents a lightweight, browser-based interface that visualises key cryptographic operations and message flows in an intuitive manner, enabling clearer understanding of protocol behaviour without requiring deep formal-methods expertise."
categories: ["Human-Computer Interaction", "Cybersecurity"]
---

This capstone project investigates how interface design can bridge the gap between formally verified security guarantees and human understanding. The work introduces a web-based, HCI-informed visual interface that makes cryptographic protocol behaviour easier to interpret, particularly for learners and practitioners without extensive formal verification backgrounds.

## Project Description

Security protocols are fundamental to modern digital systems, ensuring properties such as confidentiality, authentication, and integrity. Although formal verification tools can rigorously analyse whether these properties hold, their symbolic traces and text-heavy outputs are often inaccessible to non-experts. This project addresses this usability gap by designing an interface that translates abstract cryptographic operations into clear, visual, and interactive representations.

The system focuses on visualising core protocol operations such as hashing, encryption, decryption, pairing, unpairing, and nonce generation. Each step of a protocol is displayed sequentially, showing how messages are constructed, transformed, and exchanged between agents and how an attacker may observe or manipulate communications. Distinct visual cues, colour coding, and spatial organisation are used to differentiate operations and highlight security-relevant transformations.

Implemented entirely on the front end using HTML, CSS, and lightweight JavaScript, the interface requires no installation and runs directly in a browser. Interactivity is provided through animations, step-wise execution, and optional tooltips that explain operations on demand. The design follows accessibility principles, including high-contrast colour schemes, responsive layouts, and progressive disclosure of detail, allowing users to control the amount of information shown at any time.

User feedback from participants with and without computer science backgrounds indicates that the visual approach improves comprehension compared to traditional symbolic outputs. Participants reported greater confidence in following message flows and understanding why particular security properties hold. While the tool does not replace existing verification engines, it demonstrates how HCI-driven design can significantly enhance learning, exploration, and interpretation of security protocol behaviour.

## Objectives

- Identify usability challenges in existing security protocol verification tools  
- Design and implement a visual, HCI-informed interface for protocol exploration  
- Reduce cognitive load associated with understanding cryptographic operations  
- Support intuitive learning of secrecy, authentication, and pairing behaviours  

## Methodology / Approach

- Literature review on usable security, HCI, and formal verification tools  
- Iterative interface sketching and prototyping  
- Front-end implementation using HTML, CSS, and JavaScript  
- Informal user feedback from technical and non-technical participants  

## Key Outcomes / Contributions

- A browser-based visual interface for exploring security protocol behaviour  
- Demonstration that visual scaffolding improves understanding of cryptographic operations  
- Design insights for integrating HCI principles into security verification environments  
- Foundation for future integration with formal verification tools such as ProVerif or Tamarin  
