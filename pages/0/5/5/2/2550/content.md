
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

The motivic homotopy category (or $\mathbb{A}^1$-homotopy category) bears the same relation to [[smooth varieties]] that the ordinary [[homotopy category]] $Ho(Top)$ bears to [[smooth manifolds]].

Both are special cases of the [[homotopy theory]] induced by any sufficiently well-behaved [[interval object]] $I$ in a [[site]] $C$. Ordinary homotopy theory is obtained by taking $C$ to be the site of smooth manifold and $I$ to be the [[real line]] $\mathbb{R}$, and $\mathbb{A}^1$-homotopy theory over a [[Noetherian scheme]] $S$ is obtained when $C$ is the [[Nisnevich site]] of [[smooth scheme]]s of finite type over $S$ and 

$$
  I = \mathbb{A}^1
$$

is the standard [[affine line]] in $C$.

## The unstable motivic homotopy category

Let $S$ be a fixed [[Noetherian scheme|Notherian base scheme]], and let $Sm/S$ be the category of [[smooth schemes]] of finite type over $S$.

+-- {: .num_defn}
###### Definition
The motivic homotopy category $\mathrm{H}(S)$ over $S$ is the [[homotopy localization]] of the [[Nisnevich (∞,1)-topos]] on the site $Sm/S$ equipped with the interval object $\mathbb{A}^1$. Objects of $\mathrm{H}(S)$ are called _motivic spaces_.
=--

Thus, a motivic space over $S$ is an [[(∞,1)-presheaf]] $F$ on $Sm/S$ such that

* $F$ is an [[(∞,1)-sheaf]] for the [[Nisnevich topology]]
* $F$ is _$\mathbb{A}^1$-homotopy invariant_: for every $X\in Sm/S$, the projection $X\times\mathbb{A}^1\to X$ induces an [[equivalence]] $F(X)\simeq F(X\times\mathbb{A}^1$).

As for any [[homotopy localization]], the inclusion $\mathrm{H}(S)\subset PSh(Sm/S)$ admits a [[left adjoint]] [[localization functor]], and one can show that it preserves finite (∞,1)-products. This allows us to regard any presheaf on (or object of) $Sm/S$ as an object of $\mathrm{H}(S)$.

The (∞,1)-category $\mathrm{H}(S)$ is a [[locally presentable (∞,1)-category|locally presentable]] and [[locally cartesian closed (∞,1)-category|locally cartesian closed]] (∞,1)-category. However, it is not an [[(∞,1)-topos]].

### Motivic spheres

The **Tate sphere** is the [[pointed object]] of $\mathrm{H}(S)$ defined by

$$ T := \mathbb{A}^1/\mathbb{G}_m, $$

that is, $T$ is the [[homotopy cofiber]] of the inclusion $\mathbb{G}_m\hookrightarrow \mathbb{A}^1$.
More generally, any algebraic [[vector bundle]] $V$ on $S$ (or, equivalently, any [[locally free sheaf]] of finite rank on $S$) has an associated _motivic sphere_ given by its _Thom space_:

$$ S^V := V/V^\times. $$

Thus, $T=S^{\mathbb{A}^1}$.

A crucial observation is that $T$ is the [[suspension]] of $\mathbb{G}_m$ (pointed at $1$):

$$ T \simeq S^1\wedge\mathbb{G}_m. $$

Indeed, this follows from the definition of $T$ and the fact that $(\mathbb{A}^1,1)$ is [[contractible]] as a pointed motivic space. It is common to write, for $p\geq q\geq 0$,

$$ S^{p,q} := S^{p-q}\wedge \mathbb{G}_m^{\wedge q}. $$

+-- {: .num_prop}
###### Proposition
There is a canonical equivalence of pointed motivic spaces $T\simeq (\mathbb{P}^1,\infty)$.

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

