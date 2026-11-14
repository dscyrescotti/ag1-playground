# Blocks — Lecture 3

Every block is a rule: **if you have everything under Needs, you may write the Say sentence and you then have everything under Gives.**

- **Definition** blocks come in pairs: `-unpack` (word → meaning) and `-pack` (meaning → word).
- **Fact** blocks go one way only.
- **Formal** is the block as a mathematical claim; **Proof** proves that claim.

Total: 38 blocks (13 Definition, 25 Fact).

**Also belongs to this lecture, written out in an earlier file:** `count-graphs`


---

## Trees

### `forest-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G is a forest |
| **Gives** | G contains no cycle (G is acyclic) |
| **Formal** | G forest ⟹ G has no subgraph isomorphic to a cycle |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is a forest, G contains no cycle.” |
| **Source** | L3 slide 9 |

### `forest-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G contains no cycle (G is acyclic) |
| **Gives** | G is a forest |
| **Formal** | G has no subgraph isomorphic to a cycle ⟹ G forest |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “G contains no cycle, hence G is a forest.” |
| **Source** | L3 slide 9 |

### `tree-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree |
| **Gives** | G contains no cycle (G is acyclic)<br>G is connected |
| **Formal** | G tree ⟹ G acyclic ∧ G connected |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is a tree, G is connected and contains no cycle.” |
| **Source** | L3 slide 9 |

### `tree-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G contains no cycle (G is acyclic)<br>G is connected |
| **Gives** | G is a tree |
| **Formal** | G acyclic ∧ G connected ⟹ G tree |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “G is connected and contains no cycle, hence G is a tree.” |
| **Source** | L3 slide 9 |

### `leaf-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | v is a leaf of G |
| **Gives** | deg(v) = 1 |
| **Formal** | v leaf of G ⟹ deg_G(v) = 1 |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since v is a leaf, deg(v) = 1: v has exactly one neighbor.” |
| **Source** | L3 slide 9 |

### `leaf-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | deg(v) = 1 |
| **Gives** | v is a leaf of G |
| **Formal** | deg_G(v) = 1 ⟹ v leaf of G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “deg(v) = 1, hence v is a leaf.” |
| **Source** | L3 slide 9 |

### `subgraph-acyclic`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G contains no cycle (G is acyclic)<br>H is a subgraph of G |
| **Gives** | H contains no cycle |
| **Formal** | G acyclic ∧ H ⊆ G ⟹ H acyclic |
| **Proof** | A cycle in H consists of vertices of V(H) ⊆ V(G) and edges of E(H) ⊆ E(G), so it would be a cycle in G. ∎ |
| **Say** | “H is a subgraph of the acyclic graph G, so H contains no cycle either.” |
| **Source** | L3 slide 12 |

### `cycle-edge-removal`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is connected<br>e is an edge of a cycle of G |
| **Gives** | G − e is connected |
| **Formal** | G connected ∧ e ∈ E(C) for a cycle C ⊆ G ⟹ G − e connected |
| **Proof** | Let e = {x,y} and let C be a cycle containing e. Removing e from C leaves an x-y-path Q in G − e. Let u, v ∈ V(G); by connected-unpack there is a u-v-path P in G. If e ∉ E(P), then P is a path in G − e. Otherwise replace the edge e in P by Q (traversed in the right direction); this gives a walk from u to v in G − e, and by walk-to-path there is a u-v-path in G − e. By connected-pack, G − e is connected. ∎ |
| **Say** | “e lies on a cycle, so the rest of the cycle is a detour around e; hence G − e is still connected.” |
| **Source** | L3 slide 17 |

