

<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
***
[[!include (infinity,1)-topos - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **$\infty$-Lie groupoid** is the generalization of the notion of [[Lie group]] and [[Lie groupoid]] from [[category theory]] to [[higher category theory]] and [[homotopy theory]]:

an $\infty$-Lie groupoid is an [[∞-groupoid]] that is _smooth_ in some sense.

One way to realize this is to pick a [[site]] $C$ of smooth test spaces -- such as [[CartSp]] or [[Diff]] -- and take a smooth $\infty$-groupoid $A$ to be an [[∞-stack]]/[[(∞,1)-sheaf]] $A : C^{op} \to $ [[∞Grpd]] on this site. 

* Evalutaed on the [[point]] $* \in C$ this encodes an ordinary [[∞-groupoid]] $A(*) \in \infty Grpd$, which is the underlying $\infty$-groupoid of our smooth $\infty$-groupoid.

* Evaluated on an object $U \in C$ this encodes an $\infty$-groupoid $A(U)$ that is to be thought of as the $\infty$-groupoid of _smooth families paramterized by $U$_ of [[object]]s, [[morphism]]s, ... [[k-morphism]]s in $A(*)$.

This way of encoding smooth structure is entirely analogous to, and in fact a generalization of, the way a [[diffeological space]] is encoded as a [[sheaf]] on [[CartSp]]. 

Accordingly, the generic [[∞-stack]] on [[CartSp]] or [[Diff]] is a smooth $\infty$-groupoid that may be a more general object than one may want to call an "$\infty$-Lie groupoid". The latter term one may want to reserve for special such stacks -- for [[geometric stack]]s and their $\infty$-categorical analogs.

Notice that for the definition of the smooth structure on a [[diffeological space]] or on an ordinary [[Lie groupoid]] it is not in fact necessary to regard these as objects tested by objects in all of [[Diff]]: since smoothness is a local property, it is entirely sufficient to know around every point in the set of [[k-morphism]]s of the $\infty$-groupoid is, what all the extensions of this point to a _ball_ -shaped smooth family of points around that point are. This is precisely what an [[∞-stack]] on [[CartSp]] encodes. See the discussion below for the difference between $\infty$-stacks on [[CartSp]] and on [[Diff]].

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

For $X \in \infty Grpd$ we write $\mathbf{\Pi}_{dR}(X)$ for the [[homotopy cofiber]] of the unit $X \to \mathbf{\Pi}(X)$, i.e. for the [[pushout]]

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

+-- {: .proof}
###### Proof

The [[(∞,1)-functor]] $\Pi : \infty LieGrpd \to \infty Grpd$ is the left [[derived functor]] of $\lim_\to : [CartSp^{op}, sSet]_{proj,cov} \to sSet_{Quillen}$. Use the above cofibrant replacement for $X$ degreewise with Dugger's general description of [projective cofibrant objects](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantReplacement) in $[CartSp^{op}, sSet]$ to compute the cofibrant replacement, then apply $\lim_\to$ and use that the [[colimit]] of a [[representable functor|representable]] is the point. The statement then is degreewise the classical [[nerve theorem]].

A detailed proof can be found at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#Unstruc">path ∞-groupoid -- Unstructured homotopy ∞-groupoid</a>.

=--


### Geometric realization

+-- {: .un_prop}
###### Proposition

Let $X$ be a [[simplicial manifold]] that is degreewise [[paracompact space|paracompact]], regarded as a [[simplicial object|simplicial]]
[[diffeological space]], hence as an object in $[CartSp^{op}, sSet]$,
hence as an object in $\infty LieGrpd$.

Write $|X| \in $ [[Top]] for the [[geometric realization]] of the underlying [[simplicial object|simplicial]] [[topological space]]. Then

$$
  \Pi(X) \simeq |X| \in Top \simeq \infty Grpd
  \,.
$$

=--

+-- {: .proof}
###### Proof

A proof is given at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal">path oo-groupoid -- Geometric realization </a>

=--

+-- {: .un_prop}
###### Proposition

Let $G$ be a [[well sectioned simplicial topological group]]. Write, as usual for [[simplicial group]]s, $\mathbf{B}G := \bar W G$ for its <a href="http://ncatlab.org/nlab/show/simplicial+group#Delooping">delooping</a>.

Regard $\mathbf{B}G$ in the canonical way as an object of $[CartSp,sSet]$.
Let $X_\bullet \in [CartSp^{op}, sSet]$ be any other simplicial topological space and let $X \to \mathbf{B}G$ be a morphism. Then:

on such morphisms [[geometric realization]] $X_\bullet \mapsto |X_\bullet| \int^{[n]} \Delta^n_{Top} \times X_n \in Top$ preserves [[homotopy fiber]]s up to weak equivalence.


=--

+-- {: .proof}
###### Proof

In unpublished notes, [[Danny Stevenson]] and [[David Roberts]] show that under [[geometric realization]] the <a href="http://ncatlab.org/nlab/show/simplicial+group#UniversalBundle">universal simplicial principal bundle</a>
$\mathbf{E}G := W G \to \bar W G$ maps to the universal $|G|$-[[principal bundle]] $\mathcal{E} |G| \to \mathcal{B}|G|$ in [[Top]].

But (as described at [[homotopy fiber]] and [[generalized universal bundle]]) the universal bundle is a means to compute homotopy fibers:

the ordinary [[pullback]]

$$
  \array{
    P_\bullet &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X_\bullet &\to& \bar W G
  }
$$

computes the homotopy fiber of $X_\bullet \to \bar W G$. Since geometric realization preserves [[pullback]]s, this is sent to the pullback square

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

> may need to polish the technical assumopptions...


### Relation to $(\infty,1)$-sheaves on all manifolds

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


Many $\infty$-Lie groupoids appearing in practice are (equivalent) to objects in [[sub-(∞,1)-categories]] of $Sh_{(\infty,1)}(CartSp)$ of much stricter $\infty$-Lie groupoids. These subcategories typically offer convenient and desireable contexts for formulating and proving statements about special cases of general $\infty$-Lie groupoid.  Therefore it is of interest to have various notions of _strict_ $\infty$-Lie groupoids inside all of them.

One well-known such notion is given by the [[Dold-Kan correspondence]]. This identifies [[chain complex]]es of [[abelian group]]s with strict and strictly [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] $\infty$-groupoids.

Dropping the condition on symmetric monoidalness we obtain a more general such inclusion, a kind of non-abelian Dold-Kan correspondence: 

the identification of [[crossed complex]]es of groupoids as precisely the [[strict omega-groupoid|strict ∞-groupoid]]s. This has been studied in particular in [[nonabelian algebraic topology]].

So we have a sequence of inclusions

$$
  sAb
  \simeq
  Ch_\bullet(Ab)^+
  \hookrightarrow
  CrsdCplx
  \simeq Str \omega Grpd
  \stackrel{N}{\hookrightarrow}
  KanCplx
  \simeq
  \infty Grpd
$$

of strict $\infty$-groupoids into all $\infty$-groupoids.

Among the special tools for handling $\infty$-stacks on $CartSp$ that factor at some point through the above inclusion are the following.

* **restriction to abelian sheaf cohomology** -- Using the fact that the objects of $Sh_{(\infty,1)}(CartSp)$ are modeled by [[simplicial presheaves]] symmetric monoidal $\infty$-Lie groupoids are identified under the [[nLab:Dold-Kan correspondence]] with $\mathbb{N}$-graded [[nLab:chain complex|chain complexes]] of sheaves. To these the rich set of tools for [[abelian sheaf cohomology]] apply. 

* **descent for strict $\infty$-groupoid valued sheaves** -- There is a good theory pf [[descent]] for (presheaves) with values in strict $\infty$-groupoids (more restrictive than the fully general theory but more general than [[abelian sheaf cohomology]]). This goes back to [[nLab:Ross Street|Ross Street]] and its relation to the full theory has been clarified by [[Dominic Verity]]. This is described at 

* [[Verity on descent for strict omega-groupoid valued presheaves]].   


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

Write $N^\bullet(C^\bullet\bullet(\Delta[n]))$ for the [[Moore complex|normalized chain complex]] of the [[cochain on a simplicial set|cochains on the simplicial set]] given by the $n$-[[simplex]] $\Delta[n]$. Write also $^CE(b^n \mathbb{R})$ for the [[Chevalley-Eilenberg algebra]]
of the [[L-∞-algebra]] $b^^n \mathbb{R}$, which is the [[dg-algebra]] on a single generator in degree $n$ with vanishing differential.

With this notation we can express the flat de Rham object of $\mathbf{B}^n U(1)$
as a hom-object of [[∞-Lie algebroid]]s:

$$
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
  :
  V \mapsto
  \infty LieAlg( T V, b^n \mathbb{R})
  :=
  Hom_{dgAlg}( CE(b^n \mathbb{R}) , 
   \Omega^\bullet(U)\otimes N^\bullet(C^\bullet(\Delta[\bullet])) )
  \,.
$$

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
  \,.
$$

See also the discussion at [[generalized universal bundle]].

=--



##### Differential coefficients

We give a concrete representative for the $\infty$-Lie groupoid $\mathbf{\flat} \mathbf{B}G = LConst \Gamma \mathbf{B}G$ in terms of [[Lie algebra]]-valued [[differential form]]s.


Let $\Xi : CrsdCplx \to sSet$ now denote the inclusion of [[crossed complex]]es into all [[∞-groupoid]]s. 

+-- {: .un_prop }
###### Proposition

The object $\infty$-Lie groupoid $\mathbf{\flat}\mathbf{B}G \in \infty LieGrpd$ has a fibrant representative in $[CartSp^{op}, sSet]_{proj,cov}$ given by

$$
  \mathbf{\flat}\mathbf{B}G 
  =
  \Xi[C^\infty(-,G)\times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1 d p_1^{-1}}{\to}}{\underset{p_2}{\to}} \Omega^1_{flat}(-,\mathfrak{g})]
  \,,
