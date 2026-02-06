---
abstract: This project implements and benchmarks two Private Set
  Intersection (PSI) protocols---OT‑PSI and Laconic PSI---under
  realistic security parameters. It analyzes the trade‑off between
  computational cost and communication bandwidth, and empirically
  verifies the constant‑size receiver communication property of Laconic
  PSI.
advisor: Prof. Debayan Gupta
categories:
- Cryptography
- Systems
layout: projects/projects-individual
students: Chirag S
title: Comparative Implementation and Analysis of Authorized Private Set
  Intersection Protocols
---

## Project Description

Private Set Intersection (PSI) enables two parties to compute the
intersection of their datasets without revealing any additional
information. This project focuses on implementing and empirically
comparing two distinct PSI paradigms: the widely used, speed‑optimized
OT‑PSI protocol and the bandwidth‑optimized Laconic PSI protocol. The
central motivation is to study scenarios where communication cost
dominates, such as large receiver datasets or constrained network
environments.

The project implements both protocols from research literature and
benchmarks them across multiple security levels, ranging from 256‑bit to
2048‑bit parameters. The OT‑PSI protocol is used as a baseline due to
its practical performance and widespread adoption. Laconic PSI, in
contrast, enables an "authorized" setting in which the receiver
publishes a constant‑size digest that can be reused by multiple senders.
This enables asynchronous and bandwidth‑efficient intersections.

The implementations are written in Python with a modular architecture
separating cryptographic primitives from protocol logic. Extensive
benchmarks evaluate runtime, communication overhead, and the impact of
dataset overlap. The results confirm that OT‑PSI remains the practical
choice for real‑time applications due to its efficient symmetric‑key
operations. However, Laconic PSI achieves a constant receiver
communication size, demonstrating dramatic bandwidth savings for large
datasets.

Overall, the project bridges the gap between theoretical laconic
constructions and practical implementations, and provides empirical
evidence of the trade‑offs between computation and communication in
modern PSI protocols.

## Methodology

-   Implemented OT‑PSI using Naor‑Pinkas Base OTs and IKNP OT Extension
    with Cuckoo hashing.
-   Implemented Laconic PSI using the Damgård‑Jurik cryptosystem and a
    Hash‑and‑Test PPRF.
-   Benchmarked both protocols across security parameters of 256, 512,
    1024, and 2048 bits.
-   Measured execution time, bandwidth usage, and the impact of dataset
    overlap.
-   Evaluated scalability and analyzed computational bottlenecks.

## Key Results and Contributions

-   Developed a complete Python implementation of the Laconic PSI
    protocol.
-   Empirically verified constant‑size receiver communication (512 bytes
    at 2048‑bit security).
-   Demonstrated significant bandwidth savings compared to OT‑PSI for
    large datasets.
-   Engineered a robust OT‑PSI implementation with dynamic stash sizing
    and full correctness at large scales.
-   Quantified the computational trade‑offs across multiple security
    levels.

## References

1.  Pinkas, Schneider, and Zohner. *Scalable Private Set Intersection
    Based on OT Extension*. USENIX Security, 2016.
2.  Alamati et al. *Laconic Private Set Intersection and Applications*.
    CRYPTO, 2021.
