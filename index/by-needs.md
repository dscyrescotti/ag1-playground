# Index by Needs — “I have this fact. What can I do with it?”

Sorted alphabetically by fact, all lectures together.

| I have | Block | and it gives | Lecture |
|---|---|---|---|
| (G, ℓ) is a weighted digraph | `weighted-digraph-unpack` | G is a directed graph; every edge e has a length ℓ(e) ∈ ℝ, and a walk W has length ℓ(W) = Σ_{e∈W} ℓ(e) | 12 |
| (T, r) is a binary tree | `binary-tree-unpack` | (T, r) is a rooted tree; every vertex of T has at most two children, each marked as left or right | 4 |
| (T, r) is a rooted tree | `rooted-tree-unpack` | T is a tree; r ∈ V(T) | 4 |
| (T, r) is a rooted tree | `unique-parent` | v has exactly one parent | 4 |
| (T, r) is a rooted tree | `child-level` | every child of v is at level i + 1 | 4 |
| (T, r) is a rooted tree | `binary-tree-pack` | (T, r) is a binary tree | 4 |
| (T, r) is a rooted tree | `binary-level-size` | level i of T contains at most 2ⁱ vertices | 4 |
| (u,v) ∈ E(G) | `successor-unpack` | u is a predecessor of v and v is a successor of u | 1 |
| (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H | `iso-preserves-connectivity` | H is connected | 2 |
| all edge lengths are nonnegative | `nonnegative-no-negative-cycle` | G contains no negative cycle | 12 |
| all edge lengths are positive | `positive-is-nonnegative` | all edge lengths are nonnegative | 12 |
| C is a shortest cycle in G | `shortest-cycle-induced` | C is an induced subgraph of G | 1 |
| C is a shortest odd cycle in G | `shortest-odd-cycle-induced` | C is an induced subgraph of G | 1 |
| d(s,t) = k | `distance-unpack` | there is an s-t-path of length k; no s-t-path has length < k | 1 |
| d(u, v) = k | `weighted-distance-unpack` | some uv-path has length k, and every uv-path has length ≥ k (d(u, v) = +∞ if there is no uv-path) | 12 |
| d(u, v) ≤ d(u, w) + d(w, v) for all vertices u, v, w | `subpath-of-shortest-path` | the part of P from u to w is a shortest uw-path, and the part from w to v is a shortest wv-path | 12 |
| deg(u) = n − 1 | `universal-vertex` | u is adjacent to every other vertex of G | 1 |
| deg(v) = 1 | `leaf-pack` | v is a leaf of G | 3 |
| deg(v) = k | `degree-neighborhood` | |N(v)| = k | 1 |
| deg(v) = r for every vertex v | `regular-pack` | G is r-regular | 1 |
| deg(v) = r for every vertex v | `regular-degree-sum` | n·r = 2·|E(G)| | 1 |
| deg(w) = 0 | `isolated-unpack` | w is isolated (adjacent to no vertex) | 1 |
| deg_H(f(v)) = deg_G(v) for every v ∈ V(G) | `iso-same-degree-sequence` | G and H have the same degree sequence | 2 |
| e is an edge of a cycle of G | `cycle-edge-removal` | G − e is connected | 3 |
| e ∈ E(G) | `edge-in-spanning-tree` | G has a spanning tree that contains e | 3 |
| e ∈ E(G) ∖ E(T) | `spanning-tree-exchange` | there is an edge e′ ∈ E(T) such that (T + e) − e′ is a spanning tree of G | 3 |
| E(H) contains every edge of G with both endpoints in V(H) | `induced-pack` | H is an induced subgraph of G | 1, 2 |
| every edge of G has one endpoint in A and one in B | `bipartite-pack` | G is bipartite with parts A, B | 1 |
| every two distinct vertices of G are adjacent | `complete-pack` | G = Kₙ | 1 |
| every two distinct vertices of W are adjacent in G | `clique-pack` | W is a clique in G | 2 |
| every two distinct vertices of W are adjacent in G | `clique-induces-complete` | G[W] is a complete graph on |W| vertices | 2 |
| every vertex of G has an incoming arc | `no-source-cycle` | G contains a directed cycle | 4 |
| every vertex of T has at most two children, each marked as left or right | `binary-tree-pack` | (T, r) is a binary tree | 4 |
| every vertex of T has at most two children, each marked as left or right | `binary-level-size` | level i of T contains at most 2ⁱ vertices | 4 |
| f : V(G) → V(H) is a bijection | `isomorphism-pack` | f is an isomorphism of G and H | 2 |
| f : V(G) → V(H) is a bijection | `iso-same-vertices` | |V(G)| = |V(H)| | 2 |
| f : V(G) → V(H) is a bijection | `iso-same-edges` | |E(G)| = |E(H)| | 2 |
| f : V(G) → V(H) is a bijection | `iso-preserves-degree` | deg_H(f(v)) = deg_G(v) for every v ∈ V(G) | 2 |
| f : V(G) → V(H) is a bijection | `iso-same-degree-sequence` | G and H have the same degree sequence | 2 |
| f : V(G) → V(H) is a bijection | `iso-preserves-paths` | (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H | 2 |
| f : V(G) → V(H) is a bijection | `iso-preserves-connectivity` | H is connected | 2 |
| f : V(G) → V(H) is a bijection | `iso-inverse` | f⁻¹ is an isomorphism of H and G | 2 |
| f : V(G) → V(H) is a bijection | `iso-complement` | f is an isomorphism of Ḡ and H̄ | 2 |
| f is an automorphism of G | `automorphism-unpack` | f is an isomorphism of G and G | 2 |
| f is an isomorphism of G and G | `automorphism-pack` | f is an automorphism of G | 2 |
| f is an isomorphism of G and H | `isomorphism-unpack` | f : V(G) → V(H) is a bijection; for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | 2 |
| f is an isomorphism of G and H | `isomorphic-pack` | G ≅ H | 2 |
| f is an isomorphism of G and H | `iso-compose` | g ∘ f is an isomorphism of G and J | 2 |
| f is an isomorphism of Ḡ and H̄ | `complements-isomorphic` | Ḡ ≅ H̄ | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `isomorphism-pack` | f is an isomorphism of G and H | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `iso-same-edges` | |E(G)| = |E(H)| | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `iso-preserves-degree` | deg_H(f(v)) = deg_G(v) for every v ∈ V(G) | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `iso-preserves-paths` | (v₀,…,vₖ) is a path in G ⟺ (f(v₀),…,f(vₖ)) is a path in H | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `iso-inverse` | f⁻¹ is an isomorphism of H and G | 2 |
| for all u, v ∈ V(G): {u,v} ∈ E(G) ⟺ {f(u),f(v)} ∈ E(H) | `iso-complement` | f is an isomorphism of Ḡ and H̄ | 2 |
| for every two non-adjacent vertices u, v of G, the graph G + {u,v} contains a cycle | `maximal-acyclic-tree` | G is a tree | 3 |
| for every two vertices u, v of G there is a u-v-path in G | `connected-pack` | G is connected | 2 |
| for every two vertices u, v of G there is exactly one u-v-path in G | `unique-paths-tree` | G is a tree | 3 |
| for every two vertices u, v there is a directed path from u to v and a directed path from v to u | `strongly-connected-pack` | G is strongly connected | 3 |
| for every two vertices u, v there is a directed path from u to v and a directed path from v to u | `strong-implies-weak` | sym(G) is connected | 3 |
| f⁻¹ is an isomorphism of H and G | `isomorphic-symmetric` | H ≅ G | 2 |
| G = Cₙ | `cycle-graph-unpack` | n ≥ 3 and G has n vertices and n edges; G is 2-regular | 1 |
| G = Cₙ | `cycle-spanning-trees` | G has exactly n spanning trees | 3 |
| G = K_{a,b} with parts A, B | `complete-bipartite-unpack` | V(G) = A ∪ B and A ∩ B = ∅; u, v adjacent ⟺ u, v lie in different parts | 1 |
| G = K_{a,b} with parts A, B | `complete-bipartite-edges` | |E(G)| = a·b | 1 |
| G = K_{a,b} with parts A, B | `complete-bipartite-is-bipartite` | G is bipartite with parts A, B | 1 |
| G = Kₙ | `complete-unpack` | every two distinct vertices of G are adjacent | 1 |
| G = Kₙ | `complete-edges` | |E(G)| = n(n−1)/2 | 1 |
| G = Kₙ | `complete-regular` | G is (n−1)-regular | 1 |
| G = Kₙ | `complete-graphs-isomorphic` | G ≅ H | 2 |
| G = Pₙ | `path-graph-unpack` | G has n vertices and n − 1 edges | 1 |
| G = Pₙ | `path-is-tree` | G is a tree | 3 |
| G contains a cycle of odd length | `odd-cycle-not-bipartite` | G is not bipartite | 1 |
| G contains a directed cycle | `directed-cycle-unpack` | there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) | 4 |
| G contains no cycle (G is acyclic) | `forest-pack` | G is a forest | 3 |
| G contains no cycle (G is acyclic) | `tree-pack` | G is a tree | 3 |
| G contains no cycle (G is acyclic) | `subgraph-acyclic` | H contains no cycle | 3 |
| G contains no cycle (G is acyclic) | `maximal-acyclic-tree` | G is a tree | 3 |
| G contains no directed cycle | `dag-pack` | G is a DAG | 4 |
| G contains no directed cycle | `dag-source-sink` | G has a source; G has a sink | 4 |
| G contains no directed cycle | `dag-has-topological-ordering` | G has a topological ordering | 4 |
| G contains no directed cycle | `hamiltonian-path-unique-ordering` | G has exactly one topological ordering | 4 |
| G contains no negative cycle | `walk-contraction` | there is a uv-path P with ℓ(P) ≤ ℓ(W) | 12 |
| G contains no negative cycle | `shortest-walk-is-path` | a shortest uv-walk exists, and its length is d(u, v) | 12 |
| G contains no negative cycle | `triangle-inequality` | d(u, v) ≤ d(u, w) + d(w, v) for all vertices u, v, w | 12 |
| G has a directed path that goes through all vertices | `hamiltonian-path-unique-ordering` | G has exactly one topological ordering | 4 |
| G has a spanning tree | `spanning-tree-connected` | G is connected | 3 |
| G has a spanning tree | `connected-min-edges` | |E(G)| ≥ n − 1 | 3 |
| G has a topological ordering | `topological-ordering-acyclic` | G contains no directed cycle | 4 |
| G has at least two connected components | `two-components-disconnected` | there are vertices u, v of G with no u-v-path in G | 2 |
| G has at least two connected components | `disconnected-complement-connected` | Ḡ is connected | 2 |
| G has exactly one connected component | `one-component-connected` | G is connected | 2 |
| G has exactly one topological ordering | `unique-ordering-hamiltonian-path` | G has a directed path that goes through all vertices | 4 |
| G is (n−1)-regular | `regular-full-is-complete` | G = Kₙ | 2 |
| G is 0-regular | `zero-regular-shape` | G consists of n isolated vertices | 1 |
| G is 1-regular | `one-regular-shape` | G is a disjoint union of edges; n is even | 1 |
| G is 2-regular | `two-regular-shape` | G is a disjoint union of cycles | 1 |
| G is a DAG | `dag-unpack` | G is a directed graph; G contains no directed cycle | 4 |
| G is a directed graph | `digraph-unpack` | edges are ordered pairs; (u,v) ≠ (v,u); loops (u,u) are allowed | 1 |
| G is a directed graph | `symmetrization-unpack` | sym(G) is the undirected graph on V(G) with {u,v} ∈ E(sym(G)) ⟺ (u,v) ∈ E(G) or (v,u) ∈ E(G) | 3 |
| G is a directed graph | `dag-pack` | G is a DAG | 4 |
| G is a forest | `forest-unpack` | G contains no cycle (G is acyclic) | 3 |
| G is a forest with c connected components | `forest-edge-count` | |E(G)| = n − c | 3 |
| G is a graph on n vertices | `graph-unpack` | V(G) is nonempty and finite; every edge is a 2-element subset of V(G): no loops, no multiple edges | 1 |
| G is a graph on n vertices | `path-length-bound` | k ≤ n − 1 | 1 |
| G is a graph on n vertices | `complete-pack` | G = Kₙ | 1 |
| G is a graph on n vertices | `complement-degree` | deg_Ḡ(v) = n − 1 − deg_G(v) for every v | 1 |
| G is a graph on n vertices | `degree-bounds` | 0 ≤ deg(v) ≤ n − 1 for every vertex v | 1 |
| G is a graph on n vertices | `universal-vertex` | u is adjacent to every other vertex of G | 1 |
| G is a graph on n vertices | `same-degree` | two vertices of G have the same degree | 1 |
| G is a graph on n vertices | `degree-sum` | Σ deg(v) = 2·|E(G)| | 1, 2 |
| G is a graph on n vertices | `path-relation-equivalence` | u ↭ v ⟺ (∃ u-v-path in G) is an equivalence relation on V(G) | 2 |
| G is a graph on n vertices | `identity-automorphism` | the identity map on V(G) is an automorphism of G | 2 |
| G is a graph on n vertices | `regular-full-is-complete` | G = Kₙ | 2 |
| G is a tree | `tree-unpack` | G contains no cycle (G is acyclic); G is connected | 3 |
| G is a tree | `tree-two-leaves` | G has at least two leaves | 3 |
| G is a tree | `leaf-removal-tree` | G − v is a tree | 3 |
| G is a tree | `tree-unique-paths` | for every two vertices u, v of G there is exactly one u-v-path in G | 3 |
| G is a tree | `tree-edges-are-bridges` | G − e is disconnected for every edge e of G | 3 |
| G is a tree | `tree-edge-count` | |E(G)| = n − 1 | 3 |
| G is a tree | `tree-leaves-max-degree` | G has at least Δ leaves | 3 |
| G is a tree | `tree-add-edge-cycle` | for every two non-adjacent vertices u, v of G, the graph G + {u,v} contains a cycle | 3 |
| g is an isomorphism of H and J | `iso-compose` | g ∘ f is an isomorphism of G and J | 2 |
| G is bipartite with parts A, B | `bipartite-unpack` | V(G) = A ∪ B and A ∩ B = ∅; every edge of G has one endpoint in A and one in B | 1 |
| G is bipartite with parts A, B | `bipartite-parity` | even walk ends in its starting part; odd walk ends in the other part | 1 |
| G is connected | `connected-unpack` | for every two vertices u, v of G there is a u-v-path in G | 2 |
| G is connected | `connected-one-component` | G has exactly one connected component | 2 |
| G is connected | `connected-min-degree` | deg(v) ≥ 1 for every vertex v (no isolated vertex) | 2 |
| G is connected | `iso-preserves-connectivity` | H is connected | 2 |
| G is connected | `tree-pack` | G is a tree | 3 |
| G is connected | `cycle-edge-removal` | G − e is connected | 3 |
| G is connected | `bridges-tree` | G is a tree | 3 |
| G is connected | `edge-count-tree` | G is a tree | 3 |
| G is connected | `spanning-tree-exists` | G has a spanning tree | 3 |
| G is connected | `edge-in-spanning-tree` | G has a spanning tree that contains e | 3 |
| G is disconnected | `disconnected-unpack` | there are vertices u, v of G with no u-v-path in G | 2 |
| G is n-regular and has 2n vertices | `regular-half-connected` | G is connected | 2 |
| G is r-regular | `regular-unpack` | deg(v) = r for every vertex v | 1 |
| G is strongly connected | `strongly-connected-unpack` | for every two vertices u, v there is a directed path from u to v and a directed path from v to u | 3 |
| G is weakly connected | `weakly-connected-unpack` | sym(G) is connected | 3 |
| G − e is disconnected for every edge e of G | `bridges-tree` | G is a tree | 3 |
| G − v = G[V(G) ∖ {v}] | `delete-vertex-edges` | |E(G − v)| = |E(G)| − deg(v) | 2 |
| G − v is a tree | `leaf-addition-tree` | G is a tree | 3 |
| G ≅ H | `isomorphic-unpack` | f is an isomorphism of G and H | 2 |
| H = Kₙ | `complete-graphs-isomorphic` | G ≅ H | 2 |
| H is a (minimum) binary heap with n elements | `heap-unpack` | H is a binary tree with a key k(x) in every vertex x; heap shape: all levels of H except the last are completely filled, and the last is filled from the left; heap order: k(v) ≤ k(s) whenever s is a child of v | 4 |
| H is a binary tree with a key k(x) in every vertex x | `heap-pack` | H is a (minimum) binary heap with n elements | 4 |
| H is a connected component of G | `component-unpack` | H is an induced subgraph of G; H is connected; no connected subgraph F ≠ H of G contains H | 2 |
| H is a subgraph of G | `subgraph-unpack` | V(H) ⊆ V(G) and E(H) ⊆ E(G) | 1, 2 |
| H is a subgraph of G | `induced-pack` | H is an induced subgraph of G | 1, 2 |
| H is a subgraph of G | `subgraph-path` | v₀,…,vₖ is a path of length k in G | 2 |
| H is a subgraph of G | `subgraph-acyclic` | H contains no cycle | 3 |
| H is an induced subgraph of G | `induced-unpack` | V(H) ⊆ V(G); E(H) contains every edge of G with both endpoints in V(H) | 1, 2 |
| H is an induced subgraph of G | `induced-is-subgraph` | H is a subgraph of G | 1, 2 |
| H is an induced subgraph of G | `induced-by-vertex-set` | H = G[V(H)], so H is determined by its vertex set | 1, 2 |
| H is an induced subgraph of G | `component-pack` | H is a connected component of G | 2 |
| H is connected | `component-pack` | H is a connected component of G | 2 |
| heap order: k(v) ≤ k(s) whenever s is a child of v | `heap-pack` | H is a (minimum) binary heap with n elements | 4 |
| heap order: k(v) ≤ k(s) whenever s is a child of v | `heap-path-monotone` | on the path from any vertex to the root, the keys do not increase | 4 |
| heap shape: all levels of H except the last are completely filled, and the last is filled from the left | `heap-pack` | H is a (minimum) binary heap with n elements | 4 |
| heap shape: all levels of H except the last are completely filled, and the last is filled from the left | `heap-levels` | H has ⌊log₂ n⌋ + 1 levels | 4 |
| heap shape: all levels of H except the last are completely filled, and the last is filled from the left | `heap-indices` | numbering the vertices 1,…,n level by level from the left: vertex i has children 2i and 2i + 1 and parent ⌊i/2⌋ | 4 |
| k ≥ 0 is an integer | `weighted-geometric-sum` | Σ_{q=0}^{k} q/2^q = 2 − (k + 2)/2^k | 4 |
| level i of T contains at most 2ⁱ vertices | `binary-tree-size` | if T has ℓ levels, then T has at most 2^ℓ − 1 vertices | 4 |
| n ≥ 2 | `universal-excludes-isolated` | deg(v) ≥ 1 for every vertex v (no isolated vertex) | 1 |
| n ≥ 2 | `same-degree` | two vertices of G have the same degree | 1 |
| n ≥ 2 | `vertex-deletion` | G − v = G[V(G) ∖ {v}] | 2 |
| n ≥ 2 | `connected-min-degree` | deg(v) ≥ 1 for every vertex v (no isolated vertex) | 2 |
| n ≥ 2 | `tree-two-leaves` | G has at least two leaves | 3 |
| n ≥ 2 | `leaf-removal-tree` | G − v is a tree | 3 |
| no arc of G ends in s | `source-pack` | s is a source of G; G has a source | 4 |
| no arc of G starts in t | `sink-pack` | t is a sink of G; G has a sink | 4 |
| no connected subgraph F ≠ H of G contains H | `component-pack` | H is a connected component of G | 2 |
| no edge of G joins two different connected components of G | `disconnected-complement-connected` | Ḡ is connected | 2 |
| no s-t-path has length < k | `distance-pack` | d(s,t) = k | 1 |
| numbering the vertices 1,…,n level by level from the left: vertex i has children 2i and 2i + 1 and parent ⌊i/2⌋ | `heap-leaves` | H has exactly ⌈n/2⌉ vertices without children | 4 |
| n·r = 2·|E(G)| | `regular-odd-degree` | n is even | 1 |
| on the path from any vertex to the root, the keys do not increase | `heap-min-at-root` | the root of H holds the minimum key | 4 |
| P is a shortest uv-path and w is a vertex of P | `subpath-of-shortest-path` | the part of P from u to w is a shortest uw-path, and the part from w to v is a shortest wv-path | 12 |
| r is odd | `regular-odd-degree` | n is even | 1 |
| r ∈ V(T) | `rooted-tree-pack` | (T, r) is a rooted tree | 4 |
| s is a source of G | `source-unpack` | no arc of G ends in s | 4 |
| some uv-path has length k, and every uv-path has length ≥ k (d(u, v) = +∞ if there is no uv-path) | `weighted-distance-pack` | d(u, v) = k | 12 |
| sym(G) is connected | `weakly-connected-pack` | G is weakly connected | 3 |
| t is a sink of G | `sink-unpack` | no arc of G starts in t | 4 |
| T is a spanning tree of G | `spanning-tree-unpack` | T is a subgraph of G; V(T) = V(G); T is a tree | 3 |
| T is a spanning tree of G | `spanning-tree-exchange` | there is an edge e′ ∈ E(T) such that (T + e) − e′ is a spanning tree of G | 3 |
| T is a subgraph of G | `spanning-tree-pack` | T is a spanning tree of G | 3 |
| T is a tree | `spanning-tree-pack` | T is a spanning tree of G | 3 |
| T is a tree | `spanning-tree-edge-count` | |E(T)| = n − 1 | 3 |
| T is a tree | `rooted-tree-pack` | (T, r) is a rooted tree | 4 |
| the v-r-path in T has length i | `level-pack` | v is at level i of (T, r) | 4 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `components-partition` | every vertex of G lies in exactly one connected component of G | 2 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `no-edge-between-components` | no edge of G joins two different connected components of G | 2 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `connected-one-component` | G has exactly one connected component | 2 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `one-component-connected` | G is connected | 2 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `disconnected-two-components` | G has at least two connected components | 2 |
| the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | `two-components-disconnected` | there are vertices u, v of G with no u-v-path in G | 2 |
| the vertices v₀,…,vₖ are pairwise distinct | `path-pack` | v₀,…,vₖ is a path of length k in G | 1 |
| there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) | `directed-cycle-pack` | G contains a directed cycle | 4 |
| there are vertices c₁,…,cₖ (k ≥ 1) with (cᵢ,cᵢ₊₁) ∈ E(G) for i < k and (cₖ,c₁) ∈ E(G) | `cycle-no-topological-ordering` | G has no topological ordering | 4 |
| there are vertices u, v of G with no u-v-path in G | `disconnected-pack` | G is disconnected | 2 |
| there are vertices u, v of G with no u-v-path in G | `disconnected-two-components` | G has at least two connected components | 2 |
| there is a walk from s to t in G | `walk-to-path` | there is an s-t-path in G | 1 |
| there is an s-t-path of length k | `distance-pack` | d(s,t) = k | 1 |
| u and v are adjacent in G | `adjacent-unpack` | {u,v} ∈ E(G) | 1 |
| u and v are adjacent in G | `neighborhood-pack` | v ∈ N(u) | 1 |
| u is adjacent to every other vertex of G | `universal-excludes-isolated` | deg(v) ≥ 1 for every vertex v (no isolated vertex) | 1 |
| u is an ancestor of v in (T, r) | `ancestor-unpack` | u lies on the v-r-path in T | 4 |
| u is an ancestor of v in (T, r) | `parent-pack` | u is the parent of v in (T, r) | 4 |
| u is the parent of v in (T, r) | `parent-unpack` | u is an ancestor of v in (T, r); {u,v} ∈ E(T) | 4 |
| u lies on the v-r-path in T | `ancestor-pack` | u is an ancestor of v in (T, r) | 4 |
| u ↭ v ⟺ (∃ u-v-path in G) is an equivalence relation on V(G) | `component-classes` | the vertex sets of the connected components of G are exactly the equivalence classes of ↭ | 2 |
| u ≠ v, and G has a directed path from u to v and a directed path from v to u | `mutual-paths-cycle` | G contains a directed cycle | 4 |
| V is a fixed vertex set with |V| = n | `count-graphs` | there are exactly 2^(n(n−1)/2) graphs on V | 1, 3 |
| v is a leaf of G | `leaf-unpack` | deg(v) = 1 | 3 |
| v is a leaf of G | `leaf-removal-tree` | G − v is a tree | 3 |
| v is a leaf of G | `leaf-addition-tree` | G is a tree | 3 |
| v is at level i of (T, r) | `level-unpack` | the v-r-path in T has length i | 4 |
| v is at level i of (T, r) | `child-level` | every child of v is at level i + 1 | 4 |
| v ∈ N(u) | `neighborhood-unpack` | u and v are adjacent in G | 1 |
| v ∈ V(G) | `vertex-deletion` | G − v = G[V(G) ∖ {v}] | 2 |
| v ≠ r is a vertex of T | `unique-parent` | v has exactly one parent | 4 |
| V(G) = A ∪ B and A ∩ B = ∅ | `bipartite-pack` | G is bipartite with parts A, B | 1 |
| V(H) ⊆ V(G) and E(H) ⊆ E(G) | `subgraph-pack` | H is a subgraph of G | 1, 2 |
| V(T) = V(G) | `spanning-tree-pack` | T is a spanning tree of G | 3 |
| V(T) = V(G) | `spanning-tree-edge-count` | |E(T)| = n − 1 | 3 |
| V′ ⊆ V(G) and V′ ≠ ∅ | `induced-notation` | G[V′] has vertex set V′ and edge set E(G) ∩ (V′ choose 2); G[V′] is an induced subgraph of G | 2 |
| v₀,…,vₖ is a path of length k in G | `path-unpack` | v₀,…,vₖ is a walk of length k in G; the vertices v₀,…,vₖ are pairwise distinct | 1 |
| v₀,…,vₖ is a path of length k in G | `path-length-bound` | k ≤ n − 1 | 1 |
| v₀,…,vₖ is a path of length k in H | `subgraph-path` | v₀,…,vₖ is a path of length k in G | 2 |
| v₀,…,vₖ is a sequence with {vᵢ₋₁,vᵢ} ∈ E(G) for all i | `walk-pack` | v₀,…,vₖ is a walk of length k in G | 1 |
| v₀,…,vₖ is a walk of length k in G | `walk-unpack` | v₀,…,vₖ is a sequence with {vᵢ₋₁,vᵢ} ∈ E(G) for all i | 1 |
| v₀,…,vₖ is a walk of length k in G | `path-pack` | v₀,…,vₖ is a path of length k in G | 1 |
| v₁,…,vₙ is a topological ordering of G | `topological-ordering-unpack` | v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j | 4 |
| v₁,…,vₙ lists every vertex of G exactly once, and (vᵢ,vⱼ) ∈ E(G) implies i < j | `topological-ordering-pack` | v₁,…,vₙ is a topological ordering of G; G has a topological ordering | 4 |
| W is a clique in G | `clique-unpack` | every two distinct vertices of W are adjacent in G | 2 |
| W is a uv-walk in G | `walk-contraction` | there is a uv-path P with ℓ(P) ≤ ℓ(W) | 12 |
| w is isolated (adjacent to no vertex) | `isolated-pack` | deg(w) = 0 | 1 |
| x ≠ y are vertices of Kₙ | `count-paths-complete` | the number of x-y-paths of length k is (n−2)(n−3)···(n−k) | 1 |
| {u,v} ∈ E(G) | `adjacent-pack` | u and v are adjacent in G | 1 |
| {u,v} ∈ E(T) | `parent-pack` | u is the parent of v in (T, r) | 4 |
| |E(G)| = n − 1 | `edge-count-tree` | G is a tree | 3 |
| |E(G)| = n − 1 | `tree-degree-sum` | Σ deg(v) = 2n − 2 | 3 |
| |N(v)| = k | `degree-pack` | deg(v) = k | 1 |
| Δ ≥ 2 is the maximum degree of G | `tree-leaves-max-degree` | G has at least Δ leaves | 3 |
| Σ deg(v) = 2·|E(G)| | `degree-sum-even` | Σ deg(v) is even | 1 |
| Σ deg(v) = 2·|E(G)| | `regular-degree-sum` | n·r = 2·|E(G)| | 1 |
| Σ deg(v) = 2·|E(G)| | `tree-degree-sum` | Σ deg(v) = 2n − 2 | 3 |
| Σ deg(v) is even | `handshaking` | the number of odd-degree vertices of G is even | 1 |
| Ḡ and H̄ are the complements of G and H | `iso-complement` | f is an isomorphism of Ḡ and H̄ | 2 |
| Ḡ is the complement of G | `complement-unpack` | V(Ḡ) = V(G); for u ≠ v: {u,v} ∈ E(Ḡ) ⟺ {u,v} ∉ E(G) | 1 |
| Ḡ is the complement of G | `complement-degree` | deg_Ḡ(v) = n − 1 − deg_G(v) for every v | 1 |
| Ḡ is the complement of G | `disconnected-complement-connected` | Ḡ is connected | 2 |