$$

where $\mathfrak{g}$ is the [[nLab:Lie algebra]] of $G$. 

This is the [[groupoid of Lie-algebra valued forms]] restricted to flat forms.

=--

In other words, $U = \mathbb{R}^n$-parameterized family of objects of $\mathbf{\flat}\mathbf{B}G$ is given by an element $A \in \Omega^1(U)\otimes \mathfrak{g}$^such that $d_{dR} A + [A ,\wedge A]  = 0$, and a $U$-parameterized family of morphisms $g : A \to A'$ is given by a smooth function $f \in C^\infty(U,G)$ such that $A' = Ad_g A + g d g^{-1}$.

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

Finally we need to show that $N( G \times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{\to}{\to} \Omega^1_{flat}(-,\mathfrak{g}))$ is fibrant in $[CartSp^{op}, sSet]_{proj,cov}$. This can be seen by observing that this sheaf is the coefficient object that in [[Cech cohomology]] computes $G$-[[principal bundle]]s with flat [[connection on a bundle|connection]] and then reasoning as above: every $G$-principal bundle with flat connection is equivalent to a trivial $G$-principal bundle whose connection is given by a globally defined $\mathfrak{g}$-valued 1-form. Morphisms between these are precisely $G$-valued functions that act on the 1-forms by gauge transf&#244;rmations as in the [[groupoid of Lie-algebra valued forms]].

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


