---
layout: projects/projects-individual
title: "Agentic AI System for Conversational Data Analytics and Forecasting"
advisor: "Prof. Lipika Dey; Prof. Prartha Pratim Das"
students: "Ziv Barretto, Jacob Mathew"
abstract: "This project develops a truly agentic AI system for conversational data analytics and forecasting. Instead of running a fixed pipeline, the system autonomously reasons about a user’s natural-language request, routes it to specialized agents (e.g., exploratory data analysis vs. forecasting), and uses ReAct-style tool use to iteratively plan, act, and adapt. A key capability is autonomous Python code generation for custom EDA and analysis, enabling flexible insight discovery and end-to-end forecasting workflows from plain-language prompts."
categories: ["Artificial Intelligence", "Data Analytics"]
---

## Project Description

The democratization of data analytics is still limited by the technical barriers required to clean data, choose appropriate statistical methods, build forecasting models, and interpret results. This capstone implements an **agentic** (not merely automated) conversational system that allows a user to explore datasets and run forecasting tasks through natural language. The core idea is that the system does not execute a pre-written, linear script. Instead, it exhibits **autonomous decision-making**: it interprets intent, selects an appropriate workflow pathway, and coordinates specialized agents that can reason, call tools, and recover from errors.

The system supports multiple high-level pathways: (1) interactive exploratory data analysis (EDA) for user questions such as distributions, correlations, missingness, and descriptive statistics; (2) dataset profiling and task proposal, where the system summarizes datasets, assesses forecasting suitability (e.g., datetime columns and viable targets), and proposes a ranked set of feasible analytical tasks; and (3) a forecasting pipeline that executes an end-to-end workflow once a task is selected. A key capability is **autonomous Python code generation** for EDA: the EDA agent generates and runs custom analysis code per query, rather than relying on hard-coded analysis functions. To ensure robustness, the architecture includes explicit state management, routing logic, and recovery behaviors for tool failures, schema mismatches, and long-running multi-stage benchmarks. Overall, the project demonstrates how multi-agent routing plus ReAct-style reasoning can make data analysis and forecasting more accessible, flexible, and resilient for non-technical users while retaining the power of programmatic analytics.

## Objectives

- Enable natural-language analytics and forecasting without requiring users to write code or know modeling workflows.
- Implement intent-aware routing that selects between EDA, dataset analysis, and forecasting execution paths.
- Support autonomous tool use and reasoning (ReAct) for iterative planning, execution, and adaptation.
- Generate and execute Python code dynamically for flexible EDA and custom analytical requests.
- Improve reliability via guardrails, state-machine design, and failure recovery mechanisms.

## Methodology / Approach

- **Multi-agent architecture:** A conversation agent classifies intent and routes requests to specialized agents (e.g., EDA agent, dataset profiling, task proposal, and forecasting execution stages).
- **ReAct reasoning loop:** Agents “think–act–observe” by selecting tools, running actions, inspecting results, and adapting plans.
- **Autonomous code generation:** The EDA agent writes Python code tailored to the user’s query, executes it, and summarizes results back to the user.
- **Dataset understanding pipeline:** The system profiles datasets, computes data-quality indicators, identifies datetime columns and candidate targets, and saves structured summaries that downstream agents can reuse.
- **State management & robustness:** Checkpointing, schema validation, and recovery logic mitigate tool failures, token constraints, and join-plan or pipeline mismatches.

## Key Outcomes / Contributions

- A working conversational analytics pipeline that distinguishes **agentic** behavior (autonomous routing and reasoning) from simple automation.
- Support for both exploratory analysis and structured forecasting workflows, driven by plain-language user prompts.
- A staged dataset-analysis framework (profiling → task proposals → execution) that enables repeatable experimentation and benchmarking.
- Practical reliability features: explicit orchestration logic, memory/state handling, and error recovery strategies for real-world tool brittleness.

## Links

- LangChain (tooling foundation): https://github.com/langchain-ai/langchain

## References

- ReAct: “Reasoning and Acting in Language Models” (cited in report).
- LangGraph (multi-actor/stateful LLM applications) (cited in report).
