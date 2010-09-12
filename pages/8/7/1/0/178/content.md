
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **$\infty$-Lie groupoid** is the generalization of the notion of [[Lie group]] and [[Lie groupoid]] from [[category theory]] to [[higher category theory]] and [[homotopy theory]]:

an $\infty$-Lie groupoid is an [[∞-groupoid]] that is _smooth_ in some sense.


### Reminder: Lie groupoids and differentiable stacks

Before indicating the idea of $\infty$-Lie groupoids in more detail, recall some aspects of the theory of ordinary [[Lie groupoid]]s.

An ordinary [[Lie groupoid]] is usually understood to be a [[groupoid]] [[internalization|internal]] to [[Diff]], possibly with further extra conditions on its structure morphisms. The literature on Lie groupoids is familiar with the fact that it is often useful to regard these internal groupoids after embedding them into the more general context of [[stack]]s on the [[site]] [[Diff]] of all [[smooth manifold]]s: there they are called [[differentiable stack]]s.

Regarding a groupoid internal to manifolds $\mathcal{G}$ as a [[stack]] $\mathcal{G} : Diff^{op} \to $ [[Grpd]] means encoding it in terms of the groupoids of smooth _families_ of objects and morphisms inside it:

* to the point $* \in Diff$ it assigns the underlying bare groupoid $\mathcal{G}(*)$, the groupoid $\mathcal{G}$ with its smooth structure forgotten;

* to a manifold $U \in Diff$ it assigns the groupoid $\mathcal{G}(U)$ whose set of [[object]]s is the set $\mathcal{G}(U)_0 := Hom_{Diff}(U,\mathcal{G}_0)$ of smooth $U$-parameterized [[object]]s in $U$, and whose set of [[morphism]]s $\mathcal{G}(U)_1 := Hom_{Diff}(U,\mathcal{G}_1)$ is the set of smooth $U$-parameterized morphisms in $\mathcal{G}$.

Not every stack on [[Diff]] comes from a [[groupoid]] $\mathcal{G}$ [[internalization|internal to]] [[Diff]] this way. For instance the ([[stackification]] of the) [[groupoid of Lie-algebra valued forms]] for some [[Lie group]] $G$ is a [[concrete presheaf|non-concrete]] stack, which can never be represented by an internal groupoid. Still, most operations that one may want to apply to internal groupoids also make sense for general stacks on [[Diff]]. Indeed, some operations that one may want to apply to internal groupoids take values not in internal groupoids, but in more general stacks: the [[2-category]] $Sh_{(2,1)}(Diff)$ of all stacks on $Diff$ is formally more well behaved than the sub-category of [[differentiable stack]]s inside it. One useful way to formalize all the nice structure that $Sh_{(2,1)}(Diff)$ has is to see that this is a [[2-topos]].

Therefore it is quite useful to think of _every_ stack on $Diff$ as encoding a _smooth groupoid_ and to think of the study of Lie groupoids as being the theory of the [[2-topos]] $Sh_{(2,1)}(Diff)$. The groupoids internal to $Diff$ are special nice objects in this 2-topos: the [[geometric stack]]s.

For this reason, here we shall find it useful to adopt the term _Lie groupoid_ for a general objects in $Sh_{(2,1)}(Diff)$ and to speak of Lie groupoids _[[representable functor|represented]]_ in [[smooth manifold]]s or of [[geometric stack]]s if we mean groupoids internal to manifolds, under the embedding indicated above.


### $\infty$-Lie groupoids as $(\infty,1)$-sheaves / $\infty$-stacks

As we generalize from [[groupoid]]s to [[∞-groupoid]]s, the notion of [[stack]]/[[2-sheaf|(2,1)-sheaf]] generalizes to that of [[∞-stack]]/[[(∞,1)-sheaf]]. Therefore we shall _define_ an $\infty$-Lie groupoid to be an [[(∞,1)-sheaf]] on a [[site]] of smooth test spaces. 

Notice that for the definition of the smooth structure on a [[diffeological space]] or on an ordinary [[Lie groupoid]] it is not in fact necessary to regard these as objects tested by objects in all of [[Diff]]: since smoothness is a local property, it is entirely sufficient to know around every point in the set of [[k-morphism]]s of the $\infty$-groupoid what all the extensions of this point to a _ball_ -shaped smooth family of points around that point are. This is precisely what an [[∞-stack]] on [[CartSp]] encodes, the category of just [[Cartesian space]]s and [[smooth function]]s between them. A discussion of the difference or not between $\infty$-stacks on [[Diff]] and on [[CartSp]] see the section [below](#CartSpAndDiff)


We shall think of the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ as being the context in wich [[∞-Lie theory]] takes place. As before, inside this large context only some nice objects correspond to [[internal ∞-groupoid]]s in [[Diff]] or in [[diffeological space|Diffeol]]. These [[geometric stack|geometric ∞-stack]]s are the concrete or geometric $\infty$-Lie groupoids inside more general objects. One way to make precise the notion of _geometric ∞-stack_ with respect to a chosen notion of _geometric_ is to adopt the concept of [[geometry (for structured (∞,1)-toposes)]].

There are other sites on wich one may want a smooth $\infty$-groupoid to be modeled on. For instance instead of testing only with [[smooth manifold]]s, one may want to test with [[smooth loci]]. An ordinary [[sheaf]] on the category $\mathbb{L}$ of smooth loci is a generalized [[smooth space]] as considered in [[synthetic differential geometry]]. Accordingly, an $\infty$-stack on $\mathbb{L}$ may be thought of as a smooth $\infty$-Lie groupoid to which synthetic differential geometry applies.

The key difference of $\mathbb{L}$ to [[Diff]] is that the former contains smooth [[infinitesimal space]]s. Therefore an $\infty$-Lie groupoid modeled on $\mathbb{L}$ may have spaces of [[k-morphism]]s that have infinitesimal extension in some direction. Notably one obtains a notion of $\infty$-Lie groupoids for which _all $k$-morphisms are infinitesimal_ in a precise sense. It sturns out that such **infinitesimal $\infty$-Lie groupoids** may be identified with [[∞-Lie algebroid]]s: generalizations to [[higher category theory]] of [[Lie algebra]]s and [[Lie algebroid]]s.


## The $(\infty,1)$-topos of $\infty$-Lie groupoids {#InfSheavesOnCartSp}

We discuss in more detail some properties of the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ of [[(∞,1)-sheaves]] on [[CartSp]].

+-- {: .un_defn}
###### Definition

Let $C = $ [[CartSp]] equipped with the structure of a [[site]] by the [[coverage]] of [[good open cover]]s.
 
Write 

$$
  \infty LieGrpd := Sh_{(\infty,1)}(CartSp) 
  \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh_{(\infty,1)}(CartSp)
$$

for the corresponding [[(∞,1)-category of (∞,1)-sheaves]]. 

=--

+-- {: .un_remark}
###### Remark


By the discussion at [Cech localizaton at a coverage](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#LocalizationAtCoverage) this is modeled by the [[Bousfield localization of model categories|left Bousfield localization]] of $[CartSp^{op}, sSet]_{proj}$ at [[Cech nerve]]s of [[covering]] families.

$$
  \array{
    Sh_{(\infty,1)}(CartSp) &\stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}&
    PSh_{(\infty,1)}(CartSp)
    \\
    \uparrow^{\simeq} && \uparrow^{\simeq}
    \\
    ([CartSp^{op}, sSet]_{proj,cov})^\circ
    &\stackrel{\overset{\mathbb{L} Id}{\leftarrow}}{\underset{\mathbb{R} Id}{\to}}&
    ([CartSp^{op}, sSet]_{proj})^{\circ}
  }
  \,.
$$

=--


+-- {: .un_lemma}
###### Lemma

Let $X$ be a [[smooth manifold]], regarded as an object in $sPSh(C)$. Let $\{U_i \to X\}$ be a [[good open cover]] of $X$ and $C(\{U_i\})$ the corresponding [[Cech nerve]]. Then 

$$
  C(\{U_i\}) \stackrel{\simeq}{\to} X
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj,cov}$ and in fact a cofibrant replacement for $X$.

=--

+-- {: .proof}
###### Proof

The morphism $\coprod_i j(U_i) \to X$ of which $C(\{U_i\})$ is the [[Cech nerve]] of a [[local epimorphism]] in that for every $j(V) \to X$ there exists a [[covering]] family $\{V_i \to V\}$ and lifts $\sigma_i$

$$
  \array{
    j(V_i) &\stackrel{\sigma_i}{\to}& \coprod_i j(U_i)
    \\
    \downarrow && \downarrow
    \\
    j(V) &\to& X 
  }
  \,.
$$

Namely take $\{V_i \to V\}$ to be simply (any open refinement of) the open cover of $X$ pulled back to $V$.

By the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CechLocalization">Cech localization at Grothendieck (pre)topologies</a> this implies that $C(\{U_i\}) \to X$ is a weak equivalence in $sPSh(C)_{proj,cov}$.

Moreover, since the cover is _good_ the Cech nerve $C(\{U_i\})$ is degreewise a coproduct of representables. By the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">cofibrant objects</a> this implies that it is cofibrant.

=--

+-- {: .un_remark}
###### Remark

This fact related to the classical [[nerve theorem]] which asserts that the simplicial set obtained by contracting in $C(\{U_i\})$ all copies of [[Cartesian space]]s to the point is a model for the [[homotopy type]] of $X$.

More on that below in the discussion of $Sh_{(\infty,1)}(CartSp)$ as a [[locally ∞-connected (∞,1)-topos]]... 

=--

### $\infty$-Connectedness {#InfConnectedness}

We discuss that $\infty LieGrpd$ is an [[∞-connected (∞,1)-topos]] and recall the notions of intrinsic de Rham objects induced from that.

+-- {: .un_lemma}
###### Lemma

The $(\infty,1)$-topos $\infty LieGrpd$ is an [[∞-connected (∞,1)-topos]].

=--

This means that the [[global section]] [[geometric morphism]] is [[essential geometric morphism|essential]] in that we have a triple of [[adjoint (∞,1)-functor]]s

$$
  (\Pi \dashv LConst \dashv \Gamma)
  :
  \infty LieGrpd \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
$$

and that $LConst$ is a [[nLab:full and faithful (∞,1)-functor]].

Notice that this is the $\infty$-analog of the statement that $Sh(CartSp)$ is a [[connected topos]], as discussed in detail at [[diffeological space]].

+-- {: .proof}
###### Proof

The proof can be found at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#Unstruc">path ∞-groupoid -- Unstructured homotopy ∞-groupoid</a>.

=--

+-- {: .un_lemma}
###### Lemma

In addition the [[(∞,1)-functor]] $\Pi$ preserves finite [[product]]s.

=--

+-- {: .proof}
###### Proof

The proof can be found at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#Unstruc">path ∞-groupoid -- Unstructured homotopy ∞-groupoid</a>.

=--

#### Path $\infty$-groupoids and flat objects

We make the usual definitions in an [[∞-connected (∞,1)-topos]] as described in more detail at [[schreiber:path ∞-groupoid]] and at [[schreiber:differential cohomology in an (∞,1)-topos]]:

+-- {: .un_def}
###### Definition

Write

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat})
  :=
  (LConst \circ \Pi \dashv LConst \circ \Gamma)
  :
  \infty LieGrpd
  \stackrel{\leftarrow}{\to}
  \infty LieGrpd
$$

for the composite [[adjunction]]. For $X,A \in \infty LieGrpd$ we call $\mathbf{\Pi}_{inf}$ the **Lie [[schreiber:path ∞-groupoid]]** of $X$ and we call $\mathbf{\flat}_{inf}A$ the **flat $\infty$-Lie groupoid** of $A$.

=--


#### Coefficients for $\infty$-Lie algebra valued differential forms {#CoeffsLieAlgForms}

