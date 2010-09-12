
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[connection on a bundle]] induces a notion of [[parallel transport]] over _paths_ . A [[connection on a 2-bundle]] induces a generalization of this to a notion of parallel transport over _surfaces_ . Similarly a [[connection on a 3-bundle]] induces a notion of parallel transport over 3-dimensional volumes.

Generally, a [[connection on an ∞-bundle]] induces a notion of parallel transport in arbitrary dimension.

## Definition

### Preparatory definition

There is a definition of parallel transport of general [[connections on an ∞-bundle]]. Before describing that consider the special case where for a connection $\nabla$ on an $G$-[[principal ∞-bundle]] for an [[∞-Lie groupoid|Lie n-group]] all $k$-form components of the [[curvature]] vanish for $0 \leq k \leq n$, so that only the $(n+1)$-form curvature is allowed to be non-vanishing. (Notice that this is automatically the case when $G = \mathbf{B}^{n-1} A$ is $(n-1)$-[[connected]], as is the case for instance for a [[circle n-bundle with connection]].)

In this case the connection is given by an [[∞-anafunctor]]

$$
  \array{
    && [\mathbf{P}_n(-), \mathbf{B}G]
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

where $[\mathbf{P}_(-),\mathbf{B}G]$ is the [[∞-Lie groupoid]] given by the [[simplicial presheaf]] $U \mapsto [CartSp^{op}, sSet](\mathbf{P}_(U), \mathbff{B}G)$ on [[CartSp]], where $\mathbf{P}_n(U)$ is the [[path n-groupoid]] of $U$.

Then for $\phi : \Sigma_n \to X$ a smooth map we get a composition of [[∞-anafunctor]]s

$$
  \array{
    && && [\mathbf{P}_n(-), \mathbf{B}G]
    \\
    && & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(V) &\to& C(U) &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    \Sigma &\stackrel{\phi}{\to}& X
  }
$$

and hence a $G$-connection on $\Sigma$. We have an equivalence of $\infty$-anafunctors  

$\{\Sigma \to [\mathbf{P}_n(-), \mathbf{B}G]\}
\simeq
  \{ \mathbf{P}_n(\Sigma) \to \mathbf{B}G \}$.

(For detail in $n = 2$ see [SWIII](#SWIII)). The **higher parallel transport** of $\nabla$ over $\Sigma$ for a choice $\phi \in mor_n \mathbf{P}_n(\Sigma)$ of fundamental class in $\Sigma$ is then the image of $\phi$ under $tra_{\phi^*\nabla} : \mathbf{P}_n(\Sigma) \to \mathbf{B}G$.

Notice that this is the image of an $n$-morphism under an _anafunctor_ . Hence there are actually many such images, one for each choice of lift through the refinement $\mathbf{P}_n(C(V)) \to \mathbf{P}_n(\Sigma)$. These choices are the generalization of what for $n=1$ is the choice of lift in the fiber over the start point of a path in the base.

### General definition

In the case that the lower degree curvature forms do not vanish, the connection is an [[∞-anafunctor]] with values in the [[∞-groupoid of ∞-Lie algebroid valued forms]] $\mathbf{B}G_{conn}$. This is the [[∞-Lie groupoid]] given by the  [[concrete sheaf|non-concrete]] [[simplicial presheaf]]

$$
  \mathbf{B}G_{conn} \subset
  \mathbf{B}G_{diff}
  =
  \mathbf{B}G \times_{\mathbf{B}G} [\mathbf{\Pi}(-),\mathbf{B}G]
  :
  (U,[n])
  \mapsto
  \left\{
     \array{
       U &\to& \mathbf{B}G &&& cocycle
       \\
       \downarrow && \downarrow
       \\
       \mathbf{\Pi}(U) &\to& \mathbf{B}INN(G) &&& connection
     }
  \right\}
$$

for $INN(G)$ a [[groupal model for universal principal ∞-bundles|groupal model for the universal G-principal ∞-bundle]].


(...)

## Examples

The simplest example is the parallel transport in a [[circle n-bundle with connection]] over a [[smooth manifold]] $X$ whose underlying $\mathbf{B}^{n-1}U(1)$-bundle is trivial. This is equivalently given by a degree $n$-[[differential form]] $A \in \Omega^n(X)$. For $\phi : \Sigma_n \to X$ any [[smooth function]] from an $n$-dimensional manifold $\Sigma$, the corresponding parallel transport is simply the [[integral]] of $A$ over $\Sigma$:

$$
  \tra_A(\Sigma) = \exp(i \int_\Sigma \phi^* A)
  \;\;\; \in \;\; U(1)
  \,.
$$

One can understand higher parallel transport therefore as a generalization of integration of diifferential $n$-forms to the case where

* the $n$-form is not globally defined;

* the $n$-form takes values not in $\mathbb{R}$ but more generally is an [[∞-Lie algebroid valued differential form]].

## Applications

### In physics

In [[physics]] various [[action functional]]s for [[quantum field theories]] are nothing but higher parallel transport.

* The gauge interaction part of the action functional for the particle charged under a background [[electromagnetic field]], which is a [[circle n-bundle with connection|circle bundle with connection]] $\nabla$, is the parallel 1-transport of $\nabla$.

* The gauge interaction part of the action functional for the string charged under a background [[Kalb-Ramond field]], which is a [[circle n-bundle with connection|circle 2-bundle with connection]] $\nabla$, is the parallel 2-transport of $\nabla$.

* The gauge interaction part of the action functional for the membrane charged under a background [[supergravity C-field]], which is a [[circle n-bundle with connection|circle 3-bundle with connection]] $\nabla$, is the parallel 3-transport of $\nabla$.

* The action functional of [[Chern-Simons theory]] is the parallel 3-transport of a [[Chern-Simons circle 3-bundle]].



## References

For references on parallel 2-transport in bundle gerbes see [[connection on a bundle gerbe]].

The generalization of this to parallel 2-transport of [[connections on a 2-bundle]] as described above is in 

* SWIII (<a href="SchrWalII+III">web</a>)
{#SWIII}
