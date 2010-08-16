# Indecomposable objects
* table of contents
{: toc}

## Definition

An object $X$ of a category $C$ is **indecomposable** if it cannot be expressed as a non-trivial [[coproduct]] of objects of $C$.  Formally, $X$ is indecomposable if given an isomorphism $X \cong \coprod_i U_i$, there is a unique index $i$ such that $X \cong U_i$ and $U_j \cong 0$ for all $j \neq i$, where $0$ is an [[initial object]].

The requirement that $i$ be unique keeps the initial object itself from being indecomposable; this is analogous to being [[too simple to be simple]].


## Remarks

If $C$ is an [[extensive category]], meaning that coproducts in $C$ are [[disjoint coproduct|disjoint]] and pullback-stable, then we have

+-- {: .un_prop}
###### Proposition
An object $X$ of $C$ is indecomposable if and only if it is [[connected object|connected]], that is if the hom functor $\hom(X,-)$ preserves coproducts.
=--

+-- {: .proof}
###### Proof
If $X$ is connected, then a morphism $k \colon X \to \coprod_i U_i$ factors uniquely as $\iota_i \circ \bar k \colon X \to U_i \to \coprod_i U_i$, where $\iota_i$ is the coprojection.  Suppose $k$ is invertible -- then the composite $k^{-1} \iota_i \bar k \colon X \to U_i \to \coprod_i U_i \to X$ is the identity.  Consider
$$
U_i \overset{\iota_i}{\to} \coprod_i U_i \overset{k^{-1}}{\to} X \overset{k}{\to} \coprod_i U_i
$$
Of course $k \circ k^{-1} = 1$, while $k = \iota_i \bar k$ as before.  So $\iota_i \circ \bar k k^{-1} \iota_i = \iota_i$.  But because $C$ is extensive the coprojections are monic, so $\bar k k^{-1} \iota_i = 1$.  Thus $\bar k$ is an isomorphism $X \cong U_i$, with inverse $k^{-1} \iota_i$.  Because coproducts in $C$ are disjoint, the pullback of distinct coprojections is $0$, and because $U_i \cong X \cong \coprod_i U_i$, the pullback of $\iota_i$ along $\iota_j$ is an isomorphism, showing that $U_j \cong 0$ for $j \neq i$.

Conversely, assume $X$ is indecomposable.  Given $k \colon X \to \coprod_i U_i$, we are to produce a unique $X \to U_i$ as above.  Because $C$ is extensive, $k$ is isomorphic (in the slice category $C/\coprod_i U_i$) to $\coprod_i k_i \colon \coprod_i X_i \to \coprod_i U_i$ for some family $\{k_i \colon X_i \to U_i\}$.  But $X \cong \coprod_i X_i$ gives us by indecomposability of $X$ an isomorphism $X \cong X_i$ for a unique $i$, which composed with $k_i$ gives a morphism $X \cong X_i \to U_i$.  Because $\coprod_i k_i = [\iota_i k_i]_i$ (where the right-hand side is the copairing of the family $\{\iota_i k_i\}_i$), and because the $X_j \cong 0$ for $j\neq i$, the composite $\iota_i k_i \colon X \cong X_i \to U_i \to \coprod_i U_i$ is equal to $k$.  Hence $X$ is connected.
=--

If $C$ is a [[presheaf category]] $[S^{op}, Set]$ (thus a [[Grothendieck topos]] and so _a fortiori_ (infinitary) extensive), then it is easy to see that the [[representable functors]] $S(-,s)$ are connected and so indecomposable.  Conversely, the objects of $[S^{op}, Set]$ that are indecomposable as well as [[projective object|projective]] are precisely the objects of the [[Cauchy completion]] of $S$.

[[!redirects indecomposable object]]
[[!redirects indecomposable objects]]