becomes [[(∞,1)-pushout|homotopy cocartesian]] in the [[Nisnevich site|Nisnevich]] (even [[Zariski site|Zariski]]) (∞,1)-topos. By pointing all schemes at $1$ and using that $(\mathbb{A}^1,1)$ is contractible, we deduce that

$$(\mathbb{P}^1,1)\simeq S^1\wedge \mathbb{G}_m\simeq T.$$

Finally, $(\mathbb{P}^1,1)$ and $(\mathbb{P}^1,\infty)$ are isomorphic as pointed schemes, and the isomorphism is made "canonical" by fixing $0$.
=--


## The stable motivic homotopy category

+-- {: .num_defn}
###### Definition
The stable motivic homotopy category $SH(S)$ over $S$ is the [[inverse limit]] of the tower of (∞,1)-categories

$$ \dots \stackrel{\Omega_T}{\to} \mathrm{H}_*(S) \stackrel{\Omega_T}{\to} \mathrm{H}_*(S) \stackrel{\Omega_T}{\to} \mathrm{H}_*(S),$$

where $\Omega_T :=Hom(T, -)$. An object of the stable motivic homotopy category is called a _motivic spectrum_ (or _$T$-spectrum_).
=--

Thus, a motivic spectrum $E$ is a sequence of pointed motivic spaces $(E_0,E_1,E_2\dots)$ together with equivalences

$$ \Omega_T E_{i+1}\simeq E_i. $$

Since $T\simeq \mathbb{P}^1$, we could equivalently use $\mathbb{P}^1$ instead of $T$ in the above definition.

Since $T\simeq S^1\wedge \mathbb{G}_m$, $SH(S)$ is indeed a [[stable (∞,1)-category]].

### Symmetric monoidal structure and universal property

The functor $\Omega^\infty_T\colon SH(S)\to \mathrm{H}_*(S)$ sending a motivic spectrum $E$ to its first component $E_0$ admits a [[left adjoint]] $\Sigma_T^\infty$. One can then equip the category $SH(S)$ with the structure of a [[symmetric monoidal (∞,1)-category]] in such a way that the (∞,1)-functor $\Sigma_T^\infty$ can be promoted to a symmetric monoidal (∞,1)-functor. As such, $SH(S)$ is characterized by a [[universal property]]:

+-- {: .num_prop}
###### Proposition
Let $C$ be a [[locally presentable (∞,1)-category|locally presentable]] [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[(∞,1)-category]].
The (∞,1)-functor

$$ Fun^{\otimes, L}(SH(S),C) \to Fun^{\otimes} (Sm/S, C), \quad F\mapsto F\circ \Sigma_T^\infty(-)_+ $$

(where $\otimes$ means "symmetric monoidal" and $L$ means "colimit-preserving")
is [[fully faithful]] and its essential image consists of the symmetric monoidal (∞,1)-functors $F\colon Sm/S\to C$ satisfying:

* [[Nisnevich site|Nisevich excision]]
* $\mathbb{A}^1$-homotopy invariance
* _$T$-stability_: the [[homotopy cofiber]] of $F(\mathbb{G}_m)\to F(\mathbb{A}^1)$ is $\otimes$-invertible.

=--

