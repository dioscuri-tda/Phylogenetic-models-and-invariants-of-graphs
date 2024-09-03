# Phylogenetic models and invariants of graphs
 This repository looks at the "grammodels" type of representations for phylogenetic trees and network as well as for general metric spaces.

 The starting point is the publication "Combinatorial topological models for phylogenetics and the mergegram invariant", where the theoretical and algorithmical groundwork is made for these implementations. The associated repository with the codebase for that publication can be found [here](https://github.com/janfsenge/Combinatorial-Models-for-Phylogenetics).

The main parts are the three models Treegram, Cliquegram, Facegram (in ascending generality), which provide different methods. The three models have different representations, once as lattices, once via distance matrices, once as directed acyclic graphs, all with their respective properties and restrictions. 

Given a finite set of points X (equipped with a metric).
1) Lattice view (abbreviated, compare to the publication for a thorough definition):
    * The treegram is a partition of the power set of X, i.e. a selection of a finite number of sets $C_i$ for $i=1,..., n$ containing maximal sets (no subset of an element in $C_i$ is contained in $C_i$) such that for every set in $C_i$ there is a superset of it (or itself) in $C_{i+1}$ and that no two sets in $C_i$ have a non-empty intersection. $C_0 = \emptyset$ and $C_n =X$.
    * The cliquegram is also a selection of a finite number of sets $C_i$ for $i=1,..., n$ containing maximal sets (no subset of an element in $C_i$ is contained in $C_i$) such that for every set in $C_i$ there is a superset of it (or itself) in $C_{i+1}$, but we now have the additional condition that if all sets $\tau \subset X$ we have that for all  $\sigma \subset \tau$ with $|\sigma|+1=|\tau|$ there exists $\sigma' \in C_i$ with $\sigma \subset \sigma '$ it follows that there is a $\tau' in C_i$ with $\tau \subseteq \tau '$; in other words the cliquegram is the collection of maximal cliques of an auxiliary graph $G_t=(X,E_t)$ for increasing values of $t$ where $E_t = \{ (u,v) | d(u,v) <= t\}$ for a given distance function on the points X.
    * The facegram is also a collection as above without the extra condition of cliquegrams. In that sense, the $C_t$ are formed by maximal faces of a filtered simplicial complexes with filtration $F$ such that $\sigma \in C_t$ if $F(\sigma) \leq t$ and all proper coface of $\sigma$ have filtration value greater than $t$.
2) "distance matrix" / functional representation:
    * The treegram can be represented by a symmetric ultramatric.
    * The cliquegram can be represented by a phylogenetic network.
    * The facegram can be represented by a filtration.