### `tree-two-leaves`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree<br>n ≥ 2 |
| **Gives** | G has at least two leaves |
| **Formal** | G tree ∧ n ≥ 2 ⟹ |{v ∈ V(G) : deg(v) = 1}| ≥ 2 |
| **Proof** | Let P = (v₀,…,vₖ) be a longest path in G. Since G is connected and n ≥ 2, G has an edge, so k ≥ 1 and v₀ ≠ vₖ. We claim deg(v₀) = 1. Clearly v₁ ∈ N(v₀). Suppose v₀ has another neighbor w ≠ v₁. If w = vᵢ for some i ≥ 2, then v₀,v₁,…,vᵢ together with the edge {vᵢ,v₀} form a cycle — a contradiction with G being acyclic. If w ∉ V(P), then (w,v₀,…,vₖ) is a path longer than P — a contradiction with the choice of P. Hence deg(v₀) = 1. By symmetry deg(vₖ) = 1. ∎ |
| **Say** | “By the theorem on the existence of leaves, every tree with at least two vertices has at least two leaves.” |
| **Source** | L3 slide 10 |

### `leaf-removal-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree<br>v is a leaf of G<br>n ≥ 2 |
| **Gives** | G − v is a tree |
| **Formal** | G tree ∧ deg_G(v) = 1 ∧ n ≥ 2 ⟹ G − v tree |
| **Proof** | Connected: let x, y ∈ V ∖ {v} and let P be an x-y-path in G (connected-unpack). If v ∈ V(P), then v is an inner vertex of P, so it has two different neighbors on P, contradicting deg(v) = 1. Hence P is a path in G − v. Acyclic: G − v is a subgraph of G, so by subgraph-acyclic it contains no cycle. By tree-pack, G − v is a tree. ∎ |
| **Say** | “Removing a leaf from a tree gives a tree.” |
| **Source** | L3 slides 11–12 |

### `leaf-addition-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G − v is a tree<br>v is a leaf of G |
| **Gives** | G is a tree |
| **Formal** | G − v tree ∧ deg_G(v) = 1 ⟹ G tree |
| **Proof** | Let w be the unique neighbor of v. Acyclic: a cycle of G not containing v lies in G − v, which is acyclic; a cycle containing v would give v two neighbors, contradicting deg(v) = 1. Connected: for x, y ≠ v there is an x-y-path in G − v, hence in G. For x ≠ v there is an x-w-path in G − v; it does not contain v, so extending it by the edge {w,v} gives an x-v-path in G. By tree-pack, G is a tree. ∎ |
| **Say** | “Adding a leaf to a tree gives a tree.” |
| **Source** | L3 slides 11, 13 |

### `tree-unique-paths`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree |
| **Gives** | for every two vertices u, v of G there is exactly one u-v-path in G |
| **Formal** | G tree ⟹ ∀u, v ∈ V(G): ∃! u-v-path in G |
| **Proof** | Existence: G is connected. Uniqueness: suppose P₁ = (a₁,…,aₖ) and P₂ = (b₁,…,b_ℓ) are two different u-v-paths. Neither is an initial part of the other (the end v would repeat), so there is a smallest i with aᵢ = bᵢ and aᵢ₊₁ ≠ bᵢ₊₁. Let p > i be the smallest index with a_p ∈ {bᵢ₊₁,…,b_ℓ}; it exists because aₖ = b_ℓ. Say a_p = b_q, q > i. Then aᵢ,aᵢ₊₁,…,a_p = b_q,b_{q−1},…,bᵢ₊₁ are pairwise distinct (by the choice of p) and consecutive ones are adjacent, as are bᵢ₊₁ and bᵢ = aᵢ. Their number is (p − i) + (q − i) ≥ 3, since p − i = q − i = 1 would give aᵢ₊₁ = bᵢ₊₁. So they form a cycle in G — a contradiction. ∎ |
| **Say** | “In a tree, any two vertices are joined by exactly one path.” |
| **Source** | L3 slide 15 (1 ⇒ 2) |

### `unique-paths-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | for every two vertices u, v of G there is exactly one u-v-path in G |
| **Gives** | G is a tree |
| **Formal** | (∀u, v: ∃! u-v-path) ⟹ G tree |
| **Proof** | G is connected by connected-pack. Suppose G contains a cycle with vertices c₁,c₂,…,c_m in this order, m ≥ 3. Then (c₁,c₂) and (c₁,c_m,c_{m−1},…,c₂) are two different c₁-c₂-paths — a contradiction. So G is acyclic, and by tree-pack a tree. ∎ |
| **Say** | “Any two vertices are joined by exactly one path, so G is connected, and G has no cycle because a cycle gives two paths between two of its vertices.” |
| **Source** | L3 slide 16 (2 ⇒ 1) |

