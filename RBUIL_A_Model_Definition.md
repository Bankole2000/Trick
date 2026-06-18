# R–B–U–I–L–A MODEL
## Canonical Definition

### Version 2.0

---

# Overview

The R–B–U–I–L–A model is the foundational engine of the TRICK game family.

It represents every communication event as a chain of transformations from reality to action, and back to a modified reality.

All TRICK games derive their mechanics from specific segments of this chain.

---

# Communication Chain

```
R → B → U → I → L → A → R'
```

Each arrow is a potential distortion point.

---

# Variable Definitions

## R — Reality

The actual state of the proposition. Ground truth, independent of any observer.

| Value | Meaning              |
| ----- | -------------------- |
| R = 1 | Proposition is true  |
| R = 0 | Proposition is false |

---

## B — Speaker Belief

What the speaker believes, independent of what reality is.

| Value | Meaning                             |
| ----- | ----------------------------------- |
| B = 1 | Speaker believes statement is true  |
| B = 0 | Speaker believes statement is false |

---

## U — Utterance

What the speaker actually communicates.

| Value | Meaning                   |
| ----- | ------------------------- |
| U = 1 | Speaker asserts statement |
| U = 0 | Speaker negates statement |

---

## I — Interpretation

How the listener decodes the utterance.

| Value | Meaning                                |
| ----- | -------------------------------------- |
| I = 1 | Listener interprets statement as true  |
| I = 0 | Listener interprets statement as false |

---

## L — Listener Belief

What the listener ultimately believes after interpretation.

| Value | Meaning                    |
| ----- | -------------------------- |
| L = 1 | Listener believes statement |
| L = 0 | Listener rejects statement |

---

## A — Listener Action

The observable behavior performed by the listener as a result of belief.

| Value | Meaning                                       |
| ----- | --------------------------------------------- |
| A = 1 | Action consistent with belief                 |
| A = 0 | No action, or action inconsistent with belief |

Examples of action: leaving a location, making a purchase, trusting a person, voting, investing, cooperating, defecting.

---

## R' — Updated Reality

Reality after listener action has been applied.

```
R' = f(R, A)
```

The update function f depends on context:

| System Type   | Reality Impact |
| ------------- | -------------- |
| Physical      | Negligible     |
| Social        | Strong         |
| Economic      | Medium         |
| Informational | Immediate      |

---

# Binary State Vector

Every communication event is encoded as:

```
(R, B, U, I, L, A)
```

With R' representing the resulting reality state after the loop closes.

---

# Fundamental Communication States

## Perfect Alignment

```
(1,1,1,1,1,1)  or  (0,0,0,0,0,0)
```

Reality is preserved through the entire chain. No distortion.

---

## Honest Mistake

```
(0,1,1,1,1,1)
```

Incorrect belief transmitted accurately. Speaker sincerely believes a falsehood.

---

## Lie

```
(1,1,0,0,0,0)
```

Speaker knows the truth. Communicates the opposite. Listener is deceived.

---

## Failed Lie

```
(1,1,0,0,1,1)
```

Speaker lies. Listener rejects the lie and arrives at truth.

---

## Misunderstanding

```
(1,1,1,0,0,0)
```

Speaker communicates accurately. Listener reconstructs incorrectly.

---

## Coincidental Correctness

```
(1,0,0,1,1,1)
```

Correct outcome through an incorrect reasoning chain.

---

## Belief Without Action

```
(1,1,1,1,1,0)
```

Listener believes correctly but does not act. Belief produces no consequence.

---

# Alignment Function

```
A(X, Y) = 1    if X = Y
A(X, Y) = 0    if X ≠ Y
```

---

# Communication Score (Base)

Measures alignment across the communication chain only.

```
S = A(R,B) + A(B,U) + A(U,I) + A(I,L) + A(R,L)
```

Range: 0 ≤ S ≤ 5

| Score | Meaning               |
| ----- | --------------------- |
| S = 5 | Perfect communication |
| S = 0 | Total breakdown       |

---

# Communication Score (Extended)

Includes belief-action consistency and reality stability after the action loop.

```
S' = S + A(L,A) + A(R, R')
```

Range: 0 ≤ S' ≤ 7

Additional terms:

| Term       | Meaning                          |
| ---------- | -------------------------------- |
| A(L, A)    | Belief-action consistency        |
| A(R, R')   | Reality stability after action   |

---

# Misunderstanding Metric

```
M  = 5 − S      (base: communication layers only)
M' = 7 − S'     (extended: includes action and reality update)
```

| Score  | Meaning                                                          |
| ------ | ---------------------------------------------------------------- |
| M = 0  | Perfect transmission                                             |
| M = 5  | Maximum distortion across communication                          |
| M' = 0 | Perfect alignment across the full belief-action loop             |
| M' = 7 | Maximum distortion including behavioral and environmental impact |

---

# Error Representation (Binary)

Each link in the chain can be expressed as a binary mismatch flag:

| Flag | Link         |
| ---- | ------------ |
| e1   | R ↔ B mismatch |
| e2   | B ↔ U mismatch |
| e3   | U ↔ I mismatch |
| e4   | I ↔ L mismatch |
| e5   | R ↔ L mismatch |

```
M = e1 + e2 + e3 + e4 + e5
```

---

# Future Extensions (Planned)

Additional variables under consideration:

| Variable | Meaning                    |
| -------- | -------------------------- |
| Q        | Questioning / Challenge trigger |
| T        | Trust                      |
| C        | Confidence                 |

Full extended state vector:

```
(R, B, U, I, L, A, Q, T, C)
```

---

Version: 2.0
Status: Canonical Model Reference
