[[!redirects Euclidean topological infinity-groupoid]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}


## Idea 

A _Euclidea-topological $\infty$-groupoid_ is an [[∞-groupoid]] equipped with  [[cohesive (∞,1)-topos|cohesion]] in the form of [[Euclidean topology]].


## Definition

Let [[CartSp]]${}_{top}$ be the [[site]] of [[open ball]]s with the [[good open cover]] [[coverage]].

+-- {: .un_defn}
###### Definition

Define

$$
  ETop \infty Grpd := (\infty,1)Sh(CartSp_{top})
$$

to be the [[(∞,1)-category of (∞,1)-sheaves]] on $CartSp_{top}$.

=--


+-- {: .un_prop}
###### Proposition


The [[(∞,1)-topos]] $ETop \infty Grpf$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

The site [[CartSp]]${}_{top}$ an  [[∞-cohesive site]].  See there for details.

=--


## Structures in the cohesive $(\infty,1)$-topos $ETop \infty Grpd$

We discuss what some of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">Structures in a cohesive (∞,1)-topos</a> look like in the model $ETop \infty Grpd$. 

As usual, write

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : 
  ETop \infty Grpd
    \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
$$

for the defining quadruple of [[adjoint (∞,1)-functor]]s that refine the [[global section]] [[(∞,1)-geometric morphism]] to [[∞Grpd]].


### Geometric homotopy and Galois theory {#GeometricHomotopy}



