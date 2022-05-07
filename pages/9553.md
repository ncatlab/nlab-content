
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The Baum-Connes conjecture asserts that under suitable technical conditions, the [[operator K-theory]]/[[KK-theory]] of the [[groupoid convolution algebra]] of an [[action groupoid|action]] [[topological groupoid]] $X//G$ is equivalent to the _$G$-[[equivariant cohomology|equivariant]]_ [[topological K-theory]]/[[equivariant operator K-theory]]/[[equivariant KK-theory]] of $X$. Moreover, it says that this equivalences is exhibited by the _[[analytic assembly map]]_.
(Just the [[injective map|injectivity]] of this map is related to the [[Novikov conjecture]].)

The original version of the Baum-Connes conjecture ([Baum-Connes](#BaumConnes00)) stated for a suitable [[topological group]] $G$ that with $X = E G \simeq \ast$ the point incarnated as the $G$-[[universal principal bundle]] with its free $G$-[[action]] the [[analytic assembly map]] (the $G$-equivariant [[index]] map)

$$
  K_\bullet^G(E G) \stackrel{}{\to} K_\bullet(C(\mathbf{B}G))
  \,,
$$

from the $G$-[[equivariant K-theory]] of $E G$ to the [[operator K-theory]] of the [[group algebra]], hence the [[groupoid convolution algebra]] of the [[delooping]] groupoid $\mathbf{B}G \simeq \ast // G$, is an [[isomorphism]].

This Baum-Connes conjecture is known to be true for

* [[compact topological groups]],
* [[abelian groups]],
* [[Lie groups]] with finitely many [[connected components]];
* $p$-adic groups,
*  adelic groups.

It is not known if the conjecture is true for all [[discrete groups]].

Later the statement was generalized ([Tu 99](#Tu99)) to more general groupoids. 


In ([Kasparov 88](#Kasparov88)) the refinement of the [[analytic assembly map]] to [[equivariant cohomology|equivariant]] [[KK-theory]] is given, and called the _descent map_. This is of the form (recalled as [Blackadar, theorem 20.6.2](#Blackadar))

$$
  KK^G(A,B) \to KK(G \ltimes A, G \ltimes B)
$$

where on the left we have $G$-[[equivariant KK-theory]] and on the right ordinary [[KK-theory]] of [[crossed product C*-algebras]] (which by the discussion there are models for the [[groupoid convolution algebras]] of $G$-[[action groupoids]]).

This is an [[isomorphism]] at least for $G$ a [[compact topological group]] and restricted to [[operator K-theory]] (hence to the first argument being $\mathbb{C}$) and for $G$ a [[discrete group]] and restricted to [[K-homology]] (hence ot the second argument being $\mathbb{C}$). In this form this is the **Green-Julg theorem**, see [below](#GreenJulgTheorem).



## Theorems
 {#Theorems}

### Green-Rosenberg-Julg theorem

The Green-Rosenberg-Julg theorem identifies [[equivariant K-theory]] with the [[operator K-theory]] of [[crossed product algebras]].

+-- {: .num_theorem #GreenJulgTheorem}
###### Theorem
**(Green-Julg theorem)**

Let $G$ be a [[topological group]] acting on a [[C*-algebra]] $A$.

1. If $G$ is a [[compact topological group]] then the descent map

   $$
     KK^G(\mathbb{C}, A) \to KK(\mathbb{C},G\ltimes A) 
   $$

   is an [[isomorphism]], identifying the [[equivariant operator K-theory]] of $A$ with the ordinary [[operator K-theory]] of the [[crossed product C*-algebra]] $G \ltimes A$.

1. if $G$ is a [[discrete group]] then the descent map

   $$
     KK^G(A, \mathbb{C}) \to KK(G \ltimes A, \mathbb{C})
   $$

   is an [[isomorphism]], identifying the equivariant [[K-homology]] of $A$ with the ordinary [[K-homology]] of the [[crossed product C*-algebra]] $G \ltimes A$.

=--

This goes back to ([Green 82](#Green82)), ([Julg 81](#Julg81)). A [[KK-theory]]-proof is in ([Echterhoff, theorem 0.2](#Echterhoff)); a textbook account is in ([Blackadar, 11.7, 20.2.7](#Blackadar)). See also around ([Land 13, prop. 41](#Land13)).

## Related theorems

* [[Atiyah-Segal completion theorem]], [[Green-Julg theorem]]

* [[delocalized equivariant cohomology]]

[[!include Segal completion -- table]]

## References

### Introductions and surveys

Introductions and surveys include

* [[Alain Valette]], _Introduction to the Baum-Connes conjecture_  ([pdf](http://www.univ-orleans.fr/mapmo/membres/chatterji/Valette.pdf))

* [[Nigel Higson]], _The Baum-Connes conjecture_ ([pdf](http://media.cit.utexas.edu/math-grasp/Higson_supplemental_1.pdf))

* [[Paul Baum]], _The Baum-Connes conjecture, localisation of categories and quantum groups_, 2008 ([pdf](http://www.mimuw.edu.pl/~pwit/TOK/sem8/files/Baum_bcclcqg.pdf))

Textbook discussion:

* {#Blackadar} [[Bruce Blackadar]], Section 11.7 and  20.2.7 of: _[[K-Theory for Operator Algebras]]_,   Cambridge University Press 1986, second ed. 1999 ([doi:10.1007/978-1-4613-9572-0](https://link.springer.com/book/10.1007/978-1-4613-9572-0), [pdf](http://wolfweb.unr.edu/homepage/bruceb/Book6.pdf))

* {#MislinValette03} [[Guido Mislin]], [[Alain Valette]], _Proper Group Actions and the Baum-Connes Conjecture_, Advanced Courses in Mathematics CRM Barcelona, Springer 2003 ([doi:10.1007/978-3-0348-8089-3](https://link.springer.com/book/10.1007/978-3-0348-8089-3))



See also

* Wikipedia, _[Baum-Connes conjecture](http://en.wikipedia.org/wiki/Baum%E2%80%93Connes_conjecture)_


### Original articles

The original article is 

* [[Paul Baum]], [[Alain Connes]], _K-theory for Lie groups and foliations_, Enseign. Math. 46 (2000), 3&#8211;42.
 {#BaumConnes00}

Proof of the conjecture for hyperbolic groups is in 

* [[Vincent Lafforgue]], _La conjecture de Baum-Connes &#224; coefficients pour les groupes hyperboliques_, Journal of Noncommutative Geometry, Volume 6, Issue 1, 2012, pages 1-197 ([arXiv:1201.4653](http://arxiv.org/abs/1201.4653))

Technical subtleties are discussed in 

* [[Nigel Higson]], [[Vincent Lafforgue]], [[Georges Skandalis]], _Counterexamples to the Baum-Connes conhecture_ ([pdf](http://www.personal.psu.edu/ndh2/math/Papers_files/Higson,%20Lafforgue,%20Skandalis%20-%202002%20-%20Counterexamples%20to%20the%20Baum-Connes%20conjecture.pdf))


The generalization to [[Lie groupoids]] is due to 

* [[Jean-Louis Tu]], _The Baum-Connes conjecture for groupoids_, 1999 ([[JLTBaumConnesForGroupoids.pdf:file]])
 {#Tu99}


Proofs for some cases are in 

* [[Georges Skandalis]], [[Jean-Louis Tu]], G. Yu, _The coarse Baum-Connes conjecture and groupoids_ ([pdf](http://www.math.univ-metz.fr/~tu/publi/coarse.pdf))


[[KK-theory]] tools and the descent map are introduced in

* [[Gennady Kasparov]], _Equivariant KK-theory and the Novikov conjecture_, Inventiones Mathematicae, vol. 91, p.147, 1988([web](http://adsabs.harvard.edu/abs/1988InMat..91..147K)) 
 {#Kasparov88}

The "Green-Julg theorem" for commutative algebra and finite group is due to [[Michael Atiyah]], for commutative algebra and general group due to 

* P. Green, _Equivariant if-theory and crossed product C*- algebras_, pp.  337-338 in Operator algebras and applications (Kingston, Ont., 1980), vol. 1, edited 
by R. V. Kadison, Proc. Sympos. Pure Math. 38, Amer. Math. Soc, Providence, 1982. 
{#Green82}

and the general case is due to an unpublished result by Green and [[Jonathan Rosenberg]] and independently due to 

* P. Julg, _K-theorie equivariante et produits croises_, C. R. Acad. Sci.  Paris Ser. I Math. 292:13 1981, 629-632. 
 {#Julg81}

Further discussion is in

* Siegfried Echterhoff, _The Green-Julg theorem_ [pdf](http://wwwmath.uni-muenster.de/u/paravici/Focused-Semester/lecturenotes/green-julg-Echterhoff.pdf)
 {#Echterhoff}

* Walther Paravicini, _A generalised Green-Julg theorem for proper groupoids and Banach algebras_, ([arXiv:0902.4365](http://arxiv.org/abs/0902.4365))

* V. Lafforgue, [pdf](http://www.mmas.univ-metz.fr/~gnc/bibliographie/HarmonicAnalysis/LafforgueICM.pdf)

A modification of the Baum-Connes conjecture with coefficient where many counterexamples (to the  conjecture with coefficients) are eliminated is in

* [[Paul Baum]], Erik Guentner, Rufus Willett, _Expanders, exact crossed products, and the Baum-Connes conjecture_, [arxiv/1311.2343](http://arxiv.org/abs/1311.2343)

Discussion in terms of [[localization]]/[[homotopy theory]] is in 

* [[Ralf Meyer]], [[Ryszard Nest]], _The Baum-Connes conjecture via localisation of categories, Topology 45 (2006), no. 2, 209&#8211;259.


[[!redirects Green-Julg theorem]]
