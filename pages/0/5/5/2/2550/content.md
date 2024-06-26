
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Motivic homotopy theory_ or _$\mathbf{A}^1$-homotopy theory_ is the [[homotopy theory]] of smooth [[schemes]], where the [[affine line]] $\mathbf{A}^1$ plays the role of the [[interval]].  Hence what is called the _motivic homotopy category_ or the _$\mathbb{A}^1$-homotopy category_ bears the same relation to [[smooth varieties]] that the ordinary [[homotopy category]] $Ho(Top)$ bears to [[smooth manifolds]].

Both are special cases of a [[homotopy theory]] induced by any sufficiently well-behaved [[interval object]] $I$ in a [[site]] $C$ via [[homotopy localization at an object|localization at that object]]. Ordinary homotopy theory is obtained by taking $C$ to be the [[Diff|site of smooth manifolds]] and $I$ to be the [[real line]] $\mathbb{R}$, and $\mathbb{A}^1$-homotopy theory over a [[Noetherian scheme]] $S$ is obtained when $C$ is the [[Nisnevich site]] of [[smooth scheme]]s of finite type over $S$ and 

\[
  \label{AffineLine}
  I \coloneqq \mathbb{A}^1
\]

is the standard [[affine line]] in $C$.

As for the standard homotopy theory, one can furthermore pass to [[spectrum objects]] and consider the [[stable homotopy category]]. In the following we first discuss

