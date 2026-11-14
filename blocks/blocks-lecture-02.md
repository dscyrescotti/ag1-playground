# Blocks — Lecture 2

Every block is a rule: **if you have everything under Needs, you may write the Say sentence and you then have everything under Gives.**

- **Definition** blocks come in pairs: `-unpack` (word → meaning) and `-pack` (meaning → word).
- **Fact** blocks go one way only.
- **Formal** is the block as a mathematical claim; **Proof** proves that claim.

Total: 44 blocks (16 Definition, 28 Fact).

**Also belongs to this lecture, written out in an earlier file:** `degree-sum`, `subgraph-unpack`, `subgraph-pack`, `induced-unpack`, `induced-pack`, `induced-is-subgraph`, `induced-by-vertex-set`


---

## Subgraphs

### `induced-notation`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | V′ ⊆ V(G) and V′ ≠ ∅ |
| **Gives** | G[V′] has vertex set V′ and edge set E(G) ∩ (V′ choose 2)<br>G[V′] is an induced subgraph of G |
| **Formal** | ∅ ≠ V′ ⊆ V(G) ⟹ G[V′] := (V′, E(G) ∩ (V′ choose 2)) is an induced subgraph of G |
| **Proof** | By definition. G[V′] is a graph because V′ is nonempty and finite, and it satisfies the definition of an induced subgraph with V(H) = V′. ∎ |
| **Say** | “G[V′] denotes the subgraph of G induced by V′: its vertex set is V′ and its edges are all edges of G with both endpoints in V′.” |
| **Source** | L2 slide 2 |

### `vertex-deletion`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | v ∈ V(G)<br>n ≥ 2 |
| **Gives** | G − v = G[V(G) ∖ {v}] |
| **Formal** | v ∈ V(G), n ≥ 2 ⟹ G − v := G[V(G) ∖ {v}] |
| **Proof** | By definition. Since n ≥ 2, the set V(G) ∖ {v} is nonempty, so G − v is a graph. ∎ |
| **Say** | “G − v denotes the graph obtained from G by deleting the vertex v together with all edges incident with v.” |
| **Source** | L2 slide 2 |

### `delete-vertex-edges`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G − v = G[V(G) ∖ {v}] |
| **Gives** | |E(G − v)| = |E(G)| − deg(v) |
| **Formal** | |E(G − v)| = |E(G)| − deg_G(v) |
| **Proof** | E(G − v) = E(G) ∩ (V ∖ {v} choose 2) = E(G) ∖ {e ∈ E(G) | v ∈ e}. The removed set has exactly deg_G(v) elements by the definition of the degree. ∎ |
| **Say** | “Deleting v removes exactly the deg(v) edges incident with v.” |
| **Source** | L2 slide 2 |

### `subgraph-path`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | H is a subgraph of G<br>v₀,…,vₖ is a path of length k in H |
| **Gives** | v₀,…,vₖ is a path of length k in G |
| **Formal** | H ⊆ G ∧ (v₀,…,vₖ) path in H ⟹ (v₀,…,vₖ) path in G |
| **Proof** | The vertices v₀,…,vₖ are pairwise distinct and lie in V(H) ⊆ V(G), and {vᵢ₋₁,vᵢ} ∈ E(H) ⊆ E(G) for all i. ∎ |
| **Say** | “H is a subgraph of G, so every path in H is also a path in G.” |
| **Source** | L2 slide 2 |

### `clique-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | W is a clique in G |
| **Gives** | every two distinct vertices of W are adjacent in G |
| **Formal** | W clique in G ⟹ ∀u ≠ v ∈ W: {u,v} ∈ E(G) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since W is a clique, every two distinct vertices of W are adjacent.” |
| **Source** | L2 slide 5 |

### `clique-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | every two distinct vertices of W are adjacent in G |
| **Gives** | W is a clique in G |
| **Formal** | (∀u ≠ v ∈ W: {u,v} ∈ E(G)) ⟹ W clique in G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Every two distinct vertices of W are adjacent, hence W is a clique.” |
| **Source** | L2 slide 5 |

### `clique-induces-complete`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | every two distinct vertices of W are adjacent in G |
| **Gives** | G[W] is a complete graph on |W| vertices |
| **Formal** | (∀u ≠ v ∈ W: {u,v} ∈ E(G)) ⟹ G[W] = (W, (W choose 2)) |
| **Proof** | The assumption says (W choose 2) ⊆ E(G). Hence E(G[W]) = E(G) ∩ (W choose 2) = (W choose 2), the edge set of the complete graph on W. ∎ |
| **Say** | “All pairs of vertices of W are edges of G, so G[W] is a complete graph.” |
| **Source** | L2 slide 5 |