#### Strict Lie 2-groups {#StrictLie2Groups}

Let now $G = \Xi[G_2 \to G_1]$ be a strict [[Lie 2-group]] coming from a smooth  [[crossed module]] $G_2 \to G_1 \to Aut(G_2)$.

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

As above.

=--


##### Differential coefficients

Write $[\mathfrak{g}_2 \stackrel{\delta}{\to} \mathfrak{g}_1]$ for the [[differential crossed module]] corresponding to the Lie [[strict 2-group]] $(G_2 \to G_1)$, regarded as an [[L-∞-algebra]]. Write $CE(\mathfrak{g}_2 \to \mathfrak{g}_1)$ for the corresponding [[Chevalley-Eilenberg algebra]].


+-- {: .un_prop }
###### Proposition

The $\infty$-Lie groupoid $\mathbf{\flat}_{dR} \mathbf{B}[G_2 \to G_1]$ is represented in $[CartSp^{op}, sSet]$ by

$$
    V \mapsto 
    Hom_{dgAlg}(CE(\mathfrak{g}_2 \to \mathfrak{g}_1), 
    \Omega^{\bullet \geq 1}(V)\otimes N^\bullet(C^\bullet(\Delta[\bullet])))
  \,.
$$

=--


+-- {: .proof}
###### Proof

