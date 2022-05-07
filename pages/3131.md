
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The classical notion of an [[internal category]] in a category with [[pullbacks]], can be generalized by replacing pullbacks with cotensor products of comodules in a [[monoidal category]]. 


## Definition

One typically starts with a monoidal category $M = (M, \otimes, 1)$ which is _regular_ in the sense that it has [[equalizers]] which are preserved by $\otimes$ on both sides. (The monoidal structure does _not_ need be symmetric.)

There is a [[bicategory]] $Comod(M)$ of [[comonoids]] and _[[bicomodules]]_ in $M$: this is a special case of the bicategory $Mod(K)$ of [[monads]] and [[module over a monad|bimodules]] in a bicategory $K$, where in this case $K = \mathbf{B} M^{op} = (\mathbf{B} M)^{co}$.  Then an **internal category in $M$** is a [[monad]] in $Comod(M)$.

There are two kind of morphisms of noncartesian internal categories: [[functors]] and [[cofunctor|cofunctors]] (which here are *not* the same as [[contravariant functors]]).


## Examples

Because every [[set]] is canonically a comonoid with respect to the [[cartesian product]], a comonoid in [[Set]] is just a set and a bicomodule is a [[span]], and a monad in the bicategory of spans of sets is just a small category.  More generally, an internal category in the above sense in any category with finite cartesian products (and equalizers, of course, hence a [[finitely complete category]]) is just an [[internal category]] in the usual sense.


## References

The main historical reference is Marcelo Aguiar's 1997 Cornell thesis *Internal categories and quantum groups* ([pdf](http://pi.math.cornell.edu/~maguiar/thesis2.pdf)), under the guidance of S. Chase. [[George Janelidze]] calls such generalization **noncartesian internal category**, because if the tensor product is the cartesian product the notion reduces to the traditional internal category. 

+-- {: .query}
[[David Roberts]]: I think Ross Street and the other Australian category theorists call this a quantum category - I did go to a talk once, but my notes are elsewhere.

[[David Roberts]]: It has been pointed out to me by Jeff Egger that this is incorrect, in that quantum categories as defined by the Australian school are generalisations of bimonoids/bialgebras, whereas internal categories generalise monoids (via horizontal categorification). Hmm, I wasn't paying attention in that talk as much as I thought I was.
=--


[[!redirects internal category in a monoidal category]]
[[!redirects internal categories in a monoidal category]]
[[!redirects internal categories in monoidal categories]]
[[!redirects category in a monoidal category]]
[[!redirects categories in a monoidal category]]
[[!redirects categories in monoidal categories]]
