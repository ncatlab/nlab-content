## Field variations
 {#FieldVariations}

Given a [[field bundle]] as in def. \ref{FieldsAndFieldBundles} above, then we know what [[type]] of quantities the corresponding
[[field histories]] assign to a given spacetime point (a given [[event]]). Among all consistent such field histories, some are to qualify as those that "may occur in reality" if we think of the field theory as a means to describe parts of the [[observable universe]]. Moreover, if the reality to be described does not exhibit "action at a distance" then admissibility of its field histories should be determined over arbitrary small spacetime regions, in fact over the [[infinitesimal neighbourhood]] of any spacetime point (remark \ref{JetBundleInTermsOfSyntheticDifferentialGeometry} below). This means equivalently that the realized field histories should be those that satisfy a given _[[differential equation]]_, namely an [[equation]] between the [[partial derivatives]] of the field history at any spacetime point. This is called the _[[equation of motion]]_ of the field theory (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} below).

In order to formalize this, it is useful to first collect all the possible partial derivatives that a field history may have at any given point into one big space of "field derivatives at spacetime points". This collection is called the _[[jet bundle]]_ of the [[field bundle]], given as def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below.

Moving around in this space means to change the possible value of fields and their derivatives, hence to _vary_ the fields. Accordingly _[[variational calculus]]_ of fields is just [[differential calculus]] on the [[jet bundle]] of the [[field bundle]], this we consider in def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} below.

$\,$


