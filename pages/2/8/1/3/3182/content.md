
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

# Contents
* table of contents 
{:toc}

## Idea 

A _Euclidean-topological $\infty$-groupoid_ is an [[∞-groupoid]] equipped with  [[cohesive (∞,1)-topos|cohesion]] in the form of [[Euclidean topology]].


## Definition


+-- {: .un_defn}
###### Definition

Let [[CartSp]]${}_{top}$ be the [[site]] whose underlying [[category]] has as [[objects]] the [[Cartesian space]]s $\mathbb{R}^n$, $n \in \mathbb{N}$ equipped with the [[Euclidean topology]] and as [[morphism]]s the [[continuous maps]] between them; and whose [[coverage]] is given by [[good open cover]]s.

=--

+-- {: .un_defn}
###### Definition

Define

$$
  ETop \infty Grpd := (\infty,1)Sh(CartSp_{top})
$$

to be the [[(∞,1)-category of (∞,1)-sheaves]] on $CartSp_{top}$.
=--


## Properties

+-- {: .un_prop #ETopInfGrpdAsCohesiveTopos}
###### Proposition


The [[(∞,1)-topos]] $ETop \infty Grpf$ is a [[cohesive (∞,1)-topos]].
=--

+-- {: .proof}
###### Proof

The site [[CartSp]]${}_{top}$ an  [[∞-cohesive site]].  See there for details.

=--

+-- {: .un_def}
###### Definition

We say that $ETop \infty Grpd$ defines **Euclidean-topological cohesion**. An object in $ETop \infty Grpd$ we call a **Euclidean-topological $\infty$-groupoid**.

=--

+-- {: .un_prop #ToposOverTopMfd}
###### Proposition

Write [[TopMfd]] for the category of [[topological manifold]]s. This becomes a [[large site]] with the [[open cover]] [[coverage]]. We have an [[equivalence of (∞,1)-categories]]

$$
  ETop\infty Grpd
  \simeq
  \hat Sh_{(\infty,1)}(TopMfd)
$$

with the [[hypercompletion]] of the [[(∞,1)-category of (∞,1)-sheaves]] on [[TopMfd]].

=--

+-- {: .proof}
###### Proof

Since every [[topological manifold]] admits an [[open cover]] by [[open balls]] [[homeomorphic]] to a [[Cartesian space]] it follows that [[CartSp]]${}_{top}$ is a [[dense sub-site]] of $TopMfd$. Accordingly the [[categories of sheaves]] are [[equivalence of categories|equivalent]]

$$
  Sh(CartSp_{top}) \simeq Sh(TopMfd)
  \,.
$$

By the discussion at [[model structure on simplicial sheaves]] it follows that the [[hypercomplete (∞,1)-topos]]es  over these sites are [[equivalence of (∞,1)-categories|equivalent]]

$$
  \hat Sh_{(\infty,1)}(CartSp_{top})
  \simeq
  \hat Sh_{(\infty,1)}(TopMfd)  
 \,.
$$

But by the [above proposition](#ETopInfGrpdAsCohesiveTopos) we have that before [[hypercompletion]] $Sh_{(\infty,1)}(CartSp_{top})$ is [[cohesive (∞,1)-topos|cohesive]]. This means that it is in particular a [[local (∞,1)-topos]]. By the discussion there, this means that it already coincides with its [[hypercompletion]], $Sh_{(\infty,1)}(CartSp_{top}) \simeq \hat Sh_{(\infty,1)}(CartSp_{top})$.

=--

+-- {: .un_def}
###### Definition

Write $Top_1$ for the 1-[[category]] of [[Hausdorff space|Hausdorff]] [[topological spaces]] and continuous maps. There is a canonical functor

$$
  j : Top_1 \to \tau_{\leq 0}ETop\infty Grpd \hookrightarrow  ETop\infty Grpd
$$

given by sending a topological space $X$ to the 0-[[truncated]]
[[(∞,1)-sheaf]] (=  [[sheaf]]) on [[CartSp]]${}_{top}$ externally represented by $X$ under the embedding $CartSp_{top} \hookrightarrow Top$:

$$
  j(X) : (U \in CartSp_{top}) \mapsto Hom_{Top}(U,X)
  \in Set \hookrightarrow \infty Grpd
  \,.
$$
=--

+-- {: .un_prop}
###### Proposition

The functor $j$ exhibits [[TopMfd]] as a full [[sub-(∞,1)-category]] of $ETop\infty Grpd$

$$
  TopMfd \hookrightarrow ETop\infty Grpd
  \,.
$$

=--

+-- {: .proof}
###### Proof

With the [above proposition](#ToposOverTopMfd) this follows directly by the [[(∞,1)-Yoneda lemma]].

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

We discuss the realization of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] in $ETop \inft Grpd$.

+-- {: .un_prop #FundGroupoidOfParacompact}
###### Proposition

Let $X$ be a [[paracompact topological space]] such that that $X$ admits a [[good open cover]] by [[open ball]]s (for instance a [[paracompact manifold]]). 

Then $\Pi(X) := \Pi(i(X)) \in \infty Grpd$ is equivalent to the standard [[fundamental ∞-groupoid]] of a [[topological space]] that is presented by the [[singular simplicial complex]] $Sing X$

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

To compute this derived functor, let $\{U_i \to X\}$ be a [[good open cover]] by [[open balls]], hence [[homeomorphic]]ally by [[Cartesian space]]. By goodness of the cover the [[Cech nerve]] $C(\coprod_i U_i \to X) \in [CartSp^{op}, sSet]$ is degreewise a [[coproduct]] of [[representable functor|representable]]s, hence a [[split hypercover]]. By the discussion at [[model structure on simplicial presheaves]] we have that in this case the canonical morphism

$$
  C(\coprod_i U_i \to X) \to X
$$

is a cofibrant [[resolution]] of $X$ in $[CartSp^{op}, sSet]_{proj,loc}$. Accordingly we have

$$
  \Pi(X) \simeq (\mathbb{L} \lim_\to) (X) \simeq \lim_\to C(\coprod_i U_i \to X)
  \,.
$$

Using the [[equivalence of categories]] $[CartSp^{op}, sSet] \simeq [\Delta^{op}, [CartSp^{op}, Set]]$ and that [[colimit]]s in [[presheaf categories]] are computed objectwise and finally using that the colimit of a [[representable functor]] is the point (an incarnation of the [[Yoneda lemma]]) we have that $\Pi(X)$ is presented by the [[Kan complex]] that is obtained by contracting in the [[Cech nerve]] $C(\coprod_i U_i)$ each open subset to a point.

The classical [[nerve theorem]] asserts that this implies the claim.
=--

+-- {: .un_remark}
###### Remark

We may regard [[Top]] itself as a [[cohesive (∞,1)-topos]]. $(\Pi_{Top}\dashv Disc_{Top} \dashv \Gamma_{Top} \dashv coDisc_{Top}) Top \stackrel{\simeq}{\to} \infty Grpd$. This is discussed at [[discrete ∞-groupoid]].

Using this the above proposition may be stated as saying that for $X$ a [[paracompact topological space]] that admits a [[good open cover]] we have

$$
  \Pi_{ETop\infty Grpd}(X) \simeq \Pi_{Top}(X)
  \,.
$$

=--

+-- {: .un_prop}
###### Corollary

Let $X_\bullet$ a [[proper simplicial topological space]] that is degreewise [[paracompact topological space|paracompact]] and degreewise admitting a [[good open cover]], regarded naturally as an object $X_\bullet \in Top^{\Delta^{op}} \to ETop \infty Grpd$. 

We have that the intrinsic $\Pi(X_\bullet) \in \infty Grpd$ coincides under [[geometric realization]] $\mathbb{L}|-| : \infty Grpd \stackrel{\simeq}{\to} Top$ with the ordinary [[geometric realization of simplicial topological spaces]] $|X_\bullet|_{Top^{\Delta^{op}}}$

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

which is the simplicial presheaf that over any $\mathbb{R}^n \in CartSp$ takes as value the [[diagonal]] of the [[bisimplicial set]] whose $(n,r)$-entry is
$\coprod_{U_0 \to \cdots \to U_n \to X_k} CartSp_{top}(\mathbb{R}^n,U_0)$.

Since [[coend]]s are special [[colimit]]s, the colimit functor itself commutes with them and we find

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

By the discussion at [[Reedy model structure]] this [[coend]] is a [[homotopy colimit]] over the simplicial [[diagram]] $\lim_\to Q X_\bullet : \Delta \to sSet_{Quillen}$

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


### Cohomology and principal $\infty$-bundles
{#Cohomology}

We dicuss aspects of the intrinsic [[cohomology]] of $E Top \infty Grpd$ and of the [[principal ∞-bundle]]s that it classifies.

+-- {: .un_def }
###### Definition

Let $A \in $ [[∞Grpd]] be any [[discrete ∞-groupoid]]. Write $|A| \in $ [[Top]] for its [[geometric realization]]. For $X$ any [[topological space]], the [[nonabelian cohomology]] of $X$ with coefficients in $A$ is the set of [[homotopy]] classes of maps $X \to |A|$

$$ 
  H_{Top}(X,A) := \pi_0 Top(X,|A|)
  \,.
$$

We say $Top(X,|A|)$ itself is the [[cocycle]] [[∞-groupoid]] for $A$-valued [[nonabelian cohomology]] on $X$.

Similarly, for $X, \mathbf{A} \in ETop \infty Grpd$ two e-topological $\infty$-groupoids, write

$$
  H_{ETop}(X,\mathbf{A}) := \pi_0 ETop\infty Grpd(X,\mathbf{A})
$$

for the intrinsic [[cohomology]] of $ETop \infty Grpd$ on $X$ with coefficients in $\mathbf{A}$.

=--


+-- {: .un_prop }
###### Proposition

Let $A \in $ [[∞Grpd]], write $Disc A \in ETop \infty Grpd$ for the corresponding [[discrete ∞-groupoid|discrete topological ∞-groupoid]]. Let $X \in Top_1 \stackrel{i}{\hookrightarrow} ETop \infty Grpd$ be a [[paracompact topological space]] regarded as a 0-[[truncated]] 
Euclidean-topological $\infty$-groupoid. 

We have an [[isomorphism]] of cohomology sets

$$ 
  H_{Top}(X,A) \simeq H_{ETop}(X,Disc A)
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



+-- {: .un_prop #GeometricRealizationOfHomotopyFibers}
###### Proposition

Let $X$ and $G$ be degreewise [[paracompact topological space|paracompact]] [[simplicial topological space]]s with good open covers. Let moreover $G$ be a well-sectioned topological [[simplicial group]]. Regard both as object in $E Top \infty Grpd$ in the canonical way. Write $\mathbf{B}G$ for  [[delooping]] of the [[∞-group]]-object $G$ in $ETop \infty Grpd$.

Then the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|intrinsic fundamental (∞,1)-groupoid functor]] $\Pi : ETop \infty Grpd$ preserves [[homotopy fiber]]s of all morphisms of the form $X \to \mathbf{B}G$.


More in detail, if $P \to X$ is the $G$-[[principal ∞-bundle]] in $ETop \infty Grpd$ classified by the [[cocycle]] $X \to \matbf{B}G$ then $|\Pi(P)| \to |\Pi(X)|$ is the $|G|$-[[principal ∞-bundle]] in [[Top]] classified by $|\Pi(X)| \to B |G|$.


=--

+-- {: .proof}
###### Proof


Write, as usual for [[simplicial group]]s, $\mathbf{B}G := \bar W G$ for its <a href="http://ncatlab.org/nlab/show/simplicial+group#Delooping">delooping</a>. Write $W G$ for the <a href="http://nlab.mathforge.org/nlab/show/simplicial+group#UniversalSimplicialBundle">universal simplicial G-bundle</a>.  This is a [[resolution]] of the point inclusion $* \to \mathbf{B}G$ by a fibration in $[CartSp^{op}, sSet]_{proj}$

Therefore the ordinary [[pullback]]

$$
  \array{
    P_\bullet &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X_\bullet &\to& \bar W G
  }
$$

of topological spaces and hence (since the [[Yoneda embedding]] preserves [[limit]]s) of [[simplicial presheaves]] on [[CartSp]]${}_{top}$ is a [[homotopy pullback]] (as discussed there) and hence $P = X \times_{\bar W G} W G$ is a presentation of the [[homotopy fiber]] of $X \to \mathbf{B}G$ in the [[(∞,1)-category of (∞,1)-presheaves]] over $CartSp$ and hence by [[exact (∞,1)-functor|left exactness]] of [[(∞,1)-sheafification]] also in $ETop\infty Grpd$.

In ([StevensonRoberts](#StevensonRoberts)) it is shown that under [[geometric realization of simplicial topological spaces]] the <a href="http://nlab.mathforge.org/nlab/show/simplicial+group#UniversalSimplicialBundle">universal simplicial G-bundle</a> $W G \to \bar W G$ maps to the universal $|G|$-principal topological bundle $E |G| \to B |G|$ over the [[topological group]] $|G|$ obtained by [[geometric realization of simplicial topological spaces|geometric realization]] of $G$. This is a [[resolution]] of the point inclusion $* \to B|G|$ in [[Top]].

But [[geometric realization of simplicial topological spaces]] preserves (as discussed there) ordinary [[pullback]]s. Therefore we have that also 

$$
  \array{
    |P| &\to& E |G|
    \\
    \downarrow && \downarrow
    \\
    |X| &\to& B |G|
  }
$$

is a pullback, hence a [[homotopy pullback]], and therefore that $|P|$ is a model for the [[homotopy fiber]] of $|X| \to B |G|$ in [[Top]] $\simeq$ [[∞Grpd]]. 

In summary we have that on simplicial topological spaces $X \to \mathbf{B}G$ as in the asumptions, geometric realization preserves homotopy fibers. But by the [above proposition](#FundGroupoidOfParacompact) the [[(∞,1)-functor]] $\Pi$ is modeled on these morphisms by geometric realization, hence the claim follows.

=--

### Universal coverings and geometric Whitehead towers {#WhiteheadTowers}

We discuss <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Coverings">geometric Whitehead towers</a> in $ETop\infty Grpd$.

+-- {: .un_prop}
###### Proposition

Let $X$ be a [[pointed object|pointed] [[paracompact topological space]] that admits a [[good open cover]].  Then its ordinary [[Whitehead tower]] 
$* \to \cdots X^{(2)} \to X^{(1)} \to X^{(0)} = X$ in [[Top]] coincides with the image under the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|intrinsic fundamental ∞-groupoid functor]] $|\Pi(-)|$ of its [[Whitehead tower in an (∞,1)-topos|geometric Whitehead tower]] 
$X^{\mathbf{(\infty)}} \to \cdots X^{\mathbf{(2)}} \to X^{\mathbf{(1)}} \to X^{\mathbf{(0)}} = X$ in $ETop \infty Grpd$:

$$
  \begin{aligned} 
     |\Pi(-)| & :   
   (X^{\mathbf{(\infty)}} \to \cdots X^{\mathbf{(2)}} \to X^{\mathbf{(1)}} \to X^{\mathbf{(0)}} = X) \in ETop\infty Grpd
    \\
     & \mapsto 
      (* \to \cdots X^{(2)} \to X^{(1)} \to X^{(0)} = X) 
       \in Top
  \end{aligned}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the general discussion at [[Whitehead tower in an (∞,1)-topos]] the geometric Whitehead tower is characterized for each $n$ by the [[fiber sequence]] 

$$
  X^{\mathbf{(n)}} \to X^{\mathbf{(n-1)}} \to 
  \mathbf{B}^n \mathbf{\pi}_n(X)
  \to 
  \mathbf{\Pi}_n(X) \to \mathbf{\Pi}_{(n-1)}(X)
  \,.
$$ 

By the above [proposition on the fundamental ∞-groupoid](#FundGroupoidOfParacompact) we have that $\mathbf{\Pi}_n(X) \simeq Disc Sing X$. Since $Disc$ is [[right adjoint]] and hence preserves [[homotopy fiber]]s this implies that 
$\mathbf{B} \mathbf{\pi}_n(X) \simeq \mathbf{B}^n Disc \pi_n(X)$, where $\pi_n(X)$ is the ordinary $n$th [[homotopy group]] of the pointed topological space $X$. 

Then by the above [proposition on geometric realization of homotopy fibers](#GeometricRealizationOfHomotopyFibers) we have that under $|\Pi(-)|$ the space $X^{\mathbf{(n)}}$ maps to the homotopy fiber of $|\Pi(X^{\mathbf{(n-1)}})| \to B^n |Disc \pi_n(X)| = B^n \pi_n(X)$.

By induction over $n$ this implies the claim.

=--


### Path $\infty$-groupoid and geometric Postnikov towers
{#PathInftinityGroupoids}

Let $C$ be an [[∞-connected site]]. We give an explicit presentation of the _<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Paths">constant path inclusion</a>_ $X \to \mathbf{\Pi}(X)$ in the [[locally ∞-connected (∞,1)-topos]] over $C$ such that the component maps are cofibrations. 

+-- {: .un_remark}
###### Remark

The projective [[model structure on simplicial presheaves]] 
$[C^{op}, sSet]_{proj}$ has a set of generating cofibrations

$$
  I =
  \{
    U \cdot \partial \Delta[n] \hookrightarrow U \cdot \Delta[n] | U \in C, n \in \mathbb{N})
  \}
  \,.
$$
=--

See [[model structure on functors]] for details.

+-- {: .un_def }
###### Definition

Write 

$$
  \mathbf{Sing} : C \to [C^{op}, sSet]
$$

for the functor given by applying the [[small object argument]] to this set $I$ to obtain a functorial factorization of the [[terminal object|terminal morphisms]] $U \to *$ into a cofibration followed by an acyclic fibration

$$
  U \hookrightarrow \mathbf{Sing} U \stackrel{\simeq}{\to} *
  \,.
$$

Let

$$
  \mathbf{Sing} : [C^{op}, sSet] \to [C^{op}, sSet]
$$

be the [[Yoneda extension]] (left [[Kan extension]] through the [[Yoneda embedding]]) of this functor to all of $[C^{op}, sSet]$.
=--

+-- {: .un_remark}
###### Remark

For $U \in C$ the [[simplicial presheaf]] $\mathbf{Sing}U$ is a [[resolution]] of the ([[nerve]] of the) [[fundamental groupoid]] $\Pi_1(U)$:

the non-degenerate components of $\mathbf{Sing}U$ at the first stage of the [[small object argument]] are such that a map out of them into a simplicial presheaf $A$ are given by commuting diagrams

$$
  \array{
    U_0 \coprod U_0 &\stackrel{(s,t)}{\to}& U
    \\ 
    \downarrow && \downarrow
    \\
    U_0 \times \Delta[1] &\to& A
  }
  \,.
$$

This is a $U$-parameterized family of objects of $A$ together with a $U_0$-parameterized family of morphisms of $A$ associated to the pairs of points $(s,t) \in U$, hence to the "straight paths" from $s$ to $t$. At the next stage for every triangle of such straight path a 2-morphism is thrown in, and so on. So $\mathbf{Sing}U$ indeed is an $\infty$-groupoid of paths in $U$. 
=--

+-- {: .un_prop}
###### Proposition

The functor $\mathbf{Sing}$ is the [[left adjoint]] of a [[Quillen adjunction]]

$$
  (\mathbf{Sing} \dashv R) : 
    [C^{op}, sSet]_{proj, loc} \to [C^{op}, sSet]_{proj, loc}
  \,.
$$

Its left [[derived functor]] is equivalent to the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]

$$
  \mathbb{L}\mathbf{Sing}(-) \simeq \Pi(-)
$$

and the _constant path inclusion_ $Id \to \Pi$ is presented by the canonical [[natural transformation]] $Id \to \mathbf{Sing}$.
=--

+-- {: .proof}
###### Proof

On an arbitrary simplicial presheaf $X$ the functor $\mathbf{Sing}$ is given by the [[coend]]

$$
  \mathbf{Sing} : X \mapsto
   \int^{U \in C} X(U) \cdot \mathbf{Sing}U
  \,.
$$

By construction this preserves all colimits. Hence by the [[adjoint functor theorem]] (using that domain and codomain are [[presheaf categories]]) we have that $\mathbf{Sing}$ is a [[left adjoint]]. Explicitly, the [[right adjoint]] is given by

$$
  R X : U \mapsto [C^{op}, sSet](\mathbf{Sing}U, X)
  \,.
$$

We check that $\mathbf{Sing}$ is also a [[Quillen adjunction|left Quillen functor]] first for the [[model structure on simplicial presheaves|global projective model structure]].
For that, notice that the above expression is the evaluation of the left [[Quillen bifunctor]] (see the exmaples-section there for details)

$$
  \int^C (-) \cdot (-) : 
    [C^{op}, sSet]_{proj} \times [C, [C^{op}, sSet]_{proj}]_{inj}
  \to
   [C^{op}, sSet]_{proj}
  \,.
$$

Since every representable $U$ is cofibrant in $[C^{op}, sSet]_{proj}$ and since $U \to \mathbf{Sing}U$ is a cofibration by the [[small object argument]], we have that $\mathbf{Sing}U$ is cofibrant in $[C^{op}, sSet]_{proj}$ for all $U$. This means that also $\mathbf{Sing}(-)$ is cofibrant in $[C, [C^{op}, sSet]_{pro}]_{inj}$. Since $\int^C (-) \cdot (-)$ is a left Quillen bifunctor it follows that $\int^C (-)\cdot \mathbf{Sing}$ is a left Quillen functor. Hence it preserves cofibrations and acyclic cofibrations.

This establishes that $\mathbf{Sing}$ is a left simplicial Quillen functor on $[C^{op}, sSet]_{proj}$.

Since this is a [[left proper model category]] we have by the discussion at [[simplicial Quillen adjunction]] that for showing that this does descend to the local model structure it is sufficient to check that the right adjoint preserves local fibrant objects. Which, in turn, is implied if $\mathbf{Sing}$ send covering [[Cech nerve]]s to weak equivalences.

Let therefore $C(\coprod_i U_i \to U)$ be the Cech nerve of a covering family in the [[site]] $C$. We may write this as the [[coend]]

$$
  C(\coprod_i U_i) = \int^{[k] \in \Delta} \Delta[k] \cdot
  \left(
    \coprod_{i_0, \cdots, i_n} U_{i_0, \cdots, i_n}
  \right)
  \,,
$$

where by assumption on the [[∞-connected site]] $C$ all the $U_{i_0, \cdots, i_n}$ are representable. By precomposing the projection $C(\coprod_i U_i) \to X$ with the objectwise [[Bousfield-Kan map]] that replaces the simplices with the [[fat simplex]] $\mathbf{\Delta} : \Delta \to sSet$, we get the morphisms

$$
  C(\coprod_i U_i) = \int^{[k] \in \Delta} 
   \mathbf{\Delta}[k] \cdot
  \left(
    \coprod_{i_0, \cdots, i_n} U_{i_0, \cdots, i_n}
  \right)
   \stackrel{\simeq}{\to}
   C(\coprod_i U_i)
   \to U
  \,.
$$

Here the first map is an objectwise weak equivalence by Bousfield-Kan (see the examples at [[Reedy model structure]] for details). Hence by 2-out-of-3 we may equivalently check that $\mathbf{Sing}$ sends these morphisms to weak equivalences in $[C^{op}, sSet]_{proj}$.

Since $\mathbf{Sing}$ commutes with all colimits and hence coends the result of applying it to this morphism is

$$
  \int^{[k] \in \Delta} 
   \mathbf{\Delta}[k] \cdot
  \left(
    \coprod_{i_0, \cdots, i_n} \mathbf{Sing} U_{i_0, \cdots, i_n}
  \right)
   \to \mathbf{Sing}U
  \,.
$$

Since the [[fat simplex]] is cofibrant in $[\Delta, sSet_{Quillen}]_{proj}$ and since the above is an evaluation of the left [[Quillen bifunctor]]

$$
  \int^\Delta (-) \cdot (-) :
   [\Delta, sSet_{Quillen}]_{proj} \times
   [\Delta^{op}, [C^{op}, sSet]_{proj}]_{inj}
  \to
   [C^{op}, sSet]_{proj}
$$

the functor $\int^\Delta \mathbf{\Delta} \cdot (-)$ is left Quillen and hence preserves weak equivalences between cofibrant objects (by the [[factorization lemma]]), such as the morphisms $\mathbf{Sing}U \stackrel{\simeq}{\to} *$. Therefore we have a commuting diagram

$$
  \array{
    \int^{[k] \in \Delta} 
     \mathbf{\Delta}[k] \cdot
    \left(
      \coprod_{i_0, \cdots, i_n} \mathbf{Sing} U_{i_0, \cdots, i_n}
    \right)
      &\stackrel{\simeq}{\to}&
    \int^{[k] \in \Delta} 
     \mathbf{\Delta}[k] \cdot
    \left(
      \coprod_{i_0, \cdots, i_n} *
    \right)
    \\
    \downarrow && \downarrow^{\simeq}
    \\
    \mathbf{Sing}U &\stackrel{\simeq}{\to}& *
   }
  \,,
$$

with weak equivalences in $[C^{op}, sSet]_{proj}$ as indicated: the top morphism is a weak equivalence by the argument just given, the bottom one by the [[small object argument]]-construction of $\mathbf{Sing}$ and the right vertical morphism is a weak equivalence by the assumption on an [[∞-connected site]]. It follows by 2-out-of-3 that also the left vertical morphism is a weak equivalence.

This establishes the fact that $\mathbf{Sing}$ is left Quillen on the local model structure on simplicial presheaves. By the discussion at [[simplicial Quillen adjunction]] this implies that its left [[derived functor]] is a [[left adjoint|left]] [[adjoint (∞,1)-functor]]. Hence it preserves [[(∞,1)-colimit]]s and so is determined on representatives. There $\mathbf{Sing} U \simeq *$ does coindice with $\Pi(U) \simeq *$, hence both [[(∞,1)-functor]]s are equivalent.
=--

+-- {: .un_corollary}
###### Corollary

For all cofibrant $X \in [C^{op}, sSet]_{proj,loc}$, the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#deRhamCohomology">de Rham coefficient object</a> $\mathbf{\Pi}_{dR} X$ is presented by the ordinary [[pushout]]

$$
  \array{
     X &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathbf{Sing}X &\to& \mathbf{\Pi}_{dR} X
  }
$$

in $[C^{op}, sSet]$.
=--

+-- {: .proof}
###### Proof

By definition we have that $\mathbf{\Pi}_{dR}$ is the [[(∞,1)-pushout]] $\mathbf{\Pi}(X) \coprod_X *$ in $Sh_{(\infty,1)}(C)$. By the above proposition we have a cofibrant presentation of the pushout diagram as indicated (all three objects cofibrant, at least one of the two morphisms a cofibration). By the general discussion at [[homotopy colimit]] the ordinary pushout of that diagram does compute the [[(∞,1)-colimit]].
=--

## Homotopy localization

We discuss that the[[homotopy localization]] of topological $\infty$-groupoids reproduces [[Top]] $\simeq$ [[∞Grpd]], following ([Dugger](#Dugger)).


### Idea

A central result about the [[(∞,1)-topos]] $Sh_{(\infty,1)}(Top)$ of [[∞-stack]]s on [[Top]] is that the [[homotopy localization]] is equivalent to [[Top]] itself

$$
  Sh_{(\infty,1)}(Top)^I \simeq Top
  \,.
$$

A discussion of this is in (the nice but not quite finished) ([Dugger](#Dugger)).

In fact, this is true even for [[Lie ∞-groupoid]]s, i.e. [[∞-stack]]s on [[Diff]]: the homotopy invariant ones model plain [[topological space]]s.

This provides a useful resolution of [[topological space]]s that often helps to disentangle the two different roles played by a topological space: on the one hand as a model for an [[∞-groupoid]], in the other as a [[locale]].


### Details

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

+-- {: .un_theorem}
###### Theorem (Dugger)

This adjunction $(L \dashv R)$ is a [[Quillen equivalence]] with respect to the  standard [[model structure on simplicial sets]] on the left and the above model structure $SPSh(Diff)_{loc}^I$ on the right.
=--


## References

Section 3.2 in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

Some discussion of the $(\infty,1)$-category of $(\infty,1)$-sheaves on the category of manifolds and its restriction to open balls and a discussion of its homotopy localization is in:

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))
{#Dugger}

Discussion of geometric realization of simplicial topological principal bundles is in 

* [[nLab:Danny Stevenson]], [[nLab:David Roberts]], unpublished notes (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#StevensonRoberts">web</a>)
{#StevensonRoberts}


[[!redirects Euclidean-topological infinity-groupoid]]
[[!redirects Euclidean-topological infinity-groupoids]]
[[!redirects Euclidean-topological infnity-groupoid]]
[[!redirects Euclidean-topological ∞-groupoid]]
[[!redirects Euclidean-topological ∞-groupoids]]
[[!redirects Euclidean topological infinity-groupoid]]
[[!redirects Euclidean topological infinity-groupoids]]
[[!redirects Euclidean topological ∞-groupoid]]
[[!redirects Euclidean topological ∞-groupoids]]

[[!redirects ETop∞Grpd]]

[[!redirects topological infinity-groupoid]]
[[!redirects topological infinity-groupoids]]
[[!redirects topological ∞-groupoid]]
[[!redirects topological ∞-groupoids]]

[[!redirects ?TopGrpd]]

[[!redirects continuous infinity-groupoid]]
[[!redirects continuous infinity-groupoids]]
[[!redirects continuous ∞-groupoid]]
[[!redirects continuous ∞-groupoids]]
