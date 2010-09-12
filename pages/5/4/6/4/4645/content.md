[[!redirects infinity-Chern-Weil theory -- preparatory concepts]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--


> This is a subentry of [[∞-Chern-Weil theory]]. While there the general theory is discussed, this entry here considers some basic constructions in the traditional language of [[differential geometry]] that connect explicitly to basic concepts of ordinary [[Chern-Weil theory]].


#Contents#
* table of contents
{:toc}

## Idea

Ordinary [[Chern-Weil theory]] studies [[connection on a bundle|connections]] on $G$-[[principal bundle]]s over a [[Lie group]] $G$. In [[(∞,1)-category theory]] these generalize to connections on [[principal ∞-bundle]]s over [[∞-Lie group]]s $G$. $\infty$-Chern-Weil theory deals with these higher connections and their relation to [[ordinary differential cohomology]].

Here we describe some introducory basics of the general theory in concrete terms.



## Preparatory concepts

Two simple special cases of general $\infty$-Chern-Weil theory are obtained by

1. restricting attention to _low categorical degree_ , 

   studying [[principal bundle|principal 1-bundle]]s, [[principal 2-bundle]]s and maybe 3-bundles; in terms of [[groupoid]]s, [[2-groupoid]]s and maybe [[3-groupoid]]s;

1. restricting attention to _infinitesimal aspects_ 

   studying not [[∞-Lie groupoid]]s but just their [[∞-Lie algebroid]]s. In terms of this it is easy to raise categorical degree to $n = \infty$, but this misses various global [[cohomology|cohomological]] effects (very similar to how [[rational homotopy theory]] deswcribes just non-torsion phenomena of genuine [[homotopy theory]]).

These are the special cases that this introduction concentrates on.

We start by describing 

* [Smooth principal n-bundles](#PrincipalNBundles)

for low $n$ in detail, connecting them to standard theory, but presenting everything in such as way as to allow straightforward generalization to the full discussion of [[principal ∞-bundle]]s.

Then in the same spirit we discuss

* [Connections on principal n-bundles](#LowDimension)

for low $n$ in a fashion that connects to the ordinary notion of [[parallel transport]] and points the way to the fully-fledged formulation in terms of the [[schreiber:path ∞-groupoid]] functor.

This leads to differential-form expressions that we shall then finally reformulate in terms of 

* [∞-Lie algebra valued connections](#LieConnections).

We end by indicating how under [[Lie integration]] this lifts to the full [[∞-Chern-Weil theory]].



### Principal $n$-bundles in low dimension {#PrincipalNBundles}

#### Ordinary smooth principal bundles {#PrincipalBundles}

Let $G$ be a [[Lie group]] and $X$ a [[smooth manifold]] (all our smooth manifolds are assumed to be finite dimensional and [[nLab:paracompact space|paracompact]]). 

We give a discussion of smooth $G$-[[principal bundle]]s on $X$ in a manner that paves the way to a straightforward generalizatoin to a description of [[principal ∞-bundle]]s.

The first observation is that from $X$ and $G$ we naturally obtain the following [[groupoid]]s.

From the group $G$ we canonically obtain a [[groupoid]] that we write $\mathcal{B}G$ and call the [[delooping]] groupoid of $G$. Formally this groupoid is

$$
  \mathcal{B}G = (G \stackrel{\to}{\to} *)
$$

with composition canonically induced from the product in $G$. A useful cartoon of this groupoid is

$$
  \mathcal{B}G = 
  \left\{
    \array{
      && \bullet
      \\
      & {}^{\mathllap{g_1}}\nearrow 
      &=& 
      \searrow^{\mathrlap{g_2}}
      \\
      \bullet &&\stackrel{g_2 \cdot g_1 }{\to}&& \bullet
    }
  \right\}
$$

where the $g_i \in G$ are elements in the group, and the bottom morphism is labeled by forming the product in the group. (The order of the factors here is a convention that does not matter up to equivalence.)

But we get a bit more, even. Since $G$ is a [[Lie group]], there is smooth structure on $\mathcal{B}G$  that makes it a a [[Lie groupoid]], an [[internal groupoid]] in the [[category]] [[Diff]] of [[smooth manifold]]s: its collections of objects (trivially) and of morphisms each form a smooth manifold, and all structure maps (source, target, identity, composition) are [[smooth function]]s. We shall write

$$
  \mathbf{B}G \in LieGrpd
$$

for $\mathcal{B}G$ regarded as equipped with this smooth structure. Here and in the following the boldface is to indicate that we have an object equipped with a bit more structure -- here: smooth structure -- than present on the object denoted by the same symbols, but without the boldface. Eventually we will make this precise by having the boldface symbols denote objects in the [[(∞,1)-topos]] [[?LieGrpd]] which are taken by [[forgetful functor]]s to objects in [[∞Grpd]] denoted by the corresponding non-boldface symbols.[^TwoForgetful]

[^TwoForgetful]: There are actually two such forgetful functors, $\Gamma$ and $\Pi$. The first sends $\mathbf{B}G$ to $\mathcal{B}G$, which in [[topology]] is known as $K(G,1)$. The other sends $\mathbf{B}G$ to the [[classifying space]] $B G$. (see <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#GeometricRealization">∞-Lie groupoid -- geometric realization</a>). This distinction is in a way the origin of differential cohomology.

Also the smooth manifold $X$ may be regarded as a [[Lie groupoid]] -- a groupoid with only identity morphisms. Its cartoon description is simply

$$
  X = \{x \stackrel{id}{\to} x \}
  \,.
$$

But there are other groupoids associated with $X$:

Let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. To this is canonically associated the [[Cech groupoid]] $C(\{U_i\})$. Formally we may write this groupoid as

$$
  C(\{U_i\})
  =
  \left(
    \coprod_{i,j} U_i \cap U_j
    \stackrel{\overset{p_1}{\to}}{\underset{p_2}{\to}}
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
      (x,i) &&\to&& (x,j)
    }
  \right\}
  \,.
$$

This indicates that the objects of this groupoid are pairs $(x,i)$ consisting of a point $x \in X$ and a patch $U_i \subset X$ that contains $x$, and a morphism is a triple $(x,i,j)$ consisting of a point and _two_ patches, that both contain the point, in that $x \in U_i \cap U_j$. The triangle in the above cartoon symbolizes the evident way in which these morphisms compose. All this inherits a smooth structure from the fact that the $U_i$ are smooth manifolds and the inclusions $U_i \to X$ are [[smooth function]]s so that $C(U)$ becomes a Lie groupoid.

There is a canonical [[functor]]

$$
  C(\{U_i\}) \to X \;\; :\;\; (x,i) \mapsto x
  \,.
$$

This functor is an [[internal functor]] in [[Diff]] and moreover it is evidently [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]]. This means that it exhibits a _weak equivalence_  of the Lie groupoids, which we write  $C(U) \stackrel{\simeq}{\to}X$. However, even though the underlying functor of bare groupoids is essentially surjective and full and faithful and therefore is guaranteed to have a homotopy-inverse functor, that homotopy-inverse never has smooth component maps, unless $X$ itself is a [[Cartesian space]] and the chosen cover is trivial. 

We do however want to think of $C(U)$ as being equivalent to $X$ even as a Lie groupoid. And moreover, we shall think of $C(U)$ as a _good_ equivalent replacement of $X$ if it comes from a cover that is in fact a [[good open cover]] in that all its finite intersections $U_{i_0 \cdots i_k} := U_{i_0} \cap \cdots \cap U_{i_k}$ are [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^{dim X}$. 

We shall discuss later in which precise sense this condition makes $C(U)$ _good_ in the sense that smooth functors out of $C(U)$ model the correct notion of morphism out of $X$ in the context of smooth groupoids (namely it will mean that $C(U)$ is cofibrant in a suitable [[model category]] structure on the category of Lie groupoids). The formalization of this statement is what [[(∞,1)-topos]] theory is all about, to which we will come. For the moment we shall be content with accepting this as an ad hoc statement.

We now observe then that a [[functor]]

$$
  g : C(U) \to \mathbf{B}G
$$

is given in components precisely by a collection of functions

$$
  \{g_{i j} : U_{i j} \to G \}_{i,j \in I}
$$

such that on each $U_i \cap U_k \cap U_j$ the equality $g_{j k} g_{i j}  = g_{i k}$ of functions holds:

$$
  \left(
    \array{
       && (x,j)
       \\
       & \nearrow && \searrow
       \\
      (x,i) &&\to&& (x,j)
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

Demanding that the functor $g$ respects the smooth structure means that the functions $g_{i j}$ are [[smooth function]]s. Smooth functions $\{g_{i j}\}$ satisfying $g_{i j}  g_{j k} = g_{i k}$ are precisely in bijection with smooth functors $g : C(U) \to X$.

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

Such spans of functors, whose left leg is a weak equivalence, are sometimes known as [[anafunctor]]s. We are to think of these as concrete _models_ for more intrinsically defined morphisms $X\to \mathbf{B}G$ in the $(\infty,1)$-topos of Lie groupoids. 

Now consider yet another ie groupoid canonically associated with $G$: we shall write $\mathbf{E}G$ for the groupoid whose formal description is

$$
  \mathbf{E}G  = 
  \left(
    G \times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G 
  \right)
$$

with the evident composition operation. The cartoon description of this groupoid is

$$
  \mathbf{E}G
  = 
  \left\{
     \array{
        && g_2
        \\
        & \nearrow &=& \searrow
        \\
        g_1 &&\stackrel{}{\to}&& g_3
     }
  \right\}
  \,,
$$

where we don't need to further label the morphisms, since there is a _unique_ morphism for every ordered pair $(g_1, g_2)$ of elements in $G$. This again inherits an evident smooth structure from the smooth structure of $G$ and hence becomes a Lie groupoid.

There is an evident [[forgetful functor]]

$$
  \mathbf{E}G \to \mathbf{B}G
$$

which sends

$$
  (g_1 \to g_2) \mapsto (\bullet \stackrel{g_2^{-1} g_1}{\to} \bullet)
  \,.
$$

Consider then the [[pullback]] diagram

$$
  \array{
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
$$

in the category $Grpd(Diff)$.


The object $\tilde P$ is the Lie groupoid whose cartoon description is


$$
  \array{
    \tilde P = 
    \left\{
       \array{
          (x,i,g_1) &&\stackrel{}{\to}&& (x,j,g_2 = g_1 g_{i j}(x))
       }
   \right\}
  }
  \,,
$$

where there is a unique morphism as indicated, whenever the group labels match as indicated. Due to this uniqueness, this Lie groupoid is weakly equivalent to one that comes just from a manifold $P$ (it is 0-[[truncated]])

$$
  \tilde P \stackrel{\simeq}{\to} P
  \,.
$$

This $P$ is traditionally written as

$$
  P = \left( \coprod_{i} U_i \times G \right)_{\sim}
  \,,
$$

where the [[equivalence relation]] is precisely that exhibited by the morphisms in $\tilde P$. This is the traditional way to construct a $G$-[[principal bundle]] from cocycle functins $(g_{i j})$. We may think of $\tilde P$ as _being_ $P$. It is a particular _representative_ of $P$ in the $(\infty,1)$-topos of Lie groupoids.

While the fact that the $P$ obrained this way does indeed have a principal $G$-[[action]] on it is easy to see in components, but for later generalizations it is crucial that we can also recover this in a general abstract way. For notice that there is a canonical [[action]]

$$
  (\mathbf{E}G) \times G \to \mathbf{E}G
  \,.
$$

Then consider the [[pasting]] diagram of pullbacks

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

The morphism $\tilde P \times G \to \tilde P$ is the principal $G$-[[action]] of $G$ on $\tilde P$.


In summary we find

+-- {: .un_prop}
###### Observation

There is an [[equivalence of categories]]

$$
  SmoothFunc(C(\{U_i\}), \mathbf{B}G)
  \simeq
  G Bund(X)
$$

between the [[nLab:functor category]] of smooth functors and smooth natural transformations, and the groupoid of smooth $G$-[[nLab:principal bundle]]s on $X$. 

=--

It is no coincidence that this statemment looks akin to the maybe more familiar statement which says that _equivalence classes_ of $G$-principal bundles are classified by [[homotopy]]-classes of morphisms of [[topological space]]s 

$$
  \pi_0 Top(X, \mathcal{B}G)
  \simeq
  \pi_0 G Bund(X)
  \,,
$$

where $\mathcal{B}G \in $ [[Top]] is the topological [[classifying space]] of $G$. In fact the category [[Top]] of topological spaces, regarded as an [[(∞,1)-category]], is the archetypical [[(∞,1)-topos]] the way that [[Set]] is the archetypical [[topos]]. And it is equivalent to [[∞Grpd]], the $(\infty,1)$-category of bare [[∞-groupoid]]s. What we are seeing above is a first indication of how [[cohomology]] of bare $\infty$-groupoids is lifted to a richer $(\infty,1)$-topos to cohomology of $\infty$-groupoids with extra structure.

In fact, all of the statements that we considered so far becomes conceptually _simpler_ in the $(\infty,1)$-topos. We had already remarked that the [[anafunctor]] span $X \stackrel{\simeq}{\leftarrow} C(U) \stackrel{g}{\to} \mathbf{B}G$ is really a model for what is simply a direct morphism $X \to \mathbf{B}G$ in the $(\infty,1)$-topos. But more is true: that pullback of $\mathbf{E}G$ which we condisered is just a model for the [[homotopy pullback]] of just the _point_ 


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

#### Cech cocycles {#Cech2Cocycles}

The discussion above of $G$-principal bundles was all based on the [[Lie groupoid]]s $\mathbf{B}G$ and $\mathbf{E}G$ that are canonically induced by a [[Lie group]] $G$. We now discuss the case where $G$ is generalized to a [[Lie 2-group]]. The above discussion will go through essentially verbatim, only that we pick up [[2-morphism]]s everywhere. This is the first step towards higher Chern-Weil theory. The resulting generalization of the notion of principal bundle is that of [[principal 2-bundle]]. For historical reasons these are known in the literature often as [[gerbe]]s or as [[bundle gerbe]]s. 

Write $U(1) = \mathbb{R}/\mathbb{Z}$ for the [[circle group]]. We have already seen above the groupoid $\mathbf{B}U(1)$ obtained from this. But since $U(1)$ is an [[abelian group]] this groupoid has the special property that it still has itself the structure of an [[group object]]. This makes it what is called a [[2-group]]. Accordingly, we may form its [[delooping]] once more to arrive at a [[Lie 2-groupoid]] $\mathbf{B}^2 U(1)$.

Its cartonn picture is

$$
  \mathbf{B}^2 U(1) = 
  \left\{
     \array{
        && \bullet
        \\
        & {}^{\mathllap{Id}}\nearrow 
        & \Downarrow^{\mathrlap{g}}& 
        \searrow^{\mathrlap{Id}}
        \\
        \bullet &&\underset{Id}{\to}&& \bullet
     }
  \right\}
$$

for $g \in U(1)$. Both [[horizontal composition]] as well as [[vertical composition]] of the 2-morphisms is given by the product in $U(1)$.

Let again $X$ be a smooth manifold with [[good open cover]] $\{U_i \to X\}$. The corresponding [[Cech groupoid]] we may also think of as a Lie 2-groupoid, 

$$
  C(U) = 
  \left(
     \coprod_{i, j, k} U_i \cap U_j \cap U_k
     \stackrel{\to}{\stackrel{\to}{\to}}
     \coprod_{i, j}
     U_i \cap U_j
     \stackrel{\to}{\to}
     \coprod_i U_i
  \right)
  \,.
$$

What we see here are the first stages of the full [[Cech nerve]] of the cover. Eventually we will be looking at this object in its entirety, since for all degrees this is always a _good_ replacement of the manifold $X$.

So we look now at 2-[[anafunctor]]s given by spans 

$$
  \array{
    C(U) &\stackrel{g}{\to}& \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

of internal [[2-functor]]s. These will model direct morphisms $X \to \mathbf{B}^2 U(1)$ in the $(\infty,1)$-topos. It is straightforward to read off that the smooth 2-functor $g : C(U) \to \mathbf{B}^2 U(1)$ is given by the data of a 2-cocycle in the [[Cech cohomology]] of $X$ with coefficients in $U(1)$. On [[2-morphism]]s it specifies an assignment

$$
  g 
   \;\; : \;\;
   \left(
     \array{
       && (x,j)
       \\
       & \nearrow &\Downarrow& \searrow
       \\
      (x,i) &&\to&& (x,k)
     }
   \right)
   \;\;\;
   \mapsto
   \;\;\;
  \left\{
     \array{
        && \bullet
        \\
        & {}^{\mathllap{Id}}\nearrow 
        & \Downarrow^{\mathrlap{g_{i j k}(x)}}& 
        \searrow^{\mathrlap{Id}}
        \\
        \bullet &&\underset{Id}{\to}&& \bullet
     }
  \right\}    
$$

that is given by a collection of smooth functions

$$
  (g_{i j k} : U_i \cap U_j \cap U_k \to U(1))
$$

and on [[3-morphism]]s it gives a constraint on these functions, since there are only identity 3-morphisms in $\mathbf{B}^2 U(1)$

$$
  \begin{aligned}
  \left(
  \array{
    (x,j) &&\stackrel{g_2}{\to}&& (x,k)
    \\
    \uparrow^{} &&{}^{}\nearrow&& \downarrow^{}
    \\
    (x,i)
    &&\stackrel{}{\to}&& (x,l)
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    (x,j) &&\stackrel{}{\to}&& (x,k)
    \\
    \uparrow^{} &&\searrow^{}&& \downarrow^{}
    \\
    (x,i)
    &&\stackrel{}{\to}&& (x,l)
  }
  \right)
  \\
  & \mapsto
  \left(
  \array{
    \bullet &&\stackrel{}{\to}&& \bullet
    \\
    \uparrow^{} &\Downarrow^{g_{i j k}(x)}
    &{}^{}\nearrow&\Downarrow^{g_(i k l)(x)}& 
    \downarrow^{}
    \\
    \bullet
    &&\stackrel{}{\to}&& \bullet
  }
  \;\;\;\;
  \stackrel{Id}{\Rightarrow}
  \;\;\;\;   
  \array{
    \bullet &&\stackrel{}{\to}&& \bullet
    \\
    \uparrow^{} &\Downarrow^{g_{i j l}(x)}
    &\searrow^{}&\Downarrow^{g_{j k l}(x)}& \downarrow^{}
    \\
    \bullet
    &&\stackrel{}{\to}&& \bullet
  }
  \right)
  \end{aligned}  
  \,.
$$

This cocycle condition

$$
  g_{i j k} \cdot g_{i k l} = g_{i j l} \cdot g_{j k l}
$$

is that known from [[Cech cohomology]].

Following the general abstract formalism, it is again straightforward to find the total space of the $\mathbf{B}U(1)$-[[principal 2-bundle]] that is classified by such a cocycle.

For that we need to get the 2-groupoid $\mathbf{B} \mathbf{B}U(1)$ and the 2-functor $\mathbf{E} \mathbf{B} U(1) \to \mathbf{B}^2 U(1)$ that exhibuits the [[universal principal ∞-bundle|universal principal 2-bundle]] over $U(1)$.

It is easy to guess what this should be, but there is also a systematic way to derive this, which works in full generality:


#### Universal principal $n$-bundles {#UniversalnBundle}

For $G$ any group object, what the [[universal principal ∞-bundle]] is a good replacement for the point inclusion $* \to \mathbf{B}G$.

Write 

$$
  \mathbf{B}G^I
  :=
  [\Delta[1], \mathbf{B}G]
$$

for the [[path space object]] of $\mathbf{B}G$. For $G$ an ordinary group this is also known as the [[arrow category]] of $\mathbf{B}G$.

There are two canonical projections $d_i : \mathbf{B}G^I \to \mathbf{B}G$. 
Define $\mathbf{E}G$ to be the [[pullback]]

$$
  \array{
    \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G^I &\stackrel{d_1}{\to}& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{d_0}}
    \\
    \mathbf{B}G
  }
  \,.
$$

For $G$ an ordinary Lie group, this reproduces the groupoid $\mathbf{E}G$ discussed [above](#PrincipalBundles). 

For detailed illustration of what $\mathbf{E}G$ looks like for $G$ a [[2-group]], see ([RobertsSchreiber](#RobertsSchreiber)).


#### Circle $n$-bundles and bundle $(n-1)$-gerbes

Let $g : C(U) \to \mathbf{B}^2 U(1)$ be a Cech cocycle as [above](#Cech2Cocycles). By the discussion of [universal n-bundles](#UniversalnBundle) we find the corresponding total space object as the [[pullback]] 

$$
  \array{
    \tilde P &\to& \mathbf{E}\mathbf{B}U(1)
    \\
    \downarrow && \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
  \,.
$$

Unwinding what this means, one see that $\tilde P$ is a groupoid which is given by a (trivial) complex [[line bundle]] 

$$
  \array{
     L
     \\
     \downarrow
     \\
     C(U)_1 = U \times_X U &\stackrel{\to}{\to}& C(U)_1 = U
     \\
     && \downarrow
     \\
     && X
  }
$$

over the space $C(U)_1$ of [[morphism]]s, and where composition is encoded by a line bundle morphism

$$

  \mu_g : \pi_1^* L \otimes \pi_2^* L \to \pi_1^* L
$$

canonically induced from $g$. The cocycle condition satisfied by $g$ implies that this composition operation is associative in the evident sense

Such a structzre is called a [[bundle gerbe]] relative to the [[surjective submersion]] $U \to X$. We see that this is the total space of a $\mathbf{B}U(1)$-[[principal 2-bundle]] in a weakly equivalent incarnation akin to the presentation $(\coprod_i U_i \times G)/_{(g_{i j})}$ of an ordinary principal bundle in terms of a cocycle.

This is the beginning of a pattern. Next we can form one more [[delooping]] and produce the Lie 3-groupoid $\mathbf{B}^3 U(1)$. A cocycle $C(U) \to \mathbf{B}^3 U(1)$ classifies a _circle 3-bundle_  . The total space object $\tilde P$ in the pullback

$$
  \array{
    \tilde P &\to& \mathbf{E}\mathbf{B}^2 U(1)
    \\
    \downarrow && \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}^3 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

is essentially what is known as a [[bundle 2-gerbe]].




#### String 2-bundles and nonabelian bundle gerbes

Above we saw $\mathbf{B}U(1)$-[[principal 2-bundle]]s. The groupoid $\mathbf{B}U(1)$ is a special case of what is called a [[Lie 2-group]], which is a [[group object]] $G$ in Lie groupoids. 

An example of a nonabelian Lie 2-group is the [[string Lie 2-group]] $String$, which sits in a [[fiber sequence]] of Lie 2-groups of the form

$$
  \mathbf{B}U(1) \to String \to Spin
  \,.
$$


A quick way to understand the meaning of this 2-group is from the fact that:

**Fact.** Given a [[spin group]]-[[principal bundle]] $P \to X$, its [[Pontryagin class]] classifies a _circle 3-bundle_  (a [[bundle 2-gerbe]]) called the [[Chern-Simons circle 3-bundle]]. The nontriviality of this is precisely the obstruction to lifting the $Spin$-principal bundle $P$ to a $String$-principal 2-bundle.

Again, we can construct Lie 2-groupoids equivalent to the total space of a $String$-principal 2-bundle classified by a cocycle $g : C(U) \to \mathbf{B}String$ by forming the pullback.
 
$$
  \array{
    \tilde P &\to& \mathbf{E}String
    \\
    \downarrow && \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B} String
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

These groupoids $\tilde P$ are in the literature known as [[nonabelian bundle gerbe]].


#### A model for principal $\infty$-bundles {#ModelForPrincipalInfinityBundle}

We have seen [above](#PrincipalBundles) that the theory of ordinary smooth [[principal bundle]]s is naturally situated within the context of [[Lie groupoid]]s, and [then](#Cech2Cocycles) that the theory of smooth [[principal 2-bundle]]s is naturally situated within the theory of [[Lie 2-groupoid]]s. This is clearly the beginning of a pattern in [[higher category theory]] where in the next step we see smooth [[3-groupoid]]s and so on. Finally the general theory of [[principal ∞-bundle]]s deals with smooth [[∞-groupoid]]s. 

A comprehensive discussion of such [[∞-Lie groupoid]]s is given there. In this introduction here we will just briefly describe the main _tool_ for _modelling_ these and describe principal $\infty$-bundles in this model. See also [[models for ∞-stack (∞,1)-toposes]].

We first look at bare [[∞-groupoid]]s and then discuss how to equip these with smooth structure.

An [[∞-groupoid]] is first of all supposed to be a structure that has [[k-morphism]]s for all $k \in \mathbb{N}$, which for $k \geq 1$ go between $(k-1)$-morphisms. A useful tool for organizing such collections of morphisms is the notion of a [[simplicial set]]. This is a [[functor]] on the [[opposite category]] of the  [[simplex category]] $\Delta$, whose objects are the abstract cellular $k$-[[simplex|simplices]], denoted $[k]$ or $\Delta[k]$ for all $k \in \mathbb{N}$, and whose morphisms $\Delta[k_1] \to \Delta[k_2]$ are all ways of mapping these into each other. So we think of such a simplicial set given by a functor

$$
  K : \Delta^{op} \to Set
$$

as specifying

* a set $[0] \mapsto K_0$ of [[object]]s;

* a set $[1] \mapsto K_1$ of [[morphism]];

* a set $[2] \mapsto K_2$ of [[2-morphism]];

* a set $[3] \mapsto K_3$ of [[3-morphism]];

and generally

* a set $[k] \mapsto K_k$ of [[k-morphism]]s

as well as specifying

* functions $([n] \hookrightarrow [n+1]) \mapsto K_{n+1} \to K_n$
  that send $n+1$-morphisms to their boundary $n$-morphisms;

* functionss $([n+1] \to [n]) \mapsto K_{n} \to K_{n+1}$
  that send $n$-morphisms to [[identity]] $(n+1)$-morphisms
  on them.

The fact that $K$ is supposed to be a [[functor]] enforces that these assignments of sets and functions are consist with our interpretation of them as sets of $k$-morphisms and source- and target maps between these, in that for instance it enforces that the 1-morphisms between which a 2-morphisms goes suitably go between coinciding objects. These are called the [[simplicial identities]].

But apart from this source-target matching, a generic simplicial set does not yet encode a notion of [[composition]] of these morphisms. 

For instance for $\Lambda^1[2]$ the simplicial set consisting of two attached 1-cells 

$$
  \Lambda^1[2] = \left\{
    \array{
       && 1
       \\
       & \nearrow && \searrow
       \\
       0 &&&& 2
    }
  \right\}
$$

and for $(f,g) : \Lambda^1[2] \to K$ an image of this situation in $K$, hence a pair $x_0 \stackrel{f}{\to} x_1 \stackrel{g}{\to} x_2$ of two _composable_ 1-morphisms in $K$, we want to demand that there exists a third 1-morphisms in $K$ that may be thought of as the [[composition]] $x_0 \stackrel{h}{\to} x_2$ of $f$ and $g$. But since we are working in [[higher category theory]] (and not to be [[evil]]), we want to identify this composite only up to a [[2-morphism]] equivalence

$$
    \array{
       && 1
       \\
       & {}^{\mathllap{f}}\nearrow &\Downarrow^{\mathrlap{\simeq}}& 
       \searrow^{\mathrlap{g}}
       \\
       x_0 &&\stackrel{h}{\to}&& x_2
    }
  \,.
$$

From the picture it is clear that this is equivalent to demanding that for $\Lambda^1[2] \hookrightarrow \Delta[2]$ the obvious inclusion of the two abstract composable 1-morphisms into the 2-simplex we have a diagram of morphisms of simplicial sets

$$
  \array{
    \Lambda^1[2] &\stackrel{(f,g)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists h}}
    \\
    \Delta[2]
  }
  \,.
$$

A simplicial set where for all such $(f,g)$ such $h$ exists may be thought of as a collection of higher morphisms that is equipped with a notion of composition of adjacent 1-morphisms. 

For the purpose of describing [[groupoid]]al compostion, we now want that this composition operation has all [[inverse]]s. For that purpose, notice that for 

$$
  \Lambda^2[2] = \left\{
    \array{
       && 1
       \\
       & && \searrow
       \\
       0 &&\to&& 2
    }
  \right\}
$$

the simplicial set consisting of two 1-morphisms that touch at their end, hence for 

$$
  (g,h) : \Lambda^2[2] \to K
$$

two such 1-morphisms in $K$, then if $g$ had an inverse $g^{-1}$ we could use the above compostion operation to compose that with $h$ and thereby find a morphism $f$ connecting the sources of $h$ and $g$. This being the case is evidently equivalent to the existence of diagrams of morphisms of simplicial sets

$$
  \array{
    \Lambda^2[2] &\stackrel{(g,h)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists f}}
    \\
    \Delta[2]
  }
  \,.
$$

Demanding that all such diagrams exist is therefore demanding that we have on 1-morphisms a compositon operation with inverses in $K$. 

In order for this to qualify as an $\infty$-groupoid, this composition operation needs to satisfy an [[associativity law]] up to [[2-morphism]]s, which means that we can find the relevant [[associahedron]]s in $K$. These in turn need to be connected by _pentagonators_ and ever so on.  It is a nontrivial but true and powerful fact, that it turns out that all these [[coherence]] conditions are captured by generalizing the above conditions to all dimensions in the evident way:

let $\Lambda^i[n] \hookrightarrow \Delta[n]$ be the simplicial set -- called the $i$th $n$-[[horn]] -- that consists of all cells of the $n$-[[simplex]] $\Delta[n]$ except the interior $n$-morphism and the $i$th $(n-1)$-morphism.

Then a simplicial set is called a [[Kan complex]], if for all images $f : \Lambda^i[n] \to K$ of such horns in $K$, the missing two cells can be found in $K$- in that we can always find a _horn filler_ $\sigma$ in the diagram

$$
  \array{
     \Lambda^i[n] &\stackrel{f}{\to}& K
     \\
     \downarrow & \nearrow_{\mathrlap{\sigma}}
     \\
     \Delta[n]
  }
  \,.
$$

The basic example is the [[nerve]] $N(C) \in sSet$ of an ordinary [[groupoid]] $C$, which is the simplicial set with $N(C)_k$ precisely the set of sequence of $n$ composable morphisms in $C$. The nerve operation is a [[full and faithful functor]]  from 1-groupoids into Kan complexes and hence may be thought of as embedding 1-groupoids in the context of general [[∞-groupoid]]s.

But we need a bit more than just bare [[∞-groupoid]]s. In generalization to [[Lie groupoid]]s, we need [[∞-Lie groupoid]]s. A useful way to encode that an $\infty$-groupoid has extra structure modeled on geometric test objects that themselves form a category $C$ is to rember the rule which for each test space $U$ in $C$ produces the $\infty$-groupoid of $U$-parameterized families of $k$-morphisms in $K$.  For instance for an [[∞-Lie groupoid]] we could test with each [[Cartesian space]] $U = \mathbb{R}^n$ and find the $\infty$-groupoids $K(U)$ of smooth $n$-parameter families of $k$-morphisms in $K$.

This data of $U$-families arranges itself into a [[presheaf]] with values in Kan complexes

$$
  K : C^{op} \to KanCplx \hookrightarrow sSet
$$

hence with values in simplicial sets. This is equivalently a [[simplicial presheaf]] of sets. The [[functor category]] $[C^{op}, sSet]$ on the [[opposite category]] of the category of test objects $C$ serves as a model for the [[(∞,1)-category]] of $\infty$-groupoids with $C$-structure.

While there are no [[higher morphism]]s in this functor 1-category that could for instance witness that two $\infty$-groupoids are not [[isomorphic]], but still [[equivalence of categories|equivalent]], it turns out that all one needs in order to reconstruct _all_ these higher morphisms (up to equivalence!) is just the information of wich morphisms of simplicial presheaves would become invertible if we were keeping track of higher morphism. These would-be invertible morphisms are called _weak equivalences_ and denoted $K_1 \stackrel{\simeq}{\to} K_2$. 

For common choices of $C$ there is a well-understood way to define the weak equivalences $W \subset mor [C^{op}, sSet]$, and equipped with this information the category of simplicial presheaves becomes a _[[category with weak equivalences]]_ . There is a well-developed but somewhat intricate theory of how exactly this 1-cagtegorical data models the full higher category of structured groupoids that we are after, but for our purposes we essentially only need to work inside the [[category of fibrant objects]] of a [[model category]] structure [[model structure on simplicial presheaves|on simplicial presheaves]], which in practice amounts to the fact that we use the following three basic constructions:

1. **[[∞-anafunctor]]s** -- A morphisms $X \to Y$ between $\infty$-groupoids with $C$-structure is not just a morphism $X\to Y$ in $[C^{op}, sSet]$, but is a [[span]] of such ordinary morphisms

   $$
     \array{  
        \hat X &\to& Y
        \\
        \downarrow^{\mathrlap{\simeq}}
        \\
        X
     }
   $$

   where the left leg is a weak equivalence. This is sometimes called an _$\infty$-anafunctor_ from $X$ to $Y$.
 
1. **[[homotopy pullback]]** -- For $A \to B \stackrel{p}{\leftarrow} C$ a [[diagram]], the [[(∞,1)-pullback]] of it is the ordinary [[pullback]] in $[C^{op}, sSet]$ of a replacement diagram $A \to B \stackrel{\hat p}{\leftarrow} \hat C$, where $\hat p$ is a _good replacement_  of $p$ in the sense of the following...

1. **[[factorization lemma]]** -- For $p : C \to B$ a morphism in $[C^{op}, sSet]$, _good replacement_ $\hat p : \hat C \to B$ is given by the total vertical morphism in the ordinary [[pullback]] diagram

   $$
     \array{
       \hat C &\to& C
       \\
       \downarrow && \downarrow^{\mathrlap{p}}
       \\
       B^{\Delta[1]} &\to& B
       \\
       \downarrow
       \\
       B
     }
     \,.
   $$

  
The [[principal ∞-bundle]]s that we wish to model are already the main and simplest example of the application of these three items: 

Consider an object $\mathbf{B}G \in [C^{op}, sSet]$ which is an $\infty$-groupoid with a single object, so that we may think of it as the [[delooping]] of an [[∞-group]] $G$, let $*$ be the point and $* \to \mathbf{B}G$ the unique inclusion map. The _good replacmement_ of this inclusion morphism is the $G$-[[universal principal ∞-bundle]] $\mathbf{E}G \to \mathbf{B}G$ gives by the pullback diagram
  
$$
  \array{ 
    \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G^I &\to& \mathbf{B}G
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

we call the [[principal ∞-bundle]] $P \to X$ classified by the coycle.

It is now evident that our discussion of ordinary smooth principal bundles [above](#PrincipalBundles) is the special case of this for $\mathbf{B}G$ the [[nerve]] of the one-object groupoid associated with the ordinary group $G$.

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



### Parallel transport in low dimensions {#LowDimension}

With a decent handle on principal $\infty$-bundles as described [above](#ModelForPrincipalInfinityBundle) we now turn to the description of [[connection on an ∞-bundle|connections on ∞-bundles]]. It will turn out that the above [[cocycle]]-description of $G$-principal $\infty$-bundles in terms of  [[∞-anafunctor]] $X \stackrel{\simeq}{\leftarrow} \hat X \stackrel{g}{\to} \mathbf{B}G$ has, under mild conditions, a natural generalization where $\mathbf{B}G$ is replaced by a [[concrete sheaf|non-concrete]] [[∞-Lie groupoid]] $\mathbf{B}G_{conn}$ which we may think of as the [[∞-groupoid of ∞-Lie algebra valued forms]]. This comes with a canonical map $\mathbf{B}G_{conn} \to \mathbf{B}G$ and an $\infty$-connection $\nabla$ on the $\infty$-bundle classified by $g$ is simply a lift

$$
  \array{
    && \mathbf{B}G_{conn}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
  \,.
$$

In the language of [[∞-stack]]s we may think of $\mathbf{B}G$ as the $\infty$-stack (on [[CartSp]]) or $\infty$-prestack (on [[Diff]]) $G TrivBund(-)$ of _trivial_ $G$-principal bundles, and of $\mathbf{B}G_{conn}$ cortespondingly as trivial $G$-principal bundles with (non-trivial) connection $G TrivBund_{\nabla}(- )$. In this sense the statement that $\infty$-connections are cocycles with coefficients in some $\mathbf{B}G_{conn}$ is a tautology. The real questions are therefore:

1. What is $\mathbf{B}G_{conn}$ in concrete formulas?

1. Why are these formulas what they are? What is the general abstract concept of an $\infty$-connection? What are its defining abstract properties?

A comprehensive answer to the second question is provided by the general abstract concept of [[schreiber:differential cohomology in an (∞,1)-topos]]. Here in this introduction we will not go into the full abstract theory, but using classical tools we get pretty close. What we describe is a generalization of the concept of [[parallel transport]] to [[higher parallel transport]]. As we shall see, this is naturally expressed in terms of [[∞-anafunctor]]s out of [[path n-groupoid]]s. This reflects how the full abstract theory arises in the context of an [[∞-connected (∞,1)-topos]] that comes canonically with a notion of [[schreiber:path ∞-groupoid]]s.


We being below the discussion of $\infty$-connection by reviewing the classical theory of [[connection on a bundle]] in a way that will make its generalization to higher connections relatively straightforward:

* [Connections on principal bundles](#ConnectionOnPrincipalBundle).

In an analogous way we we can then describe certain classes of [[connections on a 2-bundle]] -- subsuming the notion of [[connection on a bundle gerbe]] -- in

* [Connections on 2-bundles](#ConnectionOn2Bundle).

With that in hand we then revisit the discussion of connections on ordinary bundles: by associating to each bundle with connection its corresponding _curvature 2-bundle with connection_ , we obtain a more refined description of connections on bundles, one that is naturally adapted to the construction of [[curvature characteristic form]]s in the [[Chern-Weil homomorphism]]:

* [Curvature characteristics of 1-bundles](#CurvatureCharacteristicsI).

This turns out to be the kind of formulation of [[connections on an ∞-bundle]] that drops out of the general abstract theory described at [[∞-Chern-Weil homomorphism]]. In classical terms, its full formulation involves the description of [[circle n-bundles with connection]] in terms of [[Deligne cohomology]] and the description of the [[∞-groupoid of ∞-Lie algebra valued forms]] in terms of [[dg-algebra]] homomorphisms. The first aspect we discuss in 

* [Circle n-bundles with connection](#c)

the second in

* [∞-Lie algebra valued connections](#LieConnections).

The combination of these two aspects yields naturally an explicit model for the [[Chern-Weil homomorphism]] and its generalization to higher bundles:

* [The ∞-Chern-Weil homomorphism](#ChernWeilHomomorphism)

Taken together, these cnstructions allow us to express a good deal of the general $\infty$-Chern-Weil theory with classical tools. As an example, we describe how the classical Cech-Deligne cocycle construction of the refined [[Chern-Weil homomorphism]] (by [BrylinskiMacLaughlin](#BrylinskiMacLaughlin)) drops out from these constructions:

* [Example: The Chern-Simons circle 3-bundle](#ChernSimons3Bund).



#### Connections on a principal bundle {#ConnectionOnPrincipalBundle}


> basic fact to be expounded here: for $G$ a Lie group 

> $\mathbf{B}G_{conn} = [\mathbf{P}_1(-), \mathbf{B}G]$.


We describe the standard notion of a [[nLab:connection on a bundle]] but from a point of view that carries in it the seed for the general concept of differential cohomology that we describe here. This also serves to introduce in simple explicit terms several of the concepts that we shall formalize later in abstract [[nLab:(∞,1)-topos]] theory.

Recall the discussion of principal bundles [above](#PrincipalBundles) and in particular the equivalence of groupoids

$$
  Hom_{Grpd(Diffeol)}(C(U), \mathbf{B}G)
  \simeq
  G Bund(X)
$$

given by an [[good open cover]] $\{U_i \to X\}$.

What we are after is an equivalence of categories of this functorial form for the case that the bundles are equipped with a [[connection on a bundle]].

For that purpose we consider now the [[nLab:path groupoid]]
$\mathbf{P}_1(X)$, defined to be the groupoid whose objects are the points of $X$, and whose morphisms are equivalence classes of smooth maps $\gamma : [0,1] \to X$ that are constant in a neighbourhood of the boundary of the interval, and where two such maps are regarded as equivalent if they can be connected by a smooth homotopy $[0,1]^2 \to X$ that is of rank $\leq 1$.

Such a map $\gamma$ constitutes a path between its endpoint $x = \gamma(0)$ and $y = \gamma(1)$, and we regard it as a morphism $[\gamma] : x \to y$ in $P_1(X)$. The composition of these morphisms is given by concatenation of paths. 

A cartoon of this [[nLab:path groupoid]] is

$$
  \mathbf{P}_1(X)
  = 
  \left\{
    \array{
      && y
      \\
      & {}^{\mathrlap{[\gamma_1]}}\nearrow && \searrow^{\mathrlap{[\gamma_2]}}
      \\
      x &&\stackrel{[\gamma_2 \circ \gamma_1 ]}{\to}&& z
    }
  \right\}
  \,.
$$

There is no good way to realize this groupoid as being internal to manifolds. But it has an nevertheless has an evident and natural smooth structure: we may declare that a family $f : \mathbb{R}^n \to Mor(\mathbf{P}_1(X))$ of morphisms of $P_1(X)$ parameterized over a [[nLab:Cartesian space]] $\mathbb{R}^n$ is a _smooth_ family if there is a [[nLab:smooth function]]  $\tilde f : \mathbb{R}^n \times [0,1] \to X$ such that $f(u)(-) = \tilde f(u,-)$.

Possibly a more familiar groupoid is the [[nLab:fundamental groupoid]] $\mathbf{\Pi}_1(X)$ of $X$. This is defined essentially as $\mathbf{P}_1(X)$, only that here here morphisms are full [[nLab:homotopy]]-classes of paths, not just [[nLab:thin homotopy]] classes. This inherits a notion of smooth families of morphisms as before, but only the constant family is smooth in this case. We write $\Pi_1(X) \in Grpd$ for the underlying bare [[nLab:fundamental groupoid]] of $X$.

There is a canonical projection functor $P_1(X) \to \mathbf{\Pi}_1(X)$ that sends a path to its homotopy class. This is a smooth functor in the above sense.

Similarly we can also conceive the smooth structure of $\mathbf{B}G$ in terms of smooth families of morphisms in the obvious way. We say then that a morphism between such groupoids equipped with an information about smooth families is a functor that takes smooth families to smooth families. 

Later on we formalize this by saying that $\mathbf{P}_1(X)$, $\mathbf{\Pi}_1(X)$ as well as $\mathbf{B}G$ etc. are groupoids [[nLab:internal category|internal to]] the category of [[nLab:diffeological space]]s and that smooth functors are functors internal to that category.

With these definitions we now find the following equivalence of categories

+-- {: .un_prop}
###### Proposition

There is a natural equivalence of categories 

$$
  SmoothFunc(\mathbf{P}_1(X), \mathbf{B}G)
  \simeq
  G TrivBund_{\nabla}(X)
 \,.
$$

=--

Here the groupoid on the right the [[nLab:groupoid of Lie-algebra valued forms]] on $X$, which may be thought of as the groupoid of _trivial_ $G$-principal bundles on $X$ equipped with connection. It is the groupoid whose

* objects are [[nLab:Lie algebra]]-valued [[nLab:differential form]]s 
  $A \in \Omega^1(X,\mathfrak{g})$;

* morphisms $\lambda : A \to A'$ are smooth $G$-valued functions $\lambda \in C^\infty(X,G)$ such that $A' = \lambda A \lambda^{-1} + \lambda d \lambda^{-1}$.

* composition of morphisms is the product of $G$-valued functions.

This equivalence is canonical: it identifies a differential form $A$ with the [[nLab:parallel transport]] that it induces: the smooth functor $tra_A : P_1(X) \to \mathbf{B}G$ corresponding to $A$ sends a path $\gamma : [0,1] \to X$ to the parallel transport

$$
  P \exp(\int_0^1 \gamma^* A)
  \,,
$$ 

which is defined to be the value at 1 of the unique $G$-valued function $f : [0,1] \to G$ that solves the differential equation $d f = r_*(f)(A)$ with boundary condition $f(0) = e$, where $r(g) : G \to G$ is the right action of $G$ on itself.

From this description and classical results it is clear that we have

+-- {: .un_prop}
###### Observation

The smooth functor $tra_A : \mathbf{P}_1(X) \to \mathbf{B}G$ factors through the [[nLab:fundamental groupoid]] $\mathbf{P}_1(X) \to \mathbf{\Pi}_1(X)$ precisely if $A$ is a _flat_ $\mathfrak{g}$-valued differential form, in that $F_A := d_{dR} A + [A \wedge A] = 0$.

=--

All these constructions are [[nLab:natural transformation|natural]] in $X$. This means that they extend in to functors

$$
  \mathbf{B}G_{diff'}
  :=
  SmoothFunc(\mathbf{P}_1(-), \mathbf{B}G)
  \simeq
  (C^\infty(-,G) \times \Omega^1(-,\mathfrak{g})
  \stackrel{\overset{}{\to}}{\underset{p_1}{\to}}
  \Omega^1(-,\mathfrak{g}))
  : 
  Diff^{op} \to Grpd
$$

and

$$
  \mathbf{\flat} \mathbf{B}G
  :=
  SmoothFunc(\mathbf{\Pi}_1(-), \mathbf{B}G)
  \simeq
  (C^\infty(-,G) \times \Omega_{flat}^1(-,\mathfrak{g})
  \stackrel{\overset{}{\to}}{\underset{p_1}{\to}}
  \Omega_{flat}^1(-,\mathfrak{g}))
  : 
  Diff^{op} \to Grpd
  \,.
$$

As our notation means to suggest, it makes sense to think of these
functors as assigning to a space $U$ the the smooth families of maps into some implicitly defined smooth groupoid. When we formalize this in terms of [[nLab:(∞,1)-topos]] theory further below, we find an [[nLab:adjunction]] of the form

$$
  Hom(\mathbf{\Pi}_1(X), \mathbf{B}G)
  \simeq
  Hom(X, \mathbf{\flat}\mathbf{B}G)
$$

and

$$
  Hom(\mathbf{P}_1(X), \mathbf{B}G)
  \simeq
  Hom(X, (\mathbf{B}G)_{diff'})
  \,.
$$

In terms of functors internal to [[nLab:diffeological space]]s, this is realized as follows: for $\{U_i \to X\}$ a (good) open cover as before, define a group $\mathbf{P}_1(C(\{U_i\}))$ that combines the [[nLab:Cech nerve|Cech groupoid]] with the [[nLab:path groupoid]]: its morphisms are generated from the morphisms of $C(\{U_i\})$ and $\mathbf{P}_1(X)$, subject to the relation indicated by the following cartoon description


$$
  \mathbf{P}_1(C(\{U_i\}))
  =
  \left\{
    \array{
      (x,i) &\stackrel{\gamma_i}{\to}& (y,i)
      \\
      \downarrow && \downarrow
      \\
      (x,j) &\stackrel{\gamma_j}{\to}& (y,j)
    }
  \right\}
  \,.
$$

In terms of this we have 

+-- {: .un_prop}
###### Proposition

$$
  SmoothFunc(\mathbf{P}_1(C(\{U_i\})), \mathbf{B}G)
  \simeq
  SmoothFunc(C(\{U_i\}), (\mathbf{B}G)_{diff'})
  \simeq G Bund_\nabla(X)
  \,,
$$

=--

where on the right we have the groupoid of $G$-[[nLab:principal bundle]]s [[nLab:connection on a bundle|with connection]] on $X$.


#### Connections on principal 2-bundles {#ConnectionOn2Bundle}

> basic fact to be expounded here: for $G$ a [[Lie 2-group]] we have

> $\flat\mathbf{B}G \simeq [\mathbf{\Pi}(-), \mathbf{B}G]$;

> $\mathbf{B}G_{diff} = [\mathbf{\Pi}(-), \mathbf{B}INN(G)] \times_{\mathbf{B}INN(G)} \mathbf{B}G$.

Above we described [[nLab:cocycle]]s for smooth 
$G$-[[nLab:principal bundle]]s on $X$ in terms of smooth functors

$$
  X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \stackrel{g}{\to} \mathbf{B}G
$$

and cocycles for bundles with connection in terms of smooth functors

$$
  \mathbf{P}_1(X) \stackrel{\simeq}{\leftarrow} \mathbf{P}_(C(\{U_i\}))   
  \stackrel{g}{\to} \mathbf{B}G
$$

out of the [[nLab:path groupoid]].

This suggests an evident generalization to higher categorical dimension.

Let $G$ be a strict [[nLab:Lie 2-group]] coming from a [[nLab:crossed module]] $[G_2 \stackrel{\delta}{\to} G_1]$. Then $\mathbf{B}G$ is the strict 2-groupoid coming from the [[nLab:crossed complex]] $[G_2 \to G_1 \stackrel{\to}{\to} *]$.

For instance if $K$ is an [[nLab:abelian group]] then $\mathbf{B}K$ is the 2-group coming from the crossed module $[K \to 1]$ and $\mathbf{B}\mathbf{B}K$ the 2-group coming from the complex $[K \to 1 \to 1]$.

Write $\mathbf{P}_2(X)$ for the smooth [[nLab:path n-groupoid|path 2-groupoid]] of $X$. 

+-- {: .un_prop}
###### Proposition

There is a natural canonical equivalence of [[nLab:2-categories]]

$$
  Smooth2Func(\mathbf{P}_2(X), \mathbf{B}G)
  \simeq
  G Triv2Bund_{\nabla,F_2=0}(X)
$$

where on the right we have the 2-category whose

* objects are pairs $A \in \Omega^1(X,\mathfrak{g}_1)$, 
  $B \in \Omega^2(X,\mathfrak{g}_2)$ such that
  the 2-form curvature 
 
  $$
    F_2(A,B) := d_{dR} A + [A \wedge A] + \delta_* B
  $$

  vanishes

* morphisms $(\lambda,a) : (A,B) \to (A',B')$ 
  are pairs $a \in \Omega^1(X,\mathfrak{g}_2)$, 
  $\lambda \in C^\infty(X,G_1)$ such that
  $A' = \lambda A \lambda^{-1} + \lambda d \lambda^{-1} + \delta_* a$
  and $B' = \lambda(B) + d_{dR} a + [A\wedge a]$

* 2-morphims are ...

=--

This is the [[nLab:2-groupoid of Lie 2-algebra valued forms]] restricted to those [[nLab:Lie 2-algebra]] valued forms whose 2-form curvature vanishes.

Under this equivalence, a 2-functor $tra_{(A,B)}$ factors through the fundamental 2-group $\mathbf{P}_2(X) \to \mathbf{\Pi}_2(X)$ precisely if also the 3-form curvature 

$$
  F_3(A,B) := d_{dR} B + [A \wedge B]
$$

vanishes.

This is in [SchrWalII](http://arxiv.org/abs/0802.0663).

As before, this is entirely natural in $X$, so that we that we get a presheaf of 2-groupoids

$$
  \mathbf{B}G_{diff'} : U \mapsto
  Smooth2Func(\mathbf{P}_2(U), \mathbf{B}G)
  \,.
$$


+-- {: .un_prop}
###### Proposition


Let $\{U_i \to X\}$ be a [[nLab:good open cover]] of $X$ and $C(\{U_i\})$ the corresponding [[nLab:Cech nerve|Cech groupoid]] internal to [[nLab:diffeological space]]s. 

We have a natural equivalence of [[nLab:bicategories]]

$$
  Smooth2Func(\mathbf{P}_2(C(\{U_i\})), \mathbf{B}^2 U(1))
  \simeq
  Smooth2Func(C(\{U_i\}), \mathbf{B}^2 U(1)_{diff'})
  \simeq
  U(1) Gerb_\nabla(X)
  \,,
$$

where on the right we have the bicategory of $U(1)$-[[nLab:bundle gerbe]]s with connection.

=--

This is in [SchrWalIII](http://arxiv.org/abs/0808.1923).

It is immediate to remove by hand the constraint that the 2-form curvature has to vanish, and thereby obtain the full Lie [[nLab:2-groupoid of Lie 2-algebra valued forms]]. All cocycle descriptions go through as before, essentially the only difference now being that there is no constraint on the 2-form curvature on a $G$-principal 2-bundle.

These unconstrained cocycles for [[nLab:automorphism 2-group]] $AUT(H)$-[[nLab:principal 2-bundle]]s (i.e. for $H$-[[nLab:gerbe]]s) have been proposed in [BreMes2001](http://arxiv.org/abs/math/0106083). See the references <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#ConnectionOnNonabelianGerbes">here</a>.

While we can remove this constraint by hand, the question remains what this amounts to conceptually.  In particular: what is the right notion of morphisms / coboundaries between general differential nonabelian 2-cocycles and what classification properties do the resulting cocycle 2-groupoids and cohomology sets have? In order to address these questions, we will now take another look at the relation between connections and their curvature.



#### Curvature characteristics of 1-bundles {#CurvatureCharacteristicsI}

Above we described connections on [[nLab:principal bundle]]s and on [[nLab:gerbe]]s and [[nLab:principal 2-bundle]]s in terms of their [[nLab:parallel transport]] manifested as a smooth $n$-functor out of the [[nLab:path groupoid]] $\mathbf{P}_1(-)$ and the [[nLab:path n-groupoid|path 2-groupoid]] $\mathbf{P}_2(-)$.

From various points of view the [[nLab:fundamental groupoid]] $\mathbf{\Pi}_1(-)$ and the fundamental 2-groupoid $\mathbf{\Pi}_2(-)$ and ultimately the [[homotopy ∞-groupoid]] $\mathbf{\Pi}(-) := \mathbf{\Pi}_{\infty}(-)$ are more fundamental than the [[nLab:path n-groupoid]] $\mathbf{P}_n$. We have seen above for low $n$ that parallel transport on $\mathbf{P}_n$ factors through $\mathbf{\Pi}_n$ precisely if the corresponding connections are flat. This is a drastic restriction, of course. But due to the nice fundamental nature of $\mathbf{\Pi}$, the _obstructions_ to equipping a [[nLab:principal ∞-bundle]] with a flat $\infty$-connection organize themselves neatly into a cohomology theory, namely a [[nLab:twisted cohomology]] theory with the twist being _$\infty$-[[curvature]]_ .  The general abstract definition of differential cohomology as curvature-twisted flat differential cohomology in the precise sense of [[nLab:twisted cohomology]] is our main goal in the sections <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#GroupalCoeffs">Differential cohomology with groupal coefficients</a>/<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#WithCurvatureClasses">with non-groupal coefficients</a>. As a preparation for that general treatment we now look at connections on ordinary bundles along these lines.

To start with, it is worth noticing that in a higher categorical context flat connections do encode a fair amount of non-trivial information. For instance by the above propositions we have for the structure [[nLab:2-group]] $G := \mathbf{E}U(1) = [U(1) \stackrel{id}{\to} U(1)]$ that the parallel surface transport with coefficients in $\mathbf{B}G$ is given by a 1-form $A$ and a 2-form $B$, where $A$ is arbitrary and $B$ is restricted to be the curvature $B = F_A = d_{dR} A$ of $A$. This is quite restrictive as a 2-connection, but it contains all the local information of an unconstrained 1-connection on a [[nLab:line bundle]]! And in fact when regarded as the connection on a line bundle the flatness of the 2-connection $(A,B)$ is an important statement about the 1-connection: it is precisely the [[nLab:Bianchi identity]] $d_{dR} B = d_{dR} F_A = 0$. 

This is the simplest example of a general phenomenon: flat $(n+1)$-connections serve to encode the [[curvature]] of non-flat $n$-connections. 

We shall now systematize this observation and show how line bundles with non-flat connection may be  expressed in terms of flat parallel 2-transport out of the fundamental 2-groupoid $\mathbf{\Pi}_2(-)$. Then we give the analogous discusion for connection on general $G$-principal bundles. It is this description of differential cohomology which we then generalize verbatim to a notion of differential cohomology with coefficients in [[nLab:∞-group]]s in gebenral [[nLab:(∞,1)-topos]]es below.

##### Of $U(1)$-principal bundles {#U1BundCurvatureCharacteristics}

Write $\mathbf{B}U(1) \to \mathbf{E}\mathbf{B}U(1) \to \mathbf{B}^2 U(1)$
for the sequence of smooth 2-groupoids that under the [[nLab:Dold-Kan correspondence]] come from the sequence of chain complexes

$$
  [1 \to U(1) \to 1] \to [U(1) \to U(1) \to 1] \to [U(1) \to 1 \to 1]
  \,.
$$

By the above discussion we have that under the equivalence

$$
  Smooth2Func(\mathbf{P}_2(X), \mathbf{B}\mathbf{E}U(1))
  \simeq
  \mathbf{E}U(1) Triv2Bund_{\nabla}
$$

smooth 2-functors $\mathbf{\Pi}_2(X) \to \mathbf{E}\mathbf{B}U(1)$ correspond to pairs $(A,B)$ with $A \in \Omega^1(X)$, $B \in \Omega^2(X)$ and $B := F_A = d_{dR} A$.

Therefore a morphism

$$
  \array{
    C(\{U_i\}) &\to& \mathbf{B}U(1)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(C(\{U_i\})) &\to& \mathbf{E}\mathbf{B}U(1)
  }
$$

of smooth 2-groupoids is a cocycle for a line bundle equipped with a [[pseudo-connection]]. Forming the [[pasting]] composite

$$
  \array{
    C(\{U_i\}) &\to& \mathbf{B}U(1) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(C(\{U_i\})) &\to& \mathbf{E}\mathbf{B}U(1)
    &\to&
    \mathbf{B}^2 U(1)
  }
$$

projects out the curvature 2-form $\mathbf{\Pi}_2(X) \to \mathbf{B}^2 U(1)$ of this bundle.

Write $\mathbf{B}U(1)_{diff}$ for the 2-groupoid valued presheaf

$$
  \mathbf{B}U(1)_{diff} :
  U
  \mapsto 
  \left\{
  \array{
    U &\to& \mathbf{B}U(1)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{E}\mathbf{B}U(1)
  }
  \right\}
$$

The forgetful morphism $\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B}U(1)_{diff}$ is a weak equivalence. A lift

$$
  \array{
    && \mathbf{B}U(1)_{diff}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
  }
$$

always exists. It corresponds to putting a connection on line bundle. 

Consider also the presheaf

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  :
  U
  \mapsto
  \left\{
    \array{
      U &\to& *
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1)
    }
  \right\}
  \,.
$$


+-- {: .un_prop}
###### Proposition

We have equivalences

$$
  SmoothFunc(C(\{U_i\}), \mathbf{B}U(1)_{diff})
  \simeq
  U(1) Bund(X)
$$

and

$$
  SmoothFunc(C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^2 U(1))
  \simeq
  [\Omega^1(X) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(X)]
  \,.
$$


=--


Forming the above [[nLab:pasting]] composite induces a morphism 

$$
  curv : \mathbf{B}U(1)_{diff} \to \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)
  \,.
$$

In total we have a 2-[[nLab:anafunctor]]

$$
  \mathbf{B}U(1) \stackrel{\simeq}{\leftarrow}
  \mathbf{B}U(1)_{diff} 
  \stackrel{curv}{\to}
  \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)
$$

of smooth 2-groupoids, which we call the [[curvature]] [[nLab:characteristic class]] of $\mathbf{B}U(1)$.

+-- {: .un_prop}
###### Proposition

The 2-groupoid $\mathbf{H}_{diff}(X,\mathbf{B}(1))$ which is
given by the [[nLab:pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1))
    &\to&
    H^2_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    SmoothFunc(C(\{U_i\}), \mathbf{B}U(1)_{diff})
    &\stackrel{curv}{\to}&
    SmoothFunc(C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}U(1))
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    SmoothFunc(C(\{U_i\}), \mathbf{B}U(1))
  }
$$

is the disjoint union over the second de Rham cohomology of $X$ of the groupoids of $U(1)$-principal bundles with curvature 2-form a fixed representative of the given cohomology class.


=--

The general formalism of pseudo-conections in intrinsic differential geometry is at <a href="http://ncatlab.org/schreiber/edit/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#LocalConnectionForms">Differential cohomology -- Local connection forms</a>. Details on the description of $U(1)$-principal bundles are at [[schreiber:differential cohomology in an (∞,1)-topos]] in the paragraph <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#CircleBundlesConnection">Circle bundles with connection</a>.


##### Of $G$-principal bundles 

Above we described connections on $U(1)$-principal bundles as a means to interpolate from cocycles with values in $\mathbf{B}U(1)$ to cocycles with values in $\mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ by passing through a 2-[[nLab:anafunctor]]

$$
  \mathbf{B}U(1)
  \stackrel{\simeq}{\leftarrow}
  \mathbf{B}U(1)_{diff}
  \to
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
$$

of smooth 2-groupoids with codomain the double
[[nLab:delooping]] of $U(1)$. As a reflection of the fact that 
this double delooping exists and is an [[nLab:Eilenberg-MacLane object]]
the curvature detected by this morphism is a single differential 2-form.

However, as soon as the group $U(1)$ is replaced by a _nonabelian_ [[nLab:Lie group]] $G$, such as the
[[nLab:orthogonal group]] $O(n)$ or the [[nLab:unitary group]] $U(n)$,
only the single delooping $\mathbf{B}G$ exists. In this case 
the role of the double delooping in the curvature characteristic class
is played by a different object whose conceptual nature we survey below in 
the section on [curvature characteristic classes](#CurvatureClasses). For the moment here we shall be content with a somewhat ad hoc definition of this coefficient object.

What is straightforward to see is what object should replace $\mathbf{B}U(1)_{diff}$. We shall write $INN(G)$ for the [[nLab:Lie 2-group]]
coming from the [[nLab:crossed module]] $[G \stackrel{Id}{\to} G]$. This may be thought of as a [[nLab:groupal model for universal principal ∞-bundles|groupal model for the universal G-principal bundle]]. 

As a special case of the above propositon on smooth 2-functors, we have that under the equivalence

$$
  Smooth2Func(\mathbf{P}_2(U), \mathbf{B}INN(g))
  \stackrel{\simeq}{\to}
  INN(G) Triv2Bund_{flat}(U)
$$

smooth 2-functors $\mathbf{\Pi}_2(U) \to \mathbf{B}INN(G)$ are identified with pairs $(A,B)$ consisting of

* a $\mathfrak{g}$-valued 1-form $A \in \Omega^1(U,\mathfrak{g})$;

* a $\mathfrak{g}$-valued 2-form $B \in \Omega^2(U,\mathfrak{g})$;

* subject to the constraint that 

  * $B = F_A$ is the [[nLab:curvature]] 2-form of $A$;

  * $d B + [A \wedge B] = 0$.

While this is a flat connection as a 2-connection, it does encode precisely the datum of a general local 1-connection. Moreover, the flatness of the 2-connection is precisely the [[nLab:Bianchi identity]] of the 1-connection.

This might suggest that we can model a $G$-principal 1-bundle with arbitrary connection in terms of functors $\mathbf{\Pi}_2(C(\{U_i\})) \to \mathbf{B}INN(G)$. However, it is a bit more subtle than that: in particular the object $\mathbf{B}INN(G)$ is weakly equivalent to the point, $\mathbf{B}INN(G)$. In fact $INN(G)$ equipped with the canonical projectin $INN(G) \to \mathbf{B}G$ is a multiplicative model for the _universal_ $G$-[[nLab:principal 2-bundle]]. This means that _up to homotopy_ , 2-functors $tra_{A,F_A} : \mathbf{\Pi}_2(U) \to \mathbf{B} INN(G)$ are all trivial. 

We can see this concretely by again invoking the above explicit equivalence of 2-categories: under this equivalence a transformation

$$
  tra_((A,F_A)) \Rightarrow tra_{(A',F_{A'})}
$$

corresponds precisely to a pair $(\lambda,a)$ with

* $\lambda \in C^\infty(U,G)$ 

* $a \in \Omega^1(U,\mathfrak{g})$ 

such that

$$
  A' = \lambda A \lambda^{-1} + \lambda d \lambda^{-1} + a
  \,.
$$
 
Except for the last term, this is the equation for a gauge
transformation of a connection 1-form. The last summand, however,
is an arbitrary _shift_ of the connection. Simply by choosing $a$
appropriately we find for every 2-functor $tra_{(A,F_A)}$ a transformation
to the trivial one $tra_{(0,0)}$.

This means that by itself, $Smooth2Func(\mathbf{P}_2(U), \mathbf{B}INN(G))$ is a resolution of the point, in much the same way as a  [[nLab:generalized universal bundle|universal bundle]] is a resolution of a point. In both cases the relevance of these objects is as a means to model a higher categorical operation by a strict rpresentative.

Concretely, in our situation the object we can build using 2-functors $\mathbf{\Pi}_2(U) \to \mathbf{B}INN(G)$ is $\mathbf{B}G_{diff}$, a resolution of $\mathbf{B}G$ that interpolates between $\mathbf{B}G$ and its curvature characteristics.

Consider the category $\mathbf{B}G_{diff}(U)$ whose

* objects are commuting diagrams

  $$
    \array{
      U &\to& \mathbf{B}G
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B} INN(G)
    }
  $$

  in the category of diffeological 2-groupoids;

* morphisms are homotopies of diagrams

  $$
    \array{
      U &{{\nearrow \searrow} \atop {\to}}& \mathbf{B}G
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &{{\nearrow \searrow} \atop {\to}}& \mathbf{B} INN(G)
    }
    \,.
  $$

* 2-morphisms are modification of such homotopies.

We may think of the lower horizontal morphism as encoding arbitrary local connection forms and arbitrary gauge transformations and shifts of these. But since it is constrained to fit into this commuting diagram, the components $\lambda$ of the gauge transformations themselves are constrained to compose without themselves being shifted.

Precisely: under the above equivalences, the groupoid $\mathbf{B}G_{diff}$ is identified as follows:

* objects are 1-forms $A \in \Omega^1(U,\mathfrak{g})$;

* morphisms $(\lambda,a) : A \to A'$ are pairs consisting of functions $\lambda \in C^\infty(U,G)$ and 1-forms $a \in \Omega^1(U,\mathfrak{g})$

  such that $A' = \lambda A \lambda^{-1} + \lambda d \lambda^{-1} + a$

* there are _no_ non-trivial 2-morphisms (while these are present in $INN(G)Triv2Bund_\nabla(U)$).

One sees that the evident projection function

$$
  \mathbf{B}G_{diff}(U) \to \mathbf{B}G(U)
$$

is [[nLab:essentially surjective functor|essentially surjective]], [[nLab:full and faithful functor|full and faithful]], precisely because of the presence of the connection shift form $a \in \Omega^1(U,\mathfrak{g})$ in the definition of the morphisms.

All this is functorial in $U$, so that in summary we have found a weak equivalence

$$
  \mathbf{B}G \stackrel{\simeq}{\leftarrow}
  \mathbf{B}G_{diff}
$$

of smooth 2-grupoids. The above discussion shows that a lift $\nabla$ of a $G$-cocycle $g$ through this equivalence

$$
  \array{
    && \mathbf{B}G_{diff}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

is precisely a choice of _pseudo-connection_ on a [[nLab:Cech cohomology|Cech-cocycle]] for a $G$-[[nLab:principal bundle]]: a choice on each patch $U_i$ of a 1-form $A_i \in \Omega^1(U_i, \mathfrak{g})$.

There is, at this point, _no_ condition on the compatibility of these 1-forms on double intersections $U_i \cap U_j$. Therefore the term "pseudo-connection". 


As we shall discuss below in the section [∞-Lie algebra valued connectons](#LieConnections), we can find a natural morphism 

$$
  ch_G : \mathbf{B}_{diff}G \to (\mathbf{\Pi}\mathbf{B}G)\otimes \mathbb{R} \simeq \prod_i \mathbf{B}^{n_i}\mathbb{R}
$$ 

into a natural curvature coefficient object. This way the differential cocycle becomes represented by a diagram of the form

$$
  \array{
    Y &\stackrel{g}{\to}& \mathbf{B}G &&& underlying\;cocycle
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(Y) &\to& \mathbf{B}INN(G) &&& connection\;and\;curvature
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}(X) &\to&  \prod_i \mathbf{B}^{n_i} \mathbb{R}
    &&&
    curvature\;characteristic\;forms
  }
  \,.
$$


The cocycles in the bottom have equivalent representatives in ordinary [[nLab:de Rham cohomology]]. And in the [[nLab:homotopy fiber]] of $ch_G$ over these nice representatives, we find those $G$-cocycles with pseudo-connection whose pseudo-connection is in fact a genuine connection.

In order to describe this curvature characteristic class, we now invoke [below](#LieConnections) a little bit of [[nLab:Chern-Weil theory]]
with the tools of  [[nLab:∞-Lie theory]].


### Circle $n$-bundles with connection {#CirclenBundles}

In the abelian case it is easy to generalize the above construction to higher degrees.

use [[Dold-Kan correspondence]] to construct

$\mathbf{B}^n U(1) := \Xi U(1)[n]$

$\mathbf{B} INN(U(1)) = \Xi (U(1) \to U(1))[n]$

Then form

$$
  \mathbf{B}^n U(1)_{diff}
  =
  U \mapsto
  \left\{
      U &\to& \mathbf{B}^n U(1)
     \\
     \downarrow && \downarrow
     \\
     \mathbf{\Pi}(U) &\to& \mathbf{B}^n INN(U(1))
  \right\}
$$

(...)

see [[circle n-bundle with connection]]

### $\infty$-Lie algebra valued connections {#LieConnections}

Above we considered connections encoded in terms of [[nLab:parallel transport]] along paths and surfaces, and saw that this definition implies that connections are locally given by [[nLab:Lie-algebra valued 1-forms]] [[nLab:Lie 2-algebra valued differential forms]].

Now we pass to what is to some extent the reverse construction: we define a notion of [[schreiber:∞-Lie algebroid valued differential forms]] and show how by a variant of [[nLab:Lie integration]] these define parallel transport and connections on higher bundles.

The material here was considered in

* [[Hisham Sati]], [[Urs Schreiber|U.S.]], [[Jim Stasheff]],
  _$L_\infty$-algebra connections_ in Fauser (eds.) Recent Developments in QFT, Birkh&#228;user ([arXiv:0801.3480](http://arxiv.org/abs/0801.3480))

and further studied in 

* [[nLab:Hisham Sati]], [[nLab:Urs Schreiber|U.S.]], [[nLab:Jim Stasheff]], _Twisted differential String- and Fivebrane structures_ ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001)).

In the main entry [[∞-Chern-Weil theory]] we discuss how this dg-algebraic construction follows from a general abstract definitions of [[schreiber:differential cohomology in an (∞,1)-topos]].

  
#### $\infty$-Lie algebras

An ordinary [[Lie algebra]] is an [[infinitesimal space|infinitesimal]] approximation to a [[Lie group]]. This statement generalizes as we pass to higher groupoids. 

We had already seen above the infinitesimal approximation of a [[Lie 2-group]]: this is a [[nLab:Lie 2-algebra]]. If the Lie 2-group is a smooth [[strict 2-group]] it is encoded equivalently by a [[crossed module]] of ordinary Lie groups, and the corresponding [[Lie 2-algebra]] is given by a [[differential crossed module]] of ordinary [[Lie algebra]]s.

One categorical dimension higher, a semistrict 3-group -- a [[nLab:Gray group]] -- is encoded by a [[2-crossed module]] of ordinary groups, and its infinitesimal approximation is a Lie 3-algebra which is encoded by a [[differential 2-crossed module]] of ordinary Lie algebras.

If instead of [[vertical categorification|vertically]] we move in [[horizontal categorification|horizontally]] in categorical dimension we find that the infinitesimal approximation to a [[nLab:Lie groupoid]] is a [[nLab:Lie algebroid]]. 

And going in both directions: the infinitesimal approximatin to a Lie 2-groupoid is a _Lie 2-algebroid_ . Famous examples of these are for instance [[nLab:Courant algebroid]]s.

All these algebraic notions are special cases of the general notion of [[nLab:∞-Lie algebroid]]s, which are precisely the infinitesimal approximations to general [[nLab:∞-Lie groupoid]]s. The infinitesimal approximation of a general [[nLab:∞-Lie group]] is an [[nLab:∞-Lie algebra]], usually called an _$L_\infty$-algebra_ . The general study of these concepts and their interrelation is the topic of [[schreiber:Lie theory in an (∞,1)-topos]]. Here we shall for the moment concentrate on describing $\infty$-Lie algebras.

One way to approach the definition of $\infty$-Lie algebras starts with the following standard observation:

+-- {: .un_prop}
###### Observation

For $\mathfrak{g}$ a vector space, write $\vee^\bullet \mathfrak{g}$ for the [[nLab:free construction|free]] graded-co-commutative [[nLab:coalgebra]] on $\mathfrak{g}$, with $\mathfrak{g}$ regarded as being in degree -1. (Over a field of [[nLab:characteristic]] 0, its underlying vector space is isomorphic to that of the [[nLab:exterior algebra]] $\wedge^\bullet \mathfrak{g}$, but we shall write $\vee^\bullet \mathfrak{g}$ to remind us of the coalgebra structure. )

Then structures of a [[nLab:differential graded coalgebra]] on $\vee^\bullet \mathfrak{g}$ given by co[[nLab:derivation]]s $D : \vee^\bullet \mathfrak{g} \to \vee^\bullet \mathfrak{g}$ of degree +1 and with $D \circ D = 0$, are in bijection with structures of a [[nLab:Lie algebra]] on $\mathfrak{g}$:

the restriction $D : \mathfrak{g} \vee \mathfrak{g} \to \mathfrak{g}$ encodes precisely a skew symmetric bracket and $D$ is entirely fixed by this restriction, and the condition $D^2  = 0$ is equivalent to the [[nLab:Jacobi identity]] satisfied by this bracket.

=--

This way of looking at Lie algebras suggests an evident generalization:

+-- {: .un_def}
###### Definition
**($L_\infty$-algebra)**

An _[[nLab:L-∞-algebra]]_ is an $\mathbb{N}$-[[nLab:graded vector space]] $\mathfrak{g}$ (which we take to be in non-positive degree) equipped a coderivation $D : \vee^\bullet \mathfrak{g} \to \vee^\bullet \mathfrak{g}$ of degree +1 with $D^2 = 0$.

=--

We say that $\mathfrak{g}$ is of [[nLab:finite type]] if it is degreewise finite-dimensional. In that case degreewise linear dualization of vector spaces maps the free graded-commutative coalgebra $\vee^\bullet \mathfrak{g}$ to the [[nLab:Grassmann algebra]] 

$$
  \wedge^\bullet \mathfrak{g}^*
  = 
  k
  \oplus (\mathfrak{g}^*_0)
  \oplus (\mathfrak{g}_0^* \wedge \mathfrak{g}_0^* \oplus \mathfrak{g}_1^*)
  \oplus 
  (\mathfrak{g}^*_0 \wedge \mathfrak{g}^*_0 \wedge \mathfrak{g}^*_0
   \oplus \mathfrak{g}^*_1 \otimes \mathfrak{g}^*_0
   \oplus \mathfrak{g}^*_2)
  \oplus
  \cdots
  \,,
$$

where the $n$th term in paranthesis is in degree $n$, and the dual $d = D^* : \wedge^\bullet \mathfrak{g}^* \to \wedge^\bullet \mathfrak{g}^*$ of the coderivation, acting as $d \omega = \omega(D(-))$, makes this a graded-commutative [[nLab:semifree dga|semifree]] [[nLab:differential graded algebra]]. This we write

$$
  CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{g}^* , d_{\mathfrak{g}})
$$

and call the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$. (For $\mathfrak{g}$ an ordinary Lie algebra, this is the ordinary notion of Chevalley-Eilenberg algebra over the trivial module.)

In fact, this construction establishes a _bijection_ between [[nLab:semifree dga]]s in non-negative degree and [[nLab:∞-Lie algebra]]s: every semifree dg-algebra is the Chevalley-Eilenberg algebra of some -- uniquely specified -- $L_\infty$-algebra.

While equivalent, the dual description is more familiar in the literature., notably due to all the rich supply of techniques from [[nLab:Sullivan model]]s in [[nLab:rational homotopy theory]]. In fact the notion of [[nLab:Lie integration]] (see there for details and references) of $L_\infty$-algebras to [[nLab:∞-Lie groupoid]]s may be understood as being essentially nothing but the [[nLab:Sullivan construction]] in rational homotopy theory. 

Therefore we shall often think of $\infty$-Lie alghebras dually in terms of their Chevalley-Eilenberg algebras. Notably we identify the standard [[nLab:model structure on dg-algebra]] as a [[nLab:presentable (∞,1)-category|presentation]] of the [[nLab:(∞,1)-category]] of $\infty$-Lie algebras, which we write

$$
  \infty Lie Alg := (dgAlg^{op})^\circ
  \,.
$$

#### $\infty$-Cartan-Chern-Weil theory

The notion of [[nLab:Lie algebra cohomology]] has a straightforward generalization to a notion of [[nLab:∞-Lie algebra cohomology]]. In fact, in the light of $\infty$-Lie algebras, the concept becomes simpler.

For $n \in \mathbb{N}$ we write $b^n \mathbb{R}$ for the $\infty$-Lie algebras defined as follows: it's [[nLab:Chevalley-Eilenberg algebra]] is generated from a single element $c$ in degree $n$ and has vanishing differential

$$
  CE(b^{n-1}\mathbb{R}) = (\wedge^\bullet \langle c\rangle, d = 0)
  \,.
$$

This is effectively the [[nLab:Eilenberg-MacLane object]] $K(n,\mathbb{R})$ in the [[nLab:(∞,1)-category]] of $\infty$-Lie algebras. For $\mathfrak{g}$ any $\infty$-Lie algebra, we say that an $n$-cocycle on $\mathfrak{g}$ is a morphism

$$
  \mu : \mathfrak{g} \to b^n \mathbb{R}
$$

of $\infty$-Lie algebras. Dually, this is a morphism of [[nLab:dg-algebra]]s

$$
  CE(\mathfrak{g}) \leftarrow CE(b^n \mathbb{R}) : \mu
$$

between the [[nLab:Chevalley-Eilenberg algebra]]s. By the nature of $CE(b^n \mathbb{R})$ this in turn is the same as an element

$$
  \mu \in \wedge^n \mathfrak{g}^*
$$

in $CE(\mathfrak{g})$ of degree $n$, which is closed

$$
  d_\mathfrak{g} \mu = 0
  \,.
$$

For $\mathfrak{g}$ an ordinary [[nLab:Lie algebra]] this is traditionally taken as the very definition of [[nLab:Lie algebra cohomology]] (with values in the trivial module): the [[nLab:chain homology and cohomology|cochain cohomology]] of the Chevalley-Eilenberg complex. For our purposes it is useful to emphasize the equivalent description in terms of morphisms of $\infty$-Lie algebas:

there is a precise sense in which an [[nLab:∞-Lie algebra]] is an [[nLab:infinitesimal space|infinitesimal]] [[nLab:∞-Lie group]]]. As we shall discuss below in [Cohomology](#Cohomology), the latter are naturally objects in an [[nLab:(∞,1)-topos]] of [[nLab:∞-Lie groupoid]]s and every $(\infty,1)$-topos comes with its [[nLab:cohomology|intrinsic cohomology]], where an [[nLab:cocycle|intrinsic cocycle]] on an object $X$ with coefficients in an object $A$ is nothing but a morphism $X \to A$. Our general definition of [[schreiber:differential cohomology in an (∞,1)-topos]] is built on this fact.

In such generality we may in fact think of any morphism $\mathfrak{g} \to \mathfrak{h}$ of $\infty$-Lie algebras as a _cocycle_ on $\mathfrak{g}$ with values in $\mathfrak{h}$, even if $\mathfrak{h}$ is not an [[nLab:Eilenberg-MacLane object]]. Such a general notion of cohomology is known as [[nLab:nonabelian cohomology]]. And indeed, restricted to the case that $\mathfrak{g}$ is an ordinary Lie algebra, this reproduces the notion of [[nLab:nonabelian Lie algebra cohomology]].

Every (nonabelian) cocyle $\mu : \mathfrak{h} \to \mathfrak{g}$ classifies something: its [[nLab:homotopy fiber]]. This is the [[nLab:homotopy pullback]] $\mathfrak{p} \to \mathfrak{h}$ of the point along $\mu$:

$$
  \array{
     \mathfrak{p} &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathfrak{h} &\stackrel{\mu}{\to}& \mathfrak{g}
  }
  \,.
$$

This $\mathfrak{p} \to \mathfrak{h}$ is the _extension_ of $\mathfrak{h}$ by the [[nLab:loop space object]] $\Omega \mathfrak{g}$ of $\mathfrak{g}$ that is classified by the cocycle.

There is a standard algorithm for computing such [[nLab:homotopy pullback]]s in terms of ordinary pullbacks of [[nLab:resolution]]s. For that, one finds an $\infty$-Lie algebra $inn(\mathfrak{g})$ and a morphism $inn(\mathfrak{g}) \to \mathfrak{g}$ such that this morphism is a fibration in the ambient [[nLab:model category|model category structure]] and such that we have a diagram

$$
  \array{
    inn(\mathfrak{g}) &\stackrel{\simeq}{\to}& *
    \\
    \downarrow && \downarrow
    \\
    \mathfrak{g} &\stackrel{=}{\to}& \mathfrak{g}
  }
  \,,
$$

where the top morphism is a weak equivalence. Such an object $inn(\mathfrak{g})$ is a [[nLab:universal principal ∞-bundle]]. In fact, here it is a [[nLab:groupal model for universal principal ∞-bundles|groupal universal principal ∞-bundle]] in a sense, in that it carries the structure of an $\infty$-Lie algebra.

There is a standard choice for $inn(\mathfrak{g})$. This is such that its [[nLab:Chevalley-Eilenberg algebra]] is the [[nLab:Weil algebra]] of $\mathfrak{g}$: $CE(inn(\mathfrak{g})) = W(\mathfrak{g})$. This is the [[nLab:semifree dga]] whose underlying graded algebra is $\wedge^\bullet( \mathfrak{g}^* \oplus \mathfrak{g}^*[1] )$, and whose differential is the one uniquely fixed by the fact that its restriction to $\wedge^1 \mathfrak{g}^*$ is $d_{inn(\mathfrak{g})} = d_{\mathfrak{g}} + \sigma$, where $\sigma : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ is the canonical degree shift morphism.

In <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntUnivBund">∞-Lie groupoid -- the Lie-integrated universal principal ∞-bundle</a> we discuss how under [[nLab:Lie integration]] the $\infty$-Lie algebra $\mathfrak{g}$ turns into the one-object [[nLab:delooping]] $\infty$-groupoid $\mathbf{B}G$ of the corresponding [[nLab:∞-Lie group]], while $inn(\mathfrak{g})$ integrates to the delooping $\mathbf{B}\mathbf{E}G$ of a [[nLab:groupal model for universal principal ∞-bundles|groupal model]] for the $G$-[[nLab:universal principal ∞-bundle]] $\mathbf{E}G$.

We may think of $CE(\mathfrak{g})$ as the 
<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#CanonmicalFormOnG">left-invariant differential forms on the ∞-Lie group</a> $G$, and of $W(\mathfrak{g}) = CE(inn(\mathfrak{g}))$ correspondingly as the canonical forms on the $G$-[[nLab:universal principal ∞-bundle]]. For $G$ an ordinary [[nLab:Lie group]] this statement of course goes all the way back to [[nLab:Élie Cartan]].

We obtain the following picture.

$$
  \array{
    delooped\; \infty group
    &&&
    \mathbf{B}G && \mathfrak{g} && 
    CE(\mathfrak{g}) &&& Chevalley-Eilenberg\;algebra
    \\
    &&& \downarrow && \downarrow && \uparrow 
    \\
    delooped\;groupal\;universal\;\infty bundle
    &&&
    \mathbf{B E}G && 
     inn(\mathfrak{g}) 
     &&
     W(\mathfrak{g}) = CE(inn(\mathfrak{g})) &&& Weil\;algebra
    \\
    &&&
    \downarrow 
      &&
    \downarrow 
      &&
    \uparrow
    \\
    rationalized\;classifying\;space
    &&&
    \prod_i \mathbf{B}^{n_i} \mathbb{R} 
    &&
    \prod_i b^{n_i-1} \mathbb{R}
    && inv(\mathfrak{g})
    &&&
    algebra\;of\;invariant\;polynomials
    \\
    \\
    &&&
    &\stackrel{Lie integration}{\leftarrow}& 
  }
$$

Here we added in the bottom row the [[nLab:invariant polynomial]]s on the $\infty$-Lie algebra $\mathfrak{g}$. This are those elements of the [[nLab:Weil algebra]] that are invariant under the action of $\mathfrak{g}$ on $inn(\mathfrak{g})$ in a strong sense. The corresponding $\infty$-Lie algebra is a collection of abelian $\infty$-Lie algebras $\prod_i b^{n_i-1}\mathbb{R}$, one factor for each indecomposable invariant polynomial. 

This may be understood as an approximation to the in general not existent _double_ delooping $\mathbf{B} \mathbf{B}G$ of $G$. We may think of the invariant polynomials as differential forms on $\mathbf{B}G$ itself.

+-- {: .un_prop}
###### Classical fact

For $G$ a [[nLab:compact space|compact]] [[nLab:Lie group]], the [[nLab:rationalization]] $\mathcal{B}G \otimes \mathbb{R}$ of the [[nLab:classifying space]] $\mathcal{B}G$ is the [[nLab:rational space]] whose [[nLab:Sullivan model]] is given by the algebra $inv(\mathfrak{g})$ of [[nLab:invariant polynomial]]s on the [[nLab:Lie algebra]] $\mathfrak{g}$.

=--

The projection morphism

$$
  inn(\mathfrak{g}) \to \prod_i b^{n_i} \mathbb{R}
$$

we shall now identify as inducing the $\infty$-Lie theoretic analog of the [[nLab:Chern-Weil homomorphism]] which computes [[nLab:curvature characteristic form]]s from connections on [[nLab:principal ∞-bundle]]s.


#### The $\infty$-Chern-Weil homomorphism {#ChernWeilHomomorphism}


It had been known in parts of the literature for a long time that there is a nice way to think of the integration of a [[nLab:Lie algebra]] to a [[nLab:Lie group]] in terms of forming _paths_  in the Lie algebra, equivalently, in terms of flat [[nLab:Lie-algebra valued 1-forms]]. But the full impact of this observation only became manifest when the procedure was generalized to [[nLab:Lie algebroid]]s and [[nLab:∞-Lie algebra]]s. (See the discussion and references at [[nLab:Lie integration]].)


For $X$ a [[nLab:smooth manifold]], write $T X$ for its [[nLab:tangent Lie algebroid]]. For $\mathfrak{g}$ any [[nLab:∞-Lie algebra]], we say that a morphism

$$
  \omega : T X \to \mathfrak{g}
$$

is a collection of _flat_ $\mathfrak{g}$-[[∞-Lie algebroid valued differential forms|valued 1-forms]]. In the special case that $\mathfrak{g}$ is an ordinary Lie algebra, this reduces to the standard notion of [[nLab:Lie-algebra valued 1-form]]s on $X$ whose [[nLab:curvature]] 2-form vanishes.

We shall see in <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#ParallelTransport">∞-Lie groupoid parallel transport</a> that the [[nLab:Lie integration]] of such _cocycles_ on the [[nLab:tangent Lie algebroid]] are the [[nLab:infinitesimal space|infinitesimal]] anlog of the flat [[nLab:parallel transport]]

$$
  \mathbf{\Pi}(X) \to \mathbf{B}G
$$

that we considered above in [Parallel transport in low dimensions](#LowDimension).

Accordingly, we may say that an abstract _path_ in $\mathfrak{g}$ is a morphism

$$
  T \Delta^1_{diff} \to \mathfrak{g}
  \,,
$$

where by $\Delta^n_{diff}$ we denotes the standard $n$-[[nLab:simplex]] regarded as a smooth manifold (striictly speaking: with boundary and corners, but in fact we may restrict attention to paths that are constant perpendicular to any boundary in a neighbourhood of that boundary). Accordingly, a 2-dimensional path or homotopy between such paths is a morphism

$$
  T \Delta^2_{diff} \to \mathfrak{g}
$$

that restricts to given paths on the boundary of the 2-simplex. If we consider paths modulo such homotopies, we obtain the [[nLab:fundamental groupoid]] of $\mathfrak{g}$. It is a central fact this is the one-object grouoid $\mathcal{B}G = \{\bullet \stackrel{g}{\to} \bullet | g \in G\}$ whose set of morphisms is the set of elements of the simply-connected Lie group that integrates $G$ in ordinary [[nLab:Lie theory]].

If instead we do not divide out homotopies, we obtain an full [[nLab:∞-groupoid]] given by the [[nLab:Kan complex]]

$$
  [n] \mapsto \left\{ T \Delta^n \to \mathfrak{g}\right\}
  \,.
$$

Dually, in terms of [[nLab:Chevalley-Eilenberg algebra]]s this is 

$$
  [n] \mapsto Hom_{dgAlg}{CE(\mathfrak{g}), \Omega^\bullet(\Delta^n)}
  \,.
$$

There is a natural way to define a _smooth family_ of such paths parameterized over a smooth test space $U$. We write

$$
  \exp(\mathfrak{g}) : U,n \mapsto
  Hom_{dgAlg}{CE(\mathfrak{g}), C^\infty(U) \otimes'\Omega^\bullet(\Delta^n)}
  \,.
$$

We shall see later (...) that this is a [[simplicial presheaf]] which represents the $\infty$-Lie algebra $\mathfrak{g}$ as an [[∞-Lie groupoid]].

There is a somewhat bigger version of this, which is however weakly equivalent


$$
  \exp(\mathfrak{g})_{diff}
  : 
   U, n
 \mapsto 
  \left\{
    \array{
       C^\infty(U)\otimes \Omega^\bullet(\Delta^n_{Diff})
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

This assigns to a smooth test space $U$ the $\infty$-groupoid whose objects are non-flat $\mathfrak{g}$-valued forms, morphisms are paths of gauge transformations of these, 2-morphisms are homotopies of paths of gauge transformations, and so on.

We have that $\exp(\mathfrak{g})_{diff}$ is a [[nLab:resolution]] of $\exp(\mathfrak{g})$ 

$$
  \exp(\mathfrak{g}) \stackrel{\simeq}{\leftarrow}
  \exp(\mathfrak{g})_{diff}
  \,.
$$

We also consider the object

$$
  \mathbf{\flat}_{dR} \prod_i \exp(b^{n_i-1}\mathbb{R})
  : 
  U,n
  \mapsto
  \left\{
    \array{
       C^\infty(U)\otimes \Omega^\bullet(\Delta^n_{Diff})
       &\leftarrow&
       0
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^n_{Diff})
      &\leftarrow&
      inv(\mathfrak{g})
    }
  \right\}
  \,.
$$

We have then a natural [[nLab:anafunctor|anamorphism]]

$$
  ch_{\exp(\mathfrak{g})}
  :
  \exp(\mathfrak{g}) 
   \stackrel{\simeq}{\leftarrow}
  \exp(\mathfrak{g})_{diff}
  \to
  \mathbf{\flat}_{dR} \prod_i \exp(b^{n_i-1}\mathbb{R}) 
$$

given by pasting-postcomposition with the universal $\mathfrak{g}$-princicpal $\infty$-bundle

$$
  \array{
    CE(\mathfrak{g}) &\leftarrow& 0
    \\
    \uparrow && \uparrow
    \\
     W(\mathfrak{g}) &\leftarrow& inv(\mathfrak{g})
  }
  \,.
$$

This descends to the $\infty$-Lie groups integrating $\mathfrak{g}$ and obtained by truncation of $\exp(\mathfrak{g})$

$$
  ch_{G}
  :
  \mathbf{B}G
   \stackrel{\simeq}{\leftarrow}
  \mathbf{B}_{diff}G
  \to
  \mathbf{\flat}_{dR} \prod_i \mathbf{B}^{n_i}\mathbb{R}
  \,.
$$


This is the **$\infty$-Chern-Weil homomorphism**.


The details of this are described at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#ChernWeilHomomorphism">∞-Lie groupoid -- Chern-Weil homomorphism</a>


For $X$ a smooth manifold, we have that 

$$
  X \stackrel{\simeq}{\leftarrow}
  Y
  \to \mathbf{B}G
$$

is the cocycle for a $G$-[[nLab:principal ∞-bundle]]. A lift (which always exists) to 

$$
  X \stackrel{\simeq}{\leftarrow}
  Y
  \to \mathbf{B}_{diff}G
$$

is a _connection_ on this principal $\infty$-bundle. The projection

$$
  X \stackrel{\simeq}{\leftarrow}
  Y
  \to \mathbf{B}_{diff}G
  \stackrel{ch_G}{\to}
  \mathbf{\flat}_{dR} \prod_i \mathbf{B}^{n_i} \mathbb{R}
$$

are the corresponding [[nLab:curvature characteristic form]]s. They are locally obtained by projecting in the diagram


$$
  \array{
    C^\infty(U)\otimes' \Omega^\bullet(\Delta^n)
    &\leftarrow&
    CE(\mathfrak{g})
    &&&
    flat\;vertical\;form
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^n)
    &\leftarrow&
    W(\mathfrak{g})
    &&&
    connection\;and\;curvature
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^n)
    &\leftarrow&
    inv(\mathfrak{g}) 
    &&&
    curvature\;characteristic\;forms
 }
$$

from the top two thirds to the bottom row. In this form $\infty$-Lie algebra valued connections were considered in <a href="http://arxiv.org/abs/0801.3480">SSSI</a>. 

### Example: Chern-Simons circle 3-bundle {#ChernSimons3Bund}

* [[Chern-Simons circle 3-bundle]]


## Summary

This section gives a concise summary of the constructions introduced above.

### For $G$-principal 1-budles

We have the following [[diffeological n-groupoid|diffeological 1- or 2-groupoids]].

* $\mathbf{\Pi}_1(X)$ -- the [[fundamental groupoid]] of $X$;

* $\mathbf{P}_1(X)$ -- the [[path groupoid]] of $X$

* $\mathbf{\Pi}_2(X)$ the [[path n-groupoid|fundamental path 2-groupoid]].

Let $G$ be a [[Lie group]]. We have the following Lie groupoids associated with that

* $\mathbf{B}G$ -- the coefficient for $G$-[[principal bundle]]s;

* $INN(G) = G//G$ -- the [[inner automorphism 2-group]] of $G$, a [[groupal model for universal principal infinity-bundles|groupal model for the universal principal bundle]];

* $\mathbf{B}INN(G)$ -- the coeffiecient for $INN(G)$-[[principal 2-bundle]];

* $\mathbf{B}G_{conn} := Hom_(Grpd(Diffeo))(\mathbf{P}_1(-), \mathbf{B}G)$ -- the coefficient for $G$-principal bundles with [[connection on a bundle|connection]];

* $\mathbf{\flat} \mathbf{B}G := Hom_{Grpd(Diffeo)}(\Pi_2(-), \mathbf{B}INN(G))$ the coefficient for flat $G$-principal bundles with flat connection;

* $\mathbf{\flat} \mathbf{B}INN(G) := [\Pi_2(-), \mathbf{B}INN(G)]$ the coefficient for flat $INN(G)$-principal 2-bundles;

* $\mathbf{B}G_{diff} := \mathbf{\flat}\mathbf{B}INN(G) \times_{\mathbf{B}INN(G)} \mathbf{B}G $ -- the coefficient for $G$-[[principal bundle]]s with [[pseudo-connection]];


We have the following morphisms between these:

* $X \to \mathbf{P}_1(X)$ -- includion of constant paths into all paths;

* $\mathbf{P}_1(X) \to \mathbf{\Pi}_1(X)$ -- sends [[thin homotopy]]-classes of paths to their full homotopy classes;

* $\mathbf{\flat}\mathbf{B}G \to \mathbf{B}G_{conn}$ -- the morphism induced by that which forgets that a connection is flat;

* $\mathbf{B}G_{conn} \to \mathbf{B}G$ -- forgets the connection on a $G$-bundle, induced locally by $U \to \mathbf{P}_1(U)$;

* $\mathbf{B}G_{conn} \to \mathbf{\flat} \mathbf{B}INN(G)$ -- the morphism that fills in the integrated curvature between paths enclosing a surface;

* $\mathbf{B}G_{conn} \to \mathbf{B}G_{diff}$ the morphism that regards an ordinary connection as a special case of a pseudo-connection, induced as a morphism into a pullback by the two morphisms $\mathbf{B}G_{conn} \to \mathbf{B}G$ and $\mathbf{B}G_{conn} \to \mathbf{\flat} \mathbf{B}INN(G)$;



### For the $\infty$-Chern-Weil homomorphism {#CWHomomorphismSummary}

For $\mathfrak{g}$ an [[∞-Lie algebra]] we have the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$, the [[Weil algebra]] $W(\mathfrak{g})$ and the algebra of [[invariant polynomial]]s $inv(\mathfrak{g})$, with canonical morphisms

$$
  \array{
    CE(\mathfrak{g})  &&& G
    \\
    \uparrow &&& \downarrow 
    \\
    W(\mathfrak{g}) &&& \mathbf{E}G
    \\
    \uparrow &&& \downarrow
    \\
    inv(\mathfrak{g}) &&& \mathbf{B}G
  }
  \,.
$$

A [[cocycle]] $\mu$ in the [[∞-Lie algebra cohomology]] of $\mathfrak{g}$ coming by transgression from an [[invariant polynomial]] $\langle - \rangle_\mu$ mediated by a Chern-Simons element $cs_\mu$ is exhibited by a diagram

$$
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
     CE(b^{k} \mathbb{R})
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{cs_\mu}{\leftarrow}&
     W(b^k \mathbb{R})
     \\
     \uparrow && \uparrow
     \\
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle_\mu}{\leftarrow}&
     inv(b^k \mathbb{R}) & = CE(b^{k+1} \mathbb{R})
  }
  \,.
$$

A connection with values in $\mathfrak{g}$ is encoded by [[simplicial presheaves]] of [[∞-Lie algebra valued differential forms]] that assign sets of diagrams of the form

$$
  \array{
     C^\infty(U)\otimes \Omega^\bullet(\Delta^n)
     &\stackrel{A_{vert}}{\leftarrow}&
     CE(\mathfrak{g})
     &&&
     transition\;function\;/\;Cech\;cocycle
     \\
     \uparrow && \uparrow
     \\
     \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
     &\stackrel{A}{\leftarrow}&
     W(\mathfrak{g})
     &&& 
     connection
     \\
     \uparrow && \uparrow
     \\
     (\Omega^\bullet(U)\otimes C^\infty(\Delta^n))_{closed}
     &\stackrel{\langle F_A\rangle}{\leftarrow}&
     inv(\mathfrak{g})
     &&&
     curvature
  }
  \,.
$$

The $\infty$-Chern-Weil homomorphism is at this level of local data the operation that takes the $\mathfrak{g}$-connection to a $b^k \mathbb{R}$-connection by forming the [[pasting]] composite of these two diagrams

$$
  \array{
     C^\infty(U)\otimes \Omega^\bullet(\Delta^n)
     &\stackrel{A_{vert}}{\leftarrow}&
     CE(\mathfrak{g})
     &\stackrel{\mu}{\leftarrow}&
     CE(b^k \mathbb{R})
     & : \mu(A_{vert})
     &&&
     characteristic\;class
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
     &\stackrel{A}{\leftarrow}&
     W(\mathfrak{g})
     &\stackrel{cs_\mu}{\leftarrow}&
     W(b^k \mathbb{R})
     &
     : cs_\mu(A)
     &&&
     Chern-Simons\;form
     \\
     \uparrow && \uparrow && \uparrow
     \\
     (\Omega^\bullet(U)\otimes C^\infty(\Delta^n))_{closed}
     &\stackrel{\langle F_A\rangle}{\leftarrow}&
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle_\mu}{\leftarrow}&
     inv(b^k \mathbb{R})
     &
     : \langle F_A\rangle_\mu
     &&&
     curvature\;characteristic\;form
  }
  \,.
$$


## References

The [[universal principal ∞-bundle|universal principal 2-bundle]] $\mathbf{E}G$ and its [[groupal model for universal principal ∞-bundles|groupal model]] $INN(G)$ is discussed in detail in

* [[David Roberts]], [[Urs Schreiber]], _The inner automorphism 3-group of a strict 2-group_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#RobertsSchreiber">web</a>).
{#RobertsSchreiber}

For more see [[principal 2-bundle]].

The ide of describing connections on principal 1- and 2-bundles in terms of parallel transport 1- and 2-functors appears in

* [[John Baez]], U. S. _Higher gauge theory_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#BaezSchreiber">web</a>)
{#BaezSchreiber}

A detailed account of the description of ordnary bundles with connection in the style that prepares the ground for our developments here is in 

* U. S., [[Konrad Waldorf]], _Parallal transport and functors_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SWI">web</a>)

A detailed account of the description of (abelian and nonabelian) [[gerbe]]s/[[bundle gerbe]]s/[[principal 2-bundle]]s in the style that we shall generalize to an $(\infty,1)$-topos theoretical context here is in

* U. S., [[Konrad Waldorf]]

  1. _Smooth functors versus differential forms_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">web</a>)

  1. _Connections on nonabelian gerbes and their holonomy_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">web</a>)
{#SW}

The description of there refined Chern-Weil homomorphisms in terms of Cech-Deligne cohomology was discussed in

* [[Jean-Luc Brylinski]], Dennis MacLaughlin, _Cech cocycles for characteristic classes_ , Communications in Mathematical Phiysics, Volume 178, Number 1 (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#CechCocyclesForCharClasses">web</a>)
{#BrylinskiMacLaughlin}

The Yoga of $\infty$-Lie algebra valued connections and the $\infty$-Chern-Weil homomorphism in local data is from 

* SSS, 

  1. _$L_\infty$-algebra connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)

  1. _Twisted differential string- and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">web</a>)
{#SSSI}

For more see [[schreiber:∞-Lie algebroid valued differential forms]].

For further references see 

* [[schreiber:differential cohomology in an (∞,1)-topos -- references]].

[[!redirects ∞-Chern-Weil theory -- preparatory concepts]]

[[!redirects ∞-Chern-Weil-theory introduction]]
[[!redirects ∞-Chern-Weil theory introduction]]