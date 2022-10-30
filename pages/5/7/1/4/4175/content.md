
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

## Examples

* If $H$ is a [[bimonoid]] in a monoidal category, then the monad $T_H X =H\otimes X$ (whose algebras are $H$-[[modules]]) is opmonoidal, with constraints induced by the comultiplication and counit of $H$.  If $H$ is moreover a [[Hopf monoid]], then $T_H$ is a (Brugui&#232;res-Lack-Virelizier) Hopf monad.

## Properties

If $T$ is a (Brugui&#232;res-Lack-Virelizier) Hopf monad on a [[closed monoidal category]], then its category of algebras is also closed and the monadic forgetful functor preserves internal-homs.

## Related concepts

* [[Hopf algebra]]

* [[Hopf monoid]]

* [[Hopf monoidal category]]


## References

* wikipedia [opmonoidal monad](http://en.wikipedia.org/wiki/Monoidal_monad)

* [[Kornél Szlachányi]], _The monoidal Eilenberg&#8211;Moore construction and bialgebroids_, J. Pure Appl. Algebra __182__, no. 2&#8211;3 (2003) 287&#8211;315

* R. Wisbauer, _Bimonads and Hopf monads on categories_, [pdf](http://www.math.uni-duesseldorf.de/~wisbauer/Hopfmonad.pdf)
* Bachuki Mesablishvili, [[Robert Wisbauer]], _Notes on bimonads and Hopf monads_, Theory Appl. Cat. __26__:10, 2012, 281-303,  [abs](http://www.tac.mta.ca/tac/volumes/26/10/26-10abs.html) [pdf](http://www.tac.mta.ca/tac/volumes/26/10/26-10.pdf) [arxiv/1010.3628](http://arxiv.org/abs/1010.3628)
* D. Chikladze, S. Lack, [[R. Street]], _Hopf monoidal comonads_, Theorya and Appl. of Cat. __24__ (2010) No. 19, 554-563.[tac](http://www.tac.mta.ca/tac/volumes/24/19/24-19abs.html)

* A. Brugui&#232;res, _Hopf monads_, [math.QA/0604180](http://arxiv.org/abs/math/0604180); _Hopf monads: an introduction_, an expos&#232;, [pdf](http://www.cirm.univ-mrs.fr/videos/2006/exposes/23/Bruguieres.pdf); _Hopf monads, tensor categories and quantum invariants_, an expos&#232;, [pdf](http://www.cirm.univ-mrs.fr/videos/2008/exposes/307/Bruguiere.pdf)
 {#Bruguieres}


* Alain Brugui&#232;res, [[Steve Lack]], Alexis Virelizier, _Hopf monads on monoidal categories_, [arxiv/1003.1920](http://arxiv.org/abs/1003.1920)
* A. Brugui&#232;res, A. Virelizier, _The double of a Hopf monad_, Adv. Math. __227__ No. 2, June 2011, pp 745--800, [arxiv/0812.2443](http://arxiv.org/abs/0812.2443)
* Group = Hopf algebra, blog discussion, [sbseminar](http://sbseminar.wordpress.com/2007/10/07/group-hopf-algebra)
* Marek Zawadowski, _The formal theory of monoidal monads_, [arxiv/1012.0547](http://arxiv.org/abs/1012.0547)
* M. Zawadowski, _coMalcev monads_, slides from a talk, [pdf](http://duch.mimuw.edu.pl/~zawado/Talks/coMalcev_talk.pdf)
* [[Ieke Moerdijk]], _Monads on tensor categories_, J. Pure. Appl. Alg. __168__, 2-3, (2002), 189-208, <a href="http://dx.doi.org/10.1016/S0022-4049(01)00096-2">doi</a> 
* [[Gabriella Böhm]], [[Stephen Lack]], [[Ross Street]], _Weak bimonads and weak Hopf monads_, J. Alg. __328__, n. 1, Feb 2011, 1-30, [doi](http://dx.doi.org/10.1016/j.jalgebra.2010.07.032), [arxiv/1002.4493](http://arxiv.org/abs/1002.4493)
[[G. Böhm]], _Weak bimonads and weak Hopf monads_, conference slides, 2010, [pdf](http://www.ual.es/congresos/hopf2010/charlas/bohm.pdf)
* S. Willerton, _A diagrammatic approach to Hopf monads_, [arxiv/0807.0658](http://arxiv.org/abs/0807.0658)
* K. Dosen, Z. Petric, _Coherence for monoidal monads and comonads_, [arxiv/0907.2199](http://arxiv.org/abs/0907.2199) 
* [[Anders Kock]], _Strong functors and monoidal monads_, [pdf](http://home.imf.au.dk/kock/SFMM.pdf), Archiv der Math. __23__: 113&#8211;120, (1972) [doi](http://dx.doi.org/10.1007%2FBF01304852); _Monads on symmetric monoidal categories_, [pdf](http://home.imf.au.dk/kock/MSMCC.pdf)
* B. J. Day, _Note on monoidal monads_, J. Austral. Math. Soc. A __23__, 292-311 (1977) [pdf](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=4897004)
* Alain Brugui&#232;res, Sonia Natale, _Exact sequences of tensor categories_, [arXiv:math.QA/1006.0569](http://arxiv.org/abs/1006.0569) (generalizes Schneider's work on [[exact sequences of Hopf algebras]]; uses Hopf monads)

[[!redirects Hopf monads]]
[[!redirects bimonad]]
[[!redirects opmonoidal monad]]