### `tree-edges-are-bridges`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree |
| **Gives** | G − e is disconnected for every edge e of G |
| **Formal** | G tree ⟹ ∀e ∈ E(G): G − e disconnected |
| **Proof** | For the sake of contradiction, suppose G − e is connected for some e = {u,v} ∈ E. Then there is a u-v-path in G − e; it does not use e, so it has length at least 2, and together with e it forms a cycle in G. This contradicts G being acyclic. ∎ |
| **Say** | “In a tree, removing any edge disconnects the graph.” |
| **Source** | L3 slide 17 (1 ⇒ 3) |

### `bridges-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is connected<br>G − e is disconnected for every edge e of G |
| **Gives** | G is a tree |
| **Formal** | G connected ∧ (∀e ∈ E(G): G − e disconnected) ⟹ G tree |
| **Proof** | It suffices to show that G is acyclic. Suppose G contains a cycle C and let e ∈ E(C). By cycle-edge-removal, G − e is connected, contradicting the assumption. Hence G is acyclic and connected; by tree-pack G is a tree. ∎ |
| **Say** | “G is connected and removing any edge disconnects it, so no edge lies on a cycle: G is a tree.” |
| **Source** | L3 slide 18 (3 ⇒ 1) |

### `tree-edge-count`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree |
| **Gives** | |E(G)| = n − 1 |
| **Formal** | G tree ⟹ |E(G)| = |V(G)| − 1 |
| **Proof** | By induction on n. For n = 1 there is no edge, and 0 = 1 − 1. Let n > 1. By tree-two-leaves G has a leaf v, and by leaf-removal-tree G′ = G − v is a tree on n − 1 vertices. By the induction hypothesis |E(G′)| = n − 2. G′ arises from G by deleting v and its single edge, so |E(G)| = |E(G′)| + 1 = n − 1. ∎ |
| **Say** | “A tree on n vertices has exactly n − 1 edges.” |
| **Source** | L3 slide 19 (1 ⇒ 4) |

### `edge-count-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is connected<br>|E(G)| = n − 1 |
| **Gives** | G is a tree |
| **Formal** | G connected ∧ |E(G)| = |V(G)| − 1 ⟹ G tree |
| **Proof** | By induction on n. For n = 1 the graph has no edge and is a tree. Let n > 1. By degree-sum, Σ deg(u) = 2|E| = 2n − 2 < 2n, so some vertex v has deg(v) ≤ 1. By connected-min-degree deg(v) ≥ 1, so v is a leaf. G′ = G − v is connected (a path between two other vertices cannot pass through the leaf v) and |E(G′)| = |E| − 1 = (n − 1) − 1. By the induction hypothesis G′ is a tree, and by leaf-addition-tree G is a tree. ∎ |
| **Say** | “G is connected and has n − 1 edges, hence G is a tree.” |
| **Source** | L3 slide 20 (4 ⇒ 1) |

### `tree-degree-sum`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | |E(G)| = n − 1<br>Σ deg(v) = 2·|E(G)| |
| **Gives** | Σ deg(v) = 2n − 2 |
| **Formal** | |E| = n − 1 ⟹ Σ_{v∈V} deg(v) = 2n − 2 |
| **Proof** | Σ deg(v) = 2|E| = 2(n − 1). ∎ |
| **Say** | “A tree has n − 1 edges, so by the Degree Sum Formula its degrees sum to 2n − 2.” |
| **Source** | L3 slide 20 |

