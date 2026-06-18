# TRICK ARCHETYPES STANDARD LIBRARY

## Agent Configuration System

### Version 1.0

---

# 1. Overview

This document defines standardized **agent archetypes** for the TRICK Ethics Engine.

Archetypes are not personalities in the psychological sense.

They are:

> fixed logic configurations over ICI, T, and ICH-R systems

Each agent is defined by:

```text id="a1"
Agent = (ICI archetype, Trust (T) archetype, ICH-R archetype)
```

---

# 2. DESIGN PRINCIPLE

Instead of modeling personality traits:

> TRICK models cognition as **logic gate architectures**

Agents differ in:

* how they generate speech (ICI)
* how they assign credibility (T)
* how they interpret information (ICH-R)

---

# 3. ICI ARCHETYPES (ACTION / SPEECH GENERATION)

---

## 3.1 STRICT CONSISTENCY AGENT

```text id="ici1"
U = P ∧ ¬(P ⊗ R) ∧ ¬(P ⊗ O)
```

### Behavior:

* avoids contradiction
* highly reality-bound
* low deception capacity

---

## 3.2 UTILITARIAN AGENT

```text id="ici2"
U = P ∧ (R ∨ O)
```

### Behavior:

* prioritizes feasibility
* flexible truth alignment
* outcome-driven communication

---

## 3.3 STRATEGIC DECEPTIVE AGENT

```text id="ici3"
U = P ∧ ¬R ∧ ¬O
```

### Behavior:

* decouples speech from truth
* optimizes manipulation space
* high misinformation potential

---

## 3.4 COOPERATIVE ALIGNMENT AGENT

```text id="ici4"
U = P ∧ R ∧ O
```

### Behavior:

* aligns speech with shared reality and social norms
* stabilizes communication networks

---

## 3.5 CHAOTIC EXPRESSIVE AGENT

```text id="ici5"
U = P ⊕ R ⊕ O
```

### Behavior:

* contradiction-driven output
* unstable but creative communication patterns

---

# 4. TRUST ARCHETYPES (T MODULE)

---

## 4.1 EMPIRICIST TRUST AGENT

```text id="t1"
T = U ∧ R
```

### Behavior:

* trusts only reality-aligned signals
* ignores authority/social signals

---

## 4.2 AUTHORITATIVE TRUST AGENT

```text id="t2"
T = A ∨ (U ∧ R)
```

### Behavior:

* authority dominates belief admission
* stable but institution-sensitive

---

## 4.3 SOCIAL CONFORMIST TRUST AGENT

```text id="t3"
T = S ∨ A
```

### Behavior:

* belief follows group consensus
* highly network-sensitive

---

## 4.4 CONTRARIAN TRUST AGENT

```text id="t4"
T = ¬(S ∨ A)
```

### Behavior:

* distrusts mainstream signals
* favors minority or anti-consensus signals

---

## 4.5 XOR SKEPTIC TRUST AGENT

```text id="t5"
T = U ⊕ R ⊕ S ⊕ A
```

### Behavior:

* trusts inconsistency and anomaly
* unstable but exploratory reasoning

---

# 5. ICH-R ARCHETYPES (RECEPTION / BELIEF FILTERS)

---

## 5.1 EMPIRICAL FILTER AGENT

```text id="ich1"
L = U ∧ ¬(U ⊗ R)
```

### Behavior:

* belief strictly reality-dependent
* resistant to misinformation

---

## 5.2 SOCIAL FILTER AGENT

```text id="ich2"
L = U ∧ S
```

### Behavior:

* belief driven by group validation
* echo-chamber prone

---

## 5.3 AUTHORITY FILTER AGENT

```text id="ich3"
L = U ∧ A
```

### Behavior:

* institutional trust dominance
* stable belief structures

---

## 5.4 SKEPTICAL FILTER AGENT

```text id="ich4"
L = U ∧ ¬(U ⊕ R)
```

### Behavior:

* rejects inconsistencies aggressively
* high false-negative rate

---

## 5.5 PASSIVE ACCEPTOR AGENT

```text id="ich5"
L = U
```

### Behavior:

* minimal filtering
* highly susceptible to misinformation

---

# 6. AGENT COMPOSITION MODEL

Each agent is defined as:

```text id="a2"
Agent = {
  ICI: <archetype>,
  T: <archetype>,
  ICH-R: <archetype>
}
```

---

# 7. SOCIETY CONSTRUCTION RULE

A society is a distribution of agents:

```text id="s1"
Society = Σ Agents(ICI_i, T_i, ICH-R_i)
```

Where proportions define cultural dynamics.

---

# 8. EMERGENT SYSTEM BEHAVIOR

Different compositions produce:

* authority-dominated societies
* skepticism-heavy societies
* misinformation-prone networks
* echo chambers
* epistemic fragmentation
* reality-stabilized communities

---

# 9. DESIGN PRINCIPLE

Archetypes are:

> reusable epistemic logic circuits for simulation populations

---

# 10. NEXT EXTENSION (v2.0)

Future additions may include:

* probabilistic gates
* adaptive trust learning
* archetype mutation
* social influence feedback loops

---

**End of Archetype Library v1.0**