For $X \in \infty LieGrpd$ we write $\mathbf{\Pi}_{dR}(X)$ for the [[homotopy cofiber]] of the unit $X \to \mathbf{\Pi}(X)$, i.e. for the [[pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{\Pi}(X) &\to& \mathbf{\Pi}_{dR}(X)
  }
$$

in $\infty LieGrpd$.

For $* \to A \in \infty LieGrpd$ a [[pointed object]], we write $\mathbf{\flat}_{dR} A$ for the [[homotopy fiber]] of the counit $\mathbf{\flat}A \to A$, i.e. for the [[pullback]]

$$
  \array{
    \mathbf{\flat}_{dR}A &\to& \mathbf{\flat}A
    \\
    \downarrow &\swArrow& \downarrow
    \\
    * &\to& A
  }
$$

in $\infty LieGrpd$\,.

=--

#### The canonical form on an $\infty$-Lie group $G$ {#CanonicalForm}

For $G \in \infty LieGrpd$ an [[∞-group]] with [[delooping]] $\mathbf{B}G$ consider the double [[(∞,1)-pullback]] diagram

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
  \,.
$$

The bottom square is an [[(∞,1)-pullback]] by definition. By the pasting law for $(\infty,1)$-pullbacks, the top square being an $(\infty,1)$-pullback implies that the outer rectangle is, too, which identifies $G$ as the top pullback.

This induces a canonical element in the $G$-valued intrinsic de Rham cohomology of $G$:

$$
  (\theta : G \to \mathbf{\flat}_{dR} \mathbf{B}G)
  \in
  \mathbf{H}_{dR}(G, \mathbf{B}G)
  \,.
$$

This we may identify with the $\infty$-groupoid analog of the [[Maurer-Cartan form]] on a Lie group $G$.

#### The vertical form on a $G$-principal $\infty$-bundle {#VerticalForm}


For $P \to X$ the $G$-[[principal ∞-bundle]] classified by a morphism $X \to \mathbf{B}G$  in $\infty LieGrpd$, for each point $x : * \to X$ the pasting diagram of [[(∞,1)-pullback]] squares

$$
  \array{
    G \simeq P_x &\to& P &\to& *
    \\
    {}^{\mathllap{\theta}_x}\downarrow && \downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}G
    &\to&
    At(P)
    &\to&
    \mathbf{\flat} \mathbf{B}G
    \\
    \downarrow && \downarrow && \downarrow
    \\
    * &\to&
    X
    &\to&
    \mathbf{B}G
  }
$$

exhibits the canonical $\mathfrak{g}$-valued vertical intrinsic form 

$$
  (\theta_x : P_x \to \mathbf{\flat}_{dR}\mathbf{B}G)
  \in 
  \mathbf{H}_{dR}(P_x, \mathbf{B}G)
$$

on the fiber $P_x$ of $P$ over $x$.


#### Geometric realization {#GeometricRealization}

+-- {: .un_prop}
###### Proposition

Let $X$ be a [[simplicial manifold]] that is degreewise [[paracompact space|paracompact]], regarded as a [[simplicial object|simplicial]]
[[diffeological space]], hence as an object in $[CartSp^{op}, sSet]$,
hence as an object in $\infty LieGrpd$.

Write $|X| \in $ [[Top]] for the [[geometric realization of simplicial topological spaces]]. Then

$$
  \Pi(X) \simeq |X| \in Top \simeq \infty Grpd
  \,.
$$

=--

+-- {: .proof}
###### Proof

The [[(∞,1)-functor]] $\Pi : \infty LieGrpd \to \infty Grpd$ is the left [[derived functor]] of $\lim_\to : [CartSp^{op}, sSet]_{proj,cov} \to sSet_{Quillen}$. Use the above cofibrant replacement for $X$ degreewise with Dugger's general description of [projective cofibrant objects](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantReplacement) in $[CartSp^{op}, sSet]$ to compute the cofibrant replacement, then apply $\lim_\to$ and use that the [[colimit]] of a [[representable functor|representable]] is the point. The statement then is degreewise the classical [[nerve theorem]].

A detailed proof can be found at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#Unstruc">path ∞-groupoid -- Unstructured homotopy ∞-groupoid</a>.

=--

+-- {: .un_prop}
###### Proposition

Let $G$ be a [[well sectioned simplicial topological group]]. Write, as usual for [[simplicial group]]s, $\mathbf{B}G := \bar W G$ for its <a href="http://ncatlab.org/nlab/show/simplicial+group#Delooping">delooping</a>.

Regard $\mathbf{B}G$ in the canonical way as an object of $[CartSp,sSet]$.
Let $X_\bullet \in [CartSp^{op}, sSet]$ be any other simplicial topological space and let $X \to \mathbf{B}G$ be a morphism. Then:

on such morphisms [[geometric realization of simplicial spaces]] $X_\bullet \mapsto |X_\bullet| :=  \int^{[n]} \Delta^n_{Top} \times X_n \in Top$ preserves [[homotopy fiber]]s (up to weak equivalence).


=--

+-- {: .proof}
###### Proof

In unpublished notes, [[Danny Stevenson]] and [[David Roberts]] show that under [[geometric realization of simplicial topological spaces]] the universal [[simplicial principal bundle]] (see there)
$\mathbf{E}G := W G \to \bar W G$ maps to the universal $|G|$-[[principal bundle]] $\mathcal{E} |G| \to \mathcal{B}|G|$ in [[Top]].

But (as described at [[homotopy fiber]] and [[generalized universal bundle]]) the universal bundle is a means to compute homotopy fibers: the ordinary [[pullback]]

$$
  \array{
    P_\bullet &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X_\bullet &\to& \bar W G
  }
$$

computes the homotopy fiber of $X_\bullet \to \bar W G$. Since [[geometric realization of simplicial spaces]] preserves [[pullback]]s (see there), this is sent to the pullback square

$$
  \array{
    |P_\bullet| &\to& \mathcal{E}G
    \\
    \downarrow && \downarrow
    \\
    |X_\bullet| &\to& \mathcal{B}G
  }
$$

in [[Top]]. Again, this computes the homotopy fiber of the bottom morphism, up to equivalence.


=--

+-- {: .un_corollary}
###### Corollary

The functor $\Pi : Sh_{(\infty,1)}(CartSp) \to \infty Grpd$ preserves homotopy fibers of morphisms represented by degreewise [[paracompact space|paracompact]] simplicial topological spaces $X_\bullet \to \mathbf{B}G$ as above.

=--

> may need to polish the technical assumptions...


