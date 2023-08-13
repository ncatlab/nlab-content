
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


A _coalgebra_ or _comodule_ over a [[comonad]] $C$ on a [[category]] $A$ is an [[object]] $a\in A$ with a [[morphisms]] $a\to C a$ satisfying [[axioms]] [[formal dual|formally dual]] to those for an [[algebra over a monad]].  The category of coalgebras is called its (co-)[[Eilenberg-Moore category]] and satisfies a universal property dual to that of the [[Eilenberg-Moore object]] for a monad; it can thereby be internalized to any [[2-category]].  The [[forgetful functor]] from the category of coalgebras to the category $A$ is called a [[comonadic functor]].  Similarly, a comonad also has a [[co-Kleisli category]].


## Examples
 {#Examples}

* the modality ! (of course) in [[linear logic]] is modeled by a comonad and its coalgebras, which are also comonoids, allow us to model intuitionistic formulas in categorical logic

* [[partial differential equations]] are the coalgebras of a [[jet comonad]] (see [there](jet+comonad#References))

* well-behaved [[lenses (in computer science)]] are the coalgebras of the [[costate comonad]] (see [there](lens+in+computer+science#LensesAreCostateCoalgebras))


## Related concepts

* [[topos of coalgebras over a comonad]]

* [[coalgebra over an endofunctor]]

* [[cocommutative coalgebra]]



## References

Some introductory material on [[comonads]], [[coalgebras]] and [[co-Kleisli morphisms]] can be found in

* [[Valeria de Paiva]], _The Dialectica Categories_, Chapter 2. ([Ph Thesis](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-213.pdf))

* [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 5. ([arXiv](http://arxiv.org/abs/1912.10642))

On [[model category]]-[[mathematical structure|structures]] on coalgebras over a comonad:


* [[Kathryn Hess]], [[Brooke Shipley]], *The homotopy theory of coalgebras over a comonad*, Proceedings of theLondon Mathematical Society **108** 2 (2014) &lbrack;[arXiv:1205.3979](https://arxiv.org/abs/1205.3979), [doi:10.1112/plms/pdt038](https://doi.org/10.1112/plms/pdt038)&rbrack;


[[!redirects coalgebras over a comonad]]
[[!redirects coalgebras over comonads]]

[[!redirects coalgebra of a comonad]]
[[!redirects coalgebras of a comonad]]

[[!redirects comodule over a comonad]]
[[!redirects comodules over a comonad]]

[[!redirects comodule for a comonad]]
[[!redirects comodules for a comonad]]




