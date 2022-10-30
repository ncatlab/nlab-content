

> under construction

#Contents#
* table of contents
{:toc}

## Idea

In the axiomatic of [[differential cohesion]] one may [[synthetic differential geometry|synthetically]] formulate a concept of _[[manifolds]]_ locally modeled on a [[group object]] $V$. In the [[interpretation]] in an [[differential cohesion|differentially]] [[cohesive (infinity,1)-topos]] these are [[étale infinity-groupoids]].

For exposition see at _[[geometry of physics -- manifolds and orbifolds]]_ and _[[geometry of physics -- supergeometry]]_.


## $V$-Manifolds
 {#VManifolds}


+-- {: .num_defn #LocalDiffeomorphismsInDifferentialCohesion}
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

is a [[homotopy pullback]] square. 

=--

Let now $V \in \mathbf{H}$ be given, equipped with the structure of a [[group]] ([[∞-group]]).

+-- {: .num_defn #VManifold}
###### Definition

A _[[V-manifold]]_ is an $X \in \mathbf{H}$ such that there exists a _$V$-[[atlas]]_, namely a [[correspondence]] of the form

$$
  \array{
    && U
    \\
    & \swarrow && \searrow
    \\
    V && && X
  }
$$

with both morphisms being [[local diffeomorphisms]], def. \ref{LocalDiffeomorphismsInDifferentialCohesion}, and the right one in addition being an [[epimorphism]], hence an [[atlas]].

=--



## Frame bundles
 {#FrameBundles}


+-- {: .num_defn #InfinitesimalDisk}
###### Definition

For $X \in \mathbf{H}$ an object and $x \colon \ast \to X$ a point, then we say that the _[[infinitesimal neighbourhood]] of_, or the _[[infinitesimal disk]] at_ $x$ in $X$ is the [[homotopy fiber]] $\mathbb{D}^X_x$ of the [[unit of a monad|unit]] of the [[infinitesimal shape modality]] at $x$:

$$
  \array{
    \mathbb{D}^X_x &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    \ast &\stackrel{x}{\longrightarrow}& \im X
  }
  \,.
$$ 

=--

+-- {: .num_defn #FormalDiskBundle}
###### Definition


For $X$ any object in differential cohesion, its _infinitesimal disk bundle_ $T_{inf} X \to X$ is the [[homotopy pullback]]

$$
  \array{
    T_{inf} X &\stackrel{ev}{\longrightarrow}& X
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\longrightarrow& \Im X
  }
$$

of the [[unit of a monad|unit]] of its [[infinitesimal shape modality]] along itself.

=--

+-- {: .num_remark}
###### Remark

By the [[pasting law]], the [[homotopy fiber]] of the infinitesimal disk bundle, def. \ref{FormalDiskBundle},  over any point $x \in X$ is the infinitesimal disk $\mathbb{D}^X_x$ in $X$ at that point, def.\ref{InfinitesimalDisk}. Nevertheless, for general $X$ the infinitesimal disk bundle need not be an [[fiber ∞-bundle]] with typical fiber (the infinitesimal disks at different points need not be equivalent, and even if they are, the bundle need not be locally trivial). Below in prop. \ref{FormalDiskBundleOfRegularManifoldsTrivializesOverCover} we see that for $X$ a $V$-manifold modeled on a group object $V$, then its infinitesimal disk bundle is indeed an [[fiber ∞-bundle]], and hence is the [[associated ∞-bundle]] to some [[principal ∞-bundle]]. That principal bundle is the [[frame bundle]] of $X$.

=--

+-- {: .num_remark}
###### Remark


The [[Atiyah groupoid]] of $T_{inf} X$ is the [[jet groupoid]] of $X$.

=--

+-- {: .num_lemma #EtalePullbackOfFormalDiskBundleIsFormalDiskBundle}
###### Lemma

If $\iota \colon U \to X$ is a local diffeomorphism, def. \ref{LocalDiffeomorphismsInDifferentialCohesion}, then

$$
  \iota^\ast T_{inf} X \simeq T_{inf}U
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the definition of local diffeos and using the [[pasting law]] we have an equivalence of [[pasting diagrams]] of [[homotopy pullbacks]] of the following form:

$$
  \array{
     \iota^\ast T_{inf} X &\longrightarrow& T_{inf} &\longrightarrow& X
     \\
     \downarrow && \downarrow && \downarrow
     \\
     U &\longrightarrow& X &\longrightarrow& \Im X
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
      T_{inf} U &\longrightarrow& U &\longrightarrow& X
       \\
       \downarrow && \downarrow && \downarrow
       \\
       U &\longrightarrow& \Im U &\longrightarrow& \Im X
  }
$$


=--

+-- {: .num_defn #Framing}
###### Definition

For $V$ an object, a **[[framing]]** on $V$ is a trivialization of its infinitesimal disk bundle, def. \ref{FormalDiskBundle}, i.e. an object $\mathbb{D}^V$ -- the typical [[infinitesimal disk]] or [[formal disk]], def. \ref{InfinitesimalDisk}, -- and a (chosen) [[equivalence]]

$$
  \array{
    T_{inf} V && \stackrel{\simeq}{\longrightarrow} && V \times \mathbb{D}^n
    \\
    & \searrow && \swarrow_{\mathrlap{p_1}}
    \\
    && V
  }
  \,.
$$



=--

+-- {: .num_defn #GeneralLinearGroup}
###### Definition

For $V$ a framed object, def. \ref{Framing}, we write

$$
  GL(V) \coloneqq \mathbf{Aut}(\mathbb{D}^V)
$$

for the [[automorphism ∞-group]] of its typical [[infinitesimal disk]]/[[formal disk]].

=--

+-- {: .num_remark #OrderOfInfinitesimalDisks}
###### Remark

When the [[infinitesimal shape modality]] exhibits first-order infinitesimals, such that $\mathbb{D}(V)$ is the first order [[infinitesimal neighbourhood]] of a point, then $\mathbf{Aut}(\mathbb{D}(V))$ indeed plays the role of the [[general linear group]]. When $\mathbb{D}^n$ is instead a higher order or even the whole [[formal neighbourhood]], then $GL(n)$ is rather a [[jet group]]. For order $k$-jets this is sometimes written $GL^k(V)$ We nevertheless stick with the notation "$GL(V)$" here, consistent with the fact that we have no index on the [[infinitesimal shape modality]]. More generally one may wish to keep track of a whole tower of infinitesimal shape modalities and their induced towers of concepts discussed here.

=--


This class of examples of framings is important:

+-- {: .num_prop #DifferentialCohesiveInfinityGroupIsCanonicallyFramed}
###### Proposition

Every differentially cohesive [[∞-group]] $G$ is canonically framed (def. \ref{Framing}) such that the horizontal map in def. \ref{FormalDiskBundle} is given by the left action of $G$ on its [[infinitesimal disk]] at the neutral element:

$$
  ev \;\colon\; T_{inf}G \simeq G \times \mathbb{D}^G_e \stackrel{\cdot}{\longrightarrow} G
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at _[[Mayer-Vietoris sequence]]_ in the section _[Over an ∞-group](Mayer-Vietoris%20sequence#OverAGroupObject)_ and using that the [[infinitesimal shape modality]] preserves group structure, the defining [[homotopy pullback]] of $T_{inf} G$, def. \ref{FormalDiskBundle}, is equivalent to the pasting of pullback diagrams

$$
  \array{
    T_{inf} G &\stackrel{}{\longrightarrow}&
    \mathbb{D}^G_e
    &\stackrel{}{\longrightarrow}& \ast
    \\
    \downarrow &&  \downarrow && \downarrow
    \\
    G \times G &\stackrel{(-)\cdot (-)^{-1}}{\longrightarrow}& G
    &\stackrel{}{\longrightarrow}&
    \Im G
  }
$$

where the right square is the defining pullback for the [[infinitesimal disk]] $\mathbb{D}^G$. Finally for the left square we find by [this proposition](Mayer-Vietoris%20sequence#HTTArgumentForPullback) that $T_{inf} G \simeq G\times \mathbb{D}^G$ and that the top horizontal morphism is as claimed.

=--




By lemma \ref{EtalePullbackOfFormalDiskBundleIsFormalDiskBundle} it follows that:

+-- {: .num_prop #FormalDiskBundleOfRegularManifoldsTrivializesOverCover}
###### Proposition

For $V$ a framed object, def. \ref{Framing}, let $X$ be a $V$-manifold, def. \ref{VManifold}. Then the infinitesimal disk bundle, def. \ref{FormalDiskBundle}, of $X$ canonically trivializes over any $V$-cover $V \leftarrow U \rightarrow X$ , i.e. there is a [[homotopy pullback]] of the form

$$
  \array{
     U \times \mathbb{D}^V &\longrightarrow& T_{inf} X
     \\
     \downarrow && \downarrow
     \\
     U &\longrightarrow& X
  }
  \,.
$$

This exhibits $T_{inf} X\to X$ as a $\mathbb{D}^V$-[[fiber ∞-bundle]].

=--

+-- {: .num_prop #ModulatingMapOfFormalDiskBundle}
###### Remark

By [this discussion](fiber+infinity-bundle#Properties) this fiber [[fiber ∞-bundle]] is the [[associated ∞-bundle]] of an essentially uniquely determined $\mathbf{Aut}(\mathbb{D}^V)$-[[principal ∞-bundle]] $Fr(X)$, i.e. there exists a [[homotopy pullback]] diagram of the form

$$
  \array{
     T_{inf} X \simeq 
     & 
   Fr(X) \underset{\mathbf{Aut}(\mathbb{D}^V)}{\times} \mathbb{D}^V 
     &\longrightarrow&
     V//\mathbf{Aut}(\mathbb{D}^V)
     \\
     & \downarrow && \downarrow
     \\
     & X &\stackrel{}{\longrightarrow}& \mathbf{B}\mathbf{Aut}(\mathbb{D}^V)
  }
  \,.
$$

=--

+-- {: .num_defn #FrameBundleMap}
###### Definition

Given a $V$-manifold $X$, def. \ref{VManifold}, for framed $V$, def. \ref{Framing}, then its _[[frame bundle]]_ 

$$
  \array{
     Fr(X)
     \\
     \downarrow
     \\
     X 
  }
$$

is the $GL(V)$-[[principal ∞-bundle]] given by prop. \ref{FormalDiskBundleOfRegularManifoldsTrivializesOverCover} via remark \ref{ModulatingMapOfFormalDiskBundle}.

=--

+-- {: .num_remark }
###### Remark

As in remark \ref{OrderOfInfinitesimalDisks}, this really axiomatizes in general [[higher order frame bundles]] with the order implicit in the nature of the [[infinitesimal shape modality]].

=--

+-- {: .num_remark #FrameBundlesFunctorial}
###### Remark

By prop. \ref{EtalePullbackOfFormalDiskBundleIsFormalDiskBundle} the construction of frame bundles in def. \ref{FrameBundleMap} is functorial in [[formally étale maps]] between $V$-manifolds.

=--

This provides all the necessary structure to now set up an axiomatic theory of [[G-structure]] and [[higher Cartan geometry]]. This is discussed further at _[[geometry of physics -- G-structure and Cartan geometry]]_.


## References

The concept is due to 

* {#Schreiber} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations Part I -- Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

Formalization in [[homotopy type theory]] is in

* [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017 ([pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf))


[[!redirects V-manifolds]]