### `tree-leaves-max-degree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree<br>Δ ≥ 2 is the maximum degree of G |
| **Gives** | G has at least Δ leaves |
| **Formal** | G tree ∧ Δ(G) ≥ 2 ⟹ G has at least Δ(G) leaves |
| **Proof** | Let ℓ be the number of leaves and x a vertex with deg(x) = Δ ≥ 2 (so x is not a leaf and n ≥ 3). By connected-min-degree every vertex has degree at least 1, so every vertex that is neither a leaf nor x has degree at least 2. Hence Σ deg(v) ≥ ℓ + Δ + 2(n − ℓ − 1). By tree-edge-count and tree-degree-sum, Σ deg(v) = 2n − 2. So 2n − 2 ≥ 2n − 2 + Δ − ℓ, i.e. ℓ ≥ Δ. ∎ |
| **Say** | “Counting degrees: one vertex has degree Δ, the leaves have degree 1, all others at least 2, and the total is 2n − 2; this forces at least Δ leaves.” |
| **Source** | T2 Ex 32 |

### `forest-edge-count`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a forest with c connected components |
| **Gives** | |E(G)| = n − c |
| **Formal** | G forest with c components ⟹ |E(G)| = n − c |
| **Proof** | Let H₁,…,H_c be the components, with nᵢ vertices. Each Hᵢ is connected and, by subgraph-acyclic, acyclic; so it is a tree and by tree-edge-count |E(Hᵢ)| = nᵢ − 1. By components-partition Σ nᵢ = n, and by no-edge-between-components every edge of G lies in exactly one component. Hence |E(G)| = Σ (nᵢ − 1) = n − c. ∎ |
| **Say** | “Each component of a forest is a tree, so a forest with c components has n − c edges.” |
| **Source** | L3 slide 9 |

### `tree-add-edge-cycle`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is a tree |
| **Gives** | for every two non-adjacent vertices u, v of G, the graph G + {u,v} contains a cycle |
| **Formal** | G tree ⟹ ∀ non-adjacent u ≠ v: G + {u,v} contains a cycle |
| **Proof** | Let u ≠ v be non-adjacent. G is connected, so there is a u-v-path P in G; since {u,v} ∉ E(G), P has length at least 2. P together with the new edge {u,v} is a cycle in G + {u,v}. ∎ |
| **Say** | “In a tree, two non-adjacent vertices are joined by a path of length at least 2; adding the edge between them closes a cycle.” |
| **Source** | T2 Ex 31 (⇒) |

### `maximal-acyclic-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G contains no cycle (G is acyclic)<br>for every two non-adjacent vertices u, v of G, the graph G + {u,v} contains a cycle |
| **Gives** | G is a tree |
| **Formal** | G acyclic ∧ (∀ non-adjacent u ≠ v: G + {u,v} contains a cycle) ⟹ G tree |
| **Proof** | Let u ≠ v ∈ V(G). If {u,v} ∈ E(G), then (u,v) is a u-v-path. Otherwise G + {u,v} contains a cycle C. C is not a cycle of G (G is acyclic), so C contains the edge {u,v}; removing this edge from C leaves a u-v-path in G. So any two vertices are joined by a path; by connected-pack G is connected, and by tree-pack G is a tree. ∎ |
| **Say** | “G has no cycle, but adding any edge creates one; the cycle must use the new edge, and the rest of it is a path joining its ends. So G is connected, hence a tree.” |
| **Source** | T2 Ex 31 (⇐) |

### `path-is-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G = Pₙ |
| **Gives** | G is a tree |
| **Formal** | G = Pₙ ⟹ G tree |
| **Proof** | Pₙ is connected: for i < j, (i,i+1,…,j) is an i-j-path. By path-graph-unpack it has n vertices and n − 1 edges. By edge-count-tree it is a tree. ∎ |
| **Say** | “The path Pₙ is connected and has n − 1 edges, hence it is a tree.” |
| **Source** | L3 slide 10 (note) |


---

## Spanning trees

### `spanning-tree-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | T is a spanning tree of G |
| **Gives** | T is a subgraph of G<br>V(T) = V(G)<br>T is a tree |
| **Formal** | T spanning tree of G ⟹ T ⊆ G ∧ V(T) = V(G) ∧ T tree |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since T is a spanning tree of G, T is a subgraph of G, V(T) = V(G), and T is a tree.” |
| **Source** | L3 slide 22 |

