
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea
 {#Idea}

A [[groupoid]] is *[[connected]]* if it is [[inhabited set|inhabited]] and every [[object]] is connected by a [[morphism]] to every other object.

So the [[skeleton|skeletal]] connected groupoids are precisely the [[delooping groupoids]] of [[groups]].

In [[homotopy theory]], [[groupoids]] model exactly the [[homotopy 1-types]] and connected groupoids model the [[connected homotopy type|connected]] homotopy 1-types. For instance the [[fundamental groupoid]] of a [[connected topological space]] is a connected groupoid.


Every [[category]] $C$ induces a [[free groupoid]] $F(C)$ by freely inverting all its [[morphisms]]. A category is called connected if the groupoid $F(C)$ is.




## Definition

A [[category]] $C$ is **connected** if it is [[inhabited set|inhabited]] and the following equivalent conditions hold:

* any two [[objects]] can be connected by a [[zigzag]] of [[morphisms]].

* the $\infty$-groupoidification of the category (the [[Kan fibrant replacement]] of its [[nerve]]) is a [[connected]] [[∞-groupoid]].

* the [[geometric realization]] of its [[nerve]] is a [[connected topological space]].

* the [[localization]] $C[C_1^{-1}]$ of $C$ at all its morphisms is a connected groupoid.

Note that the [[empty category]] is not connected.  For other purposes, one can argue about whether the [[empty set]] should be called "connected" (see [[connected space]]), but for the applications of connected categories, the empty category should definitely not be called connected.  In particular, a [[terminal object]] is not a [[connected limit]].


## Related concepts

* A *[[connected limit]]* is a [[limit]] whose domain [[diagram]] category is connected.

* [[connected homotopy type]]



## References

The notion of connected groupoids was originally defined in

* {#Brandt27} [[Heinrich Brandt]], *Über eine Verallgemeinerung des Gruppenbegriffes*, Mathematische Annalen **96** 1 (1927) 360-366 &lbrack;[doi:10.1007/BF01209171](https://doi.org/10.1007%2FBF01209171)&rbrack;

whence some authors also speak of *[[Brandt groupoids]]*.

For more see the references at *[[groupoids]]*.





[[!redirects connected category]]
[[!redirects connected categories]]
[[!redirects connected groupoid]]
[[!redirects connected groupoids]]
