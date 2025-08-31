

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Frobenius pseudomonoids

* table of contents
{: toc}

## Idea

The concept of **Frobenius pseudomonoid** is the [[categorification]] of that of [[Frobenius algebra]].  It can be defined in any [[monoidal bicategory]].  Since Frobenius pseudomonoids are closely related to [[star-autonomous categories]], they are sometimes called **$\ast$-autonomous pseudomonoids**.

## Definitions

Like a Frobenius algebra, a Frobenius pseudomonoid can be defined in many essentially equivalent ways.  Let $(K,\otimes,I)$ be a [[monoidal bicategory]], and let $(A,\mu,\eta)$ be a [[pseudomonoid]] in $K$.

1. $A$ is Frobenius if it is equipped with a morphism $\epsilon : A \to I$ such that the composite $A\otimes A \xrightarrow{\mu} A \xrightarrow{\epsilon} I$ is the counit of a specified [[2-adjunction]] $A\dashv A$.  ([Lauda06](#Lauda06)), ([Street04](#Street04))

1. $A$ is Frobenius if it is equipped with a specified [[2-adjunction]] $A\dashv A$, with counit $p:A\otimes A \to I$, and an isomorphism $p\circ (\mu\otimes 1) \cong p\circ (1\otimes \mu)$.  ([Day-Street 03](#DayStreet03))

There should also be a definition in terms of an interacting pseudomonoid and pseudocomonoid structure, but I have not been able to find this in the literature.

Note that if $K$ is a [[compact closed bicategory]], then the 2-adjunction $A\dashv A$ can equivalently be expressed as an equivalence $A\simeq A^\circ$ from $A$ to its specified dual object.

## Relation to $\ast$-autonomy

+-- {: .un_theorem}
###### Theorem
A [[star-autonomous category]] is equivalent to a Frobenius pseudomonoid in the monoidal bicategory [[Prof]] whose multiplication $A\otimes A \to A$, unit $I\to A$, and duality equivalence $A\simeq A^\circ$ are [[representable functor|representable]] [[profunctors]] (i.e. [[functors]]).
=--
+-- {: .proof}
###### Proof
See [Day-Street 03](#DayStreet03) and [Street04](#Street04).
=--

Note that the morphisms $\epsilon : A\to I$, $p:A\otimes A\to I$, and the induced comultiplication $A\to A\otimes A$ are *not* representable.  A general Frobenius pseudomonoid in $Prof$, without any representability conditions, may be called a [[promonoidal category|pro]]-$\ast$-autonomous category.

+-- {: .un_remark}
###### Remark
There is another relation between Frobenius algebras and $\ast$-autonomous categories: ([Egger10](#Egger10)) shows that cocomplete $\ast$-autonomous [[posets]] are equivalently Frobenius algebras in the $\ast$-autonomous category [[Sup]].
=--

+-- {: .un_remark}
###### Remark
This characterisation of $\ast$-autonomous algebras in terms of pseudo-Frobenius algebras can further be refined to characterise [[autonomous categories]]. Namely, an autonomous category is a representable pseudo-Frobenius algebra in [[Prof]] whose pseudomonoid and pseudocomonoid structure not only are adjoint, but which also satsify "locality" coherence equations [Bartlett-Vicary 10](#BartlettVicary10).
=--


## References

* [[Brian Day]] and [[Ross Street]], *Quantum categories, star autonomy, and quantum groupoids*, 2003, [arxiv](https://arxiv.org/abs/math/0301209)
 {#DayStreet03}

* [[Ross Street]], *Frobenius monads and pseudomonoids*, 2004, [DOI](http://dx.doi.org/10.1063/1.1788852), [pdf](http://maths.mq.edu.au/~street/Frob.pdf)
 {#Street04}

* [[Aaron Lauda]], *Frobenius algebras and planar open string topological field theories*, 2005; [arxiv](https://arxiv.org/abs/math/0508349)
 {#Lauda05}

* [[Aaron Lauda]], *Frobenius algebras and ambidextrous adjunctions*, 2006; [TAC](http://tac.mta.ca/tac/volumes/16/4/16-04abs.html)
 {#Lauda06}

* [[Bruce Bartlett]] and [[Jamie Vicary]], *Compact categories as dagger-Frobenius pseudoalgebras*, 2010, [QPL2010](https://www.youtube.com/watch?v=rZp1dPJxG3I)
 {#BartlettVicary10}

* [[Jeff Egger]], *The Frobenius relations meet linear distributivity*, 2010 [TAC](http://tac.mta.ca/tac/volumes/24/2/24-02abs.html)
 {#Egger10}

* [[Lawrence Dunn]] and [[Jamie Vicary]], *Coherence for Frobenius pseudomonoids and the geometry of linear proofs*, 2019, Logical Methods in Computer Science, July 26, 2019, Volume 15, Issue 3, <a href = "https://doi.org/10.23638/LMCS-15(3:5)2019">LCMS</a>
 {#DunnVicary19}

[[!redirects Frobenius pseudomonoids]]
[[!redirects star-autonomous pseudomonoid]]
[[!redirects star-autonomous pseudomonoids]]
[[!redirects *-autonomous pseudomonoid]]
[[!redirects *-autonomous pseudomonoids]]
