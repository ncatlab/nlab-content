[[!redirects topos of algebras over a monad]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

If a [[monad]] or [[comonad]] $T$ on a [[topos]] $\mathcal{E}$ is sufficiently well behaved, then the [[Eilenberg-Moore category|category of (co)algebras]] $T Alg(C)$ over the (co)monad is itself an ([[elementary topos|elementary]]) topos.

## Properties

### General

+-- {: .num_prop #ToposProperty}
###### Proposition

Let $\mathcal{E}$ be a [[topos]]. Then

* if a [[comonad]] $T : \mathcal{E} \to \mathcal{E}$ is [[exact functor|left exact]], then the [[Eilenberg-Moore category|category of coalgebras]] $T CoAlg(\mathcal{E})$ is itself an ([[elementary topos|elementary]]) topos.

  Moreover, 

  * the [[free functor|cofree/forgetful adjunction]]

    $$
      (U \dashv F)
      : 
      \mathcal{E} \stackrel{\overset{U}{\leftarrow}}{\underset{F}{\to}}  T CoAlg(\mathcal{E})
    $$

    is a [[geometric morphism]].

  * If $T$ is furthermore [[accessible monad|accessible]] and $\mathcal{E}$ is a [[sheaf topos]], then also $T CoAlg(\mathcal{C})$ is a sheaf topos. 

  * Even if $T$ is merely [[pullback]]-preserving, the category of coalgebras is a topos. 

* Therefore, if a [[monad]] $T : \mathcal{E} \to \mathcal{E}$ has a [[right adjoint]], then the [[Eilenberg-Moore category|category of algebras]] $T Alg(\mathcal{E})$ is itself an ([[elementary topos|elementary]]) topos. (Because the right adjoint of a monad carries a comonad structure, evidently a left exact comonad, and there is a canonical equivalence between the category of algebras over the monad and the category of coalgebras over the comonad.) 

* If a monad on a topos is pullback-preserving and [[idempotent monad|idempotent]], then the category of algebras is a subtopos (hence the category of sheaves for some [[Lawvere-Tierney topology]]). 

=--

The result for left exact comonads appears for instance as ([MacLaneMoerdijk, V 8. theorem 4](#MacLaneMoerdijk)); the result for monads possessing a right adjoint appears in _op. cit._ as corollary 7. The statement on pullback-preserving comonads is given in The [[Elephant]], A.4.2.3. For [[(∞,1)-toposes]] see [this MO discussion](http://mathoverflow.net/a/206695/381).


### Image factorization of toposes

+-- {: .num_prop}
###### Proposition

The [[geometric morphism]]s of the form $ p = (U \dashv F) : \mathcal{E} \to T CoAlg(\mathcal{E})$ from prop. \ref{ToposProperty} are precisely, up to [[equivalence of categories|equivalence]], the [[geometric surjection]]s.
 
=--

This appears as ([MacLaneMoerdijk, VII 4. prop. 4](#MacLaneMoerdijk)).

This way the [[geometric surjection/embedding factorization]] in [[Topos]] is constructed. See there for more.

## Examples

+-- {: .num_remark}
###### Observation

For $(f^* \dashv f_*) : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} \mathcal{F}$ any [[geometric morphism]], the induced [[comonad]]

$$
  f^* f_* : \mathcal{E} \to \mathcal{E}
$$

is evidently left exact, hence $(f^* f_*) CoAlg(\mathcal{E})$ is a topos of coalgebras.

=--

+-- {: .num_remark}
###### Observation 
The so-called "[[over-topos|fundamental theorem of topos theory]]", that an [[overcategory]] of a topos is a topos, is a corollary of the result that the category of coalgebras of a pullback-preserving comonad on a topos is a topos (the slice $\mathcal{E}/X$ being the category of coalgebras of the comonad $X \times - \colon \mathcal{E} \to \mathcal{E}$). 
=-- 


## Related concepts

* Also a category of [[algebra over an algebraic theory|algebras over]] a *commutative* [[finitary algebraic theory]] in [[Set]] has properties very close to the properties of a Grothendieck topos, in fact only one axiom has to be modified. This is one of the themes of the theory of [[vectoid]]s of [[Nikolai Durov]].


## References

Section V 8. of

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 


[[!redirects topos of coalgebras over a comonad]]

[[!redirects toposes of algebras over a monad]]
[[!redirects toposes of coalgebras over a comonad]]

[[!redirects topoi of algebras over a monad]]
[[!redirects topoi of coalgebras over a comonad]]

[[!redirects topos of coalgebras]]