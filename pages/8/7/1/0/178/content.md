
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _smooth $\infty$-groupoid_ is an [[∞-groupoid]] equipped with [[cohesive (∞,1)-topos|cohesion]] in the form of [[smooth structure]].

This generalizes [[Lie group]]s and [[Lie groupoid]]s from [[category theory]] to [[higher category theory]] and [[homotopy theory]].



### Reminder: Lie groupoids and differentiable stacks

Before indicating the idea of $\infty$-Lie groupoids in more detail, recall some aspects of the theory of ordinary [[Lie groupoid]]s.

An ordinary [[Lie groupoid]] is usually understood to be a [[groupoid]] [[internalization|internal]] to [[Diff]], possibly with further extra conditions on its structure morphisms. The literature on Lie groupoids is familiar with the fact that it is often useful to regard these internal groupoids after embedding them into the more general context of [[stack]]s on the [[site]] [[Diff]] of all [[smooth manifold]]s: there they are called [[differentiable stack]]s.

Regarding a groupoid internal to manifolds $\mathcal{G}$ as a [[stack]] $\mathcal{G} : Diff^{op} \to $ [[Grpd]] means encoding it in terms of the groupoids of smooth _families_ of objects and morphisms inside it:

* to the point $* \in Diff$ it assigns the underlying bare groupoid $\mathcal{G}(*)$, the groupoid $\mathcal{G}$ with its smooth structure forgotten;

* to a manifold $U \in Diff$ it assigns the groupoid $\mathcal{G}(U)$ whose set of [[object]]s is the set $\mathcal{G}(U)_0 := Hom_{Diff}(U,\mathcal{G}_0)$ of smooth $U$-parameterized [[object]]s in $U$, and whose set of [[morphism]]s $\mathcal{G}(U)_1 := Hom_{Diff}(U,\mathcal{G}_1)$ is the set of smooth $U$-parameterized morphisms in $\mathcal{G}$.

Not every stack on [[Diff]] comes from a [[groupoid]] $\mathcal{G}$ [[internalization|internal to]] [[Diff]] this way. For instance the ([[stackification]] of the) [[groupoid of Lie-algebra valued forms]] for some [[Lie group]] $G$ is a [[concrete presheaf|non-concrete]] stack, which can never be represented by an internal groupoid. Still, most operations that one may want to apply to internal groupoids also make sense for general stacks on [[Diff]]. Indeed, some operations that one may want to apply to internal groupoids take values not in internal groupoids, but in more general stacks: the [[2-category]] $Sh_{(2,1)}(Diff)$ of all stacks on $Diff$ is formally more well behaved than the sub-category of [[differentiable stack]]s inside it. One useful way to formalize all the nice structure that $Sh_{(2,1)}(Diff)$ has is to see that this is a [[2-topos]].

Therefore it is quite useful to think of _every_ stack on $Diff$ as encoding a _smooth groupoid_ and to think of the study of Lie groupoids as being the theory of the [[2-topos]] $Sh_{(2,1)}(Diff)$. The groupoids internal to $Diff$ are special nice objects in this 2-topos: the [[geometric stack]]s.

For this reason, here we shall find it useful to adopt the term _Lie groupoid_ for a general objects in $Sh_{(2,1)}(Diff)$ and to speak of Lie groupoids _[[representable functor|represented]]_ in [[smooth manifold]]s or of [[geometric stack]]s if we mean groupoids internal to manifolds, under the embedding indicated above.


### Smooth $\infty$-groupoids as $(\infty,1)$-sheaves / $\infty$-stacks

As we generalize from [[groupoid]]s to [[∞-groupoid]]s, the notion of [[stack]]/[[2-sheaf|(2,1)-sheaf]] generalizes to that of [[∞-stack]]/[[(∞,1)-sheaf]]. Therefore we shall _define_ an $\infty$-Lie groupoid to be an [[(∞,1)-sheaf]] on a [[site]] of smooth test spaces. 

