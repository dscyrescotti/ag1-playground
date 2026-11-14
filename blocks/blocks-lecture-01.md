# Blocks — Lecture 1

Every block is a rule: **if you have everything under Needs, you may write the Say sentence and you then have everything under Gives.**

- **Definition** blocks come in pairs: `-unpack` (word → meaning) and `-pack` (meaning → word).
- **Fact** blocks go one way only.
- **Formal** is the block as a mathematical claim; **Proof** proves that claim.

Total: 58 blocks (31 Definition, 27 Fact).


---

## Graph basics

### `graph-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G is a graph on n vertices |
| **Gives** | V(G) is nonempty and finite<br>every edge is a 2-element subset of V(G): no loops, no multiple edges |
| **Formal** | G = (V,E) is a graph ⟹ V ≠ ∅, |V| < ∞, E ⊆ (V choose 2) |
| **Proof** | Definition of a graph. An edge is a two-element set {u,v}, so u ≠ v (no loops); E is a set, so no edge occurs twice. ∎ |
| **Say** | “Since G is a graph, V(G) is a nonempty finite set and every edge is a two-element subset of V(G).” |
| **Source** | L1 slide 5 |

### `adjacent-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | u and v are adjacent in G |
| **Gives** | {u,v} ∈ E(G) |
| **Formal** | u, v adjacent in G ⟹ {u,v} ∈ E(G) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since u and v are adjacent, {u,v} ∈ E(G).” |
| **Source** | L1 slide 11 |

### `adjacent-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | {u,v} ∈ E(G) |
| **Gives** | u and v are adjacent in G |
| **Formal** | {u,v} ∈ E(G) ⟹ u, v adjacent in G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since {u,v} ∈ E(G), the vertices u and v are adjacent.” |
| **Source** | L1 slide 11 |


---

## Walks, paths, distance

### `walk-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | v₀,…,vₖ is a sequence with {vᵢ₋₁,vᵢ} ∈ E(G) for all i |
| **Gives** | v₀,…,vₖ is a walk of length k in G |
| **Formal** | (∀i ∈ {1,…,k}: {vᵢ₋₁,vᵢ} ∈ E(G)) ⟹ (v₀,…,vₖ) is a walk of length k |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Consecutive vertices are joined by edges of G, so v₀,…,vₖ is a walk of length k in G.” |
| **Source** | L1 slide 12 |

### `walk-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | v₀,…,vₖ is a walk of length k in G |
| **Gives** | v₀,…,vₖ is a sequence with {vᵢ₋₁,vᵢ} ∈ E(G) for all i |
| **Formal** | (v₀,…,vₖ) is a walk of length k ⟹ ∀i ∈ {1,…,k}: {vᵢ₋₁,vᵢ} ∈ E(G) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since v₀,…,vₖ is a walk, {vᵢ₋₁,vᵢ} ∈ E(G) for all i = 1,…,k.” |
| **Source** | L1 slide 12 |

### `path-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | v₀,…,vₖ is a walk of length k in G<br>the vertices v₀,…,vₖ are pairwise distinct |
| **Gives** | v₀,…,vₖ is a path of length k in G |
| **Formal** | (v₀,…,vₖ) is a walk ∧ (∀i ≠ j: vᵢ ≠ vⱼ) ⟹ (v₀,…,vₖ) is a path |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “This walk has no repeated vertex, hence it is a path of length k.” |
| **Source** | L1 slide 12 |

### `path-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | v₀,…,vₖ is a path of length k in G |
| **Gives** | v₀,…,vₖ is a walk of length k in G<br>the vertices v₀,…,vₖ are pairwise distinct |
| **Formal** | (v₀,…,vₖ) is a path ⟹ it is a walk ∧ ∀i ≠ j: vᵢ ≠ vⱼ |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since v₀,…,vₖ is a path, it is a walk and its vertices are pairwise distinct.” |
| **Source** | L1 slide 12 |

### `path-length-bound`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | v₀,…,vₖ is a path of length k in G<br>G is a graph on n vertices |
| **Gives** | k ≤ n − 1 |
| **Formal** | (v₀,…,vₖ) is a path in G, |V(G)| = n ⟹ k ≤ n − 1 |
| **Proof** | By path-unpack, the vertices v₀,…,vₖ are pairwise distinct, so the set {v₀,…,vₖ} ⊆ V(G) has exactly k + 1 elements. Hence k + 1 ≤ |V(G)| = n, i.e. k ≤ n − 1. ∎ |
| **Say** | “A path of length k has k + 1 distinct vertices, so k + 1 ≤ n, i.e. k ≤ n − 1.” |
| **Source** | L1 slide 12 |

