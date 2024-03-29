
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
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

Not every [[abelian category]] is a [[concrete category]], such as [[Ab]] or $R$[[Mod]], hence its [[objects]] do not necessarily have underlying [[sets]] whose elements one can reason about. To circumvent this and reason by "[[diagram chasing|diagram chases]]" of elements in general abelian categories, one can instead use [[generalized elements]] in a suitable way. 

This is closely related to embedding the abelian category fully-faithfully and exactly into a concrete abelian category. See at _[[abelian category]]_ the section _[Embedding theorems](abelian+category#EmbeddingTheorems)_ for more on this.

## Definition

One definition goes likes this ([MacLane, VIII.4](#MacLane) and also for instance [Gelfand-Manin, II.5](#Gelfand-Manin)):

An __element__ of an [[object]] $W$ in a given [[abelian category]] $\mathcal{A}$ is an [[equivalence class]] $[X,h]$ of pairs $(X,h)$ where $X$ is an object of $\mathcal{A}$ and $h:X\to W$ a morphism (hence a [[generalized element]]) and the equivalence is defined as follows: $[X,h] = [Y,k]$ iff there exists an object $Z$ in $\mathcal{A}$ and [[epimorphisms]] $u:Z\to X$, $v:Z\to Y$ such that $h\circ u = k\circ v : Z\to W$. 

However, beware that the passage to equivalence classes does not respect the abelian group structure and hence generalized elements in this sense cannot be added or subtracted. A more natural approach is discussed in [Bergman 1974](#Bergman74) where the actual generalized elements are remembered but a refinement of their domain is allowed, much as familiar from [[topos theory]]. 

## References

Equivalence classes of generalized elements are considered for instance in

* [[Saunders Mac Lane]], _[[Categories Work|Categories for the working mathematician]]_, 2nd edition, Springer 1998. 
 {#MacLane}

* [[Sergei Gelfand]], [[Yuri Manin]], _Methods of homological algebra_,  transl. from the 1988 Russian (Nauka Publ.) original. Springer 1996. xviii+372 pp.; 2nd corrected ed. 2002.
{#Gelfand-Manin}


Genuine generalized elements are considered in

* {#Bergman74} [[George Bergman]], _A note on abelian categories -- translating element-chasing proofs, and exact embedding in abelian groups_ (1974) &lbrack;[pdf](http://math.berkeley.edu/~gbergman/papers/unpub/elem-chase.pdf), [[Bergman-ElementChasing.pdf:file]]&rbrack;
 

[[!redirects elements in an abelian category]]
[[!redirects elements in abelian categories]]

[[!redirects element of an abelian category]]
[[!redirects elements of an abelian category]]


[[!redirects element in abelian category]]