Notice that for the definition of the smooth structure on a [[diffeological space]] or on an ordinary [[Lie groupoid]] it is not in fact necessary to regard these as objects tested by objects in all of [[Diff]]: since smoothness is a local property, it is entirely sufficient to know around every point in the set of [[k-morphism]]s of the $\infty$-groupoid what all the extensions of this point to a _ball_ -shaped smooth family of points around that point are. This is precisely what an [[∞-stack]] on [[CartSp]] encodes, the category of just [[Cartesian space]]s and [[smooth function]]s between them. A discussion of the difference or not between $\infty$-stacks on [[Diff]] and on [[CartSp]] see the section [below](#CartSpAndDiff)


We shall think of the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ as being the context in wich [[∞-Lie theory]] takes place. As before, inside this large context only some nice objects correspond to [[internal ∞-groupoid]]s in [[Diff]] or in [[diffeological space|Diffeol]]. These [[geometric stack|geometric ∞-stack]]s are the concrete or geometric $\infty$-Lie groupoids inside more general objects. One way to make precise the notion of _geometric ∞-stack_ with respect to a chosen notion of _geometric_ is to adopt the concept of [[geometry (for structured (∞,1)-toposes)]].

There are other sites on wich one may want a smooth $\infty$-groupoid to be modeled on. For instance instead of testing only with [[smooth manifold]]s, one may want to test with [[smooth loci]]. An ordinary [[sheaf]] on the category $\mathbb{L}$ of smooth loci is a generalized [[smooth space]] as considered in [[synthetic differential geometry]]. Accordingly, an $\infty$-stack on $\mathbb{L}$ may be thought of as a smooth $\infty$-Lie groupoid to which synthetic differential geometry applies.

The key difference of $\mathbb{L}$ to [[Diff]] is that the former contains smooth [[infinitesimal space]]s. Therefore an $\infty$-Lie groupoid modeled on $\mathbb{L}$ may have spaces of [[k-morphism]]s that have infinitesimal extension in some direction. Notably one obtains a notion of $\infty$-Lie groupoids for which _all $k$-morphisms are infinitesimal_ in a precise sense. It sturns out that such **infinitesimal $\infty$-Lie groupoids** may be identified with [[∞-Lie algebroid]]s: generalizations to [[higher category theory]] of [[Lie algebra]]s and [[Lie algebroid]]s.


### $\infty$-Stacks on $SmoothMfd$ and on $CartSp_{smooth}$

In the literature on [[Lie groupoid]]s and [[differentiable stack]]s, these are traditionally conceived as [[stack]]s on the [[site]] [[SmoothMfd]] of all [[smooth manifold]]s. As mentioned above, for the purpose of encoding a smooth structure on a [[groupoid]] the category [[Diff]] regarded as a category of test objects is larger than necessary. After all, every manifold is, by definition, itself patched together from [[Cartesian space]]s, and passing to sheaves or stacks on a site really just means that one allows objects patched together from the objects in the site, so that one could just as well take the site to be just that of [[Cartesian space]]s in the first place.

More precisely, we have an [[equivalence of categories]] between the [[categories of sheaves]] on [[CartSp]] and on [[Diff]]

$$
  Sh(Diff) \stackrel{\simeq}{\to} Sh(CartSp)
$$

induced from the [[full and faithful functor]] $CartSp \hookrightarrow Diff$. Under this equivalence a sheaf on all of $Diff$ is simply restricted to just the subcategory [[CartSp]].

To see this, notice that every [[smooth manifold]] $X$ admits a [[good cover]] $\{U_i \to X\}$, where each $U_i$ is [[diffeomorphism|diffeomorphic]] to a [[Cartesian space]] (essentially by definition of [[manifold]]). By the [[sheaf]] condition, the value $A(X)$ of a sheaf on $X$ is determined by its value on these $U_i$. Hence the sheaf on [[Diff]] is already entirely determined by its restriction to [[CartSp]].

An analogous discussion holds for [[(∞,1)-sheaves]] on these sites, which we illustrate by the following standard example.

Let $G$ be a [[Lie group]]. We shall write

* $\mathbf{B}G : \mapsto G TrivBund(U) := (Hom_{Diff}(U,G) \stackrel{\to}{\to} *)$ ;

* $G Bund : X \mapsto G Bund(X)$;

for the functorial assignments of groupoids to smooth manifolds, where in the last case we assign the groupoid of $G$-[[principal bundle]]s and in the  first case the groupoid of _trivial_ $G$-principal bundles.

Now let $X$ be any smooth manifold. We want to compute the groupoid of smooth $G$-principal bundles as the [[hom-object]] $X \to \mathbf{B}G$ in the [[(∞,1)-category of (∞,1)-sheaves]] on [[Diff]] or [[CartSp]]. In order to present that [[(∞,1)-category]], we shall make use of its [[model category]]-theoretic presentation in terms of the [[model structure on simplicial presheaves]] $sPSh(C)_{proj,loc}$. Then in order to compute the [[derived hom-space]] in question, we need to 

1. find a cofibrant replacement $Y \stackrel{\simeq}{\to} X $ of $X$;

1. find a fibrant replacement $A \stackrel{\simeq}{\to} B$ of $A$.

1. compute the ordinary [[enriched functor category|enriched hom-object]]

   $\mathbf{H}(X, \mathbf{B}G) = sPSh(Y,B) $

The point now is that the kind of work one has to do to achieve this differs from $sPSh(CartSp)_{proj,loc}$ and $sPSh(Diff)_{proj,loc}$. But the outcome is the same:

1. The approach traditionally used in the literature is, essentially, this: 
   in $sPSh(Diff)_{proj,loc}$ the manifold $X$ is a 
   [[representable functor|representable]] object, of course. This means
   it is already cofibrant and we can simply take $Y = X$. 

   On the other hand, in this model structure the presheaf $\mathbf{B}G$ is 
   far from being fibrant. But $G Bund$, the closure of $\mathbf{B}G$ under
   [[descent]], is of course its fibrant replacement, and the
   canonical inclusin morpism
   $\mathbf{B}G \to G Bund$ is a weak equivalence.

   So finally we can compute 

   $$
     \mathbf{H}(X,\mathbf{B}G) = sPSh_{Diff}(X,G Bund)
   $$

   simply by the [[Yoneda lemma]] as

   $$
     \cdots \simeq G Bund(X)
     \,.
   $$

   In conclusion here no work had to be done on the cofibrant replacement,
   while lots of work has to be done on the fibrant replacement.
   Notice that in order to compute the groupoid of $G$-principal bundles
   on just $X$, we here first computed the corresponding groupoid
   for each and every manifold, in that we first computed the full 
   stack $G Bund$. (Of course in this simple example this is not
   really a big deal, but it should be clear that for $G$ generalized
   to any smooth [[∞-group]] and hence $G Bund$ to the $\infty$-stack
   of $G$-[[principal ∞-bundle]]s, it does become quite a big deal).

1. Now consider the same situation, but in $sPSh(CartSp)_{proj,loc}$. 
   Here the technicalities reverse:

   Now $X$ is (in general) no longer representable, hence it
   is in general no longer cofibrant. We need to pass to a cofibrant
   replacement $Y \to X$ instead. Such can be obtained for instance
   by taking $Y$ to be the [[Cech nerve]] of a [[good cover]] of $X$.

   On the other hand, now $\mathbf{B}G$ is already fibrant! Because the
   fibrancy condition is that it satisfies [[descent]] along 
   [[Cech nerve]]s $C(\{U_i\})$ of [[cover]]s 
   $\{U_i \to U\}$ of objects $U$ in [[CartSp]].  But since every
   $G$-principal bundle on a [[Cartesian space]] is necessarily equivalent
   to the trivial one, we have that
 
   $$
     \mathbf{B}G(U) 
     =
     G TrivBund(U)
     \simeq
     G Bund(U)
     \simeq
     sPSh_{CartSp}(C(\{U_i\}), \mathbf{B}G)     
   $$

   because $U$ is topologically contractible. So $\mathbf{B}G$ _does_
   satisfy descent -- not on [[Diff]], but on [[CartSp]].

   In conclusion, here we may compute the hom-object as

   $$
     \mathbf{H}(X,\mathbf{B}G)
     \simeq
     sPSh_{CartSp}(C(\{U_i\}), \mathbf{B}G)
     \,.
   $$

   On the right this is just the [[Cech cohomology]] of $X$ with values
   in $\mathbf{B}G$ and hence indeed

   $$
     \simeq G Bund(X)
     \,.
   $$








## Definition

+-- {: .un_defn #DifferentiablyGoodOpenCover}
###### Definition

For $X$ a [[smooth manifold]], say an [[open cover]] $\{U_i \to X\}$ is a
**differentiably good open cover** if each non-empty finite intersection of the $U_i$ is [[diffeomorphism|diffeomorphic]] to a [[Cartesian space]].

=--

+-- {: .un_prop}
###### Proposition

Every [[paracompact manifold|paracompact]] [[smooth manifold]] admits a differentiably good open cover.

=--

+-- {: .proof}
###### Proof

This is a folk theorem. A detailed proof is at [[good open cover]].

=--

+-- {: .un_def}
###### Definition


Let [[SmoothMfd]] be the [[large site]] of 
[[paracompact manifold|paracompact]] [[smooth manifold]]s 
with [[smooth function]]s between them and equipped with the [[coverage]] 
of [differentiably good open covers](#DifferentiablyGoodOpenCover).

=--

+-- {: .un_def}
###### Observation

This does indeed define a coverage. The [[Grothendieck topology]] that is generated from it is the standard [[open cover]] topology.

=--

+-- {: .proof}
###### Proof

For $\{U_i \to X\}$ any open cover of a paracompact manifold also $\coprod_i U_i$ is paracompact. Hence we may find a differentiably good open cover
$\{K_j \to \coprod_i U_i\}$. This is then a refinement of the original open cover of $X$.

=--



+-- {: .un_defn}
###### Definition

Let [[CartSp]]${}_{smooth}$ be the [[site]] of [[Cartesian space]]s with [[smooth function]]s between them and equipped with the [[coverage]]
of [differentiably good open covers](#DifferentiablyGoodOpenCover).

=--
 
+-- {: .un_defn}
###### Definition

The [[(∞,1)-topos]] of **smooth $\infty$-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]] on [[CartSp]]${}_{smooth}$:

$$
  Smooth \infty Grpd 
   :=
  Sh_{(\infty,1)}(CartSp_{smooth})
  \,.
$$


=--


## Properties


+-- {: .un_prop}
###### Proposition

$Smooth \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

The [[site]] [[CartSp]]${}_{smooth}$ is (as discussed there) an [[∞-cohesive site]] (see there).

=--

+-- {: .un_def}
###### Definition

Let [[SmoothMfd]] be the [[large site]] of [[paracompact topological space|paracompact]] [[smooth manifold]]s with [[smooth function]]s between them and equipped with the [[coverage]] whose [[covering]] families are _differentiably good open covers_ : [[open cover]]s $\{U_i \to U\}$ where each non-empty open intersection is [[diffeomorphic]] to a [[Cartesian space]].

=--

+-- {: .un_prop}
###### Proposition

This does indeed define a [[coverage]] and the [[Grothendieck topology]] generated by it is the standard [[open cover]] topology.

=--

+-- {: .proof}
###### Proof

This is discussed in detail at [[good open cover]].

=--

+-- {: .un_prop #SmoothManifoldEmbeds}
###### Proposition

The [[(∞,1)-topos]] $Smooth \infty Grpd$ is equivalent to the [[hypercompletion]] $\hat Sh_{(\infty,1)}(SmoothMfg)$ of the [[(∞,1)-category of (∞,1)-sheaves]] on the large site [[SmoothMfd]]

$$
  Smooth \infty Grpd \simeq \hat Sh_{(\infty,1)}(SmoothMfd)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the above we have that [[CartSp]]${}_{smooth}$ is a [[dense sub-site]] of [[SmoothMfd]]. With this the claim follows as in the analogous discussion at [[ETop∞Grpd]].

=--

+-- {: .un_prop #EmbeddingOfSmoothManifolds}
###### Corollary

The canonical embedding of [[smooth manifold]]s as [[0-truncated]] objects in $Smooth\infty Grpd$ is a [[full and faithful (∞,1)-functor]]

$$
  SmoothMfd \hookrightarrow Smooth \infty Grpd
  ,.
$$

=--


## Structures in the cohesive $(\infty,1)$-topos $Smooth \infty Grpd$ {#InfSheavesOnCartSp}

We discuss the general abstract 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesivbe (∞,1)-topos</a> realized in $Smooth \infty Grpd$.


### Concrete objects {#StrucConcreteObjects}

We discuss the general abstract notion of 
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ConcreteObjects">concrete objects in a cohesive (∞,1)-topos</a> in 
$Smooth \infty Grpd$.

+-- {: .un_prop}
###### Proposition

Write $Conc(\tau_{\leq 0} Smooth \infty Grpd)$ for the full [[subcategory]] on the [[concrete sheaf|concrete]] [[0-truncated]] objects. This is [[equivalence of categories|equivalent]] to the category of [[diffeological space]]s

$$
  DiffeolSp 
   \simeq 
  Conc(\tau_{\leq 0} Smooth \infty Grpd)
  \,.
$$

=--


+-- {: .proof}
###### Proof

Let $X \in Sh(CartSp) \hookrightarrow Smooth \infty Grpd$ be a [[sheaf]] on $CartSp$. The condition for it to be concrete is that the [[unit of an adjunction|unit]]

$$
  X \to coDisc \Gamma X
$$

is a [[monomorphism]]. Since monomorphisms of sheaves are detected objectwise (see [[category of sheaves]]) this is equivalent to the statement that for all $U \in CartSp$ the morphism

$$
  X(U) \simeq Smooth\infty Grpd(U, X) \to Smooth \infty Grpd(U, coDisc \Gamma X)
  \simeq
  \infty Grpd(\Gamma U, \Gamma X)
$$

is a monomorphism of sets, where in the first step we used the [[(∞,1)-Yoneda lemma]] and in the last one the $(\Gamma \dashv coDisc)$-[[adjunction]]. 

That this morphism is indeed $\Gamma : Sh(U,X) \to Set(\Gamma(U), \Gamma(X)) \hookrightarrow \infty Grpd(\Gamma(U), \Gamma(X))$ follows by chasing the identity on $\Gamma X$ through the adjunction naturality square for any morphism $f : U \to X$

$$
  \array{
    Set(\Gamma X, \Gamma X) &\stackrel{\simeq}{\to}&
    Sh(X, coDisc \Gamma X)
    \\
    \downarrow^{\mathrlap{\Gamma(f)^*}} && \downarrow^{\mathrlap{f^*}}
    \\
    Set(\Gamma U, \Gamma X) &\stackrel{\simeq}{\leftarrow}& Sh(U, coDisc \Gamma X)
  }
  \,.
$$

So this is indeed the defining condition for [[concrete sheaves]] that defines [[diffeological space]]s.

=--

+-- {: .un_prop}
###### Corollary

The canonical embedding $SmoothMfd \hookrightarrow Smooth \infty Grpd$
from [above](#EmbeddingOfSmoothManifolds) factors through [[diffeological spaces]]: we have a sequence of [[full and faithful (∞,1)-functor]]s

$$
  SmoothMfd \hookrightarrow DiffeolSp \hookrigharrow Smooth \infty Grpd
  \,.
$$

=--

+-- {: .un_def #DiffeologicalKanComplex}
###### Definition

A **diffeological $\infty$-groupoid** or **diffeological Kan complex**
is a [[Kan complex]] [[internalization|internal to]] [[diffeological space]]s.

=--


+-- {: .un_prop #DiffeologicalKanComplexesAreConcrete}
###### Proposition

Let $X$ be a diffeological $\infty$-groupoid. Regarded as an object
in $Smooth \infty Grpd$ under the composite morphism

$$
  X \in Sh(CartSp_{smooth})^{\Delta^{op}} 
   \hookrightarrow
    [CartSp_{smooth}^{op}, sSet] 
  \to 
   ([CartSp_{smooth}^{op}, sSet]_{proj,loc})^\circ 
   \simeq 
  Smooth \infty Grpd
$$ 

this is a
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ConcreteObjects">concrete object</a>.

=--

+-- {: .proof}
###### Proof

By the general properties discussed at [[cohesive (∞,1)-topos]] we have that $Smooth \infty Grpd$ is a [[hypercomplete (∞,1)-topos]]. Hence we may equivalently model it by the local [[model structure on simplicial sheaves]] on $CartSp_{smooth}$. Notice that any diffeological Kan complex is naturally a fibrant object in the global model structure on simplicial sheaves.
By definition of the local model structure, the morphism from any simplicial sheaf to its local cofibrant-fibrant [[resolution]] is an isomorphism on all [[categorical homotopy groups in an (infinity,1)-topos|homotopy sheaves]]. Since the [[quasitopos]] of [[diffeological space]]s is closed under the finite [[limit]]s and [[colimit]]s involved in defining homotopy sheaves, these are themselves [[concrete sheaves]]. 

=--



### Geometry and structure sheaves {#StrucGeometry}

(...)


### Cohesive $\infty$-groups {#StrucInfinGroups}

We discuss <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#InfinGroups">cohesive ∞-groups</a> in $Smooth \infty Grpd$: smooth $\infty$-groups.


#### Strict $\infty$-Lie groupoids


Many $\infty$-Lie groupoids appearing in practice are (equivalent) to objects in [[sub-(∞,1)-categories]] of $Sh_{(\infty,1)}(CartSp)$ of much stricter $\infty$-Lie groupoids. These subcategories typically offer convenient and desireable contexts for formulating and proving statements about special cases of general $\infty$-Lie groupoids.  Therefore it is of interest to have various notions of _strict_ $\infty$-Lie groupoids inside all of them.

One well-known such notion is given by the [[Dold-Kan correspondence]]. This identifies [[chain complex]]es of [[abelian group]]s with strict and strictly [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] $\infty$-groupoids.

Dropping the condition on symmetric monoidalness we obtain a more general such inclusion, a kind of non-abelian Dold-Kan correspondence: 

the identification of [[crossed complex]]es of groupoids as precisely the [[strict omega-groupoid|strict ∞-groupoid]]s. This has been studied in particular in [[nonabelian algebraic topology]].

So we have a sequence of inclusions

$$
  \array{
     ChainCplx &\hookrightarrow& CrsCpl &\hookrightarrow& KanCplx
     \\
     \downarrow && \downarrow && \downarrow
     \\
     StrAb Str\infty Grpd &\hookrightarrow&
     Str \infty Grpd
     &\hookrightarrow&
     \infty Grpd 
  }
$$

of strict $\infty$-groupoids into all $\infty$-groupoids. See also the [[cosmic cube]] of [[higher category theory]]. 

Among the special tools for handling $\infty$-stacks on $CartSp$ that factor at some point through the above inclusion are the following:

* **restriction to abelian sheaf cohomology** -- Using the fact that the objects of $Sh_{(\infty,1)}(CartSp)$ are modeled by [[simplicial presheaves]] symmetric monoidal $\infty$-Lie groupoids are identified under the [[nLab:Dold-Kan correspondence]] with $\mathbb{N}$-graded [[nLab:chain complex|chain complexes]] of sheaves. To these the rich set of tools for [[abelian sheaf cohomology]] apply. 

* **descent for strict $\infty$-groupoid valued sheaves** -- There is a good theory pf [[descent]] for (presheaves) with values in strict $\infty$-groupoids (more restrictive than the fully general theory but more general than [[abelian sheaf cohomology]]). This goes back to [[nLab:Ross Street|Ross Street]] and its relation to the full theory has been clarified by [[Dominic Verity]] in [Verity09](#Verity).


It should be noticed that for $\infty$-stacks of $\infty$-groupoids the intuition from the [[homotopy hypothesis]] no longer quite applies, necessarily. For instance under [geometric realization](#GeometricRealization) $\Pi : \infty LieGrpd \to \infty Grpd$ already strict $\infty$-groupoid-valued presheaves exhaust all [[homotopy type]]s in [[∞Grpd]] $\simeq$ [[Top]]: because already all 0-[[truncated]] objects (set-values sheaves) exhaust all homotopy types, as the geometric geometric realization does not produces the [[categorical homotopy groups in an (∞,1)-topos]], but the [[geometric homotopy groups in an (∞,1)-topos]].


#### Descent for strict $\infty$-Lie groupoids {#DescentForStrictInf}

We state a useful theorem for the computation of [[descent]] for presheaves with values in [[strict ∞-groupoid]]s. Recall the standard terminology for [[descent]], i.e. for the $(\infty,1)$-categorical [[sheaf]]-condition:

For $U \in C$ a representable (here $C = $ [[CartSp]] for our purposes), $Y,A \in [C^{op}, sSet]$ simplicial presheaves and $p : Y \to U$ a morphism, we say that $A$ _satisfies [[descent]]_ along $p$ or equivalently that $A$ is a $p$-[[local object]] if the canonical morphism

$$
  A(U) \stackrel{=}{\to}
  [C^{op}, sSet](U,A) 
  \to 
  [C^{op}, sSet](Y,A)
$$

is a weak equivalence. Here the first equality is the enriched [[Yoneda lemma]]. By the [[co-Yoneda lemma]] we may decompose $Y$ into itsw cells as

$$
  Y = \int^{[n] \in \Delta} \Delta[n] \cdot Y_n
  \,,
$$

where in the integrand we have the [[copower|tensoring]] of $[C^{op}, sSet]$ over [[sSet]]. Using that the enriched [[hom-functor]] sends coends to ends, the enriched [[hom-functor]] on the right we may equivalently write out as an [[end]]

$$
  \begin{aligned}
    [C^{op}, sSet](Y,A) 
    & =
    [C^{op}, sSet](\int^{[n] \in \Delta} \Delta[n] \cdot Y_n ,A)
    \\
    & = 
    \int_{[n] \in \Delta}[C^{op}, sSet](\Delta[n] \cdot Y_n ,A)
    \\
    & =
    \int_{[n] \in \Delta} sSet(\Delta[n], [C^{op}, sSet](Y_n, A))
    \\
    & =
    \int_{[n] \in \Delta} sSet(\Delta[n], A(Y_\bullet))
    \\
    & =:Desc(Y,A)
  \end{aligned}  
$$

(equality signs denote [[isomorphism]]s), where in the second but last line we again used the [[copower|tensoring]] of [[simplicial presheaves]] $[C^{op}, sSet]$ over [[sSet]].

In the last line we have the _totalization_ of the cosimplicial [[simplicial object]]

$$
  A(Y_\bullet) : \Delta \to sSet
  \,,
$$

sometimes called the _descent object_ of $A$ relative to $Y$, even though in this case it is really nothing but the hom-object of $Y$ into $A$. If $A$ is fibrant and $Y$ cofibrant, then $Desc(Y,A)$ is  a Kan complex: the _descent $\infty$-groupoid_ .

Now suppose that $\mathcal{A} : C^{op} \to Str \infty Grpd$ is a presheaf with values in [[strict ∞-groupoid]]s. In the context of strict $\infty$-groupoids the standard $n$-[[simplex]] is given by the $n$th [[oriental]] $O(n)$. This allows to perform a construction that looks like a descent object in $Str\infty Grpd$:

+-- {: .un_def }
###### Definition
**(Ross Strees)**

The descent object for $\mathcal{A} \in [C^{op}, Str \infty Grpd]$ relative to $Y \in [C^{op}, sSet]$ is

$$
  Desc(Y,\mathcal{A}) := \int_{[n] \in \Delta} Str\infty Cat(O(n), \mathcal{A}(Y_n))
  \;\in Str \infty Grpd
  \,,
$$

where the [[end]] is taken in $Str \infty Grpd$. 

=--

This objects had been suggested by [[Ross Street]] to be the right descent object for strict $\infty$-category-valued presheaves in [Street03](#Street03) 

Under the [[∞-nerve]] functor $N_O : Str\infty Grpd \to sSet$ this yields a [[Kan complex]] $N_0 Desc(Y,\mathcal{A})$. On the other hand, applying the $\omega$-nerve directly to $\mathcal{A}$ yields a simplicial presheaf $N_O\mathcal{A}$ to which the above simplicial descent applies. 

The following theorem asserts that under certain conditions both notions coincide.

+-- {: .un_theorem }
###### Theorem
**(Dominic Verity)**

If $\mathcal{A} : C^{op}, Str \infty Grpd$ and $Y : C^{op} \to sSet$ are such that $N_O \mathcal{A}(Y_\bullet) : \Delta \to sSet$ is fibrant in the [[Reedy model structure]] $[\Delta, sSet_{Quillen}]_{Reedy}$, then 

$$ 
  N_O Desc(Y,\mathcal{A}) \stackrel{\simeq}{\to} Desc(Y, N_O \mathcal{A})
$$

is a [[weak homotopy equivalence]] of [[Kan complex]]es.

=--

This is proven in [Verity09](#Verity).


+-- {: .un_corollary }
###### Corollary

If $Y \in [C^{op}, sSet]$ is such that $Y_\bullet : \Delta \to [C^{op}, Set] \hookrightarrow [C^{op}, sSet]$ is cofibrant in $[\Delta, [C^{op}, sSet]_{proj}]_{Reedy}$ then for $\mathcal{A} : C^{op} \to Str \infty Grpd$ we have

$$ 
  N_O Desc(Y,\mathcal{A}) \stackrel{\simeq}{\to} Desc(Y, N_O \mathcal{A})
  \,.
$$

=--

+-- {: .proof}
###### Proof

If $Y_\bullet$ is Reedy cofibrant, then by definition the canonical morphisms

$$
  \lim_{\to}( ([n] \stackrel{+}{\to} [k]) \mapsto Y_k ) \to Y_n
$$

are cofibrations in $[C^{op}, sSet]_{proj}$. Since the latter is an $sSet_{Quillen}$ [[enriched model category]] and $N_O \mathcal{A}$ is fibrant, it follows that the [[hom-functor]] $[C^{op}, sSet](-, N_O \mathcal{A})$ sends cofibrations to fibrations, so that

$$
  N_O\mathcal{A}(Y_n)
  \to
  \lim_{\leftarrow}( [n]\stackrel{+}{\to} [k] \mapsto N_O\mathcal{A}(Y_k))
$$ 

is a [[Kan fibration]]. But this says that $N_O \mathcal{A}(Y_\bullet)$ is Reedy fibrant, so that the assumption  of Verity's theorem is met.

=--

+-- {: .un_corollary }
###### Corollary

For $Y$ the [[Cech nerve]] of a [[good open cover]] $\{U_i \to X\}$ of a [[manifold]] $X$ and any $\mathcal{A} : CartSp^{op} \to Str \infty Grpd$ we have that

$$
  [C^{op}, sSet](Y,N_O \mathcal{A})
  \simeq
  N_O Desc(Y_\bullet, \mathcal{A})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the above is sufices to note that $Y_\bullet$ is cofibrant in $[\Delta^{op}, [C^{op}, sSet]_{proj}]_{Reedy}$ if $Y$ is the [[Cech nerve]] of a good open cover. By the assumption of good open cover we have that $Y$ is degreewise a coproduct of representables and that the inclusion of all degenerate $n$-cells into all $n$-cells is a full inclusion into a coproduct, i.e. an inlusion of the form

$$
  \coprod_{i \in I} U_i \to \coprod_j U_{j \in J}
$$

induced from an inclusion of subsets $I \hookrightarrow J$. Since all representables are cofibrant in $[C^{op}, sSet]_{proj}$ such an inclusion is a cofibration.

=--

In conclusion we find that for determining the $\infty$-stack condition for _strict_ $\infty$-Lie groupoids we may equivalently use Street's formula for strict $\infty$-groupid valued presheaves. This is sometimes useful for computations in low categorical degree. 






#### Lie groups {#LieGroups}

Let $G$ be a [[Lie group]]. Under the [embedding](#SmoothManifoldEmbeds) 
$SmoothMfd \hookrightarrow Smooth \infty Grpd$ this is canonically identifed as a  [[0-truncated]] [[∞-group]] object in $Smooth \infty Grpd$.
Write $\mathbf{B}G \in Smooth \infty Grpd$ for the corresponding 
[[delooping]] object.


+-- {: .un_prop #DeloopedLieGroup}
###### Proposition

A fibrant presentation of the [[delooping]] object $\mathbf{B}G$
in the projective local [[model structure on simplicial presheaves]]
$[CartSp^{op}_{smooth}, sSet]_{proj, loc}$ 
is given by the [[simplicial presheaf]] that is the [[nerve]]
of the one-object [[Lie groupoid]]

$$
  \mathbf{B}G_c := (G \stackrel{\to}{\to} * ) 
$$

regarded as a [[simplicial manifold]] and canonically embedded into 
simplicial presheaves:

$$
  \mathbf{B}G_c : U \mapsto N(C^\infty(U,G) \stackrel{\to}{\to} *)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The presheaf is clearly objectwise a [[Kan complex]], being objectwise
the nerve of a groupoid. It satisfies [[descent]] along [[good open cover]]s
$\{U_i \to \mathbb{R}^n\}$ of [[Cartesian space]]s, because the [[descent]] $\infty$-groupoid $[CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}G)$ is $\cdots \simeq G Bund(\mathbb{R}^n) \simeq G TrivBund(\mathbb{R}^n)$: an object is a [[Cech cohomology|Cech]]
1-cocycle with coefficients in $G$, a morphism a Cech coboundary, which yields the groupoid of $G$-[[principal bundle]]s over $U$, which for the [[Cartesian space]] $U$ is however equivalent to the groupoid of trivial $G$-bundles over $U$.

To show that $\mathbf{B}G$ is indeed the [[delooping]] object of $G$
it is sufficient (by the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#HomotopyLimits">model structure on simplicial presheaves -- homotopy limits</a>)
to compute the [[(∞,1)-pullback]] 
$G \simeq * \times_{\mathbf{B}G} *$ in the global model structure $[CartSp^{op}, sSet]_{proj}$.

This is accomplished by the ordinary [[pullback]] of the 
fibrant replacement diagram 

$$
  \array{
    G &\to& N(G\times G \stackrel{\overset{p_1 \cdot p_2}{\to}}{\underset{p_1}{\to}} G)
    \\
    \downarrow && \downarrow^{\mathrlap{p_2}}
    \\
    * &\to& N(G \stackrel{\to}{\to} *)
  }
$$

as discussed at [[universal principal ∞-bundle]].

=--


#### Strict Lie 2-groups

Let now $G = \Xi[G_2 \to G_1]$ be a strict [[Lie 2-group]] coming from a smooth  [[crossed module]] $G_2 \stackrel{\delta}{\to} G_1 $ with action $\alpha : G_1 \to Aut(G_2)$.


+-- {: .un_prop }
###### Proposition

A fibrant representative of $\mathbf{B}G$ in $[CartSp^{op}, sSet]_{proj,cov}$ is given by the [[crossed complex]]

$$
  \Xi[G_2 \to G_1 \stackrel{\to}{\to} *]
  \,.
$$

=--

+-- {: .proof}
###### Proof

As [above](#LieGroupsDelooping) for Lie groups.

=--



#### Circle Lie $n$-groups {#CircleLienGroup}

+-- {: .un_def }
###### Definition

Write equivalently

$$
  U(1) = S^1 = \mathbb{R}/\mathbb{Z}
$$ 

for the [[abelian group|abelian]] [[Lie group]] called the 
_[[circle group]]_ or _1-dimensional [[unitary group]]_ , regarded as a [[0-truncated]] [[∞-group]] object in $Smooth\infty Grpd$ under the [embedding](#SmoothManifoldEmbeds) $SmoothMfd \hookrightarrow Smooth \infty Grpd$.

For $n \in \mathbb{N}$ the $n$-fold [[delooping]] $\mathbf{B}^n U(1) \in Smooth \infty Grpd$ we call the circle **Lie $(n+1)$-group**.

=--

Write 

$$
  U(1)[n] := [\cdots \to 0 \to C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
  \in
  [CartSp^{op}, Ch^+_\bullet]
$$

for the [[chain complex]] of sheaves concentrated in degree $n$ on $U(1)$.

Recall the right Quillen functor $\Xi : [CartSp^{op}, Ch_\bullet^+] \to [CartSp^{op}, sSet]$ from [above](#DoldKanInclusion).

+-- {: .un_prop }
###### Proposition

The [[simplicial presheaf]] $\Xi(U(1)[n]) \in [CartSp^{op}, sSet]$ is a fibrant representative in $[CartSp^{op},sSet]_{proj,loc}$
of the circle Lie $(n+1)$-group $\mathbf{B}^n U(1)$.

=--

+-- {: .proof}
###### Proof

First notice that since $U(1)[n]$ is fibrant in 
$[CartSp_{smooth}^{op}, Ch_\bullet]_{proj}$ we have that
$\Xi U(1)[n]$ is fibrant in $[CartSp^{op}, sSet]_{proj}$. 
We may compute the [[homotopy pullback]] that defines the [[loop space object]] in the global model structure (by the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#HomotopyLimits">model structure on simplicial presheaves -- homotopy (co)limits</a>) we may check the statement about the delooping in the global model structure.

Consider the global fibration [[resolution]] of the point inclusion $* \to \Xi(U(1)[n])$ given by

$$
  \array{
    \Xi [C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    \\
    \downarrow
    \\
    \Xi [C^\infty(-,U(1)) \to 0  \to 0 \to \cdots \to 0]
  }
  \,.
$$ 

The underlying morphism of chain complexes is clearly degreewise surjective, hence a projective fibration, hence its image under $\Xi$ is a projective fibration. Therefore the [[homotopy pullback]] in question is 
given by the ordinary [[pullback]]

$$
  \array{
    \Xi[0 \to C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    &\to&
    \Xi [C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    \\
    \downarrow && \downarrow
    \\
    \Xi [0 \to 0  \to 0 \to \cdots \to 0]
    & \to &
    \Xi [C^\infty(-,U(1)) \to 0  \to 0 \to \cdots \to 0]
  }
  \,,
$$ 

computed in $[CartSp^{op}, Ch_\bullet]$ and then using that 
$\Xi$ is the [[right adjoint]] and hence preserves pullbacks. This shows that the loop object $\Omega \Xi(U(1)[n])$ is indeed presented by 
$\Xi (U(1)[n-1])$.


Now we discuss the fibrancy of $U(1)[n]$ in the local model structure $[CartSp^{op}, sSet]_{proj,loc}$. We need to check that for all [[good open cover]]s $\{U_i \to U\}$ of a [[Cartesian space]] $U$ we have that the mophism

$$
  C^\infty(U,U(1))[n] \to [CartSp^{op}, sSet](C(\{U_i\}), \Xi U(1)[n])
$$

is an equivalence of Kan complexes, where $C(\{U_i\})$ is the [[Cech nerve]] of the cover. Observe that the Kan complex on the right is that whose vertices are [[cocycle]]s in degree-$n$ [[Cech cohomology]] (see there for details) with coefficients in $U(1)$ and whose morphisms are coboundaries between these.

We proceed by induction on $n$. For $n = 0$ the condition is just that $C^\infty(-,U(1))$ is a [[sheaf]], which clearly it is.
For general $n$ we use that since $C(\{U_i\})$ is cofibrant, the above is the [[derived hom-space]] functor which commutes with [[homotopy pullback]]s and hence with forming [[loop space object]]s, so that

$$
  \pi_1 [CartSp^{op}, sSet](C(\{U_i\}), \Xi (U(1)[n]))
  \simeq
  \pi_0 [CartSp^{op}, sSet](C(\{U_i\}), \Xi (U(1)[n-1]))
$$

by the above result on delooping. So we find that for all $0 \leq k \leq n$ that $\pi_k [CartSp^{op}, sSet](C(\{U_i\}), \Xi(U(1)[n]))$ is the [[Cech cohomology]] of $U$ with coefficients in $U(1)$ in degree $n-k$.
By standard facts about [[Cech cohomology]] (using the [[short exact sequence]] of abelian groups $\mathbb{Z} \to U(1)\to \mathbb{R}$ and the fact that the cohomology with coefficients in $\mathbb{R}$ vanishes in positive degree, for instance by a [[partition of unity]] argument) we have that this is given by the [[integral cohomology]] groups

$$
  \pi_0 [CartSp^{op}, sSet](C(\{U_i\}), \Xi (U(1)[n]))
  \simeq
  H^{n+1}(U, \mathbb{Z})
$$ 

for $n \geq 1$. For the [[contractible]] [[Cartesian space]] all these cohomology groups vanish.

So we have that $\Xi(U(1)[n])(U)$ and $[CartSp^{op}, sSet](C(\{U_i\}), \Xi U(1)[n])$ both have homotopy groups concentrated in degree $n$ on $U(1)$. The above looping argument together with the fact that $U(1)$ is a sheaf also shows that the morphism in question is an isomorphism on this degree-$n$ homotopy group, hence is indeed a [[weak homotopy equivalence]].

=--

+-- {: .un_remark}
###### Remark

In the equivalent presentation of $Smooth\infty Grpd$ by simplicial presheaves on all of [[SmoothMfd]] the objects $\Xi U(1)[n]$ are far from being locally fibrant. Instead, their local fibrant replacements are given by the $n$-stacks of [[circle n-bundle with connection|circle n-bundle]]s.

=--




#### Simplicial Lie groups {#SimplicialSmoothGroups}

Every [[connected]] object $X \in \infty Lie Grpd$ is -- by definition -- the [[delooping]] $X = \mathbf{B}G$ of a Lie [[∞-group]] $G = \Omega X$, its [[loop space object]] formed in $\infty LieGrpd$. Since the discussion of [[group object in an (infinity,1)-category|group objects]], [[loop space  object]]s etc. involves only finite [[limit in a quasi-category|(∞,1)-limits]] and [[∞-stackification]] preserves these, this may be discussed in the [[(∞,1)-category of (∞,1)-presheaves]] on [[CartSp]]. Since there $(\infty,1)$-limits are computed objectwise, an [[∞-group]] object $G$ in $\infty LieGrpd$ is modeled by a [[(∞,1)-presheaf]] with values in [[∞-group]]s in [[∞Grpd]].

By standard results on <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity,1)-category#ModelsInInfGrpd">Models for group objects in ∞Grpd</a> the latter may equivalently be modeled by [[simplicial group]]s. A simplicial group is possibly weak [[∞-groupoid]] equipped with a _strict_ group object structure. While [[strict omega-groupoid|strict ∞-groupoids]] with weak group object structure do not model all [[∞-group]]s, weak $\infty$-groupoids with strict group structure do.

There is a good supply of standard results for and constructions with [[simplicial group]]s which makes this model useful for applications.



### Cohomology and principal $\infty$-bundles {#StrucCohomology}{#Cohomology}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Cohomology">intrinsic cohomology and pricipal ∞-bundles</a> in $Smooth \infty Grpd$.


#### $G$-Principal bundles for $G$ a Lie group


Let $G$ be a Lie group, regarded as a group object in $Smooth \infty Grpd$
as in the [above discussion](#LieGroups).

The [[universal principal ∞-bundle|universal G-principal bundle]] is a replacement of the point inclusion $* \to \mathbf{B}G$ by a fibration $\mathbf{E}G \to \mathbf{B}G$.

For $G$ an ordinary [[group]] one model for this is given by the Lie groupoid

$$
  \mathbf{E}G = (G\times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G)
  \,,
$$

which is the [[action groupoid]] $G//G$ of $G$ acting on itself.

One noteworthy aspect of this object is that it is itself groupal, in fact itself a Lie [[strict 2-group]] in a way that is compatible with the canonical inclusion $G \to \mathbf{E}G$: it is an example of a [[groupal model for universal principal ∞-bundles]].

To emphasize this group structure, we also write $INN(G)$ for this groupoid, following [SchrRob](#http://arxiv.org/abs/0708.1741). The corresponding [[crossed module]] is

$$
 [INN(G)] = (G \stackrel{Id}{\to} G)
 \,.
$$

Accordingly we write $\mathbf{B E}G$ or $\mathbf{B}INN(G)$ for the 2-groupoid given by the Lie [[crossed complex]]

$$
  (G \stackrel{Id}{\to}G \stackrel{\to}{\to} * ) 
  \,.
$$




The following proposition asserts that the general definition of [[principal ∞-bundle]]s in an [[(∞,1)-topos]] $\mathbf{H}$ applied to the coefficient object $\mathbf{B}G$ in $\mathbf{H} = \infty LieGrpd$ for $G$ a [[Lie group]] does reprpduce the ordinary notion of $G$-[[principal bundle]]s.

+-- {: .un_prop }
###### Proposition

Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]]. The ordinary first [[nonabelian cohomology]] of $X$ with coefficients in $G$ coincided with the intrinsic [[cohomology]] of $\infty Lie Grpd$

$$
  H^1(X,G) \simeq \pi_0 \infty LieGrpd(X, \mathbf{B}G)
$$

and the $G$-[[principal bundle]] $P \to X$ corresponding to a [[cocycle]] $X \to \mathbf{B}G$ in $\infty LieGrpd$ is indeed the [[homotopy fiber]] of that cocycle.

=--

+-- {: .proof}
###### Proof

By the discussion at [[model structure on simplicial presheaves]] we have that a cofibrant [[resolution]] for $X$ in the model $[CartSp^{op}, sSet]_{proj,cov}$ for $\infty LieGrpd$ is civen by the [[Cech nerve]] $C\{U_i\}$ of a [[good open cover]] $\{U_i \to X\}$. It follows that $\pi_0 \infty LieGrpd(X,\mathbf{B}G)$ is the [[Cech cohomology]] of $X$ with coefficients in $G$ (see there for details).

Concretely, a cocycle 

$$
  g : C(\{U_i\}) \to \mathbf{B}G
$$

is canonically identified with a transition function

$$
  g : \coprod_{i,j} U_i \cap U_j \to G
$$

satisfying on $U_i \cap U_j \cap U_k$ the cocycle condition $g_{i j} g_{j k} = g_{i k}$.

From this we can compute the [[homotopy fiber]] of $g : C(\{U_i\}) \to \mathbf{B}G$ by forming the ordinaty [[pullback]] of the fibrant replacement $\mathbf{E}G \to \mathbf{B}G$ of the point inclusion $* \to \mathbf{B}G$, where $\mathb{E}G = \mathbf{B}G^{I} \times_{\mathbf{B}G} *$ is the smooth groupoid

$$
  \mathbf{E}G
  = 
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
       \\
       * &&\stackrel{h}{\to}&& *
    }
    \;\;|
    \;\;
    g_1,g_2,h \in G, g_2 = h g_1
  \right\}
  \,.
$$

From this we find the pullback $\hat P$ in


$$
  \array{
    \hat P &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

to be the smooth Lie groupoid

$$
  \hat P
  =
  \left(
  \coprod_{i,j} U_i\cap U_j \times G
  \stackrel{\overset{p_2 \times g_{i,j} \cdot p_3}{\to}}{\underset{p_1 \times P_3}{\to}}
  \coprod_{i} U_i \times G
  \right)
$$

i.e.

$$
  \hat P
  = 
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
       \\
       * &&\stackrel{g_{i j}(x)}{\to}&& *
       \\
       \\
       (x,i) &&\to&& (x,j)  
    }
  \right\}
  \,.
$$

The evident projection $\hat P \to P$ is objectwise a surjective and full and faithful functor.

=--










#### Cohomology of Lie groups {#CohomologyOfLieGroups}

We consider the cohomology in $\mathbf{H}$ of smooth [[delooping]] groupoids $\mathbf{B}G$ for $G$ an ordinary [[Lie group]]. This is a form of [[group cohomology]] for Lie groups.

$$
  H^n(G,A) := \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

We discuss how this related to other definitions of <a href="http://ncatlab.org/nlab/show/group+cohomology#LieGroupcohomology">Lie group cohomology</a> in the literature.

+-- {: .un_defn}
###### Definition
**(naive Lie group cohomology)**

For $G$ a Lie group and $A$ an abelian Lie group and $n \in \mathbb{N}$ define $H^n_{rest}(G,A)$ to be the group of equivalence classes of cocycles given by [[smooth function]]s $G^\times_n \to A$ by coboundatries given by smooth functions $G^{\times_{n-1}} \to A$ subject to the usual relations.

=--

Observe that with $\mathbf{B}G = G^{\times_\bullet}$ regarded as an object of $sPSh(CartSp)$, this is

$$
  H^n_{rest}(G,A)
  =
  \pi_0 sPSh(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

Written this way it is evident that this definition misses to take into account any cofibrant replacement of $\mathbf{B}G$. 

A more refined definition of cohomology of Lie groups has been given by Segal, which was later rediscovered by [[Jean-Luc Brylinski]], following Blanc.

See section 4 of

* [[Chris Schommer-Pries]], _A finite-dimensional String 2-group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))

for a review and applications.


+-- {: .un_defn}

###### Definition
**(differential Lie group cohomology)**

Let $G$ be a [[paracompact space|paracompact]] [[Lie group]] and $A$ an abelian Lie group.

For eack $k \in \mathbb{N}$ we can pick a [[good open cover]] $\{U^{k}_{i} \to G^{\times_k}| i \in I_k\}$ such that

* the index sets arrange themselves into a [[simplicial set]]
  $I : [k] \mapsto I_k$;

* and for $d_j(U^k_i)$ and $s_j(U^k_i)$ the images of the
  face and degeneracy maps of $G^{\times\bullet}$ we have

  $$
    d_j(U^k_i) \subset U^{k-1}_{d_j(i)}
  $$ 

  and

  $$
    s_j(U^k_i) \subset U^{k+1}_{s_j(i)}
    \,.
  $$

For instance start with a [[good open cover]] $\{U^1_i \to G\}$ and define a good open cover $\{U^2_{i_0 i_1 i_2}\}$ of $G \times G$ by $U^2_{i_0 i_1 i_2} := d_0^* U^1_{i_0} \cap d_1^* U^1_{i_1} \cap d_2^* U^1_{i_2}$. And so on.

Then the **<a href="http://ncatlab.org/nlab/show/group+cohomology#LieGroupcohomology">differentiable Lie group cohomology</a>** $H^\bullet_{diffr}(G,A)$ of $G$ with coefficients in 
$A$ is the cohomology of the total complex of the [[Cech cohomology|Cech]]
double complex $C^\infty( U^{\bullet}_{i_0, \cdots, i_\bullet} , A)$
whose differentials are the alternating sums of the face maps 
of $G^{\times_\bullet}$ and of the [[Cech nerve]]s, respectively:

$$
  H^n_{diff}(G,A) := H^n Tot C^\infty( U^{\bullet}_{i_0, \cdots, i_\bullet} , A)
$$


=--

This is ([Brylinski, definition 1.1](#Brylinski)).

As discussed there, this is equivalent to other definitions, notably to a definition given earlier by Segal. 


+-- {: .un_lemma}
###### Observation

There is a natural map

$$
  H^n_{restr}(G,A) \to H^n_{diffr}(G,A)
$$

obtained by pulling back globally defined cocycles and coboundaries to good covers.

=--

We can understand this differentiable Lie group cohomology in terms of maps out of a certain resolution of $\mathbf{B}G$ in $sPSh(CartSp)_{proj,cov}$:

+-- {: .un_prop}
###### Proposition

For $\{U^\bullet_{i_\bullet}\}$ a system of [[good open cover]]s as above, we obtain a simplicial diagram of [[Cech nerve]]s 

$$
  C : [k] \mapsto C(\{U^k_{i}\})
$$

which is degreewise a cofibrant resolution on $sPSh(CartSp)_{proj,cov}$ of $G^{\times_n}$. Its [[bisimplicial set|totalization]] [[coend]] is connected by a zig-zag of weak equivalences in $sPSh(CartSp)_{proj,cov}$ to $\mathbf{B}G$

$$
  \mathbf{B}G
  \stackrel{\simeq}{\leftarrow}
  \stackrel{\simeq}{\to}
  \int^{[k]} \Delta[k] \cdot C(\{U^k_i\})
$$

and we have

$$
  H^n_{diffr}(G,A)
  =
  \pi_0 sPSh(CartSp)(\int^{[k]} \Delta[k] \cdot C(\{U^k_i\}), \mathbf{B}^n A)
  \,.
$$

=--

The proof of this will also show the following

+-- {: .un_prop}
###### Proposition

Write $H^\bullet(G,A) := \pi_0 Sh_{(\infty,1)}(CartSp)(\mathbf{B}G, \mathbf{B}^n A)$ for the intrinsic cohomology of $\mathbf{B}G$ regarded as an object of the $(\infty,1)$-topos of $\infty$-Lie groupoids.

There is a natural morphism

$$
  H^n_{diffr}(G,A) \to H^n(G,A)
  \,.
$$

=--



+-- {: .proof}
###### Proof

Since $\mathbf{B}^n A$ does satisfy descent with respect to [[good open cover]]s of [[Cartesian space]]s (every $(n-1)$ $A$-[[bundle gerbe]] over an $\mathbb{R}^n$ is trivializable), to compute the intrinsic cohomology we have to find a cofibrant replacement for $\mathbf{B}G$.

A cofibrant replacement of any paracompact [[manifold]] $X$ in $[CartSp^{op}, sSet]_{proj,cov}$ is given by the [[Cech nerve]] $C(\{U_i\}) \stackrel{\simeq}{\to} X$ of a [[good open cover]] $\{U_i \to X\}$, because this is evidently a [[local epimorphism]] as described at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CechLocalization">model structure on simplicial presheaves - Cech localization</a>.

Therefore from a choice of compatible families of open covers 
$\{U^k_i \to G^{\times k}\}$ as in the definition of differentiable group cohomology above, we obtain cofibrant replacements

$$
  C(\{U^k_i\}) \stackrel{\simeq}{\to} G^{\times_k}
$$

for each $k$, and arranging themselves into a simplicial simplicial presheaf

$$
  C(\{U^\bullet_i\}) : \Delta^{op} \to [CartSp^{op}, sSet]
  \,,
$$

which is cofibrant in the injective [[model structure on functors]] 
$[\Delta^{op}, [CartSp^{op}, sSet]_{proj,cov}]_{inj}$.

Observe that the fact that this is inded a simplicial diagram in $sPSh(CartSp)$ is due to the extra compatibility condition in the above definition of differentiable Lie group cohomology.

Notice from the discussion at [[model structure on simplicial presheaves]] that we have canonically another cofibrant replacement $Q (G^{\times_n})$ of $G^{\times_n}$ in $[CartSp^{op}, sSet]_{proj}$ which is functorial and has the special property that the [[bisimplicial set|diagonal]]

$$
  \int^{[k] \in \Delta}
  \Delta[k] \cdot Q(G^{\times_k})
  \stackrel{\simeq}{\to}
  \mathbf{B}G
$$

is a cofibrant replacement of $\mathbf{B}G$. Notice that in $[\Delta^{op}, [CartSp^{op}, sSet]_{proj}]_{inj}$ we therefore have a zig-zag of weak equivalences

$$
  C(\{U^\bullet_i\}) \stackrel{\simeq}{\to}
  \stackrel{\simeq}{\leftarrow}
  Q(G^{\times_\bullet})
$$

between cofibrant replacements of $G^{\times_\bullet}$.

Write $\mathbf{\Delta}^\bullet : \Delta \to sSet : [k] \mapsto N(\Delta/[k])$ for the standard [[Bousfield-Kan map|Bousfield-Kan]] cofibrant replacement of the point, hence also of $\Delta$, in $[\Delta, sSet_{Quillen}]_{proj}$ (more discussion of this is at [[homotopy colimit]]).

Then by the fact that the [[coend]] 

$$
  \int (-)\otimes (-) : [\Delta,sSet_{Quillen}]_{proj} \times [\Delta^{op}, [CartSp^{op}, sSet_{Quilen}]_{proj,cov}]_{inj}
  \to 
  [CartSp^{op}, sSet_{Quillen}]_{proj,cov}
$$

over the [[copower|tensoring]] $\otimes sSet_{Quillen} \times [CartSp^{op}, sSet_{Quillen}]_{proj,cov} \to [CartSp^{op}, sSet_{Quillen}]_{proj,cov}$ is a left [[Quillen bifunctor]] (as discussed there), we have weak equivalences in $[CartSp^{op}, sSet]_{proj,cov}$

$$
  \mathbf{B}G
  =
  \int^{[k] \in \Delta}
   \Delta[k] \cdot G^{\times_n}
   \stackrel{\simeq}{\leftarrow}
  \int^{[k] \in \Delta} \Delta[k] \cdot Q(G^{\times_k}))  
   \stackrel{\simeq}{\leftarrow}
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot Q(G^{\times_k}))  
  \stackrel{\simeq}{\to}
  \stackrel{\simeq}{\leftarrow}
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot C(\{U^k_i\}))  
  \stackrel{\simeq}{\to}
  \int^{[k] \in \Delta} \Delta[k] \cdot C(\{U^k_i\}))  
$$

where

* the first one is Dugger's cofibrant replacement mentioned above, even a global weak equivalence;

* the second one is objectwise the [[Bousfield-Kan map]], hence also even a global weak equivalence;

* the zig-zag is the image under the left Quillen functor $\int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot (-)$ (using that $\mathf{\Delta}$ is cofibrant) of the above zig-zag of weak equivalences between cofibrant objects;

* the last one is again the global weak equivalence coming objectwise from the [[Bousfield-Kan map]].

This shows the first claim, that $\mathbf{B}G \stackrel{\simeq}{\leftarrow}\stackrel{\simeq}{\rightarrow} \int^{k} \Delta[k] \cdot C(\{U^k_i\})$.

Moreover, again by the left Quillen bifunctor property of $\int(-)\cdot(-)$ we have that $\int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot C(\{U^k_i\}))$ is cofibrant. Therefore the intrinsic cohomology $H^n(G,A)$ is

$$
  \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
  =
  [CartSp^{op}, sSet]_{proj,cov}
  \left(
    \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot C(\{U^k_i\}))
    ,
    \mathbf{B}^n A
  \right)
  \,.
$$

By pullback along the [[Bousfield-Kan map]] $\mathbf{\Delta[k]} \to \Delta[k]$ we have a natural morphism

$$
  \pi_0 sPSh(\int^{[k]} \Delta[k]\cdot C(\{U^k_i\}), \mathbf{B}^n A) \to H^n(G,A)
  \,.
$$

It remains to show that the set on the left is the differentiable Lie group cohomology.

For that observe that $\mathbf{B}^n A$ is in the image of the [[Dold-Kan correspondence]] $\Xi : [CartSp^{op}, Ch_\bullet] \to [CartSp^{op}, sAb] \stackrel{U}{\to} [CartSp^{op}, sSet]$ of the chain-complex valued presheaf $A[n] = A \otimes_\mathbb{Z} \mathbb{Z}[n]$ to reduce the computation of this simplicial hom-complex to that of a cochain complex:

$$
  \begin{aligned}
    sPSh(K_\bullet, \Xi A[n])
    & \simeq
    \int_U sSet(K_\bullet(U) , U \Xi A(U)[n])
    \\
    & \simeq \int_U sAb(\mathbb{Z} K_\bullet(U), \Xi A(U)[n])
    \\
    &\simeq \int_U Ch_\bullet( C_\bullet(\mathbb{Z} K_\bullet(U)), A(U)\otimes_{\mathbb{Z}}\mathbb{Z}[n] )
    \\
    & \simeq \int_U Ch^\bullet( \mathbb{Z}[n], C^\bullet (Set(K_\bullet(U),A(U))))
    \\
    & \simeq Ch^\bullet (\mathbb{Z}[n], 
       \int_U C^\bullet(Set(K_\bullet(U),A(U)))
    \\
    & \simeq Ch^\bullet(\mathbb{Z}[n], C^\bullet( PSh(K_\bullet, A) )
  \end{aligned}
  \,.
$$

Setting here $K_\bullet = \int^{[k]} \Delta[k] \cdot C(\{U^k_i\})$ and using the [[Eilenberg-Zilber theorem]] to identify the [[Moore complex]] of the [[bisimplicial set|diagonal]] to the [[total complex]] of the double complex of Moore complexes, the claim follows.

=--


#### Smooth nonabelian cohomology in low degree

+-- {: .un_prop}
###### Proposition

Let $G$ be a [[Lie group]] and $\mathbf{B}G \in \mathbf{H} := \infty LieGrpd$ its [[delooping]] as discussed above. Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]]. Then

$$
  \mathbf{H}(X,\mathbf{B}G)
  \simeq
  G Bund(X)
  \,.
$$

is equivalent to the groupoid of smooth $G$-[[principal bundle]]s on $X$. In particular

$$
  H^1(X,G) \simeq \pi_0 \mathbf{H}(X,\mathbf{B}G)
$$

is the [[nonabelian cohomology]] of $X$ with coefficients in $G$. 

If $K$ is any other group with a smooth [[action]] on $X$ and $X//K$ the corresponding Lie [[action groupoid]], then 

$$
  \mathbf{H}(X//K, \mathbf{B}G) \simeq G Bund^K(X)
$$

is the groupoid of $K$-[[equivariant bundle|equivariant]] $G$-[[principal bundle]]s. In particular

Analogously for $G$ a strict [[Lie 2-group]] we have that

$$
  \mathbf{H}(X, \mathbf{B}G) \simeq G Bund(X)
$$

is the [[2-groupoid]] of $G$-[[principal 2-bundle]]s.

=--


+-- {: .proof}
###### Proof

Use that, as discussed above, a cofibrant representative for $X$
in $[CartSp^{op}, sSet]_{proj,cov}$ is given by the [[Cech nerve]]
$C(\{U_i\})$ of a [[good open cover]] $\{U_i \to X\}$.
With that the above statement reduce to statements in 
[[Cech cohomology]] that hold, with the above results on 
the fibrant representative for $\mathbf{B}G$, effectively by defin&#238;tion.

=--





### Concordance {#StrucConcordance}

(...)

### Geometric homotopy and Galois theory {#StrucGeometricHomotopy}

Due to the existence of 
[differentiably good open covers](#DifferentiablyGoodOpenCover)
of [[paracompact manifold|paracompact]] [[smooth manifold]]s
the results about the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]
in  [[ETop∞Grpd]] carry over directly to $Smooth \infty Grpd$.

(...)

### van Kampen theorem {#StrucVanKampen}

(...)

### Paths and geometric Postnikov towers {#StrucPaths}

(...)


### Universal coverings and geometric Whitehead towers {#StrucWhitehead} {#SmoothWhitehead}


Given a [[Lie group]] $G$, we may regard it either as a [[topological group]] and form the [[classifying space]] $\mathcal{B}G \in $ [[Top]] $\simeq$ [[∞Grpd]], or we may form its [[delooping]] [[Lie groupoid]] $\mathbf{B}G \in \infty LieGrpd$, as discussed in the [section on Lie groups](#LieGroups) above.
By the discussion in the [section on geometric realization](#GeometricRealization) we have that under the canonical geometric realization functor

$$
  \Pi : \infty LieGrpd \to \infty Grpd \simeq Top
$$

we have

$$
  \mathcal{B}G \simeq \Pi(\mathbf{B}G)
  \,.
$$

Analogous statements hold for $\infty$-Lie groups. For instance by the same result we have that the [circle n-groupoid](#BnU1) $\mathbf{B}^n U(1)$ maps to the [[Eilenberg-MacLane space]]

$$
  \Pi(\mathbf{B}^n U(1)) \simeq K(\mathbb{Z}, n+1)
  \,.
$$

This means that given a [[cocycle]]

$$
  c : \mathcal{B}G \to K(\mathbb{Z},n+1)
$$

in [[integral cohomology]] (defining a [[characteristic class]]), it is of interest to ask of this morphism also lifts through $\Pi$ to a morphism

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)
  \,.
$$

Classes of examples of such lifts have been described in the section on [integration of ∞-Lie algebra cocycles](#IntegrationOfCocycles). 

By general reasoning, the extensions/[[principal ∞-bundle]]s classified by such cocycles are their [[homotopy fiber]]

$$
  \array{
     \mathbf{B}\hat G &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}G &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^n U(1)
  }
$$

in $\infty LieGrpd$ and

$$
  \array{
     \mathcal{B}\hat G &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathcal{B}G &\stackrel{c}{\to}& K(\mathbb{Z}, n)
  }
$$

in $Top \simeq \infty Grpd$. By the theorem discussed in the section on [Geometric realization](#GeometricRealization) we have that these two homotopy fibers correspond to each other under $\Pi : \infty LieGrpd \to \infty Grpd$:

$$
  \Pi(\mathbf{B}\hat G) \simeq \mathcal{B}\hat G
  \,.
$$

So this means with a smooth lift of a cocycle, we automatically obtain the corresponding  smooth lift of the extension that it classifies (assuming that the simplicial topological group $G$ is well-sectioned). This is notably useful for finding smooth lifts of [[Whitehead tower]]s. Examples of this we discuss in the following.


#### The smooth Whitehead tower of the orthogonal group

Let $O$ denote the [[orthogonal group]], regarded as a [[Lie group]]. We discuss steps of the [[Whitehead tower]] of $O$ refined to $\infty LieGrpd$.

##### First Stiefel-Whitney class

+-- {: .un_prop}
###### Proposition

A lift of the first [[Stiefel-Whitney class]] $w_1 : \mathcal{B}O \to K(\mathbb{Z}_2 ,1) \in Top \simeq \infty Grpd$ to $\infty LieGrpd$ is given by the morphism

$$
  \mathbf{w}_1 : \mathbf{B}O \to \mathbf{B}\mathbb{Z}_2
$$

of [[Lie groupoid]]s that is the delooping of the group homomorphism that sends $g \in O$ to its signature $\sigma(g) \in \mathbb{Z}_2$, where $\sigma(g) = 1$ if $g$ is in the connected component of $O$ (is orientation preserving as an orthogonal map) and $\sigma(g) = -1$ otherwise.

=--

We may compute the [[principal bundle]] in $\infty LieGrpd$ classified by $\mathbf{w}_1$ as the ordinry [[pullback]] of $\mathbf{E} \mathbb{Z}_2 \to \mathbf{B}\mathbb{Z}_2$, where $\mathbf{E}\mathbb{Z}_2$ is the groupoid $\mathbb{Z}_2 \times \mathbb{Z}_2 \stackrel{\ovserset{\cdot}{\to}}{\underset{p_1}{\to} \mathbb{Z}_2}$.

The resulting pullback groupoid

$$
  \array{
    Q &\to& \mathbf{E}\mathbb{Z}_2
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}O &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B}\mathbb{Z}_2
  }
$$

has two objects, $s = +1,-1$ and morphisms of the form $s \stackrel{g}{\to} \sigma(g)\cdot s$ for $g \in O$. The smooth structure is that induced from $O$.

Evidently the canonical embedding $\mathbf{B} SO \to Q$ which sends a morphism $\bullet \stackrel{h}{\to} \bullet$ for $h \in SO$ an element of the [[special orthogonal group]] is an [[essentially surjective functor]] and a [[full and faithful functor]] and hence an equivalence of $\infty$-Lie groupoids. 

This establishes the [[(∞,1)-pullback]] diagram

$$
  \array{
    \mathbf{B} SO &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} O &\stackrel{\mathbf{w}_1}{\to}& 
    \mathbf{B}\mathbf{Z}_2
  }
$$

in $\infty LieGrpd$, covering under $\Pi$ the pullback

$$
  \array{
    \mathcal{B} SO &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathcal{B} O &\stackrel{w_1}{\to}& \mathcal{B}\mathbf{Z}_2
  }
  \,.
$$

##### Second Stiefel-Whitney class

(...)

$$
  \array{
    \mathbf{B} Spin &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}& 
    \mathbf{B}^2 \mathbf{Z}_2
  }
$$

(...)

##### First fractional Pontryagin class {#SmoothFirstFracPontryaginClass}

Let $\mu_3 \in CE(\mathfrak{so}(n))$ be the [[Lie algebra cohomology|Lie algebra 3-cocycle]] 
$\langle -,[-,-]\rangle$ normalized such its left-invariant continuation to a differential 3-form on $Spin(n)$ is the image in [[deRham cohomology]] of a generator of $H^3(Spin, \mathbb{Z})$.

+-- {: .un_prop}
###### Proposition

The [integration of this cocycle](#IntegrationOfCocycles)

$$
  \frac{1}{2}\mathbf{p}_1 := \exp(\mu) : \mathbf{B}Spin \to \mathbf{B}^3 U(1)
$$

is a smooth refinement of the first fractional [[Pontryagin class]] $\frac{1}{2} p_1 : \mathcal{B}Spin \to \mathcal{B}^4 \mathbb{Z}$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[Chern-Simons circle 3-bundle]].

=--


Therefore the [[homotopy fiber]] 

$$
  \array{
    \mathbf{B} String &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} Spin &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}& 
    \mathbf{B}^3 U(1)
  }
$$

is a smooth model of the [[string group]]. 

+-- {: .un_prop}
###### Proposition


Indeed, this homotopy fiber is given by the Lie [[string 2-group]].

=--

+-- {: .proof}
###### Proof

Compute the [[homotopy pullback]] as the ordinary limit over

$$
  \array{
    &\to& \mathbf{E} \mathbf{B}^2 U(1)
    \\
    && \downarrow
    \\
    \mathbf{cosk}_3 \exp(\mathfrak{so}) &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}& 
    \mathbf{B}^3 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}Spin
  }
  \,.
$$


By inspection, this gives the [[Lie 2-group]] whose 

* objects are based paths in $G$; the product is by concatenation of such paths;

* morphisms are equivalence classes of based surfaces in $G$ labeled by some $c \in U(1)$; where two of these are equivalence if there is a ball cobounding them such that the integral of $\mu$ over this ball accounts for the difference in the two labels.

Here me may equivalently take [[thin homotopy]]-classes of paths and surfaces. 
This is indeed one of the three incarnations of the string 2-group as a strict 2-group.

(...)

=--


##### Second fractional Pontryagin class {#SmoothSecondPontryagin}

$$
  \array{
    \mathbf{B} Fivebrane &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} String &\stackrel{\frac{1}{6}\mathbf{p}_2}{\to}& 
    \mathbf{B}^7 U(1)
  }
$$

(...)

* [[fivebrane Lie 6-algebra]]

* [[fivebrane 6-group]]

* [[Chern-Simons circle 7-bundle]]


### Flat $\infty$-connections and local systems {#StrucFlat}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">intrinsic flat cohomology</a> in $Smooth \infty Grpd$.

#### Cohomology with constant coefficients

+-- {: .un_theorem }
###### Theorem

Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]] regarded as a [[0-truncated]] smooth $\infty$-groupoid under the embedding 
$SmoothMfd \hookrightarrow Smooth \infty Grpd$. Let $A \in $ [[∞Grpd]] be any [[∞-groupoid]] and $Disc A \in Smooth \infty Grpd$ the coresponding [[discrete ∞-groupoid]].  

We have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  Smooth\infty Grpd(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   Smooth \infty Grpd(X, Disc A)
$$

=--

+-- {: .proof}
###### Proof

Same proof as of the analogous statement at [[ETop∞Grpd]].

=--

#### With coefficients in ${\mathbf{B}^n U(1)}$ 

Let $\mathbf{B}^n U(1)$ be the circle $(n+1)$-Lie group
as discussed [above](#CircleLienGroup). Recall the notation and 
model category presentations as discussed there.

+-- {: .un_prop #FlatCohomologyWithCoeffsInCircle}
###### Proposition

For $n \geq 1$ a fibration presentation in $[CartSp^{op}, sSet]_{proj}$ of the 
canonical morphism $\mathbf{\flat} \mathbf{B}^n U(1) \to \mathbf{B}^n U(1)$
in $Smooth \infty Grpd$ is given by the image under $\Xi : [CartSp^{op}, Ch_\bullet^+] \to [CartSp^{op}, sSet]$ of

$$
  \array{
    C^\infty(-,U(1)) &\stackrel{d_{dR}}{\to}& \Omega^1(-) &\stackrel{d_{dR}}{\to} & \cdots &\stackrel{d_{dR}}{\to}& \Omega^n_{cl}(-)
    \\
    \downarrow && \downarrow && && \downarrow
    \\
    C^\infty(-, U(1)) &\to& 0 &\to& \cdots &\to& 0
  }
  \,,
$$

where at the top we have the _flat_ [[Deligne cohomology|Deligne complex]]. 

=--

+-- {: .proof}
###### Proof

It is clear that the morphism of chain complexes is an objectwise 
surjection and hence maps to a projective fibration under $\Xi$.
It remains to observe that the flat Deligne complex is a presentation
of $\mathbf{\flat} \mathbf{B}^n U(1)$:

By the discussion at [[∞-cohesive site]] we have that $\mathbf{\flat} = Disc \Gamma$ is given on fibrant objects by first evaluating on the point and then extending back to a constant simplicial presheaf. By the [above discussion](#CircleLienGroup) we have that $\Xi (U(1)[n])$ is indeed fibrant, and so a fibrant presentation of $\mathbf{\flat} \mathbf{B}^n U(1)$ is given by the _constant_ presheaf $U(1)_{const} [n] : U \mapsto \Xi(U(1)[n])$.

The inclusion $U(1)_{const}[n] \to U(1)[n]$ is not yet a fibration. But by a basic fact of [[abelian sheaf cohomology]] -- using the [[Poincare lemma]] -- we have a global weak equivalence $U(1)[n]_{const} \stackrel{\simeq}{\to} [C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]$ that factors this inclusion by the above fibration.
 
=--

#### With coefficients in $\mathbf{B}G$ for $G$ a Lie group 

Let $G$ be a [[Lie group]] regarded as a [[0-truncated]] [[∞-group]]
in $Smooth \infty Grpd$. Write $\mathfrak{g}$ for its [[Lie algebra]].
Write $\mathbf{B}G \in Smooth \infty Grpd$ for its [[delooping]].
Recall the fibrant presentation 
$\mathbf{B}G_c \in [CartSp_{smooth}^{op}, sSet]_{proj,loc}$ from 
[above](#DeloopedLieGroup).

{#LieGroupFlatCoefficients}

+-- {: .un_prop #LieGroupFibrantFlatInclusion}
###### Proposition

The object 
$\mathbf{\flat}\mathbf{B}G \in Smooth \infty Grpd$ has a fibrant 
presentation $\mathbf{\flat} \mathbf{B}G_{c} \in [CartSp^{op}, sSet]_{proj,loc}$ given by the [[groupoid of Lie-algebra valued forms]]

$$
  \mathbf{\flat}\mathbf{B}G _{c}
  =
  N
  \left(
    C^\infty(-,G)\times \Omega^1_{flat}(-,\mathfrak{g}) 
   \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1^{-1} d p_1}{\to}}{\underset{p_2}{\to}} \Omega^1_{flat}(-,\mathfrak{g})
  \right)
$$

and this is such that the canonical morphism 
$\mathbf{\flat} \mathbf{B}G \to \mathbf{B}G$ is presented by the canonical 
morphism of simplicial presheaves 
$\mathbf{\flat}\mathbf{B}G_{c} \to \mathbf{B}G_{c}$ which is a fibration
in $[CartSp_{smooth}^{op}, sSet]_{proj}$.

=--

+-- {: .un_remark}
###### Remark

This means that a $U$-parameterized family of objects of 
$\mathbf{\flat}\mathbf{B}G_{c}$ is given by a 
[[Lie-algebra valued 1-form]] $A \in \Omega^1(U)\otimes \mathfrak{g}$ whose [[curvature]] 2-form $F_A = d_{dR} A + [A ,\wedge A]  = 0$ vanishes,  
and a $U$-parameterized family of morphisms $g : A \to A'$ is given by a smooth function $g \in C^\infty(U,G)$ such that $A' = Ad_g A + g^{-1} d g$, where $Ad_g A = g^{-1} A g$ is the [[adjoint action]] of $G$ on its 
[[Lie algebra]], and where $g^{-1} d g := g^* \theta$ is the pullback of the [[Maurer-Cartan form]] on $G$ along $g$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[∞-cohesive site]] we have that 
$\mathbf{\flat} \mathbf{B}G$ is presented by the simplicial presheaf
that is constant on the [[nerve]] of the one-object [[groupoid]]
$$
  G_{disc} \stackrel{\to}{\to} *
  \,,
$$
for the [[discrete group]] underlying the [[Lie group]] $G$.
The canonical morphism of that into $\mathbf{B}G_c$ is however 
not a fibration.

We claim that the canonical inclusion
$N(G_{disc}\stackrel{\to}{\to}) \to \mathbf{\flat} \mathbf{B}G_{c}$
factors the inclusion into $\mathbf{B}G_c$ by a weak equivalence followed
by a global fibration.

To see the weak equivalence, notice that it is objectwise an [[equivalence of groupoids]]: it is [[essentially surjective functor|essentially surjective]] since every flat $\mathfrak{g}$-valued 1-form on the [[contractible]] $\mathbb{R}^n$ is of the form $g d g^{-1}$ for some function $g : \mathbb{R}^n \to G$ (let $g(x) = P \exp(\int_{0}^x) A$ be the [[parallel transport]] of $A$ along any path from the origin to $x$). Since the [[gauge transformation]] [[automorphism]] of the trivial $\mathfrak{g}$-valued 1-form are precisely given by the constant $G$-valued functions, this is also objectwise a [[full and faithful functor]]. 

Similarly one sees that the map $\mathbf{\flat}\mathbf{B}G_c \to \mathbf{B}G$ is a fibration.

Finally we need to show that $\mathbf{\flat}\mathbf{B}G_c$ is fibrant in $[CartSp^{op}, sSet]_{proj,loc}$. This can be seen by observing that this sheaf is the coefficient object that in [[Cech cohomology]] computes $G$-[[principal bundle]]s with flat [[connection on a bundle|connection]] and then reasoning as above: every $G$-principal bundle with flat connection 
on a [[Cartesian space]] is equivalent to a trivial $G$-principal bundle whose connection is given by a globally defined $\mathfrak{g}$-valued 1-form. Morphisms between these are precisely $G$-valued functions that act on the 1-forms by gauge transformations as in the [[groupoid of Lie-algebra valued forms]].

=--



### de Rham cohomology {#StrucDeRham}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#deRhamCohomology">intrinsic de Rham cohomology</a>
in $Smooth \infty Grpd$.


#### With coefficients in $\mathbf{B}^n U(1)$ or $\mathbf{B}^n \mathbb{R}$

Let $\mathbf{B}^n U(1)$ be the circle Lie $(n+1)$-group, as 
discussed [above](#CircleLienGroup). Recall the notation and 
model category presentations from the discussion there.

+-- {: .un_prop #OrdinaryDeRham}
###### Proposition

A fibrant representative in $[CartSp^{op}, sSet]_{proj,loc}$ of 
the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#deRhamCohomology">de Rham coefficent object</a> 
$\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ as well as
$\mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}$
is given by the 
truncated [[de Rham complex]] of sheaves of abelian groups of
[[differential form]]s

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn}
  :=
  \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{chn}
  :=
  \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2(-) \stackrel{d_{dR}}{\to}\cdots \to \Omega^{n-1}(-) \stackrel{d_{dR}}{\to}\Omega^n_{cl}(-)]
  \,.
$$

=--


+-- {: .proof}
###### Proof

By definition 
and the fact that homotoppy pullbacks in the local
structure may be computed in global structure
(discussed [here](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#HomotopyLimits))
the object $\mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn}$
is given, up to equivalence, by the [[homotopy pullback]] 
in $[CartSp^{op}, Ch_\bullet]_{proj}$
of the inclusion $U(1)_{const}[n] \to U(1)[n]$ along the point inclusion
$* \to U(1)[n]$. We may compute this as the ordinary pullback
after passing to a [[resolution]] of this inclusion by a fibration.
By the [above discussion](#FlatCohomologyWithCoeffsInCircle) of
flat cohomology with coefficients in $\mathbf{B}^n U(1)$ such a 
fibration replacement is given by the map from the flat Deligne
complex. Using this we find the ordinary [[pullback]] diagram

$$
  \array{
    \Xi[0 \to \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]
    &\to&
    \Xi[C^\infty(-,U(1)) \to \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]
    \\
    \downarrow && \downarrow
    \\
    \Xi[0 \to 0 \to \cdots \to 0]
    &\to&
    \Xi[C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
  }
  \,.
$$


=--

##### On smooth manifolds

Let $X$ be a [[smooth manifold]] regarded under the embedding
$SmoothMfd \hookrightarrow Smooth \infty Grpd$.

Write $H^n_{dR}(X)$ for the ordinary [[de Rham cohomology]]
of $X$.

+-- {: .un_prop}
###### Proposition

For $n \in \mathbb{N}$ we have isomorphisms

$$
  \pi_0 Smooth \infty Grpd(X, \mathbf{\flat}_{dR} \mathbf{B}^n U(1))
  \simeq
  \left\{
     \array{
        H^n_{dR}(X) &| n \geq 2
        \\
        \Omega^1_{cl}(X) &| n = 1
        \\
        0 &| n = 0
     }
   \right.
$$

=--

+-- {: .proof}
###### Proof

Let $\{U_i \to X\}$ be a [[good open cover]]. By the disucssion at [[model structure on simplicial presheaves]] the [[Cech nerve]] $C(\{U_i\}) \to X$ is a cofibrant [[resolution]] of $X$ in $[CartSp^{op}, sSet]_{proj,loc}$. Therefore we have for all $n$

$$
  Smooth \infty Grpd(X,\mathbf{\flat}_{dR} \mathbf{B}^n U(1))
  \simeq
  [CartSp^{op}, sSet](C(\{U_i\}), \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)])
  \,.
$$

The right hand is the $\infty$-groupoid of cocylces in the [[Cech cohomology|Cech]] [[hypercohomology]] of the truncated complex of sheaves of differential forms. A cocycle is given by a collection

$$
  (C_i, B_{i j}, A_{i j k}, \cdots  , Z_{i_1, \cdots, i_n})
$$

of differential forms, with $C_i \in \Omega^n_{cl}(U_i)$, $B_{i j} \in \Omega^{n-1}(U_i \cap U_j)$, etc. , such that this collection is annihilated by the total differential $D = d_{dR} \pm \delta$, where $d_{dR}$ is the de Rham differential and $\delta$ the alternating sum of the pullbacks along the face maps of the [[Cech nerve]].

It is a standard result of [[abelian sheaf cohomology]] that such cocycles represent classes in de Rham cohomology. 

But for the record and since the details of this computation will show up again at some mildly subtle points in further discussion below, we spell this out in some detail.

For $n = 1$ and $n= 0$ our truncated de Rham complex degenerates to 
$\mathbf{\flat}_{dR}\mathbf{B}U(1)_{chn} = \Xi[\Omega^1_{\mathrm{cl}}(-)]$
and
$\mathbf{\flat}_{dR}U(1)_{chn} = \Xi[0]$, respectively, which obviously has the cohomology as claimed above.

For $n \geq 2$ we can explicitly construct coboundaries connecting such a generic cocycle  to one of the form 

$$
  (F_i, 0, 0, \cdots, 0)
$$

by using a [[partition of unity]] $(\rho_i \in C^\infty(X))$ subordinate to the cover $\{U_i \to X\}$, i.e. $x \in U_i \Rightarrow \rho_i(x) = 0$ and $\sum_i \rho_i = 1$.

For consider 

$$
  \begin{aligned}
     & (C_i, B_{i j}, A_{i j k}, \cdots  , Y_{i_1, \cdots, i_{n}}, Z_{i_1, \cdots, i_{n+1}})
     \\
     + & D (0, 0, \cdots, \sum_{i_0} \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}},0)
     \\
     =
     & (C_i, B_{i j}, A_{i j k}, \cdots  , Y_{i_1, \cdots, i_{n}}
     + d_{dR}\sum_{i_0} \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}}, 0)   
  \end{aligned}
  \,,
$$

where we use that from $(\delta Z)_{i_1, \cdots, i_{n+2}} = 0$ it follows that

$$
  \begin{aligned}
    (\delta \sum \rho Z)_{i_1, \cdots, i_{n+1}}
    &=
    \sum_{i_0} \rho_{i_0}
    \sum_{k = 1}^{n+1}
    (-1)^k
    Z_{i_0, i_1 \cdots, \hat i_k, \cdots, i_{n+1}}
    \\
    & =
    \sum_{i_0} \rho_{i_0}
    Z_{i_1 ,\cdots, i_{n+1}}    
    \\
    & =
    Z_{i_1 ,\cdots, i_{n+1}}
  \end{aligned}
  \,.
$$

> where I am suppressing some evident signs...

By recurseively adding coboundaries this way, we can annihilate all the higher Cech-components of the original cocycle and arrive at a cocycle of the form $(F_i, 0, \cdots, 0)$. 

Such a cocycle being $D$-closed says precisely that $F_i = F|_{U_i}$ for $F \in \Omega^n_{cl}(X)$ a globally defined closed differential form. Moreover, coboundaries between two cocycles both of this form 

$$
  (F_i, 0, \cdots , 0) = (F'_i, 0, \cdots, 0) + D(\lambda_i, \lambda_{i j}, \cdots)
$$

are necessarily themselves of the form $(\lambda_i, \lambda_{i j}, \cdots) =  (\lambda_i, 0 ,\cdots, 0)$ with $\lambda_i = \lambda|_{U_i}$ for $\lambda \in \Omega^{n-1}(X)$ a globally defined differential $n$-form and $F = F' + d_{dR} \lambda$.

=--


##### On  $\mathbf{B}^n U(1)$ 



+-- {: .un_prop #DeRhamBnU1}
###### Proposition

For $n \geq 1$ we have that the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#deRham">intrinsic de Rham cohomology</a> of the <a href="BnU1">circle n-groupoid</a> $\mathbf{B}^n U(1)$ in $\mathbf{H} = \infty LieGrpd$ is concentrated in degree $(n+1)$, where it is  $\mathbb{R}$:

$$
  H(\mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k} U(1) )
  =
  \left\{
    \array{
       \mathbb{R} & for \; k = n+1
       \\
       0 & otherwise
    }
  \right.
$$

=--

+-- {: .un_remark }
###### Remark

By the discussion at [circle n-group -- differential coefficients](#DifferentialBnU1) above, we have that $\mathbf{\flat}_{dR} \mathbf{B}^k U(1) \simeq \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}$, reflecting the familiar fact that since $Lie(U(1)) \simeq Lie(\mathbb{R})$ we have that $Lie(U(1))$-valued forms are naturally identified with plain $\mathbb{R} = Lie(\mathbb{R})$-valued forms. Therefore the above may equivalently be restated as

$$
  H^{k}_{dR}(\mathbf{B}^n U(1))
  :=
  H(\mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k} \mathbb{R} )
  =
  \left\{
    \array{
       \mathbb{R} & for \; k = n+1
       \\
       0 & otherwise
    }
  \right.
  \,.
$$


=--

+-- {: .proof}
###### Proof

Since both domain and codomain are abelian, it will be sufficient to demonstrate the statement for $n = 1$, $k$ arbitrary, and for $k = 1$, $n$ arbitrary. All other combinations of $n$ and $k$ are then implied by repeatedly using the [[delooping]]/[[loop space object|looping]] [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(\Sigma \dashv \Omega)$  on abelian objects in

$$
  \begin{aligned}
    \mathbf{H}(\mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k}U(1))
    &
    \simeq
    \mathbf{H}(\mathbf{B}^n U(1), \Omega \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
    \\
    & \simeq
    \mathbf{H}(\Sigma \mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
    \\
    & \simeq
    \mathbf{H}(\mathbf{B}^{n+1} U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
  \end{aligned}
  \,.
$$

Here we use that since $\mathbf{\flat}_{dR}$ is a [[right adjoint]], it commutes with forming [[loop space object]]s.

Using this, the main work in proving the theorem is involved in establishing the statement for $k = n+1 = 2$, which we now spell out.
We note that this would be easy to prove if we did not have to pass to a cofibrant [[resolution]] of $\mathbf{B}^n U(1)$ for computing the [[derived hom-space]] in the projectve [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,cov}$. For then we would compute, using the [above](#DifferentialBnU1) fibrant model for $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$

$$
  \begin{aligned}
    & [CartSp^{op}, sSet](\;\;\Xi(C^\infty(-U(1))[n]), \;\;\Xi[\Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]\;\;)
    \\
    & \simeq
    [CartSp^{op}, Ch_\bullet](\;\; N \Xi(C^\infty(-U(1))[n]), \;\;\Omega^1(-) \to \cdots \to \Omega^n_{cl}(-) \;\;)
    \\
    & \simeq
    [CartSp^{op}, Ch_\bullet](\;\; C^\infty(-U(1))[n], \;\; \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-) \;\; )
   \\
    &\simeq
    [CartSp^{op}, Ab](\;\; C^\infty(-,U(1)), \;\; \Omega^1(-) \;\;)
  \end{aligned}
  \,,
$$

where $\Xi : [CartSp^{op}, Ch_\bullet] \to [CartSp^{op}, sSet]$ is the [[Dold-Kan correspondence]] map.

To see what this last set is, notice that if we forgot the abelian group structure, and looked at the last hom-set as one of sheaves, we find by the [[Yoneda lemma]] that is is the set $\Omega^1(U(1))$ of 1-forms. Among these the forms $\omega \in \Omega^1(U(1))$ that do respect the group structure are those such that for all $U \in CartSp$ and all $f,g : U \to U(1)$ we have

$$
  f^* \omega + g^* \omega = (f \cdot g)^* \omega
  \,.
$$

A little reflection shows that this is satisfied precisely by the constant forms, i.e. those that are a linear multiple of the [[Maurer-Cartan form]] on $U(1)$. Hence the above hom-complex is indeed just

$$
  \cdots \simeq \mathbb{R}
  \,.
$$

But $\mathbf{B}^n U(1)$ is not cofibrant in $[CartSp^{op}, sSet]_{proj}$. We will pass now to a cofibrant [[resolution]] and discuss that computing the homs out of that does nevertheless reduce to the above computation.

By Dugger's <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantReplacement">construction of cofibrant replacements in the projective model structure</a> we have that a cofibrant replacement for a simplciial presheaf $A$ is given by the diagonal of the [[bisimplicial set|bisimplicial presheaf]] which in degree $(n,k)$ has

$$
  \coprod_{U_n \to U_{n-1} \to \cdots \to U_0 \to A_k} U_n
  \,,
$$

where the coproduct ranges over all sequences of morphisms of representables $U_i \in CartSp$ into $A_k$. And face and degeneracy maps are the evident ones. 

So we prove now that the computation of $\mathbf{H}(\mathbf{B}U(1), \mathbf{\flat}_{dR}\mathbf{B}^2 U(1))$ does reduce to the above computation of morphisms out of $\mathbf{B}U(1)$. Write $Q(\mathbf{B}^1 U(1)) \stackrel{\simeq}{\to} \mathbf{B}^n U(1)$ for the above cofibrant replacement. 

Then a morphism $Q(\mathbf{B} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1))$ is a collection of horizontal morphisms in the diagram

$$
  \array{
     \Delta[2] &\to& \coprod_{U_0 \to U_1 \to U:2 \to U(1)} \Omega^2_{cl}(U_0) \times \Omega^1(U_0)\times \Omega^1(U_0)
     \\
     \downarrow \downarrow \downarrow &&
     \downarrow \downarrow \downarrow
     \\
     \Delta[1] &\to& \coprod_{U_0 \to U_1 \to U(1)} \Omega^2_{cl}(U_0) \times \Omega^1(U_0)
     \\
     \downarrow \downarrow &&
     \downarrow \downarrow
     \\
     \Delta[0]
     &\to&
     \coprod_{U_0 \in CartSp} \Omega^2_{cl}(U_0)
  }
$$

Explicitly, such a cocycle is

* a collection $\{\lambda_{U} \in \Omega^2_{cl}(U) | U \in CartSp\}$;

* a collection $\{\omega_{U_0 \to U_1 \to U(1)} \in \Omega^1(U_9)\}$ 

such that 

* for all $f : U_0 \to U_1$ we have
  $f^* \lambda \lambda_{U_1}  = 
  \lambda_{U_0} + \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}$;

* for all $U_0 \stackrel{f}{\to} U_1 \to U_2 \to U(1)\times U(1)$ we have
  
  $$
    \omega_{U_0 \to U_1 \to U(1)\times U(1) \stackrel{p_1}{\to} U(1)}
    + 
    f^* \omega_{U_1 \to U_2 \to U(1) \times U(1) \stackrel{p_2}{\to} U(1)}
    =
    \omega_{U_0 \to U_2 \to U(1) \times U(1) \stackrel{\cdot}{\to} U(1)}
  $$

* for all $U$ we have $\omega_{U \stackrel{Id}{\to} U \to \stackrel{e}{\to} U(1)} = 0$.

A coboundary between two such cocycles is 

* for all $U \in CartSp$ a $\kappa_U \in \Omega^1(U)$

such that

* $\lambda'_U = \lambda_U + d \kappa_U$;

* $\omega'_{U_0 \stackrel{f}{\to} U_1 \to U(1)} = \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)} + f^* \kappa_{U_1} - \kappa_{U_0}$.

We claim that any such cocycle $(\lambda,\omega)$ is coboundant to 
one such that

* for all $U$ we have $\lambda_U = 0$;

* for all $U_0 \stackrel{f}{\to} U(1)$ we have 
  $\omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)} = 0$.

The coboundary establishing this is given by setting

$$
  \kappa_U := \omega_{U \to * \stackrel{e}{\to} U(1)}
  \,.
$$ 

This follows from the cocycle law for for maps of the form 

$$
  \array{
    && U_1
    \\
    & {}^{\mathrlap{f}}\nearrow && \searrow
    \\
    U_0 &&\to&& *
    \\
    & {}_{\mathllap{const_{e,e}}}\searrow && \swarrow_{\mathrlap{const_{e,e}}}
    \\
    &&
    U(1) \times U(1)
  }
$$

which asserts that

$$
  \omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)}
  =
  \omega_{U_0 \to * \stackrel{e}{\to} U(1)}
  -
  f^* \omega_{U_1 \to * \stackrel{e}{\to} U(1)}
  \,.
$$

Moreover we claim that such cocycles with $\lambda_U = 0$ for all $U$ and $\omega_{U_0 \to U_1 \stackrel{e}{\to} U(1)}$ for all $U_0 \stackrel{f}{\to} U_1$ have no nontrivial morphisms between them, which means that these do constitute unique representatives of their cohomology classes. This is because such a morphism would be given by a collection $\kappa_U \in \Omega^1_{cl}(U)$ of closed 1-forms for each $U \in CartSp$, such that in particular for all $U_0 \stackrel{f}{\to} U_1 $ we'd have
$\kappa_{U_0} = f^* \kappa_{U_1}$. Clearly for any choice of $\kappa_U$s, one can find $f$ such that this is not satisfied. For instance simply take $f : U \to *$, which imposes the relation $\kappa_U = 0$ explicitly.

This shows that the cohomology in question is the set of cocycles as above, satisfying the two extra constraints. Now using the cocycle law for the diagram

$$
  \array{
    && U_0
    \\
    & {}^{\mathllap{Id}}\nearrow && \searrow^{\mathrlap{f}}
    \\
    U_0 &&\to&& U_1
    \\
    & {}_{(h,const_e)}\searrow && \swarrow_{\mathrlap{(g,const_e)}}
    \\
    &&
    U(1) \times U(1)
  }
$$

we find 

$$
  \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}
  =
  \omega_{U_0 \stackrel{Id}{\to} U_0 \to U(1)}
  + 
  \omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)}
$$

and using it for

$$
  \array{
    && U_1
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{Id}}
    \\
    U_0 &&\to&& U_1
    \\
    & {}_{(const_e,h)}\searrow && \swarrow_{\mathrlap{(const_e,g)}}
    \\
    &&
    U(1) \times U(1)
  }
$$

we find

$$
  \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}
  =
  \omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)}
  + 
  f^* \omega_{U_1 \stackrel{Id}{\to} U_1 \to U(1)}
  \,.
