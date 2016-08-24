
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A **finite topological space** is a [[topological space]] whose underlying [[set]] is a [[finite set]].

=--


## Properties

+-- {: .num_prop}
###### Proposition

Every [[finite topological space]] is an [[Alexandroff space]].

I.e. finite topological spaces are [[equivalence of categories|equivalent]] to finite [[preordered sets]], by the [[specialisation order]].

=--


+-- {: .num_theorem}
###### Theorem

Finite topological spaces have the same _[[weak homotopy equivalence|weak]]_ [[homotopy type]]s as finite [[simplicial complexes]] / finite [[CW-complexes]].

=--

This is due to ([McCord 67](#McCord67)).

+-- {: .proof}
###### Proof (sketch) 
If $\mathbf{2}$ is [[Sierpinski space]] (two points $0$, $1$ and three opens $\emptyset$, $\{1\}$, and $\{0, 1\}$), then the continuous map $I = [0, 1] \to \mathbf{2}$ taking $0$ to $0$ and $t \gt 0$ to $1$ is a weak homotopy equivalence[^fine]. 

For any finite topological space $X$ with specialization order $\mathcal{O}(X)$, the topological [[interval]] map $I \to \mathbf{2}$ induces a weak homotopy equivalence $B\mathcal{O}(X) \to X$: 

$$B\mathcal{O}(X) = \int^{[n] \in \Delta} Cat([n], \mathcal{O}(X)) \cdot Int([n], I) \to \int^{[n] \in \Delta} Cat([n], \mathcal{O}(X)) \cdot Int([n], \mathbf{2}) \cong X$$ 

(where we implicitly identify $\Delta^{op}$ with the category $Int$ of finite intervals with distinct top and bottom). The isomorphism on the right says that any finite topological space can be constructed by gluing together copies of Sierpinski space, in exactly the same way that any preorder can be constructed by gluing together copies of the preorder $\{0 \leq 1\}$. 

On the other hand, any finite simplicial complex $X$ is homotopy equivalent to its [[barycentric subdivision]], which is the [[geometric realization]] of the [[poset]] of simplices ordered by inclusion. Thus finite posets model the weak homotopy types of finite simplicial complexes. 

=--

## Examples

* [[pseudocircle]]

## Related concepts

* [[finite set]], [[finite number]]

* [[finite CW-complex]]

* [[finite spectrum]]

## References

A survey is in 

* [[Jonathan Barmak]], _Topolog&#237;a Algebraica de Espacios Topol&#243;gicos Finitos y Aplicaciones_ PhD thesis 2009 ([pdf](http://www.math.kth.se/~jbarmak/tesisfinal2.pdf))

published as

* [[Jonathan Barmak]], _Algebraic Topology of Finite Topological Spaces and Applications_, Lecture Notes in Mathematics,2032. Springer, Heidelberg (2011).

The original results by McCord are in

* {#McCord66} [[Michael C. McCord]], _Singular homology groups and homotopy groups of finite topological spaces_ , Duke Math. J. 33 (1966), 465-474. ([EUCLID](http://projecteuclid.org/euclid.dmj/1077376525)) 

* {#McCord67} [[Michael C. McCord]], _Homotopy type comparison of a space with complexes associated with its open covers_ . Proc. Amer. Math. Soc. 18 (1967), 705-708, [copy](http://www.maths.ed.ac.uk/~aar/papers/mccord2.pdf)



[^fine]: Any topological meet-semilattice $L$ with a bottom element $\bot$, for which there exists a continuous path $\alpha \colon I \to L$ connecting $\bot$ to the top element $\top$, is in fact contractible. The contracting homotopy is given by the composite $I \times L \stackrel{\alpha \times 1}{\to} L \times L \stackrel{\wedge}{\to} L$. 
 
Generalization to [[ringed space|ringed]] finite spaces is discussed in

* [[Fernando Sancho de Salas]], _Ringed Finite Spaces_ ([arXiv:1409.4574](https://arxiv.org/abs/1409.4574))

* [[Fernando Sancho de Salas]], _Finite Spaces and Schemes_ ([arXiv:1602.02393](http://arxiv.org/abs/1602.02393))

and aspects of their [[homotopy theory]] is discussed in

* [[Fernando Sancho de Salas]], _Homotopy of ringed finite spaces_ ([arXiv:1511.06284](http://arxiv.org/abs/1511.06284))


[[!redirects finite topological space]]
[[!redirects finite topological spaces]]