One application of this result is in the construction of lifts of [[Whitehead tower]]s in [[∞Grpd]] $\simeq$ [[Top]] to $\infty LieGrpd$. This we discuss in the section [Smooth Whitehead towers](#SmoothWhitehead).


### Relation to $(\infty,1)$-sheaves on all manifolds {#CartSpAndDiff}

In the literature on [[Lie groupoid]]s and [[differentiable stack]]s, these are traditionally conceived as [[stack]]s on the [[site]] [[Diff]] of all [[smooth manifold]]s. As mentioned above, for the purpose of encoding a smooth structure on a [[groupoid]] the category [[Diff]] regarded as a category of test objects is larger than necessary. After all, every manifold is, by definition, itself patched together from [[Cartesian space]]s, and passing to sheaves or stacks on a site really just means that one allows objects patched together from the objects in the site, so that one could just as well take the site to be just that of [[Cartesian space]]s in the first place.

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






### Strict $\infty$-Lie groupoids


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


#### Circle $n$-Lie groupoids  {#BnU1}

Write $U(1) = S^1 = \mathbb{R}/\mathbb{Z}$ for the [[abelian group|abelian]] [[Lie group]] called the [[circle group]] or 1-dimensional [[unitary group]].

##### Delooping {#DeloopingBnU1}

Write $\Xi : Ch_\bullet \to sAb \to sSet$ for the [[Dold-Kan correspondence]] functor and with convenient abuse of notation use the same symbols for its extension $\Xi : [CartSp^{op}, Ch_\bullet] \to [CartSp^{op}, sSet]$ to presheaves.

Write 

$$
  U(1)[n] = [\cdots \to 0 \to C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
$$

for the [[chain complex]] of sheaves concentrated in degree $n$ on $U(1)$.

+-- {: .un_theorem }
###### Theorem

The presheaf $\Xi(U(1)[n]) \in [CartSp^{op}, sSet]_{proj,cov}$ is a fibrant
model of the $n$-fold [[nLab:delooping]] of the group object $U(1)$ in $\infty LieGrpd$.

=--

+-- {: .proof}
###### Proof

The fibrant objects in question are those presheaves that are degreewise [[Kan complex]]es and that satisfy [[descent]] along [[good open cover]]s of [[Cartesian spaces]]. 

For the first, notice that all objects in the image of the Dold-Kan map are Kan complexes. 

For $n = 0$ the second condition says that the ordinary presheaf $Hom_{Diff}(-, U(1)) : CartSp^{op} \to Set \to sSet$ is in fact a [[sheaf]], which clearly it is. 

For $n \geq 1$ the integral cohomology of a [[Cartesian space]] $\mathbb{R}^k$ vanishes and therefore every $U(1)$-cocycle in degree $n$ is trivializable. The automorphism of the trivial $n$-cocycle are precisely the $(n-1)$-cocycles. Continuing this way, one finds that the $n$-groupoid of $n$-cocycle is equivalent to the $n$-fold delooping of the group of 0-cocycle, which is $C^\infty(\mathbb{R}, U(1))$. This is the value of $\Xi(U(1)[n])$ on $\mathbb{R}^k$. Hence the [[descent]] condition is satisfied. 

(Notice as before that here it is crucial that the [[site]] we use is [[CartSp]] and not all of [[Diff]].)

Now consider the delooping statement by induction. We need to show that for $n \geq 1$ the [[loop space object]] $\Omega \Xi(U(1)[n]) \simeq \Xi(U(1)[n-1])$. Since [[∞-stackification]] preserves fniite limits, it is sufficient to compute the [[homotopy pullback]] of $* \to \Xi(U(1)[n]) \leftarrow * $ in $[CartSp^{op}, sSet]_{proj}$.

Therefor we take a fibrant replacement of the morphism $* \to \Xi(U(1)[n])$ to be 

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

The underlying morphism of chain complexes is clearly surjective, hence a projective fibration, hence its image under $\Xi$ is a projective fibration. So the [[homotopy pullback]] in question is the ordinary [[pullback]]

$$
  \array{
    Xi[0 \to C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    &\to&
    \Xi [C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    \\
    \downarrow && \downarrow
    \\
    \Xi [0 \to 0  \to 0 \to \cdots \to 0]
    \to
    \Xi [C^\infty(-,U(1)) \to 0  \to 0 \to \cdots \to 0]
  }
  \,,
$$ 

computed in $[CartSp^{op}, Ch_\bullet]$ and then using that 
$\Xi$ is a right part of a [[Quillen adjunction]], hence [[right adjoint]] and hence preserves products.

=--

+-- {: .un_def }
###### Definition

We therefore write $\mathbf{B}^n U(1) \in [CartSp^{op}, sSet]$ for $\Xi(U(1)[n])$. This may be called the **circle Lie $(n+1)$-group**.

=--


##### Differential coefficients {#DifferentialBnU1}

We now describe the Lie $n$-groupoids $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ and $\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ induced from $\mathbf{B}^n U(1)$ as discussed at [∞-connectedness](#InfConnectedness).



A fibrant representative in $[CartSp^{op}, sSet]_{proj,cov}$ of $\mathbf{\flat} \mathbf{B}^n U(1)$ is

$$
  \Xi[C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)]
  \,.
$$

and of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is

$$
  \Xi[0 \to \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)]
  \,.
$$

=--


+-- {: .proof}
###### Proof

Since the [[global section]] $\Gamma$ amounts to evaluation on the 
point $\mathbb{R}^0$ and since conmstant simplicial presheaves on [[CartSp]]
satisfy descent, we have that $\mathbf{\flat} \mathbf{B}^n U(1)$ is represented by $\Xi[const U(1) \to 0 \to \cdots \to 0]$. This is weakly equivalent to $\Xi[C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]$ by the [[Poincare lemma]] applied to each [[Cartesian space]] (using the same standard logic that proves the [[de Rham theorem]]).

And so a fibration representing the counit $\mathbf{\flat} \mathbf{B}^n U(1) \to \mathbf{B}^n U(1)$ is the image under $\Xi$ of

$$
  \array{
    C^\infty(-,U(1)) &\to& \Omega^1(-) &\to & \cdots &\to& \Omega^n_{cl}(-)
    \\
    \downarrow && \downarrow && && \downarrow
    \\
    C^\infty(-, U(1)) &\to& 0 &\to& \cdots &\to& 0
  }
  \,.
$$

The pullback 

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
$$

of this is a [[homotopy pullback]] and since fibrantions are stable under pullback, we find that the top left is indeed fibrant.

=--

+-- {: .un_remark }
###### Remark

We observe that the complex of sheaves $\mathbf{\flat}\mathbf{B}^n U(1)$ is that which defines flat [[Deligne cohomology]], while that of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is that which computes [[de Rham cohomology]] in degree $n$.

Also notice that the complex that defines $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ has the following description in terms of hom-spaces of [[∞-Lie algebroid]]s.

=--



#### Lie groups {#LieGroups}

Let $G$ be a [[Lie group]], regarded as an object of 
$\mathbf{H} := \infty LieGrpd$. 

##### Delooping {#LieGroupsDelooping}

+-- {: .un_prop }
###### Proposition

A fibrant representative of the [[delooping]] object $\mathbf{B}G$
in $[CartSp^{op}, sSet]_{proj}$ is given by the [[nerve]] of the
one-objec [[Lie groupoid]]

$$
  N(G \stackrel{\to}{\to} *)
$$

=--

+-- {: .proof}
###### Proof

The presheaf is clearly objectwise a [[Kan complex]], being objectwise
the nerve of a groupoid. It satisfies [[descent]] along [[good open cover]]s
$\{U_i \to \mathbb{R}^n\}$ of [[Cartesian space]]s, because the descent $\infty$-groupoid $sPSh(C(\{U_i\}), \mathbf{B}G)$ is $G Bund(\mathbb{R}^n) \simeq G TrivBund(\mathbb{R}^n)$. 

To show that $\mathbf{B}G$ is indeed the [[delooping]] object of $G$
it is sufficient, due to the fact that fact that [[∞-stackification]] preserves finite limits to exhibit a [[homotopy pullback]] 
$G \simeq * \times_{\mathbf{B}G} *$ in $[CartSp^{op}, sSet]_{proj}$.

This is accomplished by the ordinary [[pullback]] of the 
fibrant replacement diagram 

$$
  \array{
    G &\to& N(G\times G \stackrel{\overset{p_1 \cdot p_2}{\to}}{\underset{p_1}{\to}} G)
    \\
    \downarrow && \downarrow
    \\
    * &\to& N(G \stackrel{\to}{\to} *)
  }
$$

as discussed at [[universal principal ∞-bundle]].

=--

##### The universal $G$-principal bundle {#UniversalLieGroupPrincipalBundle}

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



##### $G$-principal bundles


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



##### Differential coefficients {#DiffCoeffsForLieGroup}

For $G$ an ordinary [[Lie group]], we give a concrete representative for the $\infty$-Lie groupoid $\mathbf{\flat} \mathbf{B}G = LConst \Gamma \mathbf{B}G$ in terms of [[Lie algebra]]-valued [[differential form]]s.


Let $\Xi : CrsdCplx \to KanCplx$ now denote the inclusion of [[crossed complex]]es into all [[Kan complex]]es/[[∞-groupoid]]s. 

+-- {: .un_prop }
###### Proposition

The $\infty$-Lie groupoid $\mathbf{\flat}\mathbf{B}G \in \infty LieGrpd$ has a fibrant representative in $[CartSp^{op}, sSet]_{proj,cov}$ given by

$$
  \mathbf{\flat}\mathbf{B}G 
  =
  \Xi[C^\infty(-,G)\times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1^{-1} d p_1}{\to}}{\underset{p_2}{\to}} \Omega^1_{flat}(-,\mathfrak{g})]
  \,,
$$

where $\mathfrak{g}$ is the [[nLab:Lie algebra]] of $G$. 

This is the [[groupoid of Lie-algebra valued forms]] restricted to flat forms.

=--

In other words, a $U = \mathbb{R}^n$-parameterized family of objects of $\mathbf{\flat}\mathbf{B}G$ is given by a [[Lie-algebra valued 1-form]] $A \in \Omega^1(U)\otimes \mathfrak{g}$ whose [[curvature]] 2orm $F_A = d_{dR} A + [A ,\wedge A]  = 0$ vanishes,  and a $U$-parameterized family of morphisms $g : A \to A'$ is given by a smooth function $g \in C^\infty(U,G)$ such that $A' = Ad_g A + g^{-1} d g$, where $Ad_g A = g^{-1} A g$ is the adjoint action of $G$ on its Lie algebra, and where $g^{-1} d g := g^* \theta$ is the pullback of the [[Maurer-Cartan form]] on $G$ along $g$.

+-- {: .proof}
###### Proof

By the above discussion we have that the object in question is

$$
  \mathbb{L}LConst \circ \mathbb{R}\Gamma \mathbf{B}G
  \,,
$$

the image of $\mathbf{B}G$ under the right [[derived functor]] of 
[[global section]]s and the left derived functor of 
[[constant ∞-stack]]s. But since $\mathbf{B}G$ is fibrant 
in $[CartSp^{op}, sSet_{Quillen}]_{proj,cov}$ and every object
in $sSet_{Quillen}$ is cofibrant, this is simply

$$
  \cdots = Lconst \circ \Gamma \mathbf{B}G
  =
  N( const G \stackrel{\to}{\to} *)
  \,.
$$

So first we have to show that this is equivalent to the [[nLab:groupoid of Lie-algebra valued forms|Lie groupoid of flat Lie-algebra valued 1-forms]].
There is an evident morphism

$$
  N( const G \stackrel{\to}{\to} *) 
  \to
  N( G \times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{\to}{\to} 
  \Omega^1_{flat}(-,\mathfrak{g}))
$$

that sends the single object to the trivial 1-form. We claim that this is objectwise an equivalence of groupoids: it is [[essentially surjective functor|essentially surjective]] since every flat $\mathfrak{g}$-valued 1-form on the [[contractible]] $\mathbb{R}^n$ is of the form $g d g^{-1}$ for some function $g : \mathbb{R}^n \to G$ (let $g(x) = P \exp(\int_{0}^x) A$ be the [[parallel transport]] of $A$ along any path from the origin to $x$). Since the gauge automorphism of the trivial $\mathfrak{g}$-valued 1-form are precisely given by the constant $G$-valued functions, this is also objectwise a [[full and faithful functor]]. 

Finally we need to show that $N( G \times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{\to}{\to} \Omega^1_{flat}(-,\mathfrak{g}))$ is fibrant in $[CartSp^{op}, sSet]_{proj,cov}$. This can be seen by observing that this sheaf is the coefficient object that in [[Cech cohomology]] computes $G$-[[principal bundle]]s with flat [[connection on a bundle|connection]] and then reasoning as above: every $G$-principal bundle with flat connection is equivalent to a trivial $G$-principal bundle whose connection is given by a globally defined $\mathfrak{g}$-valued 1-form. Morphisms between these are precisely $G$-valued functions that act on the 1-forms by gauge transformations as in the [[groupoid of Lie-algebra valued forms]].

=--

A detailed discussion of how this arises concretely from the formula
$[\mathbf{\Pi}_1(-), \mathbf{B}G]$ for the [[nLab:right adjoint]] of $\mathbf{\Pi} = LConst \circ \Pi$ and how it is the coefficient object for smooth flat $G$-principal bundles is in [SchrWalI](http://arxiv.org/abs/0705.0452).

+-- {: .un_cor }
###### Corollary

The object 
$\mathbf{\flat}_{dR}\mathbf{B}G $
of <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#deRham">flat intrinsic de Rham coefficients</a> of $\mathbf{B}G$ is represented in $[CartSp^{op}, sSet]$ by the 0-[[truncated]] [[sheaf]] of flat $\mathfrak{g}$-valued forms

$$
  U \mapsto \Omega^1_{flat}(U,\mathfrak{g})
  \,.
$$

=--

+-- {: .proof}
###### Proof

The diagram

$$
  \array{
     \Omega^1_{flat}(-,\mathfrak{g}) 
     &\to&
     \Xi[C^\infty(-,G)\times \Omega^1_{flat}(-,G) \stackrel{\to}{\to} \Omega^1_{flat}(-,\mathfrak{g})]
     \\
     \downarrow && \downarrow
     \\
     {*} &\to& \Xi[C^\infty(-,G) \stackrel{\to}{\to} *]
  }
$$

is a [[pullback]] diagram in $[CartSp^{op}, sSet]_{proj}$ with all objects fibrant and the right vertical morphism being a fibration. Therefore this is a [[homotopy pullback]]. By the above statements and since [[∞-stackification]] preserves finite [[limit]]s, this also models the [[limit in a quasi-category|(∞,1)-pullback]]

$$
  \array{
    \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
  \,.
$$

=--


+-- {: .un_remark }
###### Remark

Writing $T U$ for the [[tangent Lie algebroid]] of $U$ the flat de Rham object of $\mathbf{B}G$ may be also be written as

$$
  \mathbf{\flat}_{dR} \mathbf{B}G : U \mapsto Hom(T U, \mathfrak{g})
  \,,
$$ 

where on the right we have the set of morphisms of [[Lie algebroid]]s. Equivalently in terms of [[Chevalley-Eilenberg algebra]]s this is 

$$
  \mathbf{\flat}_{dR} \mathbf{B}G : 
  U \mapsto Hom_{dgAlg}(CE(\mathfrak{g}),(\Omega^\bullet(U), d_{dR}))
  \,,
$$ 

=--

So far we have discussed the object $\mathbf{\flat}_{dR}\mathbf{B}G$ for $G$ a [[Lie group]]. By the general logic of <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#IntrinsicLieAlgebroids">intrinsic ∞-Lie algebroids</a> the object $\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{B}G$ is the intrinsic incarnation  in $\infty LieGrpd$ of the [[Lie algebra]] $\mathfrak{g}$, defined to be the $(\infty,1)$-pushout

$$
  \array{
    \mathbf{\flat}_{dR}\mathbf{B}G  &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi} \mathbf{\flat}_{dR} \mathbf{B}G
    &\to&
    \mathbf{\Pi}_{dR} \mathbf{B}G
  } 
  \,.
$$

There are some issues here with finding the right cofibrant replacement of this diagram that computes the correct $(\infty,1)$-pushout by an ordinary pushout in $[CartSp^{op}, sSet]$. We describe now some ordinary such pushout, and discuss its relation to the proper $(\infty,1)$-pushout later.

+-- {: .un_prop }
###### Proposition

For $X : CartSp^{op} \to Set$ a sheaf, write

$$
  {\tilde \mathbf{\Pi}}(X) : U \mapsto 
  Hom(U \times \Delta^\bullet_{Diff}, X)
$$

for the simplicial presheaf of paths in $X$. (By the discussion at [[schreiber:path ∞-groupoid]] this is constructed similar to the path model for $\mathbf{\Pi}(X)$, but without any cofibrant replacement thrown in.)

Then the pushout

$$
  \array{
    \mathbf{\flat}_{dR} \mathbf{B}G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}\mathbf{\flat}_{dR} \mathbf{B}G &\to&
    \exp(\mathfrak{g})
  }
$$

is the presheaf

$$
  \exp(\mathfrak{a}) : 
  U \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{g}), C^\infty(U)\otimes \Omega^1(\Delta^\bullet_{diff}))
  \,.
$$

=--

