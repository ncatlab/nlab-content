
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One analog in [[(∞,1)-category theory]] of _[[epimorphism]]_ in [[category theory]]. Beware that there are other variants such as _[[effective epimorphism in an (infinity,1)-category]]_ and generally the concept of _[[n-epimorphism]]_.

## Definition

For $C$ an [[(∞,1)-category]], a [[morphism]] $f : X \to Y$ in $C$ is an **[[epimorphism]]** if for all $A \in C$ the induced morphism

$$
  C(f,A) : C(Y,A) \to C(X,A)
$$

is a [[monomorphism in an (∞,1)-category]] in [[∞Grpd]].


## Examples
 {#Examples}

* A morphism $A\to B$ of [[E-infinity rings]] is an epimorphism iff $B$ is smashing over $A$, i.e., if $B\wedge_A B\approx B$.

* A morphism $X\to Y$ between [[connected spaces]] is an epimorphism iff $Y$ is formed via a Quillen-plus construction from a [[perfect group|perfect]] [[normal subgroup]] of the [[fundamental group]] $\pi_1 X$.  More generally, a map of spaces is an epi iff all its fibers are [[acyclic spaces]] in the sense that their [[suspensions]] are [[contractible]].  This is discussed in [Raptis](#Raptis).

* A generalization of this to epimorphisms and acyclic spaces in [[(infinity,1)-toposes]] is discussed in [Hoyois](#Hoyois).

## References

* {#Raptis} G. Raptis, *Some characterizations of acyclic maps*, [arxiv](https://arxiv.org/abs/1711.08898), 2017

* {#Hoyois} Marc Hoyois, *On Quillen's plus construction*, [web](http://www.mathematik.ur.de/hoyois/papers/acyclic.pdf), 2019


[[!redirects epimorphism in an (∞,1)-category]]
