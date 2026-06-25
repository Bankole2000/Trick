# TRICK COSTUME LAYER FRAMEWORK

## Identity Presentation Extension

### Version 0.1

---

# Purpose

This document introduces the Costume Layer (K) to the TRICK Framework.

The Costume Layer models how an agent presents themselves to other agents.

Examples include:

* clothing
* uniforms
* credentials
* social roles
* titles
* branding
* reputation signals
* disguises
* symbolic authority

The Costume Layer acts as a bridge between:

* biological agents
* symbolic identities

and therefore connects the TRICK simulation engine to the Hunter-Gatherer Magic Theory.

---

# Core Insight

Agents do not interact solely as biological organisms.

They interact through presented identities.

A listener often evaluates:

```text
Who is speaking?
```

before evaluating:

```text
What is being said?
```

The Costume Layer models this phenomenon.

---

# Position in the Framework

Current:

```text
R → B → U → T → I → P → L → A
```

Proposed:

```text
R → B → U → K → T → I → P → L → A
```

Where:

```text
K = Costume
```

---

# Interpretation A

## Modification Model

This model asks:

> Is the presentation direct or modified?

---

## Binary Definition

| K | Meaning                          |
| - | -------------------------------- |
| 0 | Direct / unmodified presentation |
| 1 | Modified / mediated presentation |

---

## Examples

### K = 0

* speaking as oneself
* no title
* no uniform
* anonymous interaction

---

### K = 1

* doctor coat
* military uniform
* business suit
* royal regalia
* religious attire
* company branding
* online avatar
* disguise

---

# Binary Table A

| Presentation | K |
| ------------ | - |
| Direct       | 0 |
| Modified     | 1 |

---

# Interpretation

The modification model does not judge truthfulness.

It merely identifies whether symbolic presentation is being used.

---

# Examples

| Case                      | K |
| ------------------------- | - |
| Doctor wearing coat       | 1 |
| Impersonator wearing coat | 1 |
| Judge wearing robe        | 1 |
| Actor in costume          | 1 |
| Anonymous citizen         | 0 |

---

# Interpretation B

## Authenticity Model

This model asks:

> Is the presented identity genuine?

---

## Binary Definition

| K | Meaning                          |
| - | -------------------------------- |
| 0 | Inauthentic / false presentation |
| 1 | Authentic / genuine presentation |

---

## Binary Table B

| Presentation | K |
| ------------ | - |
| Genuine      | 1 |
| Pretending   | 0 |

---

# Examples

### K = 1

* licensed doctor presenting as doctor
* judge presenting as judge
* elected official presenting as official
* authentic expert

---

### K = 0

* impersonator
* forged credentials
* false identity
* fraudulent authority

---

# Comparison of the Two Models

The same situation may be encoded differently.

---

## Doctor Example

Actual doctor wearing a lab coat.

| Model        | Value |
| ------------ | ----- |
| Modification | 1     |
| Authenticity | 1     |

---

## Impersonator Example

Scammer wearing a lab coat.

| Model        | Value |
| ------------ | ----- |
| Modification | 1     |
| Authenticity | 0     |

---

## Anonymous Citizen

No costume.

| Model        | Value |
| ------------ | ----- |
| Modification | 0     |
| Authenticity | 1     |

---

# Dual Costume Encoding

Future versions may support:

```text
KM = Modification
KA = Authenticity
```

---

## State Space

Two binary variables:

```text
KM
KA
```

produce:

```text
2² = 4 states
```

---

# Dual Costume Table

| KM | KA | Interpretation              |
| -- | -- | --------------------------- |
| 0  | 0  | False direct presentation   |
| 0  | 1  | Genuine direct presentation |
| 1  | 0  | Deceptive costume           |
| 1  | 1  | Genuine costume             |

---

# Costume and Trust

Costume directly influences Trust.

Example:

```text
T = K AND Authority
```

or

```text
T = Authority XOR K
```

depending on archetype.

---

# Costume and ICH-R

Listeners may evaluate messages differently based on costume.

Examples:

* authority bias
* prestige bias
* celebrity effect
* institutional trust
* credentialism

---

# Costume and Parry

Costume may reduce challenges.

Example:

```text
K = 1
```

can cause:

```text
P ↓
```

because listeners assume legitimacy.

---

# Costume Archetypes

## The Uniform

Uses symbolic markers of authority.

---

## The Expert

Uses credentials and reputation.

---

## The Performer

Uses theatrical presentation.

---

## The Merchant

Uses branding and status signaling.

---

## The Impersonator

Uses deceptive presentation.

---

## The Anonymous

Minimizes symbolic presentation.

---

# Relationship to Hunter-Gatherer Magic Theory

The Costume Layer represents the "costume" portion of:

> Humans are animals in costumes playing a game of hunter-gatherer using magic tricks.

Where:

* Animal = biological agent
* Costume = identity presentation
* Magic = symbolic communication
* Hunter-Gatherer = resource acquisition

---

# Core Insight

The Costume Layer models a simple observation:

People often respond not only to information itself, but to the identity through which the information is presented.

Costume therefore acts as a symbolic filter between communication and trust.

---

**End of TRICK Costume Layer Framework v0.1**
