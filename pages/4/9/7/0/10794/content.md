
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

> Not to be confused with the notion of *[[coherence space]]* in [[models]] of [[linear logic]].

***

#Contents#
* table of contents
{:toc}

## Idea

A _coherent space_ (alias _spectral topological space_) is a [[topological space]] which is [[homeomorphism|homeomorphic]] to the [[spectrum of a commutative ring]], hence to the topological space underlying an [[affine scheme]].

Equivalently, it is a [[compact]] [[sober]] [[topological space]]
whose collection of compact open subsets is closed under finite intersections and forms a topological base.

Morphisms of coherent spaces are continuous maps
such that preimages of compact open subsets are again compact.

## Stone duality for coherent spaces

Passing from a coherent space to its lattice of compact open subsets
establishes a contravariant equivalence
from the category of coherent spaces
to the category of (bounded) [[distributive lattices]].

A coherent space is Hausdorff if and only if it is a [[Stone space]].
Under Stone duality for coherent spaces,
this corresponds to the fact that in a [[distributive lattice]] $L$
every element has a complement if and only if $L$ is a [[Boolean algebra]].

In particular, restricting the Stone duality equivalence between
coherent spaces and distributive lattices
to Stone spaces and Boolean algebras
recovers the classical Stone duality.

## Coherent locales

A [[locale]] is coherent if its [[compact elements]]
are closed under finite meets and any element is a join of compact elements.

A morphism of coherent locales is a morphism $f$ of [[locales]]
such that $f^*$ preserves compact elements.

Assuming the [[axiom of choice]], coherent locales are
automatically spatial, and are equivalent to the category of [[Priestley spaces]]. 

The category of coherent locales is contravariantly equivalent
to the category of [[distributive lattices]].
This statement does not depend on the [[axiom of choice]],
unlike the point-set version above.

## Related notions

* [[coherent topos]]

* [[Priestley space]]

## References

* [[Peter Johnstone]], _[[Stone Spaces]]_.

* [[Michael Barr]], [[John Kennison]], [[Robert Raphael]], *Countable meets in coherent spaces with applications to the cyclic spectrum*, Theory Appl. Categories **25** 19 (2011), 508–232 &lbrack;[tac:25-19](http://www.tac.mta.ca/tac/volumes/25/19/25-19abs.html)&rbrack;


* Max Dickmann, Niels Schwartz, [[Marcus Tressl]], _Spectral Spaces_. New Mathematical Monographs 35 (2019).  Cambridge: Cambridge University Press. ISBN 9781107146723.

See also:

* Wikipedia, _[Spectral space](http://en.wikipedia.org/wiki/Spectral_space)_

[[!redirects spectral topological space]]
[[!redirects spectral topological spaces]]

[[!redirects spectral space]]
[[!redirects spectral spaces]]


[[!redirects coherent topological space]]
[[!redirects coherent topological spaces]]

[[!redirects coherent spaces]]
[[!redirects coherent locale]]
[[!redirects coherent locales]]

[[!redirects coherent map]]
[[!redirects coherent maps]]