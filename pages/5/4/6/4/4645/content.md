

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Ordinary [[Chern-Weil theory]] studies [[connection on a bundle|connections]] on $G$-[[principal bundle]]s over a [[Lie group]] $G$. In the context of the [[cohesive (∞,1)-topos]] [[Smooth∞Grpd]] of [[∞-Lie groupoid]]s these generalize to [[connection on an ∞-bundle|∞-connections]] on [[principal ∞-bundle]]s over [[∞-Lie group]]s $G$. Accordingly **[[∞-Chern-Weil theory]]** deals with these higher connections and their relation to [[ordinary differential cohomology]].

Here we describe some introdutcory basics of the general theory in concrete terms.

See <a href="http://ncatlab.org/nlab/show/infinity-Chern-Weil+theory#Motivation">∞-Chern-Weil theory -- motivation</a> for some motivation.


Two simplifying special cases of general $\infty$-Chern-Weil theory are obtained by

1. restricting attention to _low categorical degree_ , 

   studying [[principal bundle|principal 1-bundle]]s, [[principal 2-bundle]]s and maybe 3-bundles; in terms of [[groupoid]]s, [[2-groupoid]]s and maybe [[3-groupoid]]s;

1. restricting attention to _infinitesimal aspects_ 

   studying not [[∞-Lie groupoid]]s but just their [[∞-Lie algebroid]]s. In terms of this it is easy to raise categorical degree to $n = \infty$, but this misses various global [[cohomology|cohomological]] effects (very similar to how [[rational homotopy theory]] describes just non-torsion phenomena of genuine [[homotopy theory]]).

These are the special cases that this introduction concentrates on.

We start by describing 