This is [Robalo, Corollary 5.11](#Robalo).

### Stable motivic spheres

Because $T\simeq S^{2,1}$, the stable motivic spheres $S^{p,q}$ are defined for all $p,q\in\mathbb{Z}$.

All the other motivic spheres $S^V$, for $V$ a vector bundle on $S$, also become invertible in $SH(S)$. In fact, the [[Picard ∞-groupoid]] of $SH(S)$ receives a map from the [[algebraic K-theory]] of $S$. These invertible objects are all *exotic* in the sense that they are not equivalent to any of the categorical [[sphere]]s $S^n$ which exist in any [[stable (∞,1)-category]]. These exotic spheres play an important r&#244;le in the formalism of [[six operations]] in stable motivic homotopy theory (see [Ayoub](#Ayoub)).

### Cohomology theories

Any motivic spectrum $E\in SH(S)$ gives rise to a bigraded [[cohomology|cohomology theory]] for smooth $S$-schemes and more generally for motivic spaces:

$$ E^{p,q}(X) := [\Sigma^\infty_T X_+, \Sigma^{p,q} E], $$

as well as a bigraded homology theory:

$$ E_{p,q}(X) := [S^{p,q}, \Sigma^\infty_T X_+ \wedge E]. $$


## Main features


### The six operations

The categories $SH(S)$ for varying base scheme $S$ support a formalism of [[six operations]]. See [Ayoub](#Ayoub).

...

### Realization functors

...


### The slice filtration

The slice filtration is a filtration of $\mathrm{H}(S)$ and of $SH(S)$ which is analogous to the [[Postnikov tower in an (∞,1)-category|Postnikov filtration]] for [[(∞,1)-topoi]]. It generalizes the _coniveau filtration_ in [[algebraic K-theory]], the _fundamental filtration_ on [[Witt groups]], and the _weight filtration_ on [[mixed motives]].

In $SH(S)$, the layers of the slice filtrations (called the _slices_) are modules over the [motivic Eilenberg&#8211;Mac Lane spectrum](#MotivicCohomology) $H(\mathbb{Z})$. At least if $S$ is a [[field]] of characteristic zero, this is the same thing as an integral [[motive]]. The [[spectral sequences]] associated to the slice filtration are analogous to the [[Atiyah-Hirzebruch spectral sequence]]s in that their first page consists of [[motivic cohomology]] groups.

### The $\mathbb{A}^1$-Postnikov filtration

One can also consider the filtration on $\mathrm{H}(S)$ induced by the [[Postnikov tower in an (∞,1)-category|Postnikov filtration]] in the containing [[Nisnevich (∞,1)-topos]]. A motivic space is _$\mathbb{A}^1$-$n$-connected_ if it is $n$-connected as a Nisnevich (∞,1)-sheaf, and the _$\mathbb{A}^1$-homotopy groups_ $\pi_n^{\mathbb{A}^1}(X)$ and _$\mathbb{A}^1$-homology groups_ $H_n^{\mathbb{A}^1}(X)$ of a motivic space are its [[homotopy groups in an (∞,1)-topos|homotopy groups]] and [[homology groups]] as a Nisnevich (∞,1)-sheaf. 

Intuitively, $\mathbb{A}^1$-connectedness corresponds to the topological connectedness of the _real points_ rather than of the complex points. For example, $\mathbb{G}_m$ is not $\mathbb{A}^1$-connected, and $\mathbb{P}^1$ is $\mathbb{A}^1$-connected but not $\mathbb{A}^1$-simply connected.

There is a corresponding [[t-structure]] on the stable (∞,1)-category $SH(S)$ called the _homotopy t-structure_.


### Relation to the theory of motives

The stable motivic homotopy category $SH(S)$ is the basis for several definitions of the [[motive|derived category of mixed motives]] over $S$. See there for more details.

### Relation to the theory of symmetric bilinear forms

...


## Applications and examples

### $\mathbb{A}^1$-coverings and the $\mathbb{A}^1$-fundamental group

...

### The classification of surfaces

Asok and Morel used unstable $\mathbb{A}^1$-homotopy theory to solve the classification problem for rational smooth proper surfaces over [[algebraically closed field]]s. See [Asok-Morel](#AsokMorel).

...

### Euler classes and splittings of algebraic vector bundles

...


### Motivic cohomology {#MotivicCohomology}

Suppose that $S$ is a [[smooth scheme]] over a [[field]]. Then the [[motivic cohomology]] of smooth $S$-schemes is representable in $\mathrm{H}(S)$ and in $SH(S)$. If $A$ is an [[abelian group]] and $p\geq q\geq 0$, there exist a pointed motivic spaces $K(A(q),p)$, called a _motivic Eilenberg&#8211;MacLane space_, such that, for every $X\in Sm/S$,

$$ H^{p-r,q-s}(X,A) = [\Sigma^{r,s}X_+, K(A(q),p)]. $$

Voevodsky's [[cancellation theorem]] says that $\Omega_T K(A(q+1), p+2)\simeq K(A(q), p)$. It follows that the sequence of motivic spaces $K(A(n),2n)$ form a $T$-spectrum $H(A)$, called a _motivic Eilenberg&#8211;MacLane spectrum_, such that

$$ H^{p,q}(X,A) = [\Sigma_T^\infty X_+, \Sigma^{p,q} H(A)]. $$

If $R$ is a [[commutative ring]], the motivic spectrum $H(R)$ has a canonical structure of $E_\infty$-algebra in $SH(S)$ which induces the ring structure in motivic cohomology.

For $R=\mathbb{Q}$, $H(\mathbb{Q})$ is equivalent to the rational motivic sphere spectrum $S^0_{\mathbb{Q}}$ if and only if $-1$ is a sum of squares in the base field. Otherwise it is only a direct summand of $S^0_{\mathbb{Q}}$.

The stable (∞,1)-category of $H(\mathbb{Q})$-[[modules]] is equivalent to the [[derived category of mixed motives]]. See there for more details.

### Algebraic K-theory

Suppose that $S$ is a [[regular scheme]]. Then there exists a motivic $\mathbb{P}^1$-spectrum $KGL$ with the property that, for every $X\in Sm/S$,

$$ KGL^{p,q}(X) = K_{2q-p}(X), $$

where $K_*(X)$ are the [[algebraic K-theory]] groups of $X$ defined by [[Daniel Quillen|Quillen]]. In particular, $KGL$-cohomology is $(2,1)$-periodic: this is _Bott periodicity_ for algebraic K-theory.

The multiplicative structure of algebaric K-theory makes $KGL$ into a ring spectrum (up to homotopy), which comes from a unique structure of $E_\infty$-algebra (see [Naumann-Spitzweck-Ostvaer](#NSO11)).

Over non-regular schemes, the motivic spectrum $KGL$ is also defined and it represents Weibel's homotopy invariant version of [[algebraic K-theory]] (see [Cisinski13](#Cis13)).

### Algebraic cobordism

In analogy with the complex cobordism spectrum $MU$, Voevodsky defined the _[[algebraic cobordism]] spectrum_ $MGL \in SH(S)$ by

$$ MGL = colim_{n\to\infty} \Sigma_T^{\infty -n} V_n/V_n^\times, $$

where $V_n$ is the tautological vector bundle over the infinite Grassmannian of $n$-planes $Gr(n)$. More precisely, $Gr(n)$ is defined as the colimit in $\mathrm{H}(S)$ of the smooth $S$-schemes $Gr(n,k)$ as $k\to\infty$, and $V_n$ is similarly the colimit of the tautological vector bundles over $Gr(n,k)$.

Like $H(\mathbb{Z})$ and $KGL$, $MGL$ is an $E_\infty$ motivic ring spectrum

The spectrum $MGL$ was used by Voevodsky in his proof of the [[Bloch-Kato conjecture]]. It is also the starting point of [[chromatic motivic homotopy theory]].


### References

* [[Niko Naumann]], [[Markus Spitzweck]], [[Paul Arne Østvær]], _Existence and uniqueness of E-infinity structures on motivic K-theory spectra_, ([arXiv](http://arxiv.org/abs/1010.3944))
{#NSO11}

* [[Denis-Charles Cisinski]], _Descente par &#233;clatements en K-th&#233;orie invariante par homotopie_, Ann. of Math. (2) 177 (2013), no. 2, pp. 425&#8211;448 ([pdf](http://hal.archives-ouvertes.fr/docs/00/52/56/40/PDF/descente3.pdf))
{#Cis13}

* [[Aravind Asok]], [[Fabien Morel]], _Smooth varieties up to A1-homotopy and algebraic h-cobordisms_, Adv. Math. 227 (5) (2011),  pp. 1990-2058 ([arXiv](http://arxiv.org/abs/0810.0324))
{#AsokMorel}


## Related concepts

* [[equivariant homotopy theory]]

* [[motive]]
* [[motivic cohomology]]

* [[B1-homotopy theory]]
* There is an analog of $\mathbb{A}^1$-homotopy theory for other geometries. The extra left adjoint on a [[cohesive (infinity,1)-topos]] may realize the localization at an abstract [[continuum]] [[line object]]. See at _[[cohesion]]_ for more details.


## References

The original "textbook" references are

* [[Fabien Morel]], [[Vladimir Voevodsky]], _$\mathbb{A}^1$-homotopy theory of schemes_ K-theory, 0305 ([web](http://www.math.uiuc.edu/K-theory/0305/) [pdf](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf))

* [[Fabien Morel]], _$\mathbb{A}^1$-algebraic topology over a field_, LNM 2052, 2012, ([pdf](http://www.mathematik.uni-muenchen.de/~morel/A1TopologyLNM.pdf))

Readable introductions to the subject are:

* [[Marc Levine]], _Motivic Homotopy Theory_, Milan j. math (2008), ([pdf](http://www.math.unam.mx/javier/levine.pdf))

* [[Fabien Morel]], _An introduction to $\mathbb{A}^1$ homotopy theory_, ICTP Trieste July 2002 ([directory](http://publications.ictp.it/lns/vol15/vol15toc.html), [pdf](http://www.ictp.it/%7Epub_off/lectures/lns015/Morel/Morel.pdf), [ps](http://www.ictp.it/%7Epub_off/lectures/lns015/Morel/Morel.ps)).

The [[model structure on simplicial presheaves]] on the [[Nisnevich site]] and its [[homotopy localization]] to [[A1-homotopy theory]] is in

* [[Rick Jardine]], _Motivic spaces and the motivic stable category_ 
  ([pdf](http://www.aimath.org/WWN/motivesdessins/motivic.pdf))

For more on the general procedure see [[homotopy localization]].

The universal property of $SH(S)$ is proved in

* [[Marco Robalo]], _Noncommutative Motives I: A Universal Characterization of the Motivic Stable Homotopy Theory of Schemes_, 2013 ([pdf](http://arxiv.org/pdf/1206.3645v3.pdf))
{#Robalo}

For the formalism of [[six operations]] see

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique_, Ast&#233;risque 314-315 (2008) ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))
{#Ayoub}

* [[Vladimir Voevodsky]], [[Pierre Deligne]], _Voevodsky's lectures on cross functors_ ([pdf](http://mat.uab.cat/~kock/tmp/delnotes01.pdf))

The slice filtration was defined in

* [[Vladimir Voevodsky]], _Open problems in the stable motivic homotopy theory_ K-theory, 0392 ([web](http://www.math.uiuc.edu/K-theory/0392/) [pdf](http://www.math.uiuc.edu/K-theory/0392/nowmovo.pdf))

Discussion related to [[étale homotopy]] is in 

* [[Daniel Isaksen]], _&#201;tale realization of the $\mathbb{A} ^1$-homotopy theory of schemes_, Advances in Mathematics 184 (2004) 

[[!redirects A1-homotopy]]
[[!redirects A1 homotopy]]
[[!redirects A1-homotopy theory]]
[[!redirects A1 homotopy theory]]
[[!redirects A1-homotopy category]]
[[!redirects A1 homotopy category]]
[[!redirects stable motivic homotopy theory]]
[[!redirects motivic homotopy category]]
[[!redirects stable motivic homotopy category]]
[[!redirects motivic space]]
[[!redirects motivic spaces]]
[[!redirects motivic spectrum]]
[[!redirects motivic spectra]]