---

## Connectivity

### `connected-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | G is connected |
| **Gives** | for every two vertices u, v of G there is a u-v-path in G |
| **Formal** | G connected ⟹ ∀u, v ∈ V(G): ∃ u-v-path in G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since G is connected, for every two vertices u, v there is a u-v-path in G.” |
| **Source** | L2 slide 12 |

### `connected-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | for every two vertices u, v of G there is a u-v-path in G |
| **Gives** | G is connected |
| **Formal** | (∀u, v ∈ V(G): ∃ u-v-path in G) ⟹ G connected |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Any two vertices of G are joined by a path, hence G is connected.” |
| **Source** | L2 slide 12 |

### `disconnected-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | G is disconnected |
| **Gives** | there are vertices u, v of G with no u-v-path in G |
| **Formal** | G disconnected ⟹ ∃u, v ∈ V(G): there is no u-v-path in G |
| **Proof** | Disconnected means not connected; negating “∀u, v: ∃ u-v-path” gives “∃u, v: no u-v-path”. ∎ |
| **Say** | “Since G is disconnected, there are vertices u, v with no u-v-path in G.” |
| **Source** | L2 slide 12 |

### `disconnected-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | there are vertices u, v of G with no u-v-path in G |
| **Gives** | G is disconnected |
| **Formal** | (∃u, v ∈ V(G): there is no u-v-path in G) ⟹ G disconnected |
| **Proof** | The pair u, v violates the definition of a connected graph. ∎ |
| **Say** | “The vertices u and v are not joined by any path, hence G is disconnected.” |
| **Source** | L2 slide 12 |

### `path-relation-equivalence`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G is a graph on n vertices |
| **Gives** | u ↭ v ⟺ (∃ u-v-path in G) is an equivalence relation on V(G) |
| **Formal** | ↭ is reflexive, symmetric and transitive on V(G) |
| **Proof** | Reflexive: (u) is a u-u-path of length 0. Symmetric: if (v₀,…,vₖ) is a u-v-path, then (vₖ,…,v₀) is a v-u-path, because edges are unordered pairs. Transitive: if (u = a₀,…,aₖ = v) and (v = b₀,…,b_ℓ = w) are paths, then (a₀,…,aₖ,b₁,…,b_ℓ) is a walk from u to w, and by walk-to-path there is a u-w-path. ∎ |
| **Say** | “The relation “there is a u-v-path” is an equivalence relation on V(G).” |
| **Source** | L2 slide 14 |

### `component-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | H is a connected component of G |
| **Gives** | H is an induced subgraph of G<br>H is connected<br>no connected subgraph F ≠ H of G contains H |
| **Formal** | H component of G ⟹ H induced subgraph ∧ H connected ∧ ¬∃F ⊆ G connected: H ⊆ F, F ≠ H |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since H is a connected component, H is an induced subgraph of G, H is connected, and no larger connected subgraph of G contains H.” |
| **Source** | L2 slide 13 |

### `component-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | H is an induced subgraph of G<br>H is connected<br>no connected subgraph F ≠ H of G contains H |
| **Gives** | H is a connected component of G |
| **Formal** | H induced subgraph ∧ H connected ∧ ¬∃F ⊆ G connected: H ⊆ F, F ≠ H ⟹ H component of G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “H is an induced connected subgraph of G that is not contained in any larger connected subgraph, hence H is a connected component of G.” |
| **Source** | L2 slide 13 |

### `component-classes`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | u ↭ v ⟺ (∃ u-v-path in G) is an equivalence relation on V(G) |
| **Gives** | the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Formal** | {V(H) | H component of G} = V(G)/↭ |
| **Proof** | (⊇) Let C be an equivalence class. (1) G[C] is connected: for u, v ∈ C there is a u-v-path P in G; every vertex x of P satisfies u ↭ x (use the initial part of P), so x ∈ C, and P is a path in G[C]. (2) G[C] is maximal: let F ⊆ G be connected with G[C] ⊆ F. For x ∈ V(F) and u ∈ C there is a u-x-path in F, hence in G, so x ∈ C. Thus V(F) = C and E(F) ⊆ E(G) ∩ (C choose 2) = E(G[C]), i.e. F = G[C]. So G[C] is a component. (⊆) Let H be a component, u ∈ V(H), and C the class of u. H is connected, so every x ∈ V(H) has a u-x-path in H ⊆ G; hence V(H) ⊆ C. As H is induced, H = G[V(H)] ⊆ G[C]. G[C] is connected by (1), so by the maximality of H, H = G[C] and V(H) = C. ∎ |
| **Say** | “The connected components of G are exactly the subgraphs induced by the equivalence classes of ↭.” |
| **Source** | L2 slide 14 |

