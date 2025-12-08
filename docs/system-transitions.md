# System 1 ↔ System 2 Transitions

## Dual-Process Cognitive Model

We model the interaction between **System 1 (fast, intuitive)** and **System 2 (slow, reflective)** using principles from dual-process theory (Stanovich, 2008).

- **System 1** → automatic, heuristic, bagged ensemble  
- **System 2** → deliberate, analytical, boosted ensemble  

This mapping captures the dynamic interplay between *intuition* and *reasoning* in both humans and LLMs.

---

## Role Transition Dynamics

Let \( G(V, E, W(M)) \) represent the LLM ensemble graph:
- \(V\) = nodes (agents)
- \(E\) = edges (communication)
- \(W(M)\) = weights determined by the Metacognitive State Vector \(M = (ER, CE, EM, CI, PI)\)

Each node’s role (e.g., *Domain Expert*, *Critic*, *Evaluator*, *Synthesizer*) is assigned dynamically based on MSV-weighted optimization.

The formal role transition framework is:

$$
\Gamma = (R, S, T, M)
$$

where  
\(R = \{r_1, ..., r_k\}\) → roles  
\(S = \{s_1, ..., s_n\}\) → states  
\(T: R \times S \rightarrow P(R)\) → allowable transitions  

---

## Transition Triggers

System 2 activation occurs when any of the following thresholds are met:

- \(CE < \tau_{CE}\) → low correctness  
- \(CI > \tau_{CI}\) → high conflict  
- \(PI > \tau_{PI}\) → high importance  
- \(ER > \tau_{ER}\) → strong emotional salience  

When triggered, additional ensemble nodes engage in reflective evaluation or deeper analysis.

---

## Graph-Theoretic Interpretation

Ensemble roles evolve according to a weighted adjacency matrix driven by MSV values.  
Edges strengthen between nodes with complementary confidence and disagreement profiles.  
This enables dynamic self-organization and *distributed metacognition* across agents.

---

## Summary

These transition mechanisms implement a computational analogue of **System 1 ↔ System 2 reasoning**:
- Quick, automatic responses escalate to deliberate, self-aware processing when metacognitive thresholds demand it.  
- This dynamic forms the theoretical backbone for quantifying machine self-reflection.
