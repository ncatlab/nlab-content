
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of a _dual basis_ is a way of characterizing [[projective modules]], alternative to their characterization as [[direct sum|direct summands]] of [[free modules]]. The terminology derives from a similarity with a situation involving [[dual vector spaces]], see [below](#RelationToDualVectorSpaces).


## Details

Let $R$ be a [[ring]] or, more generally, an [[associative algebra]] over a unital [[commutative ring]] $k$. 

Assuming the [[axiom of choice]], one of the standard characterizations of the [[projective modules]] $N$ (say left) over $R$ is that there is an [[epimorphism]] $F\to N$ from a [[free module]] over $R$  which is [[split epimorphism|split]] ("$N$ is a [[direct summand]] of a [[free module]]", [this prop.](projective%20module#ProjectiveIsPreciselyDirectSummandOfFreeModule)).

Equivalently, an $R$-module $M$ is projective iff it has a __dual basis__ $\{(x_i,x_i^*)\in M\times Hom_k(M,R)\}_{i\in I}$ in the following sense. There is a free $R$-module $F = \oplus_{i\in I} R$, an epimorphism of $R$-modules $F\to M$, $F=\oplus_i R \ni \sum_i r_i\mapsto \sum_i r_i x_i$ which is split, i.e. has a right inverse, where this inverse, by the universal property of the direct sum, must be of the form $x\mapsto \sum_i x_i^*(x)\in \oplus_i R$ where $x_i^*\in Hom_k(M,R)$. The right inverse condition translates to  $\forall x \in M : x=\sum_i x_i^*(x)x_i$. In particular for every $x\in M$ $x_i^*(x)\neq 0$ for only finitely many $i\in I$.

## Relation to dual vector spaces
 {#RelationToDualVectorSpaces}

This terminology is related to but a bit different than in the case of $k$-vector spaces (cf. at [[dual vector space]]). 
If $V$ has a vector space
basis $(x_j)_{j\in I}$ is a [[linear basis]] of $V$ then $x_i^*$ _defined by_ $x_i^*(x_j) = \delta_i^j$ is not necessarily a basis of $V^* = Hom_k(V,k)$; it is
if $V$ is [[finite dimensional vector space|finite dimensional]].  In the case of projective module $M$, 
$x_i$ do not form a basis in a free sense, 
but only a set of generators and with the property that there exist another set $x_i^*$ in $M^*$ 
such that they together form a "dual basis". (Still, one sometimes says
that $x_i^*$ form a basis dual to $x_i$.)


category: algebra

[[!redirects dual basis]]
[[!redirects dual basises]]
[[!redirects dual bases]]