For more discussion of this and its relevance, see the section [Lie integrated ∞-Lie groupoids](#LieIntegrated) below.


##### The canonical form on $G$ {#CanonicalFormOnLieGroup}

The following proposition asserts that the abstract $(\infty,1)$-topos-theoretic definition of the canonical $\mathfrak{g}$-valued form on an $\infty$-Lie group $G$ given [above](#CanonicalForm) reduces indeed to the ordinary notion of [[Maurer-Cartan form]] when $G$ is an ordinary [[Lie group]].

Recall from the [discussion of differential coefficients](#DiffCoeffsForLieGroup) above that the $\infty$-Lie groupoid $\mathbf{\flat}_{dR} \mathbf{B}G$ is modeled by the 0-truncated simplicial sheaf of flat $\mathfrak{g}$-valued forms.

+-- {: .un_prop }
###### Proposition

For $G$ a [[Lie group]], 
the canonical morphism $G \to \mathbf{\flat}_{dR}\mathbf{B}G$ is modeled in $[CartSp^{op}, sSet]$ by the morphism of presheaves 

$$
  Hom_{Diff}(-,G) \to \Omega^1_{flat}(-,\mathfrak{g})
$$

given by

$$
  (g : U \to G) \mapsto (g^* \theta =: g^{-1} d g)
  \,,
$$

where $\theta$ is the [[Maurer-Cartan form]] on $G$.

=--

**Remark.** By the general identification of differential forms on presheaves/[[diffeological space]]s, this morphism _is_ indeed the [[Maurer-Cartan form]] $\theta$ on $G$.

+-- {: .proof}
###### Proof

We need to compute the double [[(∞,1)-pullback]] diagram

$$
  \array{
    G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
  \,.
$$

In the above [discussion of differential coefficients](#DiffCoeffsForLieGroup) we already modeled the lower $(\infty,1)$-pullback square by the ordinary pullback in $[CartSp^{op}, sSet]$ of the presheaf that assigns to $U$ the [[groupoid of Lie-algebra valued forms|groupoid of flat Lie-algebra valued forms]] on $U$:

$$
  \mathbf{\flat} \mathbf{B}G : U \mapsto 
  \{
     A \stackrel{g}{\to} Ad_g A + g^* \theta 
     | A \in \Omega^1_{flat}(U,\mathfrak{g}), g \in C^\infty(U,G)
  \}
  \,.
$$

We need to form the [[homotopy pullback]] of the point in this -- which is the vanishing form $A = 0$. A standard fibrant replacement of $* \to \mathbf{\flat}\mathbf{B}G $ (as discussed at [[generalized universal bundle]]) for this is given by the presheaf 

$$
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

where on the right the commuting triangle in $\mathbf{\flat}_{dR}\mathbf{B}G (U)$ is a morphism from $(g_1,A_1)$ to $(g_2,A_2)$.

The pullback of this along the above model for $\mathbf{\flat}_{dR}\mathbf{B}G \to \mathbf{\flat}\mathbf{B}G$ is the 0-truncated sheaf

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
  \,.
$$

First of all we see that this is indeed weakly equivalent (indeed isomorphic) to $G$, as it sould be. But the point is that we see from the above pullback that the projection $G \to \mathbf{\flat}_{dR}\mathbf{B}G$ is modeled by the morphisms of presheaves


$$
  Hom_{Diff}(-,G) \to \Omega^1_{flat}(-,\mathfrak{g})
$$

which is the codomain evaluation of the above cone morphisms:

$$
  (0 \stackrel{g}{\to} g^* \theta) \mapsto (g^* \theta = g^{-1} d g)
  \,.
$$ 

=--

##### The universal $G$-connection on the universal $G$-principal bundle {#LieGroupUniversalConnection}

> _under construction_

We have seen [above](#UniversalLieGroupPrincipalBundle) that the universal $G$-principal bundle $\mathbf{E}G$ is itself naturally modeled as a Lie [[2-group]]. In the next section [Differential coefficients for Lie 2-groups](#DiffCoeffsForLie2Group) we discuss Lie 2-groups and the canonical differential forms with values in a [[Lie 2-algebra]] on these. We shall now discuss how, in a sense, for the Lie 2-group $\mathbf{E}G$ this universal form is the _universal [[Ehresmann connection]]_ on the universal $G$-principal bundle. The reader not familiar with the section [Differential coefficients for Lie 2-groups](#DiffCoeffsForLie2Group) should skip this section here to come back later. This section here is a corollary or special case or example application of that section.


###### The universal pseudo-connection {#LieGroupUniversalConnectionPseudo}


The Lie 2-group $\mathbf{E}G$ is the one coming from the [[crossed module]] $(G \stackrel{Id}{\to} G)$. Its [[Lie 2-algebra]] is accordingly that given by the [[differential crossed module]] $(\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g})$. The [[Chevalley-Eilenberg algebra]] of this Lie 2-algebra is the [[Weil algebra]] of the Lie algebra $\mathfrak{g}$.

In section [Differential coefficients for Lie 2-groups](#DiffCoeffsForLie2Group) we find a replacement for $\mathbf{\flat}\mathbf{B} \mathbf{E}G$ and $\mathbf{\flat}_{dR} \mathbf{B E}G$ that induces a realization of the Maurer-Cartan form on the Lie 2-group $\mathbf{E}G$ in terms of a span

$$
  \array{
    \mathbf{E}_{diff} G &\stackrel{\theta_{\mathbf{E}G}}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B E}G 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{E}G
  }
$$

realized as follows. The Lie groupoid $\mathbf{E}_{diff}(G)$ is given by

$$
  \mathbf{E}_{diff}G 
  :
  U 
  \mapsto
  \left\{
    \array{
        && (0,0)
       \\
       & {}^{\mathllap{(g_1,a_1)}}\swarrow &
          {}^{\mathllap{f^{-1}}}\swArrow
       & \searrow^{\mathrlap{(g_2,a_2)}}
       \\
      (A_1 = g_1^{-1} d g_1  + g_1^{-1}a_1 g_1, F_{A_1})
      &&\stackrel{(e,\lambda)}{\to}&&
      (A_2 = g_2^{-1} d g_2  + g_2^{-1}a_2 g_2, F_{A_2})
     }
     \;\;\; | \;\;\;
     \array{
       A_i \in \Omega^1(U,\mathfrak{g})  
       \\
       g_i \in C^\infty(U,G)
       \\
       f \in C^\infty(U,G)
     }
  \right\}
  \,,
$$

where the [[cone]] on the right is a [[2-morphism]] in the model for $\mathbf{\flat}\mathbf{B E}G$ for the 2-group $\mathbf{E}G$ as described [here](#http://ncatlab.org/nlab/show/Lie+infinity-groupoid#DiffCoeffsForLie2Group) and constitutes a morphism from the object 

$$
  \array{
    0
    \\
    \downarrow^{\mathrlap{(g_1,a_1)}}
    \\
    (A_1 = g_1^{-1} d g_1 + a_1, F_{A_1})
  }
$$

to the object 

$$
  \array{
    0
    \\
    \downarrow^{\mathrlap{(g_2,a_2)}}
    \\
    (A_2 = g_2^{-1} d g_2 + a_2, F_{A_2})
  }
  \,.
$$

From the description of the [[resolution]] for $\mathbf{\flat}\mathbf{B E}G$ in [Differential coefficients for Lie 2-groups](#DiffCoeffsForLie2Group) we have that in such a morphism the label $g_1$, $g_2$ and $f$ are related by

$$
  g_2 = f g_1
  \,. 
$$

A little inspection shows that all the rest of the data is already fixed by this. Therefore the evident forgetful furnctor $\mathbf{E}_{diff} G \to \mathbf{E}G$ is clearly over each $U$ an [[essentially surjective functor|essentially surjective]] and [[full and faithful functor]], hence indeed a weak equivalence.

The canonical form $\theta_{\mathbf{E}G}$ itself is given by projection onto the codomain of these cones, as for the canonical form on $G$ discussed above. This way we find that the canonical forms on $G$ and on $\mathbf{E}(G)$ fit into a diagram

$$
  \array{
    G &\stackrel{\theta_G}{\to}& \mathbf{\flat}_{dR} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{E}_{diff}G &\stackrel{\theta_{\mathbf{E}G}}{\to}& \mathbf{\flat}_{dR} \mathbf{B E}G
  }
  \,.
$$

Observe that the $G$-action on $\mathbf{E}G$ lifts immediately to an action on the slightly bigger model $\mathbf{E}_{diff}G$, where it is still principal: the only element that leaves any objects or morphisms in $\mathbf{E}_{diff}G$  fixed is the neutral element. 

Explicitly, we have that over $U \in CartSp$ an element $h \in G(U) = C^\infty(U,G)$ acts on a morphism given by a cone as above by

$$
  \left(
    \array{
        && (0,0)
       \\
       & {}^{\mathllap{(g_1,a_1)}}\swarrow &
          {}^{\mathllap{f^{-1}}}\swArrow
       & \searrow^{\mathrlap{(g_2,a_2)}}
       \\
      (A_1 = g_1^{-1} d g_1  + g_1^{-1}a_1 g_1, F_{A_1})
      &&\stackrel{(e,\lambda)}{\to}&&
      (A_2 = g_2^{-1} d g_2  + g_2^{-1}a_2 g_2, F_{A_2})
     }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
    \array{
        && (0,0)
       \\
       & {}^{\mathllap{(g_1 h,a_1)}}\swarrow &
          {}^{\mathllap{(f h)^{-1}}}\swArrow
       & \searrow^{\mathrlap{(g_2 h,a_2)}}
       \\
      ((g_1 h)^{-1} d (g_1 h)  + (g_1 h)^{-1}a_1 g_1 h, h^{-1}F_{A_1} h)
      &&\stackrel{(e,\lambda)}{\to}&&
      ((g_2 h)^{-1} d (g_2 h)  + (g_2 h)^{-1}a_2 g_2 h, h^{-1}F_{A_1} h)
     }
  \right)
  \,,
$$

hence in particular by gauge transformations of the connection forms

$$
  A_i \mapsto h^{-1} A_i h + h^{-1} A_i h
$$

and of the curvatures

$$
  F_{A_i} \mapsto h^{-1} F_{A_i} h
  \,.
$$

It follows that the [[coequalizer]] $\mathbf{B}_{diff}G$ of

$$
  G \times \mathbf{E}G \stackrel{\to}{\to}
  \mathbf{E}G
$$

is the presheaf which over $U \in CartSp$ coequalizes the maps given by

$$
  (h,(g,a)) \mapsto (g,a)
$$

and 

$$
  (h,(g,a)) \mapsto (g\cdot h,a)
  \,,
$$

respectively. This is the presheaf

$$
  \mathbf{B}_{diff}G 
  :
  U 
  \mapsto
  \left\{
        a_1 \stackrel{f,\lambda}{\to} ( a_2
          = f^{-1}(a_1 + d)f - \lambda
        )
    \;\;\; | \;\;\;
     \array{
       a_i, \lambda \in \Omega^1(U,\mathfrak{g})  
       \\
       f \in C^\infty(U,G)
     }
  \right\}
  \,.
$$

The projection map $\mathbf{E}_{diff}G \to \mathbf{B}_{diff} G$ is on objects given by

$$
  (g,a) \mapsto a
  \,.
$$

The evident forgetful functor $\mathbf{B}G \stackrel{\simeq}{\leftarrow} \mathbf{B}_{diff} G$ is, similarly to the previous argument, a weak equivalence.

Therefore the morphism of Lie groupoids

$$
  \mathbf{E}_{diff}G \to \mathbf{B}_{diff}G
$$

that we have obtained is indeed another model for the universal $G$-principal bundle, somewhat bigger than the canonical one. 


**Cocycles with values in $\mathbf{B}_{diff}G$.

For $\{U_i \to X\}$ a [[good open cover]] of a [[paracompact space|paracompact]] [[smooth manifold]] $X$ and $C(\{U_i\})$ the [[Cech nerve|Cech groupoid]] we have that a morphism

$$
  X \stackrel{\simeq}{\leftarrow}
  C(\{U_i\})
  \stackrel{(A_i g_{i j}, \lambda_{i j})}{\to}
  \mathbf{B}_{diff}G
$$

of groupoid-valued presheaves is a $G$-[[Cech cohomology|Cech cocycle]] on $X$ _together with_ on each patch $U_i$ a choice of a [[Lie-algebra valued 1-form]] $A_i \in \Omega^1(U_i, \mathfrak{g})$. These 1-forms do _not_ need to satisfy any condition on double overlaps (yet): by the above characterization the failure of the $(A_i)$ to satisfy the usual Cech-de Rham cocycle condition for a connection on a bundle is measure on double overlaps by the forms 

$$
  \lambda_{i j}
  =
  A_j - g_{ij}^{-1}(A_i + d)g_{ij}
  \,.
$$ 

Such data is sometimes called a _pseudo-connection_ . By itself it contains no information (and otherwise $\mathbf{B}_{diff} G \to \mathbf{B}G$ would not be a weak equivalence) but it does serve to model the universal [[curvature characteristic form]] as a  2-[[anafunctor]] out of $\mathbf{B}G$. We will see [below](#http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieGroupUniversalConnectionProper) that in the [[homotopy fiber]]s of the morphism that this induces on cocycles, we do find the genuine (non-pseudo) connection forms.


###### The universal curvature characteristic forms {#LieGroupUniversalConnectionCurvature}

In order to obtain the universal [[curvature characteristic form]]s of the universal pseudo-connection we need to find the universal coefficient object in the bottom right of

$$
  \array{
     G &\stackrel{\theta_G}{\to}& \mathbf{\flat}_{dR} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{E}_{diff}G &\stackrel{\theta_{\mathbf{E}G}}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B E}G 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}_{diff} G &\to& \mathbf{\flat}_{dR}^{inv} \mathbf{B E}G
  }
  \,.
$$

This is the [[coequalizer]] of the two composite maps

$$
  G \times \mathbf{E}G \stackrel{\overset{\theta_{\mathbf{E}G}\circ \rho}{\to}}{\underset{\theta_{\mathbf{E}G}\circ p_1}{\to}}
  \mathbf{\flat}_{dR} \mathbf{E}G
  \,.
$$

The bottom one picks the codomain of the cones depicted above, and the top one first acts with $G$ as described above, and then picks the codomain. On objects the bottom is given by

$$
  (h, (g,a, F_A)) \mapsto (A:= g^{-1} d g + g^{-1} a g, F_A)
$$

whereas the top map is

$$
  (h, (g,a)) \mapsto (h^{-1} A h + h^{-1} d h, h^{-1} F_A h)
  \,.
$$

So the action divides out gauge transformations.


We therefore obtain elements in the coequalizer from the [[curvature characteristic form]]s: if $A$ and $A'$ are related by a gauge transformation, then for each [[invariant polynomial]] $P_i$ we have $P(F_A) = P_{F_{A'}}$.


So define $\mathbf{\flat}_{dR}^{inv}\mathbf{B E} G$ to be the Lie groupoid whose

* $U$-parameterized families of objects are collections $(P_i(F_{A}))$ of [[curvature characteristic form]]s (for some connection form $A \in \Omega^1(U,\mathfrak{g})$ which is not part of the data)

* $U$-parameterized families of morphisms are collections of [[Chern-Simons form]]s $(CS_i(A,A'))$  modulo exact forms interpolating between these.

Then evaluation of curvature in invariant polynomials yields yields a morphism

$$
  \mathbf{\flat}_{dR} \mathbf{B}  INN(G)
  \to
  \mathbf{\flat}^{inv}_{dR} \mathbf{B E}G
$$

where $i$ ranges over the generators of invariant polynomials and $n_i$ is the degree of the $i$th generator, that fits into  the above diagram for $Q$.

This morphism sends over $U \in $ [[CartSp]] the form $A \in \Omega^1(U,\mathfrak{g})$ to a collection $\sum_i P_i(F_{A})$ of [[curvature characteristic form]]s and sends any morphism between two such forms (which, recall, need not be a gauge transformation of forms but may involve a shift of conneciton forms) to the [[Chern-Simons form]] interpolating between these, which is indeed well defined modulo exact forms

$$
  curv_G : 
  \left(
    (A, F_A) 
    \stackrel{\lambda}{\to}
    (A', F_{A'})
  \right)  
  \;\;\;
  \mapsto
  \;\;\;
  \sum_i P_i(F_A)
  \stackrel{\sum_i CS(A,A')}{\to}
  \sum_i P_i(F_{A'})
  \,.
$$

###### The universal connection {#LieGroupUniversalConnectionProper}

In total we find a model for the universal (pseudo-)[[Ehresmann connection]] on the universal $G$-principal bundle in terms of a diagram

$$
  \array{
    G &\stackrel{\theta_G}{\to}& \mathbf{\flat}_{dR} \mathbf{B}G
    &&& vertical\; form
    \\
    \downarrow && \downarrow
    \\
    \mathbf{E}_{diff}G &\stackrel{\theta_{\mathbf{E}G}}{\to}& \mathbf{\flat}_{dR} \mathbf{B E}G
    &&&
   connection \; and \; curvature
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}_{diff} G 
    &\stackrel{char_G}{\to}& 
    \mathbf{\flat}^{inv}_{dR} \mathbf{B E}G
    &&&
    curvature\; characteristic\; class
  }
  \,.
$$

The morphism

$$
  char_G : \mathbf{B}G_{diff} \to 
  \mathbf{\flat}^{inv}_{dR} \mathbf{B E}G
$$

that arises from pushing down the canonical form/universal pseudo-connection $\theta_{\mathbf{E}G}$ on $\mathbf{E}G$ is the **universal [[curvature characteristic form]]** . We notice that cohomology with coefficients in $\mathbf{\flat}_{dR}^{inv} \mathbf{B E}G$ sits in the [[de Rham cohomology]] $\prod_i H^{n_i}_{dR}(X)$ and that every cohomology class in there has a representative

$$
  \array{
    C(\{U_i\})
    &\to&
    \mathbf{\flat}_{dR}^{inv} \mathbf{B E}G
    \\
    {}^{\mathllap{\simeq}}\downarrow
    \\
    X
  }
$$

given by a collection of globally defined forms, in other words we have representatives for each cohomology class that extend as

$$
  \array{
    C(\{U_i\})
    &\to&
    \mathbf{\flat}_{dR}^{inv} \mathbf{B E}G
    \\
    {}^{\mathllap{\simeq}}\downarrow & \nearrow
    \\
    X
  }
  \,.
$$

Picking one such representative for each class yields gives a morphism

$$
  \prod_i H^{n_i}_{dR}(X) \to 
   \mathbf{H}(X,\mathbf{\flat}_{dR}^{inv} \mathbf{B E}G)
  \,.
$$

By the general reasoning of [[schreiber:differential cohomology in an (∞,1)-topos]] we have that the differential cocycles proper are those in the [[homotopy pullback]] $\mathbf{H}_{diff}(X,\mathbf{B}G)$ of this morphism along the curvature class morphism

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}G) &\to& \prod_i H^{n_i}_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}G) &\stackrel{char_G}{\to}&
    \mathbf{H}(X,\mathbf{\flat}_{dR}^{inv} \mathbf{B E}G)
  }
 \,.
$$

Using that the quotient map is a Kan fibration, we find hat the bottom morphism evaluated on a Cech nerve is a Kan fibration, so that this homotopy pullback is computed as the ordinary pullback of cocycles.

It follows that a differential cocycle is a pseudo-connection on a bundle, that does satisfy the condition that the connection forms $(A_i)$ induce on double overlaps _exact_ [[Chern-Simons form]]s interpolating between their [[curvature characteristic form]]s. This is solved in particular by proper connections. 

This way the connection cocycle condition is imposed after all on the differential cocycles, even though the universal conneciton is a pseudo-connection.

###### Differential K-theory classes {#LieGroupUniversalConnectionKTheory}

But notice that in the above differential cohomology cocycle groupoid $\mathbf{H}_{diff}(X, \mathbf{B}G)$ we have _coboundaries_ that are more general than usual gauge transformations of connections:

Again by the nature of $\mathbf{\flat}_{dR}^{inv} \mathbf{B E}G$ we have that a coboundary between $(A_i, g_{i j})$ and $(A'_i, g'_{i j})$ is a transformation such that the interpolating [[Chern-Simons form]]s of the [[curvature characteristic form]]s are exact. 

This equivalence relation is that defining [[Simons-Sullivan structured bundle]]s. For $G = U$ the [[unitary group]] these represent classes in the [[differential K-theory]] of $X$. 


... (under construction)... 

#### Strict Lie 2-groups {#StrictLie2Groups}

Let now $G = \Xi[G_2 \to G_1]$ be a strict [[Lie 2-group]] coming from a smooth  [[crossed module]] $G_2 \stackrel{\delta}{\to} G_1 $ with action $\alpha : G_1 \to Aut(G_2)$.

##### Delooping {#StrictLie2GroupsDelooping}

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


##### Differential coefficients {#DiffCoeffsForLie2Group}

We work out, following the [general definition](#CoeffsLieAlgForms) the coefficient object for [[2-groupoid of Lie 2-algebra valued forms|Lie 2-algabra valued forms]] $\mathbf{\flat}_{dR} \mathbf{B}[G_2\to G_1]$ for $(G_2 \to G_1)$ a Lie [[crossed module]].

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

#### Examples

##### The String Lie 2-group {#String2Group}

There is a strict Lie 2-group model for the [[string Lie 2-group]].

+-- {: .un_prop}
###### Proposition

The [[string Lie 2-algebra]] in the form $\mathfrak{g}_\mu$ is equivalent to the strict [[Lie 2-algebra]] given by the [[differential crossed module]] $\hat \Omega \mathfrak{g} \to P \mathfrak{g}$, where...

=--

(...)

We now describe three different but equivalent strict Lie 2-group models for the String 2-group. 

(...)

###### Connections

(...)

##### The Fivebrane Lie 6-group

There is a strict Lie 6-group model of the [[fivebrane Lie 6-group]].

There is a strict Lie 2-group model for the [[string Lie 2-group]]

###### Connections

(...)

### General $\infty$-Lie groupoids

We now discuss general, not-necessarily strict $\infty$-Lie groupoids.


#### Lie-integrated $\infty$-Lie groupoids {#LieIntegrated}

We discuss here $\infty$-Lie groupoids that arise as the [[Lie integration]] of an [[∞-Lie algebroid]].


##### Lie integration {#LieIntegration}

+-- {: .un_def }
###### Definition
**(forms on the simplex)**

Write $\Delta_{Diff} : \Delta \to CartSp \hookrightarrow sPSh(CartSp)$ for the cosimplicial object of standard smooth simplices.

Write $\Omega^\bullet_{si}(\Delta^n_{Diff})$ for the [[dg-algebra]] of those differential forms on $\Delta^n_{Diff}$ that have the property that for every $k \in \mathbb{N}$ every $k$-face of $\Delta^n_R$ has an open neighbourhood of its boundary such that the form restricted to that face is constant in the direction perpendicular to that boundary.

=--


+-- {: .un_def }
###### Definition

Let $\mathfrak{g}$ be an [[L-∞-algebra]], dually characterized by its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g}) \in dgAlg$.

Write $\exp(b \mathfrak{g}) \in [CartSp^{op}, sSet]$ for the object

$$
  U,[n] \mapsto
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet_{si}(\Delta^n_{Diff}) \otimes C^\infty(U))
  \,.
$$


For $n \in \mathbb{N}$ 
we say the Lie $n$-groupoid universally intergating $\mathfrak{g}$
is the $n$-[[truncated|truncation]] of this object

$$
  \tau_n \exp(\mathfrak{a})
  \,.
$$

Realized objectwise as the $(n+1)$-[[simplicial skeleton|simplicial coskelton]]

$$
  U,[n] \mapsto
  \mathbf{cosk}_{n+1}
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet_{si}(\Delta^n_{Diff}) \otimes C^\infty(U))
  \,.
