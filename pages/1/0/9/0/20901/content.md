[[!redirects Pre-net]]
## Idea

A pre-net is a [[Petri net]] equipped with an ordering on the input and output of each event. These give appropriate data from which to freely generate a [[strict monoidal category]] or a [[symmetric monoidal categories|symmetric strict monoidal category]], whereas a [[Petri net]] is appropriate data from which to freely generate a [[commutative monoidal category]]. Pre-nets are the same as the [[tensor schemes]] defined by [Joyal and Street](#schemes).

## Definition 

A pre-net is a pair of functions
\begin{centre}
\begin{tikzcd}
E \ar[r, shift left=.5ex,"s"] \ar[r,shift right=.5ex,"t",swap] & P^*
\end{tikzcd}
\end{centre}
where $E$ is the set of _events_, $P$ is the set of _places_, and $P^*$ is the [[free monoid]] on the set $P$.

A morphism of of pre-nets $(f \colon E \to E', g \colon P \to P')$ is a pair of functions between the sets of events and places making the following diagrams commute

\begin{centre}
\begin{tikzcd}
E \ar[r, "s"] \ar[d,"f"] & P^* \ar[d,"g^*"] \\
E' \ar[r,"s"] & P'^* 
\end{tikzcd}
\end{centre}

\begin{centre}
\begin{tikzcd}
E \ar[r, "t"] \ar[d,"f"] & P^* \ar[d,"g^*"] \\
E' \ar[r,"t"] & P'^* 
\end{tikzcd}
\end{centre}

This defines a category $PreNet$ of pre-nets and pre-net homomorphisms.

## References

Pre-nets were introduced in

*  [[Roberto Bruni]], [[José Meseguer]], [[Ugo Montanari]], and [[Vladimiro Sassone]]. _Functorial models for Petri nets_ Information and Computation 170, no. 2 (2001): 207-236. [pdf](https://eprints.soton.ac.uk/264742/1/prenetsIandCOff.pdf)

Tensor schemes were introduced in

* {#schemes} [[André Joyal]], and [[Ross Street]]. _The geometry of tensor calculus I_ Advances in mathematics 88, no. 1 (1991): 55-112. [pdf](https://core.ac.uk/download/pdf/82659437.pdf)

[[!redirects Pre-net]] 
[[!redirects pre-nets]] 
[[!redirects tensor scheme]] 
[[!redirects tensor schemes]] 
