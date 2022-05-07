

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

__Homotopy totalizations__ are a special case of [[homotopy limits]],
when the indexing diagram is $\Delta$,
the [[category of simplices]].

Homotopy totalizations can be defined in any [[relative category]],
just like [[homotopy limits]],
but practical computations are typically carried out
in presence of additional structures such as [[model structures]],
in fact, [[enriched model categories]] are the most common setup.

## Computation

In any $V$-[[enriched model category]], the homotopy totalization
of a [[cosimplicial object]]
$$X\colon \Delta\to C$$
can be computed in three different ways,
all of which use the notion of [[enriched end]] of [[enriched functors]] (i.e., [[weighted limits]]).

Specifically, consider the [[functor]]
$$Hom\colon (V^\Delta)^{op} \times C^\Delta \to C$$
that takes the [[enriched end]] of [[functors]], i.e., the [[weighted limit]],
where $V$ is the [[monoidal model category]] over which $C$ is enriched.

If we set the first argument to the [[constant functor]]
with value $1$ (the [[monoidal unit]] of $V$),
then the resulting functor is the [[limit functor]] $C^\Delta\to C$.

The functor $Hom$ becomes a [[right Quillen bifunctor]]
if we equip $V^\Delta$ and $C^\Delta$ with one
of the three following pairs of model structures:

* injective and injective;
* projective and projective;
* Reedy and Reedy.

Accordingly, the homotopy totalization of a [[cosimplicial object]] $X\colon \Delta\to C$ can be computed as follows.

* Cofibrantly resolve the constant weight $1$ in one of the three model structures listed above.
* Fibrantly resolve $X$ in the other model structure in the same pair.
* Compute $Hom(Q 1, R X)$, which is the homotopy totalization of $X$.

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
(with the injectivity condition dropped) is a [[homotopy initial functor]],
i.e., restricting along this inclusion preserves [[homotopy limits]].

Thus, homotopy totalizations can be computed as
[[homotopy limits]] over the [[category of semisimplices]].
The latter category is a [[direct category]],
which makes cofibrancy conditions particularly easy.

## Examples

### Simplicial sets

A Reedy [[cofibrant replacement]] of the constant weight $1\colon \Delta\to sSet$
can be computed as the [[Yoneda embedding]] $Y_\Delta\colon\Delta\to sSet$.

Thus, the homotopy totalization of
$$X\colon \Delta \to sSet$$
can be computed as
$$Hom(Y_\Delta, R X),$$
where $R X$ is the Reedy [[fibrant replacement]] of $X$.

### Chain complexes of abelian groups

For [[chain complexes]] with [[quasi-isomorphisms]]
(which we equip with the [[projective model structure on chain complexes]]),
a computation analogous to the one for simplicial sets above
Reedy cofibrantly resolves the constant weight as
$$\mathrm{N} \mathbf{Z} [-]\colon \Delta \to Ch,$$
where $\mathrm{N}$ denotes the [[normalized chains functor]]
and $\mathbf{Z}[-]$ denotes the [[free simplicial abelian group functor]].

All [[cosimplicial objects]] in [[chain complexes]] are Reedy fibrant
because the [[matching map]] is a degreewise surjection of [[chain complexes]].

Thus, the homotopy totalization of $X\colon \Delta \to Ch$
can be computed as
$$Hom(\mathrm{N} \mathbf{Z} [-], X),$$
which is isomorphic to the [[direct product]] [[total complex]]
of the [[double chain complex]]
obtained by applying the [[Dold–Kan correspondence]]
to the [[cosimplicial object]] $X\colon \Delta\to Ch$.

### Topological spaces

Consider [[topological spaces]] with [[weak homotopy equivalences]].
Below, we use the [[Serre model structure]].

The [[topological simplex]] $\mathbf{\Delta}\colon \Delta\to Top$ is Reedy cofibrant as
a [[cosimplicial topological space]].

Not all [[cosimplicial objects]] in [[topological spaces]] are Reedy [[fibrant]],
since the [[matching map]] need not be a [[Serre fibration of topological spaces]].

However, we can pass to the [[semisimplicial]] setting, as explained above.
In this, case Reedy fibrancy boils down to the objectwise fibrancy,
which is always true for [[topological spaces]].

Thus, the homotopy totalization of $X\colon \Delta \to Top$
can be computed as
$$Hom(\mathbf{\Delta}, X)$$
in the category of functors $\Delta_{inj}\to Top$.
This can be seen as the totalization analog of the [[fat geometric realization]].
One could call it the __fat geometric totalization__.

## Related notions

* [[totalization]]

* [[homotopy limit]]

* [[homotopy end]]

* [[homotopy pullback]]

* [[homotopy product]]

* [[homotopy equalizer]]

* [[homotopy realization]]

[[!redirects homotopy totalizations]]