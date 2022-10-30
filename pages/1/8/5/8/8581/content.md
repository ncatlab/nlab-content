
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
* table of contents
{:toc}

## Idea

The concept of _smooth groupoid_ is the first generalization of the concept of _[[smooth sets]]_ ([[smooth spaces]]) to [[higher differential geometry]], it is a joint generalization of [[smooth sets]] ([[smooth manifolds]], [[diffeological spaces]], ...), [[orbifolds]] and [[Lie groupoids]], hence it also subsumes [[deloopings]] of [[Lie groups]] and [[diffeological groups]]. It also subsumes smooth [[moduli stacks]], for instance of [[gauge fields]].

Technically, a smooth groupoid is a [[groupoid]]-valued [[stack]] on the [[site]] of [[smooth manifolds]] (sometimes called a "smooth stack", but this is somewhat ambiguous), or equivalently on its [[dense subsite]] [[CartSp]] of just [[Cartesian spaces]] and [[smooth functions]] between them. This is equivalently an [[n-truncated object in an (infinity,1)-topos|1-truncated]] [[smooth ∞-groupoid]].

For more see also at _[[geometry of physics -- smooth homotopy types]]_.



## Definition

+-- {: .num_remark }
###### Remark
**on how not to define smooth groupoids**

One could be tempted to define smooth groupoids to be [[internal groupoids]] in [[smooth sets]]. Restricting this definition to groupoids internal to [[diffeological spaces]] yields the concept of _[[diffeological groupoid]]_, restricting it further to groupoids internal to [[smooth manifolds]] yields the concept of _[[Lie groupoid]]_. While these are respectable definitions in themselves, care needs to be exercised in interpreting them correctly: they do _not_ in themselves exhibit the correct [[homotopy theory]] of smooth groupoids. One may of course fix this by changing the concept of [[morphisms]] to generalized morphisms called _[[Morita morphisms]]_ or _[[bibundles]]_. These are certainly useful tools for working with smooth groupoids, and they serve to present their correct homotopy theory, but they do not serve well as the definition of this homotopy theory. For instance without further insight it is rather impossible to guess form the concept of [[bibundles]] between groupoids its correct generalization to [[smooth 2-groupoids]] etc.

But just as the definition of [[smooth sets]], contrasted with that of [[smooth manifolds]], is not only more powerful but also _simpler_, so there is a definition of smooth groupoids which not only does give the correct homotopy theory, but it does so while being much more transparent than these more traditional presentations.

