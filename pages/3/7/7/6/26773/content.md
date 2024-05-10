
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

## Definition

A **polynomial comonad** on a category is a [[comonad]] whose underlying [[endofunctor]] is a [[polynomial functor]]. 

## Properties

* A polynomial comonad on [[Set]] is equivalent to a [[small category]] ([Ahman-Uustalu, 2016](#AhmanUustalu2016)). 

* A morphism of polynomial comonads on $\mathrm{Set}$ is equivalent to a [[retrofunctor]] ([Ahman-Uustalu, 2017](#AhmanUustalu2017)).

## References

Polynomial comonads were first studied under the name *directed containers* in: 

* {#AhmanChapmanUustalu2014} [[Danel Ahman]], [[James Chapman]], [[Tarmo Uustalu]], _When is a container a comonad?_, Logical Methods in Computer Science **10** 3 (2014) 1-48 &lbrack;[arXiv:1408.5809](https://arxiv.org/abs/1408.5809), <a href="https://doi.org/10.2168/LMCS-10(3:14)2014">doi:10.2168/LMCS-10(3:14)2014</a>&rbrack;

The equivalence between polynomial comonads on $\mathrm{Set}$ and small categories was shown in: 

* {#AhmanUustalu2016} [[Danel Ahman]], [[Tarmo Uustalu]], _Directed Containers as Categories_, EPTCS **207** (2016) 89-98 &lbrack;[arXiv:1604.01187](https://arxiv.org/abs/1604.01187), [doi:10.4204/EPTCS.207.5](https://doi.org/10.4204/EPTCS.207.5)&rbrack;

The observation that morphisms of polynomial comonads are the same as retrofunctors (under the name *cofunctor*) appears in:

* {#AhmanUustalu2017} [[Danel Ahman]], [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings **1827** (2017) 59-73 &lbrack;[PDF](https://ceur-ws.org/Vol-1827/paper11.pdf)&rbrack;

A detailed study of polynomial comonads and their morphisms appears in Chapter 7 of the (unpublished) book: 

* {#NiuSpivak2023} [[Nelson Niu]], [[David Spivak]], _Polynomial Functors: A Mathematical Theory of Interaction_, draft (2023) &lbrack;[arXiv:2312.00990](https://arxiv.org/abs/2312.00990)&rbrack;

The notion of (two-sided) [[comodule]] between polynomial comonads was given in: 

* {#Garner2019} [[Richard Garner]], _Polynomial comonads and comodules_, HoTTEST Seminar (2019) &lbrack;[slides](https://www.math.uwo.ca/faculty/kapulkin/seminars/hottestfiles/Garner-2019-12-11-HoTTEST.pdf), [video](https://www.youtube.com/watch?v=tW6HYnqn6eI)&rbrack;

[[!redirects polynomial comonads]]
[[!redirects directed container]]