* [Smooth principal n-bundles](#PrincipalNBundles)

for low $n$ in detail, connecting them to standard theory, but presenting everything in such as way as to allow straightforward generalization to the full discussion of [[principal ∞-bundle]]s.

Then in the same spirit we discuss

* [Connections on principal n-bundles](#LowDimension)

for low $n$ in a fashion that connects to the ordinary notion of [[parallel transport]] and points the way to the fully-fledged formulation in terms of the [[schreiber:path ∞-groupoid]] functor.

This leads to differential-form expressions that we shall then finally reformulate in terms of 

* [L-∞ algebra valued connections](#LieConnections).

We end by indicating how under [[Lie integration]] this lifts to the full [[∞-Chern-Weil theory]].


## Principal $n$-bundles in low dimension {#PrincipalNBundles}

We assume here that the reader has a working knowledge of [[groupoid]]s and at least a rough idea of [[2-groupoid]]s. We first use these notions to motivate some constructions, before discussing the
formalization of [[∞-groupoid]] in terms of [[Kan complexes]].


### Ordinary smooth principal bundles {#PrincipalBundles}

Let $G$ be a [[Lie group]] and $X$ a [[smooth manifold]] (all our smooth manifolds are assumed to be finite dimensional and [[paracompact space|paracompact]]). 

We give a discussion of smooth $G$-[[principal bundle]]s on $X$ in a manner that paves the way to a straightforward generalization to a description of [[principal ∞-bundle]]s.

From the group $G$ we canonically obtain a [[groupoid]] that we write $\mathbf{B}G$ and call the [[delooping]] groupoid of $G$. Formally this groupoid is

$$
  \mathbf{B}G = (G \stackrel{\to}{\to} *)
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
      \bullet &&\stackrel{g_2 \cdot g_1 }{\to}&& \bullet
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

Now consider yet another Lie groupoid canonically associated with $G$: we shall write $\mathbf{E}G$ for the groupoid whose formal description is

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
        & {}^{\mathllap{g_2 g_1^{-1}}}\nearrow &=& \searrow^{\mathrlap{g_3 g_2^{-1}}}
        \\
        g_1 &&\stackrel{ g_3 g_1^{-1}}{\to}&& g_3
     }
  \right\}
  \,,
$$

This again inherits an evident smooth structure from the smooth structure of $G$ and hence becomes a Lie groupoid.

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
          (x,i,g_1) &&\stackrel{}{\to}&& (x,j,g_2 = g_{i j}(x) g_1 )
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
  P = \left( \coprod_{i} U_i \times G \right)/{\sim}
  \,,
$$

where the [[equivalence relation]] is precisely that exhibited by the morphisms in $\tilde P$. This is the traditional way to construct a $G$-[[principal bundle]] from cocycle functions $\{g_{i j}\}$. We may think of $\tilde P$ as _being_ $P$. It is a particular _representative_ of $P$ in the $(\infty,1)$-topos of Lie groupoids.

While it is easy to see in components that the $P$ obtained this way does indeed have a principal $G$-[[action]] on it, for later generalizations it is crucial that we can also recover this in a general abstract way. For notice that there is a canonical [[action]]

$$
  (\mathbf{E}G) \times G \to \mathbf{E}G
$$
given by the action of $G$ on the space of objects, which are themselves identified with $G$.

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

The morphism $\tilde P \times G \to \tilde P$ exhibits the principal $G$-[[action]] of $G$ on $\tilde P$.


In summary we find

+-- {: .num_prop}
###### Observation

For $\{U_i \to X\}$ a [[good open cover]], there is an [[equivalence of categories]]

$$
  SmoothFunc(C(\{U_i\}), \mathbf{B}G)
  \simeq
  G Bund(X)
$$

between the [[functor category]] of smooth functors and smooth natural transformations, and the groupoid of smooth $G$-[[principal bundle]]s on $X$. 

=--

It is no coincidence that this statement looks akin to the maybe more familiar statement which says that _equivalence classes_ of $G$-principal bundles are classified by [[homotopy]]-classes of morphisms of [[topological space]]s 

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

### Cech cocycles {#Cech2Cocycles}

The discussion above of $G$-principal bundles was all based on the [[Lie groupoid]]s $\mathbf{B}G$ and $\mathbf{E}G$ that are canonically induced by a [[Lie group]] $G$. We now discuss the case where $G$ is generalized to a [[Lie 2-group]]. The above discussion will go through essentially verbatim, only that we pick up [[2-morphism]]s everywhere. This is the first step towards higher Chern-Weil theory. The resulting generalization of the notion of principal bundle is that of [[principal 2-bundle]]. For historical reasons these are known in the literature often as [[gerbe]]s or as [[bundle gerbe]]s. 

Write $U(1) = \mathbb{R}/\mathbb{Z}$ for the [[circle group]]. We have already seen above the groupoid $\mathbf{B}U(1)$ obtained from this. But since $U(1)$ is an [[abelian group]] this groupoid has the special property that it still has itself the structure of an [[group object]]. This makes it what is called a [[2-group]]. Accordingly, we may form its [[delooping]] once more to arrive at a [[Lie 2-groupoid]] $\mathbf{B}^2 U(1)$.

Its cartoon picture is

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

What we see here are the first stages of the full [[Cech nerve]] of the cover. Eventually we will be looking at this object in its entirety, since for all degrees this is always a _good_ replacement of the manifold $X$, as long as $\{U_i \to X\}$ is a [[good open cover]].

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
  \,.
$$

On [[3-morphism]]s it gives a constraint on these functions, since there are only identity 3-morphisms in $\mathbf{B}^2 U(1)$:

$$
  \begin{aligned}
  \left(
  \array{
    (x,j) &&\stackrel{}{\to}&& (x,k)
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
    &{}^{}\nearrow&\Downarrow^{g_{i k l}(x)}& 
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

In order to find the circle [[principal 2-bundle]] classified by such a cocycle by a pullback operation as before, we need to construct the 2-functor 
$\mathbf{E} \mathbf{B} U(1) \to \mathbf{B}^2 U(1)$ that exhibits the [[universal principal ∞-bundle|universal principal 2-bundle]] over $U(1)$.
The right choice for $\mathbf{E B} U(1)$ -- which we justify systematically in a moment -- is 
indicated by

$$
  \mathbf{E B}U(1) := 
  \left\{
    \array{
      && {*}
      \\
      & {}^{\mathllap{c_1}}\nearrow &\Downarrow^{g}& \searrow^{\mathrlap{c_2}}
      \\
      * &&\underset{c_3 = g c_2 c_1}{\to}&&
    }
  \right\}
$$
for $c_1, c_2, c_3, g \in U(1)$, where all possible composition operations are given by forming the
product of these labels in $U(1)$. The projection $\mathbf{E B}U(1) \to \mathbf{B}^2 U(1)$ is
the obvious one that simply forgets the labels $c_i$ of the 1-morphisms and just remembers the labels 
$g$ of the 2-morphisms.


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

Unwinding what this means, we see that  $\tilde P$ is the 2-groupoid whose objects are that of $C(U)$, whose morphisms are finite sequences of morphisms in $C(U)$, each equipped with a label $c \in U(1)$, and whose 2-morphisms are generated from those that look like

$$
  \array{
    && (x,j)
    \\
    & {}^{\mathllap{c_1}}\nearrow &\Downarrow^{g_{i j k}(x)}& \searrow^{\mathrlap{c_2}}
    \\
    (x,i) &&\stackrel{c_3}{\to}&& (x,k)
  }
$$

subject to the condition that

$$
  c_1 \cdot c_2 = c_3 \cdot g_{i j k}(x)
$$

in $U(1)$. As before for principal 1-bundles $P$, where we saw that the analogous pullback 1-groupoid $\tilde P$ was equivalent to the 0-groupoid $P$, here we see that this 2-groupoid is equivalent to the 1-groupoid 

$$
  P = 
  \left(
    C(U)_1 \times U(1) \stackrel{\to}{\to}
    C(U)
  \right)
$$ 

with composition law

$$
  ((x,i) \stackrel{c_1}{\to} (x,j) \stackrel{c_2}{\to} (x,k))
  =
  ((x,i) \stackrel{(c_1 \cdot c_2 \cdot g_{i j k }(x))}{\to}
  (x,k))
  \,.
$$

This is a [[groupoid cohomology|groupoid central extension]]

$$
  \mathbf{B}U(1) \to P \to C(U) \simeq X
  \,.
$$

Centrally extended groupoids of this kind are known in the literature as [[bundle gerbe]]s (over the [[surjective submersion]] $Y = U \to X$ ). They may be thought of as given by a [[line bundle]] 

$$
  \array{
     L
     \\
     \downarrow
     \\
     (C(U)_1 = U \times_X U) &\stackrel{\to}{\to}& (C(U)_0 = U)
     \\
     && \downarrow
     \\
     && X
  }
$$

over the space $C(U)_1$ of [[morphism]]s, and a line bundle morphism

$$

  \mu_g : \pi_1^* L \otimes \pi_2^* L \to \pi_1^* L
$$

that satisfies an evident [[associativity]] law, equivalent to the cocycle codition on $g$.

So we see that bundle gerbes are presentations of Lie groupoids that are total spaces of $\mathbf{B}U(1)$-[[principal 2-bundle]]s.

This is clearly the beginning of a pattern. Next we can form one more [[delooping]] and produce the Lie 3-groupoid $\mathbf{B}^3 U(1)$. A cocycle $C(U) \to \mathbf{B}^3 U(1)$ classifies a _circle 3-bundle_ . The total space object $\tilde P$ in the pullback

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




### String 2-bundles and nonabelian bundle gerbes

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


### A model for principal $\infty$-bundles {#ModelForPrincipalInfinityBundle}

We have seen [above](#PrincipalBundles) that the theory of ordinary smooth [[principal bundle]]s is naturally situated within the context of [[Lie groupoid]]s, and [then](#Cech2Cocycles) that the theory of smooth [[principal 2-bundle]]s is naturally situated within the theory of [[Lie 2-groupoid]]s. This is clearly the beginning of a pattern in [[higher category theory]] where in the next step we see smooth [[3-groupoid]]s and so on. Finally the general theory of [[principal ∞-bundle]]s deals with smooth [[∞-groupoid]]s. 

A comprehensive discussion of such [[∞-Lie groupoids]] is given there. In this introduction here we will just briefly describe the main _tool_ for _modelling_ these and describe principal $\infty$-bundles in this model. See also [[models for ∞-stack (∞,1)-toposes]].

We first look at bare [[∞-groupoids]] and then discuss how to equip these with smooth structure.

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

* functions $([n] \hookrightarrow [n+1]) \mapsto (K_{n+1} \to K_n)$
  that send $n+1$-morphisms to their boundary $n$-morphisms;

* functions $([n+1] \to [n]) \mapsto (K_{n} \to K_{n+1})$
  that send $n$-morphisms to [[identity]] $(n+1)$-morphisms
  on them.

The fact that $K$ is supposed to be a [[functor]] enforces that these assignments of sets and functions satisfy conditions that make consistent our interpretation of them as sets of $k$-morphisms and source and target maps between these. 
These are called the [[simplicial identities]].

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

and for $(f,g) : \Lambda^1[2] \to K$ an image of this situation in $K$, hence a pair $x_0 \stackrel{f}{\to} x_1 \stackrel{g}{\to} x_2$ of two _composable_ 1-morphisms in $K$, we want to demand that there exists a third 1-morphisms in $K$ that may be thought of as the [[composition]] $x_0 \stackrel{h}{\to} x_2$ of $f$ and $g$. But since we are working in [[higher category theory]] with the [[principle of equivalence]], we want to identify this composite only up to a [[2-morphism]] equivalence

$$
    \array{
       && x_1
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

A simplicial set where for all such $(f,g)$ a corresponding such $h$ exists may be thought of as a collection of higher morphisms that is equipped with a notion of composition of adjacent 1-morphisms. 

For the purpose of describing [[groupoid]]al composition, we now want that this composition operation has all [[inverse]]s. For that purpose, notice that for 

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

two such 1-morphisms in $K$, then if $g$ had an inverse $g^{-1}$ we could use the above composition operation to compose that with $h$ and thereby find a morphism $f$ connecting the sources of $h$ and $g$. This being the case is evidently equivalent to the existence of diagrams of morphisms of simplicial sets of the form

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

Demanding that all such diagrams exist is therefore demanding that we have on 1-morphisms a composition operation with inverses in $K$. 

In order for this to qualify as an $\infty$-groupoid, this composition operation needs to satisfy an [[associativity law]] up to [[coherent]] [[2-morphism]]s, which means that we can find the relevant [[tetrahedra]]s in $K$. These in turn need to be connected by _pentagonators_ and ever so on.  It is a nontrivial but true and powerful fact, that all these [[coherence]] conditions are captured by generalizing the above conditions to all dimensions in the evident way:

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

The basic example is the [[nerve]] $N(C) \in sSet$ of an ordinary [[groupoid]] $C$, which is the [[simplicial set]] with $N(C)_k$ being the set of sequences of $k$ composable morphisms in $C$. The nerve operation is a [[full and faithful functor]]  from 1-groupoids into Kan complexes and hence may be thought of as embedding 1-groupoids in the context of general [[∞-groupoid]]s.

But we need a bit more than just bare [[∞-groupoid]]s. In generalization to [[Lie groupoid]]s, we need [[∞-Lie groupoid]]s. A useful way to encode that an $\infty$-groupoid has extra structure modeled on geometric test objects that themselves form a category $C$ is to remember the rule which for each test space $U$ in $C$ produces the $\infty$-groupoid of $U$-parameterized families of $k$-morphisms in $K$.  For instance for an [[∞-Lie groupoid]] we could test with each [[Cartesian space]] $U = \mathbb{R}^n$ and find the $\infty$-groupoids $K(U)$ of smooth $n$-parameter families of $k$-morphisms in $K$.

This data of $U$-families arranges itself into a [[presheaf]] with values in Kan complexes

$$
  K : C^{op} \to KanCplx \hookrightarrow sSet
$$

hence with values in simplicial sets. This is equivalently a [[simplicial presheaf]] of sets. The [[functor category]] $[C^{op}, sSet]$ on the [[opposite category]] of the category of test objects $C$ serves as a model for the [[(∞,1)-category]] of $\infty$-groupoids with $C$-structure.

While there are no [[higher morphism]]s in this functor 1-category that could for instance witness that two $\infty$-groupoids are not [[isomorphic]], but still [[equivalence of categories|equivalent]], it turns out that all one needs in order to reconstruct _all_ these higher morphisms (up to equivalence!) is just the information of which morphisms of simplicial presheaves would become invertible if we were keeping track of higher morphism. These would-be invertible morphisms are called _weak equivalences_ and denoted $K_1 \stackrel{\simeq}{\to} K_2$. 

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
 
1. **[[homotopy pullback]]** -- For $A \to B \stackrel{p}{\leftarrow} C$ a [[diagram]], the [[(∞,1)-pullback]] of it is the ordinary [[pullback]] in $[C^{op}, sSet]$ of a replacement diagram $A \to B \stackrel{\hat p}{\leftarrow} \hat C$, where $\hat p$ is a _good replacement_  of $p$ in the sense of the following factorization lemma.

1. **[[factorization lemma]]** -- For $p : C \to B$ a morphism in $[C^{op}, sSet]$, a _good replacement_ $\hat p : \hat C \to B$ is given by the composite vertical morphism in the ordinary [[pullback]] diagram

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
     \,,
   $$

  where $B^{\Delta[1]}$ is the [[path object]] of $B$: 
  the simplicial presheaf that is over each $U \in C$ the
  simplicial path space $B(U)^{\Delta[1]}$.
  
The [[principal ∞-bundle]]s that we wish to model are already the main and simplest example of the application of these three items: 

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



## Parallel transport in low dimensions {#LowDimension}

With a decent handle on principal $\infty$-bundles as described [above](#ModelForPrincipalInfinityBundle) we now turn to the description of [[connection on an ∞-bundle|connections on ∞-bundles]]. It will turn out that the above [[cocycle]]-description of $G$-principal $\infty$-bundles in terms of  [[∞-anafunctor]]s $X \stackrel{\simeq}{\leftarrow} \hat X \stackrel{g}{\to} \mathbf{B}G$ has, under mild conditions, a natural generalization where $\mathbf{B}G$ is replaced by a [[concrete sheaf|non-concrete]] simplicial presheaf $\mathbf{B}G_{conn}$ which we may think of as the [[∞-groupoid of ∞-Lie algebra valued forms]]. This comes with a canonical map $\mathbf{B}G_{conn} \to \mathbf{B}G$ and an $\infty$-connection $\nabla$ on the $\infty$-bundle classified by $g$ is a lift $\nabla$ of $g$
in the disgram

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

In the language of [[∞-stack]]s we may think of $\mathbf{B}G$ as the $\infty$-stack (on [[CartSp]]) or $\infty$-prestack (on [[Diff]]) $G TrivBund(-)$ of _trivial_ $G$-principal bundles, and of $\mathbf{B}G_{conn}$ correspondingly as the object $G TrivBund_{\nabla}(- )$ of  trivial $G$-principal bundles with (non-trivial) connection. In this sense the statement that $\infty$-connections are cocycles with coefficients in some $\mathbf{B}G_{conn}$ is a tautology. The real questions are:

1. What is $\mathbf{B}G_{conn}$ in concrete formulas?

1. Why are these formulas what they are? What is the general abstract concept of an $\infty$-connection? What are its defining abstract properties?

A comprehensive answer to the second question is provided by the general abstract concept of [[schreiber:differential cohomology in a cohesive topos]]. Here in this introduction we will not go into the full abstract theory, but using classical tools we get pretty close. What we describe is a generalization of the concept of [[parallel transport]] to [[higher parallel transport]]. As we shall see, this is naturally expressed in terms of [[∞-anafunctor]]s out of [[path n-groupoid]]s. This reflects how the full abstract theory arises in the context of an [[∞-connected (∞,1)-topos]] that comes canonically with a notion of [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]].

Below we begin the discussion of $\infty$-connections by reviewing the classical theory of [[connection on a bundle]] in a way that will make its generalization to higher connections relatively straightforward:

* [Connections on principal bundles](#ConnectionOnPrincipalBundle).

In an analogous way we can then describe certain classes of [[connections on a 2-bundle]] -- subsuming the notion of [[connection on a bundle gerbe]] -- in

* [Connections on 2-bundles](#ConnectionOn2Bundle).

With that in hand we then revisit the discussion of connections on ordinary bundles. By associating to each bundle with connection its corresponding _curvature 2-bundle with connection_ we obtain a more refined description of connections on bundles, one that is naturally adapted to the construction of [[curvature characteristic form]]s in the [[Chern-Weil homomorphism]]:

* [Curvature characteristics of 1-bundles](#CurvatureCharacteristicsI).

This turns out to be the kind of formulation of [[connections on an ∞-bundle]] that drops out of the general abstract theory described at [[∞-Chern-Weil homomorphism]]. In classical terms, its full formulation involves the description of [[circle n-bundles with connection]] in terms of [[Deligne cohomology]] and the description of the [[∞-groupoid of ∞-Lie algebra valued forms]] in terms of [[dg-algebra]] homomorphisms. The first aspect we discuss in 

* [Circle n-bundles with connection](#CirclenBundles)

the second in

* [L-∞ algebra valued connections](#LieConnections).

The combination of these two aspects yields naturally an explicit model for the [[Chern-Weil homomorphism]] and its generalization to higher bundles:

* [The ∞-Chern-Weil homomorphism](#ChernWeilHomomorphism)

Taken together, these constructions allow us to express a good deal of the general $\infty$-Chern-Weil theory with classical tools. As an example, we describe how the classical Cech-Deligne cocycle construction of the refined [[Chern-Weil homomorphism]] (by (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#CechCocyclesForCharClasses">BrylinskiMacLaughlin</a>)) drops out from these constructions:

* [Example: The Chern-Simons circle 3-bundle](#ChernSimons3Bund).



### Connections on a principal bundle {#ConnectionOnPrincipalBundle}

There are different equivalent definitions of the classical notion of a connection. One that is useful for our purposes is that a connection $\nabla$ on a $G$-principal bundle $P \to X$ is a rule $tra_\nabla$ for [[parallel transport]] along paths: a rule that assigns to each path $\gamma : [0,1] \to X$ a morphism $tra_\nabla(\gamma) : P_x \to P_y$ between the fibers of the bundle above the endpoints of these paths, in a compatible way:


$$
  \array{
    P_x &\stackrel{tra_\nabla(\gamma)}{\to}& P_y
    &\stackrel{tra_\nabla(\gamma')}{\to}& P_z &&& P
    \\
    && && &&& \downarrow
    \\
    x &\stackrel{\gamma}{\to}& y &\stackrel{\gamma'}{\to}& z
    &&&
    X
  }    
  \,.
$$

In order to formalize this, we introduce a ([[diffeological space|diffeological]]) [[Lie groupoid]] to be called the [[path groupoid]] of $X$. (Constructions and results in this section are from (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SWI">[SWI]</a>).

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]] let $[I,X]$ be the set of [[smooth function]]s $I = [0,1] \to X$. For $U$ a [[Cartesian space]], we say that _a $U$-parameterized smooth family of points in $[I,X]$_ is a smooth map $U \times I \to X$. (This makes $[I,X]$ a [[diffeological space]]).

Say a path $\gamma \in [I,X]$ has _[[sitting instant]]s_ if it is constant in a neighbourhood of the boundary $\partial I$. Let $[I,P]_{si} \subset [I,P]$ be the subset of paths with sitting instants. 

Let $[I,X]_{si} \to [I,X]_{si}^{th}$ be the projection to the set of [[equivalence class]]es where two paths are regarded as equivalent if they are cobounded by a smooth [[thin homotopy]].

Say a $U$-parameterized smooth family of points in $[I,X]_{si}^{th}$ is one that comes from a $U$-family of representatives in $[I,X]_{si}$ under this projection. (This makes also $[I,X]_{si}^{th}$ a [[diffeological space]].)

=--


+-- {: .num_remark}
###### Remark

The passage to the subset and quotient $[I,X]_{si}^{th}$ of the set of all smooth paths in the above definition is essentially the minimal adjustment to enforce that the concatenation of smooth paths at their endpoints defines the composition operation in a groupoid.

=--


+-- {: .num_prop}
###### Definition

The **path groupoid** $\mathbf{P}_1(X)$ is the groupoid

$$
  \mathbf{P}_1(X) = ([I,X]_{si}^{th} \stackrel{\to}{\to} X)
$$

with source and target maps given by endpoint evaluation and composition given by concatenation of classes $[\gamma]$ of paths along any orientation preserving [[diffeomorphism]] $[0,1] \to [0,2] \simeq [0,1] \coprod_{1,0} [0,1]$ of any of their representatives

$$
  [\gamma_2] \circ [\gamma_1] : [0,1]
  \stackrel{\simeq}{\to} [0,1] \coprod_{1,0} [0,1]
  \stackrel{(\gamma_2 , \gamma_1)}{\to}
  X
  \,.
$$

This becomes an [[internal groupoid]] in [[diffeological spaces]] with the above $U$-families of smooth paths. We regard it as a [[groupoid-valued presheaf]], an object in $[CartSp^{op}, Grpd]$:

$$
  \mathbf{P}_1(X) : U \mapsto (Diff(U \times I, X)_{si}^{th} \stackrel{\to}{\to} Diff(U,X) )
  \,.
$$

=--

Observe now that for $G$ a [[Lie group]] and $\mathbf{B}G$ its [[delooping]] [[Lie groupoid]] discussed [above](#PrincipalBundles), a smooth functor $tra : \mathbf{P}_1(X) \to \mathbf{B}G$ sends each (thin-homotopy class of a) path to an element of the group $G$ 

$$
  tra : (x \stackrel{[\gamma]}{\to} y)
  \mapsto
  (
  \bullet
  \stackrel{tra(\gamma) \in G}{\to}
  \bullet
  )
$$

such that composite paths map to products of group elements 

$$
  tra : 
  \left(
    \array{
      && y
      \\
      & {}^{\mathllap{[\gamma]}}\nearrow &=& \searrow^{\mathrlap{[\gamma']}}
      \\
      x &&\stackrel{[\gamma']\circ [\gamma]}{\to}&& z
    }
  \right)
  \mapsto
  \left(
    \array{
      && \bullet
      \\
      & {}^{\mathllap{tra(\gamma)}}\nearrow 
      &=& 
      \searrow^{\mathrlap{tra(\gamma')}}
      \\
      \bullet &&\stackrel{tra(\gamma)tra(\gamma')}{\to}&& \bullet
    }
  \right)
$$

and such that $U$-families of smooth paths induce smooth maps $U \to G$ of elements. 

There is a classical construction that yields such an assignment: the [[parallel transport]] of a [[Lie-algebra valued 1-form]].

+-- {: .num_prop}
###### Definition

Suppose $A \in \Omega^1(X, \mathfrak{g})$ is a degree-1 [[differential form]] on $X$ with values in the [[Lie algebra]] $\mathfrak{g}$ of $G$. Then its parallel transport is the smooth functor

$$
   tra_A : \mathbf{P}_1(X) \to \mathbf{B}G
$$

given by

$$
  [\gamma] \mapsto P \exp(\int_{[0,1]} \gamma^* A) \; \in G
  \,,
$$

where the group element on the right is defined to be the value at 1 of the unique solution $f :  [0,1] \to G$ of the [[differential equation]]

$$
  d_{dR} f + \gamma^*A \wedge f = 0
$$

for the boundary condition $f(0) = e$.

=--

+-- {: .num_prop}
###### Theorem 

This construction $A \mapsto tra_A$ induces an [[equivalence of categories]]

$$
  [CartSp^{op},Grpd](\mathbf{P}_1(X), \mathbf{B}G)
  \simeq
  \mathbf{B}G_{conn}(X)
  \,,
$$

where on the left we have the [[hom-groupoid]] of [[groupoid-valued presheaves]] and  where on the right we have the [[groupoid of Lie-algebra valued 1-forms]] whose 

* objects are 1-forms $A \in \Omega^1(X,\mathfrak{g})$, 

* morphisms $g : A_1 \to A_2$ are labeled by [[smooth function]]s $g \in C^\infty(X,G)$ such that $A_2 = g^{-1} A g + g^{-1}d g$.

=--

This equivalence is [[natural transformation|natural]] in $X$, so that we obtain another smooth groupoid.

+-- {: .num_defn}
###### Definition

Define $\mathbf{B}G_{conn} : CartSp^{op} \to Grpd$ to be the (generalized) Lie groupoid

$$
  \mathbf{B}G_{conn} : U \mapsto [CartSp^{op}, Grpd](\mathbf{P}_1(-), \mathbf{B}G)
$$

whose $U$-parameterized smooth families of groupoids form the [[groupoid of Lie-algebra valued 1-forms]] on $U$.

=--

+-- {: .num_remark}
###### Remark

This equivalence in particular subsumes the classical facts that parallel transport $\gamma \mapsto P \exp(\int_{[0,1]} \gamma^* A)$ 

* is invariant under orientation preserving reparameterizations of paths;

* sends reversed paths to inverses of group elements.

=--

+-- {: .num_lemma}
###### Observation

There is an evident natural smooth functor $X \to \mathbf{P}_1(X)$ that includes points in $X$ as constant paths. This induces a natural morphism $\mathbf{B}G_{conn} \to \mathbf{B}G$ that forgets the 1-forms.

=--


+-- {: .num_defn}
###### Defintion

Let $P \to X$ be a $G$-[[principal bundle]] that corresponds to a cocycle $g : C(U) \to \mathbf{B}G$ under the construction discussed [above](#PrincipalBundles).  Then a **[[connection on a bundle|connection]]** $\nabla$ on $P$ is  a lift $\nabla$ of the cocycle through $\mathbf{B}G_{conn} \to \mathbf{B}G$.

$$
  \array{
     && \mathbf{B}G_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_lemma}
###### Observation

This is equivalent to the [[connection on a bundle|traditional definitions]].

=--

A morphism $\nabla : C(U) \to \mathbf{B}G_{conn}$ is

* on each $U_i$ a 1-form $A_i \in \Omega^1(U_i, \mathfrak{g})$;

* on each $U_i \cap U_j$ a function $g_{i j} \in C^\infty(U_i \cap U_j , G)$;

such that

* on each $U_i \cap U_j$ we have $A_j = g_{i j}^{-1}( A + d_{dR} )g_{i j}$;

* on each $U_i \cap U_j \cap U_k$ we have $g_{i j} \cdot g_{j k} = g_{i k}$.


+-- {: .num_prop}
###### Definition

Let $[I,X]_{si}^{th} \to [I,X]^h$ the projection onto the full quotient by smooth [[homotopy]] classes of paths.

Write $\mathbf{\Pi}_1(X) = ([I,X]^h \stackrel{\to}{\to} X)$ for the smooth groupoid defined as $\mathbf{P}_1(X)$, but where instead of thin homotopies, all homotopies are divided out.

=--


+-- {: .num_prop}
###### Proposition

The above restricts to a natural equivalence

$$
  [CartSp^{op}, Grpd](\mathbf{\Pi}_1(X), \mathbf{B}G)
  \simeq
  \mathbf{\flat}\mathbf{B}G
  \,,
$$

where on the left we have the [[hom-groupoid]] of groupoid-valued presheaves, and on the right we have the [[full subcategory|full sub-groupoid]] $\mathbf{\flat}\mathbf{B}G \subset \mathbf{B}G_{conn}$ on those $\mathfrak{g}$-valued differential forms whose [[curvature]] 2-form $F_A = d_{dR} A + [A \wedge A]$ vanishes.

A connection $\nabla$ is _flat_ precisely if it factors through the inclusion $\flat \mathbf{B}G \to \mathbf{B}G_{conn}$.

=--

For the purposes of [[Chern-Weil theory]] we want a good way to extract the [[curvature]] 2-form in a general abstract way from a cocycle $\nabla : X \stackrel{\simeq}{\leftarrow }C(U) \to \mathbf{B}G_{conn}$. In order to do that, we first need to discuss [[connections on 2-bundles]].


### Connections on principal 2-bundles {#ConnectionOn2Bundle}

There is an evident higher dimensional generalization of the definition of connections on 1-bundles in terms of functors out of the [[path groupoid]] discussed [above](#ConnectionOnPrincipalBundle). This we discuss now. We will see that, however, the obvious generalization captures not quite all 2-connections. But we will also see a way to recode 1-connections in terms of flat 2-connections. And that recoding then is the right general abstract perspective on connections, which generalizes to [[principal ∞-bundles]] and in fact which in the [[schreiber:differential cohomology in an (∞,1)-topos|full theory]] follows from first principles.

(Constructions and results in this section are from <a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">SWII, SWIII</a>)

+-- {: .num_defn}
###### Definition

The [[path n-groupoid|path 2-groupoid]] $\mathbf{P}_2(X)$ is the smooth [[strict 2-groupoid]] analogous to $\mathbf{P}_1(X)$, but with nontrivial [[2-morphism]]s given by [[thin homotopy]]-classes of disks $\Delta^2_{Diff} \to X$ with [[sitting instant]]s.

In analogy to the projection $\mathbf{P}_1(X) \to \mathbf{\Pi}_1(X)$ there is a projection to $\mathbf{P}_2(X) \to \mathbf{\Pi}_2(X)$ to the 2-groupoid obtained by dividing out full homotopy of disks, relative boundary.

=--

+-- {: .num_lemma}
###### Observation

Let $G$ be a strict [[Lie 2-group]] coming from a [[crossed module]] $([G_2 \stackrel{\delta}{\to} G_1], \alpha : G_1 \to Aut(G_2))$.Its [[delooping]]  $\mathbf{B}G$ is the strict [[Lie 2-groupoid]] coming from the [[crossed complex]] $[G_2 \stackrel{\delta}{\to} G_1 \stackrel{\to}{\to} *]$.

$$
  \mathbf{B}G
  = 
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_1}}\nearrow 
       & \Downarrow^{\mathrlap{k}}& 
       \searrow^{\mathrlap{g_2}}
       \\
       \bullet &&\underset{\delta(k) g_1 g_2 }{\to}&&
       \bullet
    }
    \;\;
    |
    \;\;
    g_1, g_2 \in G_1, k \in G_2 
  \right\}
  \,.
$$

This induces a [[differential crossed module]] $(\mathfrak{g}_2 \stackrel{\delta_*}{\to} \mathfrak{g}_1)$, the [[Lie 2-algebra]] of $G$.

=--

+-- {: .num_example}
###### Example

For $K$ an [[abelian group|abelian]] Lie group then $\mathbf{B}K$ is the [[delooping]] 2-group coming from the crossed module $[K \to 1]$ and $\mathbf{B}\mathbf{B}K$ is the 2-group coming from the complex $[K \to 1 \to 1]$.

=--

A smooth 2-functor  $\mathbf{\Pi}_2(X) \to \mathbf{B}G$ now assigns information also to surfaces

$$
  \left(
    \array{
      && y
      \\
      & {}^{\mathllap{\gamma_1}}\nearrow 
      &\Downarrow^{\mathrlap{\Sigma}}& 
      \searrow^{\mathrlap{\gamma_2}}
      \\
      x &&\underset{}{\to}&& z
    }
  \right)
  \mapsto
  \left(
    \array{
      && y
      \\
      & {}^{\mathllap{tra(\gamma_1)}}\nearrow 
      &\Downarrow^{\mathrlap{tra(\Sigma)}}& 
      \searrow^{\mathrlap{tra(\gamma_2)}}
      \\
      x &&\to&& z
    }
  \right)
$$

and thus encodes a [[higher parallel transport]].

+-- {: .num_prop}
###### Proposition

There is a natural equivalence of [[2-groupoid]]s

$$
  [CartSp^{op}, 2Grpd](\mathbf{\Pi}_2(X), \mathbf{B}G)
  \simeq
  \mathbf{\flat} \mathbf{B}G
$$

where on the right we have the [[2-groupoid of Lie 2-algebra valued forms|2-groupoid of Lie 2-algebra valued forms]] whose

* objects are pairs $A \in \Omega^1(X,\mathfrak{g}_1)$, 
  $B \in \Omega^2(X,\mathfrak{g}_2)$ such that
  the 2-form [[curvature]] 
 
  $$
    F_2(A,B) := d_{dR} A + [A \wedge A] + \delta_* B
  $$

  and the 3-form curvature

  $$
    F_3(A,B) := d_{dR} B + [A \wedge B] 
  $$

  vanish.

* morphisms $(\lambda,a) : (A,B) \to (A',B')$ 
  are pairs $a \in \Omega^1(X,\mathfrak{g}_2)$, 
  $\lambda \in C^\infty(X,G_1)$ such that
  $A' = \lambda A \lambda^{-1} + \lambda d \lambda^{-1} + \delta_* a$
  and $B' = \lambda(B) + d_{dR} a + [A\wedge a]$

* 2-morphisms are... (exercise).

=--

As before, this is natural in $X$, so that we that we get a presheaf of 2-groupoids
$$
  \mathbf{\flat}\mathbf{B}G : U \mapsto
  [CartSp^{op}, 2Grpd](\mathbf{\Pi}_2(U), \mathbf{B}G)
  \,.
$$

+-- {: .num_prop}
###### Proposition

If in the above definition we use $\mathbf{P}_2(X)$ instead of $\mathbf{\Pi}_2(X)$, we obtain the same 2-groupoid, except that the 3-form curvature $F_3(A,B)$ is not required to vanish.

=--

+-- {: .num_defn}
###### Definition

Let $P \to X$ be a $G$-[[principal 2-bundle]] classified by a cocycle $C(U) \to \mathbf{B}G$. Then a structure of a _flat_ **[[connection on a 2-bundle]]** $\nabla $ on it is a lift

$$
  \array{
    && \mathbf{\flat}\mathbf{B}G
    \\
    & {}^{\mathllap{\nabla_{flat}}}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

For $G = \mathbf{B}A$, a **[[connection on a 2-bundle]]** (not necessarily flat) is a lift

$$
  \array{
    && [\mathbf{P}_2(-),\mathbf{B}\mathbf{B}A]
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}\mathbf{B}A
  }
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

We do not state the last definition for general Lie 2-groups $G$. The reason is that for general $G$ 2-anafunctors out of $\mathbf{P}_2(X)$ do not produce the fully general notion of 2-connections that we are after,  but yield a special case in between flatness and non-flatness: the case where precisely the 2-form [[curvature]]-components vanish, while the 3-form curvature part is unrestricted. This case is important in itself and discussed in detail [below](#below). 

Only for $G$ of the form $\mathbf{B}A$ does the 2-form curvature necessarily vanish anyway, so that in this case the  definition by morphisms out of $\mathbf{P}_2(X)$ happens to already coincide with the proper general one. This serves in the following theorem as an illustration for the toolset that we are exposing, but for the purposes of introducing the full notion of $\infty$-Chern-Weil theory we will rather focus on flat 2-connections, and then show in [Curvature characteristics of 1-bundles](#CurvatureCharacteristicsI) how using these one does arrive at a functorial definition of 1-connections that does generalize to the fully general definition of $\infty$-connections.

=--

+-- {: .num_prop}
###### Theorem

Let $\{U_i \to X\}$ be a [[good open cover]], a cocycle $C(U) \to [\mathbf{P}_2(-), \mathbf{B}^2 A]$ is a cocycle in [[Cech cohomology]]-[[Deligne cohomology]] in degree 3. 

Moreover, we have a natural equivalence of [[bicategories]]

$$
  [CartSp^{op}, 2Grpd](C(U), [\mathbf{P}_2(-), \mathbf{B}^2 U(1)])
  \simeq
  U(1) Gerb_\nabla(X)
  \,,
$$

where on the right we have the bicategory of $U(1)$-[[bundle gerbe]]s with connection.

In particular the equivalence classes of cocycles form the degree-3 [[ordinary differential cohomology]] of $X$:

$$
  H^3_{diff}(X, \mathbb{Z}) \simeq \pi_0( [C(U), [\mathbf{P}_2(-), \mathbf{B}^2 U(1)]])
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

A cocycle as above naturally corresponds to a [[∞-anafunctor|2-anafunctor]]

$$
  \array{
    Q &\to& \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{P}_2(X)
  }
  \,.
$$

The value of this on 2-morphisms in $\mathbf{P}_2(X)$ is the [[higher parallel transport]] of the connection on the 2-bundle. 

This appears for instance in the [[action functional]] of the [[sigma model]] that describes strings charged under a [[Kalb-Ramond field]].

=--

The following example of a flat nonabelian 2-bundle is very degenerate as far as 2-bundles go, but does contain in it the seed of a full understanding of connections on 1-bundles.

+-- {: .num_defn}
###### Definition

For $G$ a [[Lie group]], its _[[inner automorphism 2-group]]_ $INN(G)$ is as a groupoid the [[universal principal infinity-bundle|universal G-bundle]] $\mathbf{E}G$, but regarded as a 2-group with the group structure coming from the crossed module $[G \stackrel{Id}{\to} G]$.

=--

The cartoon presentation of the delooping [[2-groupoid]] $\mathbf{B}INN(G)$ is

$$
  \mathbf{B}INN(G)
  =
  \left\{
    \array{
      && \bullet
      \\
      & {}^{\mathllap{g_1}}\nearrow 
      & \Downarrow^{\mathrlap{k}}
      & \searrow^{\mathrlap{g_2}}
      \\
      \bullet
      &&\underset{g_3 = g_1 g_2 k}{\to}&&
      \bullet
    }
    \;\;
    \,,
    \;\;
    g_1, g_2, k \in G
  \right\}
  \,.
$$

+-- {: .num_remark}
###### Remark


This is the Lie 2-group whose [[Lie 2-algebra]] $inn(\mathfrak{g})$ is the one whose [[Chevalley-Eilenberg algebra]] is the [[Weil algebra]] of $\mathfrak{g}$.

=--

+-- {: .num_example}
###### Example

By the above theorem we have that there is a bijection of sets

$$
  \{\mathbf{\Pi}_2(X) \to \mathbf{B} INN(G)\}
  \simeq
  \Omega^1(X, \mathfrak{g})
$$

of flat $INN(G)$-valued 2-connections and Lie-algebra valued 1-forms. Under the identifications of this theorem this identification works as follows:

* the 1-form component of the 2-connection is $A$;

* the vanishing of the 2-form component of the 2-curvature $F_2(A,B) = F_A + B$  identifies the 2-form component of the 2-connection with the [[curvature]] 2-form, $B = - F_A$;

* the vanishing of the 3-form component of the 2-curvature $F_3(A,B) = d B + [A \wedge B] = d_A + [A \wedge F_A]$ is the [[Bianchi identity]] satisfied by any curvature 2-form.

=--

This means that 2-connections with values in $INN(G)$ actually model 1-connections _and_ keep track of their curvatures. Using this we see in the next section a general abstract definition of connections on 1-bundles that naturally support the [[Chern-Weil homomorphism]].


### Curvature characteristics of 1-bundles {#CurvatureCharacteristicsI}

We now describe connections on 1-bundles in terms of their _flat curvature 2-bundles_ . This gives a general abstract notion of connections that generalizes to [[connections on ∞-bundles]] and that supports naturally the [[Chern-Weil homomorphism]]

Throughout this section $G$ is a [[Lie group]], $\mathbf{B}G$ its [[delooping]] 2-groupoid and $INN(G)$ its [[inner automorphism 2-group]] and $\mathbf{B}INN(G)$ the corresponding delooping [[Lie 2-groupoid]]. 


+-- {: .num_defn #BGdiff}
###### Definition

Define the smooth groupoid $\mathbf{B}G_{diff} \in [CartSp^{op}, Grpd]$ as the [[pullback]]

$$
  \mathbf{B}G_{diff} = \mathbf{B}G \times_{\mathbf{B}INN(G)} \mathbf{\flat} \mathbf{B}INN(G)
  \,.
$$

This is the [[groupoid-valued presheaf]] which assigns to $U \in CartSp$ the groupoid whose objects are [[commuting diagram]]s

$$
  \array{
    U &\to& \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(G)
  }
  \,,
$$

where the vertical morphisms are the canonical inclusions discussed above, and whose morphisms are compatible pairs of [[natural transformation]]s 

$$
  \array{
    U &{{\nearrow \searrow} \atop {\to}}& \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &{{\nearrow \searrow} \atop {\to}}& \mathbf{B} INN(G)
  }
$$


of the horizontal morphisms.

=--

+-- {: .num_remark}
###### Remark

By the above theorems, we have over any $U \in $ [[CartSp]] that

* an [[object]] in $\mathbf{B}G_{diff}(U)$ is a 1-form $A \in \Omega^1(U,\mathfrak{g})$;

* a [[morphism]] $A_1 \stackrel{(g,a)}{\to} A_2$ is labeled by a function $g \in C^\infty(U,G)$ and a 1-form $a \in \Omega^1(U,\mathfrak{g})$ such that

  $$
    A_2 = g^{-1}A_1 g + g^{-1}d g  + a
    \,.
  $$
  
  Notice that this can always be uniquely solved for $a$, so that the genuine information in this morphism is just the data given by $g$. 

* there are _no_ nontrivial [[2-morphism]]s, even though $\mathbf{B}INN(G)$ is a 2-groupoid: since $\mathbf{B}G$ is just a 1-groupoid this is enforced by the commutativity of the above diagram.

=--

From this it is clear that

+-- {: .num_prop}
###### Proposition

The projection $\mathbf{B}G_{diff} \stackrel{\simeq}{\to} \mathbf{B}G$ is a weak equivalence.

=--

So $\mathbf{B}G_{diff}$ is a [[resolution]] of $\mathbf{B}G$. We will see that it is the resoluton that supports [[∞-anafunctor|2-anafunctor]]s out of $\mathbf{B}G$ which represent [[curvature characteristic class]]es.


+-- {: .num_defn}
###### Definition

For $X \stackrel{\simeq}{\leftarrow}C(U) \to \mathbf{B}U(1)$ a cocycle for a $U(1)$-principal bundle $P \to X$, we call a lift $\nabla_{ps}$ in

$$
  \array{
    && \mathbf{B}G_{diff}
    \\
    & {}^{\mathllap{\nabla_{ps}}}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

a [[pseudo-connection]] on $P$.

=--


Pseudo-connections in themselves are not very interesting. But notice that every ordinary connection is in particular a pseudo-connection and we have an inclusion  morphism of smooth groupoids

$$
  \mathbf{B}G_{conn} \hookrightarrow \mathbf{B}G_{diff}
  \,.
$$

This inclusion plays a central role in the theory. The point is that while $\mathbf{B}G_{diff}$ is such a boring extenion of $\mathbf{B}G$ that it is actually equivalent to $\mathbf{B}G$, there is no inclusion of $\mathbf{B}G_{conn}$ into $\mathbf{B}G$, but there is into $\mathbf{B}G_{diff}$. This is the kind of situation that [[resolution]]s are needed for.


It is useful to look at some details for the case that $G$ is an [[abelian group]] such as the [[circle group]] $U(1)$.

In this abelian case the 2-groupoids $\mathbf{B}U(1)$, $\mathbf{B}^2 U(1)$, $\mathbf{B}INN(U(1))$, etc., that so far we noticed are given by [[crossed complex]]es are actually given by ordinary [[chain complex]]es: we write 

$$
  \Xi : Ch_\bullet^+ \to sAb \to KanCplx
$$

for the [[Dold-Kan correspondence]] map that identifies [[chain complex]]es with [[simplicial abelian group]] and then considers their underlying [[Kan complex]]es. Using this map we have the following identifications of our 2-groupoid valued presheaves with complexes of group-valued sheaves

$$
  \mathbf{B}U(1) = \Xi[C^\infty(-,U(1)) \to 0]
$$

$$
  \mathbf{B}^2 U(1) = \Xi[C^\infty(-,U(1))  \to 0 \to 0]
$$

$$
  \mathbf{B} INN U(1) = \Xi[C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-,U(1)) \to 0]
 \,.
$$

+-- {: .num_remark}
###### Observation

For $G = A$ an [[abelian group]], in particular the [[circle group]], there is a canonical morphism $\mathbf{B} INN(U(1)) \to \mathbf{B}\mathbf{B}U(1)$.

=--

On the level of chain complexes this is the evident chain map

$$
  \array{
    [C^\infty(-,U(1)) &\stackrel{Id}{\to}& C^\infty(-,U(1))
    &\to& 0]
    \\
    \downarrow && \downarrow && \downarrow
    \\
    [C^\infty(-,U(1)) &\to& 0 &\to& 0]    
  }
  \,.
$$

On the level of 2-groupoids this is the map that forgets the labels on the 1-morphisms

$$
  \left\{
    \array{
        && \bullet
       \\
       & {}^{\mathllap{g_1}}\nearrow 
          & \Downarrow^{\mathrlap{k}}& \searrow^{\mathrlap{g_2}}
       \\
      \bullet &&\stackrel{k g_2 g_1}{\to}&&
    }
  \right\}
  \;\;
  \mapsto
  \;\;
  \left\{
    \array{
        && \bullet
       \\
       & {}^{\mathllap{Id}}\nearrow 
          & \Downarrow^{\mathrlap{k}}& \searrow^{\mathrlap{Id}}
       \\
      \bullet &&\stackrel{Id}{\to}&& \bullet
    }
  \right\}
  \,.
$$

In terms of this map $INN(U(1))$ serves to interpolate between the single and the double delooping of $U(1)$. In fact the sequence of 2-functors

$$
  \mathbf{B}U(1) \to \mathbf{B}INN(U(1)) \to 
  \mathbf{B}^2 U(1)
$$

is a model for the $\mathbf{B}U(1)$-[[universal principal infinity-bundle|universal principal 2-bundle]]

$$
  \mathbf{B}U(1) \to  \mathbf{E} \mathbf{B}U(1)
  \to 
  \mathbf{B}^2 U(1)
  \,.
$$

This happens to be an [[exact sequence]] of [[2-groupoid]]s. Abstractly, what really matters is rather that it is a [[fiber sequence]], meaning that it is exact in the correct sense inside the [[(∞,1)-category]] [[Smooth∞Grpd]]. For our purposes it is however relevant that this particular model is also exact in the ordinary sense in that we have a commuting diagram

$$
  \array{
    \mathbf{B}U(1) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}INN(U(1)) &\to& \mathbf{B}^2 U(1)
  }
$$

which is a [[pullback]] diagram, exhibitng $\mathbf{B}U(1)$ as the [[kernel]] of $\mathbf{B}INN(U(1)) \to \mathbf{B}^2 U(1)$.

We shall be interested in the [[pasting]] composite of this diagram with the one defining $\mathbf{B}G_{diff}$ over a domain $U$:

$$
  \array{
    U &\to&
    \mathbf{B}U(1) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1)) &\to& \mathbf{B}^2 U(1)
  }
  \,,
$$

The total outer diagram appearing this way is a component of the following (generalized) Lie 2-groupoid.

+-- {: .num_defn}
###### Definition

Set

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2U(1)  := 
  * \times_{\mathbf{B}^2 U(1)} \mathbf{\flat} \mathbf{B}^2 U(1)
  \,.
$$


=--

Over any $U \in CartSp$ this is the 2-groupoid whose objects are sets of diagrams

$$
  \array{
    U &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1)
  }
  \,.
$$

This are equivalently just morphisms $\mathbf{\Pi}_2(U) \to \mathbf{B}^2 U(1)$, which by the above theorems we may identify with closed 2-forms $B \in \Omega^2_{cl}(U)$.

The morphisms $B_1 \to B_2$ in $\mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ over $U$ are compatible [[pseudonatural transformation]]s of the horizontal morphisms

$$
  \array{
    U &{{\nearrow \searrow} \atop {\to}}& {*}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &{{\nearrow \searrow} \atop {\to}}& 
    \mathbf{B} INN(G)
  }
  \,,
$$

which means that they are pseudonatural transformations of the bottom morphism whose components over the points of $U$ vanish. These identify with 1-forms $\lambda \in \Omega^1(U)$ such that  $B_2 = B_1 + d_{dR} \lambda$.

Finally the 2-morphisms would be [[modification]]s of these, but the commutativity of the above diagram constrains these to be trivial.


In summary this shows that

+-- {: .num_prop}
###### Proposition

Under the [[Dold-Kan correspondence]] $\mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ is the sheaf of truncated [[de Rham complex]]es

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  =
  \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-)]
  \,.
$$

=--

+-- {: .num_lemma}
###### Corollary

Equivalence classes of [[infinity-anafunctor|2-anafunctor]]s

$$
  X \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
$$

are canonically in bijection with the degree 2 [[de Rham cohomology]] of $X$.

=--

+-- {: .num_remark}
###### Remark


Notice that --  while every globally defined closed 2-form $B \in \Omega^2_{cl}(X)$ defines such a 2-anafunctor -- not every such 2-anafunctor comes from a globally defined closed 2-form. Some of them assign closed 2-forms $B_i$ to patches $U_1$, that differ by differentials $B_j - B_i = d_{dR} \lambda_{i j}$ of 1-forms $\lambda_{i j}$ on double overlaps, which themselves satisfy on triple intersections the cocycle condition $\lambda_{i j} + \lambda_{j k} = \lambda_{i k}$. But (using a [[partition of unity]], see there) these non-globally defined forms are always equivalent to globally defined ones.

This simple technical point turns out to play a crucial role in the abstract definition of [[connections on ∞-bundles]]: generally, for all $n \in \mathbb{N}$ the cocycles given by globally defined forms in $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ constitute [[curvature characteristic form]]s of _genuine_ connections. The non-globally defined forms _also_ constitute curvature invariants, but of [[pseudo-connection]]s. The way the abstract theory finds the genuine connections inside all pseudo-connections is by the fact that we may find for each cocycle in $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ an equivalent one that does comes from a globally defined form.
 
=--



+-- {: .num_lemma}
###### Observation

There is a canonical [[infinity-anafunctor|2-anafunctor]] 
$\hat {\mathbf{c}}_1^{dR} : \mathbf{B}U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)$

$$
  \array{
    \mathbf{B}U(1)_{diff} &\to& \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}U(1)
  }
  \,,
$$

where the top morphism is given by forming the [[pasting]]-composite with the $\mathbf{B} U(1)$-[[universal principal infinity-bundle|universal 2-bundle]], as described above.


=--

+-- {: .num_remark}
###### Remark


For emphasis, notice that this span is governed by a presheaf of diagrams that over $U \in CartSp$ is of the form

$$
  \array{
    U &\to& \mathbf{B}U(1) &&& transition\;function
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U) &&& connection
    \\
    \downarrow &&  \downarrow
    \\
    \mathbf{\Pi}(U) &\to& \mathbf{B}^2 U(1) &&& curvature
  }
  \,.
$$

The top morphisms are the components of the presheaf $\mathbf{B}U(1)$. The top squares are those of $\mathbf{B}U(1)_{diff}$. Forming the bottom square is forming the bottom morphism, which necessarily satifies the constraint that makes it a components of $\mathbf{\flat}\mathbf{B}^2 U(1)$. 

The interpretation of the stages is as indicated in the diagram:

1. the top morphism is the transition function of the underlying bundle;

1. the middle morphism is a choice of (pseudo-)connection on that bundle;

1. the bottom morphism picks up the curvature of this connection.

We will see that full $\infty$-Chern-Weil theory is governed by a slight refinement of presheaves of essentially this kind of diagram. We will also see that the three stage process here is really an incarnation of the computation of a [[connecting homomorphism]], reflecting the fact that behind the scenes the notion of _curvature_ is exhibited as the [[twisted cohomology|obstruction cocycle]] to lifts from bare bundles to flat bundles.

=--

+-- {: .num_remark}
###### Observation

For $X \stackrel{\simeq}{\leftarrow} C(U) \stackrel{g}{\to} \mathbf{B}U(1)$ the cocycle for a $U(1)$-principal bundle as described above, the composition of [[infinity-anafunctor|2-anafunctor]]s of $g$ with $\hat {\mathbf{c}}_1^{dR}$ yields a cocycle for a 2-form $\hat {\mathbf{c}}_1^{dR}(g)$

$$
  \array{
    && \mathbf{B}U(1)_{conn}
    \\
    & {}^{\mathrlap{\nabla}}\nearrow & \downarrow
    \\
    C(V) &\stackrel{}{\to}& \mathbf{B} U(1)_{diff} &\to& \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}U(1)
    \\
    \downarrow^{\mathrlap{\simeq}} 
    \\
    X 
  }
  \,.
$$

If we take $\{U_i \to X\}$ to be a [[good open cover]], then we may assume $V = U$. We know we can always find a [[pseudo-connection]] $C(V) \to \mathbf{B}U(1)_{diff}$ that is actually a genuine [[connection on a bundle]] in that it factors through the inclusion $\mathbf{B}U(1)_{conn} \to \mathbf{B}U(1)_{diff}$ as indicated.

The corresponding total map $c_1^{dR}(g)$ represented by $c_1^{dR}(\nabla)$ is the cocycle for the [[curvature]] 2-form of this connection. This represents the first [[Chern class]] of the bundle in de Rham cohomology.

=--


For $X,A$ smooth 2-groupoids, write $\mathbf{H}(X,A)$ for the 2-groupoid of 2-anafunctors between them. 


+-- {: .num_remark}
###### Corollary

Let $H_{dR}^2(X) \to \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^2 U(1))$ be a choice of one closed 2-form representative for each degree-2 [[de Rham cohomology]]-class of $X$. Then the [[pullback]] groupoid $\mathbf{H}_{conn}(X,\mathbf{B}U(1))$ in 

$$
  \array{
    \mathbf{H}_{conn}(X,\mathbf{B}U(1)) &\to& H_{dR}^2(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}U(1)_{diff}) &\to&
    \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^2 U(1))
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{H}(X,\mathbf{B}U(1)) \simeq U(1) Bund(X)
  }
$$

is equivalent to disjoint union of groupoids of $U(1)$-bundles with connection whose curvatures are the chosen 2-form representatives.

=--



### Circle $n$-bundles with connection and Deligne cohomology
 {#CirclenBundles}


For $A$ an [[abelian group]] there is a straightforward generalization of the above constructions to $(G = \mathbf{B}^{n-1}A)$-[[principal ∞-bundle|principal n-bundle]]s [[connection on an ∞-bundle|with connection]] for all $n \in \mathbb{N}$. We spell out the ingredients of the construction in a way analogous to the above discussion. A first-principles derivation of the objects we consider here is at [[circle n-bundle with connection]].
This is  content that appeared partly in (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>, <a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#FSSIII">FSS</a>).
We restrict attention to the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle n-group</a> $G = \mathbf{B}^{n-1}U(1)$. 

There is a familiar traditional presentation for [[ordinary differential cohomology]] in terms of [[Cech cohomology|Cech]]-[[Deligne cohomology]]. We briefly recall how this works and then indicate how this presentation can be derived along the above lines as a presentation of [[circle n-bundles with connection]].

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ the **Deligne complex** is the [[chain complex]] of [[sheaves]] (on [[SmoothMfd]] in general or on [[CartSp]] for our purposes here) of [[abelian group]]s given as follows

$$
 \mathbb{Z}(n+1)^\infty_D = 
  \left[
    \array{
      C^\infty(-,\mathbb{R}/\mathbb{Z})
       &\stackrel{d_{dR}}{\to}&
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
      \cdots
        &\stackrel{d_{dR}}{\to}&
      \Omega^{n-1}(-)
        &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)      
      \\
       n && n-1 && \cdots && 1 && 0
    }
  \right]
  \,.
$$

=--

This is similar to the $n$-fold shifted [[de Rham complex]] with two important differences

1. In degree $n$ we have the sheaf of $U(1)$-valued functions, not of $\mathbb{R}$-valued functions (= 0-forms). The action of the de Rham differential on this is sometimes written $d log : C^\infty(-, U(1)) \to \Omega^1(-)$. But if we think of $U(1) \simeq \mathbb{R}/\mathbb{Z}$ then it is just the ordinary de Rham differential applied to any representative in $C^\infty(-, \mathbb{R})$ of an element in $C^\infty(-, \mathbb{R}/\mathbb{Z})$.

1. In degree 0 we do not have closed differential $n$-forms (as one would have for the the de Rham complex shifted into non-negative degree), but all $n$-forms.


As before we may use of the [[Dold-Kan correspondence]] $\Xi : Ch_\bullet^{+} \stackrel{\simeq}{\to} sAb \stackrel{U}{\to} sSet$ to identify sheaves of [[chain complex]]es with [[simplicial presheaves|simplicial sheaves]].

For $\{U_i \to X\}$ a [[good open cover]], the [[Deligne cohomology]] of $X$ in degree $(n+1)$ is 

$$
  H_{diff}^{n+1}(X)
  =
  \pi_0 [CartSp^{op}, sSet](
     C(\{U_i\}), \Xi \mathbb{Z}(n+1)^\infty_D
  )
  \,.
$$

Further using the [[Dold-Kan correspondence]] this is equivalently the cohomology of the Cech-Deligne [[double complex]]. A Deligne cocycle in degre $(n+1)$ then is a tuple

$$
  (g_{i_0, \cdots, i_n}, \cdots, A_{i j k}, B_{i j}, C_{i})
$$

with 

* $C_i \in \Omega^n(U_i)$;

* $B_{i j} \in \Omega^{n-1}(U_i \cap U_j)$;

* $A_{i j k } \in \Omega^{n-2}(U_i \cap U_j \cap U_k)$

* and so on

* $g_{i_0, \cdots, i_n} \in C^\infty(U_{i_0} \cap \cdots \cap U_{i_n} , U(1))$

satisfying the cocycle condition

$$
  (d_{dR} + (-1)^{deg}\delta)
  (g_{i_0, \cdots, i_n}, \cdots, A_{i j k}, B_{i j}, C_{i})
  = 0
  \,,
$$

where $\delta = \sum_{i} (-1)^i p_i^*$ is the alternating sum of the pullback of forms along the face maps of the [[Cech nerve]].

This is a sequence of conditions of the form

* $C_i - C_j = d B_{i j}$;

* $B_{i j} - B_{i k} + B_{j k} = d A_{i j k}$;

* and so on

* $(\delta g)_{i_0, \cdots, i_{n+1}} = 0$.

For low $n$ we have seen these conditions in the dicussion of [[line bundle]]s and of line 2-bundles ([[bundle gerbe]]s) with connection above. Generally, for any $n \in \mathbb{N}$, this is Cech-cocycle data for a [[circle n-bundle with connection]], where

* $C_i$ are the local connection $n$-forms;

* $g_{i_0, \cdots, i_n}$ is the transition function of the circle $n$-bundle.

We now indicate how the Deligne complex may be derived from differential refinement of cocycles
for circle $n$-bundles along the lines of the above discussions.

Write

$$
  \mathbf{B}^n U(1)_{ch} := \Xi U(1)[n]
  \,,
$$

for the simplicial presheaf given under the [[Dold-Kan correspondence]] by the chain complex

$$
  U(1)[n] = 
  \left(
     C^\infty(-,U(1)) \to 0 \to \cdots \to 0
  \right)
$$

with the sheaf represented by $U(1)$ in degree $n$.


+-- {: .num_prop}
###### Proposition

For $\{U_i \to X\}$ an [[open cover]] of a smooth manifold $X$ and $C(U)$ its [[Cech nerve]], [[∞-anafunctor]]s

$$
  \array{
    C(U) &\stackrel{g}{\to}& \mathbf{B}^n U(1)_{ch}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

are in natural bijection with tuples of [[smooth function]]s

$$
  g_{i_0 \cdots i_n} : U_{i_0} \cap \cdots \cap U_{i_n} \to \mathbb{R}/\mathbb{Z}
$$

satisfying 

$$
  (\partial g)_{i_0 \cdots i_{n+1}}
  :=
  \sum_{k = 0}^{n} g_{i_0 \cdots i_{k-1} i_k \cdot i_n}
  = 0
  \,,
$$

that is, to cocycles in degree $n$ [[Cech cohomology]] on $U$ with values in $U(1)$.

Transformations

$$
  \array{
    C(U)\cdot \Delta^1 &\stackrel{(g \stackrel{\lambda}{\to} g')}{\to}& \mathbf{B}^n U(1)_{ch}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X \cdot \Delta^1
  }
$$

are in natural bijection with tuples of [[smooth function]]s

$$
  \lambda_{i_0 \cdots i_{n-1}} : U_{i_0} \cap \cdots \cap U_{i_{n-1}} \to \mathbb{R}/\mathbb{Z}
$$

such that

$$
  g'_{i_0 \cdots i_n}
  - 
  g_{i_0  \cdots i_n} 
  = 
  (\delta \lambda)_{i_0 \cdots i_n}
  \,,
$$

that is, to &Ccaron;ech coboundaries.


=--

The $\infty$-bundle $P \to X$ classified by such a cocycle we may call a 
[[circle n-bundle]]. For $n = 1$ this reproduces the ordinary $U(1)$-[[principal bundle]]s that we considered before, for $n =2 $ the [[bundle gerbe]]s and for $n=3$ the [[bundle 2-gerbe]]s.

To equip these circle $n$-bundles with connections, we consider the differential refinements $\mathbf{B}^n U(1)_{diff}$, $\mathbf{B}^n U(1)_{conn}$ and $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$.

+-- {: .num_defn}
###### Definition

Write

$$
  \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{ch} := 
  \Xi\left(
    \Omega^1(-) \stackrel{d_{dR}}{\to}
    \Omega^2(-) \stackrel{d_{dR}}{\to}
    \cdots
    \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)
  \right)
$$

-- the image under $\Xi$ of the truncated [[de Rham complex]] -- and

$$
  \mathbf{B}^n U(1)_{diff,ch} = 
  \left\{
   \array{
      (-) &\to& \mathbf{B}^n U(1)
     \\
     \downarrow && \downarrow
     \\
     \mathbf{\Pi}(-) &\to& \mathbf{B}^n INN(U(1))
   }
  \right\}
  =
  \Xi
  \left(
    \array{
      C^\infty(-,\mathbb{R}/\mathbb{Z}) 
      &\stackrel{d_{dR}}{\to}&
      \Omega^1(-) &\stackrel{d_{dR}}{\to}&
      \cdots
      &
      \to
      &
      \Omega^n(-)
      \\
      \oplus & \nearrow_{\mathrlap{Id}} & \cdots 
      &
      &\cdots& 
      \nearrow_{\mathrlap{Id}}
      \\
      \Omega^1(-) 
      &\stackrel{d_{dR}}{\to}& 
      \cdots
      &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
    }
  \right)
$$

and

$$
  \mathbf{B}^n U(1)_{conn,ch}
  = 
  \Xi\left(
    C^\infty(-, \mathbb{R}/\mathbb{Z})
    \stackrel{d_{dR}}{\to} 
    \Omega^1(-) \stackrel{d_{dR}}{\to}
    \Omega^2(-) \stackrel{d_{dR}}{\to}
    \cdots
    \stackrel{d_{dR}}{\to} \Omega^n(-)
  \right)
$$

-- the [[Deligne cohomology|Deligne complex]].

There is a canonical morphism

$$
  curv : \mathbf{B}^n U(1)_{diff,ch} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)_{ch}
  \,.
$$



=--


+-- {: .num_lemma}
###### Observation

We have a [[pullback]] diagram

$$
  \array{
    \mathbf{B}^n U(1)_{conn,ch}
    &\to&
    \Omega^{n+1}_{cl}(-)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}^n U(1)_{diff,ch}
    &\stackrel{curv}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B}^{n-1}U(1)_{ch}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^n U(1)_{ch}
  }
$$

in $[Cart^{op}, sSet]$.

This models a [[homotopy pullback]]

$$
  \array{
    \mathbf{B}^n U(1)_{conn}
    &\to&
    \Omega^{n+1}_{cl}(-)
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    \mathbf{B}^n U(1)
    &\stackrel{curv}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B}^{n-1}U(1)
  }
$$

in the [[(∞,1)-topos]] $\mathbf{H} = $[[Smooth∞Grpd]] and this implies (in particular) for all smooth manifolds $X$ a homtotopy pullback

$$
  \array{
    \mathbf{H}(X,\mathbf{B}^n U(1)_{conn})
    &\to&
    \Omega^{n+1}_{cl}(X)
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\to&
    \mathbf{H}(X,\mathbf{\flat}_{dR}\mathbf{B}^{n-1}U(1))
  }
  \,.
$$


=--

Here cocycles in $\mathbf{H}(X, \mathbf{B}^n U(1)_{conn})$ are modeled by [[∞-anafunctor]]s $X \stackrel{\simeq}{\leftarrow} C(U) \stackrel{g}{\to} \mathbf{B}^n U(1)_{conn}$, which are in natural bijection with tuples

$$
  \left(
     C_{i}, B_{i_0 i_1}, A_{i_0 i_1, i_2}, 
     \cdots
     Z_{i_0 \cdots i_{n-1}},
     g_{i_0 \cdots i_{n}}
  \right)
  \,,
$$

where $C_i \in \Omega^n(U_i)$, $B_{i_0 i_1} \in \Omega^{n-1}(U_{i_0} \cap U_{i_1})$, etc. such that

$$
  C_{i_0} - C_{i_1} = d B_{i_0 i_1}
$$

and

$$
  B_{i_0 i_1} - B_{i_0 i_2} + B_{i_1 i_2} = d A_{i_0 i_1 i_2}
  \,,
$$

etc. This is a cocycle in [[Cech cohomology|Cech]]-[[Deligne cohomology]]. We may think of this as encoding a [[circle n-bundle with connection]]. The forms $(C_i)$ are the local connection $n$-forms.

**Remark.** Everything in this construction turns out to follow from general abstract reasoning in every [[cohesive (∞,1)-topos]] $\mathbf{H}$ --- except the sheaf $\Omega^n_{cl}(-)$ of closed $n$-forms, which is a non-intrinsic truncation of $\mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)$ whose definition uses concretely the choice of model $[CartSp^{op}, sSet]$. But since by the above this object is used to pick homotopy fibers, and since these depend up to equivalence only on the connected component over which they are taken, for fixed $X$ no information is lost by passing instead to the de Rham cohomology set $H_{dR}^{n+1}(X)$ and choosing a morphism $H_{dR}^{n+1}(X) \to \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1))$ that picks a closed $(n+1)$-form in each cohomology class. Then we can replace the above by the homotopy pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}^n U(1))
    &\to&
    H^{n+1}_{dR}(X)
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\to&
    \mathbf{H}(X,\mathbf{\flat}_{dR}\mathbf{B}^{n-1}U(1))
  }
$$

without losing information. And this is defined fully intrinsically.



The definition of $\infty$-connections on $G$-principal $\infty$-bundles for nonabelian $G$ may be reduced to this definition, by _approximating_ every $G$-cocylce 
$X \stackrel{\simeq}{\leftarrow} C(U) \to \mathbf{B}G$ by abelian cocycles by postcomposing with all possible [[characteristic class]]es $\mathbf{B}G \stackrel{\simeq}{\leftarrow} \hat \mathbf{B}G\to \mathbf{B}^n U(1)$ to extract a circle $n$-bundle from it. This is what we turn to now.




## The $\infty$-Chern-Weil homomorphism
 {#InfityCWHomomorphism}

We now come to the discussion the [[Chern-Weil homomorphism]] and its generalization to the [[∞-Chern-Weil homomorphism]].

We have seen [above](#http://ncatlab.org/nlab/show/infinity-Chern-Weil+theory+introduction#PrincipalNBundles) $G$-principal $\infty$-bundles for general smooth $\infty$-groups $G$ and in particular for abelian groups $G$. Naturally, the abelian case is easier and more powerful statements are known about this case. A general strategy for studying nonabelian $\infty$-bundles therefore is to _approximate_ them by abelian bundles. This is achieved by considering [[characteristic class]]es. Roughly, a characteristic class is a map that functorially sends $G$-principal $\infty$-bundles to $\mathbf{B}^n K$-principal $\infty$-bundles, for some $n$ and some abelian group $K$. In some cases such an assignment may be obtained by integration of infinitesimal data. If so, then the assignment refines to one of $\infty$-bundles [[connection on an ∞-bundle|with connection]]. For $G$ an ordinary [[Lie group]] this is then what is called the [[Chern-Weil homomorphism]]. For general $G$ we call it  the [[∞-Chern-Weil homomorphism]].



### Motivating examples
 {#ExamplesForChernWeil}

A simple motivating example for [[characteristic class]]es and the [[Chern-Weil homomorphism]]
is the construction of [[determinant line bundle]]s.

+-- {: .num_example}
###### Example

Let $N \in \mathbb{N}$. Consider the [[unitary group]] $U(N)$.
By its definition as a [[matrix Lie group]], this comes canonically equipped with the [[determinant]] function

$$
  det : U(N) \to U(1)
$$

and by the standard properties of the determinant, this is in fact a group homomorphism. Therefore this has a [[delooping]] to a morphism of [[Lie groupoid]]s

$$
  \mathbf{B}det : \mathbf{B}U(N) \to \mathbf{B}U(1)
  \,.
$$

Under [[geometric realization of simplicial topological spaces|geometric realization]] this maps to a morphism

$$
  |\mathbf{B} det| : B U(N) \to B U(1) \simeq K(\mathbb{Z},2)
$$

of [[topological space]]s. This is a [[characteristic class]] on the 
[[classifying space]] [[BU(n)|$B U(N)$]]: the first [[Chern class]] (see [[determinant line bundle]] for more on this).

By postcomposion with $\mathbf{B}det$ of the classifying morphisms for principal bundles, it acts on principal bundles: postcomposition of a [[Cech cohomology|Cech]] cocycle 

$$
  \array{
    P : & C(\{U_i\}) &\stackrel{(g_{i j})}{\to}& \mathbf{B} U(N)
    \\
    & \downarrow^{\mathrlap{\simeq}}
    \\
    & X
  }
$$

for a $U(N)$-[[principal bundle]] on a [[smooth manifold]] $X$
with this characteristic class yields the cocycle 

$$
  \array{
    det P : & C(\{U_i\}) &\stackrel{(g_{i j})}{\to}& \mathbf{B} U(N)
    &\stackrel{\mathbf{B}det}{\to}& \mathbf{B}U(1)
    \\
    & \downarrow^{\mathrlap{\simeq}}
    \\
    & X
  }
$$

for a circle bundle (or its [[associated bundle|associated]] [[line bundle]])
with transition functions $(det (g_{i j}))$:
the [[determinant line bundle]] of $P$. The unique class 

$$
  [det P] \in 
  H^2(X, \mathbb{Z})
$$ 

of this line bundle is a characteristic of the original unitary bundle: its first [[Chern class]] $c_1(P)$

$$
  [det P] = c_1(P)
  \,.
$$

This construction directly extends to the case where the bundles carry 
[[connection on a bundle|connections]].

We may canonically identify the [[Lie algebra]] 
$\mathfrak{u}(n)$ with the
[[matrix Lie algebra]] of skew-hermitian matrices on which we have the
[[trace]] operation

$$
  tr : \mathfrak{u}(n) \to \mathfrak{u}(1) = i \mathbb{R}
  \,.
$$

This is the differential version of the determinant in that when regarding the [[Lie algebra]] as the [[infinitesimal space|infinitesimal neighbourhood]] of the neutral element in $U(N)$ (see [[∞-Lie algebroid]] for more on this) the determinant becomes the trace under the exponential map

$$
  det (1 + \epsilon A) = 1 + \epsilon tr(A)
$$

for $\epsilon^2 = 0$.

It follows that for $tra_\nabla : \mathbf{P}_1(U_i) \to \mathbf{B}U(N)$ the [[parallel transport]] of a [[connection on a bundle|connection]] on $P$ locally given by a 1-forms $A \in \Omega^1(U_i, \mathfrak{u}(N))$ by

$$
  tra_\nabla(\gamma) = \mathcal{P} \exp \int_{[0,1]} \gamma^* A
$$

the determinant parallel transport

$$
  det tra_\nabla : \mathbf{P}_1(U_i) \stackrel{tra_\nabla}{\to}
   \mathbf{B} U(N) \stackrel{det}{\to} \mathbf{B}U(1)
$$
is locally given by the formula

$$
  det tra_\nabla(\gamma) = \mathcal{P} \exp \int_{[0,1]} \gamma^* tr A
$$

which means that the local connection forms on the determinant line bundle are obtained from those of the unitary bundle by tracing.

$$
  (det,tr) : \{(g_{i j}), (A_i)\} \mapsto
   \{(det  g_{i j}), (tr A_i)\}
  \,.
$$

This construction extends to a functor

$$
  (\hat \mathbf{c}_1) := (det, tr) :  U(N) Bund_{conn}(X) \to U(1) Bund_{conn}(X)
$$

natural in $X$, that sends $U(n)$-principal bundles with connection to 
[[circle n-bundle with connection|circle bundles with connection]], hence to cocycles in degree-2 [[ordinary differential cohomology]].

This assignment remembers of a unitary bundle one inegral class and its differential refinement:

* the integral class of the determinant bundle is the 
  first [[Chern class]] the $U(N)$-bundle

  $$
    [\hat \mathbf{c}_1(P)] = c_1(P)
    \,;
  $$

* the [[curvature]] 2-form of its connection is a representative
  in de Rham cohomology of this class

  $$
    [F_{\nabla_{\hat \mathbf{c}_1(P)}}] = c_1(P)_{dR}
    \,.
  $$

$$
  \array{
     && H^2_{diff}(X)
     \\
     & \swarrow &&  \searrow
     \\
     H^2(X,\mathbb{Z}) && && \Omega^2_{cl}(X) 
  }
  \;\;\;\;
  \array{
    && \hat \mathbf{c}_1
    \\
    & \swarrow && \searrow
    \\
    c_1(P) &&&& tr F_\nabla
  }
  \,.
$$


Equivalently this assignment is given by postcomposition of cocycles with a morphism of [[smooth ∞-groupoid]]s

$$
  \hat \mathbf{c}_1 : \mathbf{B}U(N)_{conn} \to \mathbf{B}U(1)_{conn}
  \,.
$$

We say that $\hat \mathbf{c}_1$ is a **differential characteristic class**, the differential refinement of the first [[Chern class]]. 


=--


In (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#CechCocyclesForCharClasses">BrylinskiMacLaughlin</a>) an algorithm is given for contructing
differential characteristic classes on Cech cocycles in this fashion for 
more general [[Lie algebra cohomology|Lie algebra cocycles]].

For instance these authors give the following construction for the diffrential refinement of the first [[Pontryagin class]].

+-- {: .num_example #BMConstruction}
###### Example

Let $N \in \mathbb{N}$, write $Spin(N)$ for the [[Spin group]]
and consider the canonical [[Lie algebra cohomology]] 3-cocycle

$$
  \mu = \langle -,[-,-]\rangle : \mathfrak{so}(n) \to \mathbf{b}^2 \mathbb{R}
$$

on [[semisimple Lie algebra]]s, where $\langle -,- \rangle$ is the [[Killing form]] [[invariant polynomial]].

Let $(P \to X, \nabla)$ be a $Spin(N)$-[[principal bundle]] [[connection on a bundle|with connection]]. Let $A \in \Omega^1(P, \mathfrak{so}(N))$ be the [[Ehresmann connection]] 1-form on the total space of the bundle.

Then construct a [[Cech cohomology|Cech cocycle]] for [[Deligne cohomology]] in degree 4 as follows:

1. pick an [[open cover]] $\{U_i \to X\}$ such that there is a choice of 
   local [[section]]s $\sigma_i : U_i \to P$. Write 

   $$
     (g_{i j}, A_i) := (\sigma_i^{-1} \sigma_j, \sigma_i^* A)
   $$

   for the induced [[Cech cohomology|Cech]] cocycle.

1. Choose a lift of this cocycle to an assignment 

   * of based paths in $Spin(N)$ to double intersections 
     
     $$
       \hat g_{i j} : U_{i j}\times \Delta^1 \to Spin(N)
       \,,
     $$

     with
     $\hat g_{i j}(0) = e$ and $\hat g_{i j}(1) = g_{i j}$;

   * of based 2-simplices between these paths to triple intersections
     
     $$
       \hat g_{i j k} : U_{i j k}\times \Delta^2 \to Spin(N)
       \,;
     $$  

     restricting to these paths in the obvious way;

   * similarly of based 3-simplices between these paths to quadruple intersections
     
     $$
       \hat g_{i j k l} : U_{i j k l}\times \Delta^3 \to Spin(N)
       \,.
     $$

  Such lifts always exists, because the Spin group is [[connected]] (because already $SO(N)$ is), [[simply connected]] (because $Spin(N)$ is the [[universal cover]] of $SO(N)$) and also has $\pi_2(Spin(N)) = 0$ (because this is the case for every compact Lie group).

1. Define from this a [[Deligne cohomology|Deligne-cochain]] by setting

   $$
     (g_{i j k l}, A_{i j k}, B_{i j}, C_{i})
     :=
     \left(
      \array{
       \int_{\Delta^3} (\sigma_i \cdot\hat g_{i j k l})^* \mu(A) mod \mathbb{Z},
        \\ 
       \int_{\Delta^2} (\sigma_i\cdot \hat g_{i j k})^* cs(A),
        \\
       \int_{\Delta^1} (\sigma_i \cdot \hat g_{i j})^* cs(A),
        \\
       \sigma_i^* \mu(A)
      }
     \right)
     \,,
   $$

   where $cs(A) = \langle A \wedge F_A\rangle + c \langle A \wedge [A \wedge A]\rangle  $ is the [[Chern-Simons form]] of the connection form $A$ with respect to the cocycle $\mu(A) = \langle A \wedge [A \wedge A]\rangle$.


They then prove:

1. This is indeed a [[Deligne cohomology]] cocycle;

1. It represents the differential refinement of the first 
   fractional [[Pontryagin class]] of $P$.

=--

$$
  \array{
    && H^4_{diff}(X)
    \\
    & \swarrow && \searrow
    \\
    H^4(X,\mathbb{Z}) &&&& \Omega^4_{cl}(X)
  }
  \;\;\;\;
  \array{
     && \frac{1}{2} \hat \mathbf{p}_1
     \\
     & \swarrow && \searrow
     \\
     \frac{1}{2}p_1 &&&& d cs(A)
  }
$$

In the form in which we have (re)stated this result here the second statement amounts, in view of the first statement, to the observation that the [[curvature]] 4-form of the Deligne cocycle is proportional to

$$
  \langle F_A \wedge F_A \rangle \in \Omega^4_{cl}(X)
$$

which represents the first Pontryagin class in [[de Rham cohomology]]. 
Therefore the key observation is that we have a Deligne cocycle at all. 
This can be checked directly, if somewhat tediously, by hand. But then the question remains: where does this successful _Ansatz_ come from? And is it _natural_ ? For instance: does this construction extend to a morphism of [[smooth ∞-groupoid]]s

$$
  \frac{1}{2}\hat \mathbf{p}_1 : \mathbf{B} Spin(N)_{conn}
   \to \mathbf{B}^3 U(1)_{conn}
$$

from Spin-[[principal bundle]]s with connection to [[circle n-bundle with connection|circle 3-bundles with connection]]?

In the following we give a natural presentation of the 
[[∞-Chern-Weil homomorphism]] by means of [[Lie integration]] of $L_\infty$-algebraic data to [[simplicial presheaves]]. Among other things, this construction yields an understanding of why this construction is what it is and does what it does. In prop. \ref{ReproducingBrylinskiMacLaughlin} we reproduce the above example.

The construction proceeds in the following broad steps

1. The [[infinitesimal object|infinitesimal]] analog of a characteristic class
   $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ is a [[∞-Lie algebra cohomology|L-∞ algebra cocycle]]

   $$
     \mu : \mathfrak{g} \to b^{n-1} \mathbb{R}
     \,.
   $$

1. There is a formal procedure of universal [[Lie integration]] which sends this to a morphism of [[smooth ∞-groupoid]]s

   $$
     \exp(\mu) : \exp(\mathfrak{g}) \to \exp(b^{n-1} \mathbb{R}) \simeq \mathbf{B}^n \mathbb{R}
   $$

   presented by a morphism of [[simplicial presheaves]] on [[CartSp]].

1. By finding a [[Chern-Simons element]] $cs$ that witnesses the [[transgression]] of $\mu$ to an [[invariant polynomial]] on $\mathfrak{g}$ this construction has a differential refinement to a morphism

   $$
     \exp(\mu,cs) : \exp(\mathfrak{g})_{conn} \to \mathbf{B}^n \mathbb{R}_{conn}     
   $$

   that sends $L_\infty$-algebra valued connections to [[circle n-bundle with connection|line n-bundles with connection]].

1. The $n$-[[truncated|truncation]] $\mathbf{cosk}_{n+1} \exp(\mathfrak{g})$ of the object on the left produces the smooth $\infty$-groups on interest -- $\mathbf{cosk}_{n+1} \exp(\mathfrak{g}) \simeq \mathbf{B}G$ -- and the corresponding truncation of $\exp((\mu,cs))$ carves out the [[lattice]] $\Gamma$ of [[period]]s in $G$ of the cocycle $\mu$ inside $\mathbb{R}$. The result is the differential characteristic class

   $$
     \exp(\mu,cs) : \mathbf{B}G_{conn} \to \mathbf{B}^n \mathbb{R}/\Gamma_{conn}
     \,.
   $$

   Typically we have $\Gamma \simeq \mathbb{Z}$ such that this then reads

   $$
     \exp(\mu,cs) : \mathbf{B}G_{conn} \to \mathbf{B}^n U(1)_{conn}
     \,.
   $$

### $\infty$-Lie theory
 {#LieTheory}

We discuss [[L-∞ algebra]]s and more generally [[∞-Lie algebroid]]s -- the higher analogs of [[Lie algebra]]s and [[Lie algebroid]]s -- and their [[Lie integration]] to [[smooth ∞-groupoid]]s presented by [[simplicial presheaves]].


#### $\infty$-Lie algebroids
 {#InfLieAlgebroids}

There is a precise sense in which one may think of a [[Lie algebra]] $\mathfrak{g}$ as the [[infinitesimal space|infinitesimal]] sub-object of the delooping groupoid $\mathbf{B}G$ of the corresponding Lie group $G$. Without here going into the details of this relation (which needs a little bit of [[(∞,1)-topos]]-theory), we want to build certain [[∞-Lie groupoid]]s from the knowledge of their infinitesimal subobjects: these subobjects are [[∞-Lie algebroid]]s and specifically [[∞-Lie algebra]]s -- traditionally known as $L_\infty$-algebras. 

A quick but useful way of formalizing what this means is to observe that ordinary (finite-dimensional) [[Lie algebra]]s $(\mathfrak{g}, [-,-])$ are entirely encoded, dually, in their [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{g}^*, d = [-,-]^*) $: free [[graded algebra|graded-commutative algebra]]s over the ground field $k$ (which is $\mathbb{R}$ for our purposes here) on the vector space $\mathfrak{g}^*[1]$ equipped a differential $d$ of degree +1 and squaring to 0.

Simply by replacing in this characterization the vector space $\mathfrak{g}^*$ be an $\mathbb{N}$-[[graded vector space]], we arrive at the notion of [[∞-Lie algebra]]: the elements of $\mathfrak{g}[1]$ in degree $k$ are the infinitesimal [[k-morphism]]s.  Moreover, replacing in this characterization the ground field $k$ by an algebra of [[smooth function]]s on a manifold $\mathfrak{a}_0$, we obtain the notion of an [[∞-Lie algebroid]] $\mathfrak{g}$ over $\mathfrak{a}_0$. Morphisms $\mathfrak{a} \to \mathfrak{b}$ of such [[∞-Lie algebroid]]s are dually precisely morphisms of [[dg-algebra]]s $CE(\mathfrak{a}) \leftarrow CE(\mathfrak{b})$.

The following definition glosses over some fine print but is entirely sufficient for our present discussion.

+-- {: .num_defn}
###### Definition

The category of [[∞-Lie algebroid]]s is the [[opposite category]] of the [[full subcategory]] of [[dgAlg]] 

$$
  \infty LieAlgbd \subset (dgAlg)^{op}
$$

on graded-commutative cochain [[dg-algebra]]s in non-negative degree whose underlying [[graded algebra]] is a [[exterior algebra]] over the degree-0 algebra.

=--


+-- {: .num_example}
###### Examples

* A _strict_ $\infty$-Lie algebra is a [[dg-Lie algebra]] $(\mathfrak{g}, \partial, [-,-])$ with $(\mathfrak{g}^*, \partial^*)$ a [[cochain complex]] in non-negative degree. With $\mathfrak{g}^*$ denoting the degreewise dual, the corresponding CE-algebra is $CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{g}^*, d_{CE} = [-,-]^* + \partial^*$. 

* We had already seen [above](#ConnectionOn2Bundle) the infinitesimal approximation of a [[Lie 2-group]]: this is a [[Lie 2-algebra]]. If the Lie 2-group is a smooth [[strict 2-group]] it is encoded equivalently by a [[crossed module]] of ordinary Lie groups, and the corresponding Lie 2-algebra is given by a [[differential crossed module]] of ordinary [[Lie algebra]]s.

* The [[tangent Lie algebroid]] $T X$ of a [[smooth manifold]] $X$ is the infinitesimal approximation to its [[fundamental ∞-groupoid]]. Its CE-algebra is the [[de Rham complex]] 

  $CE(T X) = \Omega^\bullet(X)$.


* For $n \in \mathbb{N}$, $n \geq 1$, the Lie $n$-algebra $b^{n-1}\mathbb{R}$ is the infinitesimal approximation to $\mathbf{B}^n U(\mathbb{R})$ and $\mathbf{B}^n \mathbb{R}$. Its CE-algebra is the dg-algebra on a single generators in degree $n$, with vanishing differential.

* For any $\infty$-Lie algebra $\mathfrak{g}$ there is an $\infty$-Lie algebra $inn(\mathfrak{g})$ defined by the fact that its CE-algebra is the [[Weil algebra]] of $\mathfrak{g}$:

  $$
    CE(inn(\mathfrak{g})) = 
    W(\mathfrak{g}) = 
    (\wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1]), 
    d_{W}|_{\mathfrak{g}^*} = d_{CE} + \sigma )
    \,,
  $$

  where $\sigma : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ is the grading shift isomorphism, extended as a [[derivation]].

=--

#### Lie integration
 {#LieIntegration}

We discuss [[Lie integration]]: a construction that sends an [[∞-Lie algebroid|L-∞ algebroid]] to a [[smooth ∞-groupoid]] of which it is the infinitesimal approximation.

The construction we want to describe may be understood as a generalization
of the following proposition. This is classical, even if maybe not reflected in the standard textbook literature to the extent it deserves to be (see [[Lie integration]] for details and references).

+-- {: .num_def}
###### Definition

For $\mathfrak{g}$ a (finite-dimensional) [[Lie algebra]], let $\exp(\mathfrak{g}) \in [CartSp^{op}, sSet]$ be the [[simplicial presheaf]] given by the assignment

$$
  \exp(\mathfrak{g})  : U
  \mapsto Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(U \times \Delta^\bullet)_{vert})
  \,,
$$

in degree $k$ of [[dg-algebra]] [[homomorphism]]s from the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ to the dg-algebra of [[vertical differential forms]] with respect to the trivial [[bundle]] $U \times \Delta^k \to U$.

=--

+-- {: .num_remark}
###### Remark

Shortly we will be considering variations of such assignments that are best thought about when writing out the [[hom-set]]s on the right here as sets of arrows; as in

$$
  \exp(\mathfrak{g})
   :
   (U,[k])
    \mapsto
    \left\{ 
      \array{
        \Omega^\bullet_{vert}(U \times \Delta^k) 
        &\stackrel{A_{vert}}{\leftarrow}&
        CE(\mathfrak{g})
      }
    \right\}
   ) 
  \,.
$$

=--

For $\mathfrak{g}$ an ordinary [[Lie algebra]] it is an ancient (see <a href="http://ncatlab.org/nlab/show/Chern-Weil%20theory#History">Chern-Weil theory -- history</a>) 
and simple but important observation that dg-algebra morphisms  $\Omega^\bullet(\Delta^k) \leftarrow CE(\mathfrak{g})$ are in natural bijection with [[Lie-algebra valued 1-form]]s that are _flat_ in that their [[curvature]] 2-forms vanish: the 1-form itself determines precisely a morphism of the underlying [[graded algebra]]s, and the respect for the differentials is exactly the flatness condition. It is this elementary but similarly important observation that [historically](#http://ncatlab.org/nlab/show/Chern-Weil+theory#History) led [[Eli Cartan]] to [[Cartan calculus]] and the algebraic formulation of [[Chern-Weil theory]].

One finds that it makes good sense to generally, for $\mathfrak{g}$ any [[∞-Lie algebra]] or even [[∞-Lie algebroid]], think of $Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(\Delta^k))$ as the set of [[∞-Lie algebroid valued differential forms]] whose curvature forms (generally a whole tower of them) vanishes.

+-- {: .num_prop}
###### Proposition

Let $G$ be the [[simply-connected]] [[Lie group]] integrating $\mathfrak{g}$ according to [[Lie's three theorems]] and  $\mathbf{B}G \in [CartSp^{op}, Grpd]$ its [[delooping]] [[Lie groupoid]] regarded as a [[groupoid]]-valued [[presheaf]] on [[CartSp]]. Write $\tau_1(-)$ for the 
[[truncated|truncation]] operation that quotients out [[2-morphism]]s in a simplicial presheaf to obtain a presheaf of groupoids. 

We have an [[isomorphism]]

$$
  \mathbf{B}G  
  =
  \tau_1
  \exp(\mathfrak{g})
  \,.
$$

=--


To see this, observe that the presheaf $\exp(\mathfrak{g})$ has as 1-morphisms $U$-parameterized families of $\mathfrak{g}$-valued 1-forms $A_{vert}$ on the interval, and as 2-morphisms $U$-parameterized families of _flat_ 1-forms on the disk, interpolating between these. By identifying these 1-forms with the pullback of the [[Maurer-Cartan form]] on $G$, we may equivalently think of the 1-morphisms as based smooth paths in $G$ and 2-morphisms smooth [[homotopies]] relative endpoints between them. Since $G$ is [[simply-connected]] this means that after dividing out 2-morphisms only the endpoints of these paths remain, which identify with the points in $G$. 

The following proposition establishes the Lie integraiton of the shifted
1-dimensional abelian [[L-∞ algebras]] $b^{n-1} \mathbb{R}$.

+-- {: .num_prop #IntegrationOfBnR}
###### Proposition

For $n \in \mathbb{N}$, $n \geq 1$. Write 

$$
  \mathbf{B}^n \mathbb{R}_{ch} :=
   \Xi \mathbb{R}[n]
$$

for the [[simplicial presheaf]] on [[CartSp]] that is the image of the sheaf of [[chain complex]]es [[representable functor|represented]] by $\mathbb{R}$ in degree $n$ and 0 in other degrees, under the [[Dold-Kan correspondence]] $\Xi : Ch_\bullet^+ \to sAb \to sSet$.

Then there is a canonical morphism

$$
  \int_{\Delta^\bullet} : 
   \exp(b^{n-1}\mathbb{R})
   \stackrel{\simeq}{\to}
   \mathbf{B}^n \mathbb{R}_{ch}
$$

given by [[fiber integration]] of differential forms along $U \times \Delta^n \to U$ and this is an equivalence (a global equivalence in the [[model structure on simplicial presheaves]]).

=--

The proof of this statement is discussed at [[Lie integration]]. 

This statement will make an appearance repeatedly in the following discussion. Whenever we translate a construction given in terms $\exp(-)$ into a more convenient [[chain complex]] representation.

#### Characteristic classes from Lie integration 
  {#LieIntOfCocycles}

We now describe [[characteristic class]]es and then furhter below [[curvature characteristic form]]s on $G$-bundles in terms of [[Lie integration]] to [[simplicial presheaves]]. For that purpose it is useful for a moment to ignore the truncation issue -- to come back to it later -- and consider these simplicial presheaves untruncated. 

To see characteristic classes in this picture, write $CE(b^{n-1} \mathbb{R})$ for the commutative real [[dg-algebra]] on a single generator in degree $n$ with vanishing differential. As our notation suggests, this we may think as the [[Chevalley-Eilenberg algebra]] of a _higher Lie algebra_  -- the [[∞-Lie algebra]] $b^{n-1} \mathbb{R}$ -- which is an [[Eilenberg-MacLane object]] in the [[homotopy theory]] of [[∞-Lie algebra]]s, representing [[∞-Lie algebra cohomology]] in degree $n$ with coefficients in $\mathbb{R}$.

Restating this in elementary terms, this just says that [[dg-algebra]] [[homomorphism]]s

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1}\mathbb{R}) : \mu
$$

are in natural bijection with elements $\mu \in CE(\mathfrak{g})$ of degree $n$, that are closed, $d_{CE(\mathfrak{g})} \mu = 0$. This is the classical description of a cocycle in the [[Lie algebra cohomology]] of $\mathfrak{g}$.

+-- {: .num_defn}
###### Definition

Every such $\infty$-Lie algebra cocycle $\mu$ induces a morphism of simplicial presheaves

$$
  \exp(\mu) : \exp(\mathfrak{g}) \to \exp(b^n \mathbb{R})
$$
  
given by postcomposition

$$
  \Omega^\bullet_{vert}(U \times \Delta^l)
  \stackrel{A_{vert}}{\leftarrow}
  CE(\mathfrak{g})
  \stackrel{\mu}{\leftarrow}
  CE(b^n \mathbb{R})
  \,.
$$

=--

+-- {: .num_example}
###### Example
**(first Pontryagin class)**

Assume $\mathfrak{g}$ to be a [[semisimple Lie algebra]], let $\langle -,-\rangle$ be the [[Killing form]] and $\mu = \langle -,[-,-]\rangle$ the corresponding 3-cocycle in [[Lie algebra cohomology]]. We may assume without restriction that this cocycle is normalized such that its left-invariant continuation to a 3-form on $G$ has integral [[period]]s. Observe that since $\pi_2(G)$ is trivial we have that the 3-[[coskeleton]] of $\exp(\mathfrak{g})$ is equivalent to $\mathbf{B}G$. By the inegrality of $\mu$, the operation of $\exp(\mu)$ on $\exp(\mathfrak{g})$ followed by integration over simplices, 
as in prop. \ref{IntegrationOfBnR}, descends to an [[∞-anafunctor]] from $\mathbf{B}G$ to $\mathbf{B}^3 U(1)$, as indicated on the right of this diagram in $[CartSp^{op}, sSet]$

$$
  \array{
     && \exp(\mathfrak{g}) &\stackrel{\exp(\mu)}{\to}&
     \exp(b^{n-1}\mathbb{R})
     \\
      && \downarrow && \downarrow^{\mathrlap{\int_{\Delta^\bullet}}}
     \\
     C(V) & \stackrel{\hat g}{\to}& \mathbf{cosk}_3 \exp(\mathfrak{g})
     &\stackrel{\int_{\Delta^\bullet}\mathbf{cosk}_3 \exp(\mu)}{\to}&
     \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
     \\
     \downarrow^{\mathrlap{\simeq}}&& \downarrow^{\mathrlap{\simeq}}
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

Precomposing this -- as indicated on the left of the diagram -- with another $\infty$-anafunctor $X \stackrel{\simeq}{\leftarrow}C(U)\stackrel{g}{\to} \mathbf{B}G$ for a $G$-principal bundle , hence a collection of transition functions $\{g_{i j} : U_i \cap U_j \to G\}$ amounts to choosing (possibly on a refinement $V$ of the cover $U$ of $X$)

* on each $V_i \cap V_j$ a lift $\hat g_{i j}$ of $g_{i j}$ to a familly of smooth based paths in $G$  -- $\hat g_{i j} : (V_i \cap V_j) \times \Delta^1 \to G$ -- with endpoints $g_{i j}$;

* on each $V_i \cap V_j \cap V_k$ a smooth family  $\hat g_{i j k} : (V_i \cap V_j \cap V_k) \times \Delta^2 \to G$ of disks interpolating between these paths;

* on each $V_i \cap V_j \cap V_k \cap V_l$ a a smooth family  $\hat g_{i j k l} : (V_i \cap V_j \cap V_k \cap V_l) \times \Delta^3 \to G$ of 3-balls interpolating between these disks.

On this data the morphism $\int_{\Delta^\bullet} \exp(\mu)$ acts by sending each 3-cell to the number

$$
  \hat g_{i j k l} \mapsto \int_{\Delta^3} \hat g_{i j k l}^* \mu
  \;\;  mod \mathbb{Z}
  \,,
$$

where $\mu$ is regarded in this formula as a closed 3-form on $G$.

=--

We say this is <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">Lie integration of Lie algebra cocycles</a>.

+-- {: .num_prop}
###### Proposition

The [[Cech cohomology]] cocycle obtained this way is the first [[Pontryagin class]] of the $G$-bundle classified by $G$.

=--

We shall show this below, as part of our $L_\infty$-algebraic reconstruction of the [above motivating example](#BMConstruction). In order to do so, we now add differential refinement to this Lie integration of characteristic classes.



### $L_\infty$-algebra valued connections {#LieConnections}

[Above](#LowDimension) we described ordinary [[connections on bundles]] as well as [[connections on 2-bundles]] in terms of [[parallel transport]] over paths and surfaces, and showed how such is equivalently given by cocycles with coefficients in [[Lie-algebra valued differential forms]] and [[Lie 2-algebra valued differential forms]], respectively. 

Notably we saw ([here](#CurvatureCharacteristicsI)) for the case of ordinary $U(1)$-[[principal bundle]]s, that the connection and curvature data on these is encoded in presheaves of diagrams that over a given test space $U \in $ [[CartSp]] look like

$$  
  \array{
    U &\to& \mathbf{B}U(1) &&& transition\;function
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{\Pi}(U) &\to& \mathbf{B}INN(U) &&& connection
    \\
    \downarrow &&  \downarrow
    \\
    \mathbf{\Pi}(U) &\to& \mathbf{B}^2 U(1) &&& curvature
  }
$$

together with a constraint on the bottom morphism.

It is in the form of such a kind of diagram that the general notion of [[connections on ∞-bundles]] may be modeled. In the full theory of [[schreiber:differential cohomology in a cohesive topos]] this follows from first principles, but for our present introductory purpose we shall be content with taking this simple situation of $U(1)$-bundles together with the notion of [[Lie integration]] as sufficient motivation for the constructions considered now. 

So we pass now to what is to some extent the reverse construction of the one considered before: we define a notion of [[∞-Lie algebra valued differential forms]] and show how by a variant of [[Lie integration]] these integrate to coefficient objects for [[connections on ∞-bundles]].


In the main entry [[∞-Chern-Weil theory]] we discuss how this dg-algebraic construction follows from a general abstract definitions of [[schreiber:differential cohomology in a cohesive topos]].

The material of this section is due to ([SSSI](#SSSI)) and ([FSS](#FSS)).




#### Curvature characteristics and Chern-Simons forms 
  {#CurvCharAndCS}

For $G$ a Lie group, we have described [above](#ConnectionOnPrincipalBundle) connections on $G$-principal bundles in terms of cocycles with coefficients in the Lie-[[groupoid of Lie-algebra valued forms]] $\mathbf{B}G_{conn}$

$$
  \array{
  && \mathbf{B}G_{conn} &&& connection
  \\
  & {}^{\mathllap{\nabla}}\nearrow & \downarrow
  \\
  && \mathbf{B}G_{diff} &&& pseudo-connection
  \\
  & {}^{\mathllap{\nabla_{ps}}}\nearrow & \downarrow^{\mathrlap{\simeq}} 
  \\
  C(U) &\stackrel{g}{\to}& \mathbf{B}G &&& transition\;function
  \\
   \downarrow^{\mathrlap{\simeq}}
  \\
  X
  }
  \,.
$$

In this context we had _derived_ Lie algebra valued forms from the [[parallel transport]] description $\mathbf{B}G_{conn} = [\mathbf{P}_1(-), \mathbf{B}G]$. We now turn this around and use [[Lie integration]] to construct parallel transport from Lie-algebra valued forms. The construction is such that it generalizes verbatim to [[∞-Lie algebra valued forms]].

For that purpose notice that another classical dg-algebra associated with $\mathfrak{g}$ is its [[Weil algebra]] $W(\mathfrak{g})$. 

+-- {: .num_lemma}
###### Fact

The [[Weil algebra]] $\mathrm{W}(\mathfrak{g})$ 
is the free dg-algebra on the graded vector space $\mathfrak{g}^*$, meaning that there is a [[natural isomorphism]] 

$$
  \mathrm{Hom}_{\mathrm{dgAlg}}(W(\mathfrak{g}), A) \simeq \mathrm{Hom}_{\mathrm{Vect}_{\mathbb{Z}}}(\mathfrak{g}^*, A)
  \,,
$$

which is singled out among the isomorphism class of dg-algebras with this property by the
fact that the projection of [[graded vector space]]s $\mathfrak{g}^* \oplus \mathfrak{g}^*[1] \to \mathfrak{g}^*$
extends to a [[dg-algebra]] homomorphism 

$$
  CE(\mathfrak{g}) \leftarrow W(\mathfrak{g}) : i^*
  \,.
$$

=--

(Notice that general the dg-algebras that we are dealing with are [[semi-free dga]]s in that only their underlying [[graded algebra]] is free, but not the differential). 

The most obvious realization of the free dg-algebra on $\mathfrak{g}^*$ is $\wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])$ equipped with the differential that is precisely the degree shift isomorphism $\sigma : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ extended as a [[derivation]]. This is not the Weil algebra on the nose, but is of course isomorphic to it. The differential of the Weil algebra on $\wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])$ is given on the unshifted generators by the sum of the CE-differential with the shift isomorphism

$$
  d_{W(\mathfrak{g})}|_{\mathfrak{g}^*} = d_{CE(\mathfrak{g})} + \sigma
  \,.
$$

This uniquely fixes the differential on the shifted generators -- a phenomenon known (at least after mapping this to differential forms, as we discuss below) as the [[Bianchi identity]].

Using this, we can express also the presheaf $\mathbf{B}G_{diff}$ from def \ref{BGdiff} in diagrammatic fashion.

+-- {: .num_lemma}
###### Observation

For $G$ a [[simply connected]] [[Lie group]], the presheaf $\mathbf{B}G_{diff} \in [CartSp^{op}, Grpd]$ is isomorphic to

$$
  \mathbf{B}G_{diff}  =
  \tau_1
  \left(
  \exp(\mathfrak{g})_{diff}
   :
   (U,[k]) \mapsto 
    \left\{ 
      \array{
        \Omega^\bullet_{vert}(U \times \Delta^k) 
        &\stackrel{A_{vert}}{\leftarrow}&
        CE(\mathfrak{g})
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet(U \times \Delta^k)
        &\stackrel{A}{\leftarrow}&
        W(\mathfrak{g})
      }
    \right\} 
    \right)
  \,
$$

where on the right we have the 1-truncation of the simplicial presheaf of diagrams as indicated, where the vertical morphisms are the canonical ones.

=--

Here over a given $U$ the bottom morphism in such a diagram is an arbitrary $\mathfrak{g}$-valued 1-form $A$ on $U \times \Delta^k$. This we can decompose as $A = A_U + A_{vert}$, where $A_U$ vanishes on tangents to $\Delta^k$ and $A_{vert}$ on tangents to $U$. The commutativity of the diagram asserts that $A_{vert}$ has to be such that the  curvature 2-form $F_{A_{vert}}$ vanishes when both its arguments are tangent to $\Delta^k$.

On the other hand, there is in the above no further constraint on $A_U$. Accordingly, as we pass to the 1-truncation of $\exp(\mathfrak{g})_{diff}$ we find that morphisms are of the form $(A_U)_1 \stackrel{g}{\to} (A_U)_2$ with $(A_U)^i$ arbitrary. This is the definition of $\mathbf{B}G_{diff}$.


+-- {: .num_remark}
###### Remark

We see below that it is not a coincidence that this is reminiscent 
to the first condition on an [[Ehresmann connection]] on a $G$-principal bundle, which asserts that restricted to the fibers a connection 1-form on the total space of the bundle has to be flat. Indeed, the simplicial presheaf $\mathbf{B}G_{diff}$ may be thought of as the $(\infty,1)$-sheaf of pseudo-connections on _trivial_ $\infty$-bundles. Imposing on this also the second Ehresmann condition will force the pseudo-connection to be a genuine connection.

=--


We now want to lift the [above](#LieIntOfCocycles) construction $\exp(\mu)$ of [[characteristic class]]es by <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">Lie integration of Lie algebra cocycles</a> $\mu$ from plain bundles classified by $\mathbf{B}G$ to bundles with (pseudo-)connection classified by $\mathbf{B}G_{diff}$. By what we just said we therefore need to extend $\exp(\mu)$ from a map on just $\exp(\mathfrak{g})$ to a map on $\exp(\mathfrak{g})_{diff}$.

This is evidently achieved by completing a square in [[dgAlg]] of the form

$$
  \array{
    CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{n-1} \mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}& W(b^{n-1} \mathbb{R})
  }
$$

and defining $\exp(\mu)_{diff} : \exp(\mathfrak{g})_{diff} \to \exp(b^{n-1}\mathbb{R})_{diff}$ to be the operation of forming [[pasting]] composites with this.

Here $W(b^{n-1}\mathbb{R})$ is the Weil algebra of the 
[[infinity-Lie-algebra|Lie n-algebra]] $b^{n-1} \mathbb{R}$. This is the dg-algebra on two generators $c$ and $k$, respectively, in degree $n$ and $(n+1)$ with the differential given by $d_{W(b^{n-1} \mathbb{R})} : c \mapsto k$.

The commutativity of this diagram says that the bottom morphism takes the degree-$n$ generator $c$ to an element $cs \in W(\mathfrak{g})$ whose restriction to the unshifted generators is the given cocycle $\mu$. 


As we shall see below, any such choice $cs$ will extend the characteristic cocycle obtained from $\exp(\mu)$ to a characteristic differential cocycle, exhibiting the $\infty$-Chern-Weil homomorphism. But only for special nice choices of $cs$ will this take genuine $\infty$-connections to genuine $\infty$-connections -- instead of to [[pseudo-connection]]s. As we discuss in the full [[∞-Chern-Weil theory]], this makes no difference in cohomology. But in practice it is useful to fine-tune the construction such as to produce nice models of the $\infty$-Chern-Weil homomorphism given by genuine $\infty$-connections. 

This is achieved by imposing the following additional constraint on the choice of extension $cs$ of $\mu$: 

+-- {: .num_defn}
###### Definition

For $\mu \in CE(\mathfrak{g})$ a cocycle and $cs \in W(\mathfrak{g})$ a lift of $\mu$ through $W(\mathfrak{g}) \leftarrow CE(\mathfrak{g})$, we say that $\langle -\rangle \in W(\mathfrak{g})$ is an [[invariant polynomial]] _in transgression_ with $\mu$ if 

* both $\langle -\rangle$ as well as $d_{W(\mathfrak{g})}\langle - \rangle$ sit entirely in the shifted generators, in that $\in \wedge^\bullet \mathfrak{g}^*[1] \hookrightarrow W(\mathfrak{g})$.

=--

+-- {: .num_prop}
###### Proposition

For $\mathfrak{g}$ a [[Lie algebra]], this definition of invariant polynomials is equivalent to the traditional one.

=--

To see this explicitly, let $\{t^a\}$ be a basis of $\mathfrak{g}^*$ and $\{r^a\}$ the corresponding basis of $\mathfrak{g}^*[1]$. Write $\{C^a{}_{b c}\}$ for the structure constants of the Lie bracket in this basis. 

Then for $P = P_{(a_1 , \cdots , a_k)} r^{a_1} \wedge \cdots \wedge r^{a_k} \in \wedge^{r} \mathfrak{g}^*[1]$ an element in the shifted generators, the condition that it is $d_{W(\mathfrak{g})}$-closed is equivalent to

$$
  C^{b}_{c (a_1} P_{b, \cdots, a_k)} t^c \wedge r^{a_1} \wedge \cdots \wedge r^{a_k}
  \,,
$$

where the parentheses around indices denotes symmetrization, as usual, so that this is equivalent to

$$
  \sum_{i} C^{b}_{c (a_i} P_{a_1 \cdots a_{i-1} b a_{i+1} \cdots, a_k)}
  = 0
$$ 


for all choices of indices. This is the component-version of the familiar invariance statement 

$$
  \sum_i P(t_1, \cdots, t_{i-1}, [t_c, t_i], t_{i+1}, \cdots , t_k)
  = 0
$$

for all $t_\bullet \in  \mathfrak{g}$.

+-- {: .num_defn}
###### Definition


Write $inv(\mathfrak{g}) \subset W(\mathfrak{g})$ (or $W(\mathfrak{g})_{basic}$) for the sub-dgalgebra on invariant polynomials.

=--

+-- {: .num_prop}
###### Observation

We have $W(b^{n-1}\mathbb{R}) \simeq CE(b^n \mathbb{R})$.

=--

Using this, we can now encode the two conditions on the extension $cs$ of the cocycle $\mu$ as the commutativity of this double square diagram

$$
  \array{
    CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{n-1} \mathbb{R})
    &&& cocycle
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}& W(b^{n-1} \mathbb{R})
    &&& Chern-Simons\;element
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{g})
   &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(b^{n-1} \mathbb{R}) 
    &&& 
    invariant\;polynomial
  }
  \,.
$$

+-- {: .num_defn}
###### Definition 

In such a diagram, we call $cs$ the **[[Chern-Simons element]]** that exhibits the transgression between $\mu$ and $\langle - \rangle$. 

=--

We shall see below that under the $\infty$-Chern-Weil homomorphism, Chern-Simons elements give rise to the familiar [[Chern-Simons form]]s -- as well as their generalizations -- as local connection data of [[secondary characteristic class]]es realized as [[circle n-bundles with connection]]. 

+-- {: .num_note}
###### Observation

What this diagram encodes is the construction of the [[connecting homomorphism]] for the [[fiber sequence|long exact sequence in cohomology]] that is induced from the short exact sequence

$$
  ker(i^*) \to W(\mathfrak{g}) \to CE(\mathfrak{g})
$$

subject to the extra constraint of basic elements.

$$
  \array{
     && \langle - \rangle &\leftarrow& \langle - \rangle
     \\
     && \uparrow^{\mathrlap{d_{W}}}
     \\
     \mu &\leftarrow& cs
     \\
     \\
     \\
     CE(\mathfrak{g}) &\leftarrow& W(\mathfrak{g})
     &\leftarrow&
     inv(\mathfrak{g})
  }
  \,.
$$



=--

To appreciate the construction so far, recall the

+-- {: .num_prop}
###### Classical fact

For $G$ a [[compact space|compact]] [[Lie group]], the [[rationalization]] $\mathbf{B}G \otimes k$ of the [[classifying space]] $\mathbf{B}G$ is the [[rational space]] whose [[Sullivan model]] is given by the algebra $inv(\mathfrak{g})$ of [[invariant polynomial]]s on the [[Lie algebra]] $\mathfrak{g}$.

=--

This means that we may think of the consztructons so far in terms of the following picture:

$$
  \array{
    delooped\; \infty-group
    &&&
    \mathbf{B}G && \mathfrak{g} && 
    CE(\mathfrak{g}) &&& Chevalley-Eilenberg\;algebra
    \\
    &&& \downarrow && \downarrow && \uparrow 
    \\
    delooped\;groupal\;universal\;\infty-bundle
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


+-- {: .num_example}
###### Examples

* For $\mathfrak{g}$ a [[semisimple Lie algebra]], $\langle -,-\rangle$ the [[Killing form]] invariant polynomial, there is a Chern-Simons element $cs \in W(\mathfrak{g})$ witnessing the transgression to the cocycle $\mu = - \frac{1}{6} \langle -,[-,-] \rangle$. Under a $\mathfrak{g}$-valued form $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : A$ this maps to the ordinary degree 3 [[Chern-Simons form]]

  $$ 
    cs(A) = \langle A \wedge d A\rangle + \frac{1}{3} \langle A \wedge [A \wedge A]\rangle
    \,.
  $$

=--


#### $\infty$-Connections from Lie integration 
 {#LieIntConn}

We have seen above for $\mathfrak{g}$ an $\infty$-Lie algebroid the object
$\exp(\mathfrak{g})_{diff}$ that classifies [[pseudo-connection]]s
on $\exp(\mathfrak{g})$-principal $\infty$-bundles and serves to support the $\infty$-Chern-Weil homomorphism. We now discuss the genuine [[connection on an ∞-bundle|∞-connections]] among these pseudo-connections. From the point of view of the general abstract theory these are particularly nice representatives of more intrinsically defined structures. 

For $X$ a [[smooth manifold]] and $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally an [[∞-Lie algebroid]], a  **$\infty$-Lie algebroid valued differential form** on $X$ is a morphism of [[dg-algebra]]s

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

from the [[Weil algebra]] of $\mathfrak{g}$ to the [[de Rham complex]] of $X$. Dually this is a morphism of [[∞-Lie algebroid]]s

$$
  A : T X \to inn(\mathfrak{g})
$$

from the [[tangent Lie algebroid]] to the [[Weil algebra|inner automorphism ∞-Lie algebra]].

Its [[curvature]] is the composite of morphisms of [[graded vector space]]s

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \mathfrak{g}^*[1]
  : 
  F_{A}
  \,.
$$

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] 

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
$$

in which case we call $A$ **flat**.

The [[curvature characteristic form]]s of $A$ are the composite

$$
  \Omega^\bullet(X)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{\langle F_{(-)} \rangle}{\leftarrow}
  inv(\mathfrak{g})
  :
  \langle F_A\rangle
  \,,
$$

where $inv(\mathfrak{g}) \to W(\mathfrak{g})$ is the inclusion of the [[invariant polynomial]]s. 


+-- {: .num_defn}
###### Definition

For $U$ a [[smooth manifold]], the **$\infty$-groupoid of $\mathfrak{g}$-valued forms (see [[∞-groupoid of ∞-Lie-algebra valued forms]]) is the [[Kan complex]]

$$
  \exp(\mathfrak{g})_{conn}(U)
  :
  [k]
  \mapsto
  \left\{
     \Omega^\bullet(U \times \Delta^k)
      \stackrel{A}{\leftarrow}
     W(\mathfrak{g})
     \;\;
     |
     \;\;
       \forall v \in \Gamma(T \Delta^k) : \iota_v F_A = 0
  \right\}
$$


whose [[k-morphism]]s are $\mathfrak{g}$-valued forms $A$ on $U \times \Delta^k$ with sitting instants, and with the property that their [[curvature]] vanishes on vertical vectors.

The canonical morphism

$$
  \exp(\mathfrak{g})_{conn} \to \exp(\mathfrak{g})
$$

to the untruncated [[Lie integration]] of $\mathfrak{g}$ is given by restriction of $A$ to [[vertical differential form]]s (see below).

=--

+-- {: .num_remark}
###### Remark

Here we are thinking of $U \times \Delta^k \to U$ as a trivial [[bundle]].

The _first_ [[Ehresmann connection|Ehresmann condition]] 
can be identified with the conditions on lifts $\nabla$ in [[∞-anafunctor]]s

$$
  \array{
    && \exp(\mathfrak{g})_{conn}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \exp(\mathfrak{g})
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

that define [[connections on ∞-bundles]]. 

=--


##### Curvature characteristics

+-- {: .num_prop}
###### Proposition

For $A \in \exp(\mathfrak{g})_{conn}(U,[k])$ a $\mathfrak{g}$-valued form on $U \times \Delta^k$ and for $\langle - \rangle \in W(\mathfrak{g})$ any [[invariant polynomial]], the corresponding [[curvature characteristic form]] $\langle F_A \rangle \in \Omega^\bullet(U \times \Delta^k)$ descends down to $U$.

=--

+-- {: .proof}
###### Proof

It is sufficient to show that for all $v \in \Gamma(T \Delta^k)$ we have

1. $\iota_v \langle F_A \rangle = 0$;

1. $\mathcal{L}_v \langle F_A \rangle = 0$.

The first condition is evidently satisfied if already $\iota_v F_A = 0$. The second condition follows with [[Cartan calculus]] and using that $d_{dR} \langle F_A\rangle = 0$:

$$
  \mathcal{L}_v \langle F_A \rangle = 
  d \iota_v \langle F_A \rangle
  + 
  \iota_v d \langle F_A \rangle
  = 0
  \,.
$$

=--

+-- {: .num_lemma}
###### Remark

For a general $\infty$-Lie algebra $\mathfrak{g}$ the curvature forms $F_A$ themselves are not necessarily closed (rather they satisfy the [[Bianchi identity]]), hence requiring them to have no component along the simplex does not imply that they descend. This is different for abelian $\infty$-Lie algebras: for them the curvature forms themselves are already closed, and hence are themselves already curvature characteristics that do descent.

=--


It is useful to organize the $\mathfrak{g}$-valued form $A$, together with its restriction $A_{vert}$ to [[vertical differential form]]s and with its [[curvature characteristic form]]s in the [[commuting diagram]]

$$
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      &&&
      \mathfrak{g}-valued\;form
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      curvature\;characteristic\;forms
    }
$$

in [[dgAlg]].

The commutativity of this diagram is implied by $\iota_v F_A = 0$.

+-- {: .num_defn}
###### Definition

Write $\exp(\mathfrak{g})_{CW}(U)$ for the $\infty$-groupoid of $\mathfrak{g}$-valued forms fitting into such diagrams.


$$
  \exp(\mathfrak{g})_{CW}(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
    }
  \right\}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

If we just consider the top horizontal morphism in this diagram we obtain the object

$$
  \exp(\mathfrak{g})(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
     }
  \right\}
$$

discussed in detail at [[Lie integration]]. If we consider the top square of the diagram we obtain the object

$$
  \exp(\mathfrak{g})_{diff}(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
   }
  \right\}
  \,.
$$

This forms a [[resolution]] of $\exp(\mathfrak{g})$ and may be thought of as the $\infty$-groupoid of [[pseudo-connection]]s.


We have an evident sequence of morphisms

$$
  \array{
    \exp(\mathfrak{g})_{conn} &&& genuine\;connections
    \\
    \downarrow
    \\
    \exp(\mathfrak{g})_{CW} &&& pseudo-connection\;with\;global\;curvature\;characteristics 
    \\
    \downarrow
    \\
    \exp(\mathfrak{g})_{diff} &&& pseudo-connections
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g}) &&& bar\,bundles
  }
  \,,
$$

where we label the objects by the structures they classify, as discussed at [[∞-Chern-Weil theory]].


Here the botton morphism is a weak equivalence and the others are [[monomorphism]]s. 

Notice that in full [[∞-Chern-Weil theory]] the fundamental object of interest is really $\exp(\mathfrak{g})_{diff}$ -- the object of [[pseudo-connection]]s. The other objects only serve the purpose of picking particularly nice representatives: 

the object $\exp(\mathfrak{g})_{CW}$ may contain pseudo-connections, those for which at least the associated [[circle n-bundles with connection]] given by the $\infty$-Chern Weil homomorphism are genuine connections.

This distinction is important: over objects $X \in $ [[Smooth∞Grpd]] that are not [[smooth manifold]]s but for instance [[orbifold]]s, the genuine connections for higher Lie algebras do _not_ exhaust all nonabelian differential cocycles. This just means that not every differential class in this case does have a nice representative in the usual sense.

=--



##### 1-Morphisms: integration of infinitesimal gauge transformations   
 {#InfGaugeTrafo}

The 1-[[morphism]]s in $\exp(\mathfrak{g})(U)$ may be thought of as [[gauge transformation]]s between $\mathfrak{g}$-valued forms. We unwind what these look like concretely.


+-- {: .num_defn}
###### Definition

Given a 1-morphism in $\exp(\mathfrak{g})(X)$, represented by $\mathfrak{g}$-valued forms

$$
  \Omega^\bullet(U \times \Delta^1) 
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

consider the unique decomposition

$$
  A = A_U + ( A_{vert} := \lambda \wedge d t)  \; \; 
  \,,
$$

with $A_U$ the horizonal differential form component and $t : \Delta^1 = [0,1] \to \mathbb{R}$ the canonical coordinate.

We call $\lambda$ the **gauge parameter** . This is a function on $\Delta^1$ with values in 0-forms on $U$ for $\mathfrak{g}$ an ordinary [[Lie algebra]], plus 1-forms on $U$ for $\mathfrak{g}$ a [[Lie 2-algebra]], plus 2-forms for a Lie 3-algebra, and so forth.

=--

We describe now how this enccodes a gauge transformation

$$
  A_0(s=0) \stackrel{\lambda}{\to} A_U(s = 1)
  \,.
$$

+-- {: .num_lemma}
###### Observation


By the nature of the [[Weil algebra]] we have

$$
  \frac{d}{d s} A_U
  =
  d_U \lambda + [\lambda \wedge A] + [\lambda \wedge A \wedge A] + \cdots
  + 
  \iota_s F_A
  \,,
$$

where the sum is over all higher brackets of the [[∞-Lie algebra]] $\mathfrak{g}$.

=--

In the [[Cartan calculus]] for $\mathfrak{g}$ an ordinary 
[[Lie algebra]] one writes the corresponding  **[[Ehresmann connection|second Ehremsnn condition]]** $\iota_{\partial_s} F_A = 0$ equivalently

$$
  \mathcal{L}_{\partial_s} A = ad_\lambda A
  \,.
$$


+-- {: .num_defn}
###### Definition

Define the **[[covariant derivative]] of the gauge parameter** to be

$$
  \nabla \lambda := d \lambda + [A \wedge \lambda] + [A \wedge A \wedge \lambda] + \cdots
  \,.
$$

=--

In this notation we have

* the general identity 

  \[
    \frac{d}{d s} A_U = \nabla \lambda + (F_A)_s
    \label{ShiftedGaugeTrafo}
  \]

* the **horizontality** or **[[rheonomy]]** constraint or **[[Ehresmann connection|second Ehresmann condition]]** $\iota_{\partial_s} F_A = 0$, the [[differential equation]]

  \[
    \frac{d}{d s} A_U = \nabla \lambda
    \label{GaugeTrafo}
    \,.
  \]

This is known as the equation for **infinitesimal [[gauge transformation]]s** of an $\infty$-Lie algebra valued form. 



+-- {: .num_lemma}
###### Observation

By [[Lie integration]] we have that $A_{vert}$ -- and hence $\lambda$ -- defines an element $\exp(\lambda)$ in the [[∞-Lie group]] that integrates $\mathfrak{g}$. 

The unique solution $A_U(s = 1)$ of the above [[differential equation]] at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformation $\exp(\lambda)$. 

=--



##### Examples


+-- {: .num_prop}
###### Proposition
**(connections on ordinary bundles)**

For $\mathfrak{g}$ an ordinary [[Lie algebra]] with simply connected [[Lie group]] $G$ and for $\mathbf{B}G_{conn}$ the [[groupoid of Lie algebra-valued forms]] we have an [[isomorphism]]

$$
  \tau_1 \exp(\mathfrak{g})_{conn} = \mathbf{B}G_{conn}
$$

=--

+-- {: .proof}
###### Proof

To see this, first note that the sheaves of objects on both sides are manifestly isomorphic, both are the sheaf of $\Omega^1(-,\mathfrak{g})$. For morphisms, observe that for a form $\Omega^\bullet(U \times \Delta^1) \leftarrow W(\mathfrak{g}) : A$ which we may decompose into a horizontal and a verical pice as $A = A_U + \lambda \wedge d t$ the condition $\iota_{\partial_t} F_A = 0$ is equivalent to the [[differential equation]]

$$
  \frac{\partial}{\partial t} A
  =
  d_U \lambda + [\lambda, A]
  \,.
$$

For any initial value $A(0)$ this has the unique solution

$$
  A(t) = g(t)^{-1} (A + d_{U}) g(t)
  \,,
$$

where $g : [0,1] \to G$ is the [[parallel transport]] of $\lambda$:

$$
  \begin{aligned}
    &
    \frac{\partial}{\partial t}
    \left(
       g_(t)^{-1} (A + d_{U}) g(t)
     \right)
     \\
     = &
     g(t)^{-1} (A + d_{U}) \lambda g(t)
     -
     g(t)^{-1} \lambda (A + d_{U}) g(t)    
   \end{aligned}
$$

(where for ease of notaton we write actions as if $G$ were a [[matrix Lie group]]).

In particular this implies that the endpoints of the path of $\mathfrak{g}$-valued 1-forms are related by the usual cocycle condition in $\mathbf{B}G_{conn}$

$$
  A(1) = g(1)^{-1} (A + d_U) g(1)
  \,.
$$

In the same fashion one sees that given 2-cell in $\exp(\mathfrak{g})(U)$ and any 1-form on $U$ at one vertex, there is a unique lift to a 2-cell in $\exp(\mathfrak{g})_{conn}$, obtained by parallel transporting the form around. The claim then follows from the previous statement of [[Lie integration]] that $\tau_1 \exp(\mathfrak{g}) = \mathbf{B}G$.

=--


* For $\mathfrak{g}$ [[Lie 2-algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an [[Lie 2-algebra valued form]].


* For $n \in \mathbb{N}$, a $b^{n-1}\mathbb{R}$-valued differential form is the same as an ordinary differential $n$-form.


* What is called an  "extended soft group manifold" in the literature on the [[D'Auria-Fre formulation of supergravity]] is precisely a collection of $\infty$-Lie algebroid valued forms with values in a super $\infty$-Lie algebra such as the 
[[supergravity Lie 3-algebra]]/[[supergravity Lie 6-algebra]] (for 11-dimensional [[supergravity]]). The way [[curvature]] and [[Bianchi identity]] are read off from "extded soft group manifolds" in this literature is -- apart from this difference in terminology -- precisely what is described above. 


### Differential characteristic classes from Lie integration
 {#DiffClassesFromLie}

We have now the ingredients in hand to produce a construction of 
differential characteristic classes -- the refined [[∞-Chern-Weil homomorphism]] -- in terms of [[Lie integration]] of differential refinements of $L_\infty$-algebra cocycles. 

We first consider the _local_ construction that produces the de Rham cohomology data of the differential characteristic classes. Since this turns out to be a generalization of the construction of the [[action functional]] of [[Chern-Simons theory]], we speak of

* [∞-Chern-Simons functionals](#CSFunctionals)

Applying a [[coskeleton]]-truncation to this construction carves out the [[period]] [[lattice]] of the $L_\infty$-algebra cocycle inside the line $\mathbb{R}$, which yields to the fully-fledged differential characteristic classes, typically called [[secondary characteristic classes]]

* [Secondary characteristic classes from Lie integration](#DifferentialCharacteristic)

In full [[∞-Chern-Weil theory]] the $\infty$-Chern-Weil homomorphism is conceptually very simple: for every $n$ there is canonically a morphism of [[∞-Lie groupoid]]s $\mathbf{B}^n U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)$ where the object on the right classifies ordinary [[de Rham cohomology]] in degree $n+1$. For $G$ any [[∞-group]] and any [[characteristic class]] $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^{n+1}U(1)$, the $\infty$-Chern-Weil homomorphism is the operation that takes a $G$-[[principal ∞-bundle]] $X \to \mathbf{B}G$ to the composite $X \to \mathbf{B}G \to \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$.

All the construction that we consider here in this introduction serve to _present_ this abstract operation. The $\infty$-connections that we considered yield [[resolution]]s of $\mathbf{B}^n U(1)$ and $\mathbf{B}G$ in terms of which the abstract morphisms are modeled as [[∞-anafunctor]]s.



#### $\infty$-Chern-Simons functionals
 {#CSFunctionals}

We have considered above [[connection on an ∞-bundle|∞-connections]] in terms of [[dg-algebra]] homomorphisms and [[Chern-Simons element]]s witnessing the transgression of cocycles to invariant polynomials in terms of dg-algebra homomorphisms. There is an evident way to compose these two constructions.

+-- {: .num_defn}
###### Definition

Let $\mathfrak{g}$ be an [[L-∞ algebra]] and $\mu : \mathfrak{g} \to b^{n-1}\mathbb{R}$ a cocycle in its [[L-∞ algebra cohomology]], which transgresses to an [[invariant polynomial]] $\langle -\rangle$, witnessed by a [[Chern-Simons element]] $cs$.

Then let 

$$
  \exp(\mu,cs) : \exp(\mathfrak{g})_{conn} \to \exp(b^{n-1}\mathbb{R})_{conn} 
$$

be the morphism of [[simplicial presheaves]] obtained by forming [[pasting]] composites of the defining diagrams in [[dgAlg]] of these structures:

over $U \in CartSp$ and $[k] \in \Delta$ the morphism $\exp(\mu,cs)$ sends an element 
$A \in \exp(\mathfrak{g})_{conn}(U)_k$ to the element 
$cs(A) \in \exp(b^{n-1}\mathbb{R})_{conn}$ given explicitly as follows

$$
  \left(
  \array{
     \Omega^\bullet_{vert}(U \times \Delta^k)
     &\stackrel{A_{vert}}{\leftarrow}&
     CE(\mathfrak{g})
     &&&
     transition\;function\;/\;Cech\;cocycle
     \\
     \uparrow && \uparrow 
     \\
     \Omega^\bullet(U \times \Delta^{k})
     &\stackrel{A}{\leftarrow}&
     W(\mathfrak{g})
     &&& 
     connection
     \\
     \uparrow && \uparrow 
     \\
     \Omega^\bullet(U)
     &\stackrel{\langle F_A\rangle}{\leftarrow}&
     inv(\mathfrak{g})
     &&&
     curvature\;characteristics
  }
  \right)
  \circ
  \left(
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
     CE(b^{n-1} \mathbb{R})
     &&&
     cocycle
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}&
     W(b^{n-1} \mathbb{R})
     &&&
     Chern-Simons\;element
     \\
     \uparrow && \uparrow
     \\
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle}{\leftarrow}&
     inv(b^{n-1} \mathbb{R}) 
     &&&
     invariant\;polynomial
  }
  \right)
$$

$$
  = 
  \;
  \;
  \;
  \left(
  \array{
     \Omega^\bullet(U \times \Delta^k)_{vert}
     &\stackrel{A_{vert}}{\leftarrow}&
     CE(\mathfrak{g})
     &\stackrel{\mu}{\leftarrow}&
     CE(b^{n-1} \mathbb{R})
     & : \mu(A_{vert})
     &&&
     characteristic\;class
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U \times \Delta^k)
     &\stackrel{A}{\leftarrow}&
     W(\mathfrak{g})
     &\stackrel{cs}{\leftarrow}&
     W(b^{n-1} \mathbb{R})
     &
     : cs(A)
     &&&
     Chern-Simons\;form
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U)
     &\stackrel{\langle F_A\rangle}{\leftarrow}&
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle}{\leftarrow}&
     inv(b^{n-1} \mathbb{R})
     &
     : \langle F_A\rangle
     &&&
     curvature\;characteristic\;form
  }
  \right)
  \,.
$$

By restriction to the top two layers of these diagrams this analogously yields a morphism

$$
  \exp(\mu, cs): \exp(\mathfrak{g})_{diff} \to \exp(b^{n-1}\mathbb{R})_{diff} 
  \,.
$$

Analogously, projection onto the third horizontal layer gives amorphism 

$$
  \exp(\mu,cs)
   :
  \exp(b^{n-1}\mathbb{R})_{diff} 
    \to 
  \mathbf{\flat}_{dR}\exp(b^{n} \mathbb{R})_{smp}
  \underoverset{\int_{\Delta^\bullet}}{\simeq}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}_{ch}
$$

to the de Rham coefficient object.


=--


+-- {: .num_note}
###### Note

The morphism $\exp(\mu,cs)$ carries $\mathfrak{g}$-valued connections $\nabla$ locally given by $\mathfrak{g}$-valued forms $A$ to 
$b^{n-1}\mathbb{R}$-valued connections whose [[higher parallel transport]] over an $n$-[[dimension]]al [[smooth manifold]] $\Sigma$ is locally given by the integral $\int_\Sigma cs(A)$ of the [[Chern-Simons form]] $cs(A)$ over $\Sigma$. This assignment $A \mapsto \int_\Sigma cs(A)$ is the [[action functional]] for an [[schreiber:∞-Chern-Simons theory]] defined by the [[invariant polynomial]] $\langle -\rangle \in W(\mathfrak{g})$. Therefore we may regard $\exp(\mu,cs)$ as being the [[Lagrangian]] for this [[∞-Chern-Simons theory]]. 

=--

In total, this construction constitutes an $\infty$-anafunctor

$$
  \array{
    \exp(\mathfrak{g})_{diff}
    &\stackrel{\exp(\mu)_{diff}}{\to}&
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{ch}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g})
  }
  \,.
$$

Postcomposition with this is the simple $\infty$-Chern-Weil homomorphism: it sends a cocycle

$$
  \array{
    C(U) &\to& \exp(\mathfrak{g})
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

for an $\exp(\mathfrak{g})$-[[principal ∞-bundle]] to the [[curvature]] form represented by

$$
  \array{
    C(V)
    &\stackrel{(g,\nabla)}{\to}& \exp(\mathfrak{g})_{diff}
    &\stackrel{\exp(\mu)_{diff}}{\to}&
    \exp(b^{n-1}\mathbb{R})_{diff}
    &\stackrel{}{\to}&
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{ch}
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    C(U) &\stackrel{g}{\to}& \exp(\mathfrak{g})
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
  \,.
$$

+-- {: .num_prop}
###### Proposition

For $\mathfrak{g}$ an ordinary [[Lie algebra]] the image under $\tau_1(-)$ of this diagram constitutes the ordinary [[Chern-Weil homomorphism]] in that:

for $g$ the cocycle for a $G$-principal bundle, any ordinary [[connection on a bundle]] constitutes a lift $(g,\nabla)$ to the tip of the anafunctor and the morphism represented by that is the [[Cech cohomology|Cech]]-[[hypercohomology]] cocycle on $X$ with values in the truncated de Rham complex given by the globally defined curvature characteristic form $\langle F_\nabla \wedge \cdots \wedge F_\nabla\rangle$.


=--

This construction however discards the information in the choice of [[connection on an ∞-bundle|connection]] and in the [[Chern-Simons form]] of this connection. Below we lift this construction to one that produces the full [[secondary characteristic classes]] in [[ordinary differential cohomology]] of the refined $\infty$-Chern-Weil homomorphism.




#### Secondary characteristic classes
 {#DifferentialCharacteristic}

So far we discussed the untruncated coefficient object $\exp(\mathfrak{g})_{conn}$ for $\mathfrak{g}$-valued
[[connection on an infinity-bundle|∞-connections]]. 
The real object of interest is the $k$-[[truncated]] version $\tau_k \exp(\mathfrak{g})_{conn}$ where $k \in \mathbb{N}$ is such that $\tau_k \exp)\mathfrak{g} \simeq \mathbf{B}G$ is the delooping of the $\infty$-Lie group in question. 

Under such a truncation, the integrated $\infty$-Lie algebra cocycle $exp(\mu) : exp(\mathfrak{g}) \to exp(b^{n-1}\mathbb{R})$ will no longer be a simplicial map. Instead, the [[period]]s of $\mu$ will cut out a [[lattice]] $\Gamma$ in $\mathbb{R}$, and $\exp(\mu)$ does descent to the quotient of $\mathbb{R}$ by that lattice

$$
  \exp(\mu) : \tau_k \exp(\mathfrak{g}) \to \mathbf{B}^n \mathbb{R}/\Gamma
  \,.
$$

We now say this again in more detail.

Suppose $\mathfrak{g}$ is such that the $(n+1)$-[[coskeleton]] $\mathbf{cosk}_{n+1} \exp(\mathfrak{g}) \stackrel{\simeq}{\to} \simeq \mathbf{B}G$ for the desired $G$. Then the periods of $\mu$ over $(n+1)$-balls cut out a lattice $\Gamma \subset \mathbb{R}$ and thus we get an [[∞-anafunctor]]

$$
  \array{
    \mathbf{cosk}_{n+1} \exp(\mathfrak{g})_{diff}
    &\to&
    \mathbf{B}^{n}\mathbb{R}/\Gamma_{diff}
    &\to&
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}/\Gamma
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G
  }
$$

This is [[curvature characteristic class]]. We may always restrict to genuine $\infty$-connections and refine

$$
  \array{
    \mathbf{cosk}_{n+1} \exp(\mathfrak{g})_{conn}
    &\to&
    \mathbf{B}^{n}\mathbb{R}/\Gamma_{conn}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_{n+1} \exp(\mathfrak{g})_{diff}
    &\to&
    \mathbf{B}^{n}\mathbb{R}/\Gamma_{diff}
    &\to&
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}/\Gamma
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
$$

which models the refined $\infty$-Chern-Weil homomorphism with values in [[ordinary differential cohomology]]

$$
  \mathbf{H}_{conn}(X,\mathbf{B}G)
  \to 
  \mathbf{H}_{conn}(X, \mathbf{B}^{n+1} \mathbb{R}/\Gamma)
$$


We can now reproduce our [motivating example](#BMConstruction) of the Brylinski-McLaughlin construction of the the differential refinement of the first fractional Pontryagin class as a special case of the presentation of the $\infty$-Chern-Weil homomorphism by Lie integrated simplicial presheaves.

+-- {: .num_prop #ReproducingBrylinskiMacLaughlin}
###### Proposition

Let $\mathfrak{g} = \mathfrak{so}(n)$ be the [[special orthogonal Lie algebra]], $\mu = \langle -,[-,-]\rangle$ the canonical [[Lie algebra cohomology]] 3-cocycle and $cs \in W(\mathfrak{g})$ the standard [[Chern-Simons element]] witnessing the transgression to the [[Killing form]] [[invariant polynomial]]. 

Then for $X$ any [[smooth manifold]], the [[Lie integration]] of $(\mu,cs)$ presents a morphism morphism

$$
  \exp(\mu) \mathbf{H}_{conn}(X, \mathbf{B}Spin(n)) \to 
   \mathbf{H}_{conn}(X, \mathbf{B}^3 U(1)) 
$$

that sends $Spin$-principal bundles with connection to their [[Chern-Simons circle 3-bundle]] with connection and as such represents a differential refinement of the first fractional Pontryagin class

$$
  \exp(\mu,cs) = \frac{1}{2}\hat \mathbf{p}_1
  \,.
$$

Moreover, the defining presentation on simplicial presheaves of $\exp(\mu,cs)$ given by the $\infty$-anafunctor

$$
  \array{
    && \exp(\mathfrak{g})_{diff} &\stackrel{\exp(\mu)_{diff}}{\to}& \exp(b^{n-1}\mathbb{R})_{diff}
    \\
    && \downarrow && \downarrow^{\mathrlap{\int_{\Delta^\bullet}}}
    \\
    C(V) &\stackrel{(\hat g,\hat \nabla)}{\to}& \mathbf{cosk}_3\exp(\mathfrak{g})_{diff} 
    &\to&
    \mathbf{B}^3 U(1)_{diff}
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow
    \\
    C(U) &\stackrel{(g,\nabla)}{\to}& \mathbf{B}G_{diff}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

exhibits exactly the Brylinski-MacLaughlin algorithm for constructing Cech-cocycle representatives for this class.

=--

This is due to (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#FSSIII">FSS</a>)


By feeding in more general transgressive 
[[∞-Lie algebra cohomology|∞-Lie algebra cocycles]] through this
machine, we obtain cocycles for more general differential characteristic classes. For
instance the next one is the second fractional Pontryagin class of smooth [[string 2-group|String]]
[[connection on a 2-bundle|principal 2-bundles with connection]] 
(<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#FSSIII">FSS</a>).
Moreover, these constructions naturally yield the full cocycle
$\infty$-groupoids, not just their cohomology sets. This 
allows to form the [[homotopy fiber]]s of the $\infty$-Chern-Weil
homomorphism and thus define [[differential string structure]]s
etc., and _[[twisted cohomology|twisted]]_ differential string structures etc.
(<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>).

## Summary

This section gives a concise summary of the constructions introduced above.


### For connections on $G$-principal 1-bundles

We have the following [[diffeological n-groupoid|diffeological 1- or 2-groupoids]].

* $\mathbf{\Pi}_1(X)$ -- the [[fundamental groupoid]] of $X$ (morphisms are [[homotopy]]-classes of paths);

* $\mathbf{P}_1(X)$ -- the [[path groupoid]] of $X$ (morphisms are [[thin homotopy]]-classes of paths)

* $\mathbf{P}_2(X)$ the [[path 2-groupoid]] (2-morphisms are [[thin homotopy]]-classes of disks).

* $\mathbf{\Pi}_2(X)$ the [[path n-groupoid|fundamental path 2-groupoid]] (2-morphisms are [[homotopy]]-classes of disks).

Let $G$ be a [[Lie group]]. We have the following Lie groupoids associated with that

* $\mathbf{B}G$ -- the coefficient for $G$-[[principal bundle]]s;

* $INN(G) = G//G$ -- the [[inner automorphism 2-group]] of $G$, a [[groupal model for universal principal infinity-bundles|groupal model for the universal principal bundle]];

* $\mathbf{B}INN(G)$ -- the coefficient for $INN(G)$-[[principal 2-bundle]];

* $\mathbf{B}G_{conn} := Hom_{Grpd(Diffeo)}(\mathbf{P}_1(-), \mathbf{B}G)$ -- the coefficient for $G$-principal bundles with [[connection on a bundle|connection]];

* $\mathbf{\flat} \mathbf{B}G := Hom_{Grpd(Diffeo)}(\Pi_2(-), \mathbf{B}INN(G))$ the coefficient for flat $G$-principal bundles with flat connection;

* $\mathbf{\flat} \mathbf{B}INN(G) := [\Pi_2(-), \mathbf{B}INN(G)]$ the coefficient for flat $INN(G)$-principal 2-bundles;

* $\mathbf{B}G_{diff} := \mathbf{\flat}\mathbf{B}INN(G) \times_{\mathbf{B}INN(G)} \mathbf{B}G $ -- the coefficient for $G$-[[principal bundle]]s with [[pseudo-connection]];


We have the following morphisms between these:

* $X \to \mathbf{P}_1(X)$ -- inclusion of constant paths into all paths;

* $\mathbf{P}_1(X) \to \mathbf{\Pi}_1(X)$ -- sends [[thin homotopy]]-classes of paths to their full homotopy classes;

* $\mathbf{\flat}\mathbf{B}G \to \mathbf{B}G_{conn}$ -- the morphism which forgets that a connection is flat;

* $\mathbf{B}G_{conn} \to \mathbf{B}G$ -- forgets the connection on a $G$-bundle, induced locally by $U \to \mathbf{P}_1(U)$;

* $\mathbf{B}G_{conn} \to \mathbf{\flat} \mathbf{B}INN(G)$ -- the morphism that fills in the integrated curvature between paths enclosing a surface;

* $\mathbf{B}G_{conn} \to \mathbf{B}G_{diff}$ the morphism that regards an ordinary connection as a special case of a pseudo-connection, induced as a morphism into a pullback by the two morphisms $\mathbf{B}G_{conn} \to \mathbf{B}G$ and $\mathbf{B}G_{conn} \to \mathbf{\flat} \mathbf{B}INN(G)$;



### For connections on $G$-principal $\infty$-bundles {#CWHomomorphismSummary}

For $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally an [[∞-Lie algebroid]] and $\exp(\mathfrak{g}) \in [CartSp^{op},sSet]$ its untruncated [[Lie integration]], the  [[simplicial presheaf]] $\exp(\mathfrak{g})_{conn}$  of [[∞-Lie algebra valued differential forms]] is such that lifts $\nabla$

$$
  \array{
    && \exp(\mathfrak{g})_{conn}
    \\
    & {}^{\nabla}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \exp(\mathfrak{g})
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$ 

of $\exp(\mathfrak{g})$-cocycles $g$ constitute a [[connection on an ∞-bundle]] on the [[principal ∞-bundle]] defined by $g$:

$$
  \exp(\mathfrak{g})_{conn}
  \subset 
  \exp(\mathfrak{g})_{conn'}
  : 
  (U,[k])
  \mapsto
  \left\{
  \array{
     \Omega^\bullet_{vert}(U \times \Delta^n)
     &\stackrel{A_{vert}}{\leftarrow}&
     CE(\mathfrak{g})
     &&&
     transition\;function\;/\;Cech\;cocycle
     \\
     \uparrow && \uparrow &&&& first\;Ehresmann\;condition
     \\
     \Omega^\bullet(U \times \Delta^n)
     &\stackrel{A}{\leftarrow}&
     W(\mathfrak{g})
     &&& 
     connection
     \\
     \uparrow && \uparrow &&&& second\; Ehresmann\;condition
     \\
     \Omega^\bullet(U)
     &\stackrel{\langle F_A\rangle}{\leftarrow}&
     inv(\mathfrak{g})
     &&&
     curvature\;characteristics
  }
  \right\}
  \,.
$$

For fixed $U \in $ [[CartSp]] and $k \in \Delta$ the sets on the right are sets of  [[∞-Lie algebra valued differential forms]] on $U \times \Delta^k$ subject two conditions:

1. restricted to the fibers the forms become flat and coincide with the forms that define the transition functions;

1. their [[curvature characteristic form]]s $\langle F_A \rangle$ descend to the base.

The subsheaf $\exp(\mathfrak{g})_{conn} \hookrightarrow \exp(\mathfrak{g})_{conn'}$ is that for every [[curvature]] form $F_A$ has no component along the simplicial directions.

Here $\Omega^\bullet(U \times \Delta^k)_{vert}$ are the [[vertical differential form]]s on the trivial simplex bundle $U \times \Delta^k \to U$ 
and on the right we have the canonical sequence [[Chevalley-Eilenberg algebra]] $\leftarrow$ [[Weil algebra]] $\leftarrow$ [[invariant polynomial]]s and all morphisms are [[dg-algebra]] morphisms. 

$$
  \array{
    CE(\mathfrak{g})  &&& G &&& Chevalley-Eilenberg\;algebra
    \\
    \uparrow &&& \downarrow 
    \\
    W(\mathfrak{g}) &&& \mathbf{E}G &&& Weil\;algebra
    \\
    \uparrow &&& \downarrow
    \\
    inv(\mathfrak{g}) &&& \mathbf{B}G &&& algebra\;of\;invariant\;polynomials
  }
  \,.
$$


A triple consisting of

* an [[∞-Lie algebra cocycle]] $\mu : \mathfrak{g} \to b^{n-1} \mathbb{R}$ 

* in transgression with an [[invariant polynomial]] $\langle - \rangle_\mu$

* mediated by a [[Chern-Simons element]] $cs_\mu$ 

is exhibited by a [[commuting diagram]]

$$
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
     CE(b^{k} \mathbb{R})
     &&&
     cocycle
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{cs_\mu}{\leftarrow}&
     W(b^k \mathbb{R})
     &&&
     Chern-Simons\;element
     \\
     \uparrow && \uparrow
     \\
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle_\mu}{\leftarrow}&
     inv(b^k \mathbb{R}) 
     &&&
     invariant\;polynomial
  }
$$

in [[dgAlg]].


The $\infty$-Chern-Weil homomorphism at this untruncated level is postcomposition with the lift of

$$
  \exp(\mu)  : \exp(\mathfrak{g}) \to \exp(b^{n-1}\mathbb{R})
$$

to the map

$$
  \exp(\mu)_{conn} : \exp(\mathfrak{g})_{conn} \to \exp(b^{n-1}\mathbb{R})_{conn}
$$

given by forming the [[pasting]] composites

$$
  \array{
     \Omega^\bullet(U \times \Delta^n)_{vert}
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
     \Omega^\bullet(U \times \Delta^n)
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
     \Omega^\bullet(U)
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

This produces a $b^{n-1}\mathbb{R}$-valued connections with local connection forms the [[Chern-Simons form]]s $CS_\mu(A)$ and with curvature the [[curvature characteristic form]] $\langle - \rangle_\mu$.

Under [[truncated|truncation]] $\exp(\mathfrak{g}) \to \tau_n \exp(\mathfrak{g}) \simeq \mathbf{B}G$ this decends under suitable conditions to the genuine refine $\infty$-Chern-Weil homomorphism

$$
  \exp(\mu)_{conn} : 
  \mathbf{B}G_{conn} = \tau_n \exp(\mathfrak{g})_{conn}
  \to 
  (\mathbf{B}^n \mathbb{R}/\Gamma)_{conn}
$$

that sends principal $\infty$-bundles with connection to [[circle n-bundles with connection]].

## References

The text of this entry is reproduced from the introduction of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

A commented list of further related references is at

* _[[schreiber:differential cohomology in an (∞,1)-topos -- references]]_ .


[[!redirects ∞-Chern-Weil theory -- preparatory concepts]]
[[!redirects ∞-Chern-Weil-theory introduction]]
[[!redirects ∞-Chern-Weil theory introduction]]

[[!redirects infinity-Chern-Weil theory -- preparatory concepts]]
s