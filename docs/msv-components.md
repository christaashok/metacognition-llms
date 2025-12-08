# MSV Components and Mathematical Framework

This section details the **five components** of the Metacognitive State Vector (MSV), each quantifying a distinct cognitive dimension inspired by animal and human metacognition literature.

---

## Emotional Response (ER)

Represents affective intensity across multiple emotion categories.

$$
ER = \{(e_1, v_1), (e_2, v_2), \ldots, (e_n, v_n)\}
$$

where each \(e_i\) is an emotion type and \(v_i \in [0, 100]\) is its normalized strength.  
High ER accelerates **System 2** activation, prioritizing emotionally charged content.

---

## Correctness Evaluation (CE)

Weighted sum of logical, factual, and contextual validity.

$$
CE = \alpha_1 F_1(\text{logical consistency}) + \alpha_2 F_2(\text{factual accuracy}) + \alpha_3 F_3(\text{contextual appropriateness})
$$

\(\alpha_i\) are context-dependent weights, summing to 1.  
Low CE triggers System 2 intervention and additional verification.

---

## Experiential Matching (EM)

Measures alignment with prior knowledge and history.

$$
EM = \omega_1 K(\text{response}, \text{knowledge base}) + \omega_2 S(\text{response}, \text{historical responses})
$$

Low EM indicates novelty → triggers exploration or retrieval;  
High EM → reinforces confidence in existing knowledge.

---

## Conflicting Information (CI)

Quantifies internal and external inconsistency.

$$
CI = \delta_1 D(\text{internal consistency}) + \delta_2 D(\text{source agreement}) + \delta_3 D(\text{temporal stability})
$$

High CI signals contradiction → invokes System 2 analysis.

---

## Problem Importance (PI)

Captures urgency and impact of the problem.

$$
PI = \max(\beta_1 C(\text{consequence}) + \beta_2 U(\text{temporal urgency}) + \beta_3 I(\text{scope of impact}))
$$

High PI → allocates greater cognitive and compute resources.

---

## Overall MSV

$$
MSV = (ER, CE, EM, CI, PI)
$$

Each dimension maps to a **trigger policy** determining when to escalate from System 1 (fast) to System 2 (deliberate).

---

### Key Literature

- Maniscalco & Lau (2012). *Consciousness and Cognition.*  
- Fleming & Frith (2014). *The Cognitive Neuroscience of Metacognition.*  
- Hampton (2001). *PNAS.*  
- Foote & Crystal (2007). *Current Biology.*
