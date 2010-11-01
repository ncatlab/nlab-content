# Ternary factorisation systems
* table of contents
{: toc}

## Idea

Just as an (orthogonal/unique) [[orthogonal factorization system|factorization system]] $(E,M)$ on a [[category]] $C$ gives a way to factor every [[morphism]] of $C$ as an $E$-map followed by an $M$-map, a *ternary (orthogonal) factorization system* $(E,F,M)$ gives a way to factor every map of $C$ as an $E$-map followed by an $F$-map followed by an $M$-map.

This is a special case of a notion of [[k-ary factorization system]].


## Definition

It turns out that a convenient way to state the definition is in terms of a pair of ordinary (orthogonal) factorization systems.  We define a **ternary factorization system** on $C$ to consist of a pair $(L_1,R_1)$ and $(L_2,R_2)$ of ordinary orthogonal factorization systems such that $L_1 \subseteq L_2$ (or equivalently $R_2 \subseteq R_1$).

The three classes of map $(E,F,M)$ are then defined by $E=L_1$, $F = L_2\cap R_1$, and $M=R_2$.  This is justified by:

+--{: .un_prop}
###### Proposition
Given a ternary factorization system as above, any morphism $f$ factors as 
$$ A \overset{L_1}{\to} im_2(f) \overset{L_2 \cap R_1}{\to} im_1(f) \overset{R_2}{\to} B $$
in an essentially unique way.
=--
+--{: .proof}
###### Proof
Consider the two ternary factorizations of $f$ obtained by

1. First factoring $f$ into an $L_1$-map followed by an $R_1$-map, then factoring the $R_1$-part into an $L_2$-map followed by an $R_2$-map; and
1. First factoring $f$ into an $L_2$-map followed by an $R_2$-map, then factoring the $L_2$-part into an $L_1$-map followed by an $R_1$-map.

Note that both start with an $L_1$ map and end with an $R_2$ map.  By a straightforward exercise in orthogonality, we can get comparison maps in both directions between these two factorizations which make them isomorphic.  Therefore, since the first produces a middle map which is in $L_2$ and the second produces a middle map which is in $R_1$, this middle map must in fact be in $L_2\cap R_1$.  Finally, any other such ternary factorization of $f$ induces an $(L_1,R_1)$ and $(L_2,R_2)$ factorization by composing pairwise, and uniqueness of these two implies uniqueness of the ternary factorization.
=--