+-- {: .num_defn #JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[jet bundle]] of a [[trivial vector bundle]] over [[Minkowski spacetime]])**

Given a [[field fiber]] [[super vector space]] $F = \mathbb{R}^{b\vert s}$ with [[linear basis]] $(\phi^a)$,
then for $k \in \mathbb{N}$ a natural number,  the _order-$k$ [[jet bundle]]_

$$
  \array{
    J^k_{\Sigma}( E )
    \\
    \downarrow^{\mathrlap{jb_k}}
    \\
    \Sigma
  }
$$

over [[Minkowski spacetime]] $\Sigma$ of the [[trivial vector bundle]]

$$
  E \coloneqq \Sigma \times F
$$

is the [[super Cartesian space]] (def. \ref{SuperCartesianSpace}) which is spanned by coordinate functions to be denoted as follows:

$$
  \left(
     (x^\mu)
     \,,\,
     (\phi^a )
     \,,\,
     ( \phi^a_{,\mu} )
     \,,\,
     ( \phi^a_{,\mu_1\mu_2} )
     \,,\,
     \cdots
     \,,\,
     ( \phi^a_{,\mu_1 \cdots \mu_k} )
     \,,\,
     \cdots
  \right)
$$

where the indices $\mu, \mu_1, \mu_2, \cdots$ range from 0 to $p$, while the index $a$ ranges from $1$ to $b$ for the
even field coordinates, and then from $b+1$ to $b+s$ for the odd-graded field coordinates and the lower indices are
symmetric:

$$
  \label{JetCoodinatesSymmetry}
  \phi^a_{\mu_1 \cdots \mu_{i} \cdots \mu_j \cdots \mu_k}
  \;=\;
  \phi^a_{\mu_1 \cdots \mu_{j} \cdots \mu_i \cdots \mu_k}
  \,.
$$

In terms of these coordinates the [[bundle]] [[projection]] map $jb_k$ is just the one that remembers the spacetime coordinates $x^\mu$ and forgets the values of the field $\phi^a$ and its derivatives $\phi_{\mu}$. Similarly there are intermediate projection maps

$$
  \array{
    \cdots
     &\overset{jb_{3,2}}{\longrightarrow}&
    J^{2}_\Sigma(E)
      &\overset{jb_{2,1}}{\longrightarrow}&
    J^1_\Sigma(E)
      &\overset{jb_{1,0}}{\longrightarrow}&
    E
    \\
    && &{}_{\mathllap{jb_2}}\searrow& {}^{\mathllap{jb_1}}\downarrow  &\swarrow_{\mathrlap{fb}}&
    \\
    && && \Sigma &&
  }
$$

given by forgetting coordinates with more indices.

The _infinite-order [[jet bundle]]_

$$
  J^\infty_\Sigma(E) \in SuperSmoothSet
$$

is the [[direct limit]] of [[super formal smooth sets|super smooth sets]] (def. \ref{SuperFormalSmoothSet}) over these finite order jet bundles. Explicitly this means that it is the [[smooth set]] which is defined
by the fact that a smooth function (a plot, by prop. \ref{SuperCartSpYpnedaLemma})

$$
  U \overset{f}{\longrightarrow} J^\infty_\Sigma(E)
$$

from some [[super Cartesian space]] $U$ is equivalently a system of ordinary smooth functions
into all the finite-order jet spaces

$$
  \left(
    U \overset{f_k}{\longrightarrow} J^k_\Sigma(E)
  \right)_{k \in \mathbb{N}}
  \,,
$$

such that this system is compatible with the
above projection maps, i.e. such that

$$
  \underset{k \in \mathbb{N}}{\forall} \left(
    jb_{k+1,k} \circ f_{k+1} = f_k
  \right)
  \phantom{AAAAAAA}
  \array{
    && && U &&
    \\
    && & {}^{\mathllap{f_2}}\swarrow&  {}_{\mathllap{f_1}}\downarrow  &\searrow^{f_0}&
    \\
    \cdots
     &\overset{jb_{3,2}}{\longrightarrow}&
    J^{2}_\Sigma(E)
      &\overset{jb_{2,1}}{\longrightarrow}&
    J^1_\Sigma(E)
      &\overset{jb_1}{\longrightarrow}&
    E
    \\
    && &{}_{\mathllap{jb_2}}\searrow& {}^{\mathllap{jb_1}}\downarrow  &\swarrow_{\mathrlap{fb}}&
    \\
    && && \Sigma &&
  }
$$

=--

The coordinate functions $\phi^a_{\mu_1 \cdots \mu_k}$ on a [[jet bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
are to be thought of as [[partial derivatives]] $\frac{\partial}{\partial x^{\mu_1}} \cdots \frac{\partial}{\partial x^{\mu_k}} \Phi^a$ of components $\Phi^a$ of would-be [[field histories]] $\Phi$. The power of the jet bundle is that it allows
to disentangle relations between would-be partial derivatives of field history components in themselves
from consideration of actual [[field histories]]. In traditional physics texts this is often done implicitly.
We may make it fully explit by the operation of _[[jet prolongation]]_ which reads in a [[field history]]
and records all its partial derivatives in the form of a section of the jet bundle:


+-- {: .num_defn #JetProlongation}
###### Definition
**([[jet prolongation]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) which happens to be a [[trivial vector bundle]]
over [[Minkowski spacetime]] as in example \ref{TrivialVectorBundleAsAFieldBundle}.

There is a  [[smooth function]] from the [[space of sections]] of $E$, the [[space of field histories]] (example \ref{SupergeometricSpaceOfFieldHistories}) to the space of sections of the [[jet bundle]] $J^\infty_\Sigma(E) \overset{jb^\infty}{\to} \Sigma$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) which records the field $\Phi$ and all its spacetimes [[derivatives]]:

$$
  \array{
    \Gamma_\Sigma(E)
      &\overset{j^\infty_\Sigma}{\longrightarrow}&
    \Gamma_\Sigma(J^\infty_\Sigma(E))
    \\
    (\Phi^a)
    &\mapsto&
    \left(
    \left( \Phi^a \right)
      \,,\,
      \left(  \frac{\partial \Phi^a}{\partial x^\mu}  \right)
      \,,\,
      \left( \frac{\partial^2 \Phi^a}{\partial x^{\mu_1} \partial x^{\mu_2}}  \right)
      \,,\,
      \cdots
    \right)
  }
  \,.
$$

This is called the operation of _[[jet prolongation]]_: $j^\infty_\Sigma(\Phi)$ is the jet prolongation of $\Phi$.

=--


+-- {: .num_remark #JetBundleInTermsOfSyntheticDifferentialGeometry}
###### Remark
**([[jet bundle]] in terms of [[synthetic differential geometry]])**

In terms of the [[synthetic differential geometry|infinitesimal geometry]] of [[formal smooth sets]]
(def. \ref{FormalSmoothSet}) the [[jet bundle]] $J^\infty_\Sigma(E) \overset{jb_\infty}{\to} \Sigma$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
of a [[field bundle]] $E \overset{fb}{\to}\Sigma$ has the following incarnation:

A [[section]] of the [[jet bundle]] over a point $x \in \Sigma$ of [[spacetime]] (an [[event]]),
is equivalently a section of the original [[field bundle]] over the [[infinitesimal neighbourhood]]
$\mathbb{D}_x$ of that point (example \ref{InfinitesimalNeighbourhood}):

$$
  \left\{
  \array{
     && J^\infty_\Sigma(E)
     \\
     & \nearrow & \downarrow^{\mathrlap{jb_\infty}}
     \\
     \{x\}
     &\hookrightarrow&
     \Sigma
  }
  \phantom{AA}
  \right\}
  \phantom{AA}
  \simeq
  \phantom{AA}
  \left\{
  \array{
    && E
    \\
    & {}^{\mathllap{}}\nearrow & \downarrow^{\mathrlap{fb}}
    \\
    \mathbb{D}_x &\hookrightarrow& \Sigma
  }
  \phantom{AA}
  \right\}
  \,.
$$

Moreover, given a [[field history]] $\Phi$, hence a [[section]] of the [[field bundle]],
then its [[jet prolongation]] $j^\infty(\Phi)$ (def. \ref{JetProlongation}) is that [[section]]
of the [[jet bundle]] which under the above identification is simply the restriction of
$\Phi$ to the [[infinitesimal neighbourhood]] of $x$:

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\Phi}}\nearrow & \downarrow^{\mathrlap{fb}}
    \\
    \Sigma & = & \Sigma
  }
  \phantom{AAAA}\overset{j^\infty_\Sigma}{\mapsto} \phantom{AAAA}
  \array{
    && J^\infty_\Sigma(E)
    \\
    & {}^{\mathllap{j^\infty_\Sigma(\Phi)}}\nearrow & \downarrow^{\mathrlap{jb_\infty}}
    \\
    \Sigma &=& \Sigma
  }
  \phantom{AAAA}
  \overset{(-)\vert_{\{x\}} }{\mapsto}
  \phantom{AAAA}
  \array{
    && E
    \\
    & {}^{\mathllap{\Phi\vert_{\mathbb{D}_x}}}\nearrow & \downarrow^{\mathrlap{fb}}
    \\
    \mathbb{D}_x &\hookrightarrow& \Sigma
  }
  \,.
$$

This follows with an argument as in example \ref{InfinitesimalNeighbourhoodsInTheRealLine}.

Hence in [[synthetic differential geometry]] we have:

_The jet of a section $\Phi$ at $x$ is simply the restriction of that section to the [[infinitesimal neighbourhood]] of $x$._

=--

([[schreiber:Synthetic variational calculus|Khavkine-Schreiber 17, section 3.3]])


So the canonical [[coordinates]] on the jet bundle are the spacetime-point-wise _possible_ values of fields and field derivates,
while the [[jet prolongation]] picks the actual collections of field derivatives that may occur for an actual field
history.

+-- {: .num_example #JetFaraday}
###### Example
**(universal [[Faraday tensor]]/[[field strength]] on [[jet bundle]])**

Consider the [[field bundle]] (def. \ref{FieldsAndFieldBundles}) of the [[electromagnetic field]] (example \ref{Electromagnetism})
over [[Minkowski spacetime]] $\Sigma$ (def. \ref{MinkowskiSpacetime}), i.e. the [[cotangent bundle]] $E = T^\ast \Sigma$ (def. \ref{Differential1FormsOnCartesianSpaces}) with jet coordinates
$((x^\mu), (a_\mu), (a_{\mu,\nu}), \cdots )$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}). Consider the functions on the [[jet bundle]] given by the linear combinations

$$
  \label{FaradayTensorJet}
  \begin{aligned}
    f_{\mu \nu}
    & \coloneqq
    a_{[\nu,\mu]}
    \\
    & \coloneqq
    \tfrac{1}{2}\left(
      a_{\nu,\mu} - a_{\mu,\nu}
    \right)
  \end{aligned}
$$

of the first order jets.

Then for an [[electromagnetism|electromagnetic]] [[field history]] ("[[vector potential]]"), hence a [[section]]

$$
  A \in \Gamma_\Sigma(T^\ast \Sigma) = \Omega^1(\Sigma)
$$

with components $A^\ast (a_\mu) = A_\mu$, its [[jet prolongation]] (def. \ref{JetProlongation})

$$
  j^\infty_\Sigma(A) \in \Gamma_\Sigma(J^\infty_\Sigma(T^\ast \Sigma))
$$

has components

$$
  \left(
    (A_\mu),
    \left(
      \frac{d A_\mu}{d x^\nu}
    \right)
    ,
    \cdots
  \right)
  \,.
$$

The [[pullback of differential forms|pullback]] of the functions $f_{\mu \nu}$ (eq:FaradayTensorJet)
along this jet prolongation are the components of the [[Faraday tensor]] of the field (eq:TensorFaraday):

$$
  \begin{aligned}
    \left(j^\infty_\Sigma(A)\right)^\ast(f_{\mu \nu})
    & =
    F_{\mu \nu}
    \\
    & =
    (d A)_{\mu \nu}
    \,.
  \end{aligned}
$$

More generally, for $\mathfrak{g}$ a [[Lie algebra]] and

$$
  E \coloneqq T^\ast \Sigma \otimes \mathfrak{g}
$$

the [[field bundle]] for [[Yang-Mills theory]] from example \ref{YangMillsFieldOverMinkowski}, consider the functions

$$
  f^\alpha_{\mu \nu}
  \;\in \;
  \Omega^{0,0}_\Sigma(E)
  =
  C^\infty(J^\infty_\Sigma(E))
$$

on the [[jet bundle]] given by

$$
  \label{YangMillsJetFieldStrengthMinkowski}
  \begin{aligned}
    f^\alpha_{\mu \nu}
    & \coloneqq
    \tfrac{1}{2}
    \left(
      a^\alpha_{\nu,\mu}
      -
      a^\alpha_{\mu,\nu}
      +
      \gamma^{\alpha}{}_{\beta \gamma}
      a^\beta_{\mu} a^\gamma_{\nu}
    \right)
  \end{aligned}
$$

where $(\gamma^\alpha{}_{\beta \gamma})$ are the structure constants of the Lie algebra as in (eq:LieAlgebraStructureConstants),
and where the square brackets around the indices denote anti-symmetrization.

We may call this the _universal [[Yang-Mills theory|Yang-Mills]] [[field strength]]_, being the
_[[covariant exterior derivative]]_ of the universal Yang-Mills field history.

For $\mathfrak{g} = \mathbb{R}$  the [[line Lie algebra]] and $k$ the canonical [[inner product]] on $\mathbb{R}$ the expression (eq:YangMillsJetFieldStrengthMinkowski) reduces to the universal [[Faraday tensor]] (eq:FaradayTensorJet) for
the [[electromagnetic field]] (example \ref{JetFaraday}).

For $A \in \Gamma_\Sigma(T^\ast \Sigma \otimes \mathfrak{g}) = \Omega^1(\Sigma,\mathfrak{g})$ a field history of
[[Yang-Mills theory]], hence a [[Lie algebra-valued differential 1-form]], then the value of this function on that field
are called the components of the _[[covariant exterior derivative]]_ or _[[field strength]]_

$$
  \begin{aligned}
    F_{\mu \nu}
     & \coloneqq
    A^\ast(D_{[\mu} a_{\nu]})
    \\
    & =
    (d_A A)_{\mu \nu}
  \end{aligned}
$$

=--



+-- {: .num_example #BFieldJetFaraday}
###### Example
**(universal [[B-field|B-]][[field strength]] on [[jet bundle]])**

Consider the [[field bundle]] (def. \ref{FieldsAndFieldBundles}) of the [[B-field]] (example \ref{BField})
over [[Minkowski spacetime]] $\Sigma$ (def. \ref{MinkowskiSpacetime}) with jet coordinates
$((x^\mu), (b_{\mu \nu}), (b_{\mu \nu,\rho}), \cdots )$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}). Consider the functions on the [[jet bundle]] given by the linear combinations