### `walk-to-path`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | there is a walk from s to t in G |
| **Gives** | there is an s-t-path in G |
| **Formal** | ∃ walk from s to t in G ⟹ ∃ s-t-path in G |
| **Proof** | The set of walks from s to t is nonempty and lengths are non-negative integers, so we may choose a walk W = (v₀,…,vₖ) from s to t of minimum length. Suppose vᵢ = vⱼ for some i < j. Then (v₀,…,vᵢ,vⱼ₊₁,…,vₖ) is again a walk from s to t, of length k − (j − i) < k, contradicting the minimality of W. Hence the vertices of W are pairwise distinct, and W is an s-t-path. ∎ |
| **Say** | “Every walk from s to t contains an s-t-path.” |
| **Source** | L2 |

### `distance-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | there is an s-t-path of length k<br>no s-t-path has length < k |
| **Gives** | d(s,t) = k |
| **Formal** | (∃ s-t-path of length k) ∧ (∀ s-t-path P: |P| ≥ k) ⟹ d(s,t) = k |
| **Proof** | d(s,t) := min{ |P| : P is an s-t-path }. The first assumption gives d(s,t) ≤ k, the second gives d(s,t) ≥ k. ∎ |
| **Say** | “There is an s-t-path of length k and no shorter one, hence d(s,t) = k.” |
| **Source** | L1 slides 13, 17 |

### `distance-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | d(s,t) = k |
| **Gives** | there is an s-t-path of length k<br>no s-t-path has length < k |
| **Formal** | d(s,t) = k ⟹ (∃ s-t-path of length k) ∧ (∀ s-t-path P: |P| ≥ k) |
| **Proof** | d(s,t) := min{ |P| : P is an s-t-path }. A minimum is attained and is a lower bound. ∎ |
| **Say** | “Since d(s,t) = k, there is an s-t-path of length k and every s-t-path has length at least k.” |
| **Source** | L1 slides 13, 17 |


---

## Special graphs

### `complete-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G = Kₙ |
| **Gives** | every two distinct vertices of G are adjacent |
| **Formal** | G = Kₙ ⟹ ∀u ≠ v ∈ V(G): {u,v} ∈ E(G) |
| **Proof** | By definition E(Kₙ) = (V choose 2), which contains every two-element subset {u,v} of V. ∎ |
| **Say** | “Since G = Kₙ, every two distinct vertices of G are adjacent.” |
| **Source** | L1 slide 28 |

### `complete-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | every two distinct vertices of G are adjacent<br>G is a graph on n vertices |
| **Gives** | G = Kₙ |
| **Formal** | |V(G)| = n ∧ (∀u ≠ v ∈ V(G): {u,v} ∈ E(G)) ⟹ G = Kₙ |
| **Proof** | The assumption gives (V choose 2) ⊆ E(G); always E(G) ⊆ (V choose 2). Hence E(G) = (V choose 2), which is the definition of Kₙ. ∎ |
| **Say** | “Every two distinct vertices of G are adjacent, hence G = Kₙ.” |
| **Source** | L1 slide 28 |

### `complete-edges`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G = Kₙ |
| **Gives** | |E(G)| = n(n−1)/2 |
| **Formal** | |E(Kₙ)| = n(n − 1)/2 |
| **Proof** | E(Kₙ) = (V choose 2). There are n(n − 1) ordered pairs (u,v) with u ≠ v, and every two-element subset {u,v} corresponds to exactly two of them, (u,v) and (v,u). Hence |(V choose 2)| = n(n − 1)/2. ∎ |
| **Say** | “Kₙ has n(n−1)/2 edges, one for each pair of vertices.” |
| **Source** | L1 slide 28 |

### `complete-regular`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G = Kₙ |
| **Gives** | G is (n−1)-regular |
| **Formal** | G = Kₙ ⟹ ∀v ∈ V(G): deg(v) = n − 1 |
| **Proof** | By complete-unpack, N(v) = V ∖ {v} for every v, so deg(v) = |N(v)| = n − 1. ∎ |
| **Say** | “In Kₙ every vertex is adjacent to all n − 1 others, so Kₙ is (n−1)-regular.” |
| **Source** | L1 slide 28 |

