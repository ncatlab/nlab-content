
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The effective topos $Eff$ is an example of an [[elementary topos]] with a [[natural numbers object]] which is not a [[Grothendieck topos]] (and doesn't even have a [[geometric morphism]] to [[Set]]).

It is an environment for [[higher-order logic|higher order]] [[recursion]] theory, where, in the [[internal logic]], it is provable that every [[total function]] from [[natural numbers]] to natural numbers is [[computable function|recursive]] (furthermore, the functor $Hom(1, -)$ from the effective topos into [[Set]], the inverse image part of a geometric morphism $Set \to Eff$ preserves the natural numbers object, giving a suitable version of this result in the external logic as well). 

It can be specified as the [[realizability topos]] for [[Kleene's first algebra]]. 

The effective topos construction alluded in the above paragraph can be performed more generally, in every topos $E$ with a natural numbers object, replacing [[Set]]. To every such topos one constructs the corresponding "external" effective topos $e E$ and the correspondence $E \mapsto e E$ extends to a functor admitting a [[full and faithful functor|fully faithful]] [[right adjoint]].  Kleene's first algebra can also be replaced by any [[partial combinatory algebra]], or even some more general types of gadgets; toposes obtained in this way are called [[realizability topos]]es.

The effective topos is the category obtained from the category of sets by first freely adjoining recursively-indexed coproducts (but being careful to preserve the empty set), and then adding quotients of (pseudo-)equivalence relations. ([RobinsonRosolini](#RobinsonRosolini)).

## Related concepts

* [[realizability]]

* [[topos of recursive sets|recursive topos]]

* [[effective 2-topos]]

## References

Reviews include 

* {#Vermeeren09} [[Stijn Vermeeren]], section 3 of _Realizability Toposes_, 2009 ([pdf](http://stijnvermeeren.be/download/mathematics/essay.pdf))

* J.M.E. [[Martin Hyland|Hyland]], _The effective topos_ in  A. S. Troelstra (ed.)  D. van Dalen (ed.) , _The L.E.J. Brouwer Centenary Symposium_, North-Holland  (1982)  pp. 165--216.

* [[Bart Jacobs]], Chapter 6 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;


In the context of [[triposes]]:

* Andy Pitts, _The theory of triposes_, thesis, [pdf](http://www.cl.cam.ac.uk/~amp12/papers/thet/thet.pdf)

Then

* Sori Lee, [[Jaap van Oosten]], _Basic subtoposes of the effective topos_, [arxiv/1201.2571](http://arxiv.org/abs/1201.2571)

* Edmund Robinson, Giuseppe Rosolini, _Colimit completions and the effective topos_, The Journal of symbolic logic, 55, no 2 (1990) ([JSTOR](http://www.jstor.org/discover/10.2307/2274658?uid=3738736&uid=2129&uid=2134&uid=2&uid=70&uid=4&sid=47698789906927))
 {#RobinsonRosolini}

* [[Aurelio Carboni]], _Some free constructions in realizability and proof theory_, J. Pure App. Alg., Vol. 103 Issue 2 (1995), 117-233. ([web](http://www.sciencedirect.com/science/journal/00224049/103/2)) 


[[!redirects effective toposes]]