$$

In view of the above gauge condition this is equivalently

$$  
  \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}
  =
  \omega_{U_0 \stackrel{Id}{\to} U_0 \to U(1)}
  =
  f^* \omega_{U_1 \stackrel{Id}{\to} U_1 \to U(1)}  
  \,.
$$

This says that $\omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)} =: \omega_{U_0 \to U(1)}$ in fact only depends on the domain of $f$, hence only on the map $h : U_0 \to U(1)$ and that as such these forms constitute the components of a morphism of sheaves

$$
  C^\infty(-,U(1)) \to \Omega^1(-)
  \,.
$$

But this means that the cocycle $Q(\mathbf{B}U(1)) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ indeed factors through $Q(\mathbf{B}U(1)) \to \mathbf{B}U(1)$ and therefore the naive computation at the beginning indeed applies and shows that these cocycle are in bijection with multiples of the standard [[Maurer-Cartan form]] on $U(1)$, hence with $\mathbb{R}$, so that

$$
  H(\mathbf{B}U(1), \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)) = 
  \mathbb{R}
  \,.
$$

The same kind of argument as above shows that for $k \geq 2$ cocycles $Q(\mathbf{B}U(1)) \to \mathbf{\flat}_{dR}\mathbf{B}^k U(1)$ have underlying them sheaf morphisms $C^\infty(-,U(1)) \to \Omega^{k-1}(-)$. But all these are necessarily trivial, due to the fact that $U(1)$ is 1-dimensional. This establishes the theorem for $n=1$ and arbitrary $k$.


