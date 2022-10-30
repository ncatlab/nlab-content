
> This entry contains one chapter of the material at _[[geometry of physics]]_.

> previous chapters: _[[geometry of physics -- groups|groups]]_. _[[geometry of physics -- smooth homotopy types|smooth homotopy type]]_

> next chapter: _[[geometry of physics -- manifolds and orbifolds]]_

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## **Principal bundles**
 {#PrincipalBundles}
 {#PrincipalNBundles}


### Model Layer

#### Principal bundles via Smooth groupoids
 {#PrincipalBundlesViaSmoothGroupoids}

For $G$ a [[Lie group]], we discuss $G$-[[principal bundles]] over a [[smooth manifold]] $X$ as a natural construction in the context of [[smooth groupoids]].

##### Review of Cech 1-cocycles as morphisms of smooth groupoids

Recall the discussion of [[Cech cohomology]] in degree 1 from _[[geometry of physics -- smooth homotopy types]]_.

Let $G$ be a [[Lie group]] and $X$ a [[smooth manifold]] (all our smooth manifolds are assumed to be finite dimensional and [[paracompact space|paracompact]]). 

From the group $G$ we canonically obtain a [[groupoid]] that we write $\mathbf{B}G$ and call the [[delooping]] groupoid of $G$. Formally this groupoid is

$$
  \mathbf{B}G = (G \stackrel{\longrightarrow}{\longrightarrow} *)
$$

with composition induced from the product in $G$. A useful cartoon of this groupoid is

$$
  \mathbf{B}G = 
  \left\{
    \array{
      && \bullet
      \\
      & {}^{\mathllap{g_1}}\nearrow 
      &=& 
      \searrow^{\mathrlap{g_2}}
      \\
      \bullet &&\stackrel{g_2 \cdot g_1 }{\longrightarrow}&& \bullet
    }
  \right\}
$$

where the $g_i \in G$ are elements in the group, and the bottom morphism is labeled by forming the product in the group. (The order of the factors here is a convention whose choice, once and for all, does not matter up to equivalence.)

But we get a bit more, even. Since $G$ is a [[Lie group]], there is smooth structure on $\mathbf{B}G$  that makes it a [[Lie groupoid]], an [[internal groupoid]] in the [[category]] [[Diff]] of [[smooth manifold]]s: its collections of objects (trivially) and of morphisms each form a smooth manifold, and all structure maps (source, target, identity, composition) are [[smooth function]]s. We shall write

$$
  \mathbf{B}G \in LieGrpd
$$

for $\mathbf{B}G$ regarded as equipped with this smooth structure. Here and in the following the boldface is to indicate that we have an object equipped with a bit more structure -- here: smooth structure -- than present on the object denoted by the same symbols, but without the boldface. Eventually we will make this precise by having the boldface symbols denote objects in the [[(∞,1)-topos]] [[Smooth∞Grpd]] which are taken by [[forgetful functor]]s to objects in [[∞Grpd]] denoted by the corresponding non-boldface symbols.[^TwoForgetful]

[^TwoForgetful]: There are actually two such forgetful functors, $\Gamma$ and $\Pi$. The first sends $\mathbf{B}G$ to $B G_{disc}$, which in [[topology]] is known as $K(G,1)$. The other sends $\mathbf{B}G$ to the [[classifying space]] $B G$. (see <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#GeometricRealization">∞-Lie groupoid -- geometric realization</a>). This distinction is effectively the origin of differential cohomology.

Also the smooth manifold $X$ may be regarded as a [[Lie groupoid]] -- a groupoid with only identity morphisms. Its cartoon description is simply

$$
  X = \{x \stackrel{id}{\longrightarrow} x \}
  \,.
$$

But there are other groupoids associated with $X$:

Let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. To this is canonically associated the [[Cech groupoid]] $C(\{U_i\})$. Formally we may write this groupoid as

$$
  C(\{U_i\})
  =
  \left(
    \coprod_{i,j} U_i \cap U_j
    \stackrel{\overset{p_1}{\longrightarrow}}{\underset{p_2}{\longrightarrow}}
    \coprod_i U_i
  \right)
  \,.
$$

A useful cartoon description of this groupoid is

$$
  C(\{U_i\})
  = 
  \left\{
    \array{
       && (x,j)
       \\
       & \nearrow &=& \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
  \right\}
  \,.
$$

This indicates that the objects of this groupoid are pairs $(x,i)$ consisting of a point $x \in X$ and a patch $U_i \subset X$ that contains $x$, and a morphism is a triple $(x,i,j)$ consisting of a point and _two_ patches, that both contain the point, in that $x \in U_i \cap U_j$. The triangle in the above cartoon symbolizes the evident way in which these morphisms compose. All this inherits a smooth structure from the fact that the $U_i$ are smooth manifolds and the inclusions $U_i \to X$ are [[smooth function]]s. 
hence also $C(U)$ becomes a [[Lie groupoid]].

There is a canonical [[functor]]

$$
  C(\{U_i\}) \to X \;\; :\;\; (x,i) \mapsto x
  \,.
$$

This functor is an [[internal functor]] in [[Diff]] and moreover it is evidently [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]]. 

However, while 
essential surjectivity and full-and-faithfulness implies that the underlying bare functor has a homotopy-inverse, that homotopy-inverse never 
has itself smooth component maps, unless $X$ itself is a Cartesian space and the chosen cover is trivial.

We do however want to think of $C(\{U_i\})$ as being equivalent to $X$ even as a Lie groupoid. 
One says that a smooth functor whose underlying bare functor is an equivalence of groupoids is
a _weak equivalence_ of Lie groupoids, which we write as 
$C(\{U_i\}) \stackrel{\simeq}{\to} X$.
Moreover, we shall think of $C(U)$ as a _good_ equivalent replacement of $X$ if it comes from a cover that is in fact a [[good open cover]] in that all its non-empty finite intersections $U_{i_0 \cdots i_k} := U_{i_0} \cap \cdots \cap U_{i_k}$ are [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^{dim X}$. 

We shall discuss later in which precise sense this condition makes $C(U)$ _good_ in the sense that smooth functors out of $C(U)$ model the correct notion of morphism out of $X$ in the context of smooth groupoids (namely it will mean that $C(U)$ is cofibrant in a suitable [[model category]] structure on the category of Lie groupoids). The formalization of this statement is what [[(∞,1)-topos]] theory is all about, to which we will come. For the moment we shall be content with accepting this as an ad hoc statement.

Observe that a [[functor]]

$$
  g : C(U) \to \mathbf{B}G
$$

is given in components precisely by a collection of functions

$$
  \{g_{i j} : U_{i j} \to G \}_{i,j \in I}
$$

such that on each $U_i \cap U_k \cap U_j$ the equality $g_{j k} g_{i j}  = g_{i k}$ of [[smooth function]]s holds:

$$
  \left(
    \array{
       && (x,j)
       \\
       & \nearrow && \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
  \right)
  \mapsto
  \left(
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_{i j}(x)}}\nearrow
       && \searrow^{\mathrlap{g_{j k}(x)}}
       \\
      \bullet &&\stackrel{g_{i k}(x)}{\to}&& \bullet
    }
  \right)
  \,.
$$

It is well known that such collections of functions characterize $G$-[[principal bundle]]s on $X$. While this is a classical fact, we shall now describe a way to derive it that is true to the Lie-groupoid-context and that will make clear how smooth principal $\infty$-bundles work.

First observe that in total we have discussed so far [[span]]s of smooth functors of the form

$$
  \array{
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

Such spans of functors, whose left leg is a weak equivalence, are sometimes known, essentially equivalently, as [[Morita morphism]]s or _generalized morphisms_ of Lie groupoids, as [[Hilsum-Skandalis morphism]]s or groupoid [[bibundle]]s, or as [[anafunctor]]s. We are to think of these as concrete _models_ for more intrinsically defined direct morphisms $X\to \mathbf{B}G$ in the $(\infty,1)$-topos of $\infty$-Lie groupoids. 

##### The universal $G$-principal bundle

There is another Lie groupoid canonically associated with $G$. 

+-- {: .num_defn #EGAsASmoothGroupoid}
###### Definition

For $G$ a [[Lie group]], write $\mathbf{E}G$ for the [[action groupoid]] of $G$ acting on itself from the right, hence for the [[Lie groupoid]] 

$$
  \mathbf{E}G  
  \coloneqq
  \left(
    G \times G \stackrel{\overset{(-)\cdot (-)}{\longrightarrow}}{\underset{p_1}{\longrightarrow}} G 
  \right)
$$

whose manifold of objects is $G$, whose manifold of morphisms is $G \times G$, whose source-map is projection on the first factor, whose target map is multiplication in the group, whose identity-map is $g\mapsto (g,e)$ and whose composition operation is

$$
  (g_1 g, h) \circ (g_1,g) \coloneqq (g_1, g h)
  \,.
$$



=--

+-- {: .num_remark}
###### Remark

The groupoid $\mathbf{E}G$ of def. \ref{EGAsASmoothGroupoid} has at most one morphism for every ordered pair of objects, hence the morphisms are uniquely identified by giving their source and target.

Schematically:

$$
  \mathbf{E}G
  = 
  \left\{
     \array{
        && g_2
        \\
        & {}^{\mathllap{g_1^{-1} g_2}}\nearrow &=& \searrow^{\mathrlap{g_2^{-1}g_3 }}
        \\
        g_1 &&\stackrel{ g_1^{-1}g_3}{\longrightarrow}&& g_3
     }
  \right\}
$$

or simply

$$
  \mathbf{E}G
  = 
  \left\{
     \array{
        && g_2
        \\
        & {}^{\mathllap{}}\nearrow &=& \searrow^{\mathrlap{}}
        \\
        g_1 &&\stackrel{ }{\longrightarrow}&& g_3
     }
  \right\}
  \,.
$$

=--

While therefore $\mathbf{E}G$ is a rather simplistic object, it is nevertheless worthwhile to make its following properties explicit.

+-- {: .num_prop #GActionOnEGForLieGroups}
###### Proposition

There is an evident morphism of smooth groupoids 

$$
  p\colon \mathbf{E}G \to \mathbf{B}G
$$

given by

$$
  (g_1, g) \mapsto g
$$

hence 

$$
  (g_1 \to g_2) \mapsto (\bullet \stackrel{g_1^{-1}g_2 }{\to} \bullet)
$$

There is an evident $G$-[[action]]

$$
  (\mathbf{E}G) \times G \longrightarrow G
$$

given by

$$
  ((g_1,g_2), h) \mapsto (g_1 h, g_2 h)
  \,.
$$

The projection $p$ is the [[quotient]] [[projection]] of this action.

=--

+-- {: .num_defn #FibrationOfSmoothGroupoids}
###### Definition

A morphism $p\colon E \to B$ of [[smooth groupoids]] is called a _[[fibration]]_ if for each $n\in \mathbb{N}$ the [[functor]] $p(\mathbb{R}^n) \colon E(\mathbb{R}^n)\to B(\mathbb{R}^n)$ is an [[isofibration]], hence if for each object $e \in E(\mathbb{R}^n)$, each morphism $p(e) \to b$ in $B(\mathbb{R}^n)$ has a lift through $p$ to a morphism $e \to e'$ in $E$:

$$
  \array{
    e &\stackrel{\exists \psi \in p^{-1}(\phi)}{\to} & \exists e'&&& E 
    \\
     &&&&&  \downarrow^p
    \\
    p(e) &\stackrel{\phi}{\to} & b &&& B
  }
  \,.
$$

=--

+-- {: .num_prop #EGForLieGroupIsFibrantReplacementOfPointInclusion}
###### Proposition

The projection $p \colon \mathbf{E}G \to \mathbf{B}G$ of prop. \ref{GActionOnEGForLieGroups} is a fibration of smooth groupoids, def. \ref{FibrationOfSmoothGroupoids}. Moreover, any point inclusion $\ast \longrightarrow \mathbf{E}G$ is over each $\mathbb{R}^n$ an [[equivalence of groupoids]], hence is in particular a local weak equivalence of smooth groupoids (as defined [here](geometry+of+physics+--+smooth+homotopy+types#LocalWeakEquivalence)).

In summary, the morphisms $\ast \to \mathbf{E}G \stackrel{p}{\to} \mathbf{B}G$ constitute a factorization of the canonical $\ast \to \mathbf{B}G$ into a local weak equivalence followed by a fibration.

=--


+-- {: .num_prop}
###### Proposition

The smooth groupoid $\mathbf{E}G$ of def. \ref{EGAsASmoothGroupoid} has the following equivalent incarnations as pre-smooth groupoids by [[isomorphism|isomorphic]] Lie groupoids


1. $\mathbf{E}G \simeq G//G$ is the [[action groupoid]] of $G$ acting on itself by right multiplication;

1. $\mathbf{E}G \simeq (\mathbf{B}G)^{I} \underset{\mathbf{B}G}{\times} \ast$ is the [[pullback]] of the point inclusion $\ast \to \mathbf{B}G$ along one of the projection map $d_1 \colon (\mathbf{B}G)^I \longrightarrow \mathbf{B}G$ out of the [[path space object]] of $\mathbf{B}G$.

=--

+-- {: .proof}
###### Proof

The first statement is immediate from the definitions. The second is also fairly immediate, but worth making explicit: the Lie groupoid $(\mathbf{B}G)^I$ has as objects the morphisms in $\mathbf{B}G$, hence elements of $G$, and as morphisms $g_1 \to g_2$ commuting squares between these, schematically:

$$
  (\mathbf{B}G)^I
  =
  \left\{
    \array{
      \bullet &\stackrel{h_1}{\longrightarrow}& \bullet
      \\
      {}^{\mathllap{g_1}}\downarrow && \downarrow^{\mathrlap{g_2}}
      \\
      \bullet &\stackrel{h_2}{\longrightarrow}& \bullet
    }
  \right\}
  \,.
$$

The morphism $d_1$ projects out the top horizontal morophisms:

$$
  d_1
  \;\colon\;
   \left(
    \array{
      \bullet &\stackrel{h_1}{\longrightarrow}& \bullet
      \\
      {}^{\mathllap{g_1}}\downarrow && \downarrow^{\mathrlap{g_2}}
      \\
      \bullet &\stackrel{h_2}{\longrightarrow}& \bullet
    }
  \right)
  \;\;
  \mapsto
  \;\;
   \left(
    \array{
      \bullet &\stackrel{h_1}{\longrightarrow}& \bullet
    }
  \right)  
  \,.
$$

The pullback then restricts this image to be constant and hence produces the groupoid whose objects are still the morphisms in $\mathbf{B}G$, hence elements of $G$, but whose morphisms are no longer all commuting squares, but just all commuting triangles between these, schematically:

$$
  (\mathbf{B}G)^I \underset{\mathbf{B}G}{\times} \ast
  =
  \left\{
    \array{
      && \bullet
      \\
      & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
      \\
      \bullet && \stackrel{h}{\longrightarrow} && \bullet
    }
  \right\}
  \,.
$$

Such a triangle exists precisely if $g_2 = g_1 h$, which gives 
$\mathbf{E}G$ as in def. \ref{EGAsASmoothGroupoid}.

=--


##### $G$-Principal bundles

The traditional construction of the $G$-principal bundle associated to a [[Cech cohomology|Cech cocycle]] is the following.

+-- {: .num_defn #TraditionalConstructionOfGBundleFormCocycle}
###### Definition

Let $X$ be a [[smooth manifold]], $\{U_i \to X\}_I$ an [[open cover]] and $(g_{i j})_{i,j \in I}$ a [[Cech cohomology|Cech cocycle]] of degree 1 with values in $G$. Then the [[bundle]] $P \to X$ associated with this data is the [[quotient]]

$$
  P \coloneqq \left( \coprod_{i} U_i \times G \right)/{\sim}
$$

of the [[Cartesian product]] of the [[cover]] (regarded as the [[disjoint union]] of its patches) with $G$, by the [[equivalence relation]] which identifies two elements in the product whenever they are related by the Cech cocycle:

$$
  ((x,i),g) \sim ((x,j), g \cdot g_{i j}(x))
  \,.
$$

=--

+-- {: .num_prop #GBundleAsPullbackAlongCechCocycle}
###### Proposition

Let $X$ be a [[smooth manifold]], $\{U_i \to X\}_I$ an [[open cover]] and $(g_{i j})_{i,j \in I}$ a [[Cech cohomology|Cech cocycle]] of degree 1 with values in $G$. Then the associated $G$-bundle $P$, def. \ref{TraditionalConstructionOfGBundleFormCocycle}, is equivalent, as a [[smooth groupoid]], to the [[pullback]] of the morphism $\mathbf{E}G\to \mathbf{B}G$ of def. \ref{EGAsASmoothGroupoid} along the cocycle regarded as a
homomorphism of [[smooth groupoids]] $C(\{U_i\}) \stackrel{g}{\longrightarrow} \mathbf{B}G$.

$$
  \array{
     P &\overset{\simeq}{\longleftarrow}& C(\{U_i\})\underset{\mathbf{B}G}{\times} \mathbf{E}G &\longrightarrow& \mathbf{E}G
     \\
     \downarrow && \downarrow && \downarrow
     \\
     && C(\{U_i\}) &\stackrel{g}{\longrightarrow}& \mathbf{B}G
     \\
     &\searrow & \downarrow^{\mathrlap{\simeq}}
     \\
     && X
  }
$$

=--

+-- {: .proof}
###### Proof

Pullbacks of smooth groupoids are computed componentwise. Hence a morphism in $C(\{U_i\})\underset{\mathbf{B}G}{\times} \mathbf{E}G$ is a pair consisting of a morphism $(x,i,j)$ in $C(\{U_i\})$ and a morphism $(g_1, h)$ in $\mathbf{E}G$ such that $h$ is the value of the cocycle on $(x,i,j)$.

This means that the morphisms in the pullback are of the form

$$
  \array{
     ((x,i),g_1) &&\stackrel{\simeq}{\to}&& ((x,j), g_1 g_{i j}(x) )
  }
$$

and there is at most one for any ordered pair of objects. But this means that these morphisms represent precisely the [[equivalence relation]] of def. \ref{TraditionalConstructionOfGBundleFormCocycle}: the evident projection map from this pullback to $P$ (with $P$ regarded as a groupoid with only identity morphisms) is evidently [[essentially surjective functor|essentially surjective]] and [[fully faithful functor|fully faithful]], hence an equivalence.

=--

+-- {: .num_remark}
###### Remark

By the pullback construction in prop. \ref{GBundleAsPullbackAlongCechCocycle}, 
$P$ inherits a $G$-action from 
that on $\mathbf{E}G$ of def. \ref{GActionOnEGForLieGroups}:

via the [[pasting]] diagram of pullbacks

$$
  \array{
     \tilde P \times G &\to& \mathbf{E}G \times G
     \\
     \downarrow && \downarrow
     \\
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

The morphism $\tilde P \times G \to \tilde P$ exhibits the principal $G$-[[action]] of $G$ on $\tilde P$.

=--





#### Fibration categories and the Factorization lemma

We saw [above](#PrincipalBundlesViaSmoothGroupoids) that smooth $G$-[[principal bundles]] for $G$ a [[Lie group]] may naturally be understood in terms of pullbacks of the fibrant replacement $\mathbf{E}G\to \mathbf{B}G$ of the point inclusion $\ast \to \mathbf{B}G$ along a Cech cocycle, regarded as a homomorphism of smooth groupoids. 

This is a special case of a very general construction of [[homotopy pullbacks]] which will also apply, below, to [weakly principal simplicial bundles](#WeakyPrincipalSimplicialBundles) and then generally to [[principal infinity-bundles]]. We now discuss the general axiomatization of this construction via [[categories of fibrant objects]].


##### Categories of Fibrant objects

+-- {: .num_defn #CategoryOfFibrantObjects}
###### Definition

A **[[category of fibrant objects]]** $\mathcal{C}$ is 

* a [[category with weak equivalences]], i.e equipped with a subcategory $W$ that contains all [[isomorphisms]]

  $$
    Core(\mathcal{C}) \hookrightarrow W \hookrightarrow \mathcal{C}
    \,,
  $$

  where $f \in Mor(W)$ is called a **weak equivalence**;

* equipped with a further subcategory 

  $$
    Core(\mathcal{C}) \hookrightarrow F \hookrightarrow \mathcal{C}
    \,,
  $$

  where $f \in Mor(F)$ is called a **fibration**

  Those morphisms which are both weak equivalences and fibrations are called **acyclic fibrations** .

This data has to satisfy the following properties:

* $\mathcal{C}$ has [[finite products]], and in particular a [[terminal object]] ${\ast}$;

* the [[pullback]] of a fibration along an arbitrary morphism exists, and is again a fibration;

* acyclic fibrations are preserved under [[pullback]];

* weak equivalences satisfy [[category with weak equivalences|2-out-of-3]];

* for every object there exists a [[path object]]

  * this means: for every object $B$ there exists at least one object denoted $B^I$ (not necessarily but possibly the [[internal hom]] with an [[interval object]]) that fits into a diagram

  $$
    (B \stackrel{Id \times Id}{\to} B \times B)
    =
    (B \stackrel{\sigma}{\to} B^I \stackrel{d_0 \times d_1}{\to} B \times B)
  $$

  where $\sigma$ is a weak equivalence and $d_0 \times d_1$ is a fibration;

* all objects are _fibrant_, i.e. all morphisms $B \to {\ast}$ to the terminal object are fibrations.

=--

+-- {: .num_prop #PreSmoothGroupoidsFormCategoryOfFibrantObjects}
###### Proposition

The category of pre-smooth groupoids ([here](geometry%20of%20physics%20--%20smooth%20homotopy%20types#PreSmoothGroupoids)) becomes a category of fibrant objects, def. \ref{CategoryOfFibrantObjects} with fibrations as in def. \ref{FibrationOfSmoothGroupoids} and weak equivalences the local weak equivalences (as defined [here](geometry+of+physics+--+smooth+homotopy+types#LocalWeakEquivalence)).

=--


##### Factorization lemma

Let $C$ be a [[category of fibrant objects]].  The _[[factorization lemma]]_ says the following.

+-- {: .num_lemma #FactorizationLemma}
###### Lemma

Every [[morphism]] $f : X \to Y$ in $C$ factors as

$$
  f : X \underoverset{\simeq}{i}{\longrightarrow} \hat X \stackrel{p}{\longrightarrow} Y
  \,,
$$

where 

1. $i$ is a weak equivalence (even a [[right inverse]] to an acyclic fibration);

1. $p$ is a [[fibration]].

=--

+-- {: .proof}
###### Proof

Let $Y^I$ with factorization $Y \stackrel{\simeq}{\to} Y^I \stackrel{(d_0,d_1)}{\longrightarrow} Y \times Y$ be a [[path space object]] for $Y$. Let $\hat X \coloneqq Y^I \times_Y X$ be the [[pullback]] of $f$ along one of its legs, to get the diagram

$$
  \array{
     \hat X &\to& X
     \\
     \downarrow && \downarrow^{\mathrlap{f}}
     \\
     Y^I &\stackrel{d_1}{\to}& Y
     \\
     \downarrow^{\mathrlap{d_0}}
     \\
     Y
  }
  \,.
$$

Take $p$ to be the composite vertical morphism in the above diagram, hence

$$
  p \;\colon\; \hat X \to Y^I \stackrel{d_0}{\to} Y
  \,.
$$

To see that this is indeed a fibration, notice that, by the [[pasting law]], the above pullback diagram
can be refined to a double pullback diagram as follows

$$
  \array{
    \hat X
     &\stackrel{}{\to}& 
     X \times Y 
     &\stackrel{p_1}{\to}& 
     X
     \\
     \downarrow && \downarrow^{\mathrlap{(f, Id)}} && \downarrow^\mathrlap{f}
     \\
     Y^I &\stackrel{(d_1 , d_0) }{\to}&
     Y \times Y &\stackrel{p_1}{\to}&
     Y
     \\
     \downarrow^{\mathrlap{d_0}} & \swarrow_{p_2}
     \\
     Y
  }
  \,.
$$

Both squares are pullback squares. Since
pullbacks of fibrations are fibrations, the morphism
$\hat X  \to X \times Y$ is a fibration.
Similarly, since $X$ is assumed to be fibrant (as all objects in a [[category of fibrant objects]]), also the [[projection]] map $X \times Y \to Y$ is a fibration (see [here](category+of+fibrant+objects#SimpleConsequences)). 

Since $p$ is thereby exhibited as the composite of two fibrations

$$
  \begin{aligned}
    p &: \hat X \to X \times Y
    \stackrel{(f ,Id)}{\to}
    Y \times Y
    \stackrel{p_2}{\to}
    Y
  \end{aligned}
  \,,
$$

(the first map being a pullback of a fibration as above, the composite of the second and the third map being the projection just menioned) it is itself a fibration.


Next, by the [[axioms]] of [[path space objects]] in a [[category of fibrant objects]] we have that $d_1 \;\colon\; Y^I \to Y$ is an acyclic fibration. Since these are stable under pullback, also $\hat X \to X$ is an acyclic fibration.

But, by the axioms, $Y^I \to Y$ has a right inverse $Y \to Y^I$. By the [[pullback]] property this induces a right inverse of $\hat X \to X$ fitting into a [[pasting]] diagram

$$
  \array{
     X &\to& \hat X &\to& X
     \\
     {}^{\mathrlap{f}}\downarrow && \downarrow && \downarrow^{\mathrlap{f}}
     \\
     Y &\to& Y^I &\stackrel{d_1}{\to}& Y
     \\
     & {}_{\mathllap{Id}}\searrow& \downarrow^{\mathrlap{d_0}} 
     \\
     && Y
  }
  \,.
$$

This establishes the claim.

=--

##### Homotopy and Homotopy pullback

Let $\mathcal{C}$ be a [[category of fibrant objects]].

+-- {: .num_defn}
###### Definition

Two morphism $f,g : A \to B$ in $\mathcal{C}(A,B)$ are 

* **right [[homotopy|homotopic]]**, denoted $f \simeq g$, precisely if they fit into a diagram of the form

  $$
    \array{
      && B
      \\
      & {}^f\nearrow & \uparrow^{d_0}
      \\
      A &\stackrel{\eta}{\to}&
      B^I
      \\
      & {}_g\searrow & \downarrow^{\mathrlap{d_1}}
      \\
      && B
    }
  $$ 

  for some [[path object|path space object]] $B^I$;

* **[[homotopy|homotopic]]**, denoted $f \sim g$,
  if they become right homotopic after pulled back
  to a weakly equivalent domain, 
  i.e. precisely if they fit into a diagram of the form

$$
  \array{
    &&
    A 
    &\stackrel{f}{\to}& B
    \\
    &{}^{w \in W}\nearrow&&& \uparrow^{d_0}
    \\
    \hat A 
    &&
    \stackrel{\eta}{\to}
    &&
    B^I
    \\
    &{}_{w\in W}\searrow & &&
    \downarrow^{d_1}
    \\
    &&
    A
    &\stackrel{g}{\to}& 
    B
  }
$$

for some object $\hat A$ and
for some [[path object|path space object]] $B^I$ of $I$

=--

In view of this the following definition is natural.

+-- {: .num_defn #HomotopyFiberProducts}
###### Definition

A **homotopy fiber product** 
or **homotopy pullback** of two morphisms

$$
  A \stackrel{u}{\to} C \stackrel{v}{\leftarrow} B
$$

in a category of fibrant objects
is the object $A \times_C C^I \times_C B$  defined as the 
(ordinary) [[nLab:limit|limit]]

$$
  \array{
    A \times_C C^I \times_C B &\longrightarrow& &\longrightarrow & B
    \\
    \downarrow &&&& \downarrow^v
    \\
    & &C^I & \stackrel{d_0}{\to}& C
    \\
    \downarrow &&
    \downarrow^{\mathrlap{d_1}}
    \\
    A &\stackrel{u}{\to} & C    
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The homotopy fiber product in def. \ref{HomotopyFiberProducts} is [[isomorphism|isomorphic]] to the ordinary [[fiber product]] of either of the two morphisms with the fibration replacement of the other as given by the factorization lemma, def. \ref{FactorizationLemma}.

=--

+-- {: .proof}
###### Proof

By basic properties of [[limits]] the defining limit in def. \ref{HomotopyFiberProducts} may be computed by two consecutive pullbacks.

$$
  \array{
    A \times_C C^I \times_C B \simeq & A \underset{C}{\times} \left(C^I \underset{C}{\times} B\right)  &\to& C^I \underset{C}{\times} B &\to 
    & B
    \\
    & \downarrow && \downarrow && \downarrow^{\mathrlap{v}}
    \\
    & & &C^I & \stackrel{d_0}{\to}& C
    \\
    & \downarrow &&
    \downarrow^{\mathrlap{d_1}}
    \\
    & A &\stackrel{u}{\to}& C    
  }
  \,.
$$

Here the intermediate pullback is precisely the one appearing in the proof of the factorization lemma.


=--

+-- {: .num_example}
###### Example

With $\mathcal{C}$ the category of fibrant objects given by pre-smooth groupoids, prop. \ref{PreSmoothGroupoidsFormCategoryOfFibrantObjects}, then for $G$ a Lie group, the factorization $\ast \to \mathbf{E}G \stackrel{p}{\to} \mathbf{B}G$ of prop. \ref{EGForLieGroupIsFibrantReplacementOfPointInclusion} is the one given by the [[factorization lemma]]. Hence a pullback of $p \colon \mathbf{E}G\to \mathbf{B}G$ as in prop. \ref{GBundleAsPullbackAlongCechCocycle} is equivalently the homotopy pullback of $\ast \to \mathbf{B}G$.


=--

#### Weakly principal simplicial bundles
 {#WeakyPrincipalSimplicialBundles}

(... under construction ...)

It is no coincidence that the above statement looks akin to the maybe more familiar statement which says that _equivalence classes_ of $G$-principal bundles are classified by [[homotopy]]-classes of morphisms of [[topological space]]s 

$$
  \pi_0 Top(X, \mathbf{B}G)
  \simeq
  \pi_0 G Bund(X)
  \,,
$$

where $\mathbf{B}G \in $ [[Top]] is the topological [[classifying space]] of $G$. The category [[Top]] of topological spaces, regarded as an [[(∞,1)-category]], is the archetypical [[(∞,1)-topos]] the way that [[Set]] is the archetypical [[topos]]. And it is equivalent to [[∞Grpd]], the $(\infty,1)$-category of bare [[∞-groupoid]]s. What we are seeing above is a first indication of how [[cohomology]] of bare $\infty$-groupoids is lifted to a richer $(\infty,1)$-topos to cohomology of $\infty$-groupoids with extra structure.

In fact, all of the statements that we have considered so far become conceptually _simpler_ in the $(\infty,1)$-topos. We had already remarked that the [[anafunctor]] span $X \stackrel{\simeq}{\leftarrow} C(U) \stackrel{g}{\to} \mathbf{B}G$ is really a model for what is simply a direct morphism $X \to \mathbf{B}G$ in the $(\infty,1)$-topos. But more is true: that pullback of $\mathbf{E}G$ which we considered is just a model for the [[homotopy pullback]] of just the _point_ 


$$
  \array{
     \vdots && \vdots
     \\
     \tilde P \times G &\to& \mathbf{E}G \times G
     \\
     \downarrow && \downarrow
     \\
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
     \\
     {}
     \\
     {}
     \\
     & in\;the\;model\;category &
  }
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \array{
     \vdots && \vdots
     \\
     P \times G &\to& G
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow
     \\
     P &\to& * 
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow 
     \\
     X &\stackrel{}{\to}& \mathbf{B}G
     \\
     .
     \\
     .
     \\
     \\
     \\
     & in\;the\;(\infty,1)-topos
  }
  \,.
$$



##### Universal principal bundle

* [[groupal model for universal principal infinity-bundles]]



##### Weakly principal simplicial bundles

The [[principal ∞-bundles]] that we wish to model are already the main and simplest example of the application of these three items: 

Consider an object $\mathbf{B}G \in [C^{op}, sSet]$ which is an $\infty$-groupoid with a single object, so that we may think of it as the [[delooping]] of an [[∞-group]] $G$, let $*$ be the point and $* \to \mathbf{B}G$ the unique inclusion map. The _good replacement_ of this inclusion morphism is the $G$-[[universal principal ∞-bundle]] $\mathbf{E}G \to \mathbf{B}G$ given by the pullback diagram
  
$$
  \array{ 
    \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G^{\Delta[1]} &\to& \mathbf{B}G
    \\
    \downarrow
    \\
     \mathbf{B}G
   }
$$

An [[∞-anafunctor]] $X \stackrel{\simeq}{\leftarrow} \hat X \to \mathbf{B}G$ we call a [[cocycle]] on $X$ with coefficients in $G$, and the [[(∞,1)-pullback]] $P$ of the point along this cocycle, which by the above discussion is the ordinary [[limit]]


$$
  \array{ 
    P &\to& \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    && \mathbf{B}G^I &\to& \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

we call the [[principal ∞-bundle]] $P \to X$ classified by the cocycle.

It is now evident that our discussion of ordinary smooth principal bundles [above](#PrincipalBundles) is the special case of this for $\mathbf{B}G$ the [[nerve]] of the one-object groupoid associated with the ordinary [[Lie group]] $G$.

So we find the complete generalization of the situation that we already indicated there, which is summarized in the following diagram:

$$
  \array{
     \vdots && \vdots
     \\
     \tilde P \times G &\to& \mathbf{E}G \times G
     \\
     \downarrow && \downarrow
     \\
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
     \\
     {}
     \\
     {}
     \\
     & in\;the\;model\;category &
  }
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \array{
     \vdots && \vdots
     \\
     P \times G &\to& G
     \\
     \downarrow && \downarrow
     \\
     P &\to& * 
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow 
     \\
     X &\stackrel{}{\to}& \mathbf{B}G
     \\
     .
     \\
     .
     \\
     \\
     \\
     & in\;the\;(\infty,1)-topos
  }
  \,.
$$


* [[simplicial principal bundle]]



### Semantic Layer

#### Principal $\infty$-bundles

* [[homotopy fiber]]

* [[homotopy colimit]]

* [[principal infinity-bundle]]

### Syntactic Layer

* [[connected type]]

## References

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_