### `spanning-tree-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | T is a subgraph of G<br>V(T) = V(G)<br>T is a tree |
| **Gives** | T is a spanning tree of G |
| **Formal** | T ⊆ G ∧ V(T) = V(G) ∧ T tree ⟹ T spanning tree of G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “T is a subgraph of G on all vertices of G, and T is a tree; hence T is a spanning tree of G.” |
| **Source** | L3 slide 22 |

### `spanning-tree-exists`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is connected |
| **Gives** | G has a spanning tree |
| **Formal** | G connected ⟹ ∃T: T spanning tree of G |
| **Proof** | Consider all connected subgraphs of G with vertex set V(G); G is one of them. Choose one, T, with the minimum number of edges. If T contained a cycle C, then for e ∈ E(C) the graph T − e would be connected by cycle-edge-removal, a connected subgraph on V(G) with fewer edges — a contradiction. So T is acyclic and connected, i.e. a tree, with V(T) = V(G). ∎ |
| **Say** | “Every connected graph has a spanning tree.” |
| **Source** | L3 slides 22–25 |

### `spanning-tree-connected`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G has a spanning tree |
| **Gives** | G is connected |
| **Formal** | G has a spanning tree ⟹ G connected |
| **Proof** | Let T be a spanning tree and u, v ∈ V(G) = V(T). T is connected, so there is a u-v-path in T; by subgraph-path it is a path in G. By connected-pack, G is connected. ∎ |
| **Say** | “G has a spanning tree; paths in the tree are paths in G, so G is connected.” |
| **Source** | L3 slide 22 |

### `spanning-tree-edge-count`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | V(T) = V(G)<br>T is a tree |
| **Gives** | |E(T)| = n − 1 |
| **Formal** | T spanning tree of G ⟹ |E(T)| = |V(G)| − 1 |
| **Proof** | T is a tree with |V(T)| = |V(G)| = n; apply tree-edge-count to T. ∎ |
| **Say** | “A spanning tree of G is a tree on n vertices, so it has n − 1 edges.” |
| **Source** | L3 slide 22 |

### `connected-min-edges`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G has a spanning tree |
| **Gives** | |E(G)| ≥ n − 1 |
| **Formal** | G connected ⟹ |E(G)| ≥ n − 1 |
| **Proof** | Let T be a spanning tree of G. Then E(T) ⊆ E(G) and by spanning-tree-edge-count |E(T)| = n − 1. ∎ |
| **Say** | “A connected graph contains a spanning tree with n − 1 edges, so it has at least n − 1 edges.” |
| **Source** | L3 slide 22 |

### `spanning-tree-exchange`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | T is a spanning tree of G<br>e ∈ E(G) ∖ E(T) |
| **Gives** | there is an edge e′ ∈ E(T) such that (T + e) − e′ is a spanning tree of G |
| **Formal** | T spanning tree of G ∧ e ∈ E(G) ∖ E(T) ⟹ ∃e′ ∈ E(T): (T + e) − e′ spanning tree of G |
| **Proof** | The ends of e are not adjacent in T, so by tree-add-edge-cycle T + e contains a cycle C, and C contains e because T is acyclic. C has at least 3 edges; choose e′ ∈ E(C), e′ ≠ e, so e′ ∈ E(T). T + e is connected, so by cycle-edge-removal T′ = (T + e) − e′ is connected. It has (n − 1) + 1 − 1 = n − 1 edges, so by edge-count-tree T′ is a tree. V(T′) = V(G) and E(T′) ⊆ E(G), so T′ is a spanning tree of G. ∎ |
| **Say** | “Adding e to the spanning tree creates a cycle; removing another edge of that cycle gives a spanning tree again.” |
| **Source** | T3 Ex 1 |

