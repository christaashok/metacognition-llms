# Journal Paper Literature Review

## Overview

This section focuses on how **metacognition** and **self-awareness** are defined, measured, and operationalized across both biological and artificial systems, grounding our theoretical and computational framework.

Two constructs are central:
1. **Self-awareness** — self–other discrimination and *body-as-self* representation (mirror tests, body-as-obstacle, olfactory mirrors).
2. **Metacognition** — *monitoring* and *control* of one’s cognitive states (uncertainty, opt-out, information-seeking, wagering).

Evidence across species shows variability by modality: primates show strong uncertainty monitoring; dolphins, elephants, and magpies demonstrate visual self-recognition; dogs show olfactory self-recognition; and cleaner wrasse fish exhibit modified MSR behavior.

For LLMs, these constructs map to:
- **Self-awareness analogs:** self-modeling, identity persistence, embodiment constraints  
- **Metacognition analogs:** calibration, confidence estimation, control processes

Signal-detection–based metrics (meta-d′, Mratio) provide more robust quantification than accuracy-only proxies.

---

## Definition of Self-Awareness in Animals

- **Gallup (1970, Science):**  
  Established the mirror self-recognition (MSR) test — self-directed behavior when viewing a mirror after being covertly marked.

- **Gallup (1998, Behavioral Processes):**  
  Expanded self-awareness beyond mirrors to include *body-as-self* representations.

- **Horowitz (2017, Behavioural Processes):**  
  Developed the *olfactory mirror* paradigm for dogs, introducing modality-specific self-awareness testing.

---

## Definition of Metacognition in Animals

- **Smith, Shields, & Washburn (2003, BBS):**  
  Defined animal metacognition as the capacity for *monitoring* and *control* over cognitive states via uncertainty responses, information-seeking, and wagering.

- **Fleming & Frith (2014, Springer):**  
  Canonical modern definition: “cognition about cognition,” with *monitoring* (confidence, error detection) and *control* (strategy adjustment, information-seeking).

- **Maniscalco & Lau (2012, Consciousness and Cognition):**  
  Introduced quantitative estimation of metacognitive sensitivity using **Type-2 SDT (meta-d′)**.

---

## Metacognition: Monitoring and Control

**Monitoring** = sensing your internal state (confidence, uncertainty, error detection).  
**Control** = acting on that state (adjust strategy, seek info, abstain).

### Monitoring Components
1. **Confidence:** probability of correctness  
2. **Uncertainty:** awareness of not knowing  
3. **Error Detection:** recognizing mistakes  
4. **Feeling of Knowing (FOK):** prediction of future recall  
5. **Judgment of Learning (JOL):** prediction of memory retention

### Control Components
1. **Strategy Adjustment:** change behavior based on uncertainty  
2. **Information Seeking:** gather additional data when unsure  
3. **Response Withholding:** abstain on low-confidence tasks  
4. **Effort Allocation:** invest more resources when needed

---

## Quantification Framework

Metacognitive monitoring is formalized via **Type-2 Signal Detection Theory**.

### Type-2 SDT Overview

1. **Primary task (Type-1):**
   Compute sensitivity:
   $$
   d' \approx \sqrt{2}\,\Phi^{-1}(p_{\text{correct}})
   $$

2. **Confidence ratings:** classify as “high” or “low”.

3. **Type-2 ROC curve:**
   - Type-2 hit = high confidence + correct  
   - Type-2 false alarm = high confidence + incorrect  
   Compute AUROC₂ as the area under this curve.

4. **meta-d′ (Maniscalco & Lau, 2012):**
   - Fit a model to reproduce the observed Type-2 ROC.
   - Converts metacognitive sensitivity to the same scale as d′.

5. **Mratio (efficiency):**
   $$
   \text{Mratio} = \frac{\text{meta-}d'}{d'}
   $$
   Adjusts for task difficulty.

6. **Hierarchical HMeta-d (Fleming, 2017):**  
   A Bayesian extension for small sample sizes or limited trials.

---

## Mapping Metacognition to LLMs

| Animal Paradigm | Description | LLM Analog |
|-----------------|--------------|-------------|
| Uncertainty / Opt-Out | Skip hard trials when unsure | Abstain or defer output |
| Information Seeking | Actively check when missing info | Trigger retrieval / tool use |
| Wagering / Time | Bet or invest time proportional to confidence | Adjust compute / reasoning steps |

Metrics like **AUROC₂**, **meta-d′**, and **Mratio** can quantify an LLM’s introspective calibration similarly to animals.

---

## Summary

Metacognition involves *monitoring* (sensing correctness) and *control* (acting on that signal).  
These functions have clear computational analogs in LLMs through confidence estimation, abstention, and adaptive reasoning, allowing the **Metacognitive State Vector (MSV)** to serve as a bridge between biological cognition and machine introspection.