### `complete-bipartite-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G = K_{a,b} with parts A, B |
| **Gives** | V(G) = A ∪ B and A ∩ B = ∅<br>u, v adjacent ⟺ u, v lie in different parts |
| **Formal** | G = K_{a,b} ⟹ V = A ∪ B, A ∩ B = ∅, and ∀u ≠ v: ({u,v} ∈ E ⟺ u, v lie in different parts) |
| **Proof** | By definition E = {{x,y} | x ∈ A, y ∈ B} with A ∩ B = ∅. So {u,v} ∈ E if and only if one of u, v lies in A and the other in B. ∎ |
| **Say** | “Since G = K_{a,b}, its vertex set splits into disjoint parts A, B, and two vertices are adjacent if and only if they lie in different parts.” |
| **Source** | L1 slide 29 |

### `complete-bipartite-edges`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G = K_{a,b} with parts A, B |
| **Gives** | |E(G)| = a·b |
| **Formal** | |E(K_{a,b})| = a·b |
| **Proof** | The map (x,y) ↦ {x,y} from A × B to E is onto by the definition of E, and one-to-one because A ∩ B = ∅ (from {x,y} we recover x as the element in A). Hence |E| = |A × B| = a·b. ∎ |
| **Say** | “Each of the a vertices of A is adjacent to each of the b vertices of B, so |E| = a·b.” |
| **Source** | L1 slide 29 |

### `complete-bipartite-is-bipartite`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G = K_{a,b} with parts A, B |
| **Gives** | G is bipartite with parts A, B |
| **Formal** | G = K_{a,b} with parts A, B ⟹ G is bipartite with parts A, B |
| **Proof** | V = A ∪ B and A ∩ B = ∅ by definition, and every edge has the form {x,y} with x ∈ A, y ∈ B. By bipartite-pack, G is bipartite. ∎ |
| **Say** | “K_{a,b} is bipartite with parts A and B, since every edge joins A with B.” |
| **Source** | L1 slide 29 |

### `bipartite-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G is bipartite with parts A, B |
| **Gives** | V(G) = A ∪ B and A ∩ B = ∅<br>every edge of G has one endpoint in A and one in B |
| **Formal** | G bipartite with parts A, B ⟹ V = A ∪ B, A ∩ B = ∅, ∀e ∈ E: |e ∩ A| = |e ∩ B| = 1 |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is bipartite with parts A, B, every edge of G has one endpoint in A and the other in B.” |
| **Source** | L1 slide 39 / T1 Ex 11 |

### `bipartite-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | V(G) = A ∪ B and A ∩ B = ∅<br>every edge of G has one endpoint in A and one in B |
| **Gives** | G is bipartite with parts A, B |
| **Formal** | V = A ∪ B, A ∩ B = ∅, ∀e ∈ E: |e ∩ A| = |e ∩ B| = 1 ⟹ G is bipartite with parts A, B |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “V(G) is split into disjoint sets A, B and every edge joins A with B, hence G is bipartite.” |
| **Source** | L1 slide 39 / T1 Ex 11 |

### `bipartite-parity`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G is bipartite with parts A, B |
| **Gives** | even walk ends in its starting part; odd walk ends in the other part |
| **Formal** | G bipartite with parts A, B; (v₀,…,vₖ) a walk with v₀ ∈ A ⟹ (vₖ ∈ A ⟺ k is even) |
| **Proof** | We prove by induction on i that vᵢ ∈ A if i is even and vᵢ ∈ B if i is odd. Base: v₀ ∈ A. Step: {vᵢ₋₁,vᵢ} ∈ E has exactly one endpoint in A and one in B (bipartite-unpack), so vᵢ lies in the part not containing vᵢ₋₁; the claim for i follows from the claim for i − 1. For i = k we get the statement. The case v₀ ∈ B is symmetric. ∎ |
| **Say** | “Every edge joins A with B, so each step of a walk changes the part; a walk of even length ends in the part where it starts, a walk of odd length in the other part.” |
| **Source** | Prereq 1 Ex 4 |

### `odd-cycle-not-bipartite`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G contains a cycle of odd length |
| **Gives** | G is not bipartite |
| **Formal** | G contains a cycle of odd length ⟹ G is not bipartite |
| **Proof** | For the sake of contradiction, suppose G is bipartite with parts A, B and contains a cycle with vertices v₀,v₁,…,vₖ₋₁ in this order, k odd. W.l.o.g. v₀ ∈ A. Then (v₀,v₁,…,vₖ₋₁,v₀) is a walk of odd length k starting in A, so by bipartite-parity it ends in B. But it ends in v₀ ∈ A, and A ∩ B = ∅ — a contradiction. ∎ |
| **Say** | “A graph containing an odd cycle is not bipartite.” |
| **Source** | T1 Ex 11 |