$$

=--

+-- {: .un_remark }
###### Remark

The generalization of this procedure from $\infty$-Lie algebras $\mathfrak{g}$ to [[∞-Lie algebroid]]s $\mathfrak{a}$ is essentially straightforward, except for a slight technicality: instead of the presheaf construction $U \mapsto Hom_{dgAlg}(CE(\mathfrak{g}), C^\infty(U) \otimes \Omega^\bullet(\Delta^n_{Diff}))$ one needs to consider the construction

$$
  conc(U \mapsto Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(U \times \Delta^n_{Diff})))
  \,,
$$

where $conc$ denotes the operation of passing to [[concrete presheaves]].

=--


+-- {: .un_remark }
###### Remark

The bare [[∞-groupoid]] 

$$
\Gamma \exp(\mathfrak{a} )
 : [n] \mapsto Hom_{dgAlg}(CE(\mathfrak{g}), 
    \Omega^\bullet(\Delta_{Diff}^{n}))
$$ 

underlying the untruncated $\infty$-Lie groupoid integrating $\mathfrak{g}$ is essentiall the [[Sullivan construction]] on $CE(\mathfrak{g})$, familiar from [[rational homotopy theory]]. The fact that this construction may be thought of in terms of [[Lie integration]] was amplified in 

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$-algebras_ ([arXiv])

following Hinich.

A refinement of this construction to [[internal ∞-groupoid]]s in [[nLab:Banach space]]s was considered in 

* [[Andre Henriques]], _Integrating $L_\infty$-algebras_ ([arXiv])

For more see [[Lie integration]].

The evident refinement of the [[Sullivan construction]] to $\infty$-Lie groupoids as considered here, parameterized over smooth test spaces, was mentioned around

* [[Urs Schreiber|U.S.]], _Differential nonabelian cohomology_ talk at _Higher Structures in Math and Physics_ Lausanne (2008) ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Lausanne.pdf))

and was considered around the same times also by [[Dmitry Roytenberg]]. 

In 

* [[Pavol Severa]], _..._ 

is given a proposal for how to realize Lie differentiation in this context. Below we will see that, in analogy to and generalizing the above examples, the Lie differentiation of $\tau_n \exp(\mathfrak{g})$ is canonically induced by passing to its intrinsic de Rham coefficient object $\mathbf{\flat}_{dR} \tau_n \exp(\mathfrak{a})$. Below in 
[Infinitesimal differential coefficients](#InfinitesimalDifferentialCoefficients) we discuss how these are realized in terms of infinitesimal paths in the $\infty$-Lie groupoid. This is at least in spirit close to &Scaron;evera's construction. A more detailed discussion of the relation should be given somewhere, eventually.


=--


##### The Lie-integrated universal principal $\infty$-bundle {#LieIntUnivBund}

We describe a construction of the [[universal principal ∞-bundle]]
of a [Lie integrated](#LieIntegration) $\infty$-Lie group $G$.

Let $\mathfrak{g}$ be a [[Lie n-algebra]]. The construction we consider works for choices $n \in \mathbb{N}$ such that the $\infty$-Lie groupoid

$$
  \tau_{\leq n}\exp(\mathfrak{g})
$$

is equivalent to 

$$
  \mathbf{B}G := \tau_{\leq {n+1}} \exp(\mathfrak{g})
  \,,
$$

i.e. that we can truncate the [[Sullivan construction]] one degree "too high" without picking up a superfluous homotopy group (see [[Lie integration]] for details on this). 

**Example.** This is for instance the case for $\mathfrak{g}$ an ordinary [[Lie algebra]], $n = 1$: in that case $\tau_{\leq 1}\exp(\mathfrak{g})$ is the one-object Lie groupoid $\mathbf{B}G$  for $G$ the simply connected Lie group integrating it, and since for every Lie algebra we have $\pi_2(G) = 0$ there is a trivial [[homotopy group]] in degree 2 and so (by the discussion at [[Lie integration]]) $\mathbf{B}G \simeq \tau_{\leq 2}\exp(\mathfrak{g})$.

The 1-morphism in $\tau_{\leq 2}\exp(\mathfrak{g})$ are based paths in $G$, the [[2-morphism]]s are homotopy-classes (rel boundary) of surfaces in $G$. The equivalence $\exp_{\leq 2} \exp(\mathfrak{g}) \to \mathbf{B}G$ is obtained by sending a path to its endpoint. This situation is discussed in detail at [The string Lie 2-group](#String2Group).


+-- {: .un_def}
###### Definition

For $\mathfrak{g}$ an [[L-∞-algebra]] write $inn(\mathfrak{g})$ for the
$L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] is the [[Weil algebra]] $W(\mathfrak{g})$ of $\mathfrak{g}$:

$$
  CE(inn(\mathfrak{g})) = W(\mathfrak{g})
  \,.
$$

=--

The $L_\infty$-algebra $inn(\mathfrak{g})$ is an _$L_\infty$-algebroidal model_ for the universal $\mathfrak{g}$-principal bundle, in analogy to a [[groupal model for universal principal ∞-bundles]].

+-- {: .un_example}
###### Example
**(Cartan model)**

For $\mathfrak{g}$ an ordinary [[Lie algebra]], the [[Lie 2-algebra]] $inn(\mathfrak{g})$ is the one coming from the [[differential crossed module]] $(\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g})$. That this is a Lie 2-algebraic model for the <a href="http://ncatlab.org/nlab/show/groupal+model+for+universal+principal+infinity-bundles#OrdinaryGroups">Segal groupal model of the universal G-bundle</a> is implicit in the [[Cartan model of equivariant cohomology]], which is a [[Lie algebroid]]-model of the [[Borel construction]] $\mathbf{E}G \times_G V$.

=--

+-- {: .un_def}
###### Definition
**(integrated universal principal $\infty$-bundle)**

The [[Lie integration]] of $inn(\mathfrak{g})$ we write

$$
  \mathbf{B}\mathbf{E}G := \tau_{\leq {n+1}}\exp(inn(\mathfrak{g})))
  \,.
