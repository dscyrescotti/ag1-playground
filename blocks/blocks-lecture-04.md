# Blocks — Lecture 4

Every block is a rule: **if you have everything under Needs, you may write the Say sentence and you then have everything under Gives.**

- **Definition** blocks come in pairs: `-unpack` (word → meaning) and `-pack` (meaning → word).
- **Fact** blocks go one way only.
- **Formal** is the block as a mathematical claim; **Proof** proves that claim.

Total: 40 blocks (22 Definition, 18 Fact).


---

## Rooted trees and heaps

### `rooted-tree-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | (T, r) is a rooted tree |
| **Gives** | T is a tree<br>r ∈ V(T) |
| **Formal** | (T, r) rooted tree ⟹ T tree ∧ r ∈ V(T) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since (T, r) is a rooted tree, T is a tree and r is one of its vertices, the root.” |
| **Source** | L4 slide 16 |

### `rooted-tree-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | T is a tree<br>r ∈ V(T) |
| **Gives** | (T, r) is a rooted tree |
| **Formal** | T tree ∧ r ∈ V(T) ⟹ (T, r) rooted tree |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “T is a tree and r ∈ V(T), hence (T, r) is a rooted tree.” |
| **Source** | L4 slide 16 |

### `ancestor-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | u is an ancestor of v in (T, r) |
| **Gives** | u lies on the v-r-path in T |
| **Formal** | u ancestor of v ⟹ u ∈ V(P), where P is the unique v-r-path in T |
| **Proof** | This is the definition, read in this direction. (Equivalently: v is a descendant of u.) The path is unique by tree-unique-paths. |
| **Say** | “Since u is an ancestor of v, u lies on the path from v to the root.” |
| **Source** | L4 slide 16 |

### `ancestor-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | u lies on the v-r-path in T |
| **Gives** | u is an ancestor of v in (T, r) |
| **Formal** | u ∈ V(P), P the v-r-path in T ⟹ u ancestor of v |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “u lies on the path from v to the root, hence u is an ancestor of v and v is a descendant of u.” |
| **Source** | L4 slide 16 |

### `parent-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | u is the parent of v in (T, r) |
| **Gives** | u is an ancestor of v in (T, r)<br>{u,v} ∈ E(T) |
| **Formal** | u parent of v ⟹ u ancestor of v ∧ {u,v} ∈ E(T) |
| **Proof** | This is the definition, read in this direction. (Equivalently: v is a child of u.) |
| **Say** | “Since u is the parent of v, u is an ancestor of v and {u,v} is an edge of T.” |
| **Source** | L4 slide 16 |

### `parent-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | u is an ancestor of v in (T, r)<br>{u,v} ∈ E(T) |
| **Gives** | u is the parent of v in (T, r) |
| **Formal** | u ancestor of v ∧ {u,v} ∈ E(T) ⟹ u parent of v |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “u is an ancestor of v and adjacent to v, hence u is the parent of v and v is a child of u.” |
| **Source** | L4 slide 16 |

### `unique-parent`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | (T, r) is a rooted tree<br>v ≠ r is a vertex of T |
| **Gives** | v has exactly one parent |
| **Formal** | (T, r) rooted tree ∧ v ≠ r ⟹ ∃! u: u parent of v |
| **Proof** | By tree-unique-paths there is exactly one v-r-path P = (v = a₀,a₁,…,aₘ = r), and m ≥ 1 because v ≠ r. Existence: a₁ lies on P and {a₁,v} ∈ E(T), so a₁ is a parent of v. Uniqueness: let u be a parent of v. Then u = aᵢ for some i, and i ≥ 1 since {u,v} is an edge. If i ≥ 2, the vertices a₀,a₁,…,aᵢ with the edge {aᵢ,a₀} form a cycle in T — a contradiction. Hence u = a₁. ∎ |
| **Say** | “Every vertex other than the root has exactly one parent: the second vertex on its path to the root.” |
| **Source** | L4 slide 16 |