+-- {: .un_prop #FundGroupoidOfParacompact}
###### Proposition

Let $X$ be a [[paracompact topological space]] naturally regarded as an object $X \in Top \hookrightarrow ETop \infty Grpd$. Then $\Pi(X) \in \infty Grpd$ is equivalent to the standard [[fundamental ∞-groupoid]] of a [[topological space]] that is presented by the [[singular simplicial complex]] $Sing X$

$$
  \Pi(X) \simeq Sing X
  \,.
$$

Equivalently, under [[geometric realization]] $\mathbb{L}|-| : \infty Grpd \to Top$ we have that there is a [[weak homotopy equivalence]]

$$
  X \simeq |\Pi(X)|
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

By the discussion at [[∞-cohesive site]] we have an equivalence $\Pi(-) \simeq \mathbb{L} \lim_\to$ to the [[derived functor]] of the [[sSet]]-[[colimit]] functor $\lim_\to : [CartSp^{op}, sSet]_{proj,loc} \to sSet_{Quillen}$. 

To compute this derived functor, notice that every [[paracompact topological space]] $X$ admits a [[good open cover]] (see there) $\{U_i \to X\}$ by [[Cartesian space]]s. This means that the [[Cech nerve]] $C(\coprod_i U_i \to X) \in [CartSp^{op}, sSet]$ is degreewise a [[coproduct]] of [[representable functor|representable]]s, hence a [[split hypercover]]. By the discussion at [[model structure on simplicial presheaves]] we have that in this case the canonical morphism

$$
  C(\coprod_i U_i \to X) \to X
$$

is a cofibrant [[resolution]] of $X$ in $[CartSp^{op}, sSet]_{proj,loc}$. Accordingly we have

$$
  \Pi(X) \simeq (\mathbb{L} \lim_\to) (X) \simeq \lim_\to C(\coprod_i U_i \to X)
  \,.
$$

Using the [[equivalence of categories]] $[CartSp^{op}, sSet] \simeq [\Delta^{op}, [CartSp^{op}, Set]]$ and that [[colimit]]s in [[presheaf categories]] are computed objectwise and finally using that the colimit of a [[representable functor]] is the point (an incarnation of the [[Yoneda lemma]]) we have that $\Pi(X)$ is presented by the [[Kan complex]] that is obtained by contracting in the [[Cech nerve]] $C(\coprod_i U_i)$ each open subset to a point.

The classical [[nerve theorem]] then asserts that this implies the claim.

=--


+-- {: .un_remark}
###### Remark

We may regard [[Top]] itself as a [[cohesive (∞,1)-topos]]. $(\Pi_{Top}\dashv Disc_{Top} \dashv \Gamma_{Top} \dashv coDisc_{Top}) Top \stackrel{\simeq}{\to} \infty Grpd$. This is discuseed at [[discrete ∞-groupoid]].

Using this the above proposition may be stated as saying that for $X$ a [[paracompact topological space]] we have

$$
  \Pi_{ETop\infty Grpd}(X) \simeq \Pi_{Top}(X)
  \,.
$$

=--


+-- {: .un_prop}
###### Corollary

For $X_\bullet$ a [[proper simplicial topological space]] that is degreewise [[paracompact topological space|paracompact]], regarded naturally as an object $X_\bullet \in Top^{\Delta^{op}} \to ETop \infty Grpd$ we have that the intrinsic $\Pi(X_\bullet) \in \infty Grpd$ coincides under [[geometric realization]] $\mathbb{L}|-| : \infty Grpd \stackrel{\simeq}{\to} Top$ with the ordinary [[geometric realization of simplicial topological spaces]] $|X_\bullet|_{Top^{\Delta^{op}}}$

$$
  |\Pi(X_\bullet)| \simeq |X_\bullet|_{Top^{\Delta^{op}}}
  \,.
$$

=--


+-- {: .proof}
###### Proof

Write $Q$ for Dugger's cofibrant replacement functor on $[CartSp^{op}, sSet]_{proj,loc}$ (discussed at [[model structure on simplicial presheaves]]). On a simplicially constant simplicial presheaf $X$ it is given by 

$$
 Q X := \int^{[n] \in \Delta} \Delta[n] \cdot 
    \left(
      \coprod_{U_0 \to \cdots \to U_n \to X} U_0
    \right)
   \,,
$$

where the [[coproduct]] in the integrand of the [[coend]] is over all sequences of morphisms from [[representable functor|representable]]s $U_i$ to $X$ as indicated. On a general [[simplicial presheaf]] $X_\bullet$ it is given by

$$
  Q X_\bullet := \int^{[k] \in \Delta} \Delta[k] \cdot Q X_k
  \,,
$$ 

which is the simplicial presheaf that over any $V \in CartSp$ takes as value the [[diagonal]] of the [[bisimplicial set]] whose $(n,r)$-entry is
$\coprod_{U_0 \to \cdots \to U_n \to X_k} CartSp(V,U_0)$.

Since [[coend]]s are special [[colimit]]s the colimit functor itself commutes with them and we find

$$
  \begin{aligned}
     \Pi(X_\bullet) 
     & \simeq 
      (\mathbb{L} \lim_\to) X_\bullet
     \\
     & \simeq \lim_\to Q X_\bullet
     \\
      & \simeq \int^{[n] \in \Delta} \Delta[k] \cdot \lim_\to (Q X_k)
    \,.
  \end{aligned}
$$

By the discussion at [[Reedy model structure]] this [[coend]] is a [[homotopy colimit]] over the simplicial [[diagram]] $\lim\to Q X_\bullet : \Delta \to sSet_{Quillen}$

$$
  \cdots \simeq hocolim_\Delta \lim_\to Q X_\bullet
  \,.
$$

By the [above proposition](#FundGroupoidOfParacompact) we have weak equivalences $\lim_\to Q X_k \simeq (\mathbb{L} \lim_\to) X_k \simeq Sing X_k$, so that

$$
  \begin{aligned}
    \cdots &\simeq hocolim_\Delta Sing X_k
    \\
     & \simeq \int^{[k] \in \Delta} \Delta[k] \cdot Sing X_k
    \\
     & \simeq diag Sing(X_\bullet)_\bullet
  \end{aligned}
  \,.
$$

By the discussion at [[geometric realization of simplicial topological spaces]], this maps to the [[homotopy colimit]] of the simplicial topological space $X_\bullet$, which is just its geometric realizaiton if it is proper. 

=--

### Cohomology

+-- {: .un_theorem }
###### Theorem

For [[paracompact space|paracompact]] $X$ we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  ETop \infty Grpd(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   ETop \infty Grpd(X, LConst A)
$$

=--

+-- {: .proof}
###### Proof

By the above (...).

=--




### Path $\infty$-groupoid

(...)

## Localization to $Top$

### Homotopy invariance and topological spaces

The sub-[[(∞,1)-category]] [[∞-stack]]s on [[Top]] (even on [[Diff]]) that are homotopy invariant is equivalent to plain [[∞Grpd]]. 

**Idea**

A central result about the [[(∞,1)-topos]] $Sh_{(\infty,1)}(Top)$ of [[∞-stack]]s on [[Top]] is that the [[homotopy localization]] is equivalent to [[Top]] itself

$$
  Sh_{(\infty,1)}(Top)^I \simeq Top
  \,.
$$

A discussion of this is in (the nice but not quite finished) ([Dugger](#Dugger)).

In fact, this is true even for [[Lie ∞-groupoid]]s, i.e. [[∞-stack]]s on [[Diff]]: the homotopy invariant ones model plain [[topological space]]s.

This provides a useful resolution of [[topological space]]s that often helps to disentangle the two different roles played by a topological space: on the one hand as a model for an [[∞-groupoid]], in the other as a [[locale]].

**Details**

Let $SPSh(Diff)^{loc}$ be the local [[model structure on simplicial presheaves]] obtained by left [[Bousfield localization of model categories|Bousfield localization]] at the [[Cech nerve]]s of 
[[Cech cover]]s with respect to the standard [[Grothendieck topology]] on [[Diff]]. This is a [[models for ∞-stack (∞,1)-toposes|model for ∞-stacks]] on [[Diff]].

Let $SPSh(Diff)^{loc}_I$ be furthermore the left [[Bousfield localization of model categories|Bousfield localization]]
at the set of projection morphisms out of [[product]]s of the form $X \times \mathbb{R} \to X$ for all $X \in Diff$. The $\infty$-stacks that are [[local object]]s with respect
to these morphisms are the _homotopy invariant_ $\infty$-stacks, so this localization models the [[(∞,1)-topos]] of homotopy invariant
$\infty$-stacks on $Diff$.

There is a [[adjunction]]

$$
  L : SSet \stackrel{\leftarrow}{\to} SPSh(Diff) : R
$$

where $L$ sends a simplicial set to the simplicial presheaf constant on that simplicial
set, and where evaluates a simplicial presheaf on the manifold that is the [[point]]. 

**Theorem (Dugger)**

This adjunction $(L \dashv R)$ is a [[Quillen equivalence]] with respect to the  standard [[model structure on simplicial sets]] on the left and the above model structure $SPSh(Diff)_{loc}^I$ on the right.




## References

Some discussion of the $(\infty,1)$-category of $(\infty,1)$-sheaves on the category of manifolds and its restriction to open balls is in:

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))
{#Dugger}

[[!redirects Euclidean topological ∞-groupoid]]

[[!redirects Euclidean topological infinity-groupoids]]
[[!redirects Euclidean topological ∞-groupoids]]


[[!redirects Euclidean-topological ∞-groupoid]]
[[!redirects Euclidean-topological infnity-groupoid]]


[[!redirects Euclidean-topological infinity-groupoids]]
[[!redirects Euclidean-topological ∞-groupoids]]


[[!redirects ETop∞Grpd]]

[[!redirects topological infinity-groupoid]]


[[!redirects topological ∞-groupoid]]
[[!redirects topological ∞-groupoids]]

[[!redirects ?TopGrpd]]

[[!redirects continuous infinity-groupoid]]
[[!redirects continuous infinity-groupoids]]
[[!redirects continuous ∞-groupoid]]
[[!redirects continuous ∞-groupoids]]

