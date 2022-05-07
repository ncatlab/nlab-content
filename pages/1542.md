
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

The _codiscrete groupoid_ on a [[set]] is the [[groupoid]] whose [[object]]s are the elements of the [[set]] and which has a _unique [[morphism]]_ for every ordered pair of objects.

This is also called the **pair groupoid** of $X$ and sometimes also the __chaotic groupoid__ , __indiscrete groupoid__, or __coarse groupoid__ on $X$, in older literature also [[Brandt groupoid]].


## Definition

For $X$ set, the **codiscrete groupoid** of $X$ is the groupoid $Codisc(X)$ with

* $Obj(X) = X$;

* $Mor(X) = X \times X$.

This definition makes sense also [[internal category|internally]], for $X$ an object in any category with finite [[limit]]s. (In fact, this is one of those cases where the category can easily be defined with some limits lacking; we need only finite [[product]]s of $X$.)



**Remark** The codiscrete groupoid on $X$ is also sometimes called 
the _chaotic groupoid_ on $X$. The intuition is probably that "everything being connected with everything else sounds pretty chaotic", but one can argue that the term "chaotic groupoid" exactly misses the true intrinsic nature of codiscrete groupoids: since these are all just "puffed up versions of the point" they are "maximally homogenous" things. Which space would be less chaotic than the point?




## Properties

* Every codiscrete groupoid on an [[inhabited set]] is [[contractible space|contractible]]: [[equivalence of categories|equivalent]] to the [[point]]. More generally, any codiscrete groupoid is equivalent to a [[truth value]].

* For $X$ a [[finite set]] of cardinality $n \gt 0$, the [[category algebra]] of $Codisc(X)$ is the algebra of $n\times n$ matrices. The contractibility of $Codisc(X)$ is reflected in the fact that this algebra is [[Morita equivalence|Morita equivalent]] to the [[ground ring]], which is the category algebra of the [[point]].

  This maybe serves to illustrate: even though codiscrete groupoids are pretty trivial, they are not too trivial to be entirely without interest. Often it is useful to have big puffed-up versions of the point available.

*  The underlying [[quiver]] of a codiscrete groupoid is a [[complete graph]] (in that there is one *and only one* edge between any ordered pair of vertices).

* The [[nerves]] of codiscrete groupoids are precisely the [[codiscrete objects]] in [[sSet]], regarded as a [[cohesive topos]].

## Related concepts

* [[delooping groupoid]]

* [[discrete groupoid]]

* [[indiscrete category]]

[[!redirects codiscrete groupoid]]
[[!redirects codiscrete groupoids]]

[[!redirects codiscrete category]]
[[!redirects codiscrete categories]]

[[!redirects pair groupoid]]
[[!redirects pair groupoids]]

[[!redirects chaotic groupoid]]
[[!redirects chaotic groupoids]]
