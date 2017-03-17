

.

.

.

.


***

> please don't erase the following for the moment

***

#Contents#
* table of contents
{:toc}

## Models for $n$-image factorization

The following gives a sufficient condition for modeling [[n-image]] factorizations in some [[(∞,1)-toposes]] with particularly convenient presentation.

+-- {: .num_prop #nImageFactroizationModeledOnSimplicialPrsheaves}
###### Proposition

Let $C$ be a site with [[point of a topos|enough points]], so that the weak equivalences in $sPSh(C)_{\mathrm{loc}}$ are detected on [[stalks]] ([this prop.](model+structure+on+simplicial+presheaves#OverSiteWithEnoughPointsWeakEquivalencesDetectedOnStalks)). Then given a morphism of [[Kan complex]]-valued [[simplicial presheaves]]

$$
  f \colon X \longrightarrow Y$ in $sPSh(C)
$$

such that both  $X$ and $Y$ are [[homotopy n-types|homotopy k-types]] for some finite $k \in \mathbb{N}$, then its [[n-image]] factorization in the [[(∞,1)-topos]] $L_{lwhe} sPSh(C)_{loc}$ for any $n \in \mathbb{N}$ is presented by any factorization $X \longrightarrow im_{n}(f) \longrightarrow Y$ in $sPSh(C)$ through some Kan-complex valued simplicial presheaf $im_n(f)$ such that for each object $U \in C$ the [[simplicial homotopy groups]] satisfy the following conditions:

1. $\pi_{\bullet \lt n}\left(X(U) \to (im_{n}(f))(U)\right)$ are [[isomorphisms]];

1. $\pi_n\left(X(U) \to (im_{n}(f))(U)\to Y(U)\right)$ is the [[(epi,mono) factorization]] of $\pi_n(f(U))$;

1. $\pi_{\bullet \gt n}\left((im_{n}(f))(U) \to Y(U)\right)$ are [[isomorphisms]].

=--

+-- {: .proof}
###### Proof

Evalutation on [[stalks]] is a [[filtered colimit]] which preserves the [[finite limits]] and [[finite colimits]] that go into the definition of [[simplicial homotopy groups]]. Therefore the global conditions assumed on the simplicial homotopy groups imply that the same kind of conditions holds for the stalkwise homotopy groups. These are the [[categorical homotopy groups in an infinity-topos|categorical homotopy groups]] in $L_{lwhe} sPSh(C)_{loc}$. By [this prop.](n-truncated+object+of+an+infinity-category#RecognizngnTuncationOnSimplicialHomotopyGroups) and [this def.](n-connected+object+of+an+infinity-topos#Connectedness) we may recognize $n$-truncation of morphisms on categorical homotopy groups (using the assumption that $X$ and $Y$ are $k$-truncated for some $k$). Therefore the claim now follows from the stalkwise [[long exact sequence of homotopy groups]].

=--

In order to appeal to prop. \ref{nImageFactroizationModeledOnSimplicialPrsheaves} we are interested in explicit models for $n$-image factorization of morphisms of [[Kan complexes]]. The following gives such for the special case that the the morphism of Kan complexes is the image under the [[Dold-Kan correspondence]] of a [[chain map]] between [[chain complexes]].

+-- {: .num_remark #ChainComplexnPlusOneImageInDegreen}
###### Remark

Let $f_\bullet \colon V_\bullet \longrightarrow W_\bullet$
be a [[chain map]] between [[chain complexes]]

For $n \in \mathbb{N}$, consider the abelian group

$$
  (im_{n+1}(f))_n
    \;\coloneqq\;
  coker(\,
     ker(\partial_V) \cap ker(f_n)
     \to
     V_n
  \,)
$$


For the following it is helpful to think of this abelian group in the following equivalent ways.

Define an [[equivalence relation]] on $V_n$ by

$$
  \left(
     v_n \sim v'_n
  \right)
  \;\Leftrightarrow\;
  \left(
    (\partial_V v_n = \partial_V v'_n)
    \;\text{and}\;
    (f_n(v_n) = f_n(v'_n))
  \right)
  \,.
$$

Then

$$
  (im_{n+1}(f))_n \simeq V_n/_\sim
$$

is equivalently the set of [[equivalence classes]] of this equivalence relation, which inherits abelian group structure since the eqivalence relation is linear.

This is because the equivalence relation says equivalently that

$$
  \left(
     v_n \sim v'_n
  \right)
  \;\Leftrightarrow\;
  \left(
    v_n - v'_n \;\in\; ker(\partial_V) \cap ker(f_n)
  \right)
$$

and hence is generated under linearity by

$$
  \left(
     v_n \sim 0
  \right)
  \;\Leftrightarrow\;
  \left(
    v_n  \in ker(\partial_V) \cap ker(f_n)
  \right)
  \,.
$$

Moreover, notice that the [[Dold-Kan correspondence]]

$$
  DK
  \;\colon\;
  Ch_{\bullet \geq 0}
    \longrightarrow
  KanCplx
$$

factors through [[globe|globular]] [[strict omega-groupoids]] ([here](Dold-Kan+correspondence#GlobularAndCubical)). An [[n-morphism]] in the [[strict omega-groupoid]] $DK(V_\bullet)$ is of the form

$$
  (v_{n-1})
    \overset{\phantom{AA}v_n\phantom{AA}}{\longrightarrow}
  (v_{n-1} + \partial v_n)
  \,.
$$

In terms of these morphisms the [[equivalence relation]] above says that two of them are equivalent precisely if

1. they are "[[parallel morphisms]]" in that they have the same [[source]] and [[target]];

1. they have the same image under $f$ in the [[n-morphisms]] of  $DK(W_\bullet)$.


This suggests yet another equivalent way to think of $(im_{n+1}(f))_n$: it is the [[disjoint union]] over the [[target]] $(n-1)$-cells in $V_{n-1}$ of the images under $f$ of the sets of $n$-cells from zero to that target:

$$
  (im_{n+1}(f))_n
   \simeq
   \underset{v_{n-1} \in V_{n-1}}{\sqcup}
    \left\{
      f_n(v_n) \vert v_n \in V_n \,\text{and}\,\partial v_n = v_{n-1}
    \right\}
  \,.
$$

=--

+-- {: .num_prop #ImageFactorizationForChainComplexes}
###### Proposition

Let $f_\bullet \colon V_\bullet \longrightarrow W_\bullet$
be a [[chain map]] between [[chain complexes]] and let
$n \in \mathbb{N}$. Recall the abelian group
 $\underset{v_{n-1}}{\sqcup}\{f_n(v_n) \vert \partial v_n = v_{n-1}\}$ from remark \ref{ChainComplexnPlusOneImageInDegreen}.

The following [[diagram]] of [[abelian groups]]
[[commuting diagram|commutes]]:

$$
  \array{
    \vdots && \vdots && \vdots
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}
    \\
    V_{n+3}
      &\overset{f_{n+3}}{\longrightarrow}&
    W_{n+3}
      &\overset{=}{\longrightarrow}&
    W_{n+3}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}
    \\
    V_{n+2}
      &\overset{f_{n+2}}{\longrightarrow}&
    W_{n+2}
      &\overset{=}{\longrightarrow}&
    W_{n+2}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\mathrlap{ \partial_W  } }
     &&
    \downarrow^{\mathrlap{\partial_{W}}}
    \\
    V_{n+1}
      &\overset{f_{n+1}}{\longrightarrow}&
    \left\{
      w_{n+1} | \exists v_n :  \partial_W w_{n+1} = f_n(v_n), \partial_V v_n = 0,
    \right\}
      &\overset{}{\longrightarrow}&
    W_{n+1}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\partial_W}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}
    \\
    V_n
      &\overset{ (f_n, \partial_V) }{\longrightarrow}&
    \underset{v_{n-1}}{\sqcup}
    \left\{
      f_n(v_n) \vert \partial_V v_n = v_{n-1}
    \right\}
     &\overset{  }{\longrightarrow}&
    W_n
    \\
    \downarrow^{\mathrlap{\partial_V}}
    &&
    \downarrow^{\mathrlap{(f_n(v_n),\partial_V v_n) \mapsto \partial_V v_n}}
    &&
    \downarrow^{\mathrlap{\partial_W}}
    \\
    V_{n-1}
      &\overset{=}{\longrightarrow}&
    V_{n-1}
      &\overset{f_{n-1}}{\longrightarrow}&
    W_{n-1}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_W}}
    \\
    V_{n-2}
      &\overset{=}{\longrightarrow}&
    V_{n-2}
      &\overset{f_{n-2}}{\longrightarrow}&
    W_{n-2}
    \\
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_W}}
    \\
    \vdots && \vdots && \vdots
  }
$$


Moreover, the middle vertical sequence is a chain complex $im_{n+1}(f)_\bullet$, and hence the diagram gives a factorization of $f_\bullet$ into two chain maps

$$
  f_\bullet
   \;\colon\;
  V_\bullet \longrightarrow im_{n+1}(f)_\bullet \longrightarrow W_\bullet
  \,.
$$

Finally, this is a model for the [[n-image|(n+1)-image factorization]] of $f$ in that on [[homology groups]] the following holds:

1. $H_{\bullet \lt n}(V) \overset{\simeq}{\to} H_{\bullet \lt n}(im_{n+1}(f))$ are [[isomorphisms]];

1. $H_n(V) \to H_n(im_{n+1}(f)) \hookrightarrow H_n(W)$ is the [[image|image factorization]] of $H_n(f)$;

1. $H_{\bullet \gt n}(im_{n+1}(f)) \overset{\simeq}{\to} H_{\bullet \gt n}(W)$   are [[isomorphisms]].


=--

+-- {: .proof}
###### Proof (but check)

This follows by elementary and straightforward direct inspection.

=--

## Moduli of circle $n$-connections

+-- {: .num_defn #TruncatedDelgneComplexes}
###### Definition

For $p \in \mathbb{N}$ and $k \leq p+1$ write

$$
  \mathbf{B}^{p+1}U(1)_{conn^k}
  \coloneqq
  DK
  \left(
    U(1) \to \Omega^1 \to \Omega^2 \to \cdots \to \Omega^k \to 0 \to \cdots \to 0
  \right)
  \;\in\;
  sPSh(CartSp)
$$

for the [[simplicial presheaf]] which is the image under the [[Dold-Kan correspondence]] of the presheaf of chain complexes which is the [[Deligne complex]] starting with the presheaf represented by $U(1)$ in degree $p+1$ and truncated to the differential $k$-forms, as shown.

Since the $DK$ map sends surjections of chain complexes to [[Kan fibrations]],
the canonical projection maps yield a tower of objectwise [[Kan fibrations]] of the following form:

$$
  \mathbf{B}^{p+1}U(1)_{conn}
  =
  \mathbf{B}^{p+1}U(1)_{conn^{p+1}}
    \longrightarrow
  \mathbf{B}^{p+1}U(1)_{conn^{p}}
    \longrightarrow
  \mathbf{B}^{p+1}U(1)_{conn^{p-1}}
    \longrightarrow
  \mathbf{B}^{p+1}U(1)_{conn^1}
    \longrightarrow
  \mathbf{B}^{p+1}U(1)_{conn^0}
    =
  \mathbf{B}^{p+1}U(1)
  \,.
$$

=--

+-- {: .num_defn #ModuliOfnFormConnection}
###### Definition

For $\Sigma$ a [[smooth manifold]], write

$$
  (\mathbf{B}^p U(1)) \mathbf{Conn}(\Sigma)
  \in
  sPSh(CartSp)
$$

for the image under the [[Dold-Kan correspondence]] of the presheaf of chain complexes which to $U \in CartSp$  assigns the _vertical_ [[Cech cohomology|Cech]]-[[Deligne complex]] on $\Sigma \times U \to U$ in the given degree, i.e. the Cech-Deligne complex involving differential forms on $\Sigma \times U$ that have no leg along $U$, i.e. those in $\Omega^{\bullet,0}(\Sigma \times U)$.

=--

## Differential concretification on contractibles

We first consider differential concretification on geometrically contractible base spaces. Once this is established, then the general differential concretification follows simply by stackifying along the base space.

+-- {: .num_defn #DifferentialConcretificationForCirclenConnectionsOnContractible}
###### Definition
**(differential concretification for higher circle connections on contractibles)**

Let $\Sigma$ be a [[contractible topological space|contractible]] [[smooth manifold]].
For $p \in \mathbb{N}$ write

$$
  (\mathbf{B}^p U(1))\mathbf{Conn}_0(\Sigma)
    \coloneqq
  [\Sigma, \mathbf{B}^{p+1}U(1)]
$$

and then for $0 \leq k \leq p$ define [[induction|inductively]]

$$
  (\mathbf{B}^p U(1))\mathbf{Conn}_{k+1}(\Sigma)
   \coloneqq
  im_{p+1-k}
  \left(
    [\Sigma, \mathbf{B}(\mathbf{B}^p U(1))_{conn^{k+1}}]
      \longrightarrow
    \sharp [ \Sigma, \mathbf{B}(\mathbf{B}^p U(1))_{conn^{k+1}} ]
      \underset{\sharp[\Sigma, \mathbf{B}(\mathbf{B}^p U(1))_{conn^k}]}{\times^h}
    (\mathbf{B}^p U(1))\mathbf{Conn}_k(\Sigma)
  \right)
 \,.
$$


=--

+-- {: .num_lemma #DifferentialConcretificationFornConnectionsOnContractibles}
###### Lemma

Let $\Sigma$ be a [[contractible topological space|contractible]] [[smooth manifold]].  Then there is a weak equivalence

$$
  (\mathbf{B}^p U(1)) \mathbf{Conn}_{p+1}(\Sigma)
    \simeq
  (\mathbf{B}^p U(1)) \mathbf{Conn}(\Sigma)
  \,,
$$

from the inductively defined object from def. \ref{DifferentialConcretificationForCirclenConnectionsOnContractible} to the moduli object from def. \ref{ModuliOfnFormConnection}.

=--

+-- {: .proof}
###### Proof

By the assumption that $\Sigma$ is contractible, the Cech-direction of the Cech-Deligne double complex is trivial and so we have for all $U \in CartSp$ and $0 \leq k \leq p$ weak equivalences of the form

$$
  [\Sigma, \mathbf{B}^{p+1}U(1)_{conn^k}](U)
  \;\simeq\;
  DK\left(
    C^\infty(\Sigma \times U, U(1))
     \to
    \Omega^1(\Sigma \times U)
      \to
    \Omega^2(\Sigma \times U)
     \to
    \cdots
      \to
    \Omega^{p+1}(\Sigma \times U)
  \right)
$$

and

$$
  (\mathbf{B}^p U(1))\mathbf{Conn}(\Sigma)
    \simeq
  DK\left(
    C^\infty(\Sigma \times U, U(1))
     \to
    \Omega^{1,0}(\Sigma \times U)
     \to
    \Omega^{2,0}(\Sigma \times U)
      \to
    \cdots
      \to
    \Omega^{p+1,0}(\Sigma \times U)
  \right)
  \,.
$$


We claim now for all $k \leq p$ that

$$
  (\mathbf{B}^p U(1))\mathbf{Conn}_k(\Sigma)
    \simeq
  DK\left(
    C^\infty(\Sigma \times U, U(1))
     \to
    \Omega^{1,0}(\Sigma \times U)
     \to
    \cdots
     \to
    \Omega^{k,0}(\Sigma \times U)
     \to
    0
      \to
    \cdots
      \to
    0
  \right)
  \,.
$$

For $k = p$ this is the statement to be shown.
Hence we may now prove this by [[induction]].

It is manifestly true for $k = 0$. Hence suppose it is true for some $k \lt p$.  Observe then that

$$
  \sharp [\Sigma, \mathbf{B}^{p+1}U(1)_{conn^{k+1}}]
    \longrightarrow
  \sharp [\Sigma, \mathbf{B}^{p+1}U(1)_{conn^k}]
$$

is an objectwise Kan fibration, because so is $\mathbf{B}^{p+1}U(1)_{conn^{k+1}} \to \mathbf{B}^{p+1}U(1)_{conn^k}$ by def. \ref{TruncatedDelgneComplexes}, and both $[\Sigma,-]$ as well as $\sharp$ are right Quillen functors from $sPSh(C)$ with its global projective model structre to itself.

It follows ([this prop.](homotopy+pullback#HomotopyPullbackByOrdinaryPullback)) that the homotopy fiber product in question
is presented by the plain 1-categorical fiber product. Since $DK$ is right adjoint, this in turn is given by the degreewise fiber product of the corresponding chain complexes. By direct inspection this means that

$$
  \begin{aligned}
    &
    \sharp [ \Sigma, \mathbf{B}(\mathbf{B}^p U(1))_{conn_{k+1}} ]
      \underset{\sharp[\Sigma, \mathbf{B}(\mathbf{B}^p U(1))_{conn_k}]}{\times^h}
    (\mathbf{B}^p U(1))\mathbf{Conn}_k(\Sigma)
   \\
   & \simeq
   DK
   \left(
      C^\infty(\Sigma \times U, U(1))
        \to
      \Omega^{1,0}(\Sigma \times U)
        \to
      \cdots
        \to
      \Omega^{k,0}(\Sigma \times U)
        \to
      (\sharp \Omega^{k+1}(\Sigma \times -))(U)
        \to
      0
       \to
      \cdots
        \to
      0
   \right)
  \end{aligned}
$$

Hence we are now reduced to computing the $(p+1-k)$ image of

$$
  \array{
  DK
  (
    C^\infty(\Sigma \times U)
     &\to&
    \Omega^1(\Sigma \times U)
      &\to&
    \cdots
       &\to&
    \Omega^{k}(\Sigma \times U)
      &\to&
    \Omega^{k+1}(\Sigma \times U)
      &\to&
    0
      &\to&
    \cdots
      &\to&
    0
  )
  \\
    \downarrow
    &&
    \downarrow
    &&
    &&
    \downarrow
    &&
    \downarrow
    &&
    \downarrow
    &&
    &&
    \downarrow
  \\
   DK
   (
      C^\infty(\Sigma \times U, U(1))
        &\to&
      \Omega^{1,0}(\Sigma \times U)
        &\to&
      \cdots
        &\to&
      \Omega^{k,0}(\Sigma \times U)
        &\to&
      (\sharp \Omega^{k+1}(\Sigma \times -))(U)
        &\to&
      0
       &\to&
      \cdots
        &\to&
      0
   )
  }
$$

Observe that in degree $(p+1)-(k+1)$ the ordinary image is

$$
  im\left(
    \Omega^{k+1}(\Sigma \times U)
      \to
     (\sharp \Omega^{k+1}(\Sigma \times -))(U)
  \right)
   \simeq
  \Omega^{k+1,0}(\Sigma \times U)
$$

With this the induction follows by prop. \ref{nImageFactroizationModeledOnSimplicialPrsheaves} and prop. \ref{nImageFactorizationOnChainComplex}.

=--

## General differential concretification
 {#GeneralDifferentialConcretification}

+-- {: .num_defn #DifferentialConcretificationOfCirclenConnections}
###### Definition
**(differential concretification of moduli for higher connection)**

For $\Sigma$ a [[smooth manifold]], define for $p \in \mathbb{N}$

$$
  (\mathbf{B}^{p}U(1))
  \mathbf{Conn}_{p+1}(\Sigma)
    \;\simeq\;
  \underset{\longleftarrow}{\lim}^h_i
  \;
  (\mathbf{B}^p U(1)) \mathbf{Conn}_{p+1}(U_i)
$$

to be the [[homotopy limit]] over the differential concretifications from def. \ref{DifferentialConcretificationForCirclenConnectionsOnContractible} of contractibles $U_i$, for

$$
  \Sigma \simeq \underset{\longrightarrow}{\lim}_i^h U_i
$$

a presentation of $\Sigma$ as a homotopy colimit of contractible manifolds (e.g. the realization of the [[Cech nerve]] of a [[good open cover]]).

=--

+-- {: .num_prop}
###### Proposition

For $\Sigma$ a [[smooth manifold]], then the differential concretifiction of def. \ref{DifferentialConcretificationOfCirclenConnections} is equivalent to the moduli object from def. \ref{ModuliOfnFormConnection}:


$$
  (\mathbf{B}^p U(1)) \mathbf{Conn}_{p+1}(\Sigma)
    \simeq
  (\mathbf{B}^{p}U(1)) \mathbf{Conn}(\Sigma)
  \,.
$$

=--


+-- {: .proof}
###### Proof

Let $\Sigma \simeq \underset{\longrightarrow}{\lim}_i^h U_i$ be the realization of the Cech nerve of a good open cover. Then

$$
  \underset{\longleftarrow}{\lim}_i (\mathbf{B}^p  U(1))\mathbf{Conn}_{p+1}(U_i)
$$

is equivalently the image under DK of the corresponding Cech hypercomplex with coefficients in the presheaf of chain complexes $(\mathbf{B}^p  U(1))\mathbf{Conn}_{p+1}(-)$. By lemma \ref{DifferentialConcretificationFornConnectionsOnContractibles} this is the vertical Deligne complex, and hence the claim follows.

=--
