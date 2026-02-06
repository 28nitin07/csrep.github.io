---
layout: projects/projects-individual
title: "The Dependence of Cognitive Load on Representational Formats"
advisor: "Professor Sudheendra Hangal"
students: "Anirvaan Kar, Myra Malik"
abstract: "Sudoku puzzles have evolved into numerous variations, including colour-based and symbol-based versions. While cognitive load theory suggests that tasks imposing significant information processing demands strain working memory, few studies have examined how representational changes—such as using colours versus numbers—affect cognitive load during puzzle solving. The present study investigates whether identical Sudoku puzzles produce different levels of cognitive load depending on their perceptual representation (colour vs. numbers), isolating the cognitive demands of representation from logical complexity."
categories: ["Cognitive Science", "Human-Computer Interaction"]
---

This project studies how the *representation* of the same underlying logic problem changes the mental effort required to solve it, using Sudoku as a controlled testbed.

## Project Description

Sudoku has spawned many variants that change how information is presented (for example, replacing digits with colours or symbols). Cognitive Load Theory argues that working memory is limited, and that extra “translation” effort introduced by the interface can increase *extrinsic* cognitive load even when the underlying problem remains equally difficult. This capstone tests that idea by holding puzzle logic constant and changing only representation: a traditional **number Sudoku** (digits 1–4) versus an equivalent **colour Sudoku** (four colours mapped to the same solution structure). The puzzles were deliberately kept small (4×4) to reduce confounds from extreme logical complexity, and to ensure the two conditions differ primarily in perceptual decoding rather than search depth.

The project implements a controlled **within-subjects** experiment in which every participant solves both puzzle versions, with the order counterbalanced to mitigate learning effects. The solving sessions are instrumented through the puzzle platform’s event logging: each write, erase, and overwrite is captured with timestamps and puzzle metadata. A Python-based log parsing pipeline reconstructs ordered move sequences per participant and condition, and computes derived behavioural metrics such as **time-to-first-write**, **completion time**, **inter-move intervals**, **long “thinking pauses”**, and **backtracking behaviour**. These metrics are used as objective proxies for cognitive load and efficiency, complementing participants’ perceptions of difficulty.

Across the exploratory dataset, results indicate a consistent advantage for the numerical representation on time-based and efficiency measures. Colour representation imposed a measurable orientation cost at the start of solving and was associated with more frequent long pauses during the session, even when the overall solution strategy appeared similar. The capstone’s main contribution is evidence that representational format can meaningfully alter cognitive workload in sequential logic tasks, alongside a reusable data pipeline that can scale to larger cohorts and additional interface conditions.

## Objectives

- Compare cognitive load between numerical and colour Sudoku using objective performance metrics (reaction time and accuracy).
- Examine whether colour-based representation facilitates or hinders early pattern recognition.
- Evaluate whether representational format influences how quickly participants make valid moves.
- Design two Sudoku puzzles of identical difficulty (one numerical and one colour-based) and build a logging + analysis pipeline for controlled behavioural evaluation.

## Methodology / Approach

- **Experimental design:** Within-subjects; each participant solves both the number and colour versions.
- **Independent variable:** Puzzle representation (digits 1–4 vs. four colours mapped to the same solution structure).
- **Dependent variables:** Completion time, backtracks (erasures/overwrites), and average move time; additional logged measures include time-to-first-write and long “thinking pauses” (e.g., >3s).
- **Controls:** Identical puzzle layout and solution; same device/interface and environment; equivalent puzzle difficulty; logging plugins to record move-level behaviour.
- **Counterbalancing:** Order is counterbalanced across participants to mitigate learning effects (number→colour vs. colour→number).
- **Data pipeline:** Logs are parsed in Python (regular expressions + pandas) to reconstruct ordered move sequences per participant/condition and compute derived metrics; outputs are stored as normalised CSV tables for analysis.

## Key Outcomes / Contributions

- **Consistent performance advantage for number Sudoku:** Time-based and efficiency metrics favoured numerical representation over colour representation.
- **Higher orientation cost for colour:** Participants showed substantially longer *time-to-first-write* on colour Sudoku, indicating extra initial decoding/translation effort.
- **Sustained higher cognitive load proxies on colour:** More frequent long “thinking pauses” during colour Sudoku sessions, suggesting ongoing working-memory demands beyond initial orientation.
- **Strategy vs. execution split:** Although solution paths/order heatmaps were similar across conditions, representation strongly affected execution efficiency (time and pause patterns), supporting the idea of an extrinsic “translation penalty.”
- **Reusable instrumentation:** A complete, scalable log-parsing and analysis workflow (raw log storage → parsing → derived metrics → plots) that can be extended to larger cohorts and additional representational conditions.

## Extensions / Future Work

- Evaluate **dual coding** interfaces (e.g., coloured digits) to test whether combining cues reduces load or increases interference.
- Scale up participants and include formal statistical testing (beyond exploratory/descriptive analysis).
- Test additional representational changes (symbols, shapes, ordering cues) and larger grid sizes to study generalisation.

## Links

- Report: (this submission)
- Code / dataset / demo: Not specified in the report.

## References

- Cognitive Load Theory and working memory literature motivating extrinsic vs. intrinsic load (as discussed in the report).
