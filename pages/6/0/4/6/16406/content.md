
> this entry contains one chapter of _[[geometry of physics]]_. See there for background and context.

> previous chapters: _[[geometry of physics -- smooth sets|smooth sets]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_

> next chapter: _[[geometry of physics -- G-structure and Cartan geometry]]_

#Contents#
* table of contents
{:toc}

## **Manifolds and orbifolds**


For $n \in \mathbb{N}$ a _[[manifold]]_ of [[dimension]] $n$ is an object $X$ that _locally looks_ like a [[Cartesian space]] $\mathbb{R}^n$, hence that can be thought of as being _glued together_ from Cartesian spaces by gluing these along [[diffeomorphisms]]. 

A natural way to make this precisely is to say that a [[manifold]] of dimension $X$ is an object such that first of all there is a [[cover]], hence a [[1-epimorphism]] of the form

$$
  p \;\colon\; \left(\coprod_{i \in i} \mathbb{R}^n\right) \to X
  \,.

$$

This encodes that $X$ can surjectively covered by Cartesian spaces, but it does not yet ensure that $X$ is _locally equivalent_ to a Cartesian space in the intended sense. That intended sense is that $p$ is a [[local diffeomorphism]].

Hence a manifold is a [[smooth space]] which receives a map out of a [[coproduct]] of [[Cartesian spaces]] that is a [[1-epimorphism]] and a [[local diffeomorphism]].

By the discussion above at _[Structure sheaves](#StructureSheaves)_ the general way to say _[[local diffeomorphism]]_ is to say _[[formally étale morphism]]_. Hence more generally we can consider the notion of a [[smooth groupoid]] which received a map out of a coproduct of Cartesian spaces that is a [[1-epimorphism]] and a [[formally étale morphism]]. If here the souce-fibers of the groupoid are in addition compact, then this is what is called an _[[orbifold]]_.

### Model Layer

1. [Smooth manifolds](Manifolds)

1. [Tangent bundle and frame bundle](#TangentBundle)

#### Smooth manifolds
  {#Manifolds}
  {#SmoothManifold}

A [[smooth manifold]] of [[dimension]] $n$ 

a [[smooth space]] with an [[atlas]] 

$$
  \{ \mathbb{R}^n \underoverset{\simeq}{\phi_i^{-1}}{\to} U_i \hookrightarrow X\}
$$ 

of [[coordinate charts]]. On each overlap $U_i \cap U_j$ of two charts, the [[partial derivatives]] of the corresponding [[coordinate transformations]]

$$
  \phi_j\circ \phi_i^{-1}
  : 
  U_i \cap U_j \subset \mathbb{R}^n \to \mathbb{R}^n
$$

form the [[Jacobian matrix]] of [[smooth functions]]

$$
  ((\lambda_{i j})^{\mu}{}_{\mu})
  \coloneqq
  \left[\frac{d}{d x^\nu} \phi_j \circ \phi_i^{-1} (x^\mu)
  \right]
  :
  U_i \cap U_j 
  \to 
  GL_n
$$

with values in invertible [[matrices]], hence in the
[[general linear group]] $GL(n)$. By construction (by the [[chain rule]]), these functions satisfy on triple overlaps of coordinate charts the [[matrix product]] equations

$$
  (\lambda_{i j})^\mu{}_\lambda (\lambda_{j k})^\lambda{}_{\nu} 
  = 
  (\lambda_{i k})^\mu{}_{\nu}
  \,,
$$

(here and in the following sums over an index appearing upstairs and downstairs are explicit)

hence the equation

$$
  \lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}
$$

in the [[group]] $C^\infty(U_i \cap U_j \cap U_k, GL(n))$ of smooth $GL(n)$-valued functions on the chart overlaps.

This is the _[[cocycle]] condition_ for a smooth [[Cech cohomology|Cech cocycle]] in degree 1 with coefficients in $GL(n)$ (precisely: with coefficients in the [[sheaf]] of [[smooth functions]] with values in $GL(n)$ ). We write

$$
  [(\lambda_{i j})] \in H^1_{smooth}(X, GL_n)
  \,.
$$

Formulated as [[smooth groupoids]]

* $X$ itself is a [[Lie groupoid]] $(X \stackrel{\to}{\to} X)$ with trivial morphism structure;

* from the atlas $\{U_i \to X\}$ we get the corresponding [[Cech groupoid]] 
  $$
    C(\{U_i\}) = 
    (\coprod_{i, j} U_i \cap U_j \stackrel{\to}{\to} \coprod_i U_i)
    = 
    \left\{
      \array{
         && (x,j)
         \\
         & \nearrow &=& \searrow
         \\
        (x,i) &&\to&& (x,k)
      }
      \;\;\;
      for\, x \in U_i \cap U_j \cap U_k
    \right\}
    \,,
  $$

  whose objects are the points in the atlas, with morphisms identifying lifts of a point in $X$ to different charts of the atlas;

#### Tangent bundle
 {#TangentBundle}

We discuss how the [[tangent bundle]] of a [[manifold]] $X$ naturally arises in the above perspective in terms of the map 
$\tau_X \;\colon\; X \to \mathbf{B}GL(n)$ that modulates it.

The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\tau_X}{\to}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]] (we make this more precise in a moment);

* the horizontal functor $\tau_X$ has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.


A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

This defines a morphism of [[smooth groupoids]]

$$
  \tau_X \;\colon\; X \to \mathbf{B}GL(n)
  \,.
$$

The [[homotopy fiber]] of this map is a $GL(n)$-[[principal bundle]] called the [[frame bundle]] of $X$, while  the canonically [[associated bundle]] via the canonical [[representation]] of $GL(n)$ on $\mathbb{R}^n$ is the [[tangent bundle]]

$$
  T X \to X
  \,.
$$


### Semantics Layer


#### $V$-Manifolds
 {#Manifolds}

See also at _[[geometry of physics -- manifolds and orbifolds]]_.

+-- {: .num_defn #LocalDiffeomorphisms}
###### Definition

Given $X,Y\in \mathbf{H}$ then a morphism $f \;\colon\; X\longrightarrow Y$ is a _[[local diffeomorphism]]_ if its naturality square of the [[infinitesimal shape modality]]

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

is a [[pullback]] square. 

=--

+-- {: .num_remark}
###### Remark

The abstract definition \ref{LocalDiffeomorphisms} comes down to being the appropriate [[synthetic differential supergeometry]]-version  of the traditional statement that $f$ is a [[local diffeomorphism]] if the diagram of [[tangent bundles]]

$$
  \array{
    T X &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{T f}} && \downarrow^{\mathrlap{f}}
    \\
    T Y &\longrightarrow& Y
  }
$$

To see this, notice by the discussion at _[[synthetic differential geometry]]_ that for $D$ an [[infinitesimally thickened point]], then for any $X \in \mathbf{H}$ the [[mapping space]] $[D,X]$ is the [[jet bundle]] of $X$ with jets of order as encoded by the infinitesimal order of $D$. In particular if $\mathbb{D}^1(1)$ is the first order infinitesimal interval defined by the fact that its [[algebra of functions]] is the [[algebra of dual numbers]] $C^\infty(\mathbb{D}^1(1)) = (\mathbb{R} \oplus \epsilon \mathbb{R})/(\epsilon^2)$, and $X$ is a [[smooth manifold]], then 

$$
  [\mathbb{D}^1(1), X]\simeq T X
$$

is the ordinary [[tangent bundle]] of $X$. Now use that the [[internal hom]] $[D,-]$ preserves [[limits]] in its second argument, and that, by the hom-adjunction, $\mathbf{H}(U, [D,X]) \simeq \mathbf{H}(U \times D, X)$ and finally use that $\mathbf{H}(U \times D, \Im X)\simeq \mathbf{H}(\Re(U \times D), X)\simeq \mathbf{H}(U,X)$.


=--

Let now $V \in \mathbf{H}$ be given, equipped with the structure of a [[group]] ([[infinity-group]]).

+-- {: .num_defn #VManifold}
###### Definition

A _$V$-[[manifold]]_ is an $X \in \mathbf{H}$ such that there exists a _$V$-[[atlas]]_, namely a [[correspondence]] of the form

$$
  \array{
    && U
    \\
    & \swarrow && \searrow
    \\
    V && && X
  }
$$

with both morphisms being [[local diffeomorphisms]], def. \ref{LocalDiffeomorphisms}, and the right one in addition being an [[epimorphism]], hence an [[atlas]].

=--


+-- {: .num_prop}
###### Proposition

If $f \;\colon\; X \longrightarrow Y$ is a [[local diffeomorphism]],
def. \ref{LocalDiffeomorphisms}, then so is image
$\stackrel{\rightsquigarrow}{f}\colon \stackrel{\rightsquigarrow}{X} \longrightarrow \stackrel{\rightsquigarrow}{Y}$ under the [[bosonic modality]].

=--

+-- {: .proof}
###### Proof

Since the [[bosonic modality]] provides [[Aufhebung]] for $\Re\dashv \Im$ by prop. \ref{Sublations} we have $\rightsquigarrow \Im \simeq \Im$. Moreover $\Im \rightsquigarrow \simeq \Im$ anyway. Finally $\rightsquigarrow$ preserves [[pullbacks]] (being in particular a [[right adjoint]]). Hence hitting a pullback diagram

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

with $\rightsquigarrow\;\;$ yields a pullback diagram

$$
  \array{
    \stackrel{\rightsquigarrow}{X} &\longrightarrow& \Im \stackrel{\rightsquigarrow}{X}
    \\
    \downarrow^{\mathrlap{\stackrel{\rightsquigarrow}{f}}} && \downarrow^{\mathrlap{\Im \stackrel{\rightsquigarrow}{f}}}
    \\
    \stackrel{\rightsquigarrow}{Y} &\longrightarrow& \Im \stackrel{\rightsquigarrow}{Y}
  }
$$

=--

+-- {: .num_cor }
###### Corollary

The bosonic space $\stackrel{\rightsquigarrow}{X}$ underlying 
a $V$-manifold $X$, def. \ref{VManifold}, is a $\stackrel{\rightsquigarrow}{V}$-manifold

=--

#### Frame bundles
 {#FrameBundles}

+-- {: .num_defn #GeneralLinearGroup}
###### Definition

The _[[general linear group]]_ $GL(V)$ is the [[automorphism infinity-group]] of the [[infinitesimal neighbourhood]] $\mathbb{D}^V_e$, def. \ref{InfinitesimalDiskBundle}, of the neutral element $e \colon \ast \to \mathbb{D}^V_e \to V$:

$$
  GL(V) \coloneqq \mathbf{Aut}(\mathbb{D}^V_e)
  \,.
$$

=--

+-- {: .num_prop #FrameBundle}
###### Proposition

For $X$ a $V$-manifold, def. \ref{VManifold}, then its infinitesimal disk bundle $T_{inf} X \to X$,
def. \ref{InfinitesimalDiskBundle}, is [[associated infinity-bundle|associated]]
to a $GL(V)$-[[principal infinity-bundle|principal]] $Fr(X) \to X$ -- to be called the _[[frame bundle]]_, [[modulating morphism|modulated]] by a map to be called $\tau_X$, producing [[homotopy pullbacks]] of the form

$$
  \array{
     T_{inf} X &\longrightarrow& V/GL(V)
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(V)
  }
  \;\;\;
  \array{
     Fr(X) &\longrightarrow& \ast
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(V)
  }
  \,.
$$

=--

+-- {: .num_defn #Framing}
###### Definition

A [[framing]] of a $V$-manifold is a trivialization of its [[frame bundle]], prop. \ref{FrameBundle}, hence a diagram in $\mathbf{H}$ of the fomr

$$
  \array{
    X && \longrightarrow && \ast
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}GL(V)
  }
$$


=--

+-- {: .num_remark #ModuliForFramings}
###### Remark

It is useful to express def. \ref{Framing} in terms of the [[slice topos]] $\mathbf{H}_{/\mathbf{B}GL(V)}$. Write $V\mathbf{Frame}\in \mathbf{H}_{/\mathbf{B}GL(V)}$ for the canonical morphism $\ast \to \mathbf{B}GL(V)$ regarded as an object in the slice. Then a framing as in def. \ref{Framing} is equivalently a morphism

$$
  \phi \colon \tau_X \longrightarrow V\mathbf{Frame}
$$

in $\mathbf{H}_{/\mathbf{B}GL(V)}$.

=--

+-- {: .num_prop #LeftTranslationFraming}
###### Proposition

The[[group object]] $V$, canonically regarded as a $V$-manifold, carries a canonical framing, def. \ref{Framing}, $\phi_{li}$, induced by left translation. 

=--


### Syntax Layer 

(...)
