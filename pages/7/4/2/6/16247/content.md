
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[Dynkin diagram]] is a labeled graph that possesses a one-to-one correspondence with a finite indecomposable reduced [[root system]], thus with a simple complex finite dimensional [[Lie algebra]] or [[Cartan matrix]]. 

The construction of a [[Dynkin diagram]] from the [[Cartan Matrix]], $A = (a_{i,j})_{i,j=1}^n$ is obtained from the following procedure:

1. Number of vertices = Number of simple roots = size of $A$ = n

2. If $a_{i,j} = a_{i,j} = -1$ then $i,j$ are connected by a nonlabeled edge.

3. If $a_{i,j} = -1$ and  $a_{j,i} = -l$ then $i,j$ are connected by $l$ arrows labeled by <. 

## Properties

### Classification of simple Lie groups

[[classification of simple Lie groups]]:

<center>
<img src="http://jakobschwichtenberg.com/wp-content/uploads/2016/10/dynkinclassification.jpg">
</center>

> graphics grabbed from [Schwichtenberg](http://jakobschwichtenberg.com/classification-of-simple-lie-groups/)

### ADE-Classification

Those Dynkin diagrams in the [[ADE classification]] are the following

<center>
<img src="https://ncatlab.org/nlab/files/ADEDynkin.jpg" width="490"/>
</center>

[[!include ADE -- table]]


### Dynkin Index

Let $\mathcal{g}$ be a finite simple complex [[Lie algebra]] with a [[Killing form]] $k$ on $\mathcal{g}$ given by the trace in the adjoint representation,
$k(x,y) = Tr R_{ad}(x)R_{ad}(y)$ for $x,y \in \mathcal{g}$. 

For any irreducible finite representation $R_{\lambda}$ of $\mathcal{g}$, 
$TrR_\lambda(x)R_\lambda(y) = I_\lambda k(x,y)$
Where $I_\lambda$ is the _Dynkin Index_ of $R_\lambda$.

The Dynkin index can also be defined in terms of the eigenvalue $C_\lambda$ of the quadratic [[Casimir operator]]:
$ I_\lambda = \frac{dim(R_\lambda)}{dim(\mathcal{g}}C_\lambda $.

\begin{remark}\label{DynkinIndexInInstantonNumber}
In [[mathematical physics]],in the context of [[embeddings]] of [[gauge fields]], the Dynkin index is used in the calculation of topological charges ([[instanton number]]). 
To demonstrate this, let $A_\mu$ be a gauge potential on the Euclidean space $E^4$ given by 
$$
A_\mu(x) = A_{\mu}^{\alpha}X_\alpha 
$$
where $X_\alpha$ are the generators of a compact [[gauge group]] $G$. If the gauge field $A_\mu$ is an [[embedding]] of $\tilde{G}$ in $G$ then the Dynkin index of the embedding is denoted as $j_{\tilde{G} \over G}$ . The topological charge is 
$$
q = j_{\tilde{G} \over G} q_1
$$
where $q_1$ is the charge of $A_\mu$ treated as a $\tilde{G}$ [[gauge field]]. 
The proof was carried out for $\tilde{G} \simeq SU(2)$ by Bitar and Sorba see [Myers, de Roo & Sorba 79, Sec. 2](#MyersdeRooSorba79), which can be extended to arbitrary simple [[compact groups]]. 
\end{remark}



## Related concepts

* [[Dynkin quiver]]

* [[ADE classification]]

## References

### General

See also:

* Wikipedia, _[Dynkin diagram](http://en.wikipedia.org/wiki/Dynkin_diagram)_

### Dynkin index

* Bianchi M. et al. (2004) Dynkin Index. In: Duplij S., Siegel W., Bagger J. (eds) Concise Encyclopedia of Supersymmetry. Springer, Dordrecht. _[publisher](https://doi.org/10.1007/1-4020-4522-0_169)_


* {#MyersdeRooSorba79} C. Meyers, M. de Roo, P. Sorba,  _Group-theoretical aspects of instantons_. Nuov Cim A 52, 519–530 (1979) ([doi:10.1007/BF02770858](https://doi.org/10.1007/BF02770858))


[[!redirects Dynkin diagrams]]

[[!redirects simply laced Dynkin diagram]]
[[!redirects simply laced Dynkin diagrams]]