### `path-graph-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G = Pₙ |
| **Gives** | G has n vertices and n − 1 edges |
| **Formal** | G = Pₙ ⟹ |V(G)| = n, |E(G)| = n − 1 |
| **Proof** | V = {1,…,n} and E = {{i,i+1} | i = 1,…,n − 1}; these n − 1 sets are pairwise different. ∎ |
| **Say** | “Pₙ has n vertices 1,…,n and the n − 1 edges {i,i+1}.” |
| **Source** | L1 slide 30 |

### `cycle-graph-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G = Cₙ |
| **Gives** | n ≥ 3 and G has n vertices and n edges<br>G is 2-regular |
| **Formal** | G = Cₙ ⟹ n ≥ 3, |V(G)| = |E(G)| = n, ∀v: deg(v) = 2 |
| **Proof** | V = {1,…,n}, E = {{i,i+1} | i = 1,…,n − 1} ∪ {{1,n}}. Since n ≥ 3, {1,n} is not of the form {i,i+1}, so |E| = (n − 1) + 1 = n. N(1) = {2,n}, N(n) = {n − 1,1}, and N(i) = {i − 1,i + 1} for 1 < i < n; each has two elements because n ≥ 3. ∎ |
| **Say** | “Cₙ (n ≥ 3) has n vertices and n edges, and every vertex has degree 2.” |
| **Source** | L1 slide 31 |


---

## Complement

### `complement-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | Ḡ is the complement of G |
| **Gives** | V(Ḡ) = V(G)<br>for u ≠ v: {u,v} ∈ E(Ḡ) ⟺ {u,v} ∉ E(G) |
| **Formal** | Ḡ complement of G ⟹ V(Ḡ) = V(G) ∧ ∀u ≠ v: ({u,v} ∈ E(Ḡ) ⟺ {u,v} ∉ E(G)) |
| **Proof** | By definition Ḡ = (V, (V choose 2) ∖ E). For u ≠ v, {u,v} ∈ (V choose 2), so {u,v} ∈ E(Ḡ) ⟺ {u,v} ∉ E. ∎ |
| **Say** | “By the definition of the complement, Ḡ has the same vertex set as G, and two distinct vertices are adjacent in Ḡ if and only if they are not adjacent in G.” |
| **Source** | L1 slide 32 |

### `complement-degree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | Ḡ is the complement of G<br>G is a graph on n vertices |
| **Gives** | deg_Ḡ(v) = n − 1 − deg_G(v) for every v |
| **Formal** | ∀v ∈ V: deg_Ḡ(v) = n − 1 − deg_G(v) |
| **Proof** | Let v ∈ V. By complement-unpack, every w ∈ V ∖ {v} satisfies exactly one of {v,w} ∈ E(G), {v,w} ∈ E(Ḡ). Hence N_G(v) and N_Ḡ(v) are disjoint and N_G(v) ∪ N_Ḡ(v) = V ∖ {v}. Therefore deg_G(v) + deg_Ḡ(v) = |V ∖ {v}| = n − 1. ∎ |
| **Say** | “Each of the n − 1 other vertices is adjacent to v in exactly one of G and Ḡ, so deg_Ḡ(v) = n − 1 − deg_G(v).” |
| **Source** | L1 slide 32 |


---

## Degrees

### `degree-neighborhood`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | deg(v) = k |
| **Gives** | |N(v)| = k |
| **Formal** | deg(v) = k ⟹ |N(v)| = k |
| **Proof** | deg(v) := |{e ∈ E | v ∈ e}| and N(v) := {w ∈ V | {v,w} ∈ E}. The map w ↦ {v,w} is a bijection from N(v) onto the set of edges incident with v. Hence deg(v) = |N(v)|. ∎ |
| **Say** | “deg(v) = |N(v)|, so v has exactly k neighbors.” |
| **Source** | L1 slide 33 |

### `degree-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | |N(v)| = k |
| **Gives** | deg(v) = k |
| **Formal** | |N(v)| = k ⟹ deg(v) = k |
| **Proof** | The map w ↦ {v,w} is a bijection from N(v) onto the set of edges incident with v, so deg(v) = |N(v)| = k. ∎ |
| **Say** | “v has exactly k neighbors, so deg(v) = k.” |
| **Source** | L1 slide 33 |

### `neighborhood-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | v ∈ N(u) |
| **Gives** | u and v are adjacent in G |
| **Formal** | v ∈ N(u) ⟹ u, v adjacent in G |
| **Proof** | N(u) := {v ∈ V | {u,v} ∈ E}. This is the definition, read in this direction. |
| **Say** | “Since v ∈ N(u), the vertices u and v are adjacent (and u ≠ v).” |
| **Source** | L1 slide 33 |