$$

The canonical inclusion $\mathfrak{g} \to inn(\mathfrak{g})$ induces a morphism of $\infty$-Lie groupoids

$$
  \tau_{n+1}\exp(\mathfrak{g} \to inn(\mathfrak{g}))
  :
  \mathbf{B}G \to \mathbf{B}\mathbf{E}G
  \,.
$$

This induces the corresponding morphism of [[∞-Lie group]]s.

$$
  G \to \mathbf{E}G
  \,.
$$

=--


+-- {: .un_prop}
###### Observation

Since $W(\mathfrak{g})$ is contractible (has vanishing cochain cohomology) we have a weak equivalence

$$
  \mathbf{E}G \simeq *
  \,.
$$

So the construction $\mathbf{E}G = \tau_{n+1}\exp(\mathfrak{g})$ is a [[groupal model for universal principal ∞-bundles]].

=--

(...)

##### Examples

We spell out some examples of [[Lie integration]].

###### Integration of a Lie algebra

+-- {: .un_prop}
###### Proposition

Let $\mathfrak{g}$ be an ordinary finite-dimensional [[Lie algebra]] and write $G$ for the corresponding simply connected [[Lie group]].

We have

$$
  \mathbf{B}G \simeq \tau_1 \exp(b \mathfrak{g})
$$ 

=--


+-- {: .proof}
###### Proof

We observe that $\exp(\mathfrak{g})$ has a single object. 
A [[k-morphism]] in $\exp(\mathfrak{g})$ is a  flat 
$\mathfrak{g}$-valued 1-form on $\Delta^k_{Diff}$. Hence morphisms
of $\tau_1 \exp(\mathfrak{g})$ are 
smooth $\mathfrak{g}$-valued 1-forms
on the interval, two of them are connected by a 
contractibel space of higher cells if they may be 
interpolated by a flat $\mathfrak{g}$-valued 1-form on the 
disk. That this collection of morphisms modulo this relation is indeed 
the simply connected Lie group $G$, with its standard smooth structure,
is reviewed and discussed in detail in 

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackest_
  ([arXiv](http://arxiv.org/abs/math/0105033))


=--


###### Integration to line $n$-groups {#IntegrationOfBnR}

+-- {: .un_def}
###### Definition

Write $b^n \mathbb{R}$ for the [[L-∞-algebra]] whose [[Chevalley-Eilenberg algebra]] is given by a single generator in degree $(n+1)$ and vanishing differential.

Write $e b^n \mathbb{R}$ for the dg-algebra on one generator in degree $(n+1)$ and one in degree $(n+2)$ and the differential taking the former to the latter.

=--



+-- {: .un_lemma}
###### Lemma

For each $n \in \mathbb{N}$ the diagram

$$
  \array{
    \exp(b^n \mathbb{R}) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \exp(e b^n \mathbb{R}) &\to& \exp(b^{n+1}\mathbb{R})
  }
$$

is a pullback diagram in $sPSh(CartSp)$. Moreover, there is a morphism of diagrams

$$
  \array{
    \exp(b^{n} \mathbb{R})
    &\to&
    \exp(e b^{n} \mathbb{R})
    &\to& 
    \exp(b^{n+1} \mathbb{R})
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}^n \mathbb{R} &\to& \mathbf{E}\mathbf{B}^n \mathbb{R}
    &\to&
    \mathbf{B}^{n+1} \mathbb{R}
  }
$$

where the vertical morphisms are acyclic fibrations, induced by sending differential $n$-forms on the $n$-simplex to their integral over that $n$-simplex. 

=--

+-- {: .proof}
###### Proof

The key fact underlying this is that a closed smooth $n$-form on the $n$-sphere may be extended smoothly to a closed $n$-form on the $(n+1)$-ball precisely if its integral over the sphere vanishes. 

From this it follows that also every closed $n$-form on the $k$-sphere for $k \gt n$ may be extended as a closed $n$-form to the $(n+1)$-ball. The same holds for smooth families of forms. This implies that $\exp(b^n \mathbb{R}) \to \mathbf{B}^n \mathbb{R}$ is an acyclic fibration for all $n$.

=--



##### Integration of $\infty$-Lie algebra cocycles {#IntegrationOfCocycles}

We discuss how under [[Lie integration]] a [[cocycle]] in [[∞-Lie algebra cohomology]] integrates to a cocycle on $\infty$-Lie groupoids.

For $\mathfrak{g}$ an [[∞-Lie algebra]], an $n$-cocycle on $\mathfrak{g}$ (with "values in the trivial module $\mathbb{R}$") is a morphism

$$
  \mu : \mathfrak{g} \to b^{n-1} \mathbb{R}
  \,.
$$

Dually this is a [[dg-algebra]]-morphism of [[Chevalley-Eilenberg algebra]]s

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1}\mathbb{R}) : \mu
  \,.
$$

Since the dg-algebra on the right is [[semifree dga|semifree]] on a single generator in degree $(n+1)$ and with vanishing differential, this is the same as a closed element in the CE-algebra

$$
  \mu \in \wedge^n \mathfrak{g}^* \;\;\; d_{\mathfrak{g}} \mu = 0
  \,.
$$

Applying the [[Lie integration]] functor $\exp(-)$ we obtain a morphism between the $\infty$-Lie groupoid incarnations of $\mathfrak{g}$ and $b^{n-1}\mathbb{R}$

$$
  \exp(\mu) : \exp(\mathfrak{g}) \to \exp(b^{n-1}\mathbb{R})
  \,.
$$

Remember that the [[Lie integration]] proper of a Lie $k$-algebra $\mathfrak{g}$ is the $k$-[[truncated|truncation]] 

$$
  \mathbf{B}G := \tau_k \exp(\mathfrak{g})
$$


of $\exp(\mathfrak{g})$. Similarly, the Lie integration of $b^{n-1} \mathbb{R}$ is the $n$-truncation, which by [Integration of abelian L-infinity algebras](#IntegrationOfBnR) is

$$
  \tau_n \exp(b^{n-1} \mathbb{R})
  \simeq
  \mathbf{B}^n \mathbb{R}
  \,.
$$

In general $k$ and $n$ will differ. The integration of the cocycle involves finding a discrete $\infty$-group $K$ such that the morphism nevertheless lifst to

$$
  \array{
    \tau_n \exp(\mathfrak{g}) &\stackrel{\tau_n \exp(\mu)}{\to}& \tau_n(b^{n-1} \mathbb{R}) 
      \simeq \mathbf{B}^n \mathbb{R}
    \\
    \downarrow && \downarrow
    \\
    \tau_k \exp(\mathfrak{g})
    &\to&
    \mathbf{B}^n \mathbb{R}/K
  }
$$

###### Integration of the String 3-cocycle

For $\mathfrak{g}$ a semisimple Lie algebra with binary [[invariant polynomial]] $\langle -,-\rangle$, we have a canonical 3-cocycle

$$
  \mu = \langle -, [-,-]\rangle \in CE(\mathfrak{g})
  \,.
$$

Since this controls the [[string Lie 2-algebra]], we call it the String-cocycle.

We have that $\tau_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G$ for $G$ the simply connected Lie group integrating $\mathfrak{g}$. On the other hand, since $\tau_3(G) \simeq \mathbb{Z}$ we have the pushout

$$
  \array{
    \mathbf{B}^3 \mathbb{Z} &\to& \tau_3 \exp(\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    \mathbf{E} \mathbf{B}^2 \mathbb{Z} &\to& \tau_3 \exp(\mathfrak{g})/\mathbb{Z}
  }
$$

and a weak equivalence $\tau_3 \exp(\mathfrak{g})/\mathbb{Z} \to \mathbf{B}G$.

Accordingly, the Lie algebra 3-cocycle integrates to a Lie group [[cocycle]] 

$$
  \array{
    \tau_3 \exp(\mathfrak{g}) &\stackrel{\exp(\mu)}{\to}&
    \mathbf{B}^3 \mathbb{R}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\int_\mu}{\to}&
    \mathbf{B}^3 (\mathbb{R}/\mathbb{Z})
  }
  \,.
$$

Unwinding the definitions, we see that 

* $\tau_3 \exp(\mathfrak{g})$ has as 1-morphisms based paths in $G$, as 2-morphisms based surfaces in $G$; as 3-morphisms unique morphisms between any pair of parallel 2-morphisms;

* the integrated cocycle $\int_\mu$ takes on 3-morphism the value obtained by choosing a 3-ball $\sigma : \Sigma_3 \to G$ cobounding the boundary 2-morphisms-surfaces (which always exists since $\pi_2(G) = 0$) and sending it to the 3-morphism labeled by $\int_{\Sigma_3} \sigma^* \mu \in \mathbb{R}/\mathbb{Z}$, which is well defined since $\mu$ has integral periods on $G$ (times some normalization constant).

We find that the [[string 2-group]] is the [[homotopy fiber]] of this integrated cocycle, i.e the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{B}String_\mu(G) &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\int \mu}{\to}& \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
  }
$$

in $\mathbf{H}$.

###### Parallel transport: integration of $\infty$-Lie algebra valued differential forms {#ParallelTransport}

A special case of the general notion of cocycle in an [[∞-Lie algebroid]] is of general interest: for $X$ a [[nLab:smooth manifold]] write $T X$ for the [[tangent Lie algebroid]] of $X$. For $\mathfrak{g}$ any [[∞-Lie algebra]] or [[∞-Lie algebroid]], a _cocycle_ on $T X$ with coefficients in $\mathfrak{g}$, i.e. a morphism

$$
  \omega : T X \to \mathfrak{g}
$$

is a collection of flat [[schreiber:∞-Lie algebroid valued differential forms]]. In the special case that $\mathfrak{g}$ is an ordinary Lie algebra, this reduces to the standard notion of flat [[Lie-algebra valued 1-form]] with vanishing [[curvature]] 2-form.

The integration of $T X$ is (at least locally) the [[schreiber:path ∞-groupoid]]. The integration of the cocycle $\omega$ is its [[parallel transport]]

$$
  \exp(\omega) :  \mathbf{\Pi}(X) \to \exp(\mathfrak{g})
  \,.
$$

(...)

##### Differential coefficients {#DifferentialCoefficientsOfLieInt}

Above we have defined for every [[∞-Lie algebra]] $\mathfrak{g}$ a tower of $\infty$-Lie groupoids  $\tau_n \exp(\mathfrak{g})$ _integrating_ it. Now we consider the corresponding de Rham $\infty$-Lie groupoids $\mathbf{\flat}_{dR} \tau_n \exp(\mathfrak{g})$.

Recall that in the above examples we saw for $G$ a Lie $\infty$-group that the underlying discrete Lie $\infty$-groupoid $\mathbf{\flat} \mathbf{B}G$ is resolved by the presheaf $G TrivBund_{flat}$ of trivial $G$-principal $\infty$-bundles with flat connection. From this resolution the de Rham object $\mathbf{\flat}_{dR} \mathbf{B}G$ is obtained as an ordinary pullback of presheaves. These statements we now produce in the full generality of an $\infty$-Lie group obtained from the integration of an $L_\infty$-algebra.

First we produce a [[resolution]] of the underlying bare $\infty$-groupoid

$$
  \mathbf{\flat}\exp(\mathfrak{g}) : (U,[n]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(\Delta^n_{Diff}))
  \,.
$$

+-- {: .un_def }
###### Definition

Write $\exp(\mathfrak{g}) Bund_{flat}$ for the simplicial presheaf given by

$$
  \exp(\mathfrak{g})Bund_{flat}
  :
  (U,[n]) \mapsto
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(U \times \Delta^n_{Diff}))
  \,.
$$

=--

Here and in the following it is understood that diferential forms on a space that contains a $\Delta^n_{Diff}$ as a factor have _sitting instants_ : for every $k$ and every $k$-face of $\Delta^n_{Diff}$ there is a neighbourhood of the boundary of that face on which the form is constant in the direction perpendicular to that boundary.




+-- {: .un_lemma }
###### Lemma

The canonical morphism

