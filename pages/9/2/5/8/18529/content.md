[[!redirects main theorem of perturbative renormalization theory]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A central result in the construction of [[perturbative quantum field theories]] via the method of [[causal perturbation theory]] is called the _main theorem of perturbative renormalization theory_. This says that any two _[[renormalization]] schemes_, hence any two solutions to the inductive construction of the [[S-matrix]] $V \mapsto S(V)$ for [[interaction]] terms $V$, are related by a unique transformation $Z \colon V \mapsto V'$

$$
  S' = S \circ Z
  \,.
$$

The collection of these operations $Z$ forms a [[group]] called the _[[Stückelberg-Peterson renormalization group]]_. Hence the space of renormalization schemes is a [[torsor]] over this group.

This theorem is a mathematical reflection of the idea that renormalization is about regarding a [[perturbative quantum field theory]] with [[interaction]] $V$ as a [[effective field theory]] at some energy scale and then discovering that at higher energy there is a more fundamental interaction $Z(V)$ which effectively looks like $V$ at lower energy.

## References

The theorem is originally due to 

* G. Popineau and [[Raymond Stora]], _A Pedagogical Remark on the Main Theorem of Perturbative Renormalization Theory, unpublished preprint

In various variants it has been (re-)proved in the following articles:

* G. Pinter, section 6 of _The Action Principle in Epstein Glaser Renormalization and Renormalization of the S-Matrix in $\phi^4$-Theory_, Annalen Phys. 10 (2001) 333-363 ([arXiv:hep-th/9911063](https://arxiv.org/abs/hep-th/9911063))

* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], section 4.1 of _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* [[Michael Dütsch]], [[Klaus Fredenhagen]], section 4.2 of _Causal perturbation theory in terms of retarded products, and a proof of the Action Ward Identity_,  Rev. Math. Phys. 16, 1291 (2004) ([arXiv:hep-th/0403213](https://arxiv.org/abs/hep-th/0403213))

* [[Stefan Hollands]], theorem 2 in _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys. 20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

Review is in 

* {#Rejzner16} [[Katarzyna Rejzner]], section 6.3 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))



[[!redirects Stückelberg-Peterson renormalization group]]