### `edge-in-spanning-tree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G is connected<br>e ∈ E(G) |
| **Gives** | G has a spanning tree that contains e |
| **Formal** | G connected ∧ e ∈ E(G) ⟹ ∃T spanning tree of G: e ∈ E(T) |
| **Proof** | By spanning-tree-exists G has a spanning tree T. If e ∈ E(T) we are done. Otherwise, by spanning-tree-exchange there is e′ ∈ E(T) such that (T + e) − e′ is a spanning tree of G, and it contains e. ∎ |
| **Say** | “Take any spanning tree; if it does not contain e, exchange e into it.” |
| **Source** | T3 Ex 3 |

### `cycle-spanning-trees`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | G = Cₙ |
| **Gives** | G has exactly n spanning trees |
| **Formal** | G = Cₙ ⟹ #{spanning trees of G} = n |
| **Proof** | By spanning-tree-edge-count a spanning tree has n − 1 edges, and Cₙ has n edges, so a spanning tree arises by removing exactly one edge. Removing any edge e leaves a connected graph (cycle-edge-removal) with n − 1 edges, which is a tree by edge-count-tree. The n choices of e give n different spanning trees. ∎ |
| **Say** | “A spanning tree of Cₙ has n − 1 of its n edges, and removing any one edge leaves a path; so Cₙ has exactly n spanning trees.” |
| **Source** | T3 Ex 5 |


---

## Directed graphs

### `symmetrization-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G is a directed graph |
| **Gives** | sym(G) is the undirected graph on V(G) with {u,v} ∈ E(sym(G)) ⟺ (u,v) ∈ E(G) or (v,u) ∈ E(G) |
| **Formal** | sym(G) := (V, E′) with {u,v} ∈ E′ ⟺ (u,v) ∈ E ∨ (v,u) ∈ E |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “The symmetrization sym(G) forgets the directions of all arcs.” |
| **Source** | L3 slide 5 |

### `weakly-connected-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G is weakly connected |
| **Gives** | sym(G) is connected |
| **Formal** | G weakly connected ⟹ sym(G) connected |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is weakly connected, its symmetrization sym(G) is connected.” |
| **Source** | L3 slide 5 |

### `weakly-connected-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | sym(G) is connected |
| **Gives** | G is weakly connected |
| **Formal** | sym(G) connected ⟹ G weakly connected |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “sym(G) is connected, hence G is weakly connected.” |
| **Source** | L3 slide 5 |

### `strongly-connected-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | G is strongly connected |
| **Gives** | for every two vertices u, v there is a directed path from u to v and a directed path from v to u |
| **Formal** | G strongly connected ⟹ ∀u, v ∈ V: ∃ directed u-v-path ∧ ∃ directed v-u-path |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is strongly connected, for every two vertices u, v there is a directed path from u to v and one from v to u.” |
| **Source** | L3 slide 6 |

### `strongly-connected-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 3 |
| **Needs** | for every two vertices u, v there is a directed path from u to v and a directed path from v to u |
| **Gives** | G is strongly connected |
| **Formal** | (∀u, v ∈ V: ∃ directed u-v-path ∧ ∃ directed v-u-path) ⟹ G strongly connected |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Any two vertices are joined by directed paths in both directions, hence G is strongly connected.” |
| **Source** | L3 slide 6 |

### `strong-implies-weak`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 3 |
| **Needs** | for every two vertices u, v there is a directed path from u to v and a directed path from v to u |
| **Gives** | sym(G) is connected |
| **Formal** | G strongly connected ⟹ sym(G) connected |
| **Proof** | Let u, v ∈ V. There is a directed path (u = v₀,…,vₖ = v) with (vᵢ₋₁,vᵢ) ∈ E for all i. By the definition of sym(G), {vᵢ₋₁,vᵢ} ∈ E(sym(G)) whenever vᵢ₋₁ ≠ vᵢ, so the same sequence is a walk from u to v in sym(G); by walk-to-path there is a u-v-path. By connected-pack, sym(G) is connected. ∎ |
| **Say** | “Forgetting directions turns a directed path into a walk of sym(G), so a strongly connected graph is weakly connected.” |
| **Source** | L3 slides 5–6 |