$$
  \mathbf{\flat}\exp(\mathfrak{g})
  \to
  \exp(\mathfrak{g}) Bund_{flat}
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--


Below we use this to factor the inclusion $\mathbf{\flat} \exp(\mathfrak{g}) \to \exp(\mathfrak{g})$ as $  \mathbf{\flat}\exp(\mathfrak{g})
 \stackrel{\simeq}{\to} \exp(\mathfrak{g}) Bund_{flat} \to \exp(\mathfrak{g})$ with the last morphism being a fibration.

+-- {: .proof}
###### Proof

The morphism of simplicial presheaves is on each object $U$ the morphism of simplicial sets

$$
  \alpha(U)
  :
  Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet))
  \to
  Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet \times U))
$$

which is given degreewise by postcomposition with the morphisms of dg-algebras
$\Omega^\bullet(\Delta^n_{Diff}) \to \Omega^\bullet(\Delta^n_{Diff})\otimes \Omega^\bullet(U)$ that sends $\omega$ to $\omega \otimes 1$.

To show that for fixed $U$ this is a weak equivalence in the standard [[model structure on simplicial sets]] we produce objectwise a left inverse 

$$
  F_U
  :
  Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet \times U))
  \to
  Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet))
$$

and show that this is an acyclic fibration of simplicial sets. The statement then follows by 2-out-of-3.

We take $F_U$ to be given by evaluation at $0 \in U$, i.e. by postcomposition with the morphisms

$$
  \Omega^\bullet(\Delta^n \times U)
  \stackrel{Id \times 0^*}{\to}
  \Omega^\bullet(\Delta^n \times * )
  =
  \Omega^\bullet(\Delta^n)
  \,.
$$


Recall that the morphism $F_U$ will be an acyclic [[Kan fibration]] precisely if all diagrams of the form

$$  
  \array{
    \partial \Delta[n] &\to&
    Hom(CE(\mathfrak{g}), \Omega^\bullet(\Delta^\bullet \times U))
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

which is such a form $\omega$ is sent to a form which in a neighbourhood $(1-\epsilon,1]$ of $1 \in [0,1]$ is constant along $(1-\epsilon,1] \times U$ on the value $(0 \otimes Id_{S^{n-1}})^* \omega$. 

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

by smoothly identifying the union $[0,1] \times S^{n-1} \coprod_{S^{n-1}} D^n$ with another copy of $D^n$ to obtain in total a morphism

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(U \times D^n)
$$

with the desired properties.


=--

+-- {: .un_lemma }
###### Lemma

The canonical morphism

$$
  \exp(\mathfrak{g}) Bund_{flat}
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
     \Omega^{\bullet\geq 1,\bullet}(U \times \Delta^n_{Diff})
  )
  \,,
$$

where the notation on the right denotes the dg-algebra of differential forms on $U \times\Delta^n_{Diff}$ that (apart from having setting instants on the faces of $\Delta^n_{Diff}$) are along $U$ of non-vanishing degree.

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

###### For line $n$-groups {#LieIntDiffCoeffsForLineGroups}

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
  \int_{\Delta^k} :
  \mathbf{\flat}_{dR}^{simp} \mathbf{B}^n \mathbb{R}
  \to  
  \mathbf{\flat}_{dR}^{chn} \mathbf{B}^n \mathbb{R}
$$

that sends a closed $n$-form $\omega \in \Omega^n_{cl}(U \times \Delta^n)$ to its [[fiber integration]] $\int_{\Delta^k} \omega$.

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
     \omega \mapsto d_U \int_{\Delta^k} \omega
      &= 
      \int_{\Delta^k} d_U \omega
      \\
      & = - \int_{\Delta^k} d_{\Delta^k} \omega
      \\
      & = - \int_{\partial \Delta^k} \omega
  \end{aligned}
$$

using that $\omega$ is closed, so that $d_{dR} \omega = (d_U + d_{\Delta^k}) \omega = 0$.

Therefore we have indeed objectwise a chain map.

To see that it gives a weak equivalence we need to check that this chain map is a [[quasi-isomorphism]].

From the construction of both objects we know that they have the same cohomology, and that is concentrated in degree $n$, where it is $\Omega^1_{cl}(U)$. Therefore it is in fact sufficient to check that the integration map is onto in degree $n$. 

That amounts to observing that every 1-form $\alpha \in \Omega^1(U)$ may be obtained by integration of a closed $n$-form on $U \times \Delta^k$. This is clearly the case, for instance take $\frac{1}{c} \alpha \wedge d x^1 \wedge \cdots \wedge d x^{k} - \frac{1}{c} (d_U \alpha) \wedge x^1 \wedge d x^2 \wedge \cdots \wedge d x^k$.

=--




###### $\infty$-Chern-Weil homomorphism {#ChernWeilHomomorphism}

... under construction ...

..

The ordinary [[Chern-Weil homomorphism]] constructs [[curvature characteristic form]]s for $G$-[[principal bundle]]s from [[invariant polynomial]]s of [[Lie algebra]]s. The notion of [[invariant polynomial]] generalizes straightforwardly from Lie algebras to [[∞-Lie algebra]]s. We discuss a generalization of the Chern-Weil homomorphism for $\infty$-Lie groups in the image of the [[Lie integration]] map applied to an $\infty$-Lie algebra $\mathfrak{g}$.

We discuss how to construct for each $\infty$-Lie algebra $\mathfrak{g}$ with [[Lie integration]] $\mathbf{B}G := \tau_n \exp(\mathfrak{g})$ from each [[infinity-Lie algebra cohomology|∞-Lie n-cocycle]] $\mu : \mathfrak{g} \to b^{n-1} \mathbb{R}$ in transgression with an [[invariant polynomial]] $P$ a morphism

$$
  P : \mathbf{B}G \to \mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}/K
$$

that represents a class in the intrinsic de Rham cohomology 

$$
  P \in \mathbf{H}_{dR}(\mathbf{B}G, \mathbf{B}^n \mathbb{R})
  \,.
$$



+-- {: .un_defn}
###### Definition
**(differential resolution)**

For $\mathfrak{g}$ an [[∞-Lie algebra]] with [[Lie integration]] $\mathbf{B}G := \tau_n \exp(\mathfrak{g}) \in [CartSp^{op}, sSet]$, write $\mathbf{B}_{diff}G \in [CartSp^{op}, sSet]$ for the $n$-truncation of the [[simplicial presheaf]] given by

$$
  U,n \mapsto
  \left\{
    \array{
       C^\infty(U) \otimes' \Omega^\bullet(\Delta^n_{diff}) 
       &\leftarrow&
       CE(\mathfrak{g})
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U \times \Delta^n_{Diff})
       &\leftarrow&
       W(\mathfrak{g})
    }
  \right\} 
  \,.
$$ 

=--

+-- {: .un_prop}
###### Proposition

The evident projection

$$
  \mathbf{B}G \stackrel{\simeq}{\leftarrow}
  \mathbf{B}_{diff} G
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

The projection without the truncation is a weak equivalence
by the [[free construction|freeness]] of the [[Weil algebra]] $W(\mathfrak{g})$: morphisms of [[dg-algebra]]s $\Omega^\bullet(U \times \Delta^n) \leftarrow W(\mathfrak{g})$ are fixed by and uniquely corespond to their underlying morphisms of graded vector spaces $\Omega^(U \times \Delta^n) \leftarrow \wedge^1 \mathfrak{g}^*$. This implies that every diagram

$$
  \array{
    \partial\Delta[n] &\to& \mathbf{B}_{diff}G
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& \mathbf{B}G
  }
$$

has a lift over each $U \in CartSp$, hence that the morphism on the right is over each $U$ an aacyclic  [[Kan fibration]].

=--



Let $\mu : \mathfrak{g} \to b^{n-1} \mathbb{R}$ be an [[infinity-Lie algebra cohomology|∞-Lie algebra cocycle]] which is in transgression with an [[invariant polynomial]] $P$, where the transgression is induced from a Chern-Simons element $cs_P$. This data is a diagram

$$
  \array{
    \mathfrak{g} &\stackrel{\mu}{\to}& b^{n-1}\mathbb{R}
    &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    inn(\mathfrak{g}) &\stackrel{(cs_P, P)}{\to}& 
    inn(b^{n-1}\mathbb{R})
    &\stackrel{P}{\to}&
    b^{n}\mathbb{R}
  }
$$

of $\infty$-Lie algebras, or dually a [[dg-algebra]] diagram

$$
  \array{
    CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
    CE(b^{n-1}\mathbb{R})
    &\leftarrow&
    0
    \\
    \uparrow && \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{(cs_P,P)}{\leftarrow}&
    W(b^{n-1}\mathbb{R})
    &\leftarrow&
    CE(b^n \mathbb{R})
  }
  \,.
$$

This integrates to a morphism 

$$
    \hat \mathbf{B}_{diff}G \stackrel{\int \mu}{\to}
    \mathbf{B}_{diff}^{n} \mathbb{R}/K
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}/K
$$

where $\hat \mathbf{B}G \stackrel{\simeq}{\leftarrow} \mathbf{B}_{diff}G$
and $\mathbf{B}^n \mathbb{R}/K 
  \stackrel{\simeq}{\leftarrow} \mathbf{B}^n_{diff} \mathbb{R}/K$
are the [[resolution]]s.

The following proposition asserts that this definition does indeed capture the ordinary Chern-Weil homomorphism.

Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]], $G$ a [[Lie group]] and $P \to X$ a $G$-[[principal bundle]] classified by a morphisms $X \to \mathbf{B}G$ in $\infty LieGrpd$, hence a [[Cech cohomology|Cech cocycle]] given by a span

$$
  X \stackrel{\simeq}{\leftarrow}
  Y
  \to \mathbf{B}G
$$

in $[CartSp^{op}, sSet]_{proj}$.

Let $\langle \cdots \rangle$ be an $n$-ary [[invariant polynomial]] on $\mathfrak{g}$

+-- {: .un_prop}
###### Proposition

The composite

$$
  X \to \mathbf{B}G \to \mathbf{\flat}_{dR}\mathbf{B}^{2n} U(1)
$$

in $\infty LieGrpd$, i.e. the morphism given by a zig zag

$$
  X 
   \stackrel{\simeq}{\leftarrow}
  Y 
   \stackrel{}{\to}
  \mathbf{B}G
   \stackrel{\simeq}{\leftarrow}
  \mathbf{B}_{diff}G
  \to
  \mathbf{\flat}_{dR}\mathbf{B}^{2n} U(1)  
$$

in $[CartSp^{op}, sSet]_{proj,cov}$ represents the [[de Rham cohomology]] class of the [[curvature characteristic form]]

$$
  [\langle F_\nabla \wedge \cdots \wedge F_\nabla\rangle]
  \in
  H^{2n}(X)
$$

of any [[connection on a bundle|connection]] $\nabla$ on $P$.


=---

+-- {: .proof}
###### Proof

... sketch, am being interrupted ...

By possibly refining the cover $Y$, we may lift the given cocycle $\mathbf{B}G$-cocycle to a $\mathbf{B}_{diff}G$ cocycle which on patches $U_i$ assigns the local curvature forms $A_i$ of $\nabla$.

To a double intersection this cocycle assigns a based path $\gamma_{i j}$ in $G$ with endpoint $g_{i j}$. By the discussion at [[Chern-Simons form]] we find that the corresponding image of $\langle ... \rangle$ is the Chern-Simons form $CS(A_i,A_j)$ for this path of gauge transformations. Since $A_i$ and $A_j$ are components of a genuine connection (which always exsist), this form is closed. 

Similarly for higher paths. It follows that the cocycle in $\mathbf{\flat}_{dR} \mathbf{B}^{2n }U(1) = (\Omega^1(-) \stackrel{d_{dR}}{\to}\cdots \stackrel{d_{dR}}{\to}\Omega^{2n}_{closed}(-))$ that we obtain looks like

$$
  (\langle F_{A_i} \wedge \cdots \wedge F_{A_i}\rangle, CS(A_i,A_j), \lambda_{i j k}, \cdots)
  \,.
$$

Using a [[partition of unity]] this is coboundant to a cocycle of the form

$$
  (\langle F_{A_i} \wedge \cdots \wedge F_{A_i}\rangle + d something,0, 0, \cdots)
  \,.
$$

This represents a globally defined form which differs from $\langle F_{\nabla}\wedge \cdots F_\nabla\rangle$ by an exact form.

 
=--

#### Simplicial manifolds / simplicial diffeological space

Every smooth [[simplicial manifold]], and more generally every [[simplicial object]] in [[diffeological space]]s, naturally represents a [[simplicial presheaf]] $X_\bullet \in [CartSp^{op}, sSet]$, and as such naturally represents an $\infty$-Lie groupoid.


##### Simplicial de Rham complex {#DeRhamOfSimplicialManifold}

For $X_\bullet$ a [[simplicial manifold]], there are two main models for the [[simplicial de Rham complex]] of $X$.

1. the [[total complex]] of the [[double complex]] $\Omega^\bullet(X_\bullet)$;

