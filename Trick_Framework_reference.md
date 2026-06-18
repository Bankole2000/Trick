# TRICK FRAMEWORK REFERENCE

## Version 1.0

---

# Overview

TRICK is a family of epistemic games built around a common communication engine.

The framework models how reality, belief, language, interpretation, and understanding interact.

At its foundation lies the R–B–U–I–L–A model:

Reality → Belief → Utterance → Interpretation → Listener Belief -> Listener Action

Each game within the TRICK family emphasizes different portions of this process.

---

# TRICK PROJECT TODO LIST

## Phase 1 — Core Game Expansion

### Deck and Rules Development

* [ ] Expand deck system and game variants
* [ ] Formalize category ratios
* [ ] Define difficulty tiers
* [ ] Design misunderstanding-density balancing
* [ ] Create modular deck families
* [ ] Complete ANCHOR deck
* [ ] Complete ECHO deck
* [ ] Complete GLITCH deck
* [ ] Complete MIRROR deck
* [ ] Complete SPELLS deck
* [ ] Complete PARADOX deck
* [ ] Complete PRAXIS deck

---

## Phase 2 — Digital Prototype

### Engine Development

* [ ] Implement R–B–U–I–L–A engine
* [ ] Implement transaction logging
* [ ] Build turn-based game loop
* [ ] Add scoring systems
* [ ] Add challenge system
* [ ] Implement multiplayer state management
* [ ] Build basic UI
* [ ] Support deck plug-ins

---

## Phase 3 — AI Simulation Layer

### Multi-Agent Experiments

* [ ] Use LLM agents as players
* [ ] Simulate belief formation
* [ ] Simulate misinformation spread
* [ ] Simulate consensus formation
* [ ] Test epistemic stability
* [ ] Run society-scale simulations
* [ ] Compare game variants under AI populations

---

# TRICK GAME FAMILY

All games share the same engine but focus on different psychological and epistemic phenomena.

| Game    | Focus          | Primary Layer |
| ------- | -------------- | ------------- |
| ANCHOR  | Reality        | R → L         |
| ECHO    | Consensus      | R → B → L     |
| GLITCH  | Cognitive Bias | R → B         |
| MIRROR  | Interpretation | U → I         |
| SPELLS  | Influence      | U → L         |
| PRAXIS  | Behaviour      | R -> A        |
| PARADOX | Self-Reference | Entire System |

---

# R–B–U–I–L–A MODEL

## Definitions

### R — Reality

The actual state of the proposition.

Examples:

Statement:
"The Earth orbits the Sun."

Reality:
True

R = 1

---

### B — Speaker Belief

What the speaker believes.

B = 1
Speaker believes statement is true.

B = 0
Speaker believes statement is false.

---

### U — Utterance

What the speaker communicates.

U = 1
Speaker asserts statement.

U = 0
Speaker negates statement.

---

### I — Interpretation

How the listener interprets the utterance.

I = 1
Listener interprets statement as true.

I = 0
Listener interprets statement as false.

---

### L — Listener Belief

What the listener ultimately believes after interpretation.

L = 1
Listener believes statement.

L = 0
Listener rejects statement.

---

### A — Listener Action

What the listener ultimately acts out after belief.

A = 1
Listener acts according to belief.

A = 0
Listener acts in opposition to belief.

---

# Binary Representation

Every communication event becomes a binary vector:

(R, B, U, I, L, A)

Example:

Reality:
True

Speaker believes:
True

Speaker says:
True

Listener interprets:
True

Listener believes:
True

Listener acts:
True

Vector:

(1,1,1,1,1,1)

Perfect alignment.

---

# Fundamental Binary States

## Perfect Alignment

Reality is preserved through the entire chain.

Vector:

(1,1,1,1,1,1)

or

(0,0,0,0,0,0)

Meaning:

No distortion.

---

## Honest Mistake

Reality is false.

Speaker sincerely believes it.

Vector:

(0,1,1,1,1)

Meaning:

Incorrect belief transmitted accurately.

---

## Lie

Reality is true.

Speaker knows this.

Speaker communicates the opposite.

Vector:

(1,1,0,0,0)

Meaning:

Intentional distortion.

---

## Failed Lie

Speaker lies.

Listener rejects lie.

Vector:

(1,1,0,0,1)

Meaning:

Attempted deception fails.

---

## Misunderstanding

Speaker communicates accurately.

Listener reconstructs incorrectly.

Vector:

(1,1,1,0,0)

Meaning:

Transmission failure.

---

## Coincidental Correctness

Speaker believes falsehood.

Listener ultimately arrives at truth.

Vector:

(1,0,0,1,1)

Meaning:

Correct outcome through incorrect reasoning.

---

# Misunderstanding Metric

Define alignment function:

A(X,Y) = 1 if X = Y

A(X,Y) = 0 if X ≠ Y

---

Communication Score:

S =
A(R,B)
+
A(B,U)
+
A(U,I)
+
A(I,L)
+
A(R,L)

Range:

0 ≤ S ≤ 5

---

Misunderstanding Score:

M = 5 − S

Where:

M = 0

Perfect transmission

M = 5

Maximum distortion

---

# Extended Binary Layer (Future)

Future versions may introduce:

Q = Questioning

T = Trust

C = Confidence

Resulting in:

(R,B,U,I,L,Q,T,C)

This would allow the engine to model:

* uncertainty
* challenge behavior
* reputation
* confidence calibration

in addition to truth transmission.

---

# Framework Principle

The TRICK framework assumes that communication is not merely the transfer of information.

Communication is a transformation process.

Reality becomes belief.

Belief becomes language.

Language becomes interpretation.

Interpretation becomes belief.

Each stage introduces opportunities for:

* understanding
* misunderstanding
* persuasion
* distortion
* discovery

The various TRICK games explore different regions of this process.

---

Version: 1.0

Status: Framework Reference Document