* _[The unstable motivic homotopy category](#UnstableCategory)_

and then

* _[The stable motivic homotopy category](#StableCategory)_.





## The unstable motivic homotopy category 
 {#UnstableCategory}

Let $S$ be a fixed [[Noetherian scheme|Noetherian base scheme]], and let $Sm/S$ be the category of [[smooth schemes]] of finite type over $S$.

+-- {: .num_defn #MotivicHomotopyCategory}
###### Definition

The _motivic homotopy category_ $\mathrm{H}(S)$ over $S$ is the [[homotopy localization]] at the [[affine line]] $\mathbb{A}^1$ (eq:AffineLine) of the [[(∞,1)-topos of (∞,1)-sheaves]] on the [[Nisnevich site]] $Sm/S$. Objects of $\mathrm{H}(S)$ are called _motivic spaces_.
=--

Thus, a motivic space over $S$ is an [[(∞,1)-presheaf]] $F$ on $Sm/S$ such that

* $F$ is an [[(∞,1)-sheaf]] for the [[Nisnevich topology]]
* $F$ is _$\mathbb{A}^1$-homotopy invariant_: for every $X\in Sm/S$, the projection $X\times\mathbb{A}^1\to X$ induces an [[equivalence]] $F(X)\simeq F(X\times\mathbb{A}^1$).

As for any [[homotopy localization]], the inclusion $\mathrm{H}(S)\subset PSh(Sm/S)$ admits a [[left adjoint]] [[localization functor]], and one can show that it preserves finite (∞,1)-products.

The (∞,1)-category $\mathrm{H}(S)$ is a [[locally presentable (∞,1)-category|locally presentable]] and [[locally cartesian closed (∞,1)-category|locally cartesian closed]] (∞,1)-category. However, it is not an [[(∞,1)-topos]] (see Remark 3.5 in [Spitzweck-&#216;stv&#230;r, _Motivic twisted K-theory_, pdf](http://arxiv.org/pdf/1008.4915v1.pdf))

### Motivic spheres {#MotivicSpheres}

The _[[Tate sphere]]_ is the [[pointed object]] of $\mathrm{H}(S)$ defined by

$$ T {\coloneqq} \mathbb{A}^1/\mathbb{G}_m, $$

that is, $T$ is the [[homotopy cofiber]] of the inclusion $\mathbb{G}_m\hookrightarrow \mathbb{A}^1$.
More generally, any algebraic [[vector bundle]] $V$ on $S$ (or, equivalently, any [[quasicoherent sheaf|locally free sheaf]] of finite rank on $S$) has an associated _motivic sphere_ given by its _[[Thom space]]_:

$$ S^V {\coloneqq} V/V^\times. $$

Thus, $T=S^{\mathbb{A}^1}$.

A crucial observation is that $T$ is the [[suspension]] of $\mathbb{G}_m$ (pointed at $1$):

$$ T \simeq S^1\wedge\mathbb{G}_m. $$

Indeed, this follows from the definition of $T$ and the fact that $(\mathbb{A}^1,1)$ is [[contractible]] as a pointed motivic space. It is common to write, for $p\geq q\geq 0$,

$$ S^{p,q} {:=} S^{p-q}\wedge \mathbb{G}_m^{\wedge q}. $$

+-- {: .num_prop}
###### Proposition
There is a canonical equivalence of pointed motivic spaces $T\simeq (\mathbb{P}^1,1)$.

=--

+-- {: .proof}
###### Proof

The cartesian square

$$
  \array{
    \mathbb{G}_m &\stackrel{}{\to}& \mathbb{A}^1
    \\
    \downarrow && \downarrow
    \\
    \mathbb{A}^1 &\stackrel{}{\to}& \mathbb{P}^1
  }
$$

becomes [[(∞,1)-pushout|homotopy cocartesian]] in the [[Nisnevich site|Nisnevich]] (even [[Zariski site|Zariski]]) (∞,1)-topos. By pointing all schemes at $1$ and using that $(\mathbb{A}^1,1)$ is contractible, we deduce that $(\mathbb{P}^1,1)\simeq S^1\wedge \mathbb{G}_m\simeq T.$
=--


## The stable motivic homotopy category 
 {#StableCategory}

+-- {: .num_defn #StableMotivicHomotopyCategory}
###### Definition

The _stable motivic homotopy category_ $SH(S)$ over $S$ is the [[inverse limit]] of the tower of (∞,1)-categories

$$ \dots \stackrel{\Omega_T}{\to} \mathrm{H}_*(S) \stackrel{\Omega_T}{\to} \mathrm{H}_*(S) \stackrel{\Omega_T}{\to} \mathrm{H}_*(S),$$

where $H(S)$ is the ordinary motivic homotopy category from def. \ref{MotivicHomotopyCategory}, and where $\Omega_T {:=}Hom(T, -)$. An object of the stable motivic homotopy category is called a _[[motivic spectrum]]_ (or _$T$-spectrum_).
=--

Thus, a motivic spectrum $E$ is a sequence of pointed motivic spaces $(E_0,E_1,E_2\dots)$ together with [[equivalences]]

$$ \Omega_T E_{i+1}\simeq E_i. $$

Since $T\simeq \mathbb{P}^1$, we could equivalently use $\mathbb{P}^1$ instead of $T$ in the above definition.

Since $T\simeq S^1\wedge \mathbb{G}_m$, $SH(S)$ is indeed a [[stable (∞,1)-category]].

### Symmetric monoidal structure and universal property
 {#SymmetricMonoidalStructureAndUniversalProperty}

The functor $\Omega^\infty_T\colon SH(S)\to \mathrm{H}_*(S)$ sending a motivic spectrum $E$ to its first component $E_0$ admits a [[left adjoint]] $\Sigma_T^\infty$. One can then equip the category $SH(S)$ with the structure of a [[symmetric monoidal (∞,1)-category]] in such a way that the (∞,1)-functor $\Sigma_T^\infty$ can be promoted to a symmetric monoidal (∞,1)-functor. As such, $SH(S)$ is characterized by a [[universal property]]:

+-- {: .num_prop}
###### Proposition
Let $\mathcal{C}$ be a [[locally presentable (∞,1)-category|locally presentable]] [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[(∞,1)-category]].
The (∞,1)-functor

$$ Fun^{\otimes, L}(SH(S),\mathcal{C}) \to Fun^{\otimes} (Sm/S, \mathcal{C}), \quad F\mapsto F\circ \Sigma_T^\infty(-)_+ $$

(where $\otimes$ means "symmetric monoidal" and $L$ means "colimit-preserving")
is [[fully faithful]] and its essential image consists of the symmetric monoidal (∞,1)-functors $F\colon Sm/S\to \mathcal{C}$ satisfying:

* [[Nisnevich site|Nisnevich excision]]
* $\mathbb{A}^1$-homotopy invariance
* _$T$-stability_: the [[homotopy cofiber]] of $F(\mathbb{G}_m)\to F(\mathbb{A}^1)$ is $\otimes$-invertible.

=--

This is ([Robalo, Corollary 5.11](#Robalo)).

+-- {: .num_remark}
###### Remark

Similar characterizations exist for [[noncommutative motives]], see at _[Noncommutative motive -- As the universal additive invariant](noncommutative+motive#AsUniversalAditiveInvariant)_.

=--


### Stable motivic spheres {#StableMotivicSpheres}

Because $T\simeq S^{2,1}$, the stable motivic spheres $S^{p,q}$ are defined for all $p,q\in\mathbb{Z}$.

All the other motivic spheres $S^V$, for $V$ a vector bundle on $S$, also become invertible in $SH(S)$. In fact, the [[Picard ∞-groupoid]] of $SH(S)$ receives a map from the [[algebraic K-theory]] of $S$. These invertible objects are all *exotic* in the sense that they are not equivalent to any of the "categorical" spheres $S^n = \Sigma^n\Sigma^\infty_T S_+$. These exotic spheres play an important r&#244;le in the formalism of [[six operations]] in stable motivic homotopy theory (see [Ayoub](#Ayoub)).

### Cohomology theories {#CohomologyTheories}

Any motivic spectrum $E\in SH(S)$ gives rise to a bigraded [[cohomology|cohomology theory]] for smooth $S$-schemes and more generally for motivic spaces:

$$ E^{p,q}(X) {:=} [\Sigma^\infty_T X_+, \Sigma^{p,q} E], $$

as well as a bigraded homology theory:

$$ E_{p,q}(X) {:=} [S^{p,q}, \Sigma^\infty_T X_+ \wedge E]. $$


## Main features


### The six operations {#SixOperations}

The categories $SH(S)$ for varying base scheme $S$ support a formalism of [[six operations]]. This means that to every morphism of schemes $f: X\to Y$ is associated an ([[inverse image]] $\dashv$ [[direct image]])-[[adjunction]]

$$ f^* : SH(Y) \to SH(X) : f_* $$

and, if $f$ is [[separated morphism|separated]] of finite type, a ([[direct image with compact support]] $\dashv$ [[exceptional inverse image]])-adjunction

$$ f_! : SH(X) \to SH(Y): f^!,$$

satisfying the properties listed at [[six operations]]. For more details see [Ayoub](#Ayoub).

**Stable homotopy functors.** To construct the six operations for $SH$, Voevodsky introduced an axiomatic setting which also subsumes the classical case of [[étale cohomology]]. A _stable homotopy functor_ is a contravariant (∞,1)-functor

$$ D\colon Schemes^{op} \to PrStab (\infty,1) Cat, $$

from some category of schemes to the (∞,1)-category $PrStab (\infty,1) Cat$ of [[locally presentable (∞,1)-category|locally presentable]] [[stable (∞,1)-categories]] and colimit-preserving exact functors, satisfying the following axioms (for $f$ a morphism of schemes, we denote $D(f)$ by $f^*$ and its right adjoint by $f_*$):

1. $D(\emptyset)=0$.

2. If $i: X\to Y$ is an immersion of schemes, then $i_*\colon D(X)\to D(Y)$ is [[fully faithful (∞,1)-functor|fully faithful]].

3. (Smooth base change/[[Beck-Chevalley condition]]) If $f$ is [[smooth scheme|smooth]], then $f^*$ admits a left adjoint $f_\sharp$. Moreover, given a cartesian square
$$
  \array{
    Y' &\stackrel{k}{\to}& X'
    \\
    _h\downarrow && \downarrow \;_f
    \\
    Y &\stackrel{g}{\to}& X
  }
$$
with $f$ smooth, there is a canonical equivalence $h_\sharp k^*\simeq g^* f_\sharp$.

4. (Locality) If $i: Z\hookrightarrow X$ is a [[closed immersion]] with open complement $j: U\hookrightarrow X$, then the pair $(i^*,j^*)$ is [[conservative functor|conservative]].

5. (Homotopy invariance) If $p: X\times\mathbb{A}^1\to X$ is the projection, then $p^*$ is [[fully faithful (∞,1)-functor|fully faithful]].

6. ($T$-stability) If $p$ is as above and $s$ is the zero section of $p$, then $p_\sharp s_*: D(X)\to D(X)$ is an [[equivalence of (∞,1)-categories]].

+-- {: .num_theorem}

###### Theorem
(Ayoub, Voevodsky) Every stable homotopy functor admits a formalism of four operations $f^\ast$, $f_\ast$, $f_!$, and $f^!$.
=--

For a more precise statement, see [Ayoub, Scholie 1.4.2](#Ayoub).

+-- {: .num_theorem}
###### Theorem
$SH$ is a stable homotopy functor.
=--

This is essentially proved in [Morel-Voevodsky 99](#MorelVoevodsky99). In fact, something stronger is expected to be true:

+-- {: .num_theorem}
###### Expected Theorem
$SH$ is the [[initial object]] in the [[(∞,2)-category]] of stable homotopy functors.
=--

This theorem has not been proved yet; however, [Ayoub's thesis](#Ayoub) shows that every stable homotopy functor factors through $SH$.


### Realization functors {#RealizationFunctors}

**Complex realization.** The functor

$$ Sm/\mathbb{C}\to SmoothMfd,\quad X\mapsto X(\mathbb{C}) $$

associating to a smooth $\mathbb{C}$-scheme $X$ its set of $\mathbb{C}$-points with its structure of [[smooth manifold]] induces a functor from $\mathrm{H}(\mathbb{C})$ to the [[homotopy localization]] of the [[smooth ∞-groupoid|smooth (∞,1)-topos]] at the [[interval object]] $\mathbb{A}^1(\mathbb{C})\simeq \mathbb{R}^2$. As this localization is equivalent to the [[(∞,1)-topos]] $\infty Grpd$ of [[discrete ∞-groupoid]]s, we obtain the _complex realization functor_

$$ \mathrm{H}(\mathbb{C}) \to \infty Grpd. $$

After $T$-stabilization, we obtain a functor from $SH(\mathbb{C})$ to the [[(∞,1)-category of spectra]], called the _complex Betti realization_

$$ \mathrm{Be}:\mathrm{Sp}(\mathbb{C}) \rightarrow \mathrm{Sp} $$.

**Real realization.** The functor

$$ Sm/\mathbb{R}\to \mathbb{Z}/2-SmoothMfd,\quad X\mapsto X(\mathbb{C}) $$

associating to a smooth $\mathbb{R}$-scheme $X$ its set of $\mathbb{C}$-points with its structure of [[smooth manifold]] together with the action of $\mathbb{Z}/2$ by [[complex conjugation]] induces as in the complex case the _Real realization functor_

$$ \mathrm{H}(\mathbb{R}) \to PSh_\infty(\mathcal{O}_{\mathbb{Z}/2}), $$

where $\mathcal{O}_{\mathbb{Z}/2}$ is the [[orbit category]] of $\mathbb{Z}/2$. After $T$-stabilization, we obtain a functor from $SH(\mathbb{R})$ to the (∞,1)-category of [[equivariant stable homotopy theory|genuine]] $\mathbb{Z}/2$-spectra, called the _real Betti realization_


$$ \mathrm{Be}:\mathrm{Sp}(\mathbb{R}) \rightarrow \mathrm{Sp}_{C_2} $$.

**&#201;tale realization.** Over a separably closed field $k$, we can consider the [[étale homotopy|étale homotopy type]] functor

$$ Sh_{\infty}((Sm/k)_{Nis})\to Sh_{\infty}((Sm/k)_{et}) \stackrel{\Pi}{\to} Pro(\infty Grpd) $$

(see [[shape of an (∞,1)-topos]]). However, it does not descend to $\mathrm{H}(k)$ because the &#233;tale homotopy type is not $\mathbb{A}^1$-homotopy invariant. To rectify this, we choose a prime $l\neq \operatorname{char}(k)$ and consider the reflexive [[localization]] $Pro(\infty Grpd)^\wedge_{l}$ of $Pro(\infty Grpd)$ at the class of maps inducing isomorphisms on pro-homology groups with coefficients in $\mathbb{Z}/l$. We then obtain an _&#233;tale realization functor_

$$ \mathrm{H}(k) \to Pro(\infty Grpd)^\wedge_{l}. $$


### The slice filtration {#SliceFiltration}

_See [[motivic slice filtration]]._

The slice filtration is a filtration of $\mathrm{H}(S)$ and of $SH(S)$ which is analogous to the [[Postnikov tower in an (∞,1)-category|Postnikov filtration]] for [[(∞,1)-topoi]]. It generalizes the _coniveau filtration_ in [[algebraic K-theory]], the _fundamental filtration_ on [[Witt groups]], and the _weight filtration_ on [[mixed Tate motives]].

If $S$ is [[smooth scheme|smooth]] over a [[field]], the layers of the slice filtration of a motivic spectrum (called its _slices_) are modules over the [motivic Eilenberg&#8211;Mac Lane spectrum](#MotivicCohomology) $H(\mathbb{Z})$. At least if $S$ is a [[field]] of characteristic zero, this is the same thing as an integral [[motive]]. The [[spectral sequences]] associated to the slice filtration are analogous to the [[Atiyah-Hirzebruch spectral sequence]]s in that their first page consists of [[motivic cohomology]] groups.

### The $\mathbb{A}^1$-Postnikov filtration
{#A1PostnikovFiltration}

One can also consider the filtration on $\mathrm{H}(S)$ induced by the [[Postnikov tower in an (∞,1)-category|Postnikov filtration]] in the containing [[Nisnevich (∞,1)-topos]]. A motivic space is _$\mathbb{A}^1$-n-connected_ if it is [[n-connected]] as a Nisnevich (∞,1)-sheaf, and the _$\mathbb{A}^1$-homotopy groups_ $\pi_n^{\mathbb{A}^1}(X,x)$ of a motivic space are its [[homotopy groups in an (∞,1)-topos|homotopy groups]] as a Nisnevich (∞,1)-sheaf.

If $S$ has finite [[Krull dimension]], $\mathbb{A}^1$-homotopy groups detect [[equivalences]] because the [[Nisnevich (∞,1)-topos]] is [[hypercomplete]].

+-- {: .num_remark}
###### Remark
 The usage of the $\mathbb{A}^1$- prefix in the above definitions may seem strange since all these notions are simply inherited from the Nisnevich (∞,1)-topos. The point is that, when a smooth scheme $X$ is viewed as a motivic space, a localization functor is implicitly applied. The underlying Nisnevich (∞,1)-sheaf of the motivic space "$X$" can thus be very different from the Nisnevich (∞,1)-sheaf represented by $X$ (for which these definitions would not be interesting at all!).
=--

Intuitively, $\mathbb{A}^1$-connectedness corresponds to the topological connectedness of the _real points_ rather than of the complex points. For example, $\mathbb{G}_m$ is not $\mathbb{A}^1$-connected, and $\mathbb{P}^1$ is $\mathbb{A}^1$-connected but not $\mathbb{A}^1$-simply connected.

+-- {: .num_theorem}
###### Theorem
Let $k$ be a [[perfect field]] (resp. a [[field]]) and $X$ a [[Nisnevich site|Nisnevich]] (∞,1)-sheaf of spaces (resp. of spectra) on $Sm/k$. If $X$ is [[n-connected]] for some n, then its $\mathbb{A}^1$-localization is also n-connected.
=--
 
This is Morel's _connectivity theorem_ ([Morel, Theorem 5.38](#Morel)). It follows that the $\mathbb{A}^1$-Postnikov filtration on $\mathrm{H}(k)$ "extends" to a [[t-structure]] on the stable (∞,1)-category $SH(k)$, called the _homotopy t-structure_.


### Relation to the theory of motives

The stable motivic homotopy category $SH(S)$ is the basis for several definitions of the [[motive|derived category of mixed motives]] over $S$. See there for more details.

### Relation to the theory of symmetric bilinear forms

Motivic homotopy theory is also related to the classical theory of symmetric [[bilinear forms]] (or [[quadratic forms]] in characteristic $\neq 2$). Invariants such as [[Witt groups]], oriented [[Chow groups]], and [[Hermitian K-theory]] are representable in the motivic homotopy category.

A central theorem of [[Fabien Morel]] states that, if $k$ is a [[field]], the ring of endomorphisms of the motivic sphere spectrum $S^0\in SH(k)$ is canonically isomorphic to the _Grothendieck&#8211;Witt ring_ $GW(k)$: this is the [[group completion]] of the [[semiring]] of isomorphism classes of nondegenerate symmetric [[bilinear form]]s over $k$ ([Morel, Corollary 5.43](#Morel)). The case $k=\mathbb{R}$ is especially enlightening: there the stable homotopy class of a pointed endomorphism of $\mathbb{P}^1$ corresponds to the nondegenerate symmetric bilinear form over $\mathbb{R}$ whose dimension is the degree of the induced endomorphism of $\mathbb{P}^1(\mathbb{C})\simeq S^2$ and whose signature is the degree of the induced endomorphism of $\mathbb{P}^1(\mathbb{R})\simeq S^1$.

## Equivariant motivic homotopy theory
 {#EquivariantMotivicHomotopyTheory}

A general theory of [[equivariant motivic homotopy theory|equivariant]] (unstable and stable) motivic homotopy theory was introduced in ([Carlsson-Joshua 2014](#CJ2014)) and further developed in ([Hoyois 15](#Hoyois15)).

## Applications and examples

### $\mathbb{A}^1$-coverings and the $\mathbb{A}^1$-fundamental groupoid
{#A1coverings}

Like the $\mathbb{A}^1$-[Postnikov filtration](#A1PostnikovFiltration), $\mathbb{A}^1$-coverings and the $\mathbb{A}^1$-fundamental groupoid $\Pi_1^{\mathbb{A}^1}$ are defined in the containing [[Nisnevich (∞,1)-topos]]. A morphism of motivic spaces $f: Y\to X$ is an _$\mathbb{A}^1$-covering_ if it is [[n-truncated object of an (∞,1)-category|0-truncated]] as a morphism between Nisnevich (∞,1)-sheaves. Such a morphism is determined by its 1-truncation $\tau_{\leq 1}f$, and hence there is an equivalence between the category of $\mathbb{A}^1$-coverings of $X$ and that of $\mathbb{A}^1$-invariant objects in the [[classifying topos]] of the Nisnevich sheaf of groupoids
$$ \Pi_1^{\mathbb{A}^1}(X):=\tau_{\leq 1}X. $$

+-- {: .num_theorem}
###### Theorem
Let $k$ be a [[field]] and $X\in\mathrm{H}_\ast(k)$ a pointed $\mathbb{A}^1$-connected motivic space. Let $\tilde X$ be the $\mathbb{A}^1$-localization of the 1-connected cover of $X$ (as a pointed Nisnevich (∞,1)-sheaf). Then:

1. $\tilde X$ is the initial object in the category of pointed $\mathbb{A}^1$-coverings of $X$.

2. $\tilde X$ is the unique pointed $\mathbb{A}^1$-covering of $X$ which is $\mathbb{A}^1$-simply connected.

3. The Nisnevich sheaf of (unpointed) automorphisms $Aut_X(\tilde X)$ is canonically isomorphic to $\pi_1^{\mathbb{A}^1}(X)$.
=--

This is [Morel, Theorem 6.8](#Morel). The key input for this theorem is the fact that $\Pi_1^{\mathbb{A}^1}(X)$ is $\mathbb{A}^1$-invariant; this is only known for $\mathbb{A}^1$-connected motivic spaces over fields, which explains the hypotheses of the theorem.

When $X$ is a smooth $S$-scheme, examples of $\mathbb{A}^1$-coverings of $X$ include $\mathbb{G}_m$-torsors and finite Galois coverings of degree prime to the characteristics of $X$ ([Morel, Lemma 6.5](#Morel)). This can be used to compute some $\mathbb{A}^1$-fundamental groups, for example:

+-- {: .num_prop}
###### Proposition
If $n\geq 2$, $\pi_1^{\mathbb{A}^1}(\mathbb{P}^n)=\mathbb{G}_m$.
=--

+-- {: .proof}
###### Proof
The projection $\mathbb{A}^{n+1}-0\to\mathbb{P}^n$ is a $\mathbb{G}_m$-torsor and hence an $\mathbb{A}^1$-covering. If $n\geq 2$, $\mathbb{A}^{n+1}-0$ is moreover $\mathbb{A}^1$-simply connected and hence is the universal $\mathbb{A}^1$-covering of $\mathbb{P}^n$. Thus, $\pi_1^{\mathbb{A}^1}(\mathbb{P}^n)=Aut_{\mathbb{P}^n}(\mathbb{A}^{n+1}-0)=\mathbb{G}_m$.
=--


### $\mathbb{A}^1$-h-cobordisms and the classification of surfaces

An _$\mathbb{A}^1$-h-cobordism_ is a surjective [[proper map]] $X\to\mathbb{A}^1$ in $Sm/S$ such that, for $i=0,1$, the fiber $X_i$ is smooth and the inclusion $X_i\hookrightarrow X$ becomes an equivalence in $\mathrm{H}(S)$.

Asok and Morel used $\mathbb{A}^1$-h-cobordisms to classify rational smooth proper surfaces over [[algebraically closed field]]s up to $\mathbb{A}^1$-homotopy. See [Asok-Morel](#AsokMorel).

### Euler classes and splittings of algebraic vector bundles

Let $k$ be a [[perfect field]]. If $X$ is a smooth affine $k$-scheme, Morel proved that

$$ Vect_n(X) \cong [X,BGL_n], $$

where $[-,-]$ denote homotopy classes of maps in the motivic homotopy category $\mathrm{H}(k)$, def. \ref{MotivicHomotopyCategory}. The classical problem of determining whether a [[rank]] $n$ [[vector bundle]] splits off a trivial [[line bundle]] is thus equivalent to determining whether the classifying map $X\to BGL_n$ lifts to $BGL_{n-1}$ in $\mathrm{H}(k)$. If the Nisnevich [[cohomological dimension]] of $X$ is at most $n$, we can use [[obstruction theory]] together with the [[fiber sequence]]

$$ \mathbb{A}^n-0 \to BGL_{n-1} \to BGL_n $$

to obtain the following criterion:

+-- {: .num_theorem}
###### Theorem
(Morel)
Suppose that $n\geq 2$ and that $X$ has dimension $\leq n$. Let $\xi$ be a vector bundle of rank $n$ over $X$.
Then there exists a canonical class
$$ e(\xi)\in H^n_{Nis}(X,\pi_{n-1}^{\mathbb{A}^1}(\mathbb{A}^n-0)(\mathrm{det} \xi)) $$
which vanishes if and only if $\xi$ splits off a trivial line bundle.
=--

The twist by the determinant $\mathrm{det} \xi$ comes from the nontrivial $\mathbb{A}^1$-fundamental group $\pi_1^{\mathbb{A}^1}(BGL_n)=\mathbb{G}_m$.

The Nisnevich sheaf $\pi_{n-1}^{\mathbb{A}^1}(\mathbb{A}^n-0)$ is the n-th Milnor&#8211;Witt K-theory sheaf $\mathbf{K}^{MW}_n$, so that

$$ H^n_{Nis}(X,\pi_{n-1}^{\mathbb{A}^1}(\mathbb{A}^n-0)(\mathrm{det} \xi)) \cong \widetilde{CH}^n(X; \mathrm{det} \xi) $$

is the n-th oriented [[Chow group]] of $X$. When $k$ is [[algebraically closed field|algebraically closed]], this is just the usual Chow group of $X$ and $e(\xi)$ can be identified with the top Chern class of $\xi$.


### Motivic cohomology {#MotivicCohomology}

Suppose that $S$ is a [[smooth scheme]] over a [[field]]. Then the [[motivic cohomology]] of smooth $S$-schemes is representable in $\mathrm{H}(S)$ and in $SH(S)$. If $A$ is an [[abelian group]] and $p\geq q\geq 0$, there exist a pointed motivic spaces $K(A(q),p)$, called a _motivic Eilenberg&#8211;MacLane space_, such that, for every $X\in Sm/S$,

$$ H^{p-r,q-s}(X,A) = [\Sigma^{r,s}X_+, K(A(q),p)]. $$

Voevodsky's _cancellation theorem_ implies that $\Omega_T K(A(q+1), p+2)\simeq K(A(q), p)$. It follows that the sequence of motivic spaces $K(A(n),2n)$ form a $T$-spectrum $H(A)$, called a _motivic Eilenberg&#8211;MacLane spectrum_, such that

$$ H^{p,q}(X,A) = [\Sigma_T^\infty X_+, \Sigma^{p,q} H(A)]. $$

If $R$ is a [[commutative ring]], the motivic spectrum $H(R)$ has a canonical structure of $E_\infty$-algebra in $SH(S)$ which induces the ring structure in motivic cohomology.

Unlike in topology, $H(\mathbb{Q})$ is not always equivalent to the rational motivic sphere spectrum $S^0_{\mathbb{Q}}$: this is only the case if $-1$ is a sum of squares in the base field. In general, $H(\mathbb{Q})$ is a direct summand of $S^0_{\mathbb{Q}}$.

The stable (∞,1)-category of $H(\mathbb{Q})$-[[modules]] is equivalent to the [[derived category of mixed motives]]. See there for more details.

### Algebraic K-theory

See [[algebraic K-theory spectrum]].

### Algebraic cobordism
 {#AlgebraicCobordism}

See [[algebraic cobordism]].





## Related concepts

* [[equivariant homotopy theory]]

* [[motive]]
* [[motivic cohomology]]

* [[slice spectral sequence]]

* [[B1-homotopy theory]]

* There is an analog of $\mathbb{A}^1$-homotopy theory for other geometries. The extra left adjoint on a [[cohesive (infinity,1)-topos]] may realize the localization at an abstract [[continuum]] [[line object]]. See at _[[cohesion]]_ for more details.


## References

### General

The original references:

* [[Vladimir Voevodsky]], $\mathbf{A}^1$-Homotopy Theory. Proceedings of the International Congress of Mathematicians, Vol. I (Berlin, 1998). Doc. Math. 1998, Extra Vol. I, 579&#8211;604 (electronic).  [web](http://www.math.uiuc.edu/documenta/xvol-icm/00/Voevodsky.MAN.html)

* {#MorelVoevodsky99} [[Fabien Morel]], [[Vladimir Voevodsky]], _$\mathbb{A}^1$-homotopy theory of schemes_, Publications Mathématiques de l'IHÉS, Volume 90 (1999), p. 45-143  ([Numdam:PMIHES_1999__90__45_0](http://www.numdam.org/item/?id=PMIHES_1999__90__45_0) [K-Theory:0305](https://faculty.math.illinois.edu/K-theory/0305/) )


* {#Morel} [[Fabien Morel]], _$\mathbb{A}^1$-algebraic topology over a field_, LNM 2052, 2012, ([pdf](https://www.mathematik.uni-muenchen.de/~morel/Prepublications/A1TopologyLNM.pdf))

* {#AsokMorel} [[Aravind Asok]], [[Fabien Morel]], _Smooth varieties up to $\mathbb{A}^1$-homotopy and algebraic h-cobordisms_, Adv. Math. **227** (5) (2011) 1990-2058 &lbrack;[arXiv:0810.0324](http://arxiv.org/abs/0810.0324), [doi:10.1016/j.aim.2011.04.009](https://doi.org/10.1016/j.aim.2011.04.009)&rbrack;



Readable introductions to the subject are:

* [[Bjørn Ian Dundas]], [[Marc Levine]], [[Paul Arne Østvær]], [[Oliver Röndigs]], [[Vladimir Voevodsky]], _Motivic Homotopy Theory: Lectures at a Summer School in Nordfjordeid, Norway, August 2002_, Springer, Universitext, (2006) ([doi:10.1007/978-3-540-45897-5](https://www.springer.com/de/book/9783540458951))

* [[Marc Levine]], _Motivic Homotopy Theory_, Milan j. math (2008), ([pdf](http://www.math.unam.mx/~javier/levine.pdf))

* [[Fabien Morel]], _An introduction to $\mathbb{A}^1$ homotopy theory_, ICTP Trieste July 2002 ([directory](http://publications.ictp.it/lns/vol15/vol15toc.html), [pdf](http://www.ictp.it/%7Epub_off/lectures/lns015/Morel/Morel.pdf), [ps](https://www.mathematik.uni-muenchen.de/~morel/Prepublications/lectureTrieste.ps))

* [[Fabien Morel]], _On the motivic stable &#960;&#8320; of the sphere spectrum_ ([ps](https://www.mathematik.uni-muenchen.de/~morel/Prepublications/Newton.ps))

* {#Arndt17} [[Peter Arndt]], _Abstract motivic homotopy theory_, thesis 2017 ([web](https://repositorium.ub.uni-osnabrueck.de/handle/urn:nbn:de:gbv:700-2017021015476?mode=full),  [pdf](https://repositorium.ub.uni-osnabrueck.de/bitstream/urn:nbn:de:gbv:700-2017021015476/6/thesis_arndt.pdf), [[ArndtAbstractMotivic.pdf:file]])

   {#Arndth19} exposition: lecture at _[Geometry in Modal HoTT](https://felix-cherubini.de/abstracts.html)_, 2019 ([recording I](https://www.youtube.com/watch?v=f0wpcNs8hQo), [recording II](https://www.youtube.com/watch?v=sTl8637a2Zo))


Detailed discussion of the [[model structure on simplicial presheaves]] on the [[Nisnevich site]] and its [[homotopy localization]] to [[A1-homotopy theory]]:

* [[John F. Jardine]], *[[Local homotopy theory]]*, Springer Monographs in Mathematics (2015) &lbrack;[doi:10.1007/978-1-4939-2300-7](https://doi.org/10.1007/978-1-4939-2300-7)&rbrack;

with brief exposition in:

* [[John F. Jardine]], *Motivic spaces and the motivic stable category* &lbrack;[pdf](http://www.aimath.org/WWN/motivesdessins/motivic.pdf), [[Jardine-MotivicSpaces.pdf:file]]&rbrack;


For more on the general procedure see [[homotopy localization]].

The universal property of $SH(S)$ is proved in

* {#Robalo} [[Marco Robalo]], _Noncommutative Motives I: A Universal Characterization of the Motivic Stable Homotopy Theory of Schemes_, 2013 ([pdf](http://arxiv.org/pdf/1206.3645v3.pdf))


For the formalism of [[six operations]] see

* {#Ayoub} [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescants dans le monde motivique_ PhD thesis, Paris &lbrack;[pdf](http://www.math.uiuc.edu/K-theory/0761/THESE.pdf), [K:0761](https://faculty.math.illinois.edu/K-theory/0761)&rbrack;

* [[Joseph Ayoub]], *Les six opérations de Grothendieck et le formalisme des cycles évanescents dans le monde motivique (I)*, Astérisque **314** (2007) &lbrack;[numdam:AST_2007__314__R1_0](http://www.numdam.org/issues/AST_2007__314__R1_0)&rbrack;

* [[Joseph Ayoub]], *Les six opérations de Grothendieck et le formalisme des cycles évanescents dans le monde motivique (II)*, Astérisque **315** (2007) &lbrack;[numdam:AST_2007__315__1_0](http://www.numdam.org/issues/AST_2007__315__1_0)&rbrack;

* [[Vladimir Voevodsky]], [[Pierre Deligne]], _Voevodsky's lectures on cross functors_ ([pdf](https://www.math.ias.edu/vladimir/sites/math.ias.edu.vladimir/files/2015_transfer_from_ps_delnotes01.pdf))

The slice filtration was defined in

* [[Vladimir Voevodsky]], _Open problems in the stable motivic homotopy theory_ K-theory, 0392 ([web](https://faculty.math.illinois.edu/K-theory/0392/) [pdf](https://faculty.math.illinois.edu/K-theory/0392/nowmovo.pdf))

Representability results:

* [[Aravind Asok]], [[Marc Hoyois]], [[Matthias Wendt]], *Affine representability results in $\mathbb{A}^1$-homotopy theory I: Vector bundles*, Duke Math. J. **166** 10 (2017) 1923-1953 &lbrack;[arXiv:1506.07093](http://arxiv.org/abs/1506.07093), [doi:10.1215/00127094-0000014X](https://doi.org/10.1215/00127094-0000014X)&rbrack;

* [[Aravind Asok]], [[Marc Hoyois]], [[Matthias Wendt]], _Affine representability results in $\mathbb{A} ^1$-homotopy theory II: principal  bundles and homogeneous spaces_, Geom. Topol. **22** (2018) 1181-1225 &lbrack;[arXiv:1507.08020](http://arxiv.org/abs/1507.08020), [doi:10.2140/gt.2018.22.1181](https://doi.org/10.2140/gt.2018.22.1181)&rbrack;

Discussion related to [[étale homotopy]]:

* [[Daniel Isaksen]], _&#201;tale realization of the $\mathbb{A} ^1$-homotopy theory of schemes_, Advances in Mathematics 184 (2004) 

Discussion about [[thick ideals]]:

* [[Ruth Joachimi]], _Thick ideals in equivariant and motivic stable homotopy categories_, [arXiv:1503.08456](http://arxiv.org/abs/1503.08456).

On ([[stable cohomotopy|stable]]) [[motivic cohomology|motivic]] [[Cohomotopy]] of [[schemes]] (as  [[motivic homotopy theory|motivic homotopy classes]] of maps into [[motivic sphere|motivic]] [[Tate spheres]]):

* [[Aravind Asok]], [[Jean Fasel]], [[Mrinal Kanti Das]], *Euler class groups and motivic stable cohomotopy*, Journal of the EMS **24** 8 (2022) 2775–2822 &lbrack;[arXiv:1601.05723](https://arxiv.org/abs/1601.05723), [doi:10.4171/jems/1156](https://doi.org/10.4171/jems/1156)&rbrack;

* [[Samuel Lerbet]], *Motivic stable cohomotopy and unimodular rows*, Advances in Mathematics **436** 109415 (2024) &lbrack;[arXiv:2206.11688](https://arxiv.org/abs/2206.11688), [doi:10.1016/j.aim.2023.109415](https://doi.org/10.1016/j.aim.2023.109415)&rbrack;


### Motivic homotopy theory in other contexts

[[equivariant motivic homotopy theory]] is developed in

* {#CJ2014} [[Gunnar Carlsson]], [[Roy Joshua]], _Equivariant motivic homotopy theory_, [arXiv](http://arxiv.org/abs/1404.1597v1).

This was vastly generalized and studied more thoroughly in

* {#Hoyois15} [[Marc Hoyois]], *The six operations in equivariant motivic homotopy theory*, Adv. Math. **305** (2017) 197-279 &lbrack;[arXiv:1509.02145](https://arxiv.org/abs/1509.02145), [doi:10.1016/j.aim.2016.09.031](https://doi.org/10.1016/j.aim.2016.09.031)&rbrack;

  > (cf. [[Grothendieck's six operations]])




Motivic homotopy theory of [[derived noncommutative geometry|noncommutative spaces]] (associative dg-algebras) is studied in

* [[Marco Robalo]], _Noncommutative Motives I: A Universal Characterization of the Motivic Stable Homotopy Theory of Schemes_, 2013 ([pdf](http://arxiv.org/pdf/1206.3645v3.pdf))

Motivic homotopy theory of [[associative ring|associative]] [[nonunital rings]] is studied in

* [[Grigory Garkusha]], _Homotopy theory of associative rings_, [arXiv:math/0608482](http://arxiv.org/abs/math/0608482v2).

* [[Grigory Garkusha]], _Algebraic Kasparov K-theory. II_, [arXiv:1206.0178](http://arxiv.org/abs/1206.0178v2).

See also

* [[analytic motivic homotopy theory]]
* [[logarithmic motivic homotopy theory]]

[[!redirects A1-homotopy]]
[[!redirects A1 homotopy]]
[[!redirects A1-homotopy theory]]
[[!redirects A1 homotopy theory]]
[[!redirects A1-homotopy category]]
[[!redirects A1 homotopy category]]

[[!redirects stable motivic homotopy theory]]
[[!redirects motivic stable homotopy theory]]

[[!redirects motivic homotopy category]]
[[!redirects stable motivic homotopy category]]
[[!redirects motivic space]]
[[!redirects motivic spaces]]
[[!redirects motivic spectrum]]
[[!redirects motivic spectra]]

[[!redirects homotopy theory of schemes]]