Finally the same argument that above showed that no nontrivial automorphisms of certain cocycles exist shows the theorem for $k=1$ and arbitrary $n \geq 1$, namely that no nontrivial morphisms $Q(\mathbf{B}^n  U(1)) \to \mathbf{\flat}_{dR} \mathbf{B}U(1)$ exist: such are given by a collection of 1-forms $\lamba_U \in \Omega^1(U)$ for all $U$, satisfyine for all possible maps $f : U_0 \to U_1$ the relation $\lambda_{U_0} = f^* \lambda_{U_1}$. If $\lambda_{U}$ does not vanish for all $U$, one can always find some $f$ for which this is not satisfied.  


=--




#### With coefficients in $\mathbf{B}G$ for a Lie group $G$ 

Let $G$ be a [[Lie group]]. Write $\mathfrak{g}$ for its 
[[Lie algebra]].


+-- {: .un_prop #LieGroupDeRhamCoefficients}
###### Proposition

The object $\mathbf{\flat}_{dR}\mathbf{B}G \in Smooth \infty Grpd$
has a fibrant presentation in $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ 
by the [[sheaf]] 
$\mathbf{\flat}\mathbf{B}G_c = \Omega^1_{flat}(-, \mathfrak{g})$ of 
[[groupoid of Lie-algebra valued forms|flat Lie-algebra valued forms]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}G_c
  :
  U \mapsto \Omega^1_{flat}(U,\mathfrak{g})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By a [proposition above](#LieGroupFibrantFlatInclusion) we have a
fibration $\mathbf{\flat}\mathbf{B}G_c \to \mathbf{B}G_c$
in $[CartSp_{smooth}^{op}, sSet]_{proj}$ modeling the canonical 
inclusion $\mathbf{\flat}\mathbf{B}G \to \mathbf{B}G$. Therefore
we may get a presentation for the defining [[(∞,1)-pullback]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}G  := * \times_{\mathbf{B}G} \mathbf{\flat} \mathbf{B}G
$$

in $Smooth \infty Grpd$ by the ordinary [[pullback]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}G_c 
  \simeq * \times_{\mathbf{B}G_c} \mathbf{\flat} \mathbf{B}G_c
$$

in $[CartSp^{op}, sSet]$.

The resulting simplicial presheaf is fibrant in $[CartSp^{op}, sSet]_{proj,loc}$ because it is a [[sheaf]].

=--


+-- {: .un_remark }
###### Remark

Writing $T U$ for the [[tangent Lie algebroid]] of $U$ 
we may equivalently write

$$
  \mathbf{\flat}_{dR} \mathbf{B}G_ : U \mapsto Hom(T U, \mathfrak{g})
  \,,
$$ 

where on the right we have the set of morphisms of [[Lie algebroid]]s. Equivalently in terms of [[Chevalley-Eilenberg algebra]]s this is 

$$
  \mathbf{\flat}_{dR} \mathbf{B}G_c : 
  U \mapsto Hom_{dgAlg}(CE(\mathfrak{g}),(\Omega^\bullet(U), d_{dR}))
  \,,
$$ 

=--


+-- {: .un_prop #LieGroupDeRhamCohomology}
###### Corollary

For $X \in $ [[SmoothMfd]] $\hookrightarrow Smooth \infty Grpd$ we find
the intrinsic de Rham cohomology set

$$
  H^1_{dR, Smooth}(X, G)
  :=
  \pi_0 Smooth \infty Grpd(X, \mathbf{\flat}_{dR} \mathbf{B}G)
  \simeq
  \Omega^1_{flat}(X, \mathfrak{g})
$$

is the set of smooth flat $\mathfrak{g}$-valued differential forms on $X$.

=--

#### With coefficients in $\mathbf{B}G$ for $G$ a strict 2-group



We work out, following the [general definition](#CoeffsLieAlgForms) the coefficient object for [[2-groupoid of Lie 2-algebra valued forms|Lie 2-algabra valued forms]] $\mathbf{\flat}_{dR} \mathbf{B}[G_2\to G_1]$ for $(G_2 \to G_1)$ a Lie [[crossed module]].

Let $\Xi : CrsdCplx \to KanCplx$ now denote the inclusion of [[crossed complex]]es into all [[Kan complex]]es/[[∞-groupoid]]s.


Write $[\mathfrak{g}_2 \stackrel{\delta_*}{\to} \mathfrak{g}_1]$ for the corresponding [[differential crossed module]] with action $\alpha_* : \mathfrak{g}_1 \to der(\mathfrak{g}_2)$ corresponding to the Lie [[strict 2-group]] [[crossed module]] $(G_2 \stackrel{\delta}{\to} G_1)$ with action $\alpha : G_1 \to Aut(G_2)$. 

+-- {: .un_prop }
###### Proposition

The Lie [[2-groupoid]] $\mathbf{\flat} \mathbf{B}[G_2 \stackrel{\delta}{\to} G_1]$ is represented in $[CartSp^{op}, sSet]$ by the Lie [[2-groupoid]] which on $U \in CartSp$ s the following 2-groupoid:

* An [[object]] is a pair 

  $$
    A \in \Omega^1(U,\mathfrak{g}_1)\,, \;\;\;
    B \in \Omega^2(U,\mathfrak{g}_2)
  $$ 
  
  such that 

  $$
    \delta_* B - d A + [A \wedge A] = 0
  $$

  and

  $$
    d B + [A \wedge B] = 0
    \,.
  $$

* A 1-[[morphism]] $(g,a) : (A,B) \to (A',B')$ is a pair

  $$  
    g \in C^\infty(U,G_1)\,,\;\;\; a \in \Omega^1(U,\mathfrak{g}_2)
  $$

  such that

  $$
    A' = g^{-1} A g + g^{-1} d g + g^{-1} \delta_* a g
  $$

  and

  $$
    B' = \alpha_{g^{-1}}(
      B + d a + [a \wedge a] + \alpha_*(A \wedge a)
    )
    \,.
  $$

  The composite of two 1-morphisms

  $$
    (A,B) \stackrel{(g_1,a_1)}{\to} (A',B') \stackrel{(g_2,a_2)}{\to}
    (A'', B'')
  $$

  is given by the pair

  $$
    (g_1 g_2, a_1 + (\alpha_{g_2})_* a_2)
    \,.
  $$

* a [[2-morphism]] $f : (\lambda,a) \to (\lambda', a')$ is a function

  $$
    f \in C^\infty(U,G_2)
  $$

  such that 

  $$
    g' = \delta(f)^{-1} \cdot g 
  $$
 
  and

  $$
    a' = f^{-1} d f + f^{-1} a f + f^{-1}(r_f^{-1} \circ \alpha_f)_*(a)f
  $$

and composition is defined as follows

(...)

=--

This is the [[2-groupoid of Lie 2-algebra valued forms]] as described in [definition 2.11](http://arxiv.org/PS_cache/arxiv/pdf/0802/0802.0663v3.pdf#page=27) of [SchrWalII](http://arxiv.org/abs/0802.0663). There are many possible conventions. The above is supposed to describe the _bidual_ [[opposite 2-category]] of the 2-groupoid as defined in that article, with the direction of 1- and 2-morphisms reversed. 


+-- {: .un_cor }
###### Corollary

The 2-groupoid $\mathbf{\flat}_{dR} \mathbf{B}[G_2 \to G_1]$ is as the one above, discarding the piece $C^\infty(-,G_1)$ in the 1-morphisms and the piece f$C^\infty(-,G_2)$ in the 2-morphismms.

=--

+-- {: .proof}
###### Proof

Form the defining pullback as before. (...)

=--




### Exponentiated $\infty$-Lie algebras {#StrucLieAlg}

We discuss here the  <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#LieAlgebras">intrinsic exponentiated ∞-Lie algebras</a> in $Smooth \infty Grpd$.


+-- {: .un_def}
###### Definition

Write [[dgAlg]] for the [[category]] of [[dg-algebra]]s over 
the [[real number]]s $\mahbb{R}$.

For $U \in $ [[CartSp]] and $n \in \mathbb{N}$, write
$\Omega^\bullet(U \times \Delta^n)$ for the [[dg-algebra]] of smooth [[differential form]]s with sitting instants (...) on the simplex.

Write $\Omega^\bullet_{vert}(U \times \Delta^n)$ for the [[quotient]] dg-algebra of [[vertical differential form]]s with respect to the projection $p : U \times \Delta^n \to U$: the [[coequalizer]] 

$$
  \Omega^\bullet(U)
    \stackrel{\overset{p^*}{\to}}{\underset{0}{\to}}
  \Omega^\bullet(U \times \Delta^n)
   \to
  \Omega^\bullet_{vert}(U \times \Delta^n)
$$

in [[dgAlg]].

=--

+-- {: .un_def}
###### Definition

For $\mathfrak{g}$ an [[L-∞ algebra]] (over the [[real number]]s $\mathbb{R}$)
of  [[finite type]], with [[Chevalley-Eilenberg algebra]] 
$CE(\mathfrak{g}) \in $ [[dgAlg]]${}_{\mathbb{R}}$
write $\exp(\mathfrak{g}) \in [CartSp_{smooth}^{op}, sSet]$ for the [[simplicial presheaf]] defined over $U \in $ [[CartSp]] and 
$n \in \mathbb{N}$ by

$$
  \exp(\mathfrak{g}) 
   :
  (U, [n]) \mapsto
  Hom_{dgAlg}(\Omega_{vert}^\bullet(U \times \Delta^n), CE(\mathfrak{g}))
$$

with the evident structure maps given by pullback of [[differential form]]s.

=--

For references related to this definition see _[[Lie integration]]_ .

+-- {: .un_prop}
###### Proposition

The objects $\exp(\mathfrak{g})$ are [concrete objects](#StrucConcreteObjects).

=--

+-- {: .proof}
###### Proof

We claim that the object $\exp(\mathfrak{g})$
is a [diffeological Kan complex](#DiffeologicalKanComplex).
By [a proposition above](DiffeologicalKanComplexesAreConcrete) 
this implies that it is concrete.

To see this, first notice that for each $n \in \mathbb{N}$ the
presheaf $\exp(\mathfrak{g})_n : CartSp_{smooth}^{op} \to Set$
is indeed [[sheaf]]. This follows from the fact that 
$\Omega^\bullet : CartSp_{smooth}^{op} \to Set$ is a sheaf.

Moreover, by definition of [[vertical differential form]]s
we have that [[dg-algebra]] homomorphisms 
$A : CE(\mathfrak{g}) \to \Omega_{vert}^\bullet(U \times \Delta^n)$
are encoded by sets of certain [[function]]s $f_A : U \to \Omega^\bullet(\Delta^n) \otimes \mathfrak{g}$.

Each such function is determined by its value on all points of $U$, and therefore the map

$$
  \{
      f_A : U \to \Omega^\bullet(\Delta^n) \otimes \mathfrak{g}
  \}
    \to
  Set(CartSp(*,U),\Omega^\bullet(\Delta^n) \otimes \mathfrak{g})
$$

is an injection.

=--


+-- {: .un_prop}
###### Proposition

The objects $\exp(\mathfrak{g}) \in Smooth \infty Grpd$ are
geometrically contractible:

$$
  \Pi \exp(\mathfrak{g}) \simeq *
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

Observe that every [[simplicial presheaf]] $X$ is the [[homotopy colimit]] over its component presheaves $X_n \in [CartSp_{smooth}^{op}, Set] \hookrightarrow [CartSp_{smooth}^{op}, sSet]_{loc}$

$$
  X \simeq \mathbb{L} {\lim_{\to}}_n X_n
  \,.
$$

(Use for instance the injective model structure for which $X_\bullet$ is cofibrant in the [[Reedy model structure]] $[\Delta^{op},[CartSp_{smooth}^{op}, sSet]_{inj,loc}]_{Reedy}$ ).

Therefore it is sufficient to show that in each degree $n$ the [[0-truncated]] object $\exp(\mathfrak{g})_{n}$ is geometrically contractible. To exhibit a geometric contraction, choose for each $n \in \mathbb{N}$, a smooth retraction

$$
  \eta_n : \Delta^n \times [0,1] \to \Delta^n  
$$

of the $n$-[[simplex]]: a smooth map such that $\eta_n(-,1) = Id$ and $\eta_n(-,0)$ factors through the point.


We claim that this induces a diagram of presheaves

$$
  \array{
     \exp(\mathfrak{g})_n
      \\
      {}^{\mathllap{(id,1)}}\downarrow & \searrow^{\mathrm{id}}
      \\
     \exp(\mathfrak{g})_n \times [0,1] &\stackrel{\eta_n^*}{\to}& \exp(\mathfrak{g})_n
      \\
      {}^{\mathllap{(id,0)}}\uparrow & & \uparrow
      \\
      \exp(\mathfrak{g})_n &\to& *
  }
  \,,
$$

where over $U \in CartSp$ the middle morphism is given by

$$
  \eta_n^*  
     : 
     (\alpha, f)
      \mapsto 
    (f,\eta_n)^* \alpha
  \,,
$$

where 

* $\alpha : CE(\mathfrak{g}) \to \Omega^\bullet_{vert}(U \times \Delta^n)$ is an element of the set $\exp(\mathfrak{g})_n(U)$, 

* $f$ is an element of $[0,1](U)$;

* $(f,\eta_n)$ is the composite morphism

  $$
    U \times \Delta^n  
       \stackrel{(Id,f)\times id}{\to}
    U \times [0,1] \times \Delta^n
      \stackrel{(Id,\eta_n)}{\to}
    U \times \Delta^n
    \;
  $$

* $(f,\eta)^* \alpha$ is the postcomposition of $\alpha$ with
  the image of $(f,\eta_n)$ under $\Omega^\bullet_{vert}(-)$.

Here the last item is well defined given the [[coequalizer]] definition of $\Omega^\bullet_{vert}$ because $(f,\eta_n)$ is a morphism of [[bundle]]s over $U$

$$
  \array{
    U \times \Delta^n  
       &\stackrel{(id,f) \times id}{\to}&
    U \times [0,1] \times \Delta^n
      &\stackrel{id \times \eta_n}{\to}&
    U \times \Delta^n
    \\
    \downarrow && \downarrow && \downarrow
    \\
    U &\stackrel{id}{\to}& U &\stackrel{id}{\to}& U
  }
  \,.
$$

Similarly, for $h : K \to U$ any morphism in [[CartSp]]${}_{smooth}$ the [[natural transformation|naturality]] condition for a morphism of [[presheaves]] follows from the fact that the composites of [[bundle]] morphisms

$$
  \array{
    K \times \Delta^n
     &\stackrel{h \times id}{\to}&
    U \times \Delta^n  
       &\stackrel{(Id,f)\times id}{\to}&
    U \times [0,1] \times \Delta^n
      &\stackrel{(Id,\eta_n)}{\to}&
    U \times \Delta^n
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    K &\stackrel{h}{\to}& U &\stackrel{id}{\to}& U &\stackrel{id}{\to}& U
  }
$$

and

$$
  \array{
    K \times \Delta^n  
       &\stackrel{((id,f \circ h) \times id }{\to}&
    K \times [0,1] \times \Delta^n
      &\stackrel{id \times \eta_n}{\to}&
    K \times \Delta^n
      &\stackrel{h \times id}{\to}&
    U \times \Delta^n
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    K &\stackrel{id}{\to}& K &\stackrel{id}{\to}& K
     &\stackrel{h}{\to}& 
   U
  }
$$

coincide.

Moreover, notice that the lower morphism in our diagram of presheaves indeed factors through the point as indicated, becase for an [[L-∞ algebra]] $\mathfrak{g}$ we have that the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ is in degree 0 the ground field algebra algebra $\mathbb{R}$, so that there is a unique morphism $CE(\mathfrak{g}) \to \Omega^\bullet_{vert}(U \times \Delta^0) \simeq C^\infty(U)$ in $dgAlg$.

Finally, since $[0,1]$ is a [[contractible]] [[paracompact manifold]], we have that $\Pi([0,1]) \simeq *$ by the [above proposition](#StrucGeometricHomotopy). Therefore the above diagram of presheaves presents a geometric homotopy in $Smooth \infty Grpd$ from the identity map to a map that factors through the point.

By the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Homotopy">propositon about geometric homotopy</a> in a [[cohesive (∞,1)-topos]] it follows that 
$\Pi(\exp(\mathfrak{g})_n) \simeq *$ for all $n \in \mathbb{N}$.
And since $\Pi$ preserves the [[homotopy colimit]] $\exp(\mathfrak{g}) \simeq \mathbb{L} {\lim_\to}_n \exp(\mathfrak{g})_n$ we have that $\Pi(\exp(\mathfrak{g})) \simeq *$, too.

=--

+-- {: .un_remark}
###### Remark

We may think of $\exp(\mathfrak{g})$ as the smooth 
**[[n-connected|∞-simply connected]] [[Lie integration]]**
of $\mathfrak{g}$.

Notice however that $\exp(\mathfrak{g}) \in Smooth \infty$
in general has nontrivial and interesting 
[[categorical homotopy groups in an (infinity,1)-topos|categorical homotopy groups]].
The above statement says that its 
_[[geometric homotopy groups in an (infinity,1)-topos|geometric homotopy groups]]_ vanish .

=--

#### For $\mathfrak{g}$ a Lie algebra

(...) see [[Lie integration]] (...)

#### For $\mathfrak{g} = b^n \mathfrak{u}(1)$

(...) see [[Lie integration]] (...)


#### de Rham coefficients {#DifferentialCoefficientsOfLieInt}

Above we have defined for every [[L-∞ algebra]] $\mathfrak{g}$ a tower of $\infty$-Lie groupoids  $\tau_n \exp(\mathfrak{g})$ _integrating_ it. Now we consider the corresponding de Rham $\infty$-Lie groupoids $\mathbf{\flat}_{dR} \tau_n \exp(\mathfrak{g})$.

Recall that in the above examples we saw for $G$ a Lie $\infty$-group that the underlying discrete Lie $\infty$-groupoid $\mathbf{\flat} \mathbf{B}G$ is resolved by the presheaf $G TrivBund_{flat}$ of trivial $G$-principal $\infty$-bundles with flat connection. From this resolution the de Rham object $\mathbf{\flat}_{dR} \mathbf{B}G$ is obtained as an ordinary pullback of presheaves. These statements we now produce in the full generality of an $\infty$-Lie group obtained from the integration of an $L_\infty$-algebra.

First we produce a [[resolution]] of the underlying bare $\infty$-groupoid

$$
  \mathbf{\flat}\exp(\mathfrak{g}) : (U,[n]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(\Delta^n))
  \,.
$$

+-- {: .un_def }
###### Definition

Write $\exp(\mathfrak{g})_{flat}$ for the simplicial presheaf given by

$$
  \exp(\mathfrak{g})_{flat}
  :
  (U,[n]) \mapsto
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(U \times \Delta^n))
  \,.
$$

=--

Here and in the following it is understood that differential forms on a space that contains a $\Delta^n$ as a factor have _sitting instants_ : for every $k$ and every $k$-face of $\Delta^n$ there is a neighbourhood of the boundary of that face on which the form is constant in the direction perpendicular to that boundary.




+-- {: .un_lemma }
###### Lemma

The canonical morphism

$$
  \mathbf{\flat}\exp(\mathfrak{g})
  \to
  \exp(\mathfrak{g})_{flat}
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--


Below we use this to factor the inclusion $\mathbf{\flat} \exp(\mathfrak{g}) \to \exp(\mathfrak{g})$ as $\mathbf{\flat}\exp(\mathfrak{g})
 \stackrel{\simeq}{\to} \exp(\mathfrak{g})_{flat} \to \exp(\mathfrak{g})$ with the last morphism being a fibration.

+-- {: .proof}
###### Proof

The morphism of simplicial presheaves is on each object $U$ the morphism of simplicial sets

$$
  \alpha(U,[k])
  :
  Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^k))
  \to
  Hom(CE(\mathfrak{g}), \Omega^\bullet(U \times \Delta^k))
$$

which is given by pullback along the projection $U \times \Delta^k \to U$.


To show that for fixed $U$ this is a weak equivalence in the standard [[model structure on simplicial sets]] we produce objectwise a left inverse 

$$
  F_U
  :
  Hom(CE(\mathfrak{g}), \Omega^\bullet(U \times \Delta^\bullet))
  \to
  Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet))
$$

and show that this is an acyclic fibration of simplicial sets. The statement then follows by the [[category with weak equivalences|2-out-of-3]]-property of weak equivalences.

We take $F_U$ to be given by evaluation at $0: * \to U$, i.e. by postcomposition with the morphisms

$$
  \Omega^\bullet(U \times \Delta^k )
  \stackrel{Id \times 0^*}{\to}
  \Omega^\bullet(* \times \Delta^k )
  =
  \Omega^\bullet(\Delta^k)
  \,.
$$


The morphism $F_U$ is an acyclic [[Kan fibration]] precisely if all diagrams of the form

$$  
  \array{
    \partial \Delta[n] &\to&
    Hom(CE(\mathfrak{g}), \Omega^\bullet(U \times \Delta^\bullet ))
    \\
    \downarrow && \downarrow^\mathrlap{F_U}
    \\
    \Delta[n]
    &\to&
    Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet))
  }
$$

have a lift. Since the differential forms on the simplices have sitting instances, we may for convenience equivalently reformulate this in terms of spheres as follows:

for every morphism $CE(\mathfrak{g}) \to \Omega^\bullet(D^n)$ and morphism $CE(\mathfrak{g}) \to \Omega^\bullet(U \times S^{n-1})$ such that the diagram

$$
  \array{
    CE(\mathfrak{g}) &\to& \Omega^\bullet(U \times S^{n-1})
    \\
    \downarrow && \downarrow
    \\
    \Omega^\bullet(D^n) &\to& \Omega^\bullet(S^{n-1})
  }
$$

commutes, this may be factored as

$$
  \array{
   CE(\mathfrak{g})
   \\
   & \searrow
   \\
   &&\Omega^\bullet(U \times D^n)
   &\to& \Omega^\bullet(U \times S^{n-1})
    \\
    &&\downarrow && \downarrow
    \\
    &&\Omega^\bullet(D^n) &\to& \Omega^\bullet(S^n)
  }
  \,.
$$

This factorization we now construct. 

Let first $f : [0,1] \to [0,1]$ be any smoothing function, i.e. a [[smooth function]] which is non-decreasing, onto, and constant in a neighbourhood of the boundary. Define a smooth map

$$
  U \times [0,1] \to U 
$$

by 

$$
  (u,\sigma) \mapsto u \cdot f(1-\sigma)
  \,,
$$

where we use the multiplicative structure on the [[Cartesian space]] $U$. This function is the identity at $\sigma = 0$ and is the constant map to the origin at $\sigma = 1$. It exhibits a smooth contraction of $U$.

Pullback of differential forms along this map produces a morphism

$$
  \Omega^\bullet(U \times S^{n-1}) 
  \to 
  \Omega^\bullet(U \times S^{n-1} \times [0,1])
$$

which is such that a form $\omega$ is sent to a form which in a neighbourhood $(1-\epsilon,1]$ of $1 \in [0,1]$ is constant along $(1-\epsilon,1] \times U$ on the value $(0 , Id_{S^{n-1}})^* \omega$. 

We can then glue to the morphism

$$
  CE(\mathfrak{g}) \to
  \Omega^\bullet(U \times S^{n-1})
  \to
  \Omega^\bullet(U \times [0,1] \times S^{n-1})
$$

the morphism

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(D^n)
  \to
  \Omega^\bullet(U \times \{1\} \times D^n)
$$

by smoothly identifying the union $[0,1] \times S^{n-1} \coprod_{S^{n-1}} D^n$ with another copy of $D^n$ (we glue a disk into an annulus to obtain a larger disk) to obtain in total a morphism

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(U \times D^n)
$$

with the desired properties.


=--

+-- {: .un_lemma }
###### Lemma

The canonical morphism

$$
  \exp(\mathfrak{g})_{flat}
  \to 
  \exp(\mathfrak{g})
$$

is a fibration in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

Over each $U \in CartSp$
the morphisms is induced from the morphism of dg-algebras

$$
  \Omega^\bullet(U) \to C^\infty(U)
$$

that discards all differential forms of non-vanishing degree. 

It will be sufficient to show that for 

$$
  CE(\mathfrak{g}) 
    \to 
   \Omega^\bullet(
     D^n \times [0,1]
   )
   \otimes' C^\infty(U)
$$

a morphism and 

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(D^n \times U)
$$

a lift of its restriction to $\sigma = 0 \in [0,1]$ we have a
lift 

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(D^n \times [0,1] \times U)
$$

extending the lift. From these lifts all the required lifts are obtained by precomposition with some evident smooth retractions.


The idea of the proof is that the lifts in question are obtained from solving differential equations with boundary conditions, and exist due to the existence of solutions of first order systems of partial differential equations and the Bianchi identities for flat $L_\infty$-algebra valued forms. 


**1st case: $\mathfrak{g} = \mathfrak{u}(1)$**

To warm up, consider the simplest case where $\mathfrak{g} = \mathfrak{u}(1)$.


Then a morphism $C(\mathfrak{g}) \to \Omega^\bullet(D^1 \times U \times [0,1]) \otimes C^\infty(U)$ is an element $A_v(u) d v + A_\sigma(u) d \sigma $ that satisfies

$$
  \partial_v A_u = \partial_u A_v
$$

and 

$$
  \partial_\sigma A_v = \partial_v A_\sigma
  \,.
$$

To lift this to a morphism $CE(\mathfrak{g}) \to \Omega^\bullet(D^1 \times U \times [0,1])$ that restricts to the former for $\sigma = 0$ we need to add a term $A_u(u,\sigma) d u$. That satisfies the differential equations

$$
  \partial_\sigma A_u = \partial_u A_\sigma
$$

and 

$$
  \partial_v A_u = \partial_u A_v
  \,.
$$

The first one already uniquely defines and fixes $A_u$: since the value of $A_0$ at $\sigma = 0$ is given, this differential equation has a unique solution along $\sigma \in [0,1]$. 

So it remains to check that this unique solution to the first equation also solves the second

$$
  \partial_v A_u = \partial_u A_v
$$

for all $\sigma$. It is true by assumption at $\sigma = 0$, so it is sufficient to show that the $\sigma$-derivatives of both sides coincide.

On the left we have 

$$
  \partial_\sigma \partial_v A_u = \partial_v \partial_\sigma A_u =
  \partial_v \partial_u A_\sigma
$$

by the above, and similarly on the right

$$
  \partial_\sigma \partial_u A_v = \partial_u \partial_\sigma A_v = 
  \partial_u \partial_v A_\sigma
$$

so that indeed this is equal. This constitutes the required lift.

**2nd case: $\mathfrak{g} an arbitrary Lie algebra$**

Now let $\mathfrak{g}$ be an arbitrary Lie algebra. Choose a dual basis $\{t^a\}$ and structue constants $C^a{}_{b c}$. We get a discussion analogous to the above with structure constant terms thrown in:

the original element is a collection of 1-forms $A^a_v d v + A^a_\sigma d \sigma $ satisfying

$$
  \partial_\sigma A_v^a = \partial_v A_\sigma 
   - C^a{}_{b c} A_v^b A_\sigma^c
  \,.
$$

We lift by adding a term $A_u^a d u$ that is uniquely fixed by the condition that it solves the differential equation

$$
  \partial_\sigma A_u = \partial_u A_\sigma 
  - C^a{}_{b c} A_\sigma^b  A_u^c
$$

for given boundary value at $\sigma = 0$.

We need to show that the lift found this way also satisfies the equation

$$
  F_{v u}^a
  :=
  \partial_v A^a_u - \partial_u A^a_v + C^a{}_{b c} A_v^b A_u^c = 0
  \,.
$$

By assumption, this is true at $\sigma = 0$. We now show that the $\sigma$-derivative of this expression satisfies the Binachi-type equation

$$
  \partial_\sigma F^a_{v u} 
  = 
  C^a{}_{b c} A^b_\sigma F^c_{v u} 
  \,.
$$

A solution to this differential equation with initial value 0 is $F^a_{v u} = 0$. Since this solution is guaranteed to be unique, we will have shown our claim.

Now compute:

$$
  \begin{aligned}
    \partial_\sigma F^a_{u v} 
    &:=
    \partial_\sigma \partial_u A^a_v -
    \partial_\sigma \partial_v A^a_u
    +
    \partial_\sigma C^a{}_{b c} A_u^b A^c_v
    \\
    & =
    \partial_u \partial_\sigma  A^a_v -
    \partial_v \partial_\sigma  A^a_u
    +
    \partial_\sigma C^a{}_{b c} A_u^b \wedge A^c_v
    \\
    &=
    \partial_u 
    (\partial_v A^a_\sigma - C^a{}_{b c} A^b_\sigma A^c_v)
    -
    \partial_v 
    (\partial_u A^a_\sigma - C^a{}_{b c} A^b_\sigma A^c_u)
    +
    \partial_\sigma C^a{}_{b c} A_u^b A^c_v
    \\
    & =
    \partial_u C^a{}_{b c} A^b_\sigma A^c_v
    -
    \partial_v C^a{}_{b c} A^b_\sigma A^c_u
    +
    \partial_\sigma C^a{}_{b c} A_u^b A^c_v    
    \\
    & =
    C^a{}_{b c} A^b_\sigma  (\partial_u A^c_v - 
    \partial_v A^c_u)
    +
    C^a{}_{b c} 
     (\partial_\sigma A^b_u - C^b{}_{d e} A^d_u A^e_\sigma)
     A^c_v
    -
    C^a{}_{b c} 
     (\partial_\sigma A^b_\nu - C^b{}_{d e} A^d_v A^e_\sigma)
     A^b_u
   + 
   \partial_\sigma C^a{}_{b c} A^b_v A^c_u
   \\
   & =
   C^a{}_{b c} A^c_\sigma F^b_{u v}   
\end{aligned}
  \,.
$$  

Here in the last step we use the [[Jacobi identity]]

$$
  C^a{}_{b c} C^b{}_{d e}
  +
  C^a{}_{b d} C^b{}_{e c}
  +
  C^a{}_{b e} C^b{}_{c d}
  = 0
  \,.
$$


**general case**

For $\mathfrak{g}$ a general $L_\infty$-algebra, the computation is essentially as above for the Lie algebra case only that all indices become multi-indices in a suitable sense. 

For instance the structure constants  now have components of arbitrary arity. But for the discussion of the lift it is still always just the components with two legs along the $u$-, $v$-, $\sigma$- direction that matter, all other indices just run along.

I'll try to think of a convenient notation to express this.

=--

With $\mathbf{\flat}\exp(\mathfrak{g}) \to \exp(\mathfrak{g})$ realized as a fibration between fibrant objects, we now obtain the de Rham coefficient object $\mathbf{\flat}_{dR} \exp(\mathfrak{g})$ as an ordinary pullback, as in the above discussions.

+-- {: .un_corollary}
###### Corollary

For $\mathfrak{g}$ an $L_\infty$-algebra, a representive in $[CartSp^{op}, sSet]_{proj}$ of the object $\mathbf{\flat}_{dR} \exp(\mathfrak{g})$ is the presheaf

$$
  (U,[n])
  \mapsto
   Hom_{dgAlg}(
     CE(\mathfrak{g}),
     \Omega^{\bullet\geq 1,\bullet}(U \times \Delta^n)
  )
  \,,
$$

where the notation on the right denotes the dg-algebra of differential forms on $U \times\Delta^n$ that (apart from having sitting instants on the faces of $\Delta^n$) are along $U$ of non-vanishing degree.

=--

Compare this to the more explicit examples that we had discussed above.

+-- {: .un_corollary}
###### Corollary

All statements go through verbatim for the $n$-truncation $\tau_n \exp(\mathfrak{g})$.

(...)

=--

+-- {: .un_remark}
###### Remark

Observe that $\exp(\mathfrak{g})$ is the _concretization_ (in the sense of [[concrete presheaf]]) of $G TrivBund_{flat} \simeq \mathbf{\flat} \mathbf{B}G$. And $\mathbf{\flat}_{dR}\mathbf{B}G$, being the kernel of the concretization map, is in a sense the maximally non-concrete sub-presheaf of $G TrivBund_{flat}$.

=--

##### For line $n$-groups {#LieIntDiffCoeffsForLineGroups}

For the [circle n-groupoid](#BnU1) $\mathbf{B}^{n}U(1)$ we have now obtained two different models for its de Rham coefficient object $\mathbf{\flat}_{dR}\mathbf{B}^n U(1)$:

1. The image under the [[Dold-Kan correspondence|Dold-Kan map]] 
   $\Xi : [CartSp^{op}, Ch_\bullet] \to [CartSp^{op}, sSet]$ of the
   complex of sheaves of forms

   $$
     \mathbf{\flat}_{dR}^{chn}\mathbf{B}^n \mathbb{R}
     :=
     \Xi
     (\Omega^1(-) \stackrel{d_{dR}}{\to}
     \Omega^2(-) \stackrel{d_{dR}}{\to}
     \cdots
     \Omega^n_{cl}(-))
     \,.
   $$

   (This is discussed <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+examples#FlatCircleCohomology">here</a>).

1. The $(n+1)$-[[coskeleton]] of the simplicial presheaf

   $$
     \mathbf{\flat}^{simp}_{dR}\mathbf{B}^n \mathbb{R}
     :
     U,[k] \mapsto \tilde \Omega^n_{cl}^n(U \times \Delta^k)
     \,,
   $$

   where the tilde indicates the subset of all those forms with at least one leg along $U$.

   (This is the result of the [Lie integration algorithm](#DifferentialCoefficientsOfLieInt).)

There is an evident degreewise map

$$
  (-1)^{\bullet+1}
  \int_{\Delta^\bullet} :
  \mathbf{\flat}_{dR}^{simp} \mathbf{B}^n \mathbb{R}
  \to  
  \mathbf{\flat}_{dR}^{chn} \mathbf{B}^n \mathbb{R}
$$

that sends a closed $n$-form $\omega \in \Omega^n_{cl}(U \times \Delta^k)$ to $(-1)^{k+1}$ times  its [[fiber integration]] $\int_{\Delta^k} \omega$.

+-- {: .un_prop}
###### Proposition

This map yields a morphism of simplicial presheaves

$$
  \int : 
   \mathbf{\flat}_{dR}^{simp} \mathbf{B}^n \mathbb{R}
     \to
   \mathbf{\flat}_{dR}^{chn} \mathbf{B}^n \mathbb{R}
$$

which is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

By the [[Dold-Kan correspondence]] we may check the statement for 
sheaves of (normalized) chain complexes.

Notice that the chain complex differential on the forms 
$\omega \in \Omega^n_{cl}(U \times \Delta^k)$ on simplices
sends a form to the alternating sum of its restriction to the faces of the
simplex. Postcomposed with the integration map this is the operation
$\omega \mapsto \int_{\partial \Delta^k} \omega$.

Conversely, first integrating over the simplex and then applying the de Rham differential on $U$ yields

$$
  \begin{aligned}
     \omega \mapsto (-1)^{k+1} d_U \int_{\Delta^k} \omega
      &= 
      - \int_{\Delta^k} d_U \omega
      \\
      & = \int_{\Delta^k} d_{\Delta^k} \omega
      \\
      & =  \int_{\partial \Delta^k} \omega
  \end{aligned}
  \,,
$$

where we first used that $\omega$ is closed, so that $d_{dR} \omega = (d_U + d_{\Delta^k}) \omega = 0$, and then [[Stokes' theorem]].

Therefore we have indeed objectwise a chain map.

To see that it gives a weak equivalence we need to check that this chain map is a [[quasi-isomorphism]].

From the construction of both objects we know that they have the same cohomology, because both are models for the same homotopy pullback. For $\mathbf{\flat}_{dR}^{chn}$ that cohomology is concentrated in degree $n$, where it is $\Omega^1_{cl}(U)$. Therefore it is in fact sufficient to check that the integration map is onto in degree $n$. 

That amounts to observing that every 1-form $\alpha \in \Omega^1(U)$ may be obtained by integration of a closed $n$-form on $U \times \Delta^k$. This is clearly the case, for instance take $\frac{1}{c} \alpha \wedge d x^1 \wedge \cdots \wedge d x^{k} - \frac{1}{c} (d_U \alpha) \wedge x^1 \wedge d x^2 \wedge \cdots \wedge d x^k$.

=--





### Maurer-Cartan forms and curvature characteristic forms {#StrucCurvatureForms}

We discuss the 
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">intrinsic Maurer-Cartan and curvature characteristic forms</a> defined in any cohesive $(\infty,1)$-topos
realized in $Smooth \infty Grpd$.

#### The canonical form on a Lie group  {#CanonicalFormOnLieGroup}

Let $G$ be a [[Lie group]]. Write $\mathfrak{g}$ for 
its [[Lie algebra]].


+-- {: .un_prop }
###### Proposition

Under the identification

$$
  Smooth \infty Grpd(X, \mathbf{\flat}_{dR}\mathbf{B}G)
  \simeq
  \Omega^1_{flat}(X,\mathfrak{g})
$$

from [the above proposition](#LieGroupDeRhamCohomology), for $X \in $ [[SmoothMfd]], we have that the canonical morphism

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}G
$$

in $Smooth \infty Grpd$ corresponds to the 
ordinary [[Maurer-Cartan form]] on $G$.


=--


+-- {: .proof}
###### Proof

We compute the defining double [[(∞,1)-pullback]]

$$
  \array{
    G &\to& *
    \\
    {}^{\mathllap{\theta}}\downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
$$

in $Smooth \infty Grpd$ as a [[homotopy pullback]]
in $[CartSp_{smooth}^{op}, sSet]_{proj}$

In the above [discussion of differential coefficients](#LieGroupDeRhamCoefficients) we already modeled the lower $(\infty,1)$-pullback square by the ordinary pullback 

$$
  \array{
    \mathbf{\flat}_{dR}\mathbf{B}G_c
      &\to&
    \mathbf{\flat}\mathbf{B}G_c
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G_c
  }
$$

A standard fibration replacement of the point inclusion
$* \to \mathbf{\flat}\mathbf{B}G $ is
(as discussed at [[universal principal ∞-bundle]]) 
given by replacing the point by the presheaf that assigns groupoids of the form


$$
  Q : 
  U \mapsto 
  \left\{
    \array{
       && A_0 = 0
       \\
       & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
       \\
       A_1 &&\stackrel{h}{\to}&& A_2
    }
  \right\}
  \,,
$$

where on the right the commuting triangle is in 
$(\mathbf{\flat}_{dR}\mathbf{B}G_c)(U)$ and here regarded as a morphism from $(g_1,A_1)$ to $(g_2,A_2)$. And the fibration $Q \to \mathbf{\flat}\mathbf{B}G_c$ is given by projecting out the base of these triangles.

The pullback of this along
$\mathbf{\flat}_{dR}\mathbf{B}G_c \to \mathbf{\flat}\mathbf{B}G_c$ is over each $U$  the restriction of the groupoid $Q(U)$ to its set of objects, hence is the [[sheaf]]

$$
  U \mapsto 
  \left\{
    \array{
       A_0 = 0
       \\
       \downarrow^{\mathrlap{g}}
       \\
       g^* \theta
    }
  \right\}
  \simeq 
  C^\infty(U,G)
  = G(U)
  \,,
$$

equipped with the projection

$$
 t_U :  G \to \mathbf{\flat}_{dR} \mathbf{B}G_c
$$

given by

$$
  t_U : (g : U \to G) \mapsto g^* \theta
  \,.
$$

Under the [[Yoneda lemma]] (over [[SmoothMfd]]) this 
identifies the morphism $t$ with the [[Maurer-Cartan form]]
$\theta \in \Omega^1_{flat}(G,\mathfrak{g})$.

=--


#### The universal curvature characteristic on $\mathbf{B}^n U(1)$

Recall the discussion of $\mathbf{B}^n U(1)$ and of 
$\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ from 
[above](#StrucDeRham).

+-- {: .un_def}
###### Definition

For $n \in \mathbb{N}$ define the simplicial presheaf

$$
  \mathbf{B}^n U(1)_{diff,chn}
  :=
  \array{
    \Xi\left(
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \right)
  }
  \,.
$$

=--


+-- {: .un_prop #CurvatureCharOnBnU1}
###### Proposition

The evident projection

$$
  \mathbf{B}^n U(1)_{diff,chn} \to \mathbf{B}^n U(1)_{chn}
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.
Moreover,  the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature characteristic</a> 

$$
  curv :  \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)
$$

in $Smooth \infty Grpd$ is presented in $[CartSp^{op}, sSet]_{proj,loc}$
by a span

$$
  \array{
    \mathbf{B}^n U(1)_{diff,chn} &\stackrel{curv_{chn}}{\to}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^n U(1)
  }
$$

where the horizontal morphism is the evident projection

$$ 
  \array{
    \Xi\left(\;
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \right)
    \\
    \downarrow 
    \\
    \Xi\left(
    \; 0 \stackrel{}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to}
    \Omega^2(-)
    \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-))    
    \right)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof


We need to present the defining [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{B}^n U(1) &\to& *
    \\
    {}^{\mathllap{curv}}\downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1) &\to&
    \mathbf{\flat} \mathbf{B}^{n+1} U(1)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}^{n+1} U(1)
  }
$$

by a [[homotopy pullback]] in $[CartSp^{op}, sSet]_{proj}$ (since [[(∞,1)-sheafification]] preserves finite [[(∞,1)-pullback]]s it is sufficient to present the $(\infty,1)$-pullback in [[(∞,1)-presheaves]]).

We claim that we have a commuting diagram

$$ 
  \array{
    \Xi(\;
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \;)
    &\to&
    \Xi(\;
     C^\infty(-,U(1)) \stackrel{Id + d_{dR}}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    { \Omega^{n-1}(-) \atop \oplus \Omega^n(-)}
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \;)
    \\
    \downarrow && \downarrow^{\mathrlap{(Id, p_2, p_2, \cdots, p_2,d_{dR})}}
    \\
    \Xi(
    \; 0 \stackrel{}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to}
    \Omega^2(-)
    \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-))    
    &\to&
    (C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to} 
    \Omega^2(-)
    \stackrel{d_{dR}}{\to}
    \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-)
    \;)
    \\
    \downarrow && \downarrow
    \\
    \Xi(
     \; 0 \to 0 \to 0 \to \cdots \to 0\;)
    &\to&
    \Xi(
     \; C^\infty(-,U(1)) \to 0 \to 0 \to \cdots \to 0
     \;)
  }
$$

in $[CartSp^{op},sSet]_{proj}$ where

* the objects are fibrant models for the corresponding objects in the
  above $(\infty,1)$-pullback diagram;

* the two right vertical morphisms are fibrations;

* the two squares are [[nLab:pullback]] squares.

Therefore this is a [[homotopy pullback]] in $[CartSp^{op}, sSet]_{proj}$ that realizes the  $(\infty,1)$-pullback in question. 

For the lower square we had discussed this already [above](#OrdinaryDeRham). For the upper square the same type of reasoning applies. The main point is to find the chain complex in the top right such that it is a [[resolution]] of the point and maps by a fibration onto our model for $\mathbf{\flat}\mathbf{B}^n U(1)$. The top right complex is

$$
  \array{
    &&
    C^\infty(-,U(1)) 
     &\stackrel{d_{dR}}{\to}&
    \Omega^1(-)
     &\stackrel{d_{dR}}{\to}&
    \Omega^2(-)
     &\stackrel{d_{dR}}{\to}&
     \cdots
     &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
     \\
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \cdots  &
     {}^{\mathrlap{id}}\nearrow& 
     \\
    C^\infty(-,U(1)) 
     &\stackrel{d_{dR}}{\to}&
    \Omega^1(-)
     &\stackrel{d_{dR}}{\to}&
    \Omega^2(-)
     &\stackrel{d_{dR}}{\to}&
     \cdots
     &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
  }
$$

and the vertical map out of it into $C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n(-) \stackrel{d_{dR}}{\to} \Omega^{n+1}_{cl}(-)$ is in positive degree the projection onto the lower row and in degree 0 the de Rham differential. This is manifestly surjective (by the [[Poincare lemma]] applied to each object $U \in $ [[CartSp]]) hence this is a fibration.

The pullback object in the top left is in this notation

$$
  \mathbf{B}^n U(1)_{diff,chn}
  :=
  \Xi
  \left(
    \array{
      C^\infty(-,U(1)) 
       &\stackrel{d_{dR}}{\to}&
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
       \cdots
       &\stackrel{d_{dR}}{\to}&
        \Omega^n(-)
       \\
       \oplus 
       &{}^{\mathrlap{id}}\nearrow& \oplus 
       &{}^{\mathrlap{id}}\nearrow& \cdots  &
       {}^{\mathrlap{id}}\nearrow& 
       \\
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
       \cdots
       &\stackrel{d_{dR}}{\to}&
        \Omega^n(-)
    }
  \right)
$$

and in turn the top left vertical morphism $curv : \mathbf{B}_{diff}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ is in positive degree the projection on the lower row and in degree 0 the de Rham differential.

=--

Notice that the evident forgetful morphism $\mathbf{B}^n U(1) \stackrel{}{\leftarrow} \mathbf{B}^n_{diff} U(1)$ is indeed a weak equivalence.


### Differential cohomology {#StrucDifferentialCohomology}

We discuss the 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">intrinsic differential cohomology</a> in $Smooth \infty Grpd$

We first expose the simple special case of ordinary
$U(1)$-[[principal bundle]]s with [[connection on a bundle|connection]]
in more detail. Then we turn to the general case.



#### Circle bundles with connection {#CircleBundlesConnection}

Before discussing [the full theorem](#DeligneCohomologyTheorem), it is instructive to start by looking at the special case $n=1$ in some detail, which is about ordinary  $U(1)$-[[nLab:principal bundle]]s [[nLab:connection on a bundle|with connection]]. 

This contains in it already all the relevant structure of the general case, but the low categorical degree is more transparently written out and will allow us to pause to highlight some maybe noteworthy aspects of the situation, such as the phenomenon of _pseudo-connections_ [below](#CircleBunlePseudoConnection).

In terms of the [Dold-Kan correspondence](#DoldKan) the object $\mathbf{B}U(1) \in \mathbf{H}$ is modeled in $[CartSp^{op}, sSet]$ by

$$
  \mathbf{B}U(1)
  =
  \Xi(\;
    C^\infty(-,U(1)) \to 0    
  \;)
  \,.
$$

Accordingly we have for the double [[nLab:delooping]] the model

$$
  \mathbf{B}^2 U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \to 0  \to 0    
  \;)
$$

and for the [[nLab:universal principal ∞-bundle|universal principal 2-bundle]]

$$
  \mathbf{E}\mathbf{B}U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-, U(1)) \to 0    
    \;
  )
  \,.
$$

In this notation we have also the constant presheaf

$$
  \mathbf{\flat} \mathbf{B}^2 U(1)
  = 
  \Xi(
    \;
     const U(1) \to 0 \to 0
    \;
  )  
  \,.
$$

Above we already found the model 

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  = 
  \Xi(0 \to \Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))
  \,.
$$

In order to compute the differential cohomology 
$\mathbf{H}_{diff}(-,\mathbf{B}U(1))$ by an ordinary
pullback in [[nLab:sSet]] we also want to resolve the curvature characteristic morphism $\mathbf{B}U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ by a fibration. We claim that this may be obtained by choosing the resolution 
$\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B} U(1)_{diff,chn}$ given by

$$
  \mathbf{B}U(1)_{diff} 
  :=
  \Xi(
    \;
    C^\infty(-,U(1))
    \oplus
    \Omega^1(-)
    \stackrel{d_{dR} \oplus Id}{\to}
    \Omega^1(-)
    \;
  )
$$

with the morphism $curv : \mathbf{B}_{diff}U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)$ given by