### `components-partition`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Gives** | every vertex of G lies in exactly one connected component of G |
| **Formal** | ∀v ∈ V(G): ∃! component H of G with v ∈ V(H) |
| **Proof** | The equivalence classes of an equivalence relation on V(G) partition V(G): every vertex lies in exactly one class. By component-classes the classes are the vertex sets of the components. ∎ |
| **Say** | “The components correspond to the classes of an equivalence relation, so every vertex lies in exactly one connected component.” |
| **Source** | L2 slide 14 |

### `no-edge-between-components`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Gives** | no edge of G joins two different connected components of G |
| **Formal** | {u,v} ∈ E(G) ⟹ u, v lie in the same component of G |
| **Proof** | If {u,v} ∈ E(G), then (u,v) is a u-v-path, so u ↭ v, and u, v lie in the same equivalence class. By component-classes this class is the vertex set of one component. ∎ |
| **Say** | “An edge {u,v} is a u-v-path, so its endpoints lie in the same connected component: no edge joins two different components.” |
| **Source** | L2 slide 14 |

### `connected-one-component`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G is connected<br>the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Gives** | G has exactly one connected component |
| **Formal** | G connected ⟹ G has exactly one component |
| **Proof** | By connected-unpack, u ↭ v for all u, v ∈ V(G), so ↭ has the single class V(G) (V(G) ≠ ∅). By component-classes, G has exactly one component, namely G[V(G)] = G. ∎ |
| **Say** | “G is connected, so all vertices are in one class of ↭ and G has exactly one connected component.” |
| **Source** | L2 slide 14 (Observation) |

### `one-component-connected`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G has exactly one connected component<br>the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Gives** | G is connected |
| **Formal** | G has exactly one component ⟹ G connected |
| **Proof** | By component-classes, ↭ has exactly one class, which must be V(G). Hence u ↭ v, i.e. there is a u-v-path, for all u, v ∈ V(G). By connected-pack, G is connected. ∎ |
| **Say** | “G has exactly one connected component, so any two vertices lie in it and are joined by a path: G is connected.” |
| **Source** | L2 slide 14 (Observation) |

### `disconnected-two-components`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | there are vertices u, v of G with no u-v-path in G<br>the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Gives** | G has at least two connected components |
| **Formal** | (∃u, v: no u-v-path) ⟹ G has ≥ 2 components |
| **Proof** | u and v are not related by ↭, so they lie in different equivalence classes. By component-classes these are the vertex sets of two different components. ∎ |
| **Say** | “u and v are not joined by a path, so they lie in different connected components: G has at least two components.” |
| **Source** | L2 slide 14 |

### `two-components-disconnected`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G has at least two connected components<br>the vertex sets of the connected components of G are exactly the equivalence classes of ↭ |
| **Gives** | there are vertices u, v of G with no u-v-path in G |
| **Formal** | G has ≥ 2 components ⟹ ∃u, v: no u-v-path in G |
| **Proof** | Choose u and v in two different components. By component-classes they lie in different classes of ↭, i.e. u ↭ v does not hold: there is no u-v-path. ∎ |
| **Say** | “Take u and v in two different components; they lie in different classes of ↭, so there is no u-v-path.” |
| **Source** | L2 slide 14 |

### `connected-min-degree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G is connected<br>n ≥ 2 |
| **Gives** | deg(v) ≥ 1 for every vertex v (no isolated vertex) |
| **Formal** | G connected ∧ n ≥ 2 ⟹ ∀v ∈ V(G): deg(v) ≥ 1 |
| **Proof** | Let v ∈ V(G). Since n ≥ 2 there is a vertex u ≠ v, and by connected-unpack a v-u-path (v = v₀,v₁,…,vₖ = u). As u ≠ v we have k ≥ 1, so v₁ ∈ N(v) and deg(v) ≥ 1. ∎ |
| **Say** | “G is connected and has at least two vertices, so every vertex has a neighbor: every degree is at least 1.” |
| **Source** | T2 Ex 15 |

