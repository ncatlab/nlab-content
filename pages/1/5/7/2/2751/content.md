
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

In an [[associated bundle]] with [[connection]] the _covariant derivative_ of a [[section]] is a measure for how that section fails to be constant with respect to the connection.

## Definition


### In the context of connections on $\infty$-groupoid principal bundles

We give here a definition of covariant derivatives that is natural in the general context of [[∞-Chern-Weil theory]] in that it applies to [[connections on ∞-bundles]]. 

We start by describing this just for ordinary [[connections on a bundle]] and demonstrate how this general abstract definition reproduces the traditional definitions found in the literature.

The central statement is: a covariant derivative $\nabla \sigma$ of a section may be identified with the 1-form [[curvature]]-component of a [[Lie algebroid]]-valued connection, and the curvature equation

$$
  \nabla \nabla \sigma = F_\nabla \sigma
$$ 

is the [[Bianchi identity]] on its curvature 1-form.

#### Preliminaries on action Lie algebroid cohomology {#ActionLieAlgebroidCohomology}

Let $G$ be a [[Lie group]], $V$ a [[smooth manifold]] and $\rho : G \times V \to V$ a smooth [[action]]. Write $V//G$ for the corresponding [[action groupoid]], itself a Lie groupoid.  The [[Lie algebroid]] $Lie(V//G)$ corresponding to this is the [[action Lie algebroid]].

Below we shall define covariant derivatives as curvature components of [[∞-Lie algebroid valued forms]] with values in this action Lie algebroid. To prepare the ground for this, the following observation recalls some basic facts.


The [[Chevalley-Eilenberg algebra]] of the action Lie algebroid is

