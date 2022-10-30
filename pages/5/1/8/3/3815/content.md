
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of $(\infty,1)$-Kan extension is the generalization of the notion of [[Kan extension]] from [[category theory]] to [[(∞,1)-category theory]].


## Definition

### General

Independent of any models or concrete realizations chosen, the notion of $(\infty,1)$-Kan extension is intrinsically determined from just the notions of 

* [[(∞,1)-functor]], 

* [[(∞,1)-category of (∞,1)-functors]]

*  [[adjoint (∞,1)-functor]].

In terms of these, for $f : C \to C'$ any [[(∞,1)-functor]] and any [[(∞,1)-category]] $A$, there is an induced $(\infty,1)$-functor $f^* : Func_{(\infty,1)}(C',A) \to Func_{(\infty,1)}(C,A)$.

The  **left $(\infty,1)$-Kan extension functor** is the left [[adjoint (∞,1)-functor]] to $f^*$.

The  **right $(\infty,1)$-Kan extension functor** is the right [[adjoint (∞,1)-functor]] to $f^*$.

Given different incarnations of or models for the notion of [[(∞,1)-category]], there are accordingly different incarnations and models of this general abstract prescription.


#### In terms of quasi-categories


([LurieHTT, def. 4.3.2.2, 4.3.3.2](#LurieHTT))


#### In terms of Kan-complex enriched categories

see [[homotopy Kan extension]]

#### In terms of simplicial model categories


see [[homotopy Kan extension]]

## Properties

### Pointwise (strong)
 {#Pointwise}

$\infty$-Kan extensions as above are [pointwise/strong](Kan+extension#Pointwise). That is in fact the very content of ([LurieHTT, def. 4.3.2.2, 4.3.3.2](#LurieHTT)).

### As adjoints to pullbacks

left/right $\infty$-Kan extension is left/right [[adjoint (∞,1)-functor]] to restriction. ([LurieHTT, prop. 4.3.3.7](#LurieHTT))

## Related concepts

* [[Kan extension]]

* **$(\infty,1)$-Kan extension**

## References

A general concept of $(\infty,1)$-Kan extensions in terms of quasi-categories are discussed in section 4.3 of

* {#LurieHTT} [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

For [[simplicially enriched categories]] and [[model categories]] a discussion is in section A.3.3 there.

Coinciding left/right ([[ambidextrous adjunction|ambidextrous]]) $\infty$-Kan extensions along maps of [[∞-groupoids]] are discussed in 

* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], section 4 of _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_

Pointwise [[homotopy Kan extensions]] are discussed in 

* {#Radulescu-Banu06} Andrei Radulescu-Banu, _Cofibrations in Homotopy Theory_ ([arXiv:0610009](http://arxiv.org/abs/math/0610009))

* {#Cisinski09} [[Denis-Charles Cisinski]], _Locally constant functors_, Math. Proc. Camb. Phil. Soc. (2009), 147, 593 ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/lcmodcat3.pdf))

* {#Gonzales11} Beatriz Rodriguez Gonzalez, section 4 of _Realizable homotopy colimits_ ([arXiv:1104.0646](http://arxiv.org/abs/1104.0646))



See also

* [[Samuel Isaacson]], _A note on unenriched homotopy coends_ ([pdf](http://www.math.uwo.ca/~sisaacso/PDFs/coends.pdf))

[[!redirects (∞,1)-Kan extension]]
[[!redirects (∞,1)-Kan extensions]]
[[!redirects (infinity,1)-Kan extensions]]

[[!redirects pointwise (∞,1)-Kan extension]]
[[!redirects pointwise (∞,1)-Kan extensions]]

[[!redirects pointwise (infinity,1)-Kan extension]]
[[!redirects pointwise (infinity,1)-Kan extensions]]