### `level-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | v is at level i of (T, r) |
| **Gives** | the v-r-path in T has length i |
| **Formal** | v at level i ⟹ the v-r-path has length i |
| **Proof** | This is the definition, read in this direction. The root is at level 0, its children at level 1, and so on. The depth of the rooted tree is the number of its levels. |
| **Say** | “v is at level i, i.e. its path to the root has i edges.” |
| **Source** | L4 slide 16 |

### `level-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | the v-r-path in T has length i |
| **Gives** | v is at level i of (T, r) |
| **Formal** | the v-r-path has length i ⟹ v at level i |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “The path from v to the root has i edges, so v is at level i.” |
| **Source** | L4 slide 16 |

### `child-level`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | (T, r) is a rooted tree<br>v is at level i of (T, r) |
| **Gives** | every child of v is at level i + 1 |
| **Formal** | v at level i ∧ w child of v ⟹ w at level i + 1 |
| **Proof** | Let w be a child of v. Then v lies on the w-r-path P and {v,w} ∈ E(T), so as in unique-parent v is the second vertex of P: P = (w,v,…,r). The part of P from v to r is the v-r-path, of length i. Hence P has length i + 1. ∎ |
| **Say** | “A child's path to the root goes through its parent, so it is one edge longer: children are one level below.” |
| **Source** | L4 slide 16 |

### `binary-tree-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | (T, r) is a binary tree |
| **Gives** | (T, r) is a rooted tree<br>every vertex of T has at most two children, each marked as left or right |
| **Formal** | (T, r) binary tree ⟹ (T, r) rooted ∧ every vertex has ≤ 2 children, each left or right |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since T is a binary tree, it is rooted and every vertex has at most two children, a left one and a right one.” |
| **Source** | L4 slide 18 |

### `binary-tree-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | (T, r) is a rooted tree<br>every vertex of T has at most two children, each marked as left or right |
| **Gives** | (T, r) is a binary tree |
| **Formal** | (T, r) rooted ∧ every vertex has ≤ 2 children, each left or right ⟹ (T, r) binary tree |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “T is rooted and every vertex has at most two children with assigned positions, hence T is a binary tree.” |
| **Source** | L4 slide 18 |

### `binary-level-size`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | (T, r) is a rooted tree<br>every vertex of T has at most two children, each marked as left or right |
| **Gives** | level i of T contains at most 2ⁱ vertices |
| **Formal** | (T, r) binary tree ⟹ ∀i ≥ 0: |{v : v at level i}| ≤ 2ⁱ |
| **Proof** | By induction on i. Level 0 contains only the root: 1 = 2⁰. Let i ≥ 1. Every vertex at level i is not the root, so by unique-parent it has a parent, which by child-level is at level i − 1. Each vertex of level i − 1 has at most two children. Hence level i has at most 2 · 2ⁱ⁻¹ = 2ⁱ vertices by the induction hypothesis. ∎ |
| **Say** | “Level 0 has one vertex, and each level has at most twice as many vertices as the one above; so level i has at most 2ⁱ vertices.” |
| **Source** | L4 slide 21 |

### `binary-tree-size`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | level i of T contains at most 2ⁱ vertices |
| **Gives** | if T has ℓ levels, then T has at most 2^ℓ − 1 vertices |
| **Formal** | (T, r) binary tree with ℓ levels ⟹ |V(T)| ≤ 2^ℓ − 1 |
| **Proof** | The levels 0,…,ℓ − 1 partition V(T), and level i has at most 2ⁱ vertices. Hence |V(T)| ≤ 2⁰ + 2¹ + ⋯ + 2^{ℓ−1} = 2^ℓ − 1. ∎ |
| **Say** | “Summing 2ⁱ over the ℓ levels gives at most 2^ℓ − 1 vertices.” |
| **Source** | L4 slide 21 |

