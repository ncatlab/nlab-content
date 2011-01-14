
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

## Properties


+-- {: .un_prop}
###### Proposition


The [[(∞,1)-topos]] $ETop \infty Grpf$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

The site [[CartSp]]${}_{top}$ an  [[∞-cohesive site]].  See there for details.

=--

+-- {: .un_def}
###### Definition

Write $Top_1$ for the 1-[[category]] of [[topological spaces]] and continuous maps. There is a canonical functor

$$
  i : Top_1 \to \tau_{\leq 0}ETop\infty Grpd \hookrightarrow  ETop\infty Grpd
$$

given by sending a topological space $X$ to the [[sheaf]] on [[CartSp]]${}_{top}$ externally represented by $X$ under the embedding $CartSp_{top} \hookrightarrow Top$:

$$
  X : U \mapsto Hom_{Top}(U,X)
  \,.
$$

=--

On [[topological manifold]]s this is a [[full and faithful functor]].


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

We discuss the realization of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] in $ETop \inft Grpd$.

+-- {: .un_prop #FundGroupoidOfParacompact}
###### Proposition

Let $X$ be a [[paracompact topological space]] naturally regarded as an object $X \in Top_1 \stackrel{i}{\hookrightarrow} ETop \infty Grpd$. Then $\Pi(X) \in \infty Grpd$ is equivalent to the standard [[fundamental ∞-groupoid]] of a [[topological space]] that is presented by the [[singular simplicial complex]] $Sing X$

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

### Cohomology {#Cohomology}

We dicuss aspects of the intrinsic [[cohomology]] of $E Top \infty Grpd$.


+-- {: .un_def }
###### Definition

Let $A \in $ [[∞Grpd]] be any [[∞-groupoid]]. Write $|A| \in $ [[Top]] for its [[geometric realization]]. For $X$ any [[topological space]], the [[nonabelian cohomology]] of $X$ with coefficients in $A$ is the set of [[homotopy]] classes of maps $X \to |A|$

$$ 
  H_{Top}(X,A) := \pi_0 Top(X,|A|)
  \,.
$$

We say $Top(X,|A|)$ itself is the [[cocycle]] [[∞-groupoid]] for $A$-valued cohomology on $X$.

Similarly, for $X,A \in ETop \infty Grpd$ two objects, write

$$
  H_{ETop\infty Grpd}(X,A) := \pi_0 ETop\infty Grpd(X,A)
$$

for the intrinsic [[cohomology]] of $ETop \infty Grpd$ on $X$ with coefficients in $A$.

=--

+-- {: .un_prop }
###### Proposition

Let $A \in $ [[∞Grpd]], write $Disc A \in ETop \infty Grpd$ for the corresponding [[discrete ∞-groupoid|discrete topological ∞-groupoid]]. Let $X \in Top_1 \stackrel{i}{\hookrightarrow} ETop \infty Grpd$ be [[paracompact topological space|paracompact]]. Then we have an [[isomorphism]] on cohomology sets

$$ 
  H_{Top}(X,A) \simeq H_{ETop\infty Grpd}(X,Disc A)
$$

and in fact an [[equivalence in an (∞,1)-category|equivalence]] of [[cocycle]] [[∞-groupoid]]s

$$
  Top(X,|A|) \simeq ETop\infty Grpd(X, Disc A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the $(\Pi \dashv Disc)$-[[adjunction]] of the [[locally ∞-connected (∞,1)-topos]] $ETop \infty Grpd$ we have

$$
  ETop\infty Grpd(X, Disc A) \simeq \infty Grpd(\Pi(X), A)
  \underoverset{\simeq}{|-|}{\to}
  Top(|\Pi X|, |A|)
  \,.
$$

From this the claim follows by the [above proposition](#FundGroupoidOfParacompact).

=--




### Path $\infty$-groupoid

We discuss concrete presentations of the canonical path $\infty$-groupoid functor 
$\mathbf{\Pi} : ETop\infty Grpd \to ETop\infty Grpd$ in terms of actual paths.

By the [above discussion](#GeometricHomotopy) a fairly explicit presentaiton of $\Pi(X)$ is given by forming Dugger's cofibrant replacement $Q X$ and then contracting all representables to points, equivalently forming degreewise the coproduct $\lim\limits_\to Q X$. In terms of this presentation the _constant path inclusion_ morphism $X \to \mathbf{\Pi}(X)$ (the [[unit of an adjunction|unit]] of the $(\Pi \dashv Disc)$-adjunction) is presented by the canonical projection $Q X \to \lim\limits_\to Q X$ that degreewise projects every representable to the point. One deficiency of this presentation is that it is far from being a cofibration. However, in order to compute the de Rham space object $\mathbf{\Pi}_{dR} X := \mathbf{\Pi}(X) \coprod_X *$ it is useful to have the _constant path inclusion morphism_ be prsented by a cofibration.
We now consider a different presentation of $\mthbf{\Pi}(X)$ in terms of actual paths that does achieve this and which does live up to the term _constant path inclusion_ .


+-- {: .un_def }
###### Definition

For $V \in $ [[CartSp]] write $\mathbf{Sing} U \in [CartSp^{op}, sSet]$ for the [[simplicial presheaf]] given by

$$
  \mathbf{Sing}V : (U, [n]) \mapsto  Hom_{Top}(U \times \Delta^n, V)
  \,,
$$

where $\Delta^n \in Top_1$ is the standard topological $n$-[[simplex]].

This extends to a functor

$$
  \mathbf{Sing} : CartSp \to [CartSp^{op}, sSet] 
  \,.
$$

Let

$$
  i_V : V \to \mathbf{Sing} V
$$

the morphism of simplicial presheaves induced in degree $k$ be precomposition with the projection $U \times \Delta^k \to U$.

=--

+-- {: .un_prop }
###### Observation

In the injective local [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{inj,loc}$ we have for each $V \in CartSp$ that the composite

$$
  V \hookrightarrow \mathbf{Sing}V \stackrel{\simeq}{\to} *
$$

is a factorization of the terminal morphism into a cofibration followed by a weak equivalence.

=--

+-- {: .proof}
###### Proof

Using the standard lifting properties of the [[model structure on topological spaces]]  we have that all lifts $\sigma$ as indicated in

$$
  \array{
     U \times \partial \Delta^n &\to& V
     \\
     \downarrow & \nearrow_{\sigma}
     \\
     U \times \Delta^n
  }
$$

exist, since $V \times \partial \Delta^n \to V \times \Delta^n$ is a cofibation in $Top_{Quillen}$ and for $V$ a [[Cartesian space]] the terminal morphism $V \to *$ is an acyclic fibration.

This shows that $\mathbf{Sing} V \to *$ is a weak equivalence of simplicial sets over each $U$, hence is a weak equivalence of simplicial presheaves.

The morphism $i_V : V \to \mathbf{Sing} V$ includes in degree $k$ precisely the maps $U \times \Delta^k \to V$ that are constant on $\Delta^n$ into the set of all continuous maps, hence this is degreewise a monomorphism, hence objectwise a cofibration of simplicial sets, hence a cofibration in $[CartSp^{op}, sSet]_{inj,loc}$.

=--

(...)


## Homotopy localization


We discuss that the[[homotopy localization]] of topological $\infty$-groupoids reproduces [[Top]] $\simeq$ [[∞Grpd]], following ([Dugger](#Dugger)).


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

Some discussion of the $(\infty,1)$-category of $(\infty,1)$-sheaves on the category of manifolds and its restriction to open balls and a discussion of its homotopy localization is in:

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

[[!redirects Euclidean topological infinity-groupoid]]
