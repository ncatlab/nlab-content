
> This entry is about [[rings]] which mimic the [[composition]] operation on endo-functions on the [[ground ring]]. For the unrelated notion of [[algebras]] mimicking the *composition of sums of squares* see at *[[composition algebra]]*.


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of *composition rings* is an abstraction of the [[structure]] present in a [[ring of functions]] from the [[ground ring]] to itself: In addition to (pointwise) [[addition]] and [[multiplication]], there is a compatible operation of *[[composition]]*.

## Definition 

A *composition ring* is a [[commutative ring]] $R$ equipped with an operation 
$$(-)\circ(-) \colonR \times R \to R$$ 
such that for all [[elements]] $f \in R$, $g \in R$, and $h \in R$, we have:

1. $(f + g) \circ h = (f \circ h) + (g \circ h)$,

1. $(f \cdot g) \circ h = (f \circ h) \cdot (g \circ h)$,

1. $f \circ (g \circ h) = (f \circ g) \circ h$
  
   ([[associativity]] of composition).


## Examples

* The [[endofunction|endo]-[[function algebra]] on a [[commutative ring]] is a composition ring, with "$\circ$" being the [[composition]] of functions.

* In particular, every [[polynomial ring]] is a composition ring with "$\circ$" being the actual [[composition]] of polynomials regarded as [[functions]] from the [[ground ring]] to itself.

* Every commutative ring becomes a composition ring by setting $f \circ g \coloneqq f$. 


## See also

* [[commutative ring]]

* [[polynomial ring]]

* [[function algebra]]

* *un-related*: [[composition algebra]]


## References 

The concept is due to:

* Irving Adler, *Composition rings*, Duke Mathematical Journal, **29** 4 (1962) 607–623, $[$[doi:10.1215/S0012-7094-62-02961-7](https://projecteuclid.org/journals/duke-mathematical-journal/volume-29/issue-4/Composition-rings/10.1215/S0012-7094-62-02961-7.short), ISSN 0012-7094, MR 0142573$]$

See also:

* Wikipedia, *[Composition ring](https://en.m.wikipedia.org/wiki/Composition_ring)*

* Erhard Aichinger, *The Structure of Composition Algebras*(1998) $[$[pdf](http://www.algebra.uni-linz.ac.at/~erhard/Diss/diss.pdf)$]$

[[!redirects composition rings]]