### `neighborhood-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | u and v are adjacent in G |
| **Gives** | v ∈ N(u) |
| **Formal** | u, v adjacent in G ⟹ v ∈ N(u) |
| **Proof** | N(u) := {v ∈ V | {u,v} ∈ E}. This is the definition, read in this direction. |
| **Say** | “u and v are adjacent, hence v ∈ N(u) (and u ∈ N(v)).” |
| **Source** | L1 slide 33 |

### `degree-bounds`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G is a graph on n vertices |
| **Gives** | 0 ≤ deg(v) ≤ n − 1 for every vertex v |
| **Formal** | ∀v ∈ V(G): 0 ≤ deg(v) ≤ n − 1 |
| **Proof** | Let v ∈ V. If w ∈ N(v) then {v,w} is an edge, a two-element set, so w ≠ v. Hence N(v) ⊆ V ∖ {v} and 0 ≤ deg(v) = |N(v)| ≤ |V ∖ {v}| = n − 1. ∎ |
| **Say** | “A vertex can be adjacent only to the n − 1 other vertices, so 0 ≤ deg(v) ≤ n − 1.” |
| **Source** | T1 Ex 1d |

### `universal-vertex`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | deg(u) = n − 1<br>G is a graph on n vertices |
| **Gives** | u is adjacent to every other vertex of G |
| **Formal** | deg(u) = n − 1 ⟹ N(u) = V ∖ {u} |
| **Proof** | N(u) ⊆ V ∖ {u} (see degree-bounds), and both sets are finite with |N(u)| = n − 1 = |V ∖ {u}|. A subset of a finite set with the same number of elements is the whole set. ∎ |
| **Say** | “Since deg(u) = n − 1, the vertex u is adjacent to all other vertices of G.” |
| **Source** | T1 Ex 1f, 2c |

### `isolated-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | deg(w) = 0 |
| **Gives** | w is isolated (adjacent to no vertex) |
| **Formal** | deg(w) = 0 ⟹ N(w) = ∅ |
| **Proof** | |N(w)| = deg(w) = 0, so N(w) = ∅; such a vertex is called isolated. ∎ |
| **Say** | “Since deg(w) = 0, the vertex w is isolated: it is adjacent to no vertex.” |
| **Source** | L1 slide 34 |

### `isolated-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | w is isolated (adjacent to no vertex) |
| **Gives** | deg(w) = 0 |
| **Formal** | N(w) = ∅ ⟹ deg(w) = 0 |
| **Proof** | deg(w) = |N(w)| = |∅| = 0. ∎ |
| **Say** | “w is adjacent to no vertex, so deg(w) = 0.” |
| **Source** | L1 slide 34 |

### `universal-excludes-isolated`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | u is adjacent to every other vertex of G<br>n ≥ 2 |
| **Gives** | deg(v) ≥ 1 for every vertex v (no isolated vertex) |
| **Formal** | n ≥ 2 ∧ N(u) = V ∖ {u} ⟹ ∀v ∈ V: deg(v) ≥ 1 |
| **Proof** | Let v ∈ V. If v ≠ u, then v ∈ V ∖ {u} = N(u), so {u,v} ∈ E and u ∈ N(v); hence deg(v) ≥ 1. If v = u, then deg(u) = |V ∖ {u}| = n − 1 ≥ 1, because n ≥ 2. ∎ |
| **Say** | “u is adjacent to every other vertex, so every vertex other than u has u as a neighbor, and u itself has n − 1 ≥ 1 neighbors. Hence every vertex of G has degree at least 1; in particular G has no isolated vertex.” |
| **Source** | T1 Ex 2c |

### `same-degree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G is a graph on n vertices<br>n ≥ 2 |
| **Gives** | two vertices of G have the same degree |
| **Formal** | n ≥ 2 ⟹ ∃u ≠ v ∈ V(G): deg(u) = deg(v) |
| **Proof** | For the sake of contradiction, suppose all degrees are distinct. By degree-bounds, deg is a one-to-one map from V into {0,1,…,n − 1}. Both sets have n elements, so deg is onto: there are w, u ∈ V with deg(w) = 0 and deg(u) = n − 1. By universal-vertex, N(u) = V ∖ {u}; by universal-excludes-isolated, every vertex has degree at least 1. This contradicts deg(w) = 0. ∎ |
| **Say** | “The degrees lie in {0,…,n−1}, and 0 and n − 1 cannot both occur, so the n vertices use at most n − 1 values; by the pigeonhole principle two vertices have the same degree.” |
| **Source** | T1 Ex 2a, 3 |


