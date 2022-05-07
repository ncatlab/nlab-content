

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
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

__Homotopy realization__ are a special case of [[homotopy colimits]],
when the indexing diagram is $\Delta^{op}$,
the [[opposite category]] of the [[category of simplices]].

Homotopy coequalizers can be defined in any [[relative category]],
just like [[homotopy colimits]],
but practical computations are typically carried out
in presence of additional structures such as [[model structures]],
in fact, [[enriched model categories]] are the most common setup.

## Computation

In any $V$-[[enriched model category]], the homotopy realization
of a [[simplicial object]]
$$X\colon \Delta^{op}\to C$$
can be computed in three different ways,
all of which use the notion of [[tensor product of functors]] (i.e., [[weighted colimits]]).

Specifically, consider the [[functor]]
$$\otimes\colon V^\Delta \times C^{\Delta^{op}} \to C$$
that takes the [[tensor product of functors]], i.e., the [[weighted colimit]],
where $V$ is the [[monoidal model category]] over which $C$ is enriched.

If we set the first argument to the [[constant functor]]
with value $1$ (the [[monoidal unit]] of $V$),
then the resulting functor is the [[colimit functor]] $C^{\Delta^{op}}\to C$.

The functor $\otimes$ becomes a [[left Quillen bifunctor]]
if we equip $V^\Delta$ and $C^{\Delta^{op}}$ with one
of the three following pairs of model structures:
* injective and projective;
* projective and injective;
* Reedy and Reedy.

Accordingly, the homotopy realization of a [[simplicial object]] $X\colon \Delta^{op}\to C$ can be computed as follows.
* Cofibrantly resolve the constant weight $1$ in one of the three model structures listed above.
* Cofibrantly resolve $X$ in the other model structure in the same pair.
* Compute $Q 1 \otimes Q X$, which is the homotopy realization of $X$.

Cofibrant resolutions in the [[injective model structure]]
can be computed by appling some [[cofibrant resolution functor]] of $C$ objectwise.

Cofibrant resolutions in the [[Reedy model structure]]
can be computed inductively, by repeatedly factoring the [[latching map]] of $X$
as a [[cofibration]] followed by a [[weak equivalence]]
and adjusting $X$ accordingly.

Cofibrant resolutions in the [[projective model structure]]
can be computed explicitly in some practical examples.

### Reduction to semisimplicial objects

The inclusion of the
[[category of semisimplices]] (i.e., fininite inhabited totally ordered sets and injective order-preserving maps) into the [[category of simplices]]
(with the injectivity condition dropped) is a [[homotopy final functor]],
i.e., restricting along this inclusion preserves [[homotopy colimits]].

Thus, homotopy realizations can be computed as
[[homotopy colimits]] over the [[category of semisimplices]].
The latter category is a [[direct category]],
which makes cofibrancy conditions particularly easy.

## Examples

### Simplicial sets

In [[simplicial sets]] with [[simplicial weak equivalences]],
the [[Reedy model structure]] on [[simplicial objects]] in [[simplicial sets]]
coincides with the [[injective model structure]],
as explained in the article [[elegant Reedy category]].
In particular, all objects are [[cofibrant]].

A Reedy [[cofibrant replacement]] of the constant weight $1\colon \Delta\to sSet$
can be computed as the [[Yoneda embedding]] $Y\colon\Delta\to sSet$.

Thus, the homotopy coequalizer of
$$X\colon \Delta^{op} \to sSet$$
can be computed as
$$Y\otimes X,$$
which is isomorphic to the [[diagonal]] of $X$.

### Chain complexes of abelian groups

For [[chain complexes]] with [[quasi-isomorphisms]]
(which we equip with the [[injective model structure on chain complexes]]),
a computation analogous to the one for simplicial sets above
Reedy cofibrantly resolves the constant weight as
$$\mathrm{N} \mathbf{Z} [-]\colon \Delta \to Ch,$$
where $\mathrm{N}$ denotes the [[normalized chains functor]]
and $\mathbf{Z}[-]$ denotes the [[free simplicial abelian group functor]].

Once again, all [[simplicial objects]] in [[chain complexes]] are Reedy cofibrant.

Thus, the homotopy realization of $X\colon \Delta^{op} \to Ch$
can be computed as
$$\mathrm{N} \mathbf{Z} [-] \otimes X,$$
which is isomorphic to the [[coproduct totalization]]
of the [[double chain complex]]
obtained by applying the [[Dold–Kan correspondence]]
to the [[simplicial object]] $X\colon \Delta^{op}\to Ch$.

### Topological spaces

Consider [[topological spaces]] with [[weak homotopy equivalences]].
Below, we use the [[Serre model structure]].

The [[topological simplex]] $\mathbf{\Delta}\colon \Delta\to Top$ is Reedy cofibrant as
a [[cosimplicial topological space]].

Not all [[simplicial objects]] in [[topological spaces]] are Reedy [[cofibrant]],
since the [[latching map]] need not be a [[cofibration of topological spaces]],
i.e., a [[retract]] of a relative cellular map.

However, we can pass to the semisimplicial setting, as explained above.
In this, case Reedy cofibrancy boils down to the objectwise cofibrancy.

Thus, the homotopy realization of $X\colon \Delta^{op} \to Top$
can be computed as
$$\mathbf{\Delta}\otimes Q X,$$
where $Q$ denotes objectwise [[cofibrant replacement]].
This is precisely the classical [[fat geometric realization]]
of [[simplicial topological spaces]].


## Related notions

* [[coproduct]]

* [[homotopy colimit]]

* [[homotopy pushout]]

* [[homotopy coproduct]]

* [[homotopy coequalizer]]

* [[homotopy totalization]]

[[!redirects homotopy realizations]]