
#Contents#
* table of contents
{:toc}

## Idea

In an [[associated bundle]] with [[connection]] the _covariant derivative_ of a [[section]] is a measure for how that section fails to be constant with respect to the connection.

## Definition

Let $G$ be a [[Lie group]], $V$ a [[smooth manifold]] and $\rho : G \tmes V \to V$ a smooth [[action]]. Write $V//G$ for the corresponding [[action groupoid]], itself a Lie groupoid. 

+-- {: .un_lemma}
###### Observation

The [[Chevalley-Eilenberg algebra]] of the corresponding [[Lie algebroid]] $Lie(V((G)$ -- the [[action Lie algebroid]] -- is 

$$
  CE(Lie(V//G)) = (\wedge^\bullet_{C^\infty(V)} \mathfrak{g}^*, d_{\rho})
  \,,
$$

where the differential acts on functions $f \in C^\infty(V)$ 

$$
  d_\rho : f \mapsto \rho(-)()^* f \in C^\infty(V)\otimes \mathfrak{g}^*
  \,.
$$

Explicitly, for $t \in \mathfrak{g}$ this sends $f$ to the function
$(d_\rho f)(t)$ which is the derivative along $t \in T_e G$ of the function $G \times V \stackrel{\rho}{\to}V \stackrel{f}{\to} \mathbb{R}$.

=--

Notice that we may identify the [[delooping]] Lie groupoid $\mathbf{B}G$ of $G$ with the action groupoid of the trivial action on the point, $\mathbf{B}G \simeq *//G$. This induces a canonical moprhism $V//G \to \mathbf{B}G$.

For $X$ [[smooth manifold]], a $G$-[[principal bundle]] $P \to X$ is given by a  [[cocycle]] in [[∞LieGrpd]] $g : X \to \mathbf{B}G$. 

+-- {: .un_lemma}
###### Observation

On Lie algebroids this morphism is dually the inclusion

$$
  CE(Lie(V//G)) \leftarrow CE(\mathfrak{g})
$$

that is the identity on $\mathfrak{g}^*$.

=--

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

+-- {: .un_lemma}
###### Observation

Given a [[connection on a bundle|connection]] $\nabla$ on the $G$-[[principal bundle]] with cocycle $g$, there is a unique connection $\nabla \sigma$ on the $V//G$-[[ggroupoid principal bundle]] that corresponds to a section $\sigma$ by the above proposition.

=--

+-- {: .un_def}
###### Definition

The **covariant derivative** of a section $\sigma$ is the _1-form component_ $F_{\nabla \sigma}^1$ of the [[curvature]] of this groupoid-bundle connection.

=--

This is literally the measure for the _non-flatness of the section_ . Whereas the 2-form curvature is a measure for the non-flatness of the connection.

+-- {: .un_lemma}
###### Observation

On a single $U_i$ the connection $\nabla$ is given by a morphism of [[dg-algebra]]s 

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

This is the dual of the local section $\sigma_i$ itself. In degree 1 this is linear map

$$
  \Omega^1(U_i) \leftarrow \mathfrak{g}^* : A_i
  \,,
$$

which is the connection forrm itself, as well as a linear map

$$
  \Omega^1(U_i) \leftarrow \Omega^1(C) : F^1_{\nabla \sigma_i}
  \,,
$$

which is the curvature 1-form. The respect of these maps for the differential says that

$$
  F^1_{\nabla \sigma_i} = d_{dR} \sigma_i + \rho(A)(\sigma_i)
  \,.
$$

This is the familiar local formula for a covariant derivative as one finds it in the literature.

=--

[[!redirects covariant derivative]]