---

## Regular graphs, Degree Sum Formula

### `regular-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G is r-regular |
| **Gives** | deg(v) = r for every vertex v |
| **Formal** | G is r-regular ⟹ ∀v ∈ V: deg(v) = r |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is r-regular, deg(v) = r for every vertex v.” |
| **Source** | L1 slide 34 |

### `regular-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | deg(v) = r for every vertex v |
| **Gives** | G is r-regular |
| **Formal** | ∀v ∈ V: deg(v) = r ⟹ G is r-regular |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Every vertex of G has degree r, hence G is r-regular.” |
| **Source** | L1 slide 34 |

### `degree-sum`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | G is a graph on n vertices |
| **Gives** | Σ deg(v) = 2·|E(G)| |
| **Formal** | Σ_{v∈V} deg(v) = 2·|E| |
| **Proof** | Let I = {(v,e) | v ∈ V, e ∈ E, v ∈ e}. Counting by vertices: each v lies in exactly deg(v) edges, so |I| = Σ_{v∈V} deg(v). Counting by edges: each edge has exactly two elements, so |I| = Σ_{e∈E} 2 = 2|E|. Comparing the two counts gives the formula. ∎ |
| **Say** | “By the Degree Sum Formula, Σ deg(v) = 2|E|.” |
| **Source** | L1 slide 35, L2 slide 6 |

### `degree-sum-even`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | Σ deg(v) = 2·|E(G)| |
| **Gives** | Σ deg(v) is even |
| **Formal** | Σ deg(v) = 2|E| ⟹ Σ deg(v) ≡ 0 (mod 2) |
| **Proof** | |E| is an integer, so 2|E| is divisible by 2. ∎ |
| **Say** | “Hence the sum of all degrees is even.” |
| **Source** | L1 slide 36 |

### `handshaking`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | Σ deg(v) is even |
| **Gives** | the number of odd-degree vertices of G is even |
| **Formal** | Σ deg(v) even ⟹ |{v ∈ V : deg(v) is odd}| is even |
| **Proof** | Let O = {v ∈ V | deg(v) is odd}. Then Σ_{v∈V} deg(v) = Σ_{v∈O} deg(v) + Σ_{v∉O} deg(v). The left side is even and the last sum is a sum of even numbers, so S = Σ_{v∈O} deg(v) is even. S is a sum of |O| odd numbers, hence S ≡ |O| (mod 2). Therefore |O| is even. ∎ |
| **Say** | “The degree sum is even, so the number of odd-degree vertices is even (Handshaking Lemma).” |
| **Source** | L1 slide 36 |

### `regular-degree-sum`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | deg(v) = r for every vertex v<br>Σ deg(v) = 2·|E(G)| |
| **Gives** | n·r = 2·|E(G)| |
| **Formal** | (∀v: deg(v) = r) ∧ Σ deg(v) = 2|E| ⟹ n·r = 2|E| |
| **Proof** | Σ_{v∈V} deg(v) = Σ_{v∈V} r = n·r. ∎ |
| **Say** | “All n vertices have degree r, so by the Degree Sum Formula n·r = 2|E|.” |
| **Source** | L1 slide 36 |

### `regular-odd-degree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | n·r = 2·|E(G)|<br>r is odd |
| **Gives** | n is even |
| **Formal** | n·r = 2|E| ∧ r odd ⟹ n even |
| **Proof** | n·r = 2|E| is even. If n were odd, n·r would be a product of two odd numbers, hence odd — a contradiction. So n is even. ∎ |
| **Say** | “n·r is even and r is odd, hence n is even.” |
| **Source** | L1 slide 36 |

### `zero-regular-shape`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G is 0-regular |
| **Gives** | G consists of n isolated vertices |
| **Formal** | G 0-regular ⟹ E(G) = ∅ |
| **Proof** | Every vertex has deg(v) = 0, so N(v) = ∅ for all v. An edge {u,v} would give v ∈ N(u). Hence E = ∅. ∎ |
| **Say** | “A 0-regular graph has no edges: it consists of n isolated vertices.” |
| **Source** | L1 slide 34 |

