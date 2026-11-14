# Index by Gives — “I want this fact. Which block produces it?”

Sorted alphabetically by fact, all lectures together.

| I want | Block | and it needs | Lecture |
|---|---|---|---|
| (T, r) is a binary tree | `binary-tree-pack` | (T, r) is a rooted tree; every vertex of T has at most two children, each marked as left or right | 4 |
| (T, r) is a rooted tree | `rooted-tree-pack` | T is a tree; r ∈ V(T) | 4 |
| (T, r) is a rooted tree | `binary-tree-unpack` | (T, r) is a binary tree | 4 |
| (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H | `iso-preserves-paths` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | 2 |
| 0 ≤ deg(v) ≤ n − 1 for every vertex v | `degree-bounds` | G is a graph on n vertices | 1 |
| a shortest uv-walk exists, and its length is d(u, v) | `shortest-walk-is-path` | G contains no negative cycle | 12 |
| all edge lengths are nonnegative | `positive-is-nonnegative` | all edge lengths are positive | 12 |
| C is an induced subgraph of G | `shortest-cycle-induced` | C is a shortest cycle in G | 1 |
| C is an induced subgraph of G | `shortest-odd-cycle-induced` | C is a shortest odd cycle in G | 1 |
| d(s,t) = k | `distance-pack` | there is an s-t-path of length k; no s-t-path has length < k | 1 |
| d(u, v) = k | `weighted-distance-pack` | some uv-path has length k, and every uv-path has length ≥ k (d(u, v) = +∞ if there is no uv-path) | 12 |
| d(u, v) ≤ d(u, w) + d(w, v) for all vertices u, v, w | `triangle-inequality` | G contains no negative cycle | 12 |
| deg(v) = 1 | `leaf-unpack` | v is a leaf of G | 3 |
| deg(v) = k | `degree-pack` | |N(v)| = k | 1 |
| deg(v) = r for every vertex v | `regular-unpack` | G is r-regular | 1 |
| deg(v) ≥ 1 for every vertex v (no isolated vertex) | `universal-excludes-isolated` | u is adjacent to every other vertex of G; n ≥ 2 | 1 |
| deg(v) ≥ 1 for every vertex v (no isolated vertex) | `connected-min-degree` | G is connected; n ≥ 2 | 2 |
| deg(w) = 0 | `isolated-pack` | w is isolated (adjacent to no vertex) | 1 |
| deg_H(f(v)) = deg_G(v) for every v ∈ V(G) | `iso-preserves-degree` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | 2 |
| deg_Ḡ(v) = n − 1 − deg_G(v) for every v | `complement-degree` | Ḡ is the complement of G; G is a graph on n vertices | 1 |
| E(H) contains every edge of G with both endpoints in V(H) | `induced-unpack` | H is an induced subgraph of G | 1, 2 |
| edges are ordered pairs; (u,v) ≠ (v,u); loops (u,u) are allowed | `digraph-unpack` | G is a directed graph | 1 |
| even walk ends in its starting part; odd walk ends in the other part | `bipartite-parity` | G is bipartite with parts A, B | 1 |
| every child of v is at level i + 1 | `child-level` | (T, r) is a rooted tree; v is at level i of (T, r) | 4 |
| every edge e has a length ℓ(e) ∈ ℝ, and a walk W has length ℓ(W) = Σ_{e∈W} ℓ(e) | `weighted-digraph-unpack` | (G, ℓ) is a weighted digraph | 12 |
| every edge is a 2-element subset of V(G): no loops, no multiple edges | `graph-unpack` | G is a graph on n vertices | 1 |
| every edge of G has one endpoint in A and one in B | `bipartite-unpack` | G is bipartite with parts A, B | 1 |
| every two distinct vertices of G are adjacent | `complete-unpack` | G = Kₙ | 1 |
| every two distinct vertices of W are adjacent in G | `clique-unpack` | W is a clique in G | 2 |
| every vertex of G lies in exactly one connected component of G | `components-partition` | the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| every vertex of T has at most two children, each marked as left or right | `binary-tree-unpack` | (T, r) is a binary tree | 4 |
| f : V(G) → V(H) is a bijection | `isomorphism-unpack` | f is an isomorphism of G and H | 2 |
| f is an automorphism of G | `automorphism-pack` | f is an isomorphism of G and G | 2 |
| f is an isomorphism of G and G | `automorphism-unpack` | f is an automorphism of G | 2 |
| f is an isomorphism of G and H | `isomorphism-pack` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | 2 |
| f is an isomorphism of G and H | `isomorphic-unpack` | G ≅ H | 2 |
| f is an isomorphism of Ḡ and H̄ | `iso-complement` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H); Ḡ and H̄ are the complements of G and H | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `isomorphism-unpack` | f is an isomorphism of G and H | 2 |
| for every two non-adjacent vertices u, v of G, the graph G + {u,v} contains a cycle | `tree-add-edge-cycle` | G is a tree | 3 |
| for every two vertices u, v of G there is a u-v-path in G | `connected-unpack` | G is connected | 2 |
| for every two vertices u, v of G there is exactly one u-v-path in G | `tree-unique-paths` | G is a tree | 3 |
| for every two vertices u, v there is a directed path from u to v and a directed path from v to u | `strongly-connected-unpack` | G is strongly connected | 3 |
| for u ≠ v: {u,v} ∈ E(Ḡ) ⟺ {u,v} ∉ E(G) | `complement-unpack` | Ḡ is the complement of G | 1 |
| f⁻¹ is an isomorphism of H and G | `iso-inverse` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | 2 |
| G = Kₙ | `complete-pack` | every two distinct vertices of G are adjacent; G is a graph on n vertices | 1 |
| G = Kₙ | `regular-full-is-complete` | G is (n−1)-regular; G is a graph on n vertices | 2 |
| G and H have the same degree sequence | `iso-same-degree-sequence` | f : V(G) → V(H) is a bijection; deg_H(f(v)) = deg_G(v) for every v ∈ V(G) | 2 |
| G consists of n isolated vertices | `zero-regular-shape` | G is 0-regular | 1 |
| G contains a directed cycle | `directed-cycle-pack` | there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) | 4 |
| G contains a directed cycle | `no-source-cycle` | every vertex of G has an incoming arc | 4 |
| G contains a directed cycle | `mutual-paths-cycle` | u ≠ v, and G has a directed path from u to v and a directed path from v to u | 4 |
| G contains no cycle (G is acyclic) | `forest-unpack` | G is a forest | 3 |
| G contains no cycle (G is acyclic) | `tree-unpack` | G is a tree | 3 |
| G contains no directed cycle | `dag-unpack` | G is a DAG | 4 |
| G contains no directed cycle | `topological-ordering-acyclic` | G has a topological ordering | 4 |
| G contains no negative cycle | `nonnegative-no-negative-cycle` | all edge lengths are nonnegative | 12 |
| G has a directed path that goes through all vertices | `unique-ordering-hamiltonian-path` | G has exactly one topological ordering | 4 |
| G has a sink | `sink-pack` | no arc of G starts in t | 4 |
| G has a sink | `dag-source-sink` | G contains no directed cycle | 4 |
| G has a source | `source-pack` | no arc of G ends in s | 4 |
| G has a source | `dag-source-sink` | G contains no directed cycle | 4 |
| G has a spanning tree | `spanning-tree-exists` | G is connected | 3 |
| G has a spanning tree that contains e | `edge-in-spanning-tree` | G is connected; e ∈ E(G) | 3 |
| G has a topological ordering | `topological-ordering-pack` | v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j | 4 |
| G has a topological ordering | `dag-has-topological-ordering` | G contains no directed cycle | 4 |
| G has at least two connected components | `disconnected-two-components` | there are vertices u, v of G with no u-v-path in G; the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| G has at least two leaves | `tree-two-leaves` | G is a tree; n ≥ 2 | 3 |
| G has at least Δ leaves | `tree-leaves-max-degree` | G is a tree; Δ ≥ 2 is the maximum degree of G | 3 |
| G has exactly n spanning trees | `cycle-spanning-trees` | G = Cₙ | 3 |
| G has exactly one connected component | `connected-one-component` | G is connected; the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| G has exactly one topological ordering | `hamiltonian-path-unique-ordering` | G contains no directed cycle; G has a directed path that goes through all vertices | 4 |
| G has n vertices and n − 1 edges | `path-graph-unpack` | G = Pₙ | 1 |
| G has no topological ordering | `cycle-no-topological-ordering` | there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) | 4 |
| G is (n−1)-regular | `complete-regular` | G = Kₙ | 1 |
| G is 2-regular | `cycle-graph-unpack` | G = Cₙ | 1 |
| G is a DAG | `dag-pack` | G is a directed graph; G contains no directed cycle | 4 |
| G is a directed graph | `weighted-digraph-unpack` | (G, ℓ) is a weighted digraph | 12 |
| G is a directed graph | `dag-unpack` | G is a DAG | 4 |
| G is a disjoint union of cycles | `two-regular-shape` | G is 2-regular | 1 |
| G is a disjoint union of edges | `one-regular-shape` | G is 1-regular | 1 |
| G is a forest | `forest-pack` | G contains no cycle (G is acyclic) | 3 |
| G is a tree | `tree-pack` | G contains no cycle (G is acyclic); G is connected | 3 |
| G is a tree | `leaf-addition-tree` | G − v is a tree; v is a leaf of G | 3 |
| G is a tree | `unique-paths-tree` | for every two vertices u, v of G there is exactly one u-v-path in G | 3 |
| G is a tree | `bridges-tree` | G is connected; G − e is disconnected for every edge e of G | 3 |
| G is a tree | `edge-count-tree` | G is connected; |E(G)| = n − 1 | 3 |
| G is a tree | `maximal-acyclic-tree` | G contains no cycle (G is acyclic); for every two non-adjacent vertices u, v of G, the graph G + {u,v} contains a cycle | 3 |
| G is a tree | `path-is-tree` | G = Pₙ | 3 |
| G is bipartite with parts A, B | `complete-bipartite-is-bipartite` | G = K_{a,b} with parts A, B | 1 |
| G is bipartite with parts A, B | `bipartite-pack` | V(G) = A ∪ B and A ∩ B = ∅; every edge of G has one endpoint in A and one in B | 1 |
| G is connected | `connected-pack` | for every two vertices u, v of G there is a u-v-path in G | 2 |
| G is connected | `one-component-connected` | G has exactly one connected component; the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| G is connected | `regular-half-connected` | G is n-regular and has 2n vertices | 2 |
| G is connected | `tree-unpack` | G is a tree | 3 |
| G is connected | `spanning-tree-connected` | G has a spanning tree | 3 |
| G is disconnected | `disconnected-pack` | there are vertices u, v of G with no u-v-path in G | 2 |
| G is not bipartite | `odd-cycle-not-bipartite` | G contains a cycle of odd length | 1 |
| G is r-regular | `regular-pack` | deg(v) = r for every vertex v | 1 |
| G is strongly connected | `strongly-connected-pack` | for every two vertices u, v there is a directed path from u to v and a directed path from v to u | 3 |
| G is weakly connected | `weakly-connected-pack` | sym(G) is connected | 3 |
| G − e is connected | `cycle-edge-removal` | G is connected; e is an edge of a cycle of G | 3 |
| G − e is disconnected for every edge e of G | `tree-edges-are-bridges` | G is a tree | 3 |
| G − v = G[V(G) ∖ {v}] | `vertex-deletion` | v ∈ V(G); n ≥ 2 | 2 |
| G − v is a tree | `leaf-removal-tree` | G is a tree; v is a leaf of G; n ≥ 2 | 3 |
| g ∘ f is an isomorphism of G and J | `iso-compose` | f is an isomorphism of G and H; g is an isomorphism of H and J | 2 |
| G ≅ H | `isomorphic-pack` | f is an isomorphism of G and H | 2 |
| G ≅ H | `complete-graphs-isomorphic` | G = Kₙ; H = Kₙ | 2 |
| G[V′] has vertex set V′ and edge set E(G) ∩ (V′ choose 2) | `induced-notation` | V′ ⊆ V(G) and V′ ≠ ∅ | 2 |
| G[V′] is an induced subgraph of G | `induced-notation` | V′ ⊆ V(G) and V′ ≠ ∅ | 2 |
| G[W] is a complete graph on |W| vertices | `clique-induces-complete` | every two distinct vertices of W are adjacent in G | 2 |
| H = G[V(H)], so H is determined by its vertex set | `induced-by-vertex-set` | H is an induced subgraph of G | 1, 2 |
| H contains no cycle | `subgraph-acyclic` | G contains no cycle (G is acyclic); H is a subgraph of G | 3 |
| H has exactly ⌈n/2⌉ vertices without children | `heap-leaves` | numbering the vertices 1,…,n level by level from the left: vertex i has children 2i and 2i + 1 and parent ⌊i/2⌋ | 4 |
| H has ⌊log₂ n⌋ + 1 levels | `heap-levels` | heap shape: all levels of H except the last are completely filled, and the last is filled from the left | 4 |
| H is a (minimum) binary heap with n elements | `heap-pack` | H is a binary tree with a key k(x) in every vertex x; heap shape: all levels of H except the last are completely filled, and the last is filled from the left; heap order: k(v) ≤ k(s) whenever s is a child of v | 4 |
| H is a binary tree with a key k(x) in every vertex x | `heap-unpack` | H is a (minimum) binary heap with n elements | 4 |
| H is a connected component of G | `component-pack` | H is an induced subgraph of G; H is connected; no connected subgraph F ≠ H of G contains H | 2 |
| H is a subgraph of G | `subgraph-pack` | V(H) ⊆ V(G) and E(H) ⊆ E(G) | 1, 2 |
| H is a subgraph of G | `induced-is-subgraph` | H is an induced subgraph of G | 1, 2 |
| H is an induced subgraph of G | `induced-pack` | H is a subgraph of G; E(H) contains every edge of G with both endpoints in V(H) | 1, 2 |
| H is an induced subgraph of G | `component-unpack` | H is a connected component of G | 2 |
| H is connected | `component-unpack` | H is a connected component of G | 2 |
| H is connected | `iso-preserves-connectivity` | (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H; f : V(G) → V(H) is a bijection; G is connected | 2 |
| H ≅ G | `isomorphic-symmetric` | f⁻¹ is an isomorphism of H and G | 2 |
| heap order: k(v) ≤ k(s) whenever s is a child of v | `heap-unpack` | H is a (minimum) binary heap with n elements | 4 |
| heap shape: all levels of H except the last are completely filled, and the last is filled from the left | `heap-unpack` | H is a (minimum) binary heap with n elements | 4 |
| if T has ℓ levels, then T has at most 2^ℓ − 1 vertices | `binary-tree-size` | level i of T contains at most 2ⁱ vertices | 4 |
| k ≤ n − 1 | `path-length-bound` | v₀,…,vₖ is a path of length k in G; G is a graph on n vertices | 1 |
| level i of T contains at most 2ⁱ vertices | `binary-level-size` | (T, r) is a rooted tree; every vertex of T has at most two children, each marked as left or right | 4 |
| n is even | `regular-odd-degree` | n·r = 2·|E(G)|; r is odd | 1 |
| n is even | `one-regular-shape` | G is 1-regular | 1 |
| n ≥ 3 and G has n vertices and n edges | `cycle-graph-unpack` | G = Cₙ | 1 |
| no arc of G ends in s | `source-unpack` | s is a source of G | 4 |
| no arc of G starts in t | `sink-unpack` | t is a sink of G | 4 |
| no connected subgraph F ≠ H of G contains H | `component-unpack` | H is a connected component of G | 2 |
| no edge of G joins two different connected components of G | `no-edge-between-components` | the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| no s-t-path has length < k | `distance-unpack` | d(s,t) = k | 1 |
| numbering the vertices 1,…,n level by level from the left: vertex i has children 2i and 2i + 1 and parent ⌊i/2⌋ | `heap-indices` | heap shape: all levels of H except the last are completely filled, and the last is filled from the left | 4 |
| n·r = 2·|E(G)| | `regular-degree-sum` | deg(v) = r for every vertex v; Σ deg(v) = 2·|E(G)| | 1 |
| on the path from any vertex to the root, the keys do not increase | `heap-path-monotone` | heap order: k(v) ≤ k(s) whenever s is a child of v | 4 |
| r ∈ V(T) | `rooted-tree-unpack` | (T, r) is a rooted tree | 4 |
| s is a source of G | `source-pack` | no arc of G ends in s | 4 |
| some uv-path has length k, and every uv-path has length ≥ k (d(u, v) = +∞ if there is no uv-path) | `weighted-distance-unpack` | d(u, v) = k | 12 |
| sym(G) is connected | `weakly-connected-unpack` | G is weakly connected | 3 |
| sym(G) is connected | `strong-implies-weak` | for every two vertices u, v there is a directed path from u to v and a directed path from v to u | 3 |
| sym(G) is the undirected graph on V(G) with {u,v} ∈ E(sym(G)) ⟺ (u,v) ∈ E(G) or (v,u) ∈ E(G) | `symmetrization-unpack` | G is a directed graph | 3 |
| t is a sink of G | `sink-pack` | no arc of G starts in t | 4 |
| T is a spanning tree of G | `spanning-tree-pack` | T is a subgraph of G; V(T) = V(G); T is a tree | 3 |
| T is a subgraph of G | `spanning-tree-unpack` | T is a spanning tree of G | 3 |
| T is a tree | `spanning-tree-unpack` | T is a spanning tree of G | 3 |
| T is a tree | `rooted-tree-unpack` | (T, r) is a rooted tree | 4 |
| the identity map on V(G) is an automorphism of G | `identity-automorphism` | G is a graph on n vertices | 2 |
| the number of odd-degree vertices of G is even | `handshaking` | Σ deg(v) is even | 1 |
| the number of x-y-paths of length k is (n−2)(n−3)···(n−k) | `count-paths-complete` | x ≠ y are vertices of Kₙ | 1 |
| the part of P from u to w is a shortest uw-path, and the part from w to v is a shortest wv-path | `subpath-of-shortest-path` | P is a shortest uv-path and w is a vertex of P; d(u, v) ≤ d(u, w) + d(w, v) for all vertices u, v, w | 12 |
| the root of H holds the minimum key | `heap-min-at-root` | on the path from any vertex to the root, the keys do not increase | 4 |
| the v-r-path in T has length i | `level-unpack` | v is at level i of (T, r) | 4 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `component-classes` | u ↭ v ⟺ (∃ u-v-path in G) is an equivalence relation on V(G) | 2 |
| the vertices v₀,…,vₖ are pairwise distinct | `path-unpack` | v₀,…,vₖ is a path of length k in G | 1 |
| there are exactly 2^(n(n−1)/2) graphs on V | `count-graphs` | V is a fixed vertex set with |V| = n | 1, 3 |
| there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) | `directed-cycle-unpack` | G contains a directed cycle | 4 |
| there are vertices u, v of G with no u-v-path in G | `disconnected-unpack` | G is disconnected | 2 |
| there are vertices u, v of G with no u-v-path in G | `two-components-disconnected` | G has at least two connected components; the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| there is a uv-path P with ℓ(P) ≤ ℓ(W) | `walk-contraction` | G contains no negative cycle; W is a uv-walk in G | 12 |
| there is an edge e′ ∈ E(T) such that (T + e) − e′ is a spanning tree of G | `spanning-tree-exchange` | T is a spanning tree of G; e ∈ E(G) ∖ E(T) | 3 |
| there is an s-t-path in G | `walk-to-path` | there is a walk from s to t in G | 1 |
| there is an s-t-path of length k | `distance-unpack` | d(s,t) = k | 1 |
| two vertices of G have the same degree | `same-degree` | G is a graph on n vertices; n ≥ 2 | 1 |
| u and v are adjacent in G | `adjacent-pack` | {u,v} ∈ E(G) | 1 |
| u and v are adjacent in G | `neighborhood-unpack` | v ∈ N(u) | 1 |
| u is a predecessor of v and v is a successor of u | `successor-unpack` | (u,v) ∈ E(G) | 1 |
| u is adjacent to every other vertex of G | `universal-vertex` | deg(u) = n − 1; G is a graph on n vertices | 1 |
| u is an ancestor of v in (T, r) | `ancestor-pack` | u lies on the v-r-path in T | 4 |
| u is an ancestor of v in (T, r) | `parent-unpack` | u is the parent of v in (T, r) | 4 |
| u is the parent of v in (T, r) | `parent-pack` | u is an ancestor of v in (T, r); {u,v} ∈ E(T) | 4 |
| u lies on the v-r-path in T | `ancestor-unpack` | u is an ancestor of v in (T, r) | 4 |
| u ↭ v ⟺ (∃ u-v-path in G) is an equivalence relation on V(G) | `path-relation-equivalence` | G is a graph on n vertices | 2 |
| u, v adjacent ⟺ u, v lie in different parts | `complete-bipartite-unpack` | G = K_{a,b} with parts A, B | 1 |
| v has exactly one parent | `unique-parent` | (T, r) is a rooted tree; v ≠ r is a vertex of T | 4 |
| v is a leaf of G | `leaf-pack` | deg(v) = 1 | 3 |
| v is at level i of (T, r) | `level-pack` | the v-r-path in T has length i | 4 |
| v ∈ N(u) | `neighborhood-pack` | u and v are adjacent in G | 1 |
| V(G) = A ∪ B and A ∩ B = ∅ | `complete-bipartite-unpack` | G = K_{a,b} with parts A, B | 1 |
| V(G) = A ∪ B and A ∩ B = ∅ | `bipartite-unpack` | G is bipartite with parts A, B | 1 |
| V(G) is nonempty and finite | `graph-unpack` | G is a graph on n vertices | 1 |
| V(H) ⊆ V(G) | `induced-unpack` | H is an induced subgraph of G | 1, 2 |
| V(H) ⊆ V(G) and E(H) ⊆ E(G) | `subgraph-unpack` | H is a subgraph of G | 1, 2 |
| V(T) = V(G) | `spanning-tree-unpack` | T is a spanning tree of G | 3 |
| V(Ḡ) = V(G) | `complement-unpack` | Ḡ is the complement of G | 1 |
| v₀,…,vₖ is a path of length k in G | `path-pack` | v₀,…,vₖ is a walk of length k in G; the vertices v₀,…,vₖ are pairwise distinct | 1 |
| v₀,…,vₖ is a path of length k in G | `subgraph-path` | H is a subgraph of G; v₀,…,vₖ is a path of length k in H | 2 |
| v₀,…,vₖ is a sequence with {vᵢ₋₁,vᵢ} ∈ E(G) for all i | `walk-unpack` | v₀,…,vₖ is a walk of length k in G | 1 |
| v₀,…,vₖ is a walk of length k in G | `walk-pack` | v₀,…,vₖ is a sequence with {vᵢ₋₁,vᵢ} ∈ E(G) for all i | 1 |
| v₀,…,vₖ is a walk of length k in G | `path-unpack` | v₀,…,vₖ is a path of length k in G | 1 |
| v₁,…,vₙ is a topological ordering of G | `topological-ordering-pack` | v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j | 4 |
| v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j | `topological-ordering-unpack` | v₁,…,vₙ is a topological ordering of G | 4 |
| W is a clique in G | `clique-pack` | every two distinct vertices of W are adjacent in G | 2 |
| w is isolated (adjacent to no vertex) | `isolated-unpack` | deg(w) = 0 | 1 |
| {u,v} ∈ E(G) | `adjacent-unpack` | u and v are adjacent in G | 1 |
| {u,v} ∈ E(T) | `parent-unpack` | u is the parent of v in (T, r) | 4 |
| |E(G − v)| = |E(G)| − deg(v) | `delete-vertex-edges` | G − v = G[V(G) ∖ {v}] | 2 |
| |E(G)| = a·b | `complete-bipartite-edges` | G = K_{a,b} with parts A, B | 1 |
| |E(G)| = n − 1 | `tree-edge-count` | G is a tree | 3 |
| |E(G)| = n − c | `forest-edge-count` | G is a forest with c connected components | 3 |
| |E(G)| = n(n−1)/2 | `complete-edges` | G = Kₙ | 1 |
| |E(G)| = |E(H)| | `iso-same-edges` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | 2 |
| |E(G)| ≥ n − 1 | `connected-min-edges` | G has a spanning tree | 3 |
| |E(T)| = n − 1 | `spanning-tree-edge-count` | V(T) = V(G); T is a tree | 3 |
| |N(v)| = k | `degree-neighborhood` | deg(v) = k | 1 |
| |V(G)| = |V(H)| | `iso-same-vertices` | f : V(G) → V(H) is a bijection | 2 |
| Σ deg(v) = 2n − 2 | `tree-degree-sum` | |E(G)| = n − 1; Σ deg(v) = 2·|E(G)| | 3 |
| Σ deg(v) = 2·|E(G)| | `degree-sum` | G is a graph on n vertices | 1, 2 |
| Σ deg(v) is even | `degree-sum-even` | Σ deg(v) = 2·|E(G)| | 1 |
| Σ_{q=0}^{k} q/2^q = 2 − (k + 2)/2^k | `weighted-geometric-sum` | k ≥ 0 is an integer | 4 |
| Ḡ is connected | `disconnected-complement-connected` | G has at least two connected components; no edge of G joins two different connected components of G; Ḡ is the complement of G | 2 |
| Ḡ ≅ H̄ | `complements-isomorphic` | f is an isomorphism of Ḡ and H̄ | 2 |
