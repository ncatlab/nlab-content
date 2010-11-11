[[!redirects spherical object]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
 
##Idea

Spherical objects in a general [[pointed category|pointed]]  [[model category]] play the role of the spheres in $Top$.

##Spherical objects
Let $\mathcal{C}$ be a [[pointed category|pointed]] [[model category]].
+--
{: .un_defn}
######Definition######
A **spherical object** for $\mathcal{C}$ is a [[model category|cofibrant]] homotopy [[cogroup]] in $\mathcal{C}$.
=--

###Examples

1. The spheres form the obvious examples of spherical objects in the category $Top$, but the rational spheres give other examples.

1. In the category of path connected pointed spaces with action of a discrete group, $Gr.Top^*_0$ and space of form $S^n_G= \bigvee_G S^n$ is a spherical object.(see Baues, 1991, ref. below, p.273).

1. Any rational sphere is a sphere object (in a suitable category for [[rational homotopy theory]]).

1. Let $T$ be a contractible locally finite 1-dimensional simplicial complex, with $T^0$ its 0-skeleton. Let $\epsilon : E'T^0$ be a finite-to-one function. By $S^n_\epsilon$ we mean the space obtained by attaching an $n$-sphere to the vertices of $T$ with at vertex $v$, the spheres attached to $v$ being indexed by $\epsilon^{-1}(v)$. This space $S^n_\epsilon$ is a spherical object in the proper category, $Proper_\infinity^T$, of $T$-based spaces. (In this context $T$ is acting as the analogue of the base point.  It gives a base tree within the spaces.  This is explored a bit more in [[proper homotopy theory]].)

For instance, take $T = \mathbb{R}_{\geq 0}$, made up of an infinite number of closed unit intervals (end-to-end), then $S^n_\epsilon$ will be the infinite string of spheres considered in the entry on the [[Brown-Grossmann homotopy groups]] if we take $\epsilon$ to be the identity function on $T^0$. 


+--
{: .un_defn}
######Definition######
By a  **family of spherical objects** for $\mathcal{C}$ is meant a collection of spherical objects in $\mathcal{C}$ closed under suspension.
=--


##The theory, $\Pi_\mathcal{A}$

Let $\mathcal{A}$ be such a family of spherical objects. Let $\Pi_\mathcal{A}$ denote the full subcategory of $Ho(\mathcal{C})$, whose objects are the finite coproducts of objects from $\mathcal{A}$.

###Example

For $\mathcal{A} = \{S^n\}^\infty_{n=1}$ in $Top$, $\Pi_\mathcal{A} = \Pi$, the [[algebraic theory|theory]] of [[Pi-algebras]].

Of course, $\Pi_\mathcal{A}$ is a _finite product theory_ in the sense of [[algebraic theories]], and the corresponding models/algebras/modules are called:

##$\Pi_\mathcal{A}$-algebras
We thus have that these are the product preserving functors $\Lambda : \Pi_\mathcal{A}^{op}\to Set_*$.  Morphisms of $\Pi_\mathcal{A}$-algebras are simply the natural transformations.  This gives a category $\Pi_\mathcal{A}-Alg$.

###Properties

*  Such a $\Pi_\mathcal{A}$-algebra, $\Lambda$, is determined by its values $\Lambda(A)\in Set_*$ for $A$ in $\mathcal{A}$, together with, for every $\xi : A \to \bigsqcup_{i\in I}A_i$ in $\Pi_\mathcal{A}$, a map

$$\xi^* : \prod \Lambda(A_i)\to \Lambda(A).$$

* The object $A$ being a (homotopy) cogroup, $\Lambda(A)$ is a group (but beware the $\xi^*$ need not be group homomorphisms).

###Example
If $X$ is in $\mathcal{C}$, define $\pi_\mathcal{A}(X):= [-,X]_{Ho(\mathcal{C})} : \Pi_{\mathcal{A}}^{op}\to Set_*$.  This is the **homotopy $\Pi_{\mathcal{A}}$-algebra** of $X$.  As with $\Pi$-[[Pi-algebra|algebras]], there is a _realisablity problem_, i.e., given $\Lambda$, find a $X$ and an isomorphism, $\pi_\mathcal{A}(X)\cong \Lambda$.  The realisability problem is discussed in Baues-Blanc (2010) (see below).

##References

Spherical objects are considered in 

*  [[Hans-Joachim Baues]] and [[David Blanc]], Comparing cohomology obstructions, (2010), [Arxiv](http://arxiv.org/PS_cache/arxiv/pdf/1008/1008.1712v1.pdf) (to appear JPAA).

Examples are given in earlier work by Baues and by Blanc. 

The group action case is in 

*  [[Hans-Joachim Baues]],  _Combinatorial Homotopy and 4-Dimensional Complexes_, de Gruyter Expositions in Mathematics 2, Walter de Gruyter, (1991).

The example from [[proper homotopy theory]] is discussed in

* H.-J. Baues and  Antonio Quintero, _Infinite Homotopy Theory_,  K-monographs in mathematics, Volume 6, Kluwer, 2001.

[[!redirects spherical objects]]
[[!redirects spherical object and Pi(A)-algebra]]
[[!redirects spherical objects and Pi(A)-algebra]]
[[!redirects spherical objects and Pi(A)-algebras]]