---
layout: projects/projects-individual
title: "Implementation of Social Media News Communities: Gatekeeping, Coverage, and Statement Bias in the Indian Context"
advisor: "Prof. Anirban Sen"
students: "Kartikeya Agrawal"
abstract: "This capstone project implements an end-to-end computational pipeline to analyze and quantify media bias within the Indian news ecosystem. Adapting the framework of Saez-Trumper et al. (2013), the project introduces a novel Event Threading algorithm using SBERT embeddings and Time Decay to cluster over 84,000 news stories. The study uncovers systemic structural biases, including a tendency towards 'Pop-Patriotism', the formation of 'Megaphone' echo chambers in foreign policy, and a 'Compliance Machine' that aligns media sentiment with state narratives."
categories: ["Natural Language Processing", "Computational Social Science"]
---

## Project Description

In the world's largest democracy, the news media plays a critical role in shaping public opinion. However, this landscape is increasingly fractured by polarization and systemic bias. This capstone project addresses the challenge of quantifying these biases at scale, moving beyond simple keyword counts to understand the structural "agenda setting" and "framing" mechanisms of the news cycle. The primary objective was to implement an automated pipeline capable of ingesting, clustering, and analyzing Indian news coverage to detect three specific types of bias: Gatekeeping (what stories are chosen), Coverage (how attention is allocated), and Statement bias (how stories are framed).

The motivation for this work lies in the difficulty casual readers face in identifying systemic bias amidst the noise of the 24-hour news cycle. By analyzing over 84,000 stories from the MediaCloud API covering five key political topics (Elections, Budget, Foreign Policy, Supreme Court, and Military) between 2020 and 2025, the project sought to provide a data-driven "audit" of the Indian media ecosystem. The study adapts the framework of Saez-Trumper et al. (2013) to the Indian context, introducing methodological advancements such as Semantic Embeddings (SBERT) and Time-Decay clustering to handle the specific complexities of the Indian digital news environment.

## Methodology

The system follows a modular pipeline architecture designed to process high-dimensional and noisy text data:

1.  **Data Ingestion & Preprocessing:** Data was sourced from the MediaCloud API, focusing on National and State/Local Indian collections. A critical deduplication step was implemented using unique story IDs to filter out syndicated wire content (e.g., PTI, ANI), ensuring the analysis focused on editorial choices rather than syndication volume.
2.  **Semantic Embedding & Clustering:** Unlike traditional TF-IDF approaches, this project utilized Sentence-BERT (SBERT all-MiniLM-L6-v2) to map headlines to a dense vector space, capturing semantic meaning beyond keyword overlap. A core innovation was the **Event Threading with Time Decay** algorithm. This approach models the "lifecycle" of news events by combining semantic similarity with a time-decay function ($\alpha=0.15$), effectively separating distinct events that share similar keywords but occur at different times.
3.  **Bias Quantification:**
    - **Gatekeeping Bias (Volume):** Measured by aggregating story counts per cluster to identify prioritized topics.
    - **Coverage Bias (Network Analysis):** Utilized Jaccard Similarity indices ($J > 0.075$) to construct source networks, identifying "Echo Chambers" where media outlets exhibit high structural overlap.
    - **Statement Bias (Sentiment):** Applied VADER sentiment analysis to quantify the "Framing" of headlines, measuring the compound sentiment scores (-1 to +1) across different topics.

## Key Outcomes

The analysis revealed that the Indian media ecosystem functions less as a check on power and more as a "Manufactured Consensus Engine." Key findings include:

- **The "Pop-Patriotism" Gap (Gatekeeping):** The study found that "performative" spectacle is consistently prioritized over substantive policy. For instance, a Bollywood celebrity's tweet regarding a military operation received 3.3x more coverage than a strategic analysis of ceasefire violations, highlighting a preference for entertainment over civic accountability.
- **The "Megaphone" Effect (Coverage):** Network analysis exposed a high-homophily "hairball" structure in Foreign Policy coverage, where diverse sources collapsed into a single narrative node. Conversely, economic policy (Budget) coverage was fractured into an "SEO Archipelago" of disconnected micro-topics, preventing cohesive national debate.
- **The Sentiment Paradox (Statement):** A clear "Hope vs. Fear" dichotomy was observed. Foreign Policy was consistently framed with negative "War Rhetoric" (fear), while the Budget was framed with overwhelmingly positive government slogans (hope). Additionally, the "Conditional Sanctity" of the Supreme Court showed that judicial verdicts are framed positively only when they align with majoritarian sentiment.

### References

- Saez-Trumper, D., Castillo, C., & Lalmas, M. (2013). Social Media News Communities: Gatekeeping, Coverage, and Statement Bias.
- Reimers, N., & Gurevych, I. (2019). Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks.
- MediaCloud API Collections: India National (34412118) and India State/Local (38379954).
