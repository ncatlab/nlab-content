
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

[[supergravity Lie 6-algebra]] $\to$ [[supergravity Lie 3-algebra]] $\to$ **super-Poincar&#233; Lie algebra**

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[super Lie algebra]] extension of a [[Poincare Lie algebra]]. 

The corresponding [[super Lie group]] is the [[super Euclidean group]] (except for the signature of the metric).


## Cohomology

The super Poincareacute; Lie algebra has, on top of the [[Lie algebra cohomology|Lie algebra cocycles]] that it inherits from $\mathfrak{so}(n)$, a discrete number of special cocycles bilinear in the spinors, on the super translation algebra, that exist only in very special dimensions.

For the statement of the following theorem, we use the relation between [[division algebra and supersymmetry]], as described there.

**Theorem**

* In dimensional $d =  3,4,6, 10$, $\mathfrak{siso}(d-1,1)$ has a nontrivial 3-cocycle given by

  $$
    (\psi, \phi, A) \mapsto g(\psi \cdot \phi, A)
  $$

  for spinors $\psi, \phi \in \mathcal{S}$ and vectors $A \in \mathcal{T}$, and 0 otherwise.

* In dimensional $d =  4,5,7, 11$, $\mathfrak{siso}(d-1,1)$ has a nontrivial 4-cocycle given by

  $$
    (\Psi, \Phi, \mathcal{A}, \mathcal{B}) \mapsto 
    \langle \Psi , (\mathcal{A}\mathcal{B}- \mathcal{B} \mathcal{A})\Phi \rangle
  $$

  for spinors $\Psi, \Phi \in \mathcal{S}$ and vectors $\mathcal{A}, \mathcal{B} \in \mathcal{V}$, with the commutator taken in the Clifford algebra.

The 4-cocycle in $d = 11$ is the one that induces the [[supergravity Lie 3-algebra]].

## References

A comprehensive account and classification of super Poincar&#233; Lie algebras is in

* D. V. Alekseevsky, V. Cort&#233;s, C. Devchand, A. Van Proeyen, _Polyvector Super-Poincar&#233; Algebras_ ([arXiv](http://arxiv.org/abs/hep-th/0311107))

The exceptional fermionic cocycles of the super Poincar&#233; Lie algebra are discussed in 

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_ ([pdf](http://math.ucr.edu/home/baez/susy2_1.pdf))

For more see [[division algebra and supersymmetry]].

[[!redirects super Poincaré Lie algebra]]