$$
  \array{
    C^\infty(-,U(1)) 
    \oplus
    \Omega^1(-)
    &\stackrel{d_{dR} + Id}{\to}&
    \Omega^1(-)
    \\
    \downarrow^{\mathrlap{p_2}} && \downarrow^{\mathrlap{d_{dR}}}
    \\
    \Omega^1(-) &\stackrel{d_{dR}}{\to}&
    \Omega^2_{cl}(-)
  }
  \,.
$$

By the [[nLab:Poincare lemma]] applied to each [[nLab:Cartesian space]], this is indeed a fibration.

In the [next section](#AbGerbesConnection) we give the proof of this (simple) claim. Here in the warmup phase we instead want to discuss the geometric interpretation of this resolution, along the lines of the section <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#CurvatureCharacteristicsI">curvature characteristics of 1-bundles</a> in the [[schreiber:differential cohomology in an (∞,1)-topos -- survey|survey-part]].


+-- {: .un_prop }
###### Proposition

We have the following geometric interpretation of the above models:

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  : 
  U \mapsto 
  \left\{
    \array{
      U &\to& *
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1)
    }
  \right\}
  =
  \left\{
    \mathbf{\Pi}_2(U) \to \mathbf{B}^2 U(1)
  \right\}
$$

and

$$
  \mathbf{B}U(1)_{diff}
  : 
  U \mapsto 
  \left\{
    \array{
      U &\to& \mathbf{B}U(1)
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1))
    }
  \right\}
  \,.