Now, this definition, given below, amounts to saying that smooth groupoids are stacks on the site of smooth manifolds, and that in turn may tend to not sound like a simple definition at all. But there is a further simplification at work. Traditional texts tend to define stacks in terms of the comparatively intricate structures of [[pseudofunctors]] or (dually under the [[Grothendieck construction]]) [[fibered categories]] satisfying [[descent]], and the rich structure of these combinatorial objects tends to become unwieldy already for fairly simple examples. But the theory of [[localization]] of categories turns out to handle the same theory of stacks by much more tractable means (e.g. [Hollander 01](stack#Hollander01)). Here a stack is _presented_ by a plain functor with no [[descent]] condition imposed, something that is hence as simple as a pair of two presheaves. The nature of stacks is then instead just encoded in remembering that some of the morphisms of presheaves of groupoids are to be labeled as [[weak equivalences]], namely those that locally restrict to equivalences of groupoids. 

This style of definition combines the simplicity of the naive definition of Lie groupoids with the full power of [[homotopy theory]], and it immediately generalizes to a definition of [[∞-stacks]] which is just as simple, hence, in the present context, to a definition of [[smooth ∞-groupoid]].

=--

### Pre-smooth groupoids
 {#PreSmoothGroupoids}


+-- {: .num_defn }
###### Definition

Write [[CartSp]] for the [[category]] of [[Cartesian spaces]] $\mathbb{R}^n$, $n \in \mathbb{N}$, with [[smooth functions]] between them. (The [[full subcategory]] of [[SmoothMfd]] on the Cartesian spaces.) Regard this as a [[site]] by equipping it with the [[coverage]] of (differentiably) [[good open covers]].

=--

For more on this see at _[[geometry of physics -- coordinate systems]]_.


In view of the [[motivation for sheaves, cohomology and higher stacks]] and in direct [[analogy]] with the discussion at _[[geometry of physics -- smooth sets]]_, just replacing [[sets]] by [[groupoids]] throughout, we set:

+-- {: .num_defn #PreSmoothGroupoid}
###### Definition

A _pre-smooth groupoid_ $X$ is a [[presheaf]] of [[groupoids]] on [[CartSp]], hence a [[functor]]

$$
  X \colon CartSp^{op} \longrightarrow Grpd
$$

from [[CartSp]] to the [[1-category]] [[Grpd]].


=--

See at _[geometry of physics -- homotopy types -- groupoids](geometry+of+physic+--+homotopy+types#Groupoids)_ for more on bare groupoids. Here we will freely assume familiarity with these.

+-- {: .num_remark #YonedaIntuition}
###### Remark

The intuition for def. \ref{PreSmoothGroupoid} is the following: a smooth structure on a groupoid is to be determined by which maps from abstract [[coordinate systems]] $\mathbb{R}^n$ into it are to be regarded as smooth maps. Since, by its groupoidal nature, two such maps may be related by a smooth [[homotopy]]/[[gauge transformation]] (in physics: "twisted sectors"), the collection of all smooth functions from $\mathbb{R}^n$  into the smooth groupoid $X$ is itself a bare groupoid. We here _define_ a pre-smooth groupoid as something that assigns to each abstract coordinate systems a groupoid of would-be smooth maps into it

"$X(\mathbb{R}^n) = \left\{ \array{
     & \nearrow \searrow^{\mathrlap{smooth}}
     \\
    \mathbb{R}^n
    &\Downarrow&
    X
    \\
    & \searrow \nearrow_{\mathrlap{smooth}}
 } \right\}$"

We sometimes therefore speak of $X(\mathbb{R}^n)$ as the groupoid of _plots_ or of _probes_ of $X$ (which here is only defined by these!) by $n$-dimensional coordinate systems.

=--

The [[Yoneda lemma]] will turn this intuition into a theorem. For that we need to speak of [[homomorphisms]] of pre-smooth groupoids, hence of "smooth functors" betwen pre-smooth groupoids.

+-- {: .num_defn #HomGroupoidsOfPreSmoothGroupoids}
###### Definition

A [[homomorphism]] or _smooth map_ between pre-smooth groupoids is a [[natural transformation]] between the [[presheaves]] that they are. We write  

$$
  PreSmooth1Type
  \coloneqq
  Funct(CartSp^{op}, Grpd)
$$ 

for the [[functor category]], the _[[category]] of pre-smooth groupoids_, def. \ref{PreSmoothGroupoid}, regarded naturally as a [[Grpd]]-[[enriched category]].

This means that for $X,Y \in PreSmooth1Type$ two pre-smooth groupoids, then the bare [[hom-groupoid]] 

$$
  PreSmooth1Type(X,Y)_\bullet
  \in 
  Grpd
$$

between them has 

* as [[objects]] the [[natural transformations]] $f \colon X \to Y$ between $X$ and $Y$ regarded as [[functors]], hence collections $\{f(\mathbb{R}^n)\}_{n \in \mathbb{N}}$ of [[functors]] between [[groupoids]] of probes

  $$
     f(\mathbb{R}^n) \colon X(\mathbb{R}^n) \longrightarrow Y(\mathbb{R}^n)
  $$

  such that for every [[smooth function]] $\phi \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ between abstract coordinate charts, these form a (strictly) [[commuting diagram]] with the probe-pullback functors of $X$ and $Y$:

  $$
    \array{
       X(\mathbb{R}^{n_1}) &\overset{f(\mathbb{R}^n)}{\longrightarrow}& Y(\mathbb{R}^{n_1})
       \\
       {}^{\mathllap{X(\phi)}}\downarrow && \downarrow^{\mathrlap{Y(\phi)}}
       \\
       X(\mathbb{R}^{n_2}) &\overset{f(\mathbb{R}^n)}{\longrightarrow}& Y(\mathbb{R}^{n_2})       
    }
    \,;
  $$

* as [[morphisms]] $H \colon f \rightarrow g$ the "[[modifications]]" of these, hence collections $H(\mathbb{R}^n) \colon f(\mathbb{R}^n)\to g(\mathbb{R}^n)$ of [[natural transformations]], such that for every [[smooth function]] $\phi \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ the [[whiskering]] of these satisfies

  $$
    \array{
       X(\mathbb{R}^{n_1})
       \\
       \downarrow^{\mathrlap{X(\phi)}}
       \\
       & \nearrow \searrow^{\mathrlap{f(\mathbb{R}^{n_2})}}
       \\
       X(\mathbb{R}^{n_2})
       &\Downarrow^{H(\mathbb{R}^{n_2})}&
       Y(\mathbb{R}^{n_2})
       \\
       & \searrow \nearrow_{\mathrlap{g(\mathbb{R}^{n_1})}}
    }
    \;\;\;
    =
    \;\;\;
    \array{
       & \nearrow \searrow^{\mathrlap{f(\mathbb{R}^{n_1})}}
       \\
       X(\mathbb{R}^{n_1})
       &\Downarrow^{H(\mathbb{R}^{n_1})}&
       Y(\mathbb{R}^{n_1})
       \\
       & \searrow \nearrow_{\mathrlap{g(\mathbb{R}^{n_1})}}
       \\
       && \downarrow^{\mathrlap{Y(\phi)}}
       \\
       && Y(\mathbb{R}^{n_2}) 
    }
  $$
 
=--

+-- {: .num_remark}
###### Remark

Despite the size of the diagrams in def. \ref{HomGroupoidsOfPreSmoothGroupoids}, what they encode is immediate: this just says that smooth maps between pre-smooth groupoids take all probes of $X$ by abstract coordinate charts to probes of $Y$ by these charts, and take gauge transformations between these to gauge transformations between those, in a way that it compatible with changing probes along smooth maps.

=--


The following is the [[Yoneda lemma]] in this context, and it says that this intuition in remark \ref{YonedaIntuition} is fully correct:


+-- {: .num_prop #YonedaForPreSmoothGroupoids}
###### Proposition

Every [[Cartesian space]] $\mathbb{R}^n$ defines a pre-smooth groupoid $\underline{\mathbb{R}}^n$, def. \ref{PreSmoothGroupoid}, by the assignment

$$
  \underline{\mathbb{R}}^n \colon \mathbb{R}^k  \mapsto C^\infty(\mathbb{R}^k, \mathbb{R}^n)
   \in 
  Set
  \hookrightarrow
  Grpd
$$

where the [[set]] of [[smooth functions]] on the right is regarded as a [[groupoid]] with only [[identity]] morphisms. This construction constitutes a [[fully faithful functor]]

$$
  \underline{(-)}
  \colon
  CartSp \hookrightarrow PreSmooth1Type
$$

making [[CartSp]] a [[full subcategory]] of that of pre-smooth groupoids (the [[Yoneda embedding]]).
Under this embedding for any pre-smooth groupoid $X\in PreSmooth1Type$ and any Cartesian space $\mathbb{R}^n$, there is a [[natural equivalence]] of [[groupoids]]

$$
  PreSmooth1Type(\underline{\mathbb{R}}^n, X)
  \simeq
  X(\mathbb{R}^n)
$$

(the [[Yoneda lemma]] proper).

=--

+-- {: .num_remark}
###### Remark

The last statement of the [[Yoneda lemma]] in prop. \ref{YonedaForPreSmoothGroupoids} expresses just the intuition of remark \ref{YonedaIntuition} and justifies removing the quotation marks displayed there. It also justifies dropping the extra underline denoting the [[Yoneda embedding]]. We will freely identify from now on $\mathbb{R}^n$ with the pre-smooth groupoid that it represents.

=--

+-- {: .num_example}
###### Example

For $X$ a [[smooth set]] (e.g. a [[smooth manifold]]), hence in particular a functor

$$
  X \colon CartSp^{op} \to Set
$$

then its embedding into groupoids

$$
  X \colon CartSp^{op} \to Set \hookrightarrow Grpd
$$

is a pre-smooth groupoid.

=--

More generally:

+-- {: .num_example #ExternalYonedaEmbeddingsIntoPreSmooth1Type}
###### Example

Let 

$$
  \mathcal{G}_\bullet
  = 
  \left\{
    \mathcal{G}_1
      \stackrel{\overset{s}{\longrightarrow}}{\stackrel{\overset{i}{\longleftarrow}}{\underset{t}{\longrightarrow}}}
    \mathcal{G}_0
  \right\}
$$ 

be an [[internal groupoid]] in [[smooth sets]], hence a pair $\mathcal{G}_0, \mathcal{G}_1 \in Smooth0Type$ of smooth sets, equipped with source, target, identity homomorphisms of smooth sets between them, and equipped with a compatibly unital, associative and invertible composition map $\mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1 \to \mathcal{G}_1$. By definition of [[smooth sets]], this means that for every abstract coordinate system $\mathbb{R}^n$ then 

$$
  \mathcal{G}(\mathbb{R}^n)_\bullet
  = 
  \left\{
    \mathcal{G}(\mathbb{R}^n)_1
      \stackrel{\overset{s(\mathbb{R}^n)}{\longrightarrow}}{\stackrel{\overset{i(\mathbb{R}^n)}{\longleftarrow}}{\underset{t(\mathbb{R}^n)}{\longrightarrow}}}
    \mathcal{G}(\mathbb{R}^n)_0
  \right\}
$$ 

is a bare [[groupoid]]. Moreover, this assignment is functorial and hence defines a pre-smooth groupoid

$$
  \mathbb{R}^n 
  \mapsto
  \mathcal{G}(\mathbb{R}^n)_\bullet
  \,.
$$


This exhibits sequence of [[full subcategory]] inclusions

$$
  Grp
  \hookrightarrow
  LieGrpd
  \hookrightarrow
  DiffGrpd
  \hookrightarrow
  Grpd(Smooth0Type)
  \hookrightarrow
  PreSmooth1Type
$$

of [[internal groupoids]] in [[smooth sets]] into pre-smooth groupoids, and hence (by further restriction) also of [[diffeological groupoids]], of [[Lie groupoids]] and of course of just bare [[groupoids]], too. 

Regarding a bare groupoid $\mathcal{G}_\bullet$ as a pre-smooth groupoid this way means to regard it as equipped with [[discrete object|discrete]] [[smooth structure]]. It is given by the [[constant presheaf]]

$$
  \mathbb{R}^n \mapsto \mathcal{G}_\bullet
$$

exhibiting the fact that smooth functions from an $\mathbb{R}^n$ into a geometrically discrete space are constant on one of the points of this space, a situation which here is only refined by the fact that every morphism in the groupoid thus gives a [[homotopy]]/[[gauge transformation]] between the two smooth functions that are constant on the two endpoints of this morphism.

=--

A particular case of this of special importance is this:

+-- {: .num_example #DeloopedGroupAsPreSmoothGroupoid}
###### Example

For $G$ a [[Lie group]], we write $(\mathbf{B}G)_\bullet \in Grpd(Smooth0Type)$ for the Lie groupoid which 

$$
  (\mathbf{B}G)_\bullet
  =
  \left(
     G \stackrel{\longrightarrow}{\stackrel{\overset{i}{\longleftarrow}}{\longrightarrow}}
    \ast
  \right)
$$

whose composition is the product operation in the group (the groupoidal [[delooping]] of $G$). The pre-smooth groupoid that this corresponds to under the embedding of example \ref{ExternalYonedaEmbeddingsIntoPreSmooth1Type} has groupoids of probes of the form


$$
  \mathbb{R}^n 
   \mapsto 
   B \left(C^\infty(\mathbb{R}^n,G)_{disc}\right)
$$

where on the right we have the [[homotopy 1-type]] whose [[fundamental group]] is that of smooth $G$-valued functions on $\mathbb{R}^n$, under pointwise mulitplication.


=--


More specifically, the following class of examples plays a special role in the theory, as the encode what it takes for a pre-smooth groupoid to be a genuinely smooth groupoid.

+-- {: .num_example #GroupoidOfCover}
###### Example

For $X$ a [[smooth manifold]], let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. Its _[[Cech groupoid]]_ is the [[Lie groupoid]] ([[diffeological groupoid]]) $C(\{U_i\})_\bullet$ whose

* manifold of objects is $C(\{U_i\})_0 \coloneqq \underset{i \in I}{\coprod} U_i$ is the [[disjoint union]] of all the [[charts]] of the cover;

* manifold of morphisms is $C(\{U_i\})_1 \coloneqq  \underset{i,j \in I}{\coprod}U_i \underset{X}{\times} U_j$ is the [[disjoint union]] of all [[intersections]] of charts.

and whose source, target and identity maps are the evident inclusions. There is then a _unique_ composition operation.

So a global point $\ast \to C(\{U_i\})_\bullet$ may be thought of as a pair $(x,i)$ of a point in the manifold $X$ and a label $i$ of a chart $U_i$ that contains it, and there is is precisely one morphism between two such global point $(x,i)\to (y,j)$ whenever $x = y$ in $X$ and both $U_i$ as well as $U_j$ contain $x$, hence one morphism for each point in an intersection of two patches. Composition of morphism is just re-remembering which intersections they sit in, the schematic picture of the Cech groupoid is this this:

$$
  C(\{U_i\})_\bullet
  =
  \left\{
    \array{
      && (x,j)
      \\
      & \nearrow && \searrow
      \\
      (x,i)
      && \longrightarrow &&
      (x,k)
    }
  \right\}
  \,.
$$

Under the embedding of example \ref{ExternalYonedaEmbeddingsIntoPreSmooth1Type} there is an evident morphism of pre-smooth groupoids

$$
  C(\{U_i\})
  \longrightarrow
  X
$$

from this Cech groupoid of the cover to the manifold that is being covered. This morphism simply forgets the information of which chart or intersection of charts a point is regarded to be in, and just remembers it as a point of $X$. 

$$
  ((x,i) \to (x,j))
  \mapsto
  (x \stackrel{id_x}{\to} x)
  \,.
$$

=--

+-- {: .num_prop #CechCoyclesAsSmoothMaps}
###### Proposition


Let $X$ a [[smooth manifold]], $\{U_i \to X\}$ an [[open cover]]
and $C(\{U_i\})$ the corresponding Cech groupoid, def. \ref{GroupoidOfCover}.
Let $G$ be a [[Lie group]] and $\mathbf{B}G$ its groupoidal [[delooping]] according to example \ref{DeloopedGroupAsPreSmoothGroupoid}.

Then the hom-groupoid $PreSmooth1Type(C(\{U_i\}), \mathbf{B}G)$ of maps from $C(\{U_i\})$ to $\mathbf{B}G$, def. \ref{HomGroupoidsOfPreSmoothGroupoids},
has

* as [[objects]] the [[Cech cohomology|Cech cocycles]] of degree 1 on $X$ relative to the cover and with values in $G$; i.e. collections of smooth functions

  $$
    g_{ i j} \;\colon\; U_i \underset{X}{\times} U_j \longrightarrow G
  $$

  satisfying on each triple intersection the cocycle condition

  $$
    g_{i j} g_{j k} = g_{i k}
  $$

* as [[morphisms]] the [[coboundaries]] between such cocycles $\{g_{i j}\}$ and $\{\tilde g_{j k}\}$, hence  collections of smooth functions 

  $$
    h_{i} \colon U_i \longrightarrow G
  $$

  such that on each intersection of charts

  $$
    g_{i j} h_j  = h_i \tilde g_{i j}
    \,.
  $$

In particular the [[connected components]] of the Hom-groupoid is hence the [[Cech cohomology]] itself:

$$ 
  \pi_0
  PreSmooth1Type(C(\{U_i\}), \mathbf{B}G)
  \simeq
  H^1_{Cech}(X,\{U_i\}; G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is a matter of unwinding the definitions that the statement holds disregarding smooth structure everywhere, hence after evaluating the morphisms of pre-smooth groupoids on $\mathbb{R}^0$. That the component functions that one finds this way all have to be smooth then follows componentwise with the [[Yoneda lemma]] for presheaves of sets on $CartSp$ (as discussed at _[[geometry of physics -- smooth sets]]_).

=--


### Gluing 
 

The "bootstrap"-definition of pre-smooth groupoids [above](#PreSmoothGroupoids) works as intended, by prop. \ref{YonedaForPreSmoothGroupoids}, it just needs to be restricted now to something a little less general. The issue is that while this definition consistently identifies a smooth-structure-to-be by what its possible smooth probes are, it does not enforce yet the consistent _gluing_ of probes:

for $X$ a pre-smooth groupoid, then given a probe of it of the form $\sigma \colon \mathbb{R}^n \to X$ and given a [[covering]] $\{U_i \to \mathbb{R}^n\}$ of the probe space by other probe spaces $U_i \simeq \mathbb{R}^n$, then it should be possible to reconstruct $\sigma$ from knowing its restrictions $\sigma_{|U_i}\colon U_i \to X$ to these charts, and the information of how these are identified by gauge transformations on double overlaps.

Such a system of local data and of gauge identification on double overlaps is just what maps out of the Cech groupoid $C(\{U_i\})$, def. \ref{GroupoidOfCover}, encode. This is shown by prop. \ref{CechCoyclesAsSmoothMaps} for the case that $X$ is of the form $(\mathbf{B}G)_\bullet$, example \ref{DeloopedGroupAsPreSmoothGroupoid}, but this is already the archetypical case. 

In other words, the condition that smooth probes of $X$ by coordinate charts $\mathbb{R}^n$ glue along covers $\{U_i \to \mathbb{R}^n\}$ of these charts is the condition that the groupoid of smooth maps out of $\mathbb{R}^n$ itself

$$
  \mathbb{R}^n \longrightarrow X
$$

is equivalent to the groupoid of maps out of the Cech groupoid of any cover

$$
  C(\{U_i\}) \longrightarrow X
$$

and is so via the "restriction" map that takes the former and precomposes it with the canonical map $C(\{U_i\}) \to \mathbb{R}^n$.

$$
  \array{
    C(\{U_i\}) &\longrightarrow& X
    \\
    \downarrow & \nearrow
    \\
    \mathbb{R}^n
  }
  \,.
$$


+-- {: .num_defn #DescentForPreSmoothGroupoids}
###### Definition

A pre-smooth groupoid $X \in PreSmooth1Type$, def. \ref{PreSmoothGroupoid}, _satisfies descent_ if for all $n \in \mathbb{N}$ and for all differentiably [[good open covers]] $\{U_i \to \mathbb{R}^n\}$ of the $n$-dimensional abstract [[coordinate chart]], the functor

$$
  X(\mathbb{R}^n) \simeq PreSmooth1Type(\mathbb{R}^n, X)
  \longrightarrow
  PreSmooth1Type(C(\{U_i\}),X)
$$

given by pre-composition with $C(\{U_i\}) \to \mathbb{R}^n$, is an [[equivalence of groupoids]].

=--

+-- {: .num_remark}
###### Remark

The condition in def. \ref{DescentForPreSmoothGroupoids} is called the _stack condition_, or the condition of _[[descent]]_, alluding to the fact that it says that $X$ "descends" down along the cover projection. So a smooth groupoid is a _[[stack]]_ on the [[site]] [[CartSp]]. This is a higher analog of the [[sheaf]] condition (see the next example) and hence a more systematic terminology would be to say that such $X$ is a _[[2-sheaf]]_ or rather a _[[(2,1)-sheaf]]_ (since it takes values in [[groupoids]] as opposed to in more general [[categories]]).

=--

+-- {: .num_prop}
###### Proposition

Let $X \in PreSmooth0Type \hookrightarrow PreSmooth1Type$ be a pre-smooth groupoid which is really just a pre-smooth set, hence a presheaf on $CartSp$ that takes values in groupoids with only identity morphisms

$$
  X \colon CartSp^{op} \longrightarrow Set \hookrightarrow Grp
  \,.
$$ 

Then $X$ is a smooth groupoid in the sense of def. \ref{DescentForPreSmoothGroupoids} precisely if it is a [[smooth set]], hence precisely if, as a presheaf, it satisfies the [[sheaf]] condition.

=--

+-- {: .num_example #SmoothManifoldsSatisfyDescentAsPreSmoothGroupoids}
###### Example

In particular, for $X \in SmoothMfd \hookrightarrow PreSmooth0Type \hookrightarrow PreSmooth1Type$ a [[smooth manifold]], it satisfies descent as a pre-smooth groupoid.

=--


+-- {: .num_remark}
###### Remark

There is an alternative formulation of the whole theory where instead of the [[site]] [[CartSp]] one uses the site [[SmoothMfd]] of all [[smooth manifolds]]. Everything discussed so far goes through verbatim for that site, too, but the [[descent]] condition in def. \ref{DescentForPreSmoothGroupoids} is a much stronger condition.

For instance the presheaves of the form $(\mathbf{B}G)_\bullet = (G \stackrel{\longrightarrow}{\longrightarrow} \ast)$ from example \ref{DeloopedGroupAsPreSmoothGroupoid} satisfy descent on $CartSp$, but not all $SmoothMfd$. Still, once we have defined the higher category of smooth groupoids, the definition wil be equivalent for both choices of sites. 

The choice of the smaller site is the one that is easier to work with, and therefore we stick with that. In fact, most every example of a pre-smooth groupoid that one runs into satisfies descent on $CartSp$.

=--

For example:

+-- {: .num_prop #bfBGbulletSatisfiesDescent}
###### Proposition

For $G$ a [[Lie group]], then the pre-smooth [[delooping]] groupoid
$(\mathbf{B}G)_\bullet$ of example \ref{DeloopedGroupAsPreSmoothGroupoid}
satisfies descent on $CartSp$, def. \ref{DescentForPreSmoothGroupoids}.

=--

+-- {: .proof}
###### Proof

For $\{U_i \to \mathbb{R}^n\}$ a differentiably good open cover,
then by prop. \ref{CechCoyclesAsSmoothMaps} the groupoid
$PreSmooth1Type(C(\{U_i\}),(\mathbf{B}G)_\bullet)$
is the groupoid of [[Cech cohomology|Cech 1-cocycles and coboundaries]]
with coeffcients in $G$ on $\mathbb{R}^n$ relative to the cover.
But this is equivalently the groupoid of $G$-principal bundles
on $\mathbb{R}^n$. Now because the underlying [[topological space]]
of $\mathbb{R}^n$ is [[contractible topological space|contractible]],
all $G$-principal bundles on it are equivalent to the trivial one. 
But this is evidently represented by the image of point
under the map

$$
  B (C^\infty(G)_{disc})
  \simeq
  PreSmooth1Type(\mathbb{R}^n, (\mathbf{B}G)_\bullet)
  \longrightarrow
  PreSmooth1Type(C(\{U_i\}), (\mathbf{B}G)_\bullet)
  \,.
$$

Therefore this is an [[essentially surjective functor]] of groupoids.
Moreover, the [[automorphisms]] of the trivial $G$-principal bundles
are precisely the smooth $G$-functions, hence this is also 
a [[fully faithful functor]] of groupoids. Accordingly it is 
an [[equivalence]] of groupoids.

=--

The same argument however shows that on the larger site [[SmoothMfd]] this object does not satisfy descent. Put positively, this is the content of prop. \ref{StackMapsFromXtoDeloopingOfG}. below.





### Weak equivalences

While the morphisms of pre-smooth groupoids defined above correctly encode
morphisms of smooth structures (by taking smooth probes compatibly to smooth probes),
they are not sensitive enough yet to the required concept of [[equivalence]].
This is because smooth structure, being about existence of [[differentiation]],
is to be detected entirely locally, namely [[stalk]]-wise. If for instance $X$ is a [[smooth manifold]], then its smooth structure is determined, around any of its points, by the smooth structure of an arbitrarily small [[open ball]] around that point.

+-- {: .num_defn #Stalks}
###### Definition

For $n \in \mathbb{N}$, and $0 \lt r \lt 1 \in \mathbb{R}$ let 

$$
  \mathbb{R}^n \simeq D^n_r \hookrightarrow \mathbb{R}^n
$$

be the [[smooth function]] that regards the [[Cartesian space]] $\mathbb{R}^n$ as the standard $n$-[[disk]] of [[radius]] $r$ around the origin in $\mathbb{R}^n$. 

For $X \in PreSmooth1Type$ we write

$$
  (D^n)^* X \coloneqq {\underset{\longrightarrow_r}{\lim}} X(D^n_r) \in Grpd
$$

for the [[colimit]] (in the 1-category of groupoids) of the restrictions of its groupoids of plots along the inclusion of these open balls -- the _$n$-[[stalk]]_ of $X$. This extends to a [[functor]]

$$
  (D^n)^* \colon PreSmooth1Type \longrightarrow Grpd
$$

=--

This means that objects in $(D^n)^\ast X$ are [[equivalence classes]] of pairs $(r,x_r)$ where $0 \lt r \lt 1$ and where $x_r \in X(D^n_r)$, with two such pairs being equivalent $(r_1, x_{r_1})\sim (r_2, x_{r_2})$ precisely if there is $r_0 \lt r_1,r_2$ such that $x_{r_1}$ becomes equal to $x_{r_2}$ after restriction to $D^n_{r_0}$.

+-- {: .num_defn #LocalWeakEquivalence}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of pre-smooth groupoids, def. \ref{HomGroupoidsOfPreSmoothGroupoids}, is called a 
_local [[weak equivalence]]_ if for every $n \in \mathbb{N}$
the $n$-stalk, def. \ref{Stalks}, is an [[equivalence of groupoids]]

$$
  ((D^n)^* f) \colon (D^n)^* X \stackrel{}{\longrightarrow} (D^n)^* Y
  \,.
$$

=--

We write $X\stackrel{\simeq}{\longrightarrow} Y$ for local
weak equivalences of pre-smooth groupoids. We will mostly just say
_weak equivalence_ for short.


+-- {: .num_prop #CoveringMapIsLocalWeakEquivalence}
###### Proposition

For $X$ a [[smooth manifold]] and $\{U_i \to X\}$ an [[open cover]] for it, then 
the canonical morphism from the corresponding [[Cech groupoid]] to $X$, 
def. \ref{GroupoidOfCover}, is a local weak equivalence in the sense of
def. \ref{LocalWeakEquivalence}.

=--

+-- {: .proof}
###### Proof

The $n$-stalk of the smooth manifold $X$ regarded as a presheaf is the set of equivalence classes of maps from open pointed $n$-disks into it, where two such are identified if they coincide on some small joint sub-disk of their domain. We may call this the set of _[[germs]]_ of $X$ (but beware that this terminology is typically used for something a little bit more restrictive, namely for the case that $n$ is the dimension of $X$ and that all maps from the disks into $X$ are required to be [[embeddings]]).

On the other hand the $n$-stalk of $C(\{U_i\})$ is the groupoid whose set of objects is the set of germs, in this sense, of the disjoint union $\underset{i}{\coprod} U_i$, and whose set of morphisms is the set of germs of the disjoint union $\underset{i,j}{\coprod} U_i \underset{X}{\times} U_j$.

But now since the cover is by _[[open subset|open]]_ subsets, it follows that for every $(x,i,j) \in \underset{i,j}{\coprod} U_i \underset{X}{\times} U_j$, then every germ of objects $[g]$ around $(x,i)$  has a representative $g$ that factors through this double intersection charts:  $g \colon D^n_r \to U_i \underset{X}{\times} U_j \to \underset{i}{\coprod} U_u$. And similarly for $(x,j)$.

This means that the groupoid of $n$-stalks is a disjoint union of groupoids, one for each germ of $X$, all whose components are groupoids in which there is a unique morphism between any two objects, which are copies of this germ regarded as sitting in one of the charts of the cover. This means that each of these connected components is [[equivalence of groupoids|equivalent]] to the point.

Now the canonical cover projection sends each of these connected components to the germ that it corresponds to. Hence this is a an [[equivalence of groupoids]].

=--

### Hypercovers

+-- {: .num_defn #SplitHypercover}
###### Definition

A morphism $p \colon Y \longrightarrow X$ of pre-smooth groupoids
is called a [[split hypercover]] if 

1. $Y$ is 

   1. degreewise a [[coproduct]] of [[Cartesian spaces]];

   1. such that the degenerate elements split off as a dijoint summand.

1. $p$ is a weak equivalence, def. \ref{LocalWeakEquivalence}.

=--

+-- {: .num_prop #GoodCechCoverIsSplitHypercover}
###### Proposition

For $X$ a [[smooth manifold]] and $\{U_i \to X\}$ an [[open cover]],
then the canonical projection $C(\{U_i\}) \to X$
from the corresponding [[Cech groupoid]], def. \ref{GroupoidOfCover},
is a split hypercover precisely if the cover is differentiably [[good open cover|good]].

=--

+-- {: .proof}
###### Proof

For every cover the map is a weak equivalence, by prop. \ref{CoveringMapIsLocalWeakEquivalence}.

For the Cech groupoid the condition of cofibrancy in def. \ref{SplitHypercover} means that every non-empty finite intersection of patches is [[diffeomorphism|diffeomorphic]] to a [[Cartesian space]], hence to an [[open ball]].
This is precisely the definition of differentialbly [[good open cover]].

=--




### The $(2,1)$-category of smooth groupoids

The [[Grpd]]-[[enriched category]] of genuine smooth groupoids is that obtained from that of pre-smooth groupoids, def. \ref{HomGroupoidsOfPreSmoothGroupoids} by "universally turning local [[weak equivalences]], def. \ref{LocalWeakEquivalence}, into actual [[homotopy equivalences]]". This is stated formally by def. \ref{SmoothGroupoidsBySimplicialLocalization} below, but for many applications in practice certain concrete presentations of what this means concretely are well sufficient, one of these we state below in prop. \ref{HomGroupoidsOutOfCofibrantIntoFibrantGroupoidPresheaves}.

+-- {: .num_defn #SmoothGroupoidsBySimplicialLocalization}
###### Definition

Write 

$$
  Smooth1Type 
   \coloneqq
  L_{lwe} PreSmooth1Type
$$

for the [[(2,1)-category]] which is the [[simplicial localization]] of groupoid-valued presheaves at the local weak equivalences, def. \ref{LocalWeakEquivalence}.

An [[object]] $X \in Smooth1Type$ we call a **[[smooth groupoid]]** or
**[[smooth homotopy type|smooth homotopy 1-type]]**.

=--



+-- {: .num_prop #HomGroupoidsOutOfCofibrantIntoFibrantGroupoidPresheaves}
###### Proposition

Let $X,A \in PreSmooth1Type$ such that $A$ satisfies descent, 
def. \ref{DescentForPreSmoothGroupoids}. Let $Y \to X$
be a [[split hypercover]] of $X$, def. \ref{SplitHypercover}.

Then there is an [[equivalence of groupoids]]

$$
  Smooth1Type(X,A)
  \simeq
  PreSmooth1Type(Y,A)
$$

between the [[hom-groupoid]] of smooth groupoids from $X$ to $A$,
and that of pre-smooth groupoids, def. \ref{HomGroupoidsOfPreSmoothGroupoids},
from $Y$ to $A$.

=--

Such statements follow with [[model structures on simplicial presheaves]] after embedding the present situation in the more general context of [[smooth infinity-groupoids]]. See there for more.

+-- {: .num_remark #NotationForLocalization}
###### Remark

There is a canonical localization functor

$$
  PreSmooth1Type
  \longrightarrow
  L_{lwe} PreSmooth1Type
  =
  Smooth1Type
  \,.
$$

which is really just the identity as a functor. Instead of doing anything
to the objects, passing along this functor just means to change the
definition of the hom-groupoids from the direct definition of 
def. \ref{HomGroupoidsOfPreSmoothGroupoids} to the localized definition.

When a pre-smooth groupoid is given by an [[internal groupoid]]
$\mathcal{G}_\bullet$ in [[smooth sets]] via example \ref{ExternalYonedaEmbeddingsIntoPreSmooth1Type}, then we indicate its image under this functor by removing the subscript index, writing just $\mathcal{G}$.
This reflects the fact that in $Smooth1Type$ it no longer makes
sense to ask what the space of 0-cells and of 1-cells of an object is, as
these are concepts not invariant under local weak equivalence.

In particular this means that we write $\mathbf{B}G$ for the
image of $(\mathbf{B}G)_\bullet$ in $Smooth1Type$.

=--


+-- {: .num_prop #StackMapsFromXtoDeloopingOfG}
###### Proposition

Let $X$ be a [[smooth manifold]], regarded as a smooth 0-groupoid, and let $G$ be a [[Lie group]], with smooth [[delooping]] groupoid $\mathbf{B}G$ 
(example \ref{DeloopedGroupAsPreSmoothGroupoid}, remark \ref{NotationForLocalization}).

Then 

$$
  Smooth1Type(X,\mathbf{B}G)
  \simeq
  G Bund(X)
$$

is equivalently the [[groupoid]] of $G$-[[principal bundles]] on $X$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{bfBGbulletSatisfiesDescent} the object
$(\mathbf{B}G)_\bullet$ satisfies descent on [[CartSp]].
Choose $\{U_i \to X\}$ a differentiably [[good open cover]].
By prop. \ref{GoodCechCoverIsSplitHypercover} the correspoding
[[Cech groupoid]] projection
$C(\{U_i\}) \to X$ is a [[split hypercover]], def. \ref{SplitHypercover}.
Hence, by prop. \ref{HomGroupoidsOutOfCofibrantIntoFibrantGroupoidPresheaves},
there is an [[equivalence of groupoids]]

$$
  Smooth1Type(X,\mathbf{B}G)
  \simeq
  PreSmooth1Type(C(\{U_i\}), (\mathbf{B}G)_\bullet)
  \,.
$$

The groupoid on the right is, by prop. \ref{CechCoyclesAsSmoothMaps},
the groupoid of [[Cech cohomology|Cech 1-cocycles and coboundaries]]
with values in $G$ relative to a good open cover. This is 
equivalently the groupoid of $G$-principal bundles.

=--


+-- {: .num_remark }
###### Remark

The content of prop. \ref{StackMapsFromXtoDeloopingOfG} is in 
common jargon that: _$\mathbf{B}G \in SmoothGrpd$ is the [[moduli stack]] of $G$-[[principal bundles]]".

=--





## Properties

### Embedding into smooth $\infty$-groupoids

By generalizing here [[groupoids]] to general [[Kan complexes]] and [[equivalences of groupoids]] to [[homotopy equivalences]] of Kan complexes, one obtains _smooth [[∞-stacks]]_ or _[[smooth ∞-groupoids]]_, which we write 

$\;\;\; $[[Smooth∞Grpd]] $\coloneqq Sh_{(\infty,1)}(CartSp) \simeq L_{lhe} Func(CartSp^{op}, KanCplx) $. 

We often write $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] for short.

By the [[(∞,1)-Yoneda lemma]] there is a sequence of [[full and faithful (∞,1)-functor|faithful inclusions]]

$\;\;\;$ [[SmoothMfd]] $\hookrightarrow$ [[SmoothGrpd]] $\hookrightarrow$ [[Smooth∞Grpd]].

This induces a corresponding inclusion of [[simplicial objects]] and hence of [[groupoid objects in an (∞,1)-category|groupoid objects]]

$$
  LieGrpd \hookrightarrow Grpd_\infty(SmoothMfd)  \hookrightarrow  Grpd_\infty(Smooth\infty Grpd)
  \,.
$$

For $\mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ a groupoid object we write 

$$
  \mathcal{G}_0 \to \mathcal{G} \coloneqq \underset{\longrightarrow}{\lim}_{n} \mathcal{G}_n
$$

for its [[(∞,1)-colimit|(∞,1)-colimiting]] [[cocone]], hence $\mathcal{G} \in \mathbf{H}$ (without subscript decoration) denotes the [[realization]] of $\mathcal{G}_\bullet$ as a single object in $\mathbf{H}$.

By the [[Giraud-Rezk-Lurie axioms]] of the [[(∞,1)-topos]] $\mathbf{H}$ this morphism $\mathcal{G}_0 \to \mathcal{G}$ is a [[1-epimorphism]] -- an [[atlas]] -- and its construction establishes is an [[equivalence of (∞,1)-categories]] $Grpd_\infty(\mathbf{H}) \simeq \mathbf{H}^{\Delta^1}_{1epi}$, hence morphisms $\mathcal{G}_\bullet \to \mathcal{K}_\bullet$ in $Grpd_\infty(\mathbf{H})$ are equivalently [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
    \mathcal{G}_0 &\to& \mathcal{K}_0
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathcal{G} &\to& \mathcal{K}
  }
  \,.
$$

This is evidently more constrained that just morphisms 

$$
  \mathcal{G} \to \mathcal{K}$ in $\mathbf{H}
$$

by themselves. The latter are the "generalized" or [[Morita morphisms]] between the groupoid objects $\mathcal{G}_\bullet$, $\mathcal{K}_\bullet$. These can be modeled as $\mathcal{G}_\bullet$-$\mathcal{K}_\bullet$-[[bibundles]].




## Examples


### Zoo of concepts subsumed by smooth groupoids

+-- {: .num_example }
###### Example

Every [[smooth space]] is canonically a [[smooth groupoid]] with only identity morphisms.

=--

+-- {: .num_prop }

###### Proposition

The canonical identification yields a [[full subcategory]]

$$
  Smooth0Type \hookrightarrow Smooth1Type
  \,.
$$


=--


Every [[Lie groupoid]] presents a smooth groupoids. Those of this form are also called [[differentiable stacks]].

A [[0-truncated]] smooth groupoid is equivalently a [[smooth space]]. 

For $G$ a [[smooth group]], its [[delooping]] $\mathbf{B}G$ is a smooth groupoid, the [[moduli stack]] of smooth $G$-[[principal bundles]].

### Action groupoids

+-- {: .num_example }
###### Example

For $X$ a [[smooth space]] and $G$ a [[smooth group]] and 

$$\rho : X \times G \to X
$$ 

an [[action]] then  the [[action groupoid]]
 
$$
  X // G \in Smooth1Type

$$

$$
  X // G = 
  \left(
    X \times G 
     \stackrel{\overset{\rho}{\longrightarrow}}{\underset{p_1}{\longrightarrow}}
    X
  \right)
$$

is a [[smooth groupoid]].

=--


### Moduli spaces of gauge fields

#### Groupoid of electromagnetic field configurations
 {#GroupoidOfElectromagneticFieldConfigurations]

The mathematical concept of _[[smooth groupoid]]_ is well familiar, in slight disguise, in the [[physics]] of basic _[[gauge theory]]_. Here we make this explicit for basic [[electromagnetism]]. For more exposition and details along these lines see
([Eggersson 14](#Eggersson14)).

We have seen in _[The electromagnetic field strength](#ElectromagneticFieldStrength)_ that a configuration of the electromagnetic field on $\mathbb{R}^4$ is given by a [[differential 1-form]] $A \in \Omega^1(\mathbb{R}^4)$, the "[[electromagnetic potential]]". It describes a field configuration with [[field strength]] Lorentz tensor (with respect to the canonical [[coordinates]] $(t, x^1, x^2, x^3) \coloneqq (x^i)_{i = 1}^4 = $ on $\mathbb{R}^4$)

$$
  \begin{aligned}
    F & = \mathbf{d}A 
      \\
      & =
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
      \\
      & 
       + B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3
       + B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1
       + B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2
  \end{aligned}     
$$

with electric [[field strength]] $(E_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ and magnetic [[field strength]] $(B_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ given  that is given by the [[de Rham differential]] of $A$:

$$
  \begin{aligned}
    F = \mathbf{d}A
  \end{aligned}
  \,.
$$

After Maxwell it was thought that $F \in \Omega^2(\mathbb{R}^4)$ alone genuinely reflects the configuration of the electromagnetic field. But with the discovery of [[quantum mechanics]] it became clear that it is indeed the potential $A$ itself that reflects the configuration of the electromagnetic field: in the presence of [[magnetic flux]] or other topoligical constraints, there can be different $A, A' $ with the _same_ $F = \mathbf{d}A = \mathbf{d}A'$ which nevertheless describe experimentally distinguishable electromagnetic field configurations. (Distinguishable by the [[Aharonov-Bohm effect]] and also to some extent by [[Dirac charge quantization]]; this is discussed at _[Circle-principal connections](#CirclePrincipalConnections)_ below.)

However, not all different gauge potentials describe different physics. The actual configuration space of electromagnetism on a [[spacetime]] $X$ is finer than $\mathbf{\Omega}^2_{cl}(X)$ but coarser than $\mathbf{\Omega}^1(X)$. And it is not quite a smooth space itself, but a _[[smooth groupoid]]_:

one finds that two electromagnetic potentials $A, A' \in \Omega^1(\mathbb{R}^4)$ for which there is a function $\lambda \in C^\infty(\mathbb{R}^4)$ such that 

$$
  A' = A + \mathbf{d}\lambda
$$

represent _different but [[equivalence|equivalent]]_ field configurations. One says that _$\lambda$ induces a [[gauge transformation]] from $A$ to $A'$_. We write $\lambda \colon A \stackrel{\simeq}{\to} A'$ to reflect this.

So the configuration space of electromagnetism does not just have points and coordinate systems. But it is also equipped with the information of a space of gauge transformations between any two coordinate systems laid out in it (which may be empty). 

To see what the structure of such a _smooth gauge groupoid_ should be, notice that the above defines an [[action]] of smooth functions $\lambda$ on smooth $1$-forms $A$, 


+-- {: .num_defn #ActionOfFunctionsOnForms}
###### Definition

For any $U \in $ [[CartSp]], Write $\Omega^1_{vert}(X \times U)$ for the set of [[differential 1-forms]] on $X \times U$ with no components along $U$, and write $C^\infty(X \times U , U(1))$ for the [[group]] of [[circle group]] valued [[smooth functions]]. There is an [[action]] of this group on the 1-forms 

$$
  \rho_U 
   \colon 
  \Omega^1_{vert}(X \times U) \times C^\infty(X \times U, U(1))
    \to
  \Omega^1_{vert}(X \times U)
$$

given by

$$
  \rho_U \colon (A,\lambda) \mapsto A + \mathbf{d}_X \lambda
  \,.
$$

=--

Given such an action of a [[discrete group]] on a [[set]], we might be demoted to form the [[quotient]] set $\Omega^1_{vert}(X\times U)/C^\infty(X \times U, U(1))$. This set contains the gauge [[equivalence classes]] of $U$-parameterized collections of electromagnetic gauge fields on $X$. But it turns out that this is too little information to correctly capture physics. For that instead we need to remember not just that two gauge fields are equivalent, but how they are equivalent. That is, we for $\lambda$ a gauge transformation from $A_1$ to $A_2$, we should have an [[equivalence]] $\lambda \colon A_1 \stackrel{\simeq}{\to} A_2$.

+-- {: .num_defn #EMGaugeGroupoidOverU}
###### Definition

The [[action groupoid]]

$$
  \Omega^1_{vert}(X\times U)//  C^\infty(X \times U, U(1))
  \coloneqq
  (
    \Omega^1_{vert}(X\times U) \times C^\infty(X \times U, U(1))
    \stackrel{\overset{t = \rho}{\longrightarrow}}{\underset{s = p_1}{\longrightarrow}}
    \Omega^1_{vert}(X\times U)
  )
$$

is the [[groupoid]] whose 

* [[objects]] are $U$-parameterized collections of gauge potentials $A \in \Omega^1_{vert}(X \times U)$;

* [[morphisms]] are pairs $(A,\lambda)$ with $A$ an object and $\lambda \in C^\infty(X \times U, U(1))$, with [[domain]] $A$ and [[codomain]] $A + \mathbf{d}_X \lambda$;

* [[composition]] is given by multiplication of the $\lambda$-labels in the group $C^\infty(X \times U, U(1))$.

=--

This is the discrete _gauge groupoid_ for $U$-parameterized collections of fields. It refines the _[[gauge group]]_, which is recoverd as its [[fundamental group]]:

+-- {: .num_prop }
###### Proposition

Let $A_0 \coloneqq 0 \in \Omega^1_{vert}(X \times U)$ be the trivial gauge field. Then its [[automorphism group]] in the gauge groupoid of def. \ref{EMGaugeGroupoidOverU} is the group of [[circle]]-group valued functions on $U$:

$$
  \pi_1(\Omega^1_{vert}(X\times U)// C^\infty(X \times U, U(1)), A_0)
  =
  Aut(A_0)
  \simeq
  C^\infty(U,U(1))
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition, an automorphism of $A_0$ is given by a function 
$\lambda \in C^\infty(X \times U, U(1))$ such that $A_0 = A_0 + \mathbf{d}_X \lambda$. This is the case precisely if $\mathbf{d}_X \lambda = 0$, hence if $\lambda$ is contant along $X$. But a function on $X \times U$ which is constant along $X$ is canonically identified with a function on just $U$.

=--

All this data in in fact [[natural transformation|natural]] in $U$. Recall that $\Omega^1_{vert}(X \times U) = \mathbf{\Omega}^1(X)(U)$ is the set of $U$-charts of the smooth moduli space $\mathbf{\Omega}^1(X)$ of smooth 1-forms on $X$. Similarly $C^\infty(X \times U) = \mathbf{C}^\infty(X)(U)$.

+-- {: .num_prop }
###### Proposition

There is a homomorphism of [[smooth spaces]] (def. \ref{HomomorphismOfSmoothSpaces})

$$
  \rho \colon \mathbf{\Omega}^1(X)\times \mathbf{C}^\infty(X) \to \mathbf{\Omega}^1(X)
$$

from the product smooth space, def. \ref{ProductOfSmoothSpaces}, of the smooth moduli spaces of 1-forms and 0-forms on $X$, def. \ref{SmoothSpaceOfFormsOnSmoothSpace}, to that of smooth functions, def. \ref{SmoothSpaceOfSmoothFunctions}, whose component over $U \in $ [[CartSp]] is the action 

$$
  \rho_U \colon (A,\lambda) \mapsto  A + \mathbf{d}\lambda
$$

of def. \ref{ActionOfFunctionsOnForms}.

=--

We then also want to consider a _smooth action groupoid_.

+-- {: .num_defn }
###### Definition

Write 

$$
  \mathbf{\Omega}^1(X) // \mathbf{C}^\infty(X, U(1))
  : 
  CartSp^{op}
  \to 
  Grpd
$$

for the [[contravariant functor]] from coordinate systems to the [[category]] of [[groupoids]], which assigns to $U \in CartSp$ the discrete action groupoid of $U$-collections of gauge fields of def. \ref{EMGaugeGroupoidOverU}.

$$
  U \mapsto \Omega^1_{vert}(X \times U) // C^\infty(X\times U, U(1))
  \,.
$$

=--

Such a structure _[[presheaf]]_ of [[groupoids]] is a common joint generalization of the notion of [[discrete groupoids]] and [[smooth spaces]]. We call them _[[smooth groupoids]]_. This is what we turn to in _[Smooth groupoids](#SmoothGroupoids)_


## Related concepts

* [[moduli stack]]

* [[centrally extended groupoid]]

## References

Discussion of [[diffeological groups]] (such as [[diffeomorphism groups]] and [[quantomorphism groups]]) goes back to 

* {#Souriau79} [[Jean-Marie Souriau]], _Groupes diff&#233;rentiels_, in _Differential Geometrical Methods in Mathematical Physics_ (Proc. Conf., Aix-en-Provence/Salamanca, 1979), Lecture Notes in Math. 836, Springer, Berlin, (1980), pp. 91&#8211;128. ([MathScinet](http://www.ams.org/mathscinet-getitem?mr=607688))

Exposition of the concept of smooth groupoids motivated from basic [[gauge theory]] is in 

* {#Eggersson14} [[Ragnar Eggertsson]], _[[schreiber:bachelor thesis Eggertsson|Stacks in gauge theory]]_, 2014-

Discussion of smooth stacks as [[target spaces]] for [[sigma-model]] [[quantum field theories]] is in 

* [[Tony Pantev]], [[Eric Sharpe]], _String compactifications on Calabi-Yau stacks_, Nucl.Phys. B733 (2006) 233-296, ([arXiv:hep-th/0502044](http://arxiv.org/abs/hep-th/0502044))

* [[Tony Pantev]], [[Eric Sharpe]], _Gauged linear sigma-models for gerbes (and other toric stacks)_, ([arXiv:hep-th/0502053](http://arxiv.org/abs/hep-th/0502053))
 {#PantevSharpe}

* S. Hellerman, [[Eric Sharpe]], _Sums over topological sectors and quantization of Fayet-Iliopoulos parameters_, ([arXiv:1012.5999](http://arxiv.org/abs/1012.5999))
 {#HellermanSharpe}

Discussion of [[geometric Langlands duality]] in terms of 2d sigma-models on stacks ([[moduli stacks]] of [[Higgs bundles]] over a given [[algebraic curve]]) is in 

* {#Witten08} [[Edward Witten]], section 6 of _Mirror Symmetry, Hitchin's Equations, And Langlands Duality_ ([arXiv:0802.0999](http://arxiv.org/abs/0802.0999))


[[!redirects smooth groupoids]]

[[!redirects smooth group]]
[[!redirects smooth groups]]

[[!redirects smooth stack]]
[[!redirects smooth stacks]]

[[!redirects SmoothGrpd]]