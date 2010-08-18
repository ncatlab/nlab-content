
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

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

[[Introduction to Higher-Order Categorical Logic|Lambek & Scott]] give a different definition of indecomposability.  Generalizing their definition slightly, we may say that an object $X$ is **indecomposable** (in the sense of Lambek--Scott) if any jointly epimorphic family $\{U_i \to X\}_i$ of arrows into $X$ contains at least one epimorphism $U_i \twoheadrightarrow X$, and moreover the unique arrow $0 \to X$ is not epic (this to ensure that 0 is not indecomposable).

If the epi $U_i \twoheadrightarrow X$ is required to be [[regular epimorphism|regular]], then in an _extensive_ category the Lambek--Scott definition implies that given above: if $k \colon X \cong \coprod_i U_i$, then the family $\{k^{-1} \iota_i \colon U_i \to \coprod_i U_i \cong X\}_i$ is jointly epi, so it contains a regular epi $\iota_i k^{-1}$.  But extensivity implies that the $\iota_i$ are mono, and since isos are mono so is the composite $\iota_i k^{-1}$, hence it is iso.  The converse does not hold in general, but it does hold if $X$ is [[projective object|projective]].  See [this](http://mathoverflow.net/questions/35855/indecomposable-objects-in-a-category) MathOverflow thread for a discussion.


## Indecomposability vs irreducibility
{#irreducible}

An [[indecomposable representation]] is precisely an indecomposable object in an appropriate category $Rep$ of [[representations]], as one would expect.  In contrast, an [[irreducible representation]] is precisely a [[simple object]] in $Rep$.  Every irreducible representation is indecomposable, but the converse holds only in special situations (such as the category of finite-dimensional linear representations of a real semisimple Lie group).

However, one level [[decategorified]], an [[irreducible element]] of a [[poset]] $P$ is precisely an indecomposable object of $P$ when thought of as a [[thin category]].  In contrast, a simple object is analogous to an [[atomic element]], although they are not the same thing.  (One might say that atomic = $0$-simple.)  Again, every atomic element is irreducible, but the converse holds only in special situations (such as the power set of any set).

The bottom line is that 'irreducible' and 'indecomposable' sometimes mean the same thing but sometimes don\'t, and 'irreducible' doesn\'t even mean the same thing across different fields.


[[!redirects indecomposable object]]
[[!redirects indecomposable objects]]