$$

And in this presentation the morphism $curv : \mathbf{B}_{diff}U(1) \to \mathbf{B}^2 U(1)$ is given over $U \in CartSp$ by forming the pasting composite

$$
  \array{
    U &\to& \mathbf{B}U(1) &&& underlying\;cocycle
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1)) &&& connection
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1) &&& curvature
  }
$$

and picking the lowest horizontal morphism.

=--

Here the terms mean the following:

* $INN(U(1))$ is the [[nLab:2-group]] $\Xi(U(1) \to U(1))$, which is a 
  [[nLab:groupal model for universal principal ∞-bundles|groupal model for the universal U(1)-principal bundle]] $\mathbf{E}U(1)$;

* $\mathbf{\Pi}_2(U)$ is the [[nLab:path 2-groupoid]] with homotopy class of 2-dimensional paths as 2-morphisms

* the groupoids of diagrams in braces have as objects commuting diagrams in $[CartSp^{op}, sSet]$ as indicated, and horizontal 2-morphisms fitting into such diagrams as morphisms.

Using the discussion at [[nLab:2-groupoid of Lie 2-algebra valued forms]] (<a href="http://arxiv.org/abs/0802.0663">SchrWalII</a>) we have the following:


1. For $X$ a [[nLab:smooth manifold]], morphisms in $[CartSp^{op}, 2Grpd]$ of the form $tra_A : \Pi_2(X) \to \mathbf{E}\mathbf{B}U(1)$ are in bijection with smooth 1-forms $A \in \Omega^1(X)$: the 2-functor sends a path in $X$ to the the [[nLab:parallel transport]] of $A$ along that path, and sends a surface in $X$ to the exponentiated integral of the curvature 2-form $F_A = d A$ over that surface. The [[nLab:Bianchi identity]] $d F_A = 0$ says precisely that this assignment indeed descends to homotopy classes of surfaces, which are the 2-morphisms in $\Pi_2(X)$.

