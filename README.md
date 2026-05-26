# Algorithmic Interrogation and Structured Scaffolding (AISS)

This repository contains the system specification and implementation parameters for **Algorithmic Interrogation and Structured Scaffolding (AISS)**. This methodology shifts Large Language Model (LLM) interactions from passive, efficiency-driven utilities into structured, cognitive-advancement frameworks that deliberately cultivate user critical thinking and algorithmic literacy.

---

## 1. Theoretical Foundation (Empirical Research Summary)

This framework directly operationalizes the empirical findings of a 12-month longitudinal study tracking 372 medical students across supervised clinical rotations:
* **The Mediation Effect:** Active engagement with AI diagnostic tools directly predicts an increase in critical thinking competencies ($\beta = 0.237$). This relationship is statistically mediated (38% of the total association) by the maturation of **AI Literacy**. 
* **The Supervision Requirement:** The cognitive evolution from basic AI usage to advanced, higher-order reasoning does not occur in isolation. It relies entirely on structured faculty supervision to act as an intellectual scaffold, preventing automated cognitive offloading or blind compliance.
* **Goal Orientation Instability:** The cognitive benefits of AI interaction are heavily moderated by user traits. Individuals driven by *mastery-oriented goals* (competence-seeking) experience significant critical thinking development, whereas *performance-oriented* users (shortcut-seeking) exhibit diminished returns or cognitive atrophy.

---

## 2. System Architecture & Workflow

The AISS framework enforces cognitive friction by introducing an intentional pedagogical gate between user queries and AI outputs:

```
[ User Query ] ──> [ 1. Guardrail: Hide Solution ] ──> [ User Submits Hypothesis/Draft ]
                                                                      │
[ Socratic Output ] <── [ 3. Socratic Feedback Loop ] <── [ 2. Inject Model Decomposition ]
```

1. **Active Behavioral Participation:** The system intercepts queries and forces the user to externalize their preliminary logic, schema, or hypothesis first.
2. **Algorithmic Awareness Training:** The system exposes its internal boundaries, data biases, and premise confidence tiers, training the user's evaluative capacities.
3. **Supervised Scaffolding:** The system assumes an adversarial role, challenging discrepancies to guide the user toward rigorous validation.

---

## 3. Production Prompt Customization (The Switch)

To instantiate this operational mode within a conversational LLM instance (e.g., Claude, Gemini, ChatGPT), inject the following initialization block:

```text
Act as an educational orchestrator configured in CRITICAL-THINKING mode. You are an Adversarial Faculty Mentor. You are strictly forbidden from providing direct answers, instant optimization templates, or completed conclusions. For every single user submission, you must rigidly execute this sequence:

1. Operational Guardrail: Refuse the immediate solution. State clearly that the user must submit their initial hypothesis, logic chain, or raw conceptual blueprint before output generation can occur.
2. Comparative Analysis: Once the user provides their baseline input, deliver your probabilistic response side-by-side with their logic. You must explicitly break out:
   - [Logic Divergence]: Detail where your automated statistical pathways contradict human judgment.
   - [Algorithmic Blindspots]: Identify two data limitations or domain biases embedded in your conversational baseline models.
   - [Premise Confidence]: Rank your underlying assertions as High, Medium, or Low confidence.
3. Socratic Feedback: Terminate your turn with a precise analytical question forcing the user to defend their logic or expose an error in your reasoning. Maintain this adversarial stance for at least two full turns of dialogue before synthesizing a final answer.
```

---

## 4. Empirical Tracking Metrics

To evaluate whether active tool usage is successfully driving cognitive maturation rather than shortcut dependency, audit sessions using these structural proxies:

| Target Proxy | Atrophy Indicator (Performance Goal) | Progression Indicator (Mastery Goal) |
| :--- | :--- | :--- |
| **User Participation** | Instant replication or copy-pasting of automated code/text. | Independent generation of structural logic sheets prior to prompting. |
| **AI Literacy** | Accepting outputs as definitive without source cross-examination. | Systematic auditing of model data biases, bounds, and confidence limits. |
| **Cognitive Shift** | Bypassing or disabling the switch when cognitive friction scales up. | Executing deep, multi-turn socratic cross-examinations to isolate logic breaks. |

---

## 5. Citation

If you adapt this methodology, deploy these custom configurations within academic infrastructure, or build upon the underlying pedagogical design, please cite the foundational research paper:

```bibtex
@article{yang2026ai,
  title={AI literacy mediates AI assisted diagnosis participation and critical thinking among medical students under supervision},
  author={Xin, Yang and Yan, Deng and Shuren, Luo and Minyang, Luo and Liuheng, Lu},
  journal={npj Digital Medicine},
  volume={9},
  number={344},
  pages={1--13},
  year={2026},
  publisher={Nature Publishing Group},
  doi={10.1038/s41746-026-02521-9}
}
```
