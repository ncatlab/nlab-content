
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One can consider various compatibilities between a ([[comonad|co]])[[monad]] on a [[monoidal category]] and the underlying monoidal product; they are variants of the idea of a [[distributive law]]. Similarly, one can look at a compatibility between an action of a monoidal category and a (co)monad on the same category. A _Hopf monad_ satisfies conditions analogous to that of a _[[Hopf monoid]]_ ([Brugui&#232;res 06](#Bruguieres)).

## Definitions

Warning: more than one notion comes up with the names of [[bimonad]] and Hopf monad; there are also related notions of monoidal monad and opmonoidal monad as well of a [[strong monad]].

### Monoidal monads...

A __monoidal monad__ on a monoidal category is a [[monad]] whose underlying [[endofunctor]] is a [[lax monoidal functor]] and such that the unit and multiplication are monoidal natural transformations. Consequently, the [[Kleisli category]] of a monoidal monad has a canonical monoidal structure such that the [[forgetful functor]] is strict monoidal. 

(...)

### Opmonoidal monads with invertible fusion

An **opmonoidal monad** on a monoidal category is a [[monad]] whose underlying [[endofunctor]] is a [[colax monoidal functor]], and such that the unit and multiplication are monoidal natural transformations.  An opmonoidal monad is also called a **bimonad**.

For an opmonoidal monad $T$, one can define the **left fusion operator** to be the natural transformation
$$ T(X\otimes T Y) \to T X \otimes T^2 Y \to T X \otimes T Y $$
of the opmonoidal constraint of $T$ and its monad multiplication.  Similarly, we have the **right fusion operator**
$$ T(T X\otimes Y) \to T^2 X \otimes T Y \to T X \otimes T Y $$
The fusion operators satisfy certain axioms.  In fact, an opmonoidal monad structure on $T$ is uniquely determined by a fusion operator (of either sort) along with the monad unit $Id\to T$ and the opmonoidal unit constraint $T I \to I$, satisfying appropriate axioms.

An opmonoidal monad is called a **Hopf monad** if both of its fusion operators are invertible.  More generally we have *left* and *right* Hopf monads where only one fusion operator is invertible.  This definition is in Brugui&#232;res-Lack-Virelizier.

### Distributing monad and comonad structures

Alternatively, one might be tempted to define a Hopf monad to be a [[Hopf monoid]] in the monoidal category of endofunctors, but that monoidal category is not [[symmetric monoidal category|symmetric]] or even [[braided monoidal category|braided]] or [[duoidal category|duoidal]], so this doesn't make sense.  However, we can instead ask for a "local" braiding in the form of a mixed [[distributive law]].

Thus, we might define a **bimonad** to be an endofunctor $H$ equipped with the structure of both a monad and a comonad, along with a [[distributive law]] $\lambda: H H \to H H$ satisfying suitable axioms analogous to those of a bimonoid.  A bimonad in this sense is a **Hopf monad** if it has an antipode $s:H\to H$ making the same diagrams commute as for a [[Hopf monoid]].  This definition is in Mesablishvili-Wisbauer.

## Examples

* If $H$ is a [[bimonoid]] in a [[braided monoidal category]], then the monad $T_H X =H\otimes X$ (whose algebras are $H$-[[modules]]) is opmonoidal, with constraints induced by the comultiplication and counit of $H$.  If $H$ is moreover a [[Hopf monoid]], then $T_H$ is a (Brugui&#232;res-Lack-Virelizier) Hopf monad.

* In fact, if $H$ is a bimonoid as before, then $T_H$ is *also* a bimonad in the sense of Mesablishvili-Wisbauer, with monad and comonad structures induced by the monoid and comonoid structures of $H$.  Moreover, if $H$ is a Hopf monoid, then $T_H$ is a Hopf monad in their sense as well.

## Properties

If $T$ is a (Brugui&#232;res-Lack-Virelizier) Hopf monad on a [[closed monoidal category]], then its category of algebras is also closed and the monadic forgetful functor preserves internal-homs.

## Related concepts

* [[Hopf adjunction]]

* [[Hopf algebra]]

* [[Hopf monoid]]

* [[Hopf monoidal category]]

* [[Frobenius monad]]


## References

* [[Alain Bruguières]], [[Alexis Virelizier]], *Hopf monads*, Advances in Mathematics **215** 2 (2007) 679-733 &lbrack;[doi:10.1016/j.aim.2007.04.011](https://doi.org/10.1016/j.aim.2007.04.011), [arXiv:math/0604180](https://arxiv.org/abs/math/0604180)&rbrack;

* Masahito Hasegawa and Jean-Simon Pacaud Lemay, *Hopf Monads on Biproducts*, Theory and Applications of Categories **39** 28 (2023) 804-823 &lbrack;[tac:3928](http://www.tac.mta.ca/tac/volumes/39/28/39-28abs.html)&rbrack;

Monograph:

* [[Gabriella Böhm]], _Hopf algebras and their generalizations from a category theoretical point of view_, Lecture Notes in Math. __2226__, Springer 2018, [doi](https://link.springer.com/book/10.1007/978-3-319-98137-6)

See also:

* Wikipedia. *[Opmonoidal monad](http://en.wikipedia.org/wiki/Monoidal_monad)*


* [[Kornél Szlachányi]], _The monoidal Eilenberg-Moore construction and bialgebroids_, J. Pure Appl. Algebra __182__, no. 2&#8211;3 (2003) 287&#8211;315

* R. Wisbauer, _Bimonads and Hopf monads on categories_, [pdf](http://www.math.uni-duesseldorf.de/~wisbauer/Hopfmonad.pdf)

* Bachuki Mesablishvili, [[Robert Wisbauer]], _Notes on bimonads and Hopf monads_, Theory Appl. Cat. __26__:10, 2012, 281-303,  [abs](http://www.tac.mta.ca/tac/volumes/26/10/26-10abs.html) [pdf](http://www.tac.mta.ca/tac/volumes/26/10/26-10.pdf) [arxiv/1010.3628](http://arxiv.org/abs/1010.3628)

* D. Chikhladze, S. Lack, [[R. Street]], _Hopf monoidal comonads_, Theory and Appl. of Cat. __24__ (2010) No. 19, 554-563.[tac](http://www.tac.mta.ca/tac/volumes/24/19/24-19abs.html)

* {#Bruguieres} A. Brugui&#232;res, _Hopf monads_, [math.QA/0604180](http://arxiv.org/abs/math/0604180); 

  * _Hopf monads: an introduction_, an expos&#232;, [pdf](http://www.cirm.univ-mrs.fr/videos/2006/exposes/23/Bruguieres.pdf); 

  * _Hopf monads, tensor categories and quantum invariants_, an expos&#232;, [pdf](http://www.cirm.univ-mrs.fr/videos/2008/exposes/307/Bruguiere.pdf); 

  * _Galois-Grothendieck duality, Tannaka duality and Hopf (co)monads_. talk at workshop "Hopf algebras and tensor categories", University of Almer&#237;a, July 4-8, 2011, [pdf](http://www.ual.es/Congresos/hopf2010/charlas/bruguiertalk.pdf)
 


* Group = Hopf algebra, blog discussion, [sbseminar](http://sbseminar.wordpress.com/2007/10/07/group-hopf-algebra)
* Marek Zawadowski, _The formal theory of monoidal monads_, [arxiv/1012.0547](http://arxiv.org/abs/1012.0547)
* M. Zawadowski, _coMalcev monads_, slides from a talk, [pdf](http://duch.mimuw.edu.pl/~zawado/Talks/coMalcev_talk.pdf)
* [[Ieke Moerdijk]], _Monads on tensor categories_, J. Pure. Appl. Alg. __168__, 2-3, (2002), 189-208, <a href="http://dx.doi.org/10.1016/S0022-4049(01)00096-2">doi</a> 
* [[Gabriella Böhm]], [[Stephen Lack]], [[Ross Street]], _Weak bimonads and weak Hopf monads_, J. Alg. __328__, n. 1, Feb 2011, 1-30, [doi](http://dx.doi.org/10.1016/j.jalgebra.2010.07.032), [arxiv/1002.4493](http://arxiv.org/abs/1002.4493)
[[G. Böhm]], _Weak bimonads and weak Hopf monads_, conference slides, 2010, [pdf](http://www.ual.es/congresos/hopf2010/charlas/bohm.pdf)

* [[Simon Willerton]], _A diagrammatic approach to Hopf monads_, [arxiv/0807.0658](http://arxiv.org/abs/0807.0658)

* K. Dosen, Z. Petric, _Coherence for monoidal monads and comonads_, [arxiv/0907.2199](http://arxiv.org/abs/0907.2199) 
* [[Anders Kock]], _Strong functors and monoidal monads_, [pdf](http://home.imf.au.dk/kock/SFMM.pdf), Archiv der Math. __23__: 113&#8211;120, (1972) [doi](http://dx.doi.org/10.1007%2FBF01304852); _Monads on symmetric monoidal categories_, [pdf](http://home.imf.au.dk/kock/MSMCC.pdf)
* B. J. Day, _Note on monoidal monads_, J. Austral. Math. Soc. A __23__, 292-311 (1977) [pdf](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=4897004)
* Alain Brugui&#232;res, Sonia Natale, _Exact sequences of tensor categories_, [arXiv:math.QA/1006.0569](http://arxiv.org/abs/1006.0569) (generalizes Schneider's work on [[exact sequences of Hopf algebras]]; uses Hopf monads)

[[weak bimonad|Weak bimonad]] version

* [[Gabriella Böhm]], [[Stephen Lack]], [[Ross Street]], _Weak bimonads and weak Hopf monads_, J. Algebra 328 (2011), 1-30, [arXiv:1002.4493](http://arxiv.org/abs/1002.4493)

[[!redirects Hopf monads]]
[[!redirects bimonad]]
[[!redirects bimonads]]
[[!redirects opmonoidal monad]]
[[!redirects opmonoidal monads]]