### `one-regular-shape`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G is 1-regular |
| **Gives** | G is a disjoint union of edges<br>n is even |
| **Formal** | G 1-regular ⟹ E(G) is a set of pairwise disjoint edges covering V, and n is even |
| **Proof** | Every vertex v has exactly one neighbor; call it m(v). Since v ∈ N(m(v)) and |N(m(v))| = 1, we get m(m(v)) = v. So the sets {v, m(v)} partition V into pairs, each pair is an edge, and there are no other edges, because an edge {v,w} forces w = m(v). The pairs are disjoint, so n = 2·(number of pairs) is even. ∎ |
| **Say** | “In a 1-regular graph every vertex lies in exactly one edge, so G is a disjoint union of edges and n is even.” |
| **Source** | L1 slide 34 |

### `two-regular-shape`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | G is 2-regular |
| **Gives** | G is a disjoint union of cycles |
| **Formal** | G 2-regular ⟹ G is a disjoint union of cycles |
| **Proof** | (Sketch.) Start at any vertex v₀ and walk v₀,v₁,v₂,…, always leaving a vertex by the edge not used to enter it (possible since every degree is 2). V is finite, so some vertex repeats; the first repeated vertex is v₀, since any other first repeat would have three different neighbors on the walk. This gives a cycle C through v₀. No vertex of C has a neighbor outside C (both its edges lie in C). Remove C; the rest is still 2-regular; repeat. ∎ |
| **Say** | “A 2-regular graph is a disjoint union of cycles.” |
| **Source** | L1 slide 34 |


---

## Counting

### `count-graphs`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1, Lecture 3 |
| **Needs** | V is a fixed vertex set with |V| = n |
| **Gives** | there are exactly 2^(n(n−1)/2) graphs on V |
| **Formal** | |V| = n ⟹ |{G : V(G) = V}| = 2^(n(n−1)/2) |
| **Proof** | A graph on V is the pair (V,E) with E ⊆ (V choose 2), so the graphs on V correspond one-to-one to the subsets of (V choose 2). By complete-edges, |(V choose 2)| = n(n − 1)/2, and a set with N elements has exactly 2^N subsets. ∎ |
| **Say** | “A graph on V is determined by its edge set, a subset of the n(n−1)/2 pairs; hence there are 2^(n(n−1)/2) graphs on V.” |
| **Source** | T1 Ex 5, L3 slide 8 |

### `count-paths-complete`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | x ≠ y are vertices of Kₙ |
| **Gives** | the number of x-y-paths of length k is (n−2)(n−3)···(n−k) |
| **Formal** | x ≠ y ∈ V(Kₙ) ⟹ #{x-y-paths of length k} = (n − 2)(n − 3)···(n − k) |
| **Proof** | An x-y-path of length k is a sequence (x,w₁,…,wₖ₋₁,y) of pairwise distinct vertices; conversely every such sequence is a path, since all distinct vertices of Kₙ are adjacent (complete-unpack). So the paths correspond one-to-one to the ordered (k − 1)-tuples of distinct elements of V ∖ {x,y}, a set of size n − 2. There are (n − 2)(n − 3)···(n − k) such tuples. ∎ |
| **Say** | “An x-y-path of length k has k − 1 inner vertices, distinct and different from x, y; choosing them in order gives (n−2)(n−3)···(n−k) paths, and each choice is a path because all vertices of Kₙ are adjacent.” |
| **Source** | T1 Ex 6, Prereq 1 Ex 3 |


---

## Subgraphs

### `subgraph-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | H is a subgraph of G |
| **Gives** | V(H) ⊆ V(G) and E(H) ⊆ E(G) |
| **Formal** | H ⊆ G ⟹ V(H) ⊆ V(G) ∧ E(H) ⊆ E(G) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since H ⊆ G, V(H) ⊆ V(G) and E(H) ⊆ E(G).” |
| **Source** | L2 slide 2 |

### `subgraph-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | V(H) ⊆ V(G) and E(H) ⊆ E(G) |
| **Gives** | H is a subgraph of G |
| **Formal** | V(H) ⊆ V(G) ∧ E(H) ⊆ E(G) ⟹ H ⊆ G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “V(H) ⊆ V(G) and E(H) ⊆ E(G), hence H is a subgraph of G.” |
| **Source** | L2 slide 2 |

### `induced-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | H is an induced subgraph of G |
| **Gives** | V(H) ⊆ V(G)<br>E(H) contains every edge of G with both endpoints in V(H) |
| **Formal** | H induced subgraph of G ⟹ V(H) ⊆ V(G) ∧ E(H) = E(G) ∩ (V(H) choose 2) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since H is an induced subgraph, every edge of G with both endpoints in V(H) is an edge of H.” |
| **Source** | L2 slide 2 |

