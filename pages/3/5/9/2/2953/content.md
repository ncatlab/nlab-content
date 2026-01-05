
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a [[concrete category]], an **injective hull** of an object $A$ is an [[extension]] $A \stackrel{m}{\longrightarrow} B$ of $A$ such that $B$ is [[injective object|injective]] and $m$ is an [[essential embedding]]. It is the dual concept to a [[projective cover]].

Beware that, in general, there is no way of making the assignment of the injective hull to an object into a [[functor]] such that there is a [[natural transformation]] from the [[identity functor]] to that functor.


## Examples 

* In [[Vect]] every object $A$ has an injective hull, $A \stackrel{id_A}{\longrightarrow} A$. In other words, every vector space is an [[injective object]].
* In [[Pos]], every object has an injective hull—its [[MacNeille completion]].
* In [[Ab]], every object has an injective hull. The embedding $\mathbb{Z} \hookrightarrow \mathbb{Q}$ is an example.
* In the category [[Field]] of [[fields]] and algebraic field extensions, every object has an injective hull—its [[algebraic closure]].
* In the category of metric spaces and [[short maps]], the injective hull is a standard construction also known as the [[tight span]] (see [Wikipedia](http://en.wikipedia.org/wiki/Tight_span)).
* Given a ring $R$, the category $R-Mod$ of left $R$-modules has injective envelopes. Moreover, every essential monomorphism whose domain is an injective $R$-module is an isomorphism. The injective envelope of a module $M$ is a terminal object in the subcategory of the [[slice category]] $M/R-Mod$ consisting of the essential morphisms. (These terminal objects are called maximal essential extensions.)

## Generalization

Given a class $\mathcal{E}$ of objects in a category, an **$\mathcal{E}$-hull**
(or **$\mathcal{E}$-envelope**) of an object $A$ is a morphism $h: A \longrightarrow E$ into some $E$ in $\mathcal{E}$
such that the following two conditions hold:

1. Any morphism $A \longrightarrow E'$ to an object in $\mathcal{E}$ factors through $h$ via some morphism $E \longrightarrow E'$.

1. Whenever a morphism $f: E \longrightarrow E$ satisfies $f\circ h = h$, then it
must be an automorphism.

On the other hand, given a class $\mathcal{H}$ of *morphisms* in a category, an **$\mathcal{H}$-injective hull** of an object $A$ is a morphism $h:A\to E$ in $\mathcal{H}$ such that:

1. $E$ is an $\mathcal{H}$-injective object and

2. $h$ is $\mathcal{H}$-essential, i.e., if $k\circ h \in \mathcal{H}$, then $k\in\mathcal{H}$.

## Related concepts

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

* [[injective object]], [[injective presentation]], **injective envelope**, [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]

## References

Discussion in [[homological algebra]]:

* {#HiltonStammbach71} [[Peter Hilton]],  [[Urs Stammbach]], Section I.9 in: _A course in homological algebra_, Springer-Verlag, New York, 1971, Graduate Texts in Mathematics, Vol. 4 ([doi:10.1007/978-1-4419-8566-8](https://link.springer.com/book/10.1007/978-1-4419-8566-8), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/hilton-stammbach.pdf))

Discussion in general [[concrete categories]]:

* [[Jiri Adamek|Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]],  Definition 9.16 (page 156) in: [[The Joy of Cats]] (2004)

See also:

* [[Jiří Adámek]], [[Horst Herrlich]], [[Jiří Rosický]], [[Walter Tholen]], _Injective hulls are not natural_, Algebra univers. 48 (2002) 379--388 [doi](https://doi.org/10.1007/s000120200006) [pdf](https://link.springer.com/content/pdf/10.1007/s000120200006.pdf) [ps](http://www.iti.cs.tu-bs.de/~adamek/injective.hulls.AHRT.ps) 
* Jinzhog Xu; 1996; Flat Covers of Modules, SLNM 1634.
* [[Walter Tholen]], "Essential weak factorization systems".  *Contributions to General Algebra* 13 (2001) 321-333.  [ps](http://www.math.yorku.ca/~tholen/newessential.ps).

On injective hulls of [[partial order|partially ordered]] [[monoids]]:

* [[Joachim Lambek]], [[Michael Barr]], [[John Kennison]], [[Robert Raphael]], *Injective hulls of partially ordered monoids*, Theory Appl. Categories **26** 13 (2012) 338–348 &lbrack;[tac:16-13](http://www.tac.mta.ca/tac/volumes/26/13/26-13abs.html)&rbrack;


[[!redirects injective envelopes]]

[[!redirects injective hull]]
[[!redirects injective hulls]]