### `heap-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | H is a (minimum) binary heap with n elements |
| **Gives** | H is a binary tree with a key k(x) in every vertex x<br>heap shape: all levels of H except the last are completely filled, and the last is filled from the left<br>heap order: k(v) ≤ k(s) whenever s is a child of v |
| **Formal** | H heap ⟹ H binary tree with keys ∧ heap shape ∧ heap order |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since H is a heap, it is a binary tree with keys that satisfies the heap shape and the heap order.” |
| **Source** | L4 slide 19 |

### `heap-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | H is a binary tree with a key k(x) in every vertex x<br>heap shape: all levels of H except the last are completely filled, and the last is filled from the left<br>heap order: k(v) ≤ k(s) whenever s is a child of v |
| **Gives** | H is a (minimum) binary heap with n elements |
| **Formal** | H binary tree with keys ∧ heap shape ∧ heap order ⟹ H heap |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “H is a binary tree with keys that satisfies the heap shape and the heap order, hence H is a heap.” |
| **Source** | L4 slide 19 |

### `heap-path-monotone`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | heap order: k(v) ≤ k(s) whenever s is a child of v |
| **Gives** | on the path from any vertex to the root, the keys do not increase |
| **Formal** | heap order ⟹ for the path (v = a₀,a₁,…,aₘ = root): k(a₀) ≥ k(a₁) ≥ ⋯ ≥ k(aₘ) |
| **Proof** | On the path from v to the root, aⱼ₊₁ is the parent of aⱼ (unique-parent). By the heap order, k(aⱼ₊₁) ≤ k(aⱼ) for every j. ∎ |
| **Say** | “By the heap order, each step from a vertex to its parent does not increase the key.” |
| **Source** | L4 slide 20 (Observation) |

### `heap-min-at-root`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | on the path from any vertex to the root, the keys do not increase |
| **Gives** | the root of H holds the minimum key |
| **Formal** | ∀v ∈ V(H): k(root) ≤ k(v) |
| **Proof** | Let v be any vertex. The keys on the path from v to the root do not increase, so k(root) ≤ k(v). ∎ |
| **Say** | “Keys do not increase on the way to the root, so the root holds the minimum.” |
| **Source** | L4 slide 20 (Observation) |

### `heap-levels`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | heap shape: all levels of H except the last are completely filled, and the last is filled from the left |
| **Gives** | H has ⌊log₂ n⌋ + 1 levels |
| **Formal** | heap shape, n ≥ 1 elements, ℓ levels ⟹ ℓ = ⌊log₂ n⌋ + 1 |
| **Proof** | Let ℓ be the number of levels. By the heap shape, the levels 0,…,ℓ − 2 are full and contain 2⁰ + ⋯ + 2^{ℓ−2} = 2^{ℓ−1} − 1 vertices, and the last level contains at least 1 and at most 2^{ℓ−1} vertices. Hence 2^{ℓ−1} ≤ n ≤ 2^ℓ − 1 < 2^ℓ, so ℓ − 1 ≤ log₂ n < ℓ, i.e. ⌊log₂ n⌋ = ℓ − 1. ∎ |
| **Say** | “A heap with n elements has ⌊log₂ n⌋ + 1 levels.” |
| **Source** | L4 slide 21 |

### `heap-indices`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | heap shape: all levels of H except the last are completely filled, and the last is filled from the left |
| **Gives** | numbering the vertices 1,…,n level by level from the left: vertex i has children 2i and 2i + 1 and parent ⌊i/2⌋ |
| **Formal** | index(left child of i) = 2i, index(right child of i) = 2i + 1, index(parent of i) = ⌊i/2⌋ |
| **Proof** | The levels 0,…,j − 1 are full and contain 2ʲ − 1 vertices, so level j holds the indices 2ʲ,…,2ʲ⁺¹ − 1, and the vertex at position p (counted from 0) of level j has index i = 2ʲ + p. The p vertices to its left have 2p children, which come first in level j + 1; so its children are at positions 2p and 2p + 1 of level j + 1, i.e. they have indices 2ʲ⁺¹ + 2p = 2i and 2i + 1 (when these do not exceed n). Conversely, the parent of 2i and of 2i + 1 is i = ⌊2i/2⌋ = ⌊(2i + 1)/2⌋. ∎ |
| **Say** | “With the vertices numbered level by level, the children of vertex i are 2i and 2i + 1, and its parent is ⌊i/2⌋.” |
| **Source** | L4 slide 31 (Observation) |