### `disconnected-complement-connected`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G has at least two connected components<br>no edge of G joins two different connected components of G<br>Ḡ is the complement of G |
| **Gives** | Ḡ is connected |
| **Formal** | G disconnected ⟹ Ḡ connected |
| **Proof** | Let u ≠ v be vertices of Ḡ (for u = v the path of length 0 works). Case 1: u, v lie in different components of G. By no-edge-between-components {u,v} ∉ E(G), so by complement-unpack {u,v} ∈ E(Ḡ) and (u,v) is a u-v-path in Ḡ. Case 2: u, v lie in the same component of G. G has at least two components, so there is a vertex w in another component. Then {u,w}, {v,w} ∉ E(G), hence {u,w}, {w,v} ∈ E(Ḡ), and (u,w,v) is a u-v-path in Ḡ. In both cases there is a u-v-path in Ḡ; by connected-pack Ḡ is connected. ∎ |
| **Say** | “The complement of a disconnected graph is connected.” |
| **Source** | T2 Ex 14 |

### `regular-half-connected`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G is n-regular and has 2n vertices |
| **Gives** | G is connected |
| **Formal** | G n-regular, |V(G)| = 2n ⟹ G connected |
| **Proof** | Let u ≠ v ∈ V(G). If {u,v} ∈ E(G), then (u,v) is a u-v-path. Otherwise u ∉ N(v) and v ∉ N(u), so N(u), N(v) ⊆ V ∖ {u,v}, a set of 2n − 2 elements. Since |N(u)| + |N(v)| = 2n > 2n − 2, the sets N(u) and N(v) are not disjoint (pigeonhole principle); take w ∈ N(u) ∩ N(v). Then (u,w,v) is a u-v-path. By connected-pack G is connected. ∎ |
| **Say** | “Two non-adjacent vertices have n neighbors each among the remaining 2n − 2 vertices, so they have a common neighbor; hence any two vertices are joined by a path of length at most 2.” |
| **Source** | T2 Ex 17 |


---

## Isomorphism

### `isomorphism-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | f is an isomorphism of G and H |
| **Gives** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) |
| **Formal** | f isomorphism of G and H ⟹ f bijection ∧ ∀u, v ∈ V(G): ({u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H)) |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “Since f is an isomorphism, f is a bijection and {u,v} ∈ E(G) if and only if {f(u),f(v)} ∈ E(H).” |
| **Source** | L2 slide 26 |

### `isomorphism-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) |
| **Gives** | f is an isomorphism of G and H |
| **Formal** | f bijection ∧ ∀u, v ∈ V(G): ({u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H)) ⟹ f isomorphism of G and H |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “f is a bijection that preserves edges and non-edges, hence f is an isomorphism of G and H.” |
| **Source** | L2 slide 26 |

### `isomorphic-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | G ≅ H |
| **Gives** | f is an isomorphism of G and H |
| **Formal** | G ≅ H ⟹ ∃f: f isomorphism of G and H |
| **Proof** | This is the definition, read in this direction. Fix one such f. |
| **Say** | “Since G ≅ H, there is an isomorphism f of G and H.” |
| **Source** | L2 slide 27 |

### `isomorphic-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | f is an isomorphism of G and H |
| **Gives** | G ≅ H |
| **Formal** | (∃f: f isomorphism of G and H) ⟹ G ≅ H |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “f is an isomorphism of G and H, hence G ≅ H.” |
| **Source** | L2 slide 27 |

### `automorphism-unpack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | f is an automorphism of G |
| **Gives** | f is an isomorphism of G and G |
| **Formal** | f automorphism of G ⟹ f isomorphism of G and G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “An automorphism of G is an isomorphism of G with itself.” |
| **Source** | L2 slide 28 |

### `automorphism-pack`

| | |
|---|---|
| **Type** | Definition |
| **Lecture** | Lecture 2 |
| **Needs** | f is an isomorphism of G and G |
| **Gives** | f is an automorphism of G |
| **Formal** | f isomorphism of G and G ⟹ f automorphism of G |
| **Proof** | This is the definition, read in this direction. |
| **Say** | “f is an isomorphism of G with itself, hence an automorphism of G.” |
| **Source** | L2 slide 28 |

### `identity-automorphism`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G is a graph on n vertices |
| **Gives** | the identity map on V(G) is an automorphism of G |
| **Formal** | id_{V(G)} is an automorphism of G |
| **Proof** | id is a bijection V(G) → V(G), and {u,v} ∈ E(G) ⟺ {id(u),id(v)} ∈ E(G) trivially. ∎ |
| **Say** | “The identity map is an automorphism of every graph.” |
| **Source** | T2 Ex 28 |

