# Phylogenetic models and invariants of graphs
 This repository provides the code for the publication "Combinatorial topological models for phylogenetics and the mergegram invariant", where the theoretical and algorithmical groundwork is made for these implementations. 

The main parts are the three models Treegram, Cliquegram, Facegram (in ascending generality), which provide different methods. The three models have different representations, once as lattices, once via distance matrices and once as directed acyclic graphs, all with their respective properties and restrictions. 

To illustrate the following table, let us fix some notation, needed for this repository. Given a finite set $X$, define a filtration $F: \mathbf{pow}(X) \rightarrow mathbb{R}