### `heap-leaves`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | numbering the vertices 1,…,n level by level from the left: vertex i has children 2i and 2i + 1 and parent ⌊i/2⌋ |
| **Gives** | H has exactly ⌈n/2⌉ vertices without children |
| **Formal** | #{vertices of H without children} = ⌈n/2⌉ |
| **Proof** | By heap-indices, vertex i has a child if and only if 2i ≤ n, i.e. i ≤ ⌊n/2⌋. So exactly ⌊n/2⌋ vertices have a child, and n − ⌊n/2⌋ = ⌈n/2⌉ have none. (The lecture states this for n ≥ 3 and proves it by counting insertions.) ∎ |
| **Say** | “Vertex i has a child exactly when 2i ≤ n, so the ⌊n/2⌋ first vertices have children and the remaining ⌈n/2⌉ are leaves.” |
| **Source** | L4 slide 22 |

### `weighted-geometric-sum`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | k ≥ 0 is an integer |
| **Gives** | Σ_{q=0}^{k} q/2^q = 2 − (k + 2)/2^k |
| **Formal** | ∀k ≥ 0: Σ_{q=0}^{k} q/2^q = 2 − (k + 2)/2^k |
| **Proof** | By induction on k. For k = 0 both sides are 0. For k ≥ 1: Σ_{q=0}^{k} q/2^q = (2 − (k + 1)/2^{k−1}) + k/2^k = 2 − (2k + 2 − k)/2^k = 2 − (k + 2)/2^k, using the induction hypothesis for k − 1. ∎ |
| **Say** | “By induction on k, Σ q/2^q = 2 − (k + 2)/2^k; in particular the sum is less than 2.” |
| **Source** | L4 slide 34 |


---

## Topological ordering

### `topological-ordering-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | v₁,…,vₙ is a topological ordering of G |
| **Gives** | v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j |
| **Formal** | v₁,…,vₙ topological ordering ⟹ V = {v₁,…,vₙ} ∧ ∀(vᵢ,vⱼ) ∈ E: i < j |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since v₁,…,vₙ is a topological ordering, every arc goes from an earlier vertex to a later one.” |
| **Source** | L4 slide 38 |

### `topological-ordering-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j |
| **Gives** | v₁,…,vₙ is a topological ordering of G<br>G has a topological ordering |
| **Formal** | V = {v₁,…,vₙ} ∧ ∀(vᵢ,vⱼ) ∈ E: i < j ⟹ v₁,…,vₙ topological ordering |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “The ordering lists all vertices and every arc goes forward, hence it is a topological ordering of G.” |
| **Source** | L4 slide 38 |

### `directed-cycle-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | G contains a directed cycle |
| **Gives** | there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) |
| **Formal** | G contains a directed cycle ⟹ ∃ distinct c₁,…,cₖ, k ≥ 1: (cᵢ,cᵢ₊₁) ∈ E for i < k, (cₖ,c₁) ∈ E |
| **Proof** | This is the definition, read in this direction. For k = 1 the cycle is a loop (c₁,c₁). |
| **Say** | “Since G contains a directed cycle, there are vertices c₁,…,cₖ with arcs c₁ → c₂ → ⋯ → cₖ → c₁.” |
| **Source** | L4 slide 39 |

### `directed-cycle-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) |
| **Gives** | G contains a directed cycle |
| **Formal** | ∃ distinct c₁,…,cₖ, k ≥ 1: (cᵢ,cᵢ₊₁) ∈ E for i < k, (cₖ,c₁) ∈ E ⟹ G contains a directed cycle |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “The arcs c₁ → c₂ → ⋯ → cₖ → c₁ form a directed cycle in G.” |
| **Source** | L4 slide 39 |

