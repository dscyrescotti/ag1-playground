# Technique blocks

A technique is a reasoning move that connects fact blocks. Nothing in the statement forces it; you pick it when the facts alone do not reach the goal.

## `contradiction`

| | |
|---|---|
| **Use when** | The goal is negative (“no…”, “cannot…”, “at most…”), or the direct way gives nothing to work with. |
| **Skeleton** | For the sake of contradiction, suppose [negation of the goal]. Then … . This contradicts [earlier fact]. Hence [goal]. |

## `case-split`

| | |
|---|---|
| **Use when** | The objects can be in a few different situations and no single argument covers all. |
| **Skeleton** | We distinguish two cases. Case 1: … . Case 2: … . In both cases [goal]. (The cases must cover everything.) |

## `induction`

| | |
|---|---|
| **Use when** | A claim for all n (or all steps of an algorithm), where an object of size n contains one of size n − 1. |
| **Skeleton** | By induction on n. Base (n = n₀): … . Step: let n > n₀ and assume the claim holds for n − 1 (induction hypothesis). … Hence it holds for n. |

## `pigeonhole`

| | |
|---|---|
| **Use when** | More objects than possible values; you want two objects that share something. |
| **Skeleton** | There are N objects but at most N − 1 possible values of … . By the pigeonhole principle, two objects have the same value. |

## `double-counting`

| | |
|---|---|
| **Use when** | A formula linking two quantities (degrees and edges, …). |
| **Skeleton** | Count the pairs (v, e) with v ∈ e in two ways. By vertices: … . By edges: … . Comparing the two counts gives … . |

## `extremal-choice`

| | |
|---|---|
| **Use when** | You need an object with a special property and nothing in the statement hands it to you. |
| **Skeleton** | Let X be a shortest/longest/minimal/maximal … (it exists, since there are finitely many). Suppose X did not have [property]. Then we could construct a shorter/longer one — a contradiction. |

## `construct-and-verify`

| | |
|---|---|
| **Use when** | The frame is exists. |
| **Skeleton** | Let V = {…} and E = {…}. Then: [property 1] holds because … ; [property 2] holds because … . |

## `wlog`

| | |
|---|---|
| **Use when** | The situation is symmetric (two vertices, two parts, two layers). |
| **Skeleton** | Without loss of generality k ≤ ℓ (otherwise swap the roles of u and w). |

## `termination`

| | |
|---|---|
| **Use when** | Prove that an algorithm stops. |
| **Skeleton** | Each [vertex/edge] is [enqueued/processed] at most once, and each iteration of the loop [removes/processes] one. Hence the loop runs at most [bound] times. |

## `pass-to-complement`

| | |
|---|---|
| **Use when** | Degrees are large, or the statement has a mirror version (0 ↔ n − 1, adjacent ↔ non-adjacent). |
| **Skeleton** | Consider the complement Ḡ. By complement-degree, [degree d in G] becomes [n − 1 − d in Ḡ], so the claim for G follows from the already proved claim for Ḡ. |

## `parity`

| | |
|---|---|
| **Use when** | Odd/even appears in the statement (odd degree, odd cycle, path of odd length). |
| **Skeleton** | The quantity … is even because … , but it is also odd because … — a contradiction. / Each step changes the parity, so after k steps … . |