### `iso-same-vertices`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection |
| **Gives** | |V(G)| = |V(H)| |
| **Formal** | f : V(G) → V(H) bijection ⟹ |V(G)| = |V(H)| |
| **Proof** | Two finite sets with a bijection between them have the same number of elements. ∎ |
| **Say** | “f is a bijection between the vertex sets, so G and H have the same number of vertices.” |
| **Source** | T2 Ex 19–21 |

### `iso-same-edges`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) |
| **Gives** | |E(G)| = |E(H)| |
| **Formal** | f isomorphism of G and H ⟹ |E(G)| = |E(H)| |
| **Proof** | Define φ({u,v}) = {f(u),f(v)} for {u,v} ∈ E(G). By (⟹) of the edge condition, φ maps into E(H). φ is one-to-one because f is. φ is onto: for {x,y} ∈ E(H) put u = f⁻¹(x), v = f⁻¹(y); by (⟸), {u,v} ∈ E(G) and φ({u,v}) = {x,y}. So φ is a bijection E(G) → E(H). ∎ |
| **Say** | “An isomorphism maps edges to edges bijectively, so G and H have the same number of edges.” |
| **Source** | T2 Ex 19–21 |

### `iso-preserves-degree`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) |
| **Gives** | deg_H(f(v)) = deg_G(v) for every v ∈ V(G) |
| **Formal** | f isomorphism of G and H ⟹ ∀v ∈ V(G): deg_H(f(v)) = deg_G(v) |
| **Proof** | Let v ∈ V(G). For every w: w ∈ N_G(v) ⟺ {v,w} ∈ E(G) ⟺ {f(v),f(w)} ∈ E(H) ⟺ f(w) ∈ N_H(f(v)). Since f is a bijection, it maps N_G(v) one-to-one onto N_H(f(v)). Hence |N_G(v)| = |N_H(f(v))|. ∎ |
| **Say** | “An isomorphism maps the neighbors of v exactly onto the neighbors of f(v), so it preserves degrees.” |
| **Source** | T2 Ex 19–21 |

### `iso-same-degree-sequence`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>deg_H(f(v)) = deg_G(v) for every v ∈ V(G) |
| **Gives** | G and H have the same degree sequence |
| **Formal** | G ≅ H ⟹ the sorted lists of degrees of G and of H are equal |
| **Proof** | f is a bijection V(G) → V(H) with deg_H(f(v)) = deg_G(v), so every degree value occurs equally often in G and in H. ∎ |
| **Say** | “Isomorphic graphs have the same degree sequence.” |
| **Source** | T2 Ex 19–21 |

### `iso-preserves-paths`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) |
| **Gives** | (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H |
| **Formal** | f isomorphism ⟹ ((v₀,…,vₖ) path in G ⟺ (f(v₀),…,f(vₖ)) path in H) |
| **Proof** | f is one-to-one, so v₀,…,vₖ are pairwise distinct ⟺ f(v₀),…,f(vₖ) are pairwise distinct. By the edge condition, {vᵢ₋₁,vᵢ} ∈ E(G) ⟺ {f(vᵢ₋₁),f(vᵢ)} ∈ E(H) for every i. ∎ |
| **Say** | “An isomorphism maps paths to paths, in both directions.” |
| **Source** | T2 Ex 19–21 |

### `iso-preserves-connectivity`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H<br>f : V(G) → V(H) is a bijection<br>G is connected |
| **Gives** | H is connected |
| **Formal** | G ≅ H ∧ G connected ⟹ H connected |
| **Proof** | Let x, y ∈ V(H), and put u = f⁻¹(x), v = f⁻¹(y). By connected-unpack there is a u-v-path (u = v₀,…,vₖ = v) in G. By iso-preserves-paths, (f(v₀),…,f(vₖ)) is a path in H from x to y. By connected-pack, H is connected. ∎ |
| **Say** | “G is connected and the isomorphism maps paths of G to paths of H, so H is connected.” |
| **Source** | T2 Ex 19–21 |

### `iso-inverse`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) |
| **Gives** | f⁻¹ is an isomorphism of H and G |
| **Formal** | f isomorphism of G and H ⟹ f⁻¹ isomorphism of H and G |
| **Proof** | f⁻¹ : V(H) → V(G) is a bijection. For x, y ∈ V(H) put u = f⁻¹(x), v = f⁻¹(y). Then {x,y} ∈ E(H) ⟺ {f(u),f(v)} ∈ E(H) ⟺ {u,v} ∈ E(G) ⟺ {f⁻¹(x),f⁻¹(y)} ∈ E(G). ∎ |
| **Say** | “The inverse of an isomorphism is an isomorphism.” |
| **Source** | T2 Ex 22 |

### `isomorphic-symmetric`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f⁻¹ is an isomorphism of H and G |
| **Gives** | H ≅ G |
| **Formal** | G ≅ H ⟹ H ≅ G |
| **Proof** | By iso-inverse there is an isomorphism of H and G; apply the definition of H ≅ G. ∎ |
| **Say** | “f⁻¹ is an isomorphism of H and G, hence H ≅ G.” |
| **Source** | L2 slide 27 |

### `iso-compose`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f is an isomorphism of G and H<br>g is an isomorphism of H and J |
| **Gives** | g ∘ f is an isomorphism of G and J |
| **Formal** | f isomorphism of G, H ∧ g isomorphism of H, J ⟹ g ∘ f isomorphism of G, J |
| **Proof** | g ∘ f is a bijection V(G) → V(J) as a composition of bijections. For u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) ⟺ {g(f(u)),g(f(v))} ∈ E(J). ∎ |
| **Say** | “The composition of two isomorphisms is an isomorphism, so ≅ is transitive.” |
| **Source** | L2 slide 27 |