### `induced-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | H is a subgraph of G<br>E(H) contains every edge of G with both endpoints in V(H) |
| **Gives** | H is an induced subgraph of G |
| **Formal** | H ⊆ G ∧ E(G) ∩ (V(H) choose 2) ⊆ E(H) ⟹ H is an induced subgraph of G |
| **Proof** | Since H is a graph, E(H) ⊆ (V(H) choose 2); since H ⊆ G, E(H) ⊆ E(G). So E(H) ⊆ E(G) ∩ (V(H) choose 2). The other inclusion is assumed. Hence equality holds, which is the definition of an induced subgraph. ∎ |
| **Say** | “H is a subgraph of G and no edge of G between two vertices of H is missing in H, hence H is induced.” |
| **Source** | L2 slide 2 |

### `induced-is-subgraph`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | H is an induced subgraph of G |
| **Gives** | H is a subgraph of G |
| **Formal** | H induced subgraph of G ⟹ H ⊆ G |
| **Proof** | V(H) ⊆ V(G) by definition, and E(H) = E(G) ∩ (V(H) choose 2) ⊆ E(G). ∎ |
| **Say** | “Every induced subgraph is a subgraph.” |
| **Source** | L2 slide 2 |

### `induced-by-vertex-set`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1, Lecture 2 |
| **Needs** | H is an induced subgraph of G |
| **Gives** | H = G[V(H)], so H is determined by its vertex set |
| **Formal** | H induced subgraph of G ⟹ H = G[V(H)] |
| **Proof** | E(H) = E(G) ∩ (V(H) choose 2) = E(G[V(H)]) and the vertex sets agree. So H depends only on V(H). ∎ |
| **Say** | “An induced subgraph is determined by its vertex set: H = G[V(H)].” |
| **Source** | L2 slide 2 |

### `shortest-cycle-induced`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | C is a shortest cycle in G |
| **Gives** | C is an induced subgraph of G |
| **Formal** | C a shortest cycle in G ⟹ C is an induced subgraph of G |
| **Proof** | Let C have vertices v₁,…,vₖ in this order. For the sake of contradiction, suppose C is not induced: there is an edge {vᵢ,vⱼ} ∈ E(G) ∖ E(C) with i < j. Then j − i ≥ 2 and (i,j) ≠ (1,k), so 2 ≤ j − i ≤ k − 2. The vertices vᵢ,vᵢ₊₁,…,vⱼ together with the edge {vⱼ,vᵢ} form a cycle of length j − i + 1, where 3 ≤ j − i + 1 ≤ k − 1 < k. This contradicts the choice of C as a shortest cycle. ∎ |
| **Say** | “A shortest cycle is induced: an edge of G joining two non-consecutive vertices of C (a chord) would, with one of the two arcs of C, form a shorter cycle.” |
| **Source** | T1 Ex 13 |

### `shortest-odd-cycle-induced`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 1 |
| **Needs** | C is a shortest odd cycle in G |
| **Gives** | C is an induced subgraph of G |
| **Formal** | C a shortest odd cycle in G ⟹ C is an induced subgraph of G |
| **Proof** | Let C have vertices v₁,…,vₖ in this order, k odd. Suppose there is an edge {vᵢ,vⱼ} ∈ E(G) ∖ E(C), i < j; as before 2 ≤ j − i ≤ k − 2. It splits C into two cycles: C₁ on vᵢ,…,vⱼ of length j − i + 1, and C₂ on vⱼ,…,vₖ,v₁,…,vᵢ of length k − (j − i) + 1. Both lengths are between 3 and k − 1, and their sum is k + 2, an odd number. Hence one of C₁, C₂ has odd length and is shorter than C — a contradiction. ∎ |
| **Say** | “A shortest odd cycle is induced: a chord splits C (length k) into two shorter cycles whose lengths sum to k + 2, an odd number, so one of them is odd — contradicting minimality.” |
| **Source** | T1 Ex 13 |


---

## Directed graphs

### `digraph-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | G is a directed graph |
| **Gives** | edges are ordered pairs; (u,v) ≠ (v,u); loops (u,u) are allowed |
| **Formal** | G = (V,E) directed ⟹ E ⊆ V × V |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “In a directed graph the edges are ordered pairs of vertices; loops are allowed.” |
| **Source** | L1 slide 37 |

### `successor-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 1 |
| **Needs** | (u,v) ∈ E(G) |
| **Gives** | u is a predecessor of v and v is a successor of u |
| **Formal** | (u,v) ∈ E(G) ⟹ u predecessor of v, v successor of u |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since (u,v) ∈ E, u is a predecessor of v and v is a successor of u.” |
| **Source** | L1 slide 37 |