$$
  CE(Lie(V//G)) = (\wedge^\bullet_{C^\infty(V)} \mathfrak{g}^*, d_{\rho})
  \,,
$$

where the differential acts on functions $f \in C^\infty(V)$ by

$$
  d_\rho : f \mapsto \rho(-)(-)^* f \in C^\infty(V)\otimes \mathfrak{g}^*
  \,.
$$

Explicitly, for $t \in \mathfrak{g}$ this sends $f$ to the function
$(d_\rho f)(t)$ which is the derivative along $t \in T_e G$ of the function $G \times V \stackrel{\rho}{\to}V \stackrel{f}{\to} \mathbb{R}$.

Even more explicitly, if we choose local coordinates $\{v^k\} : \mathbb{R}^{dim V} \to V$ on a patch, and choose a basis $\{t^a\}$ of $\mathfrak{g}^*$ then we have that restricted to this patch the differential is on generators by

$$
  d_\rho : f \mapsto \rho^\mu{}_a t^a \wedge \partial_k f
$$

$$
  d_\rho : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,.
$$

Specifically for $V$ a finite dimensional [[vector space]], $\rho : G$ a _linear_ action, $\{v^k\}$ a choice of basis of that vector space and $f$ a _[[linear function]]_ $f= f_k v^k$ , we have that $(f_k := \partial_k f) \in \mathbb{R}^{dim V}$ are the components vector of the dual vector given by $V$ in this basis, and the above gives the [[matrix multiplication]] form of the action

$$
  d_\rho : v^k \mapsto t^a \rho_a{}^k{}_l  v^l
  \,.
$$

Notice for completeness that the equation $(d_\rho)^2 = 0$ is equivalent to the [[Jacobi identity]] of the Lie bracket and the action property of $\rho$:

$$
  d_\rho d_\rho v^k = 
   (t^a \wedge t^b \rho_a{}^k{}_r \rho_b{}^r{}_l
    -
    \frac{1}{2}C^a{}_{b c}t^b \wedge t^c \rho_a{}^k{}_l )
     v^l
  \,.
$$

These local formulas shall be useful below for recognizing from our general abstract definition of covariant derivative the formulas traditionally given in the literature. For that notice that in the above local coordinates further restricting attention to linear actions, the [[Weil algebra]] of the action Lie algebroid is given by

$$
  W(Lie(V//G)) = (\wedge^\bullet_{C^\infty(\mathbb{R}^{dim V})} ( \Gamma(T^* \mathbb{R}^{dim V}) \oplus \mathfrak{g}^* \oplus \mathfrak{g}^*[1]), d_{W_\rho})
$$

where the differential is given on generators by

$$
  d_{W_\rho} : v^k \mapsto \rho_a{}^k{}_l t^a \wedge v^l + d_{dR} v^k
$$

$$
  d_{W_\rho} : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a
$$

and where the uniquely induced differential on the shifted generators -- the one encoding [[Bianchi identities]] -- is

$$
  d_{W_\rho}  : d_{dR} v^k 
      \mapsto 
        \rho_a{}^k{}_k r^a \wedge v^l 
      - \rho_a{}^k{}_l t^a \wedge  d_{dR} v^l
$$

and 

$$
  d_{W} : r^a \mapsto C^a{}_{b c} t^b \wedge r^c
  \,.
$$



Notice that we may identify the [[delooping]] Lie groupoid $\mathbf{B}G$ of $G$ with the action groupoid of the trivial action on the point, $\mathbf{B}G \simeq *//G$.  On Lie algebroids this morphism is dually the inclusion

$$
  CE(Lie(V//G)) \leftarrow CE(\mathfrak{g})
$$

that is the identity on $\mathfrak{g}^*$.



#### Sections of bundles as groupoid principal bundles


For $X$ [[smooth manifold]], a $G$-[[principal bundle]] $P \to X$ is given by a  [[cocycle]] in [[?LieGrpd]] $g : X \to \mathbf{B}G$. 

+-- {: .un_prop}
###### Proposition

The [[section]]s $\sigma$ of the corresponding $\rho$-[[associated bundle]] $P \times_\rho V$ are in natural [[bijection]] with the lifts to a $V//G$-cocycle

$$
  \array{
    && V//G
    \\
    & {}^{\mathllap{\sigma}}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

We may model the coycle $X \to \mathbf{B}G$ in the [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,loc}$ by an [[anafunctor]] $X \stackrel{\simeq}{\leftarrow} C(U) \stackrel{g}{\to} \mathbf{B}G$ for $C(U)$ the [[Cech groupoid]] of a [[good open cover]] $\{U_i \to X\}$. This is a collection of [[smooth function]]s $(g_{i j} : U_i \cap U_j \to G)$ such that

$$
  \left(
    \array{
      && (x,j)
      \\
      & \nearrow && \searrow
      \\
      (x,i) &&&& (x,k)
    }
  \right)
  \mapsto
  \left(
    \array{
      && \bullet
      \\
      & {}^{\mathllap{g_{i j}(x)}}\nearrow && \searrow^{\mathrlap{g_{j k}(x)}}
      \\
      \bullet &&\stackrel{g_{i k}(x)}{\to}&& \bullet
    }
  \right)
  \,.
$$

A lift of this cocycle through $V//G \to \mathbf{B}G$ is in addition a collection of smooth functions $\{sigma_i : U_i \to V\}$ such that on all $U_i \cap U_j$ the equation

$$
  \sigma_j = \rho(g_{i j})(\sigma_i)
$$

$$
  \left(
    \array{
      \sigma_i(x) &&\stackrel{\rho(g_{i k}(x))}{\to}&& \sigma_k(x)
    }
  \right)
$$

is satisfied. This identifies the $\sigma_i$ as precisely the components of a section $\sigma$ of $P \times_\rho G$ with respect to the local trivialization encoded by $g$.

=--

#### Definition of covariant derivative

+-- {: .un_lemma}
###### Observation

Given a [[connection on a bundle|connection]] $\nabla$ on the $G$-[[principal bundle]] with cocycle $g$, there is a unique connection $\nabla \sigma$ on the $V//G$-[[groupoid principal bundle]] that corresponds to a section $\sigma$ by the above proposition.

=--

+-- {: .un_def}
###### Definition

The **covariant derivative** of a section $\sigma$ is the _1-form component_ $F_{\nabla \sigma}^1$ of the [[curvature]] of this groupoid-bundle connection.

=--

This 1-form curvature is literally the measure for the _non-flatness of the section_ . Whereas the 2-form curvature is a measure for the non-flatness of the connection.

#### Equivalence to more traditional definitions

We unwind this definition and find the traditional formulation of covariant derivatives as traditionally stated in the literature.


On a patch $U_i \hookrightarrow X$ the connection $\nabla$ is given by a morphism of [[dg-algebra]]s 

$$
  \Omega^\bullet(U_i) \leftarrow W(\mathfrak{g}) : A_i
$$

for $W(\mathfrak{g})$ the [[Weil algebra]] of $\mathfrak{g}$.

The groupoid connection $\nabla \sigma$ on this patch is given by

$$
  \Omega^\bullet(U_i) \leftarrow W(Lie(V//G)) : \nabla \sigma_i
  \,.
$$

In degree 0 this is an algebra homomorphism

$$
  C^\infty(U_i) \leftarrow C^\infty(V) : \sigma_i
  \,.
$$

This is the dual of the local section $\sigma_i$ itself. In the case that $V$ is a vector space with chosen basis $\{v^k\}$, we have the corresponding components $(\sigma_i^k)$ of the local section.



Further, in degree 1 the connection is linear map

$$
  \Omega^1(U_i) \leftarrow \mathfrak{g}^* : A_i
  \,,
$$

which is the connection form itself, as well as a linear map

$$
  \Omega^1(U_i) \leftarrow \Omega^1(V) : F^1_{\nabla \sigma_i}
  \,,
$$

which is the curvature 1-form. The respect of these maps for the differential says that

$$
  F^1_{\nabla \sigma_i} = d_{dR} \sigma_i + \rho(A)(\sigma_i)
  \,.
$$

This is the familiar local formula for a covariant derivative as one finds it in the literature. We therefore write for short

$$
  \nabla_{(-)} \sigma_i := F^1_{\nabla sigma_i}
$$

If we keep $\nabla$ fixed and let $\sigma_i$ vary, then this may be thought of as a 1-form with values in [[endomorphism]]s of the space of sections

$$
  \nabla_{(-)} : \Gamma(P \times_\rho V) \to \Gamma(P \times_\rho V)
  \,.
$$

There is a [[Bianchi identity]] on every [[curvature]] component, induced from the respect for differentials of the dg-algebra morphism $\Omega^\bullet(U_i) \leftarrow W(Lie(V//G)) : F_\nabla$ on shifted generators. 

From the discussion at [Action Lie algebroid cohomology](#ActionLieAlgebroidCohomology) above we read off the Bianchi identity for the 1-form curvature that we identified with the covariant derivative in the case of linear actions to be given in local coordinates (as above) by (suppressing the patch index ${}_i$)


$$
  d_{dR} \nabla_{(-)} \sigma^k = \rho_a{}^k{}_k F_A^a \wedge \sigma^k 
  - 
  \rho_a{}^k{}_l A^a d_{dR} \sigma^k
  ,.
$$

More invariantly we may write this as 

$$
  \nabla_{(-)} \nabla_{(-)} \sigma = \rho(F_A)(\sigma)
$$

and this find the usual expression of the [[curvature]] of a connection as the square of the covariant derivative.

[[!redirects covariant derivative]]