In analogy to the above computations we resolve

$$
  \mathbf{\flat} \mathbf{B}[G_2 \to G_1]
  \simeq
  \Xi[
    const G_2 \to const G_1 \stackrel{\to}{\to} *
  ]
$$

by applying a non-commutative version of the [[Poincare lemma]]-reasoning to find

$$
  \cdots \simeq
  \Xi[
    C^\infty(-,G_2)
    \stackrel{}{\to}
    \Omega^\bullet_{\flat}(-,\mathfrak{g}_2 \to \mathfrak{g}_1)
    \times
    C^\infty(-, G_1) \times \Omega^1(-, \mathfrak{g}_2)
    \stackrel{\overset{}{\to}}{\underset{p_1}{\to}}
    \Omega^\bullet_{\flat}(-,\mathfrak{g}_2 \to \mathfrak{g}_1)
  ]
  \,.
$$

This is the 2-groupoid of flat Lie 2-algebra valued forms as described in 
[SchrWalII](http://arxiv.org/abs/0802.0663).

With this the [[homotopy pullback]] defining $\mathbf{\flat}_{dR} \mathbf{B}[G_2 \to G_1]$ is the ordinary pullback in $[CartSp^{op}, sSet]$,
which yields the stated result.

=--

### General $\infty$-Lie groupoids


#### Simplicial Lie and diffeological groups {#SimplicialSmoothGroups}

Every [[connected]] object $X \in \infty Lie Grpd$ is -- by definition -- the [[delooping]] $X = \mathbf{B}G$ of a Lie [[∞-group]] $G = \Omega X$, its [[loop space object]] formed in $\infty LieGrpd$. Since the discussion of [[group object in an (infinity,1)-category|group objects]], [[loop space  object]]s etc. involves only finite [[limit in a quasi-category|(∞,1)-limits]] and [[∞-stackification]] preserves these, this may be discussed in the [[(∞,1)-category of (∞,1)-presheaves]] on [[CartSp]]. Since there $(\infty,1)$-limits are computed objectwise, an [[∞-group]] object $G$ in $\infty LieGrpd$ is modeled by a [[(∞,1)-presheaf]] with values in [[∞-group]]s in [[∞Grpd]].

By standard results on <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity,1)-category#ModelsInInfGrpd">Models for group objects in ∞Grpd</a> the latter may equivalently be modeled by [[simplicial group]]s. A simplicial group is possibly weak [[∞-groupoid]] equipped with a _strict_ group object structure. While [[strict omega-groupoid|strict ∞-groupoids]] with weak group object structure do not model all [[∞-group]]s, weak $\infty$-groupoids with strict group structure do.

There is a good supply of standard results for and constructions with [[simplicial group]]s which makes this model useful for applications.

##### Delooping