1. The complex whose elements in degree $n$ are collections
   
   $$
     \{\omega_p \in \Omega^n(X_p \times \Delta^p)\}_{p = 0}^\infty
   $$

   subject to the conditions

   $$
     (id \times (\Delta^{p-1} \stackrel{\sigma_i}{\to} \Delta^p))^*
     \omega_p
     =
     ((X_p \stackrel{\delta_i}{\to} X_{p-1}) \times id)^* \omega_{p-1}
   $$

   for all $p,i$, and whose differential is degreewise the ordinary
   de Rham differential.


There is a [[quasi-isomorphism]] from the latter to the former, given by the [[fiber integration]] of forms over simplices.

[Above](#LieIntDiffCoeffsForLineGroups) we had obtained two different simplicial presheaves representing the intrinsic de Rham coefficient object $\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}$, which we denoted $\mathbf{\flat}_{dR}^{simp}\mathbf{B}^n \mathbb{R}$ and $\mathbf{\flat}_{dR}^{chn}\mathbf{B}^n \mathbb{R}$, and a weak equivalence

$$
  \int \; : \; \mathbf{\flat}_{dR}^{simp}\mathbf{B}^n \mathbb{R}
   \to 
    \mathbf{\flat}_{dR}^{chn}\mathbf{B}^n \mathbb{R}
  \,.
$$


We want to claim now that 

1. the cocycle $\infty$-groupoids of the two simplicial de Rham complexes are the hom-complexes

   $$
     [CartSp^{op}, sSet](X_\bullet, \mathbf{\flat}_{dR}^{simp}\mathbf{B}^n \mathbb{R})
   $$

   and

   $$
     [CartSp^{op}, sSet](X_\bullet, \mathbf{\flat}_{dR}^{chn}\mathbf{B}^n \mathbb{R})
     \,,
   $$

   respectively;

1. the quasi-isomorphism relating them is the morphism induced by the weak equivalence of these coeffient objects

   $$
     [CartSp^{op}, sSet](X_\bullet, \int )
     : 
     [CartSp^{op}, sSet](X_\bullet, 
     \mathbf{\flat}_{dR}^{simp}, \mathbf{B}^n \mathbb{R})
     \to
     [CartSp^{op}, sSet](X_\bullet, \mathbf{\flat}_{dR}^{chn}, \mathbf{B}^n \mathbb{R})
     \,.
   $$

To see this, notice for instance for the second version of the simplicial de Rham complex that its $n$-cocycles $\{\omega_p \in \Omega_{cl}^n(X_p \times \Delta^p)\}$,  are diagrams of sheaves on $CartSp$ of the form

$$
  \array{
    \vdots && \vdots
    \\
    X_2 &\stackrel{\omega_2}{\to}& \Omega^n_{cl}(- \times \Delta^2)
    \\
    \downarrow \downarrow \downarrow && 
     \downarrow \downarrow \downarrow
    \\
    X_1 &\stackrel{\omega_1}{\to}& \Omega^n_{cl}(- \times \Delta^1)
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    X_0 &\stackrel{\omega_0}{\to}& \Omega^n_{cl}(-)
  }
  \,.
$$

But these are exactly the [[coend]] diagrams that encode the morphisms of simplicial presheaves $\omega : X_\bullet \to \mathbf{\flat}_{dR}^{simp} \mathbf{B}^n \mathbb{R}$.

(...)



#### Simplicial Lie and diffeological groups {#SimplicialSmoothGroups}

Every [[connected]] object $X \in \infty Lie Grpd$ is -- by definition -- the [[delooping]] $X = \mathbf{B}G$ of a Lie [[∞-group]] $G = \Omega X$, its [[loop space object]] formed in $\infty LieGrpd$. Since the discussion of [[group object in an (infinity,1)-category|group objects]], [[loop space  object]]s etc. involves only finite [[limit in a quasi-category|(∞,1)-limits]] and [[∞-stackification]] preserves these, this may be discussed in the [[(∞,1)-category of (∞,1)-presheaves]] on [[CartSp]]. Since there $(\infty,1)$-limits are computed objectwise, an [[∞-group]] object $G$ in $\infty LieGrpd$ is modeled by a [[(∞,1)-presheaf]] with values in [[∞-group]]s in [[∞Grpd]].

By standard results on <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity,1)-category#ModelsInInfGrpd">Models for group objects in ∞Grpd</a> the latter may equivalently be modeled by [[simplicial group]]s. A simplicial group is possibly weak [[∞-groupoid]] equipped with a _strict_ group object structure. While [[strict omega-groupoid|strict ∞-groupoids]] with weak group object structure do not model all [[∞-group]]s, weak $\infty$-groupoids with strict group structure do.

There is a good supply of standard results for and constructions with [[simplicial group]]s which makes this model useful for applications.

##### Delooping

For the moment see [simplicial group - delooping](http://ncatlab.org/nlab/show/simplicial+group#Delooping).

##### Simplicial principal bundles

For the moment see the discussion about geometric realization further above.




### Cohomology {#Cohomology}

As every [[(∞,1)-topos]], $\mathbf{H} = Sh_{(\infty,1)}(CartSp)$ comes with its [[cohomology|intrinsic cohomology]].


#### With constant coefficients

We discus the [[cohomology|intrinsic cohomology]] of $\mathbf{H}$ with _constant_ coefficients, i.e. coefficients that are [[constant (∞,1)-sheaf|constant (∞,1)-sheaves]] on [[CartSp]].

+-- {: .un_theorem }
###### Theorem

Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]] and $A \in $ [[∞Grpd]]. Then we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  Sh_{(\infty,1)}(CartSp)(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   Sh_{(\infty,1)}(CartSp)(X, LConst A)
$$

=--

+-- {: .proof}
###### Proof

The key point is that for paracompact $X$, the [[nerve theorem]] asserts that $\Pi(X)$ is [[weak homotopy equivalence|weak homotopy equivalent]] to $Sing X$, the standard [[fundamental ∞-groupoid]] of $X$. This is discussed in detail in the section <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal">geometric realization</a> at [[schreiber:path ∞-groupoid]].

Using this, the statement follows by the [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(\Pi \dashv LConst)$, that is discussed in detail at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#Unstruc">Unstructured homotopy ∞-groupoid</a>.

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

This is definition 1.1 in 

* [[Jean-Luc Brylinski]], _Differentiable cohomology of gauge groups_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf)).

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




#### Intrinsic De Rham cohomology of $B^n U(1)$ {#DeRhamBnU(1)}



+-- {: .un_prop }
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
    \mathbf{H}(\Sigma \mathbf{B}^n U(1), \Omega \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
    \\
    & \simeq
    \mathbf{H}(\mathbf{B}^{n+1} U(1), \Omega \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
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





#### Flat nonabelian cohomology

For $G$ a Lie $n$-group, 
recall the expression for the fibrant representat&#238;ve of
$\mathbf{\flat}\mathbf{B}^n G$ from above.

+-- {: .un_corollary}
###### Corollary

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]],
we have that

$$
  H(X, \mathbf{\flat} \mathbf{B} G )
  \simeq
  \hat H^1_{flat}(X,G)
  \simeq
  \pi_0 G Bund_{flat}(X)
$$

is the flat [[nonabelian cohomology]] of $X$ with coefficients in $G$.

=--

#### Differential cohomology with coefficients in $B^n U(1)$

See [[circle n-bundle with connection]].

### Smooth Whitehead towers {#SmoothWhitehead}

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


##### Second fractional Pontryagin class

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

[[fivebrane 6-group]]





## The infinitesimally thickened $(\infty,1)$-topos $\infty$-Lie groupoids and $\infty$-Lie algebroids {#InfSheavesOnCartSp}

If we pass from the [[site]] [[CartSp]] to the site [[ThCartSp]] of [[infinitesimal object|infinitesimally thickened]] [[Cartesian space]]s, then the objects in the corresponding $(\infty,1)$-topos are $\infty$-Lie groupoids whose spaces of $k$-morphisms may have [[nLab:infinitesimal object|infinitesimal extension]]. This then also inclused [[∞-Lie algebroid]]s.

**Definition**

Write

$$
  \infty SDLieGrpd := Sh_{(\infty,1)}(ThCartSp)
  \,.
$$

This is the $(\infty,1)$-[[Cahiers topos]].



(...)

### Relative $\infty$-connectedness



+-- {: .un_prop}
###### Proposition


$\infty SDLieGrpd$ is an <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#InfinitesimalExtension">infinitesimal thickening of the (∞,1)-topos</a> $\infty LieGrpd$: the morphism of [[site]]s

$$
  CartSp \stackrel{\overset{}{\leftarrow}}{\hookrightarrow}
  ThCartSp
$$

is a [[reflective subcategory|coreflective embedding]] and induces an $\infty$-[[connected geometric morphism]]

$$
  \infty SDLieGrpd
  \stackrel{\overset{\Pi_{inf}}{\to}}{\stackrel{\overset{LConst_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\to}}}
  \infty LieGrpd
  \,.
$$

=--

This induces the following infinitesimal analogs of the structures discussed above for $\infty LieGrpd$


+-- {: .un_def}
###### Definition

Write

$$
  (\mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})
  :=
  (LConst_{inf} \circ \Pi_{inf} \dashv LConst_{inf} \circ \Gamma_{inf})
  :
  \infty SDLieGrpd
  \stackrel{\leftarrow}{\to}
  \infty SDGrpd
$$

for the composite [[adjunction]]. For $X,A \in \infty SDGrpd$ we call $\mathbf{\Pi}$ the **Lie [[schreiber:path ∞-groupoid|infinitesimal homotopy ∞-groupoid]]** of $X$ and we call $\mathbf{\flat}A$ the **infinitesimally flat $\infty$-Lie groupoid** of $A$.

For $X \in \infty Grpd$ we write $\mathbf{\Pi}_{inf,dR}(X)$ for the [[homotopy cofiber]] of the unit $X \to \mathbf{\Pi}_{inf}(X)$, i.e. for the [[pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{\Pi}_{inf}(X) &\to& \mathbf{\Pi}_{inf,dR}(X)
  }
$$

in $\infty SDGrpd$.

For $* \to A \in \infty SDGrpd$ a [[pointed object]], we write $\mathbf{\flat}_{inf,dR} A$ for the [[homotopy fiber]] of the counit $\mathbf{\flat}_{inf} A \to A$, i.e. for the [[pullback]]

$$
  \array{
    \mathbf{\flat}_{inf,dR}A &\to& \mathbf{\flat}_{inf} A
    \\
    \downarrow &\swArrow& \downarrow
    \\
    * &\to& A
  }
$$

in $\infty Grpd$\,.

=--



## Examples

### Infinitesimal

* [[∞-Lie algebroid]]

* [[Lie algebra]]

* [[Lie algebroid]]

  * [[tangent Lie algebroid]]

  * [[Atiyah Lie algebroid]]

* [[Lie 2-algebra]]

  * [[string Lie 2-algebra]]

* [[n-symplectic manifold]]

  * [[Poisson Lie algebroid]]

  * [[Courant algebroid]]


### Non-infinitesimal

* [[Lie group]]

* [[Lie groupoid]], [[differentiable stack]]

  * [[Atiyah Lie groupoid]]

  * [[path groupoid]]

* [[Lie 2-group]]

* Lie [[∞-group]]

  * [[string 2-group]]

    For $\mathfrak{g}$ a [[semisimple Lie algebra]], 
    $\mu \in CE(\mathfrak{g})$ the normalized 
    [[Lie algebra cohomology|Lie algebra 3-cocycle]] and 
    $\mathfrak{g}_{\mu}$ the corresponding [[string Lie 2-algebra]], 
    the **[[string 2-group]]** is

    $$
      \mathbf{B}String(G) := \tau_1 \exp(\mathfrak{g}_\mu)
      \,.
    $$    

    It has a model by a 
    [[paracompact space|paracompact]] [[diffeological space|diffeological]]
    [[strict 2-group]] $[\hat \Omega G \to P G]$.

  * [[fivebrane 6-group]]

* [[schreiber:path ∞-groupoid]]

## References

> ... to be done ... not even close to a beginning of anything comprehensive ...

For more references see 

* [[Lie theory]], [[Lie integration]] etc. 

Some useful notes on the topic of $\infty$-stacks on the site [[Diff]] is in the (unfinished but noteworthy) notes

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

However, there the emphasis is on the [[localization of an (infinity,1)-category|localization]] to those $\infty$-stacks that are in fact homotopy invariant and hence collapse to discrete $\infty$-groupoids. See also [[topological ∞-groupoid]].


The proposal for descent objects for strict $\infty$-groupoid-valued presheaves discussed in [Descent for strict infinity-groupoids](#DescentForStrictInf) appeared in 

* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math/0303175)) {#Street03}

The relation to the general descent condition is discussed in

* [[Dominic Verity]], _[[Verity on descent for strict omega-groupoid valued presheaves|Relating descent notions]]_ {#Verity}






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
