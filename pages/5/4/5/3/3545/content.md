
>  This entry is about [[quasi-isomorphism]] to [[cochain cohomology]]. For [[infinitesimal neighbourhood|infinitesimal thickening]] of [[smooth manifolds]] see at _[[formal smooth manifold]]_.

***

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
* table of contents
{:toc}

## Definition

A [[dg-algebra]] $A$ is a **formal dg-algebra** if it is [[quasiisomorphism|quasi-isomorphic]] (i.e.: [[isomorphism|isomorphic]] in the [[homotopy category]] of the [[model structure on dg-algebras]])

$$
  A 
  \xrightarrow{\;\;\; \simeq \;\;\;}
  H^\bullet(A)
$$

to its [[chain homology and cohomology|chain (co)homology]] regarded as a dg-algebra with trivial differential. 

Since all dg-algebras are fibrant in the standard model, this is equivalent to the existence of a [[span]]

$$
  A \overset{\;\; \simeq_w \;\;}{\leftarrow} 
  Q A 
  \overset{\;\; \simeq \;\;}{\rightarrow}
  H^\bullet(A)
$$

of [[quasi-isomorphisms]] of dg-algebras.


## Examples

In [[rational homotopy theory]] [[rational topological spaces]] are encoded in their [[Sullivan algebra|Sullivan dg-algebras]] (cf. The [[fundamental theorem of dg-algebraic rational homotopy theory]]). A [[simply connected topological space]] $X$ whose Sullivan dg-algebra $\Omega^\bullet(X)$ is formal is called a **formal topological space**.  (One can also say a __formal rational space__, to distinguish from the unrelated formal spaces in [[formal topology]].)  Such a space represents a **formal homotopy type**.

Examples are

* compact [[Kähler manifolds]] (e.g. smooth projective varieties),

* [[Lie groups]],

* [[classifying spaces]]$\;B G$ of [[Lie groups]] $G$,

* some [[homogeneous spaces]] $G/H$,

* the unstable [[Thom spaces]] $M U_n$ and $M S O_n$,

* the [[Eilenberg-MacLane space]] $K(\mathbb{Z},n)$, 

  whose Sullivan minimal model is the dg-algebra on a single degree$=n$ generator with trivial differential.,

* [[the little n-disk operad is formal]].

## Related concepts

* [[H-cohomology]]


## References

For an early discussion of formal dg-algebras in the context of [[rational homotopy theory]] see section 12 of 

* [[Dennis Sullivan]], _Infinitesimal computations in topology_ , Publications Math&#233;matiques de l'IH&#201;S, 47 (1977), p. 269-331 (numdam: [djvu](http://archive.numdam.org/article/PMIHES_1977__47__269_0.djvu), [pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))

* [[Pierre Deligne]], Phillip Griffiths, John Morgan, [[Dennis Sullivan]], _Real homotopy theory of K&#228;hler manifolds_, Invent. Math. 29 (1975), no. 3, 245--274, [doi](http://dx.doi.org/10.1007/BF01389853)
[[!redirects formal differential graded algebra]]
[[!redirects formal homotopy type]]

A survey is around definition 2.1 of

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

Review with an eye towards the [[dd^c-lemma]] and [[H-cohomology]] is in

* {#Cavalcanti03} [[Gil Cavalcanti]], p. 12 of _New aspects of the $d d^c$-lemma_ ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

The case of [[Sullivan algebras]] of [[sphere bundles]]:

* Jiawei Zhou, *Formality of Sphere Bundles* &lbrack;[arXiv:2304.09594](https://arxiv.org/abs/2304.09594)&rbrack;


[[!redirects formal dg-algebra]]
[[!redirects formal dg-algebras]]

[[!redirects formal rational space]]
[[!redirects formal rational spaces]]

[[!redirects formal homotopy type]]
[[!redirects formal homotopy types]]
[[!redirects formal rational homotopy type]]
[[!redirects formal rational homotopy types]]