### `dag-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | G is a DAG |
| **Gives** | G is a directed graph<br>G contains no directed cycle |
| **Formal** | G DAG ⟹ G directed ∧ G contains no directed cycle |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is a DAG, G is a directed graph that contains no directed cycle.” |
| **Source** | L4 slide 40 |

### `dag-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | G is a directed graph<br>G contains no directed cycle |
| **Gives** | G is a DAG |
| **Formal** | G directed ∧ G contains no directed cycle ⟹ G DAG |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “G is a directed graph with no directed cycle, hence G is a DAG.” |
| **Source** | L4 slide 40 |

### `source-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | s is a source of G |
| **Gives** | no arc of G ends in s |
| **Formal** | s source ⟹ ¬∃u: (u,s) ∈ E |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since s is a source, no arc ends in s.” |
| **Source** | L4 slide 41 |

### `source-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | no arc of G ends in s |
| **Gives** | s is a source of G<br>G has a source |
| **Formal** | ¬∃u: (u,s) ∈ E ⟹ s source |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “No arc ends in s, hence s is a source.” |
| **Source** | L4 slide 41 |

### `sink-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | t is a sink of G |
| **Gives** | no arc of G starts in t |
| **Formal** | t sink ⟹ ¬∃u: (t,u) ∈ E |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since t is a sink, no arc starts in t.” |
| **Source** | L4 slide 41 |

### `sink-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 4 |
| **Needs** | no arc of G starts in t |
| **Gives** | t is a sink of G<br>G has a sink |
| **Formal** | ¬∃u: (t,u) ∈ E ⟹ t sink |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “No arc starts in t, hence t is a sink.” |
| **Source** | L4 slide 41 |

### `cycle-no-topological-ordering`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) |
| **Gives** | G has no topological ordering |
| **Formal** | G contains a directed cycle ⟹ G has no topological ordering |
| **Proof** | For the sake of contradiction, let v₁,…,vₙ be a topological ordering and let p(x) denote the position of x in it. For the cycle c₁,…,cₖ every arc goes forward, so p(c₁) < p(c₂) < ⋯ < p(cₖ) < p(c₁) — a contradiction (for k = 1: p(c₁) < p(c₁)). ∎ |
| **Say** | “Along a directed cycle the positions in a topological ordering would have to increase all the way around, which is impossible.” |
| **Source** | L4 slide 39 (Observation) |

### `topological-ordering-acyclic`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | G has a topological ordering |
| **Gives** | G contains no directed cycle |
| **Formal** | G has a topological ordering ⟹ G contains no directed cycle |
| **Proof** | This is the contrapositive of cycle-no-topological-ordering. ∎ |
| **Say** | “A graph with a topological ordering contains no directed cycle.” |
| **Source** | L4 slide 39 (Observation) |

### `dag-source-sink`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | G contains no directed cycle |
| **Gives** | G has a source<br>G has a sink |
| **Formal** | G DAG ⟹ ∃ source ∧ ∃ sink |
| **Proof** | Let P = (v₀,…,vₖ) be a longest directed path in G (it exists: V is finite and a single vertex is a path). We claim v₀ is a source. Suppose (w,v₀) ∈ E. If w = vᵢ for some i, then v₀ → v₁ → ⋯ → vᵢ → v₀ is a directed cycle — a contradiction. Otherwise (w,v₀,…,vₖ) is a longer directed path — a contradiction. Symmetrically, vₖ is a sink. ∎ |
| **Say** | “By the theorem on the existence of a source and a sink, every DAG has at least one source and at least one sink.” |
| **Source** | L4 slide 42 |

### `no-source-cycle`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | every vertex of G has an incoming arc |
| **Gives** | G contains a directed cycle |
| **Formal** | (∀v ∃u: (u,v) ∈ E) ⟹ G contains a directed cycle |
| **Proof** | For the sake of contradiction, suppose G contains no directed cycle. By dag-source-sink G has a source s, i.e. no arc ends in s. This contradicts the assumption that every vertex has an incoming arc. ∎ |
| **Say** | “Every vertex has an incoming arc, so G has no source; a DAG always has one, hence G contains a directed cycle.” |
| **Source** | T3 Ex 7a |

