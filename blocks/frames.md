# Frame blocks

A frame is the outer shell of the proof: its first and last line. **The form of the question decides the frame — you do not choose it.**

## `for-all`

| | |
|---|---|
| **Trigger** | “Prove that every X has property Q”, “Let G be … . Prove …” |
| **Open with** | Let X be arbitrary (with the given properties). |
| **Close with** | Since X was arbitrary, the claim holds for every X. ∎ |
| **Note** | Never pick a concrete example. Everything you use about X must come from a GIVEN block. |

## `exists`

| | |
|---|---|
| **Trigger** | “Prove that there exists …”, “Find a graph such that …” |
| **Open with** | Consider the following object: … (give V and E explicitly, or name it: Kₙ, Cₙ, …). |
| **Close with** | It has the required properties, because … (check each one). ∎ |
| **Note** | One example is enough, but you must verify every required property. |

## `not-exists`

| | |
|---|---|
| **Trigger** | “Prove that no graph … exists” |
| **Open with** | For the sake of contradiction, suppose such a graph G exists. |
| **Close with** | This is a contradiction; hence no such graph exists. ∎ |
| **Note** | Unpack every property of the supposed G with blocks until two facts clash. |

## `decide`

| | |
|---|---|
| **Trigger** | “Decide whether …”, “Find … or prove that it does not exist”, “Can it happen that …” |
| **Open with** | State the answer first: “Yes, such a graph exists.” / “No, such a graph does not exist.” |
| **Close with** | Then continue with the frame exists or not-exists. |
| **Note** | Try small examples and the necessary conditions (degree-bounds, degree-sum, handshaking) to guess the answer. |

## `true-or-false`

| | |
|---|---|
| **Trigger** | “Decide if it is true or false: …” (a general statement) |
| **Open with** | True: use the frame for-all. False: “The statement is false. Counterexample: …” |
| **Close with** | …so the counterexample satisfies the assumption but not the conclusion. ∎ |
| **Note** | A counterexample is a single concrete graph; check both that it satisfies the assumption and that it violates the conclusion. |

## `if-and-only-if`

| | |
|---|---|
| **Trigger** | “Prove that A if and only if B”, “A ⟺ B” |
| **Open with** | (⇒) Suppose A. … Hence B. |
| **Close with** | (⇐) Suppose B. … Hence A. ∎ |
| **Note** | Two separate proofs. The given blocks of one direction are the goal blocks of the other. |

## `for-which`

| | |
|---|---|
| **Trigger** | “For which n does there exist …” |
| **Open with** | Claim: such a graph exists if and only if n ∈ {…}. |
| **Close with** | For n in the set: frame exists. For all other n: frame not-exists. ∎ |
| **Note** | Both halves are needed: constructions for the good n, impossibility for the bad n. |

## `equality`

| | |
|---|---|
| **Trigger** | “Prove that a = b”, “Determine d(s,t)”, “What is the maximum …” |
| **Open with** | (≤) … (exhibit an object achieving the value). |
| **Close with** | (≥) … (show nothing better is possible). Hence a = b. ∎ |
| **Note** | Maximum/minimum questions always need both: an example reaching the value, and a proof that it cannot be beaten. |

## `set-equality`

| | |
|---|---|
| **Trigger** | “Prove that X = Y”, “… are exactly those that …” |
| **Open with** | (⊆) Let x ∈ X. … Hence x ∈ Y. |
| **Close with** | (⊇) Let y ∈ Y. … Hence y ∈ X. ∎ |
| **Note** | The word “exactly” in a statement signals this frame. |

## `count`

| | |
|---|---|
| **Trigger** | “Find the number of …”, “How many …” |
| **Open with** | Each object is determined by the following choices: … |
| **Close with** | The choices are independent, so the number is (product). Every choice gives a valid object and different choices give different objects. ∎ |
| **Note** | State why nothing is counted twice and nothing is missed. |

## `algorithm`

| | |
|---|---|
| **Trigger** | “Design an algorithm to …” |
| **Open with** | Model: define the graph (vertices = …, edges = …). Algorithm: run … on it and output … . |
| **Close with** | Correctness: … (cite the algorithm's correctness blocks). Time: … . ∎ |
| **Note** | Four parts, always in this order: model, algorithm, correctness, complexity. |
