

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


\tableofcontents

## Idea

The concept of **Frobenius pseudomonoid** is the [[categorification]] of that of [[Frobenius algebra]].  It can be defined in any [[monoidal bicategory]].  Since Frobenius pseudomonoids are closely related to [[star-autonomous categories]], they are sometimes called **$\ast$-autonomous pseudomonoids**.

## Definitions

Like Frobenius algebras, Frobenius pseudomonoids can be defined in many essentially equivalent ways.  Let $(K,\otimes,I)$ be a [[monoidal bicategory]], and let $(A,\mu,\eta)$ be a [[pseudomonoid]] in $K$.

1. $A$ is Frobenius if it is equipped with a morphism $\epsilon : A \to I$ such that the composite $A\otimes A \xrightarrow{\mu} A \xrightarrow{\epsilon} I$ is the counit of a specified [[2-adjunction]] $A\dashv A$.  ([Lauda06](#Lauda06)), ([Street04](#Street04))

1. $A$ is Frobenius if it is equipped with a specified [[2-adjunction]] $A\dashv A$, with counit $p:A\otimes A \to I$, and an isomorphism $p\circ (\mu\otimes 1) \cong p\circ (1\otimes \mu)$.  ([Day-Street 03](#DayStreet03))

There should also be a definition in terms of an interacting pseudomonoid and pseudocomonoid structure, but I have not been able to find this in the literature.

Note that if $K$ is a [[compact closed bicategory]], then the 2-adjunction $A\dashv A$ can equivalently be expressed as an equivalence $A\simeq A^\circ$ from $A$ to its specified dual object.

## Properties

### Relation to $\ast$-autonomy

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


## Related concepts

* [[Frobenius monad]]

## References

* {#DayStreet03} [[Brian Day]], [[Ross Street]], *Quantum categories, star autonomy, and quantum groupoids*, in: *Galois Theory, Hopf Algebras, and Semiabelian Categories*, Fields Institure Communications **43**, AMS (2004) 187-225 &lbrack;[arxiv:math/0301209](https://arxiv.org/abs/math/0301209), [ISBN:978-0-8218-3290-5](https://bookstore.ams.org/view?ProductCode=FIC/43)&rbrack;
 
* {#Street04} [[Ross Street]], *Frobenius monads and pseudomonoids*, J. Math. Phys. **45** 3930 (2004) &lbrack;[doi:10.1063/1.1788852](https://doi.org/10.1063/1.1788852)&rbrack;

* {#Lauda05} [[Aaron Lauda]], *Frobenius algebras and planar open string topological field theories*, 2005; [arxiv](https://arxiv.org/abs/math/0508349)
 
* {#Lauda06} [[Aaron Lauda]]: *Frobenius algebras and ambidextrous adjunctions*, Theory and Applications of Categories **16** 4 (2006) 84-122 &lbrack;[tac:16-04](http://tac.mta.ca/tac/volumes/16/4/16-04abs.html), [arXiv:math/0502550](http://arxiv.org/abs/math/0502550)&rbrack; 
 
* {#BartlettVicary10} [[Bruce Bartlett]], [[Jamie Vicary]], *Compact categories as dagger-Frobenius pseudoalgebras*, talk at QPL 2010 &lbrack;[pdf](https://www.cs.ox.ac.uk/people/bob.coecke/Vicary.pdf), video:[YT](https://www.youtube.com/watch?v=rZp1dPJxG3I)&rbrack;
 
* {#Egger10} [[Jeff Egger]]: *The Frobenius relations meet linear distributivity*, Theory and Applications of Categories **24**2 (2010) &lbrack;[tac:24-2](http://tac.mta.ca/tac/volumes/24/2/24-02abs.html)&rbrack;
 
*  {#DunnVicary19} Lawrence Dunn, [[Jamie Vicary]]: *Coherence for Frobenius pseudomonoids and the geometry of linear proofs*, Logical Methods in Computer Science **15** 3 (2019) &lbrack;<a href = "https://doi.org/10.23638/LMCS-15(3:5)2019">doi:10.23638/LMCS-15(3:5)2019</a>, [arXiv:1601.05372](https://arxiv.org/abs/1601.05372)&rbrack;


[[!redirects Frobenius pseudomonoids]]
[[!redirects star-autonomous pseudomonoid]]
[[!redirects star-autonomous pseudomonoids]]
[[!redirects *-autonomous pseudomonoid]]
[[!redirects *-autonomous pseudomonoids]]