### `iso-complement`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f : V(G) → V(H) is a bijection<br>for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H)<br>Ḡ and H̄ are the complements of G and H |
| **Gives** | f is an isomorphism of Ḡ and H̄ |
| **Formal** | f isomorphism of G, H ⟹ f isomorphism of Ḡ, H̄ |
| **Proof** | V(Ḡ) = V(G) and V(H̄) = V(H), so f is a bijection V(Ḡ) → V(H̄). Let u, v ∈ V(G). If u = v, neither {u,v} nor {f(u),f(v)} is an edge. If u ≠ v then f(u) ≠ f(v), and by complement-unpack: {u,v} ∈ E(Ḡ) ⟺ {u,v} ∉ E(G) ⟺ {f(u),f(v)} ∉ E(H) ⟺ {f(u),f(v)} ∈ E(H̄). ∎ |
| **Say** | “The same bijection f is an isomorphism of the complements, because it preserves non-edges as well.” |
| **Source** | T2 Ex 22 |

### `complements-isomorphic`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | f is an isomorphism of Ḡ and H̄ |
| **Gives** | Ḡ ≅ H̄ |
| **Formal** | G ≅ H ⟹ Ḡ ≅ H̄ |
| **Proof** | Apply the definition of isomorphic graphs to Ḡ, H̄ and f. (The converse follows by applying this to Ḡ, H̄, since the complement of Ḡ is G.) ∎ |
| **Say** | “f is an isomorphism of Ḡ and H̄, hence Ḡ ≅ H̄.” |
| **Source** | T2 Ex 22 |

### `regular-full-is-complete`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G is (n−1)-regular<br>G is a graph on n vertices |
| **Gives** | G = Kₙ |
| **Formal** | G (n−1)-regular on n vertices ⟹ G = Kₙ |
| **Proof** | By regular-unpack every vertex u has deg(u) = n − 1, so by universal-vertex N(u) = V ∖ {u}. Hence every two distinct vertices are adjacent, and by complete-pack G = Kₙ. ∎ |
| **Say** | “Every vertex has degree n − 1, so it is adjacent to all other vertices: G is the complete graph Kₙ.” |
| **Source** | T2 Ex 24 |

### `complete-graphs-isomorphic`

| | |
|---|---|
| **Type** | Fact |
| **Lecture** | Lecture 2 |
| **Needs** | G = Kₙ<br>H = Kₙ |
| **Gives** | G ≅ H |
| **Formal** | G = Kₙ ∧ H = Kₙ ⟹ G ≅ H |
| **Proof** | |V(G)| = |V(H)| = n, so there is a bijection f : V(G) → V(H). For u ≠ v we have f(u) ≠ f(v), and by complete-unpack both {u,v} ∈ E(G) and {f(u),f(v)} ∈ E(H) hold; for u = v neither holds. So f is an isomorphism. ∎ |
| **Say** | “Any bijection between the vertex sets of two complete graphs on n vertices is an isomorphism.” |
| **Source** | T2 Ex 24 |