1. Moreover [[nLab:k-morphism|2-morphisms]] of the form $(\lambda,\alpha) : tra_A \to \tra_{A'}$ in $[CartSp^{op}, 2Grpd]$ are in bijection with pairs consisting of a $\lambda \in C^\infty(X,U(1))$ and a 1-form $\alpha \in \Omega^1(X)$ such that $A' = A + d_{dR} \lambda - \alpha$. 

1. And finally [[nLab:k-morphism|3-morphisms]] $h : (\lambda, \alpha) \to (\lambda', \alpha')$ are in bijection with $h \in C^\infty(X,U(1))$ such that $\lambda' = \lambda \cdot h$ and $\alpha' = \alpha + d_{dR} h$.


By the same reasoning we find that the coefficient object for flat $\mathbf{B}^2 U(1)$-valued differential cohomology is

$$
  \mathbf{\flat}\mathbf{B}^2 U(1)
  =
  [\Pi_2(-), \mathbf{B}^2U(1)]
  =
  \Xi(
    C^\infty(-,U(1))
    \stackrel{d_{dR}}{\to}
    \Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-)
  )
  \,.
$$


So by the above definition of differential cohomology in $\mathbf{H}$ we find that $\mathbf{B}U(1)$-differential cohomology of a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$ is given by choosing any [[nLab:good open cover]] $\{U_i \to X\}$, taking $C(\{U_i\})$ to be the [[nLab:Cech nerve]], which is then a cofibrant replacement of $X$ in $[CartSp^{op}, sSet]_{proj,cov}$ and forming the ordinary pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1)) &\to& H^2_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    [CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}_{diff}U(1))
    &\stackrel{curv}{\to}&
    [CartSp^{op},sSet](C(\{U_i\}), \flat_{dR}\mathbf{B}^2 U(1))
  }
$$

(because the bottom vertical morphism is a fibration, by the fact that our model for $\mathbf{B}_{diff} U(1) \to \flat_{dR}\mathbf{B}^2 U(1)$ is a fibration, that $C(\{U_i\})$ is cofibrant and using the axioms of the [[nLab:sSet]]-[[nLab:enriched model category]] $[CartSp^{op}, sSet]_{proj}$).

+-- {: .un_prop}
###### Observations

A cocycle in $[CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}_{diff}U(1))$ is

1. a collection of functions

   $$
     (g_{i j } \in C^\infty(U_i \cap U_j, U(1)))
    $$

    satsifying $g_{i j} g_{j k} = g_{i k}$ on $U_i \cap U_j \cap U_k$;
  
1. a collection of 1-forms

   $$
      (A_i \in \Omega^1(U_i))
   $$
  
1. a collection of 1-forms


    $$
      (a_{i j} \in \Omega^(U_i \cap U_j))
    $$

    such that

    $$
      A_j = A_i + d_{dR} g_{i j} + a_{i j}
    $$

    on $U_i \cap U_j$ and

    $$
      a_{i j} + a_{j k} = a_{i k}
    $$

    on $U_i \cap U_j \cap U_k$.

The curvature-morphism takes such a cocycle to the cocycle

$$
  (d A_i, a_{i j}, )
$$

in the [above model](#OrdinaryDeRham) $[CartSp^{op},sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^2 U(1))$ for intrinsic de Rham cohomology.


Every cocycle with nonvanishing $(a_{i j})$ is in $[C(\{U_i\}), \mathbf{B}_{diff}U(1)]$ coboundant to one with vanishing $(a_{i j})$ 
   
=--

+-- {: .proof}
###### Proof

The first statements are effectively the definition and the construction of the above models. The last statement is as in the [above discussion](#OrdinaryDeRham) of our model for ordinary de Rham cohomology: given a cocycle with non-vanishing closed $a_{i j}$, pick a partition of unity $(\rho_i \in C^\infty(X))$ subordinate to the chosen cover and the coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i})$. This connects $(A_i,a_{i j}, g_{i j})$ with the cocycle $(A'_i, a'_{i j}, g_{i j})$ where

$$
  A'_i = A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}
$$

and

$$
  \begin{aligned}
    a'_{i j} 
      & = A'_j - A'_i - d g_{i j} 
     \\ 
      & = a_{i j} + 
      - \sum_{i_0}( a_{i_0 i} - a_{i_0 j} )
    \\
    & = 0    
  \end{aligned}
  \,.
$$

=--

So in total we have found the following story:

1. In order to compute the curvature characteristic form of a [[nLab:Cech cohomology]] cocycle $g : C(\{U_i\}) \to \mathbf{B}U(1)$ of a $U(1)$-principal bundle, we first lift it 

   $$
     \array{
       && \mathbf{B}_{diff}U(1)
       \\
       & {}^{\mathllap{(g,\nabla)}}\nearrow & \downarrow
       \\
       C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
     }
   $$

   to an equivalent $\mathbf{B}_{diff}U(1)$-cocycle, and this amounts to putting (the Cech-representatitve of) a _pseudo-connection_ on the $U(1)$-principal bundle.

1. From that lift the desired curvature characteristic is simply projected out

   $$
     \array{
       && \mathbf{B}_{diff}U(1) &\stackrel{curv}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)
       \\
       & {}^{\mathllap{(g,\nabla)}}\nearrow & \downarrow
       \\
       C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
     }
     \,,
   $$

   and we find that it lives in the sheaf [[nLab:hypercohomology]] that models ordinary de Rham cohomology.

1. Therefore we find that in each _cohomology class_ of curvatures, there is at least one representative which is an ordinary globally defined 2-form. Moreover, the pseudo-connections that map to such a representative are precisely the _genuine_ connections, those for which the $(a_{i j})$-part of the cocycle vaishes.

So we see that ordinary connections on ordinary circle bundles are a means to model the homotopy pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1)) &\to& H_{dR}^2(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}U(1)) &\to& \mathbf{H}_{dR}(X,\mathbf{B}U(1)) 
  }
$$

in a 2-step process: first the choice of a pseudo-connection realizes the bottom horizontal morphism as an [[nLab:anafunctor]], and then second the restriction imposed by forming the ordinary pullback chooses from all pseudo-connections precisely the genuine connections.

The general version of this story is discussed in detail at <a href="#Connections">differential cohomology in an (∞,1)-topos -- Local (pseudo-)connections.</a>


#### Circle bundles with pseudo-connection {#CircleBunlePseudoConnection}

In the above discussion of extracting ordinary connections on ordinary $U(1)$-principal bundles from the abstract topos-theoretic definition of differential cohomology, we argued that a certain homotopy pullback may be computed by choosing in the Cech-hypercohomology of the complex of sheaves $(\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))$ over a manifold $X$ those cohomology representatives that happen to be represented by globally defined 2-forms on $X$. We saw that the homotopy fiber of _pseudo-connections_ over these 2-forms happened to have connected components indexed by _genuine_ connections.

But by the general abstract theory, up to isomorphism the differential cohomology computed this way is guaranteed to be independent of all such choices, which only help us to compute things.

To get a feeling for what is going on, it may therefore be useful to re-tell the analgous story with pseudo-connections that are not genuine connections.

By the very fact that $\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B}_{diff}U(1)$ is a weak equivalence, it follows that every pseudo-connection is equivalent to an ordinary connection as cocoycles in $[CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}_{diff}(G))$. 

If we choose a [[nLab:partition of unity]] $(\rho_i \in C^\infty(X,\mathbb{R}))$ subordinate to the cover $\{U_i \to X\}$, then we can construct the corresponding coboundary explicitly:

let $(A_i g_{ij}, a_{i j})$ be an arbitrary pseudo-connection cocycle. Consider the Cech-hypercohomology coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i}, 0)$. This lands in the shifted cocycle

$$
  (A'_i := A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}, g_{i j}, a'_{i j})
  \,,
$$

and we can find the new pseudo-components $a'_{i j}$ by 

$$
  a'_{i j} = A'_j - A'_i - d_{dR} g_{i j}
  \,.
$$

Using the computation 

