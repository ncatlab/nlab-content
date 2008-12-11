#Idea#



A directed $n$-graph is a higher dimensional generalization of a [[directed graph]] with $r$-dimensional _edges_ spanning $(r-1)$-dimensional _vertices_.

#Definition#

A **directed $n$-graph** $G = \prod_{r=0}^n G_r$ is 

* a collection $G_r$ of $r$-dimensional _edges_;

* together with, for each $r \geq 1 \in \mathbb{N}$, two maps $s,t : G_r \to G_{r-1}$, called
the _source_ and _target_ maps, where $G_{-1}$ is the empty set.

##Remarks##

* A directed 1-graph is a [[directed graph]].


* A directed $n$-graph is like an [[n-category]] with units and composition forgotten. Indeed, an [[n-category]] is a directed $n$-graph with extra structure.

+--{.query}



_[[Urs Schreiber|Urs]] says_: I am still searching the literature: somewhere _$n$-graph_ has been defined before. Notice that if the _globularity condition_ on source and target maps are imposed, then an $\infty$-graph is a **[[globular set]]**. Indeed, $\omega$-[[omega-category|categories]] are [[globular set]]s with extra structure.

_[[Eric Forgy|Eric]] says: Here are some references that might be relevant:: [Fundamental groupoids of k-graphs](http://www.emis.de/journals/NYJM/j/2004/10-12.pdf), [$C^*$-algebras associated to higher-rank graphs](http://www.newcastle.edu.au/service/library/adt/uploads/approved/adt-NNCU20060327.122628/public/02whole.pdf). 

=--