Conversely, just as for a binary factorization system, the extra requirement of orthogonality can be deduced from uniqueness of the factorizations, a unique and *functorial* ternary factorization implies that it "splits" into a pair of binary factorization systems, i.e. a ternary factorization system as defined here.  This is remarked on [here](http://golem.ph.utexas.edu/category/2010/07/ternary_factorization_systems.html#c034162).

One can also characterize the notion in terms of a ternary factorization with a "ternary orthogonality" property; see the paper of Pultr and Tholen referenced below.


## The sixth class of maps

In addition to $L_1$, $R_1$, $L_2$, $R_2$, and $L_2\cap R_1$, a ternary factorization system also determines a sixth important class of morphisms, namely those whose $(L_2\cap R_1)$-part is an isomorphism, or equivalently those that can be factored as an $L_1$-map followed by an $R_2$-map.  We therefore call this class $R_2 L_1$.

+--{: .un_prop}
###### Proposition
In a ternary factorization system, $L_1 = L_2 \cap R_2L_1$ and $R_2 = R_1 \cap R_2L_1$.
=--
+--{: .proof}
###### Proof
In both cases $\subseteq$ is obvious.  Conversely, if $f \in L_2 \cap R_2 L_1$, say $f = m e$ for $m\in R_2$ and $e\in L_1$, then orthogonality in the square
$$\array{a & \overset{e}{\to} & c\\
  ^f \downarrow && \downarrow ^m\\
  b & \underset{id}{\to} & b}$$
exhibits $f$ as a retract of $e$ in $Arr(C)$, whence $f\in L_1$ since $L_1$ is closed under retracts.
=--


## Examples

* In [[Top]], let $L_1=$ quotient maps, $R_1=$ injective continuous maps, $L_2=$ surjective continuous functions, and $R_2=$ subspace embeddings.  Here $L_2\cap R_1=$ bijective continuous maps, and the two intermediate objects in the ternary factorization of a continuous map are obtained by imposing the coarsest and the finest compatible topologies on its set-theoretic image.

* More generally, if a category has both ([[epimorphism|epi]], [[strong monomorphism|strong mono]]) and ([[strong epimorphism|strong epi]], [[monomorphism|mono]]) factorizations, then since strong epis are epi, we have a ternary factorization.  Here $L_2\cap R_1$ is the class of monic epics, sometimes called [[bimorphisms]].  The maps in $R_2 L_1$ are sometimes called [[strict morphisms]].

* On [[Cat]] there is a 2-categorical version of a ternary factorization system, determined by the [[factorization system on a 2-category|2-categorical factorization systems]] ([[essentially surjective functor|eso]]+[[full functor|full]], [[faithful functor|faithful]]) and (eso, [[fully faithful functor|full and faithful]]).  Here $L_2\cap R_1$ is the class of eso+faithful functors, while $R_2 L_1$ is the class of full functors.  This factorization system plays an important role in the study of [[stuff, structure, property]].

* On [[Topos]] there is also a 2-categorical ternary factorization system composed of the binary 2-categorical factorization systems ([[hyperconnected geometric morphism|hyperconnected]], [[localic geometric morphism|localic]]) and ([[geometric surjection|surjection]], [[geometric embedding|inclusion]]). Here the maps in $L_2\cap R_1$ have no name other than "localic surjections," and those in $R_2 L_1$ have no established name (although they are briefly mentioned in A4.6.10 of the [[Elephant]]).

* Suppose that $C$ has a binary factorization system $(E,M)$ and that $p\colon A\to C$ is an [[ambifibration]] relative to $(E,M)$: i.e. every arrow in $E$ has an opcartesian lift and every arrow in $M$ has a [[cartesian morphism|cartesian]] lift.  (In particular, $p$ could be a [[bifibration]].)  Then there is a ternary factorization system on $A$ for which $L_1$ is the class of opcartesian arrows over $E$, $R_2$ is the class of cartesian arrows over $M$, and $L_2\cap R_1$ is the class of vertical arrows (those lying over identities).  See [this comment](http://golem.ph.utexas.edu/category/2010/07/ternary_factorization_systems.html#c034162).

  For instance, the above factorization system on $Top$ is induced in this way via the [[forgetful functor]] $Top\to Set$ from the (epi,mono) factorization system on [[Set]].


## Related concepts

* The notion of [[model category]] involves a pair of [[weak factorization systems]] called (acyclic cofibration, fibration) and (cofibration, acyclic fibration) which are compatible in the same sense as above.  However, non-uniqueness of these factorizations means that the resulting "ternary factorization" of a morphism is not unique.  The class corresponding to $R_2 L_1$ is important, however: it is precisely the class of [[weak equivalences]].

* The notion of [[k-ary factorization system]] is a generalization to factorizations into $k$ morphisms.

* Just as [[strict factorization system]]s can be identified with [[distributive laws]] in the [[bicategory]] of [[spans]], so "strict" ternary (and k-ary) factorization systems can be identified with [[iterated distributive law]]s in $Span$.


## References

* A. Pultr and W. Tholen, *Free Quillen Factorization Systems*.  Georgian Math. J.9 (2002), No. 4, 807-820

* [Cafe discussion](http://golem.ph.utexas.edu/category/2010/07/ternary_factorization_systems.html)


[[!redirects ternary factorization system]]
[[!redirects ternary factorization systems]]
[[!redirects ternary factorisation system]]
[[!redirects ternary factorisation systems]]
[[!redirects double factorization system]]
[[!redirects double factorization systems]]
[[!redirects double factorisation system]]
[[!redirects double factorisation systems]]
[[!redirects 3-way factorization system]]
[[!redirects 3-way factorization systems]]
[[!redirects 3-way factorisation system]]
[[!redirects 3-way factorisation systems]]
[[!redirects 3-step factorization system]]
[[!redirects 3-step factorization systems]]
[[!redirects 3-step factorisation system]]
[[!redirects 3-step factorisation systems]]
[[!redirects 3-stage factorization system]]
[[!redirects 3-stage factorization systems]]
[[!redirects 3-stage factorisation system]]
[[!redirects 3-stage factorisation systems]]
[[!redirects 3-fold factorization system]]
[[!redirects 3-fold factorization systems]]
[[!redirects 3-fold factorisation system]]
[[!redirects 3-fold factorisation systems]]

[[!redirects Quillen factorization system]]
[[!redirects Quillen factorization systems]]
[[!redirects Quillen factorisation system]]
[[!redirects Quillen factorisation systems]]
