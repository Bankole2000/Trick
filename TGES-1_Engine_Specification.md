# TRICK GAME ENGINE SPECIFICATION (TGES-1)

---

## 1. Overview

TRICK is a communication-based game engine in which players exchange statements about reality and attempt to manage:

- Truth
- Belief
- Interpretation
- Trust
- Misunderstanding

All interactions are modeled through the R–B–U–I–L–A system.

For full model definitions see: `RBUIL_A_Model_Definition.md`

```
Reality → Belief → Utterance → Interpretation → Listener Belief → Action → R'
```

---

## 2. Core Principle

Every statement is a **transaction** in a model exchange system.

Players are not only evaluating truth, but:
- transmitting models
- interpreting models
- updating beliefs based on imperfect transmission
- acting on those beliefs and observing consequences

---

## 3. Core State Model

Each transaction is defined by the full R–B–U–I–L–A vector:

| Variable | Meaning                                    |
| -------- | ------------------------------------------ |
| R        | Reality (1 true / 0 false)                 |
| B        | Speaker belief                             |
| U        | Utterance (what is said)                   |
| I        | Listener interpretation                    |
| L        | Listener belief                            |
| A        | Listener action                            |
| R'       | Updated reality after action               |

### Communication Flow

```
R → B → U → I → L → A → R'
```

Each arrow is a potential distortion point.

---

## 4. Alignment Function

```
A(X, Y) = 1 if X == Y else 0
```

---

## 5. Scoring System

### Base Communication Score

```
S = A(R,B) + A(B,U) + A(U,I) + A(I,L) + A(R,L)
```

Range:
- 5 = perfect communication
- 0 = total breakdown

### Extended Score (Action Layer)

```
S' = S + A(L,A) + A(R, R')
```

Range:
- 7 = perfect alignment including action
- 0 = full distortion

### Misunderstanding Score

```
M  = 5 - S    (base)
M' = 7 - S'   (extended)
```

---

## 6. Core Gameplay Loop

Each round consists of:

### Phase 1: Card Draw / Statement Generation
A statement is introduced:
- from deck OR
- written by player (Joker mode)

Each card contains:
- proposition P
- truth value R (hidden in most modes)

---

### Phase 2: Speaker Action (U)
Player selects:
- Assert P
- Assert NOT P
- Bluff (optional mode)
- Pass

---

### Phase 3: Listener Action
Listener may:
- Accept
- Reject
- Question (Q=1)
- Challenge (force reveal)
- Request verification

---

### Phase 4: Resolution
Reveal R and evaluate:
- alignment scores
- deception detection
- interpretation accuracy

---

### Phase 5: Scoring

Points are awarded based on:

| Behavior                              | Reward    |
| ------------------------------------- | --------- |
| Accurate belief                       | + points  |
| Correct challenge                     | + bonus   |
| Successful deception (mode-dependent) | + points  |
| Misinterpretation avoided             | + points  |
| Misunderstanding (M)                  | penalty   |

---

## 7. Standard Challenge Scoring

| Outcome            | Points |
| ------------------ | ------ |
| Correct challenge  | +2     |
| Incorrect challenge | -1    |

Individual game modes may adjust these values to match their design goals.

---

## 8. Question Mechanic (Q Layer)

```
Q ∈ {0, 1}
```

- 0 = no challenge
- 1 = challenge/question triggered

If Q = 1:
- card must be revealed OR
- justification must be provided

---

## 9. Game Modes

### 9.1 PvP (Truth Duel)
Two players:
- one asserts
- one evaluates

Win condition:
- highest total score after N rounds

---

### 9.2 PvE (Reality Mode)
Player vs deck/system:
- system generates statements
- player evaluates truth

Focus:
- calibration training

---

### 9.3 Co-op Mode
Players collaborate:
- maximize shared accuracy score
- minimize misunderstanding (M)

Win condition:
- collective threshold S_avg ≥ target

---

### 9.4 PvPvE Mode
Players compete AND reality intervenes:
- deception allowed (mode-dependent)
- reality always resolves final truth

---

### 9.5 Mass Mode (Network Play)
Many players interacting:
- global statement pool
- distributed belief formation
- emergent consensus tracking

---

## 10. Card System Specification

Each card contains:

### Front:
- Statement P

### Hidden Data:
- R (truth value)
- explanation (optional)

### Optional Fields:
- category (science, social, self, myth)
- difficulty level
- ambiguity level

---

## 11. Special Card Types

### 11.1 Joker Card (Creation Mode)
Player writes:
- a statement
- assigns truth value (or guesses it if challenge mode)

Used for:
- creativity
- bluffing
- self-testing

---

### 11.2 Mirror Card
Forces player to:
- repeat opponent's statement under transformation

---

### 11.3 Paradox Card
Allows:
- contradiction statements
- inversion logic

---

## 12. Digital Engine Architecture

### Core Objects

#### Player Object

```
Player {
  belief_state: binary vector,
  score: int,
  trust_map: dict[player_id → float],
}
```

---

#### Statement Object

```
Statement {
  proposition: string,
  R: 0|1,
  category: enum,
}
```

---

#### Transaction Object

```
Transaction {
  R, B, U, I, L, A,
  Q,
  score_S,
  score_S_prime,
  mismatch_M,
  mismatch_M_prime,
}
```

---

### Engine Loop

```
for each round:
  generate_statement()
  speaker_action()
  listener_action()
  resolve_Q()
  compute_RBUILA()
  compute_scores()
  resolve_action()
  update_reality()
  update_players()
```

---

## 13. Win Conditions

Depending on mode:

### Competitive
- highest score S_total

### Cooperative
- lowest average M

### Calibration Mode
- best statistical alignment over time

---

## 14. Core Design Insight

TRICK is not just a game.

It is a simulation of:

> How minds exchange models of reality through language under uncertainty, and how those models—when acted upon—reshape the world they described.

It models:
- truth transmission
- belief formation
- misunderstanding
- persuasion
- deception
- interpretation error
- belief-driven action
- reality feedback

---

## 15. Philosophical Interpretation

At its deepest level:

- Reality is a constraint (R)
- Minds are model generators (B, L)
- Language is transmission (U)
- Interpretation is reconstruction (I)
- Action is consequence (A)
- Updated reality is the world reshaped by belief (R')

Communication is:

> A lossy transmission of reality through multiple cognitive transformations, culminating in behavior that modifies the world being described.

---

END SPECIFICATION
