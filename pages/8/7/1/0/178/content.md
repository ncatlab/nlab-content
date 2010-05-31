

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

## Relation between $\infty$-groupoids modeled on $Diff$ and on $CartSp$

In the literature on [[Lie groupoid]]s and [[differentiable stack]]s, these are traditionally conceived as [[stack]]s on the [[site]] [[Diff]] of all [[smooth manifold]]s. As mentioned above, for the purpose of encoding a smooth structure on a [[groupoid]] the category [[Diff]] regarded as a category of test objects is larger than necessary. After all, every manifold is, by definition, itself patched together from [[Cartesian space]]s, and passing to sheaves or stacks on a site really just means that one allows objects patched together from the objects in the site, so that one could just as well take the site to be just that of [[Cartesian space]]s in the first place.

More precisely, notice that we have an [[equivalence of categories]] between the [[category of sheaves]] on [[CartSp]] and on [[Diff]]

$$
  Sh(Diff) \stackrel{\simeq}{\to} Sh(CartSp)
$$

induced from the [[full and faithful functor]] $CartSp \hookrightarrow Diff$. Under this equivalence a sheaf on all of $Diff$ is simply restricted to just the subcategory [[CartSp]].

To see this, simply notice that every [[smooth manifold]] $X$ admits a [[good cover]] $\{U_i \to X\}$, where each $U_i$ is [[diffeomorphism|diffeomorphic]] to a [[Cartesian space]] (essentially by definition of [[manifold]]). By the [[sheaf]] condition, the value $A(X)$ of a sheaf on $X$ is determined by its value on these $U_i$. Hence the sheaf on [[Diff]] is already entirely determined by its restriction to [[CartSp]].


An analogous discussion holds for $\infty$-stacks on these sites. To see what is going on, the following standard example should be a helpful illustration

### Example: the smooth groupoid $\mathbf{B}G$

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

### Properties of the $(\infty,1)$-toposes


One useful aspect of using the site [[CartSp]] to model smooth $\infty$-groupoids is that it is a _site of topologically contractible objects_ . Using this one can show that 

$$
  \mathbf{H} = Sh_{(\infty,1)}(CartSp) \simeq 
  (sPSh(CartSp)_{proj, loc})^\circ
$$

is a [[locally contractible (∞,1)-topos]] and one can explicitly construct models for the corresponding [[schreiber:path ∞-groupoid]]-functor $\Pi : \mathbf{H} \to \infty Grpd$.

...



## The $(\infty,1)$-topos on $CartSp$ of $\infty$-Lie groupoids {#InfSheavesOnCartSp}

We discuss in more detail some properties of the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ of [[(∞,1)-sheaves]] on [[CartSp]].

+-- {: .un_defn}
###### Definition

Let $C = $ [[CartSp]] equipped with the structure of a [[site]] by the [[coverage]] of [[good open cover]]s.
 
Write $Sh_{(\infty,1)}(CartSp) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}$ for the induced [[topological localization]]. 

=--

By the discussion at [Cech localizaton at a coverage](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#LocalizationAtCoverage) this is modeled by the [[Bousfield localization of model categories|left Bousfield localization]] of $sPSh(CartSp)_{proj}$ at [[Cech nerve]]s of covering families.

+-- {: .un_lemma}
###### Lemma

Let $X$ be a [[smooth manifold]], regarded as an object in $sPSh(C)$. Ket $\{U_i \to X\}$ be a [[good open cover]] of $X$ and $C(\{U_i\})$ the corresponding [[Cech nerve]]. Then 

$$
  C(\{U_i\}) \stackrel{\simeq}{\to} X
$$

is a weak equivalence in $sPSh(CartSp)_{proj,cov}$ and in fact a cofibrant replacement for $X$.

=--

+-- {: .proof}
###### Proof

The morphism $\coprod_i j(U_i) \to X$ of which $C(\{U_i\})$ is the Cech nerve of a [[local epimorphism]] in that for every $j(V) \to X$ there exists a [[covering]] family $\{V_i \to V\}$ and lifts $\sigma_i$

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

### Strict smooth $\infty$-groupoids


Many $\infty$-Lie groupoids appearing in practice are (equivalent) to objects in sub-$(\infty,1)$-categories of $Sh_{(\infty,1)}(CartSp)$ of much stricter $\infty$-Lie groupoids. These subcategories typically offer convenient and desireable contexts for formulating and proving statements about special cases of general $\infty$-Lie groupoid.  Therefore it is of interest to have various notions of _strict_ $\infty$-Lie groupoids inside all of them.

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