$$
  \label{BFieldFaradayTensorJet}
  \begin{aligned}
    h_{\mu_1 \mu_2 \mu_3}
      & \coloneqq
    \tfrac{1}{2}
      b_{[\mu_1 \mu_2, \mu_3]}
    \\
    & \coloneqq
     \tfrac{1}{6}
    \left(
      \underset{ \sigma \atop  \text{permutation} }{\sum}
      (-1)^{ {\vert \sigma \vert} }
      b_{\mu_{\sigma_1} \mu_{\sigma_2}, \mu_{\sigma_3}}
    \right)
    \\
    & =
    b_{\mu_1 \mu_2, \mu_3}
    +
    b_{\mu_2 \mu_3, \mu_1}
    +
    b_{\mu_3 \mu_1, \mu_2}
    \,,
  \end{aligned}
$$

where in the last step we used that $b_{\mu \nu} = - b_{\nu \mu}$.

=--

$\,$

While the [[jet bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) is not [[finite number|finite]] [[dimension|dimensional]],
reflecting the fact that there are arbitrarily high orders of spacetime derivatives of a field histories,
it turns out that it is only very "mildly [[infinite dimensional manifold|infinite dimensional]]"
in that
[[smooth  functions]] on jet bundles turn out to _locally_ depend on only finitely many of the jet coordinates
(i.e. only on a finite order of spacetime derivatives). This is the content
of the following prop. \ref{JetBundleIsLocallyProManifold}.

This reflects the _locality_ of [[Lagrangian field theory]] defined over [[jet bundles]]: If
functions on the jet bundle could depend on infinitely many jet coordinates, then by [[Taylor series]]
expansion of fields the function at one point over spacetime could in fact depend on field
history values at a _different_ point of spacetime. Such non-local dependence is ruled out by prop. \ref{JetBundleIsLocallyProManifold} below.

In practice this means that the situation is very convenient:

1. Any given [[local Lagrangian density]] (which will define a field theory, we come to this in def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below)
   will locally depend on some finite number $k$ of derivatives and may hence locally
   be treated as living on the ordinary manifold $J^k_\Sigma(E)$.

1. while at the same time all formulas (such as for the [[Euler-Lagrange equations]], def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) work uniformly
without worries about fixing a maximal order of derivatives.

+-- {: .num_prop #JetBundleIsLocallyProManifold}
###### Proposition
**([[jet bundle]] is a [[locally pro-manifold]])**

Given a [[jet bundle]] $J^\infty_\Sigma(E)$ as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime},
then a [[smooth function]] out of it

$$
  J^\infty_\Sigma(E) \longrightarrow X
$$

is such that around each point of $J^\infty_\Sigma(E)$ there is a [[neighbourhood]] $U \subset J^\infty_\Sigma(E)$
on which it is given by a function on a smooth function on $J^k_\Sigma(E)$ for some finite $k$.

=--

(see [Khavkine-Schreiber 17, section 2.2 and 3.3](locally+pro-manifold#KhavkineSchreiber17))


Example \ref{JetFaraday} shows that the [[de Rham differential]] (def. \ref{deRhamDifferential}) may be encoded in terms of
composing [[jet prolongation]] with a suitable function on the [[jet bundle]].
More generally, jet prolongation neatly encodes (possibly non-linear) [[differential operators]]:


+-- {: .num_defn #DifferentialOperator}
###### Definition
**([[differential operator]])**

Let $E_1 \overset{fb_1}{\to} \Sigma$ and $E_2 \overset{fb_2}{\to} \Sigma$
be two smooth [[fiber bundles]] over a common base space $\Sigma$. Then a
(possibly non-linear) _[[differential operator]]_ from [[sections]] of $E_1$
to sections of $E_2$ is a [[bundle morphism]] from the [[jet bundle]] of $E_1$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
to $E_2$:

$$
  \array{
    J^\infty_\Sigma(E_1)
      && \overset{\tilde D}{\longrightarrow} &&
    E_2
    \\
    & \searrow && \swarrow
    \\
    && \Sigma
  }
$$

or rather the function $D$ between the [[spaces of sections]] of these bundles
which this induces after [[composition]] with [[jet prolongation]] (def. \ref{JetProlongation}):

$$
  D
  \;\colon\;
  \Gamma_\Sigma(E_1)
    \overset{j^\infty_\Sigma}{\longrightarrow}
  \Gamma_\Sigma(J^\infty_\Sigma(E_1))
    \overset{\tilde D \circ (-)}{\longrightarrow}
  \Gamma_\Sigma(E_2)
  \,.
$$

If both $E_1$ and $E_2$ are [[vector bundles]] (def. \ref{VectorBundle})
so that their [[spaces of sections]] canonically are [[vector spaces]], then $D$
is called a _[[linear differential operator]]_ if it is a [[linear function]]
between these vector spaces. This means equivalently that $\tilde D$ is a [[linear function]]
in jet coordinates.

=--

+-- {: .num_defn #NormallyHyperbolicDifferentialOperator}
###### Definition
**([[normally hyperbolic differential operator]] on [[Minkowski spacetime]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) which is a [[vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}). Write $E^\ast \overset{}{\to} \Sigma$ for its [[dual vector bundle]] (def. \ref{DualVectorBundle})

A [[linear differential operator]] (def. \ref{DifferentialOperator})

$$
  P
    \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \Gamma_{\Sigma}(E^\ast)
$$

is of _second order_ if it has a coordinate expansion of the form

$$
  (P \Phi)_a
  \;=\;
  P^{\mu \nu}_{a b} \frac{\partial^2 \Phi^b}{\partial x^\mu \partial x^\nu}
  +
  P^\mu_{a b} \frac{\partial \Phi^b}{\partial x^\mu}
  +
  P_{a b} \Phi^b
$$

for $\{(P^{\mu \nu}_{a b}), (P^\mu_{a b}), P_{a b}\}$ [[smooth functions]] on $\Sigma$.

This is called a _[[normally hyperbolic differential operator]]_ if its _[[principal symbol]]_
$(P^{\mu \nu}_{a b})$ is proportional to the inverse [[Minkowski metric]] (prop./def. \ref{SpacetimeAsMatrices}) $(\eta^{\mu \nu})$,
i.e.

$$
  P^{\mu \nu}_{a b} = \eta^{\mu \nu} Q_{a b}
  \,.
$$

=--


+-- {: .num_defn #FormallyAdjointDifferentialOperators}
###### Definition
**([[formally adjoint differential operators]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]]
$\Sigma = \mathbb{R}^{p,1}$  (def. \ref{MinkowskiSpacetime}) and write $E^\ast \to \Sigma$ for the [[dual vector bundle]] (def. \ref{DualVectorBundle}).

Then a [[pair]] of [[linear differential operators]] (def. \ref{DifferentialOperator}) of the form

$$
  P, P^\ast
   \;\colon\;
  \Gamma_\Sigma(E_1)
    \longrightarrow
  \Gamma_\Sigma(E^\ast)
$$

are called _[[formally adjoint differential operators]]_ via a [[bilinear map|bilinear]] [[differential operator]]

$$
  \label{FormallyAdjointDifferentialOperatorWitness}
  K \;\colon\;
  \Gamma_\Sigma(E) \otimes \Gamma_\Sigma(E)
    \longrightarrow
   \Gamma_\Sigma(\wedge^{p} T^\ast \Sigma)
$$

with values in [[differential n-form|differential p-forms]] (def. \ref{DifferentialnForms})
such that for all [[sections]] $\Phi_1, \Phi_2 \in \Gamma_\Sigma(E)$ we have

$$
  \left(
    P(\Phi_1) \cdot \Phi_2
    -
    \Phi_1 \cdot P^\ast(\Phi_2)
  \right) dvol_\Sigma
   \;=\;
  d K(\Phi_1, \Phi_2)
  \,,
$$

where $dvol_\Sigma$ is the [[volume form]] on [[Minkowski spacetime]] (eq:MinkowskiVolume) and
where $d$ denoted the [[de Rham differential]] (def. \ref{deRhamDifferential}).

This implies by [[Stokes' theorem]] (prop. \ref{StokesTheorem}) in the case of [[compact support]] that
under an [[integral]] $P$ and $P^\ast$ are related via [[integration by parts]].


=--

([Khavkine 14, def. 2.4](Green+hyperbolic+partial+differential+equation#Khavkine14))


$\,$

+-- {: .num_remark #ReplacingBundleMorphismsByDifferentialOperators}
###### Remark
**([[variational calculus]] -- replacing plain [[bundle morphisms]] by [[differential operators]])**

Various concepts in [[variational calculus]], especially the concept of _[[evolutionary vector fields]]_ (def. \ref{EvolutionaryVectorField} below)
and _[[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge symmetries]]_ (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} below) follow from
concepts in plain [[differential geometry]] by systematically replacing
plain [[bundle morphisms]] by bundle morphisms out of the [[jet bundle]], hence by [[differential operators]] $\tilde D$
as in def. \ref{DifferentialOperator}.

=--

+-- {: .num_defn #VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[variational derivative]] and [[total derivative|total spacetime derivative]] -- the [[variational bicomplex]])**

On the [[jet bundle]] $J^\infty_\Sigma(E)$ of a [[trivial vector bundle|trivial]] [[super vector space]]-[[vector bundle]]  over [[Minkowski spacetime]] as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} we may consider its [[de Rham complex]] of
[[super differential forms]] (def. \ref{DifferentialFormOnSuperCartesianSpaces}); we write its [[de Rham differential]] (def. \ref{deRhamDifferential}) in boldface:

$$
  d \;\colon\; \Omega^\bullet(J^\infty_\Sigma(E)) \longrightarrow \Omega^{\bullet+1}(J^\infty_\Sigma(E))
  \,.
$$

Since the jet bundle unifies spacetime with field values, we want to decompose this differential into
a contribution coming from forming the [[total derivatives]] of fields along spacetime ("[[horizontal derivatives]]"), and
actual _variation_ of fields at a fixed spacetime point ("[[vertical derivatives]]"):


The  _[[total derivative|total spacetime derivative]]_ or  _[[horizontal derivative]]_ on $J^\infty_\Sigma(E)$
is the map on [[differential forms]] on the jet bundle of the form

$$
  d
  \;\colon\;
  \Omega^\bullet( J^\infty_\Sigma(E) )
  \longrightarrow
  \Omega^{\bullet+1}( J^\infty_\Sigma(E) )
$$

which on functions $f \colon J^\infty_\Sigma(E) \to \mathbb{R}$ (i.e. on 0-forms) is defined by

$$
  \label{SpacetimeTotalDerivativeOnSmoothFunctions}
  \begin{aligned}
    d f
    & \coloneqq
    \frac{d f}{d x^\mu}
    \mathbf{d} x^\mu
    \\
    & \coloneqq
    \left(
      \frac{\partial f}{\partial x^\mu}
      +
      \frac{\partial f}{\partial \phi^a}
      \phi^a_{,\mu}
      +
      \frac{ \partial f }{ \partial \phi^a_{,\nu}}
      \phi^a_{,\nu \mu }
      +
      \cdots
    \right)
    \mathbf{d} x^\mu
  \end{aligned}
$$

and extended to all forms by the graded [[Leibniz rule]], hence  as a nilpotent [[derivation]] of degree +1.

The  _[[variational derivative]]_ or _[[vertical derivative]]_

$$
  \label{VariationalDerivative}
  \delta
  \;\colon\;
  \Omega^\bullet( J^\infty_\Sigma(E) )
  \longrightarrow
  \Omega^{\bullet+1}( J^\infty_\Sigma(E) )
$$

is what remains of the full [[de Rham differential]] when the total spacetime derivative ([[horizontal derivative]]) is subtracted:

$$
  \label{VerticalDerivative}
  \delta \coloneqq \mathbf{d} - d
  \,.
$$

We may then extend the [[horizontal derivative]] from functions on the jet bundle to all
[[differential forms]] on the jet bundle by declaring that

$$
  d \circ \mathbf{d} \;\coloneqq\; - \mathbf{d} \circ d
$$

which by (eq:VerticalDerivative) is equivalent to

$$
  \label{HorizontalAndVerticalDerivativeAnticommute}
  d \circ \;\delta\; = - \delta \circ d
  \,.
$$

For example

$$
  \begin{aligned}
    d \delta \phi
    & =
    - \delta d  \phi
    \\
    & =
    - \delta \left( \phi_{,\mu} d x^\mu \right)
    \\
    & = - \delta \phi_{,\mu} \wedge d x^\mu
    \,.
  \end{aligned}
$$


This defines a bigrading on the [[de Rham complex]] of $J^\infty_\Sigma(E)$, into horizontal degree $r$ and vertical degree $s$

$$
  \Omega^\bullet\left( J^\infty_\Sigma(E) \right)
  \;\coloneqq\;
  \underset{r,s}{\oplus} \Omega^{r,s}(E)
$$

such that the horizontal and vertical derivative increase horizontal or vertical degree, respectively:

$$
  \label{VariationalBicomplexDiagram}
  \array{
     C^\infty(J^\infty_\Sigma(E)) = & \Omega^{0,0}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{1,0}_\Sigma(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{2,0}_\Sigma(E)
       &\overset{d}{\longrightarrow}&
     \cdots
       &\overset{d}{\longrightarrow}&
     \Omega^{p+1,0}_\Sigma(E)
     \\
     & \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}}
     && \cdots && \downarrow^{\mathrlap{\delta}}
     \\
     &
     \Omega^{0,1}_\Sigma(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{1,1}_\Sigma(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{2,1}_\Sigma(E)
       &\overset{d}{\longrightarrow}&
     \cdots
       &\overset{d}{\longrightarrow}&
     \Omega^{p+1,1}_\Sigma(E)
     \\
     & \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}}
     && \cdots && \downarrow^{\mathrlap{\delta}}
     \\
     &
     \Omega^{0,2}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{1,2}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{2,2}(E)
       &\overset{d}{\longrightarrow}&
     \cdots
       &\overset{d}{\longrightarrow}&
     \Omega^{p+1,2}_\Sigma(E)
     \\
     & \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}}
     && \cdots && \downarrow^{\mathrlap{\delta}}
     \\
     & \vdots && \vdots && \vdots
  }
  \,.
$$

This is called the _[[variational bicomplex]]_.

Accordingly we will refer to the differential forms on the jet bundle often as _variational differential forms_.

=--

$\,$

**[[derivatives]] on [[jet bundle]]**

| def.  | symbols |  name in physics | name in mathematics |
|--|--|---|--|
| def. \ref{DifferentialFormOnSuperCartesianSpaces} | $\; \mathbf{d}$ | [[de Rham differential]]  | [[de Rham differential]] |
| \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}  | $\; d \coloneqq d x^\mu \frac{d}{d x^\mu}$ | [[total derivative|total spacetime derivative]]   | [[horizontal derivative]]  |
| \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} | $ \; \frac{d}{d x^\mu} \coloneqq \frac{\partial}{\partial x^\mu} +  \phi^a_{,\mu} \frac{\partial}{\partial \phi^a}  + \cdots $ | [[total derivative|total spacetime derivative]] <br/> along $\partial_\mu$  |  [[horizontal derivative]] <br/> along $\partial_\mu$ |
| \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} | $\; \delta \coloneqq \mathbf{d} - d$ | [[variational derivative]]  | [[vertical derivative]] |
| \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}  | $\; \delta_{EL} \mathbf{L} \coloneqq \mathbf{d}\mathbf{L} + d \Theta_{BFV}$ | [[Euler-Lagrange variational derivative|Euler-Lagrange variation]]  | [[Euler-Lagrange operator]] |
| \ref{BVComplexOfOrdinaryLagrangianDensity} | $\; s_{BV}$  | [[BV-differential]]  |  [[Koszul complex|Koszul differential]]  |
| \ref{LocalOffShellBRSTComplex} | $\; s_{BRST} $ | [[BRST differential]] |  [[Chevalley-Eilenberg complex|Chevalley-Eilenberg differential]]  |
| \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm} | $\; s $ | [[BV-BRST differential]] |  [[Chevalley-Eilenberg complex|Chevalley-Eilenberg]]-[[Koszul-Tate complex|Koszul-Tate differential]]  |
| \ref{BVVariationalBicomplex} | $\; s - d $ | [[local BV-BRST differential]] |   |
$\,$

+-- {: .num_example #BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}
###### Example
**(basic facts about [[variational calculus]])**

Given the jet bundle of a [[field bundle]] as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}, then
in its [[variational bicomplex]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
we have the following:

* The spacetime [[total derivative]] ([[horizontal derivative]]) of a spacetime coordinate function $x^\mu$
  coincides with its ordinary de Rham differential

  $$
    \begin{aligned}
      d x^\mu
      & =
      \frac{\partial x^\mu}{ \partial x^\nu} \mathbf{d}x^\nu
      \\
      & = \mathbf{d} x^\mu
    \end{aligned}
  $$

  which hence is a horizontal 1-form

  $$
    \mathbf{d}x^\mu \;\in\; \Omega^{1,0}_\Sigma(E)
    \,.
  $$

* Therefore the variational derivative ([[vertical derivative|vertical derivative]]) of a spacetime coordinate function vanishes:

  $$
    \label{VariationalDerivativeOfSpacetimeCoordinateVanishes}
    \delta x^\mu = 0
    \,,
  $$

  reflective the fact that $x^\mu$ is not a field coordinate that could be varied.

* In particular the given [[volume form]] on $\Sigma$ gives a horizontal $p+1$-form on the jet bundle,
  which has the same coordinate expression (and which we denote by the same symbol)

  $$
    dvol_\Sigma =  d x^0 \wedge d x^1 \wedge \cdots \wedge d x^p
     \;\in\;
    \Omega^{p+1,0}
    \,.
  $$

* Generally any horizontal $k$-form is of the form

  $$
    f_{\mu_1 \cdots \mu_k} d x^{\mu_1} \wedge \cdots \wedge d x^{\mu_k}
    \;\in\;
    \Omega^{k,0}_{\Sigma}(E)
  $$

  for

  $$
    f_{\mu_1 \cdots \mu_k} = f_{\mu_1 \cdots \mu_k}\left((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots\right)
    \in C^\infty(J^\infty_\Sigma(E))
  $$

  any smooth function of the spacetime coordinates and the field coordinates (locally depending only on a finite
  order of these, by prop. \ref{JetBundleIsLocallyProManifold}).

* In particular every horizontal $(p+1)$-form $\mathbf{L} \in \Omega^{p+1,0}(E)$ is proportional to the
  above volume form

  $$
    \mathbf{L} = L \, dvol_\Sigma
  $$

  for $L = L((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots)$ some smooth function that may depend on all the
  spacetime and field coordinates.

* The spacetimes [[total derivatives]] /horizontal derivatives) of the variational derivative (vertical derivative) $\delta \phi$ of a field variable is the differential 2-form of horizontal degree 1 and vertical degree 1 given by

  $$
    \begin{aligned}
      d (\delta \phi^a)
      & =
      -
      \delta (d \phi_a)
      \\
      & =
      - (\delta \phi^a_{,\mu}) \wedge \mathbf{d} x^\mu
    \end{aligned}
    \,.
  $$

  In words this says that "the spacetime derivative of the variation of the field is the variation of its spacetime derivative".

=--

The following are less trivial properties of variational differential forms:

+-- {: .num_prop #PullbackAlongJetProlongationIntertwinesHorizontalDerivative}
###### Proposition
**([[pullback of differential forms|pullback]] along [[jet prolongation]] compatible with [[total derivative|total spacetime derivatives]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{FieldsAndFieldBundles}),
with induced [[jet bundle]] $J^\infty_\Sigma(E)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then for $\Phi \in \Gamma_\Sigma(E)$ any field history, the [[pullback of differential forms]] (def. \ref{PullbackOfDifferentialForms})

$$
  j^\infty_\Sigma(\Phi)^\ast
   \;\colon\;
  \Omega^\bullet(J^\infty_\Sigma(E))
    \longrightarrow
  \Omega^\bullet(\Sigma)
$$

along the [[jet prolongation]] of $\Phi$ (def. \ref{JetProlongation})

1. intertwines the [[de Rham differential]] on [[spacetime]] (def. \ref{Differential1FormsOnCartesianSpaces}) with the [[total spacetime derivative]] ([[horizontal derivative]]) on the [[jet bundle]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

   $$
     d \circ j^\infty_\Sigma(\Phi)^\ast
     \;=\;
     j^\infty_\Sigma(\Phi)^\ast \circ d
     \,.
   $$

1. annihilates all [[vertical differential forms]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

   $$
     j^\infty_\Sigma(\Phi)^\ast\vert_{\Omega^{r, \geq 1}_\Sigma(E)} = 0
     \,.
   $$

=--

+-- {: .proof}
###### Proof

The operation of [[pullback of differential forms]] along any [[smooth function]] intertwines the full [[de Rham differentials]]
(prop. \ref{PullbackOfDifferentialForms}). In particular we have that

$$
  d \circ j^\infty_\Sigma(\Phi)^\ast
  =
  j^\infty_\Sigma(\Phi)^\ast \circ \mathbf{d}
  \,.
$$

This means that the second statement immediately follows from the
first, by definition of the variational (vertical) derivative as the difference between
the full de Rham differential and the horizontal one:

$$
  \begin{aligned}
    j^\infty_\Sigma(\Phi)^\ast \circ \delta
    & =
    j^\infty_\Sigma(\Phi)^\ast \circ (\mathbf{d} - d)
    \\
    & =
    (d - d) \circ j^\infty_\Sigma(\Phi)^\ast
    \\
    & =
    0
  \end{aligned}
$$

It remains to see the first statement:

Since the [[jet prolongation]] $j^\infty_\Sigma(\Phi)$ preserves the spacetime coordinates $x^\mu$
(being a [[section]] of the [[jet bundle]]) it is immediate that the claimed relation
is satisfied on the
horizontal [[linear basis|basis]] 1-forms $\mathbf{d}x^\mu = d x^\mu$ (example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}):

$$
  d j^\infty_\Sigma(\Phi)^\ast( \mathbf{d}x^\mu )
  =
  d^2 x^\mu = 0
  \phantom{AAAAA}
  j^\infty_\Sigma(\Phi)^\ast d \mathbf{d} x^\mu
  =
  j^\infty_\Sigma(\Phi)^\ast d^2 x^\mu
  \,.
$$

Therefore it finally remains only to check the first statement on smooth functions (0-forms).
So let

$$
  f
    =
  f\left(
    (x^\mu)
    \,,\,
    (\phi^a)
    \,,\,
    ( \phi^a_{,\mu} )
    \,,\,
    \cdots
  \right)
$$

be a smooth function on the jet bundle. Then by the [[chain rule]]

$$
  \begin{aligned}
    d j^\infty_\Sigma(\Phi)^\ast
    f\left(
      (x^\mu)
      \,,\,
      (\phi^a)
      \,,\,
      ( \phi^a_{,\mu} )
      \,,\,
      \cdots
    \right)
    & =
    d
    f\left(
      (x^\mu)
      \,,\,
      (\Phi^a)
      \,,\,
      \left(  \frac{\partial \Phi^a}{\partial x^\mu} \right)
      \,,\,
      \cdots
    \right)
    \\
    & =
    \left(
      \frac{\partial f}{\partial x^\mu}
      +
      \frac{\partial f}{\partial \phi^a}
      \frac{\partial \Phi^a}{\partial x^\mu}
      +
      \frac{\partial f}{\partial \phi^a_{,\nu}}
      \frac{\partial^2 \Phi^a}{\partial x^\nu \partial x^\mu}
      +
      \cdots
    \right)
    d x^\mu
  \end{aligned}
$$

That this is equal to $j^\infty_\Sigma(\Phi)^\ast d f$ follows by the very definition
of the total spacetime derivative of $f$ (eq:SpacetimeTotalDerivativeOnSmoothFunctions).


=--


+-- {: .num_prop #HorizontalVariationalComplexOfTrivialFieldBundleIsExact}
###### Proposition
**([[horizontal variational complex]] of [[trivial vector bundle|trivial]] [[field bundle]] is [[exact sequence|exact]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] which is a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}). Then the [[chain complex]] of [[horizontal differential forms]] $\Omega^{s,0}_\Sigma(E)$
with the [[total spacetime derivative]] ([[horizontal derivative]]) $d$ (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})

$$
  \label{ExactSequenceTotalSpacetimeDerivative}
  \mathbb{R}
    \overset{}{\hookrightarrow}
  \Omega^{0,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
  \Omega^{1,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
  \Omega^{2,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
    \cdots
    \overset{d}{\longrightarrow}
  \Omega^{p,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
  \Omega^{p+1,0}_\Sigma(E)
$$

is [[exact sequence|exact]]: for all $0 \leq s \leq p$ the [[kernel]] of $d$ coincides with the [[image]] of $d$
in $\Omega^{s,0}_\Sigma(E)$.

More explicitly, this means that not only is every horizontally exact differential form $\omega = d \alpha$ horizontally closed
$d \omega = 0$ (which follows immediately from the fact that we have a [[cochain complex]] in the first place, hence that $d^2 = 0$),
but, conversely, if $\omega \in \Omega^{0 \leq s \leq p,0}_\Sigma(E)$ satisfies $d \omega = 0$, then there exists
$\alpha \in \Omega^{s-1,0}_\Sigma(E)$ with $\omega = d \alpha$.

=--

(e.g. [Anderson 89, prop. 4.3](variational+bicomplex#Anderson89))

We will encounter the extension of the [[exact sequence]] (eq:ExactSequenceTotalSpacetimeDerivative) further steps to the right below in example \ref{TrivialLagrangianDensities}.


$\,$

This concludes our discussion of [[variational calculus]] on the [[jet bundle]] of the [[field bundle]].
In the [next chapter](#Lagrangians) we apply this to [[Lagrangian densities]] on the [[jet bundle]], defining [[Lagrangian field theories]].