For the moment see [simplicial group - delooping](http://ncatlab.org/nlab/show/simplicial+group#Delooping).

##### Simplicial principal bundles

For the moment see the discussion about geometric realization further above.


#### Lie-integrated $\infty$-Lie groupoids {#LieIntegrated}

> under construction

+-- {: .un_def }
###### Definition
**(forms on the simplex)**

Write $\Delta_{Diff} : \Delta \to CartSp \hookrightarrow sPSh(CartSp)$ for the cosimplicial object induced from the standard [[nLab:interval object]] $* \stackrel{0}{\to} \mathbb{R} \stackrel{1}{\leftarrow} 1$ in [[CartSp]], i.e. the object of standard smooth simplices.

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

There however only this bare $infty$-groupoid underlying the $\infty$-Lie groupoid $\exp(\mathfrak{a})$ is explicitly considered, the focus of the article being on the construction of small equivalent models.

A refinement of this construction to [[internal ∞-groupoid]]s in [[nLab:Banach space]]s was considered in 

* [[Andre Henriques]], _Integrating $L_\infty$-algebras_ ([arXiv])

The evident refinement of the [[Sullivan construction]] to $\infty$-Lie groupoids as considered here, parameterized over smooth test spaces, was mentioned around

* [[Urs Schreiber|U.S.]], _Differential nonabelian cohomology_ talk at _Higher Structures in Math and Physics_ Lausanne (2008) ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Lausanne.pdf))

and was considered around the same times also by [[Dmitry Roytenberg]]. 

In 

* [[Pavol Severa]], _..._ 

