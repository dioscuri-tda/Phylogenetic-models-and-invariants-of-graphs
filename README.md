# Phylogenetic models and invariants of graphs
 This repository provides the code for the publication "Combinatorial topological models for phylogenetics and the mergegram invariant", where the theoretical and algorithmical groundwork is made for these implementations. 

The main parts are the three models Treegram, Cliquegram, Facegram (in ascending generality), which provide different methods. The three models have different representations, once as lattices, once via distance matrices, once as directed acyclic graphs, all with their respective properties and restrictions. 

Given a finite set of points X.
1) Lattice view (abbreviated, compare to the publication for a throurough definition):
    * The treegram is a partition of the power set of X, i.e. a selection of a finite number of sets $C_i$ for $i=1,..., n$ containing maximal sets (no subset of an element in $C_i$ is contained in $C_i$) such that for every set in $C_i$ there is a superset of it (or itself) in $C_{i+1}$ and that no two sets in $C_i$ have a non-empty intersection. $C_0 = \emptyset$ and $C_n =X$.
    * The cliquegram is also a selection of a finite number of sets $C_i$ for $i=1,..., n$ containing maximal sets (no subset of an element in $C_i$ is contained in $C_i$) such that for every set in $C_i$ there is a superset of it (or itself) in $C_{i+1}$, but we now have the additional condition that if all sets $\tau \subset X$ we have that for all  $\sigma \subset \tau$ with $|\sigma|+1=|\tau|$ we have that there exists $\sigma' \in C_i$ with $\sigma \subset \sigma '$ it follows that there is a $\tau' in C_i$ with $\tau \subseteq \tau '$.
    * The cliquegram is also a selection of a finite number of sets $C_i$ for $i=1,..., n$ containing maximal sets (no subset of an element in $C_i$ is contained in $C_i$) such that for every set in $C_i$ there is a superset of it (or itself) in $C_{i+1}$. 

2) distance matrix:
    * The treegram can be represented by a symmetric ultramatric.
    * The cliquegram can be represented by a phylogenetic network.
    * The facegram can be represented by a filtration.

To illustrate the following table, let us fix some notation, needed for this repository. Given a finite set $X$, define a filtration $F: \mathbf{pow}(X) \rightarrow mathbb{R}$. It has the properties that $F(\sigma) \leq F(\tau)$ for all $\sigma \subseteq \tau$. 