### `mutual-paths-cycle`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | u ≠ v, and G has a directed path from u to v and a directed path from v to u |
| **Gives** | G contains a directed cycle |
| **Formal** | u ≠ v ∧ ∃ directed u-v-path ∧ ∃ directed v-u-path ⟹ G contains a directed cycle |
| **Proof** | Joining the two paths gives a closed directed walk (w₀,w₁,…,wₘ = w₀) with m ≥ 2. Choose indices i < j with wᵢ = wⱼ and j − i as small as possible (they exist: w₀ = wₘ). Then wᵢ,…,wⱼ₋₁ are pairwise distinct, (wₜ,wₜ₊₁) ∈ E for i ≤ t < j, and wⱼ = wᵢ. By directed-cycle-pack these vertices form a directed cycle. ∎ |
| **Say** | “Going from u to v and back to u is a closed directed walk, and every closed directed walk contains a directed cycle.” |
| **Source** | T3 Ex 8a |

### `dag-has-topological-ordering`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | G contains no directed cycle |
| **Gives** | G has a topological ordering |
| **Formal** | G contains no directed cycle ⟹ G has a topological ordering |
| **Proof** | By induction on n. For n = 1 the single vertex is an ordering (there is no loop, since a loop is a directed cycle). Let n > 1. By dag-source-sink G has a source s. G − s contains no directed cycle (a cycle in it would be a cycle in G), so by the induction hypothesis it has a topological ordering v₂,…,vₙ. Put v₁ = s. An arc not touching s goes forward by the hypothesis; an arc (s,vⱼ) goes forward because s is first; no arc ends in s. So v₁,…,vₙ is a topological ordering of G. ∎ |
| **Say** | “Every DAG has a topological ordering: put a source first and order the rest by induction.” |
| **Source** | L4 slides 38–42 (proved with an algorithm in a later lecture) |

### `hamiltonian-path-unique-ordering`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | G contains no directed cycle<br>G has a directed path that goes through all vertices |
| **Gives** | G has exactly one topological ordering |
| **Formal** | G DAG with a directed path through all vertices ⟹ G has exactly one topological ordering |
| **Proof** | Let (p₁,…,pₙ) be a directed path through all vertices. By dag-has-topological-ordering G has a topological ordering. In any topological ordering the arc (pᵢ,pᵢ₊₁) forces pᵢ before pᵢ₊₁, for every i. So the ordering must be p₁,…,pₙ: it is unique. ∎ |
| **Say** | “The path through all vertices fixes the order of every two consecutive vertices, so only one topological ordering is possible.” |
| **Source** | T3 Ex 9 (⇐) |

### `unique-ordering-hamiltonian-path`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 4 |
| **Needs** | G has exactly one topological ordering |
| **Gives** | G has a directed path that goes through all vertices |
| **Formal** | G has exactly one topological ordering ⟹ G has a directed path through all vertices |
| **Proof** | Let v₁,…,vₙ be the topological ordering. We claim (vᵢ,vᵢ₊₁) ∈ E for all i < n. Suppose not, for some i. Swap vᵢ and vᵢ₊₁. The only pair of vertices whose relative order changes is {vᵢ,vᵢ₊₁}; there is no arc (vᵢ,vᵢ₊₁) by assumption and no arc (vᵢ₊₁,vᵢ) because the original ordering is topological. So all arcs still go forward, and we get a second topological ordering — a contradiction. Hence (v₁,…,vₙ) is a directed path through all vertices. ∎ |
| **Say** | “If two neighbors in the ordering were not joined by an arc, swapping them would give a second topological ordering; so consecutive vertices are joined and the ordering itself is a path through all vertices.” |
| **Source** | T3 Ex 9 (⇒) |