is given a proposal for how to realize Lie differentiation in this context. Below we will see that, in analogy to and generalizing the above examples, the Lie differentiation of $\tau_n \exp(\mathfrak{g})$ is canonically induced by passing to its intrinsic de Rham coefficient object $\mathbf{\flat}_{dR} \tau_n \exp(\mathfrak{a})$. Below in 
[Infinitesimal differential coefficients](#InfinitesimalDifferentialCoefficients) we discuss how these are realized in terms of infinitesimal paths in the $\infty$-Lie groupoid. This is at least in spirit close to &Scaron;evera's construction. A more detailed discussion of the relation should be given somewhere, eventually.


=--



##### Examples

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


###### Integration of $b^n \mathbb{R}$

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

The key fact underlying this is that Aa closed smooth $n$-form on the $n$-sphere may be extended smoothly to a closed $n$-form on the $(n+1)$-ball precisely if its integral over the sphere vanishes. 

From this it follows that also every closed $n$-form on the $k$-sphere for $k \gt n$ may be extended as a closed $n$-form to the $(n+1)$-ball. The same holds for smooth families of forms. This implies that $\exp(b^n \mathbb{R}) \to \mathbf{B}^n \mathbb{R}$ is an acyclic fibration for all $n$.

=--






##### Differential coefficients

Above we have defined for every [[L-∞-algebra]] $\mathfrak{g}$ a tower of $\infty$-Lie groupoids  $\tau_n \exp(\mathfrak{g})$ _integrating_ it. Now we consider the corresponding de Rham $\infty$-Lie groupoids $\mathbf{\flat}_{dR} \tau_n \exp(\mathfrak{g})$.

First we produce a resolution of the underlying bare $\infty$-groupoid

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


The idea of the proof is that the lifts in question are obtained from solving differential equations with boundary conditions, and exist due to the existence of these solutions. Since the idea is simple but the system of differential equations can be big and involved, we write out the construction in simple cases and trust that the generalization is evident.

To warm up, consider the case where $\mathfrak{g} = b^n \mathfrak{u}(1)$, i.e. where $CE(\mathfrak{g})$ is given by a single generator in degree $n+1$ and vanishing differential. First $n = 0$.

Then a morphism $C(\mathfrak{g}) \to \Omega^\bullet(D^1 \times U \times [0,1]) \otimes C^\infty(U)$ is an element $A_v(u) d v + A_\sigma(u) d \sigma + A_{v \sigma}(u) d v \wedge d \sigma $ that satisfies

$$
  \partial_v A_u = \partial_u A_v
$$

and 

$$
  \partial_\sigma A_v = \partial_v A_\sigma
  \,.
$$

To lift this to a morphism $CE(\mathfrak{g}) \to \Omega^\bullet(D^1 \times U \times [0,1])$ that restricts to the former for $\sigma = 0$ we need to add a term $A_u(u,\sigma) d u$. This needs to satisfy the differential equation

$$
  \partial_\sigma A_u = \partial_u A_\sigma
  \,.
$$

For the given initial value at $\sigma = 0$ this has a unique solution and defines $A_u$ on all of $[0,1]$.

For this to be a consistent solution it must also be true that

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

For a general Lie algebra $\mathfrak{g}$ with dual basis $\{t^a\}$ and structue constants $C^a{}_{b c}$ we get the analogous discussion with structure constant terms thrown in:

the original element is a collection of 1-forms $A^a_v(u) d v + A^a_\sigma(u) d \sigma $ satisfying

$$
  \partial_\sigma A_v^a = \partial_v A_\sigma + C^a{}_{b c} A_\sigma^b \wedge A_v^c
  \,.
$$

We lift by adding a term $A_u^a d u$ that solves the differential equation

$$
  \partial_\sigma A_u = \partial_u A_\sigma + C^a{}_{b c} A_\sigma^b \wedge A_u^c
  \,.
$$

Again, for the given boundary condition at $\sigma = 0$ this has a unique solution. And since the boundary lift at $\sigma = 0$ satisfies

$$
  \partial_v A_u(\sigma = 0) = \partial_u A_v(\sigma = 0)
  + C^a{}_{b c} A_v^b(\sigma = 0) \wedge A_u^c(\sigma = 0)
$$

it is sufficient to check that we have equality of derivatives

$$
  \partial_\sigma \partial_v A_u 
  = \partial_\sigma \partial_u A_v
  + 
  C^a{}_{b c} \partial_\sigma A_v^b 
  \wedge A_u^c
  +
  C^a{}_{b c} A_v^b 
  \wedge \partial_\sigma A_u^c
  \,.
$$

The left hand is

$$
  \partial_v \partial_\sigma A_u = 
  \partial_v \partial_u A_\sigma 
  + 
  \partial_v(
  C^a{}_{b c} A_\sigma^b \wedge A_u^c)
$$

whereas the right hand is 

$$
  \partial_u \partial_\v A^a_\sigma
  +
  \partial_u(C^a{}_{^b c} A^b_v \wedge A^c_\sigma)
  +
  \partial_\sigma(C^a{}_{^b c} A^b_u \wedge A^c_v)
$$
  
(...)

=--

(...)

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


#### Flat Deligne cohomology

Recall the expression for the fibrant representat&#238;ve of
$\mathbf{\flat}\mathbf{B}^n U(1)$ from above.

+-- {: .un_corollary}
###### Corollary

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]],
we have that

$$
  H(X, \mathbf{\flat} \mathbf{B}^n U(1))
  \simeq
  \hat H^n_{flat}(X,U(1))
$$

is the flat [[Deligne cohomology]] of $X$ in degree $n$.

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

This induces the follo^wing infinitesimal analogs of the structures discussed above for $\infty LieGrpd$


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

for the composite [[adjunction]]. For $X,A \in \infty SDGrpd$ we call $\mathbf{\Pi}$ the **Lie [[schreiber:infinitesimal homotopy ∞-groupoid]]** of $X$ and we call $\mathbf{\flat}A$ the **infinitesimally flat $\infty$-Lie groupoid** of $A$.

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

in the (unfinished but noteworthy) notes

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

$\infty$-stacks on [[Diff]] considered, but there with an emphasis of the [[localization of an (infinity,1)-category]] to those that are in fact homotopy invariant and hence collapse to discrete $\infty$-groupoids. See also [[topological ∞-groupoid]].



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