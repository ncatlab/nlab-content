
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


# Contents
* automatic table of contents goes here
{:toc}

## Definition

A [[dg-algebra]] $A$ is a **formal dg-algebra** if in the [[homotopy category]] of the [[model structure on dg-algebras]] it is [[isomorphism|isomorphic]] 

$$
  A \stackrel{\simeq}{\to} H^\bullet(A)
$$

to its [[chain homology and cohomology|chain (co)homology]] (regarded as a dg-algebra with trivial differential). Since all dg-algebras are fibrant in the standard model, this is equivalent to the existence of a [[span]]

$$
  A \stackrel{\simeq_w}{\leftarrow} Q A \stackrel{\simeq}{\to}
  H^\bullet(A)
$$

of [[quasi-isomorphism]]s of dg-algebras.


## Applications

### In rational homotopy theory

In [[rational homotopy theory]] [[rational topological space]]s are encoded in their dg-algebras of Sullivan forms. A simply connected topological space $X$ whose dg-algebra of Sullivan forms $\Omega^\bullet(X)$ is formal is called a **formal topological space**.  (One can also say a __formal rational space__, to distinguish from the unrelated formal spaces in [[formal topology]].)  Such a space represents a **formal homotopy type**.

Examples are

* compact [[Kähler manifold]]s (e.g. smooth projective varieties);

* [[Lie group]]s;

* [[classifying space]]s of Lie groups;

* some [[homogeneous space]]s $G/H$

* the unstable [[Thom space]]s $M U_n$ and $M S O_n$

* the space $K(\mathbb{Z},2)$, 

  whose Sullivan minimal model is the dg-algebra on a single degree-2 generator with trivial differential.


## References

For an early discussion of formal dg-algebras in the context of [[rational homotopy theory]] see section 12 of 

* [[Dennis Sullivan]], _Infinitesimal computations in topology_ , Publications Math&#233;matiques de l'IH&#201;S, 47 (1977), p. 269-331 (numdam: [djvu](http://archive.numdam.org/article/PMIHES_1977__47__269_0.djvu), [pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))

* [[Pierre Deligne]], Phillip Griffiths, John Morgan, [[Dennis Sullivan]], _Real homotopy theory of K&#228;hler manifolds_, Invent. Math. 29 (1975), no. 3, 245--274, [doi](http://dx.doi.org/10.1007/BF01389853)
[[!redirects formal differential graded algebra]]
[[!redirects formal homotopy type]]

A survey is around definition 2.1 of

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


[[!redirects formal dg-algebra]]
[[!redirects formal dg-algebras]]

[[!redirects formal rational space]]
[[!redirects formal rational spaces]]

[[!redirects formal homotopy type]]
[[!redirects formal homotopy types]]
[[!redirects formal rational homotopy type]]
[[!redirects formal rational homotopy types]]
