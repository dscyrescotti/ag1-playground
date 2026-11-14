# Blocks — Lecture 12

Every block is a rule: **if you have everything under Needs, you may write the Say sentence and you then have everything under Gives.**

- **Definition** blocks come in pairs: `-unpack` (word → meaning) and `-pack` (meaning → word).
- **Fact** blocks go one way only.
- **Formal** is the block as a mathematical claim; **Proof** proves that claim.

Total: 9 blocks (3 Definition, 6 Fact).


---

## Weighted graphs and distances

### `weighted-digraph-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 12 |
| **Needs** | (G, ℓ) is a weighted digraph |
| **Gives** | G is a directed graph<br>every edge e has a length ℓ(e) ∈ ℝ, and a walk W has length ℓ(W) = Σ_{e∈W} ℓ(e) |
| **Formal** | (G, ℓ) weighted digraph ⟹ G directed ∧ ℓ : E → ℝ ∧ ℓ(W) = Σ_{e∈W} ℓ(e) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since (G, ℓ) is a weighted digraph, every edge e has a length ℓ(e), and the length of a walk is the sum of the lengths of its edges.” |
| **Source** | L12 slide 2 |

### `weighted-distance-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 12 |
| **Needs** | d(u, v) = k |
| **Gives** | some uv-path has length k, and every uv-path has length ≥ k (d(u, v) = +∞ if there is no uv-path) |
| **Formal** | d(u, v) := min{ℓ(P) : P a uv-path}, or +∞ if there is none |
| **Proof** | This is the definition, read in this direction. The minimum exists because a graph has finitely many paths. In a digraph d(u, v) and d(v, u) may differ. |
| **Say** | “Since d(u, v) = k, some uv-path has length k and no uv-path is shorter.” |
| **Source** | L12 slide 3 |

### `weighted-distance-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 12 |
| **Needs** | some uv-path has length k, and every uv-path has length ≥ k (d(u, v) = +∞ if there is no uv-path) |
| **Gives** | d(u, v) = k |
| **Formal** | (∃ uv-path of length k) ∧ (every uv-path has length ≥ k) ⟹ d(u, v) = k |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Some uv-path has length k and none is shorter, so d(u, v) = k.” |
| **Source** | L12 slide 3 |

### `positive-is-nonnegative`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 12 |
| **Needs** | all edge lengths are positive |
| **Gives** | all edge lengths are nonnegative |
| **Formal** | ℓ(e) > 0 ∀e ⟹ ℓ(e) ≥ 0 ∀e |
| **Proof** | Trivial. ∎ |
| **Say** | “Positive lengths are in particular nonnegative.” |
| **Source** | L12 slide 2 |

### `nonnegative-no-negative-cycle`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 12 |
| **Needs** | all edge lengths are nonnegative |
| **Gives** | G contains no negative cycle |
| **Formal** | ℓ ≥ 0 ⟹ no cycle C has ℓ(C) < 0 |
| **Proof** | The length of a cycle is a sum of nonnegative numbers. ∎ |
| **Say** | “With nonnegative lengths every cycle has nonnegative length, so there is no negative cycle.” |
| **Source** | L12 slide 29 |

### `walk-contraction`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 12 |
| **Needs** | G contains no negative cycle<br>W is a uv-walk in G |
| **Gives** | there is a uv-path P with ℓ(P) ≤ ℓ(W) |
| **Formal** | no negative cycle ∧ W a uv-walk ⟹ ∃ uv-path P with ℓ(P) ≤ ℓ(W) |
| **Proof** | If W is not a path, some vertex repeats; let t be the first such vertex (from u). Cut out the part of W between the first and the last occurrence of t. That part is a closed walk, which splits into cycles, none of them negative, so its length is ≥ 0 (with nonnegative lengths this is immediate). The result is a shorter-or-equal uv-walk with at least one edge fewer. Repeat until no vertex repeats: this gives a uv-path P with ℓ(P) ≤ ℓ(W). ∎ |
| **Say** | “Every uv-walk contains a uv-path that is not longer (Walk Contraction Lemma).” |
| **Source** | L12 slides 5–6 (nonnegative lengths); slide 30 (no negative cycle) |

### `shortest-walk-is-path`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 12 |
| **Needs** | G contains no negative cycle |
| **Gives** | a shortest uv-walk exists, and its length is d(u, v) |
| **Formal** | no negative cycle ∧ v reachable from u ⟹ min{ℓ(W) : W a uv-walk} = d(u, v) |
| **Proof** | Let P be a shortest uv-path. If some uv-walk W were shorter than P, walk-contraction would give a uv-path not longer than W, hence shorter than P — a contradiction. So P is a shortest uv-walk. ∎ |
| **Say** | “A shortest uv-walk exists and its length equals the length of a shortest uv-path, d(u, v).” |
| **Source** | L12 slide 7 |

### `triangle-inequality`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 12 |
| **Needs** | G contains no negative cycle |
| **Gives** | d(u, v) ≤ d(u, w) + d(w, v) for all vertices u, v, w |
| **Formal** | no negative cycle ⟹ ∀u, v, w: d(u, v) ≤ d(u, w) + d(w, v) |
| **Proof** | If d(u, w) or d(w, v) is +∞ there is nothing to prove. Otherwise join a shortest uw-path and a shortest wv-path: this is a uv-walk of length d(u, w) + d(w, v). By shortest-walk-is-path it is not shorter than d(u, v). ∎ |
| **Say** | “By the triangle inequality, d(u, v) ≤ d(u, w) + d(w, v).” |
| **Source** | L12 slide 8 (also slide 29) |

### `subpath-of-shortest-path`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 12 |
| **Needs** | P is a shortest uv-path and w is a vertex of P<br>d(u, v) ≤ d(u, w) + d(w, v) for all vertices u, v, w |
| **Gives** | the part of P from u to w is a shortest uw-path, and the part from w to v is a shortest wv-path |
| **Formal** | P shortest uv-path, w ∈ V(P) ⟹ P_uw shortest uw-path ∧ P_wv shortest wv-path |
| **Proof** | By the triangle inequality, ℓ(P) = d(u, v) ≤ d(u, w) + d(w, v) ≤ ℓ(P_uw) + ℓ(P_wv) = ℓ(P). So equality holds throughout, and since d(u, w) ≤ ℓ(P_uw) and d(w, v) ≤ ℓ(P_wv), both must be equalities: ℓ(P_uw) = d(u, w) and ℓ(P_wv) = d(w, v). ∎ |
| **Say** | “Every part of a shortest path is a shortest path between its ends.” |
| **Source** | L12 slide 9 |
