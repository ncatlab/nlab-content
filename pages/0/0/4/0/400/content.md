
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Roughly speaking, a **factorization system** on a [[category]] consists of two classes of [[morphism|maps]], $L$ and $R$, such that every map factors into an $L$-map followed by an $R$-map, and the $L$-maps and $R$-maps satisfy some [[lifting property|lifting]] or [[diagonal fill-in]] property.  The various ways of filling in the details give rise to many kinds of factorization systems:

* In most of the literature, "factorization system" unqualified refers specifically to [[orthogonal factorization system]]s (OFS).

* [[weak factorization system]]s (WFS) are "more general" than orthogonal ones, in the sense that every OFS is also a WFS.  But since the most important examples of WFS (those that occur in [[model category|model categories]]) are not OFS, intuitively they are more or less independent concepts.

* [[algebraic weak factorization system]]s (AWFS) are a strengthened "algebraic" version of WFS in which the factorizations are functorial and the two classes of maps are algebraic.

* In an [[enriched category]] it is natural to consider [[enriched factorization system|enriched (orthogonal) factorization systems]].  The enriched version of WFS falls under [[enriched model category|enriched model categories]].

* In a [[bicategory]] (i.e. a possibly non-strict [[2-category]]) one wants instead the notion of [[factorization system in a 2-category]], which is like a Cat-enriched OFS "up to isomorphism."  The situation in an [[n-category]] is analogous; see for instance [[orthogonal factorization system in an (∞,1)-category]] and [[orthogonal factorization system in a derivator]].

* In a [[model category]], a [[homotopy factorization system]] leverages the ambient weak factorization systems to give a presentation of an orthogonal factorization system in the underlying $(\infty,1)$-category.

* In a [[strict 2-category]] there is also the notion of an [[enhanced factorization system|enhanced (orthogonal) factorization system]], of which the main example is [[bo-ff factorization system|(bo,ff)]] in [[Cat]].

* A [[strict factorization system]] is one in which the factorizations are specified uniquely on the nose, rather than merely up to isomorphism.

* A [[factorization system over a subcategory]] is a common generalization of orthogonal and strict factorization systems, which requires uniqueness of factorizations only up to specified zigzags.

Particular examples of factorization systems of various sorts can be found on the individual pages referred to above.


## Higher-ary factorization systems

The above notion of "binary" factorization system can be generalized to factor a morphism into more than two factors.

* The orthogonal 3-ary version is a [[ternary factorization system]].

* This has a generalization to a [[k-ary factorization system]].

* The corresponding 3-ary version for *weak* factorization systems is closely related to the notion of [[model category]] (one of the main applications of weak factorization systems).

## Cylinder factorization systems

See [[cylinder factorisation system]].


## Related concepts

* [[anodyne morphism]], [[small object argument]]

* [[Joyal-Tierney calculus]]

## References

* [[joyalscatlab:HomePage|Joyal's CatLab]], _[[joyalscatlab:Factorization systems]]_

Introductory texts:

* [[Introduction to Homotopy Theory]]
* {#Riehl2008} [[Emily Riehl]], [_Factorization Systems_](https://math.jhu.edu/~eriehl/factorization.pdf), 2008
* The following dissertation section is entirely written after learning from Riehl's note above, but has complementary examples and may dive deeper into some proofs:
  * {#Nuyts2020} [[Andreas Nuyts]], _Contributions to Multimode and Presheaf Type Theory, section 2.4: Factorization Systems_, [PhD thesis](https://lirias.kuleuven.be/retrieve/581985), KU Leuven, Belgium, 2020

The factorization systems were probably first introduced in 

* [[S. MacLane]], _Duality for groups_,  Bull. Amer. Math. Soc. __56__,  (1950). 485--516, [MR0049192](http://www.ams.org/mathscinet-getitem?mr=0049192), [doi](http://dx.doi.org/10.1090/S0002-9904-1950-09427-0)
* J. R. Isbell, _Some remarks concerning categories and subspaces_, Canad. J. Math. __9__ (1957), 563--577; [MR0094405](http://www.ams.org/mathscinet-getitem?mr=0094405)

* [[Ross Street]], _Notes on factorization systems_, ([pdf](http://www.maths.mq.edu.au/~street/factoriz.pdf))
[[!redirects factorization systems]]

On the relationship between [[cones]] and factorisation systems:

* [[Rudolf-E. Hoffmann]], _Factorization of cones_, Mathematische Nachrichten **87** 1 (1979) 221-238. &lbrack;[doi:10.1002/mana.19790870120](https://doi.org/10.1002/mana.19790870120)&rbrack;

* [[Rudolf-E. Hoffmann]], _Factorization of cones II, with applications to weak Hausdorff spaces_, in: *Categorical Aspects of Topology and Analysis: Proceedings of an International Conference Held at Carleton University, Ottawa, August 11–15, 1981*, Springer (2006) &lbrack;[doi:10.1007/BFb0092878](https://doi.org/10.1007/BFb0092878)&rbrack;


A list of elementary examples of factorization systems 
(associated with the notions of: compact, discrete, connected, and totally disconnected spaces, dense image, induced topology, and separation axioms; finite groups being nilpotent, solvable, torsion-free, p-groups, and prime-to-p groups; injective and projective modules; injective, surjective, and split homomorphisms)

* M. Gavrilovich, [_The unreasonable power of the lifting property in elementary mathematics_](http://mishap.sdf.org/by:gavrilovich/expressive-power-of-lifting-property.pdf)

* M. Gavrilovich, [_A naive diagram-chasing approach to formalisation of tame topology_](http://mishap.sdf.org/by:gavrilovich/mintsGE.pdf)

[[!redirects factorization systems]]

[[!redirects factorisation system]]
[[!redirects factorisation systems]]



