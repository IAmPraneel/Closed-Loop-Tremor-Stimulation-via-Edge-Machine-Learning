# Closed-Loop Tremor Stimulation via Edge Machine Learning

A local, closed-loop version for the **Felix Neural AI Wristband**, with multi-stage modeling.

### Why?
This approach provides **more freedom and flexibility** for users, especially useful in circumstances where:
- **Cloud connectivity** might be limited
- The **phone** is discharged or out of proximity

---

 Project3.ipynb has my attempt of simulating data through prompting LLMs, but I quickly realised simulating data without domain knowledge won't allow for meaningfull machine learning. Would love to continue this project on access to representative/actual data.

 Although tremor detection data might be available, but there is a lack of Stimulation data for further stage of modelling.

## My Approach/Understanding
## Tremor Detection and Stimulation

### Detection Stage

#### Spectral Analysis
- Detecting 4–12 Hz oscillations

#### Time Domain Features
- Zero crossing
- RMS (Root Mean Square)
- Variance

#### Detection Models
- Small RNN (Recurrent Neural Network) or Decision Tree for dynamic state detection

---

### Decision Logic

#### Personalized AI Analytics
- Context-aware adjustments
- Predictive modeling (e.g., tremor after certain activity?)

#### Dynamic Parameter Tuning
Adjust stimulation parameters based on:
- User tremor history
- Real-time response to stimulation
- AI "closed loop" optimization (likely reinforcement or rule-based tuning)

#### Peripheral Nerves Targeted
- Radial
- Median
- Ulnar

---

### Scientific Mechanism

1. **Desynchronization of central oscillatory networks** by disrupting rhythmic feedback
2. **Reflex Inhibition:** Activating certain motor pathways to suppress pathological tremor loops
3. **Neuroplastic tuning over time:** Possible long-term benefits through consistent stimulation

---

### Control Theory + Reinforcement Learning = Contextual Adaptation

---

## Logic Constructs

- Understand sequential context
- Model user-specific tremor patterns & response history

Decision-making includes:
- Which nerve to stimulate
- How much current to apply
- What timing to use
- Balance efficacy vs comfort/safety

---

## Algorithms

- RNN, LSTM (Long Short-Term Memory)
- Reinforcement Learning:
  - Deep RL, Deep Q-Networks
  - Q-learning
  - Proximal Policy Optimization (PPO)
  - DDPG: Deep Deterministic Policy Gradients for contextual adaptation

---

## Project Stages & Suggested Models

| **Stage** | **Task**                        | **Suggested Models**                                          |
| --------- | ------------------------------- | ------------------------------------------------------------ |
| **1**     | Tremor detection                 | Lightweight binary classifier: Decision Tree, TinyML, SVM    |
| **2**     | Severity/Frequency analysis     | RNN, LSTM, GRU, 1D CNN, or Clustering (e.g. DBSCAN)          |
| **3**     | Adaptive stimulation strategy   | Reinforcement Learning (PPO, DDPG), SNNs, or Transformers    |
|           |                                 | + Heuristic control blending for safety                      |

---

## Workflow Diagram

```plaintext
+---------------------------+
| 0. Data Input + Caching   |
| (IMU buffer, time series) |
+------------+--------------+
             |
             v
+---------------------------+
| 1. Tremor Detection       |
| (Low-power binary ML)     |
+------------+--------------+
             |
     If tremor detected
             v
+---------------------------+
| 2. Detailed Tremor        |
| Analysis (Severity, Freq, |
| Type - Regression/Clust.) |
+------------+--------------+
             |
             v
+---------------------------+
| 3. Adaptive Stimulation   |
| Algorithm (Context-aware, |
| RL / DL / Control logic)  |
+------------+--------------+
             |
             v
+---------------------------+
| 4. Stimulation Execution  |
| (Via Peripheral Hardware) |
+---------------------------+