$$
  \begin{aligned}
    \sum_{i_0} \rho_{i_0} (a_{i_0 i} - a_{i_0 j}
    &=
    - \sum_{i_0} \rho_{i_0} (a_{i i_0} + a_{i_0 j}
    \\
    & = \sum_{i_0} \rho_{i_0} a_{i j}
    \\
    & = a_{i j}
  \end{aligned}
$$

we find that these indeed vanish.

The most drastic example for this is a lift $\nabla$ of a cocycle $g = (g_{i j})$ in 

$$
  \array{
    && \mathbf{B}_{diff} U(1)
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
  }
$$

is one which takes all the ordinary curvature forms to vanish identically

$$
  \nabla = (A_i := 0, g_{i j}, a_{i j})
  \,.
$$

This fixes the pseudo-components to be $a_{i j} = - d g_{i j}$. By the above discussion, this pseudo-connection with vanishing connection 1-forms is equivalent, as a pseudo-connection, to the ordinary connection cocycle with connection forms $(A_i := \sum_{i_0} \rho_{i_0} d g_{i_0 i})$. This is a <a href="http://ncatlab.org/nlab/show/connection+on+a+bundle#Properties">standard formula</a> for equipping $U(1)$-principal bundles with Cech cocycle $(g_{i j})$ with a connection.


#### $U(1)_0$-groupoid bundles {#U1GroupoidBundle}

We saw above that the intrinsic coefficient object $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ yields ordinary de Rham cohomology in degree $n \gt 1$. For $n = 1$ we [have](#FlatCircleCohomology) that $\mathbf{\flat}_{dR} \mathbf{B}U(1)$ is given simply by the 0-[[nLab:truncated]] sheaf of 1-forms, $\Omega^1(-) : CartSp^{op} \to Set \hookrightarrow sSet$. Accordingly we have for $X$ a paracompact smooth manifold

$$
  \mathbf{H}(X, \mathbf{\flat}_{dR}\mathbf{B}U(1)) = 
  \Omega^1_{cl}(X)
$$ 

instead of $H^1_{dR}(X)$.

There is a good reason for this discrepancy: for $n \geq 1$ the object $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is the recipient of the intrinsic curvature characteristic morphism

$$
  curv_{\mathbf{B}^{n-1} U(1)} : \mathbf{B}^{n-1} U(1) \to 
   \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
  \,.
$$

For $X \to \mathbf{B}^{n-1} U(1)$ a [[nLab:cocycle]] (an $(n-2)$-gerbe without connection), the cohomology class of the composite $X \to \mathbf{B}^{n-1} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is precisely the obstruction to the existence of a flat extension $X \to \mathbf{\flat} \mathbf{B}^{n-1} U(1) \to \mathbf{B}^{n-1} U(1)$ for the original cocycle.

For $n = 2$ this is the usual [[nLab:curvature]] 2-form of a [[nLab:line bundle]], for $n = 3$ it is curvature 3-form of a [[nLab:bundle gerbe]], etc. But for $n = 1$ we have that the original cocycle is just a map of spaces

$$
  f : X \to U(1)
  \,.
$$

This can be understoody as a cocycle for a _groupoid_ principal bundle, for the 0-truncated groupoid with $U(1)$ as its space of objects. Such a cocycle extends to a flat cocycle precisely if $f$ is _constant_ as a function. The corresponding **curvature 1-form** is $d_{dR} f$ and this is precisely the obstruction to constancy of $f$ already, in that $f$ is constant if and only if $d_{dR} f$ vanishes. _Not_ (necessarily) if it vanishes _in de Rham cohomology_ . 

This is the simplest example of a general statement about curvatures of higher bundles: the curvature 1-form is not subject to gauge transformations.








#### Circle $n$-bundles with connection {#ProofOfDeligneTheorem}


Recall the definition of the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">intrinsic differential cohomology</a> on $X \in Smooth \infty Grpd$ with coefficients in $U(1)$ as the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}^n U(1)) &\to & H_{dR}(X,\mathbf{B}^{n+1} U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))
  }
$$

in [[∞Grpd]], where the morphism on the right picks one base point in each connected component.

+-- {: .un_theorem #DeligneCohomologyTheorem}
###### Theorem

For $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ 
a [[paracompact space|paracompact]] [[smooth manifold]] we have

$$
  H_{diff}(X,\mathbf{B}^n U(1))
  \simeq
  \left( 
     \;\; H(X,\mathbb{Z}(n+1)_D^\infty) \;\;
  \right)
  \times_{\Omega_{cl}^{n+1}(X)} H_{dR}^{n+1}_{int}(X)
  \,.
$$

Here on the right we have the subset of Deligne cocycles that picks for each integral de Rham cohomology class of $X$ only one curvature form representative.

=--

If we make use of the explicit presentation of $Smooth \infty Grpd$ by the [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,loc}$ and the explicit presentation 
$\mathbf{\flat}_{\mathrm{dR}} \mathbf{B}^{n+1}U(1)_{chn}$
for $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ by ordinary [[differential form]]s, as 
[above](#StrucDeRham) we may replace the right morphism in this pullback by $\Omega^{n+1}_{cl}(X) \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}U(1))$ and consider the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}'_{diff}(X,\mathbf{B}^n U(1)) &\to & 
   \Omega^{n+1}_{cl}(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))
  }
$$


+-- {: .un_theorem }
###### Theorem

For $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ 
a [[paracompact space|paracompact]] [[smooth manifold]] we have that

$$
  H'_{diff}(X,\mathbf{B}^n U(1))
  \simeq
     \;\; H(X,\mathbb{Z}(n+1)_D^\infty) \;\;
$$

is the ordinary [[Deligne cohomology]] of $X$ in degree $n+1$.

=--


+-- {: .proof}
###### Proof 

Choose a [differentiably good open cover](#DifferentiablyGoodOpenCover) 
$\{U_i \to X\}$ and let $C(\{U_i\}) \to X$  in $[CartSp^{op}, sSet]_{proj}$ be the corresponding [[Cech nerve]] projection, a cofibrant resolution of $X$.
 
Since the [above model](#CurvatureCharOnBnU1) 
$curv_{chn} : \mathbf{B}_{diff}^n U(1)_{chn} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)_{chn}$
for the intrinsic $curv : \mathbf{B}_{diff}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ is a fibration and $C(\{U_i\})$ is cofibrant, also 

$$
  [Cartp^{op}, sSet](C(\{U_i\}), \mathbf{B}^n_{diff}U(1)_{chn})
  \to
  [Cartp^{op}, sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn})
$$

is a [[Kan fibration]] by the fact that $[CartSp^{op}, sSet]_{proj}$ is an [[simplicial model category]]. Therefore the [[homotopy pullback]] is computed as an ordinary [[pullback]].  

By the [above discussion of de Rham cohomology](#OrdinaryDeRham) we have that we can assume the morphism $H_{dR}^{n+1}(X) \to [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^{n+1}_{chn})$ picks only cocycles represented by globally defined closed differential forms $F \in \Omega^{n+1}_{cl}(X)$.

By the nature of the chain complexes 
$curv_{chn} : \mathbf{B}_{diff}^n U(1)_{chn} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)_{chn}$, we see that the elements in the fiber over such a globally defined $(n+1)$-form $F$ are precisely the cocycles with values only in the "upper row complex" of 
$\mathbf{B}_{diff}^{n}U(1)_{chn}$

$$
  C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-)
  \stackrel{d_{dR}}{\to}
  \cdots 
  \stackrel{d_{dR}}{\to}
  \Omega^n(-)
$$

such that $F$ is the differential of the last term.

This is the complex of sheaves that defines [[Deligne cohomology]] in degree $(n+1)$.

=--





#### Models from $\infty$-Lie integration {#U1FromLieIntegration}

In the [previous section](#FlatCircleCohomology) we discussed a model 

$$
  \array{
    \mathbf{B}^n U(1)_{diff,chn}
    &\stackrel{curv_{chn}}{\to}& 
    \mathbf{\flat}_{dR}\mathbf{B}^{n+1} U(1)_{chn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^n U(1) 
  }
$$

in $[CartSp^{op}, sSet]$ for the canoncal curvature characteristic class $curv : \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ in [[Smooth∞Grpd]] with the special property that it did model the abstract [[(∞,1)-topos]]-theoretic class under the [[Dold-Kan correspondence]] precisely in terms of the familiar [[Deligne cohomology]] coefficient complex.

There is another model for the curvature class in $[CartSp^{op}, sSet]$, one that is useful for constructing the [∞-Chern-Weil homomorphism](#InfChernWeil) that maps from [[nonabelian cohomology]] in $Smooth \infty Grpd$ to $U(1)$-valued differential cohomology. This second model is the one naturally adapted to the construction of the object $\mathbf{B}^n U(1)$ by [[Lie integration]] from its [[∞-Lie algebra]] $b^{n-1} \mathbb{R}$. This is described at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegration">∞-Lie groupoid -- Lie integration</a>. 

For distinguishing the two models, we will indicate the former one by the subscript ${}_{chn}$ and the one described now by the subscript ${}_{simp}$.

+-- {: .un_def }
###### Convention 

Here and in the following we adopt for differential forms on simplices the following notational convention:

* by $\Omega^\bullet(\Delta^n)$ we denote the complex of smooth differential forms on the standard smooth $n$-simplex with **sitting instants**: for every $k \in \mathbb{N}$ every $k$-face of $\Delta^n$ has a neighbourhood of its boundary such that the form restricted to that neighbourhood is constant in the direction perpendicular to that boundary.

* for $U \in CartSp$ we write $\Omega^\bullet(U \times \Delta^k)_{vert}$ for the complex of [[vertical differential form]]s with respect to the trivial simplex bundle $U \times \Delta^k \to U$.

=--

+-- {: .un_def }
###### Definition

For $n \in \mathbb{N}$, define the [[simplicial presheaf]] $\mathbf{B}^n U(1)_{simp} \in [CartSp^{op}, sSet]$ by

$$
  \mathbf{B}^n U(1)_{simp}
  :=
  \mathbf{cosk}_{n+1}
  (
  (U, [k]) \mapsto 
   Hom_{dgAlg}(
     CE(b^{n-1}\mathbb{R}), 
     \Omega^\bullet(U \times \Delta^k)_{vert})
  )
  /\mathbf{B}^n \mathbb{Z}
  \,.
$$

Here $CE(b^{n-1}\mathbb{R})$ is the [[Chevalley-Eilenberg algebra]] of $b^{n-1}\mathbb{R}$, which is simply the graded-commutative [[dg-algebra]] (over $\mathbb{R}$) on a single generator in degree $n$ with vanishing differential.

Moreover, $\mathbf{cosk}_{n+1}(-)$ is the [[coskeleton]]-operation and the quotient is by constant $n$-forms $\omega \in \Omega^n_{cl}(U \times \Delta^k)_{vert}$ such that $\int_{\Delta^n}\omega \in \mathbb{Z}$. We take the quotient as a quotient of abelian [[simplicial group]]s (the group operation is the addition of differential forms).

=--

+-- {: .un_lemma }
###### Observation

Under the [Dold-Kan correspondence](#DoldKan) the [[Moore complex|normalized chain complex]] of $\mathbf{B}^n U(1)_{sim}$ is

$$
  N_\bullet(\mathbf{B}^n U(1)_{simp})
  =
  (
  \cdots
  \to
  \Omega^n_{cl}((-)\times \Delta^{n+1})_{vert}/\sim
  \stackrel{\sum_k (-1)^k \partial_k^* }{\to}
  \Omega^n_{cl}((-)\times \Delta^{n})_{vert}/\sim
  \to
  0 
  \to
  \cdots
  \to
  0
)
  \,,
$$

where $\partial_k : \Delta^n \to \Delta^{n+1}$ denotes the embedding of the $k$th face of the smooth $(n+1)$-[[simplex]].

=--

Here and in the following we indicate the homologically trivial part of the normalized chain complex of an $(n+1)$-coskeletal simplicial abelian group just by ellipses.

+-- {: .un_prop }
###### Proposition

The evident [[fiber integration]] of differential forms over simplices 

$$
  \int_{\Delta^n} : \Omega^\bullet(U \times \Delta^n)
   \to \Omega^\bullet(U)
$$

yields a morphism 

$$
  \int_{\Delta^\bullet} : \mathbf{B}^n U(1)_{simp} \stackrel{\simeq}{\to}
  \mathbf{B}^n U(1)
$$

in $[CartSp^{op}, sSet]_{proj}$, which is a weak equivalence.

=--

This is discussed at [[Lie integration]].

+-- {: .un_def }
###### Definition

Write

$\mathbf{\flat} \mathbf{B}^n \mathbb{R}_{simp}$ for the [[simplicial presheaf]]

$$
  \mathbf{\flat}\mathbf{B}^n \mathbb{R}_{simp}
  :=
  \mathbf{cosk}_{n+1}
  (
    (U,[k])
    \mapsto
    Hom_{dgAlg}(
      CE(b^{n-1}\mathbb{R}),
      \Omega^{\bullet}(U \times\Delta^k)
    )
  )
$$

and write $\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp} \in [CartSp^{op}, sSet]$ for the simplicial presheaf

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp}
  :=
  \mathbf{cosk}_{n+1}
  (
    (U,[k])
    \mapsto
    Hom_{dgAlg}(
      CE(b^{n-1}\mathbb{R}),
      \Omega^{\bullet \geq 1, \bullet}(U \times\Delta^k)
    )
  )
  \,,
$$

where on the right we have the subcomplex of $\Omega^\bullet(U \times \Delta^k)$ on those forms that are non-vanishing on some vector field tangent to $U$.

=--

At <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#DifferentialCoefficientsOfLieInt">∞-Lie groupoid -- Lie integrated ∞-groups -- Differential coefficients</a> the following is shown:

+-- {: .un_lemma }
###### Lemma

The evident [[fiber integration]] over simplices induces morphisms of simplicial presheaves

$$
  \int_{\Delta^\bullet} : 
  \mathbf{\flat} \mathbf{B}^n U(1)_{simp}
  \to 
  \mathbf{\flat} \mathbf{B}^n U(1)_{chn}
$$

and

$$
  \int_{\Delta^\bullet} : 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)_{simp}
  \to 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)_{chn}
$$

that are weak equivalences in $[CartSp^{op}, sSet]_{proj}$.

=--



+-- {: .un_def }
###### Definition

Write $\mathbf{B}^n  U(1)_{diff,simp}$ for the simplicial presheaf given by 

$$
  \mathbf{B}^n  U(1)_{diff,simp}
  :=
  \mathbf{cosk}_{n+1}
  (
    U,[k]
    \mapsto
   \left\{
     \array{
        \Omega^\bullet(U \times \Delta^k)_{vert}
        &\leftarrow&
        CE(b^{n-1}\mathbb{R})
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet(U \times \Delta^k )
        &\leftarrow&
        W(b^{n-1} \mathbb{R})
     }
   \right\}
  ) / \mathbf{B}^n \mathbb{Z}
  \,.
$$

Let the morphism

$$
  curv_{simp}
  :
  \mathbf{B}^n U(1)_{diff,simp}
  \to 
  \mathbf{\flat}_{dR}\mathbf{B}^{n+1} U(1)_{simp}
$$

be the one given by postcomposition with the square of [[nLab:dg-algebra]]s

$$  
  \array{
     CE(b^{n-1}\mathbb{R}) &\leftarrow& 0
     \\
     \uparrow && \uparrow
     \\
     W(b^{n-1}\matbb{R}) &\leftarrow& CE(b^n \mathbb{R})
  }
$$

described at [[nLab:∞-Lie algebra cohomology]].

=--

+-- {: .un_remark }
###### Remark

The set of square diagrams of [[dg-algebra]]s above is over $(U,[k])$ the set of $n$-forms $\omega$ on $U \times \Delta^k$ whose [[curvature]] $(n+1)$-form $d \omega$ has no component with all legs along $\Delta^k$.

=--

+-- {: .un_prop }
###### Proposition

The morphism given by [[fiber integration]] of differential forms over the simplex factor fits into a diagram

$$
  \array{
    \mathbf{B}^n U(1)_{diff,simp} &\stackrel{curv_{simp}}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{simp}
    \\
    \downarrow^{\mathrlap{\int}_{\Delta^\bullet}} && 
    \downarrow^{\mathrlap{\int}_{\Delta^\bullet}}
    \\
    \mathbf{B}^n U(1)_{diff,chn} &\stackrel{curv_{chn}}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}    
  }
  \,,
$$

where the vertical morphisms are weak equivalences. 

=--



+-- {: .un_prop }
###### Proposition

Fiber integration induces a weak equivalence

$$
  \int_{\Delta^\bullet} : 
  \mathbf{B}^n \mathbb{R}_{diff,simp}
  \stackrel{\simeq}{\to}
  \mathbf{B}^n \mathbb{R}_{diff, chn}
$$

=--

+-- {: .proof}
###### Proof

Observe that $\mathbf{B}^n \mathbb{R}_{diff,simp}$ is the [[pullback]] of $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{simp} \to \mathbf{\flat}\mathbf{B}^{n+1} \mathbb{R}_{simp}$ along the evident forgetful morphism from

$$
  (U,[k]) \mapsto \{\Omega^\bullet(U \times \Delta^k) \leftarrow
  W(b^{n-1} \mathbb{R})\}
  \,.
$$

This forgetful morphism is evidently a fibration (because it is a degreewise surjection under Dold-Kan), hence this pullback models the [[homotopy fiber]] of $\mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R} \to \mathbf{\flat} \mathbf{B}^{n+1} \mathbb{R}$. Since by the above fiber integration gives a weak equivalence of pulback diagrams the claim follows.


=--



+-- {: .un_def }
###### Definition

Write $\mathbf{B}^n U(1)_{conn,simp} \hookrightarrow \mathbf{B}^n U(1)_{diff,simp}$ for the sub-presheaf which over $(U,[k])$ is the set of those forms $\omega$ on $U \times \Delta^k$ such that the [[curvature]] $d \omega$ has no leg along $\Delta^k$.

=--

+-- {: .un_cor }
###### Corollary

Under fiber integration over simplices, $\mathbf{B}^n U(1)_{conn,simp}$ is [[quasi-isomorphism|quasi-isomorphic]] to the [[Deligne cohomology]]-complex.


=--



$$
  \array{
     && 
     \mathbf{B}^n U(1)_{conn,simp}
     &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     U(1)(n)_D^\infty
     &&&
     connection
     \\
     & \nearrow & \downarrow && \downarrow
     \\
     \hat X &\to& 
     \mathbf{B}^n U(1)_{diff,simp}
     &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     \mathbf{B}^n U(1)_{diff,chn}
     &&&
     pseudo-connection
     \\
     & \searrow & \downarrow && \downarrow
     \\
     && \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{simp}
      &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}
     &&&
     curvature
  }
  \,.
$$

In summary this gives us the following alternative perspective on connections on $\mathbf{B}^{n-1}U(1)$-[[principal ∞-bundle]]s: such a connection is a cocycle with values in the $\mathbf{B}^n \mathbb{Z}$-quotient of the  $(n+1)$-coskeleton of the simplicial presheaf which over $(U,[k])$ is the set of diagrams of [[dg-algebra]]s

$$
  \array{
    C^\infty(U)\otimes \Omega^\bullet(\Delta^k) 
     &\leftarrow&
    CE(b^{n-1}\mathbb{R})
    &&&
    underlying\;cocycle
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^k) 
     &\leftarrow&
    W(b^{n-1}\mathbb{R})    
    &&& 
    connection
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)\otimes C^\infty(\Delta^k) &\leftarrow& CE(b^n \mathbb{R})
    &&&
    curvature
  }
$$

where the restriction to the top morphism is the underlying cocycle and the restriction to the bottom morphism the curvature form.

The generalization to such diagram cocycles from $b^{n-1}\mathbb{R}$ to general [[nLab:∞-Lie algebra]]s $\mathfrak{g}$ we discuss below in [∞-Lie algebra valued connections](#InfinityLieAlgebraConnection).







### Chern-Weil homomorphism and $\infty$-connections {#StrucChernWeil}

* [[∞-Chern-Weil theory]]


### Higher holonomy and Chern-Simons functional {#StrucChernSimons}

* [[scheiber:∞-Chern-Simons theory]]


## Infinitesimal smooth cohesion

The [[cohesive (∞,1)-topos]] [[SynthDiff∞Grpd]] of 
[[synthetic differential ∞-groupoid]]s is an 
<a href="">infinitesimal cohesive neighbourhood</a> of $Smooth \infty Grpd$

$$
  SynthDiff\infty Grpd
    \stackrel{\overset{\Pi_{inf}}{\to}}
   {\stackrel{\overset{Disc_{inf}}{\leftarrow}}
   {\underset{\Gamma_{inf}}{\to}}}
  Smooth \infty Grpd
  \,.
$$


In [[SynthDiff∞Grpd]] we have [[∞-Lie algebra]]s and [[∞-Lie algebroid]]s as actual [[infinitesimal object]]s. 







## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[continuous ∞-groupoid]]

  * **smooth $\infty$-groupoid**

  * [[synthetic differential ∞-groupoid]]

## References

Section 3.3 in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

A discussion of $\infty$-Lie groupoids as $(\infty,1)$-sheaves on $CartSp$ is in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cech cocycles for differential characteristic classes -- An $\infty$-Lie theoretic construction_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS">web</a>).


The refined [[Lie group cohomology]] is discussed in

* [[Jean-Luc Brylinski]], _Differentiable cohomology of gauge groups_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf)).
{#Brylinski}

For more references see 

* [[Lie theory]], [[Lie integration]] etc. 


The proposal for descent objects for strict $\infty$-groupoid-valued presheaves discussed in [Descent for strict infinity-groupoids](#DescentForStrictInf) appeared in 

* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math/0303175)) {#Street03}

The relation to the general descent condition is discussed in

* [[Dominic Verity]], _[[Verity on descent for strict omega-groupoid valued presheaves|Relating descent notions]]_ {#Verity}



[[!redirects Smooth∞Grpd]]


[[!redirects Lie infinity-groupoids]]
[[!redirects Lie-infinity-groupoid]]

[[!redirects infinity-Lie-groupoid]]
[[!redirects infinity-Lie-groupoids]]

[[!redirects infinity-Lie groupoid]]
[[!redirects infinity-Lie groupoids]]

[[!redirects Lie ∞-groupoid]]
[[!redirects Lie ∞-groupoids]]

[[!redirects ∞-Lie groupoid]]
[[!redirects ∞-Lie groupoids]]

[[!redirects ?LieGrpd]]

[[!redirects Lie-infinity groupoid]]

[[!redirects ∞-Lie groupoid cohomology]]
[[!redirects infinity-Lie groupoid cohomology]]

[[!redirects smooth ∞-groupoid]]
[[!redirects smooth ∞-groupoids]]

[[!redirects smooth infinity-groupoid]]
[[!redirects smooth infinity-groupoids]]

[[!redirects Lie infinity-groupoid]]
[[!redirects Lie infinity-groupoid]]
