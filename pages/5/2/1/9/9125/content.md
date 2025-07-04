

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


>  This entry is about the notion in [[physics]] in the sense of [[field theory]] ([[classical field theory|classical]]/[[quantum field theory]]). For the different notion of the same name in [[algebra]] see at _[[field]]_.


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In fundamental [[physics]] the basic entities that are being described are called _fields_, as they appear in the terms _[[classical field theory]]_ and _[[quantum field theory]]_.

### General

The basic example that probably gives the whole concept its name is the [[electric field]] and the [[magnetic field]] in the [[theory (physics)|theory]] of [[electromagnetism]]: if we fix a [[coordinate chart]] of [[spacetime]], then the [[electromagnetic field]] splits into the [[electric field]] and the [[magnetic field]] which are both modeled by a _[[vector field]]_, traditionally denoted $\vec E$ and $\vec B$, respectively, on this coordinate chart. The value $\vec E(x)$ of the vector field at a given point of spacetime is a [[vector]] that expresses the magnitude and direction of the electric [[force]] that is exerted on an [[electric charge|electrically charged]] [[particle]] at $x$. 

In fact more fundamentally, if we do not specify a [[coordinate chart]], then the [[electromagnetic field]] is not in fact represented by two vector fields. Rather, its [[field strength]] is represented by a [[differential 2-form]], hence a [[tensor field]] of rank $(0,2)$, but the the whole field as such is not a tensor field, but is a [[cocycle]] of degree-2 in [[ordinary differential cohomology]]: a [[circle n-bundle with connection|circle bundle with connection]].

Or for instance the field of [[gravity]] if modeled as a [[pseudo-Riemannian metric]] is a [[tensor field]] of rank $(2,0)$ -- but subject to the constraint that this be pointwise non-degenerate. More fundamentally the field of gravity is instead a [[vielbein field]].

Similar statements hold for all [[forces]] of nature, such as the force of [[gravity]] and the [[weak nuclear force]] and [[strong nuclear force]]: a configuration of these is mathematically modeled by [[connection on a bundle|connections]]. Their [[field strengths]] are rank $(0,2)$-tensor fields.

The [[electromagnetic field]] and the field of [[gravity]] are the physical fields that historically gave rise to what is now called _[[classical field theory]]_. But it turns out that fundamentally, in [[quantum physics]], also all [[matter]] in physics is constituted by fields in a similar sense. Specifically, where [[force]] fields in physics are usually [[connection on a bundle|connections on a bundle]], matter fields are [[sections]] of [[associated bundles]]. 

Field theory was originally discovered as a [[theory (physics)|theory]] of fields on _[[spacetime]]_. But also the [[physical system]] consisting of a single [[particle]] propagating in a _fixed_ [[spacetime]] $X$ is described by a field theory. In this case the field is not defined on spacetime, but on the abstract _[[worldline]]_ of the particle, say the _[[real line]]_ $\mathbb{R}$. A configuration of the system, namely a [[trajectory]] of the particle, is then a [[smooth function]] $\phi \;\colon\; \mathbb{R}\to X$. This function may be regarded as a _field_ on the [[worldline]] and is then called a _[[sigma-model]]_ field. The [[quantum mechanics]] of a single particle may be equivalently thought of as a [[quantum field theory]] on the 1-dimensional [[worldline]] of the particle.

This perspective generalizes. Next one can consider fields on 2-dimensional [[surfaces]] $\Sigma_2$ which again are given by maps into some [[spacetime]] $X$. The corresponding 2-dimensional [[sigma-model]] [[quantum field theory]] is then said to describe not a particle but a _[[string]]_ propagating in spacetime, defined on the _[[worldsheet]]_ $\Sigma_2$, replacing the [[worldline]] of the particle. For $\Sigma$ of dimension 3 one accordingly speaks of the _[[worldvolume]]_ of a [[membrane]] and then for $\Sigma$ of general dimension here one speaks of the _[[worldvolume]]_ of a _[[brane]]_. 

But there is no fundamental distinction between physical fields on spaces that are interpreted as [[spacetimes]] and those that are interpreted as [[worldvolumes]] of objects propagating _in_ a fixed spacetime. In general these notions mix. For instance the full description of [[relativistic particles]] and [[relativistic strings]] involves a field that is really a field of [[gravity]] on the [[worldvolume]]. Conversely, [[theory (physics)|theories]] on [[spacetimes]] that arise by [[Kaluza-Klein compactification]] of higher dimensional theories typically have "[[scalar field|scalar moduli fields]]" that used to be components of the field of [[gravity]] in higher dimensions but now after compactifications become maps into some auxiliary [[target space]], hence again _[[sigma-model]]_ fields.



### A first idea of quantum fields
 {#AFirstIdeaOfQuantumFields}

We introduce here the basic concepts of _[[Lagrangian field theory]]_, first for [[prequantum field theory]] and then for its [[deformation quantization]] to [[perturbative quantum field theory]].

In full beauty these concepts are extremely general; but in this section the aim is to give a first good idea of the subject, and therefore we present for the moment only a restricted setup, notably assuming that [[spacetime]] is [[Minkowski spacetime]], that the [[field bundle]] (see below) is an ordinary and [[trivial bundle|trivial]] [[fiber bundle]] and that all fields are [[boson|bosonic]].

This does subsume what is considered in most traditional texts on the subject. In subsequent sections we will eventually discuss more general situations, notably we will eventually allow spacetime to be any [[globally hyperbolic Lorentzian manifold]] and the [[field bundle]] to be an super [[infinity-Lie algebroid]]. This is sufficient generality to capture the established perturbative [[BV formalism|BRST-BV quantization]]
of [[fermions]] coupled to [[gauge fields]] [[AQFT on curved spacetime|on curved spacetimes]].

Throughout we use the case of the real [[scalar field]] as an illustrative running example, which we develop alongside with the theory. The discussion of other [[field (physics)|field]] species that are of more genuine interest in applications is postponed to their dedicated sections below.


#### Spacetime

Throughout, let

$$
  p \in \mathbb{N}
$$

be a [[natural number]] and write

$$
  \Sigma \coloneqq \mathbb{R}^{p,1} \coloneqq (\mathbb{R}^{p+1}, \eta)
$$

for [[Minkowski spacetime]] of [[dimension]] $p+1$, hence for the [[smooth manifold]] which is the [[Cartesian space]] $\mathbb{R}^{p+1}$ of dimension $p+1$ equipped with the [[left invariant differential form|constant]] [[pseudo-Riemannian metric]] $\eta$ which at the origin is given by the standard [[quadratic form]] of [[signature of a quadratic form|signature]]

$$
  (-, +, \cdots, +)
$$

in terms of the canonical [[coordinate functions]]

$$
  x^k \;\colon\; \mathbb{R}^{p+1} \longrightarrow \mathbb{R}
$$

which we index starting at zero: $(x^k)_{k = 0}^p$.

We write

$$
  dvol_\Sigma
   \;\coloneq\;
  d x^0 \wedge d x^1 \wedge \cdots \wedge d x^p
  \in \Omega^{p+1}(\mathbb{R}^{p,1})
$$

for the induced [[volume form]], and we call

$$
  d x^0 \in \Omega^1(\Sigma)
$$

the canonical representative of the canonical [[time orientation]] on Minkowski spacetime.


#### Fields

A _[[field (physics)|field]] configuration_ on a given [[spacetime]] $\Sigma$ is meant to be some kind of [[quantity]] assigned to each point of spacetime (each [[event]]), such that this assignment varies smoothly with spacetime points. For instance an _[[electromagnetic field]]_ configuration is at each point of spacetime a collection of [[vectors]] that encode the direction in which a [[charged particle]] passing through that point will feel a [[force]] (the [[Lorentz force]]).

This is readily formalized: If

$$
  F \in SmthMfd
$$

is the [[smooth manifold]] of "values" that the given kind of field may take at any spacetime point, then a field configuration $\Phi$ is modeled as a [[smooth function]] from spacetime to this space of values:

$$
  \Phi
    \;\colon\;
   \Sigma
     \longrightarrow
   F
  \,.
$$

It will be useful to unify spacetime and the space of field values into a single space, the [[Cartesian product]]

$$
  E \;\coloneqq\; \Sigma \times F
$$

and to think of this equipped with the [[projection]] map onto the first factor as a [[fiber bundle]] of spaces of field values over spacetime


$$
  \array{
     E &\coloneqq& \Sigma \times F
     \\
     {}^{\mathllap{fb}}\downarrow & \swarrow_{\mathrlap{pr_1}}
     \\
     \Sigma
  }
  \,.
$$

This is then called the _[[field bundle]]_, which specifies the kind of values that the given field species may take at any point of spacetime. Since the space $F$ of field values is the [[fiber]] of this [[fiber bundle]], it is sometimes also called the _[[field fiber]]_.

+-- {: .num_defn}
###### Definition
**(fields)**

Given a [[spacetime]] $\Sigma$ and a [[field bundle]] $\array{E \\ \downarrow^{\mathrlap{fb}} \\ \Sigma }$,
then a _[[field (physics)|field]] configuration_ (of type specified by this field bundle)
is a _smooth [[section]]_ of this [[bundle]], namely a [[smooth function]] of the form
$\Phi \colon \Sigma \longrightarrow E$ such that composed with the [[projection]] map it is the [[identity function]], i.e. such that $fb \circ \Phi = id$, or, diagrammatically, such that

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\Phi}}\nearrow & \downarrow^{\mathrlap{fb}}
    \\
    \Sigma & = & \Sigma
  }
  \,.
$$

The _field [[configuration space]]_ is the [[smooth set|smooth]] [[space of sections|space of all these]], to be denoted

$$
  \Gamma_\Sigma(E) \in SmoothSet
  \,.
$$

This is the [[set]] of all field configurations $\Phi$ as above, and it is equipped with the
structure of a [[smooth set]] by declaring that a _smooth family_ of field configurations,
parameterized over any [[Cartesian space]] $U$ is a smooth function

$$
  \array{
    U \times \Sigma &\overset{\Phi_{(-)}(-)}{\longrightarrow}& E
    \\
    (u,x) &\mapsto& \Phi_u(x)
  }
$$

such that for each $u \in U$ we have $p \circ \Phi_{u}(-) = id_\Sigma$, i.e.

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\Phi_{(-)}(-)}}\nearrow & \downarrow^{\mathrlap{fb}}
    \\
    U \times \Sigma &\underset{pr_2}{\longrightarrow}& \Sigma
  }
  \,.
$$



=--

+-- {: .num_example #TrivialVectorBundleAsAFieldBundle}
###### Example
**([[trivial vector bundle]] as a [[field bundle]])**

In applications the [[field fiber]] $F$ is often a [[finite number|finite]] [[dimension|dimensional]] [[Euclidean space]] and equipped with the structure of a [[vector space]]. In this case the trivial field bundle with fiber $F$ is of course a _[[trivial vector bundle|trivial]] [[vector bundle]]_.

Choosing any [[linear basis]] $(\phi^a)_{a = 1}^s$ of the field fiber, then over [[Minkowski spacetime]] we have canonical [[coordinates]] on the total space of the field bundle

$$
  ( (x^\mu)_{\mu = 0}^p, ( \phi^a )_{a = 1}^s )
  \,.
$$

=--


+-- {: .num_example #RealScalarFieldBundle}
###### Example
**([[real scalar field]])**

If $\Sigma$ is a [[spacetime]] and if

$$
  F \coloneqq \mathbb{R}
$$

is simply the [[real line]], then the corresponding trivial [[field bundle]]

$$
  \array{
    \Sigma \times \mathbb{R}
    \\
    {}^{\mathllap{pr_1}}\downarrow
    \\
    \Sigma
  }
$$

is the _[[trivial fiber bundle|trivial]] [[real line bundle]]_ (a special case of example \ref{TrivialVectorBundleAsAFieldBundle}) and the corresponding [[field (physics)|field]] is called the _[[real scalar field]]_ on $\Sigma$. A configuration of this field is simply a [[smooth function]] on $\Sigma$ with values in the [[real numbers]]:

$$
  \Gamma_\Sigma(\Sigma \times \mathbb{R})
    \;\simeq\;
  C^\infty(\Sigma)
  \,.
$$

=--

#### Field variations

Given a [[field bundle]] as above, we know what type of quantities the corresponding fields assign to a given spacetime point. Among all consistent such field configurations, some are to qualify as those that "may occur in reality" if we think of the field theory as a means to describe parts of the [[observable universe]]. Moreover, if the reality to be described does not exhibit "action at a distance" then admissibility of its field configurations should be determined over arbitrary small spacetime regions, in fact over the [[infinitesimal neighbourhood]] of any point. This means equivalently that the realized field configurations should be those that satisfy a specific _[[differential equation]]_, hence an [[equation]] between the value of its [[derivatives]] at any spacetime point.

In order to formalize this, it is useful to first collect all the possible derivatives that a field may have at any given point into one big space of "field derivatives at spacetime points". This collection is called the _[[jet bundle]]_ of the [[field bundle]], given as def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below.

Moving around in this space means to change the possible value of fields and their derivatives, hence to _vary_ the fields. Accordingly _[[variational calculus]]_ is just [[differential calculus]] on a [[jet bundle]], this we consider in def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} below.


+-- {: .num_defn #JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[jet bundle]] of a [[trivial vector bundle]] over [[Minkowski spacetime]])**

Given a [[field fiber]] [[vector space]] $F = \mathbb{R}^s$ with [[linear basis]] $(\phi^a)_{a = 1}^s$,
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

is the [[Cartesian space]] which is spanned by coordinate functions to be denoted as follows:

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
  \right)
$$

where the indices $\mu, \mu_1, \mu_2, \cdots$ range from 0 to $p$, while the index $a$ ranges from $1$ to $s$. In terms of these coordinates the [[bundle]] [[projection]] map $jb_k$ is just the one that remembers the spacetime coordinates $x^\mu$ and forgets the values of the field $\phi^a$ and its derivatives $\phi_{\mu}$. Similarly there are intermediate projection maps

$$
  \array{
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

given by forgetting coordinates with more indices.

The _infinite-order [[jet bundle]]_

$$
  J^\infty_\Sigma(E) \in SmoothSet
$$

is the [[smooth set]] defined so that a smooth function

$$
  U \overset{f}{\longrightarrow} J^\infty_\Sigma(E)
$$

from some [[Cartesian space]] $U$ is equivalently a system of ordinary smooth functions

$$
  \left(
    U \overset{f_k}{\longrightarrow} J^k_\Sigma(E)
  \right)_{k \in \mathbb{N}}
$$

into all the finite-order jet bundles, such that this is compatible with the
above projection maps, i.e. such that

$$
  \underset{k \in \mathbb{N}}{\forall} \left(
    jb_{k+1,k} \circ f_{k+1} = f_k
  \right)
  \,.
$$

Finally _[[jet prolongation]]_ is that function from the [[space of sections]] of the original bundle to the space of sections of the jet bundle which records the field $\Phi$ and all its spacetimes [[derivatives]]:

$$
  \array{
    \Gamma_\Sigma(E)
      &\overset{j^\infty}{\longrightarrow}&
    \Gamma_\Sigma(J^\infty_\Sigma(E))
    \\
    (\Phi^a)
    &\mapsto&
    \left(
      (\Phi^a)
      \,,\,
      ( \frac{\partial \Phi^a}{\partial x^\mu} )
      \,,\,
      ( \frac{\partial^2 \Phi^a}{\partial x^{\mu_1} \partial x^{\mu_2}} )
      \,,\,
      \cdots
    \right)
  }
  \,.
$$

=--

Smooth functions on jet bundles turn out to _locally_ depend on only finitely many of the jet coordinates:

+-- {: .num_prop}
###### Proposition

Given a [[jet bundle]] $J^\infty_\Sigma(E)$ as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime},
then a [[smooth function]] out of it

$$
  J^\infty_\Sigma(E) \longrightarrow X
$$

is such that around each point of $J^\infty_\Sigma(E)$ there is a [[neighbourhood]] $U \subset J^\infty_\Sigma(E)$
on which it is given by a function on a smooth function on $J^k_\Sigma(E)$ for some finite $k$.

=--



+-- {: .num_defn #VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[variational bicomplex]])**

On the [[jet bundle]] $J^\infty_\Sigma(E)$ of a [[trivial vector bundle]] over [[Minkowski spacetime]] as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} we may consider its [[de Rham complex]] of
[[differential forms]]; we write its [[de Rham differential]] in boldface:

$$
  \mathbf{d} \;\colon\; \Omega^\bullet(J^\infty_\Sigma(E)) \longrightarrow \Omega^{\bullet+1}(J^\infty_\Sigma(E))
  \,.
$$

Since the jet bundle unified spacetime with field values, we want to decompose this differential into
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
  \begin{aligned}
    d f
    & \coloneqq
    \frac{d f}{d x^\mu}
    \mathbf{d} x^\mu
    \\
    & \coloneqq
    \underoverset{\mu = 0}{p}{\sum}
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

The  _[[vertical derivative]]_

$$
  \delta
  \;\colon\;
  \Omega^\bullet( J^\infty_\Sigma(E) )
  \longrightarrow
  \Omega^{\bullet+1}( J^\infty_\Sigma(E) )
$$

is what remains of the full [[de Rham differential]] when the total spacetime derivative ([[horizontal derivative]]) is subtracted:

$$
  \delta \coloneqq \mathbf{d} - d
  \,.
$$

This defines a bigrading on the [[de Rham complex]] of $J^\infty_\Sigma(E)$, into horizontal degree $r$ and vertical degree $s$:

$$
  \Omega^\bullet\left( J^\infty_\Sigma(E) \right)
  \;\coloneqq\;
  \underset{r,s}{\oplus} \Omega^{r,s}(E)
$$

such that the horizontal and vertical derivative increase horizontal or vertical degree, respectively:

$$
  \array{
     C^\infty(J^\infty_\Sigma(E)) = & \Omega^{0,0}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{1,0}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{2,0}(E)
       &\overset{d}{\longrightarrow}&
     \cdots
     \\
     & \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}}
     \\
     &
     \Omega^{0,1}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{1,1}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{2,1}(E)
       &\overset{d}{\longrightarrow}&
     \cdots
     \\
     & \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}}
     \\
     &
     \Omega^{0,2}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{1,2}(E)
       &\overset{d}{\longrightarrow}&
     \Omega^{2,2}(E)
       &\overset{d}{\longrightarrow}&
     \cdots
     \\
     & \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}} && \downarrow^{\mathrlap{\delta}}
     \\
     & \vdots && \vdots && \vdots
  }
  \,.
$$

This is called the _[[variational bicomplex]]_.

=--

**derivatives on [[jet bundle]]**

| symbols |  name |
|--|---|
| $\mathbf{d}$ | [[de Rham differential]]  |
| $d \coloneqq d x^\mu \frac{d}{d x^\mu}$ | ([[total derivative|total]]) [[horizontal derivative]]  |
| $ \frac{d}{d x^\mu} \coloneqq \frac{\partial}{\partial x^\mu} +  \phi^a_{,\mu} \frac{\partial}{\partial \phi^a}  + \cdots $ | ([[total derivative|total]]) [[horizontal derivative]] along $\partial_\mu$ |
| $\delta \coloneqq \mathbf{d} - d$ | (variational) [[vertical derivative]] |
| $\delta_{EL} L \coloneqq \mathbf{d}L + d \Theta$ | [[Euler-Lagrange variational derivative]] |



+-- {: .num_example #BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}
###### Example
**(basic facts about [[variational calculus]])**

Given the jet bundle of a [[field bundle]] as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}, then
in its [[variational bicomplex]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
we have the following:

* The [[horizontal derivative]] of a spacetime coordinate function $x^\mu$
  coincides with its ordinary de Rham differential

  $$
    d x^\mu = \mathbf{d} x^\mu \in \Omega^{1,0}(E)
  $$

  and hence this is a horizontal 1-form.

* Therefore the vertical derivative of a spacetime coordinate vanishes:

  $$
    \delta x^\mu = 0
    \,.
  $$

* In particular the given [[volume form]] on $\Sigma$ gives a horizontal $p+1$-form

  $$
    dvol_\Sigma =  d x^0 \wedge d x^1 \wedge \cdots \wedge d x^p \in \Omega^{p+1,0}
    \,.
  $$

* Generally any horizontal $k$-form is of the form

  $$
    f_{\mu_1 \cdots \mu_k} d x^{\mu_1} \wedge \cdots \wedge d x^{\mu_k}
    \;\in\;
    \Omega^{k,0}(E)
  $$

  for $f_{\mu_1 \cdots \mu_k} = f_{\mu_1 \cdots \mu_k}\left((x^\mu), (\phi^a), (\phi^a_{,\mu})\right)$ any smooth function of the spacetime coordinates and the field coordinates.

* The horizontal differential of the vertical differential $\delta \phi$ of a field variable is the differential 2-form of horizontal degree 1 and vertical degree 2 given by

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

+-- {: .num_defn #LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[local Lagrangian density]])**

Given a [[field bundle]] $E$ over a $(p+1)$-dimensional [[Minkowski spacetime]] $\Sigma$ as in example \ref{TrivialVectorBundleAsAFieldBundle}, then a _[[local Lagrangian density]]_ $\mathbf{L}$ (for the field species thus defined) is a [[horizontal differential form]] of degree $(p+1)$ on the corresponding [[jet bundle]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

$$
  \mathbf{L} \;\in \; \Omega^{p+1,0}(E)
  \,.
$$

By example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle} any such Lagrangian density may uniquely be written as

$$
  \mathbf{L} = L dvol_\Sigma
$$

with $L = L((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots ) $ a smooth function on the jet bundle.


=--

+-- {: .num_prop #EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}
###### Proposition
**([[Euler-Lagrange operator]])**

If a [[Lagrangian density]] $\mathbf{L}$ as in def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}, then its de Rham differential has a _unique_ decomposition as a sum of two terms

$$
  \mathbf{d} \mathbf{L}
  =
  \delta_{EL} \mathbf{L}
  -
  d \Theta
$$

such that $\delta_{EL}$ is a "[[source form]]":

$$
  \delta_{EL} \mathbf{L} \in \Omega^{p+1,0}(E) \wedge \delta \Omega^{0,0}(E) \; \subset \Omega^{p+1,1}(E)
  \,.
$$

The map

$$
   \delta_{EL} \;\colon\; \Omega^{p+1,0}(E) \longrightarrow \Omega^{p+1,1}_s(E)
$$

thus defined is called the _[[Euler-Lagrange operator]]_ and is explicitly given by

$$
  \begin{aligned}
    \delta_{EL} L \, dvol_\Sigma
    & \coloneqq
    \frac{\delta L}{ \delta \phi^a}
    \delta \phi^a \wedge dvol_\Sigma
    \\
    & \coloneqq
    \left(
      \frac{\partial L}{\partial \phi^a}
      -
      \frac{d}{d x^\mu}
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      +
      \frac{d^2}{d x^{\mu^1} d x^{\mu^2}}
      \frac{\partial L}{\partial \phi^a_{\mu_1, \mu_2}}
      -
      \cdots
    \right)
    \delta \phi^a
    \wedge
    dvol_\Sigma
    \,.
  \end{aligned}
$$

The remaining term $d \Theta$ is unique, while $\Theta \in \Omega^{p,1}(E)$ is unique only up to terms in the image of $d$.
One possible choice is

$$
  \label{StandardThetaForTrivialVectorFieldBundleOnMinkowskiSpacetime}
  \begin{aligned}
    \Theta
    & \coloneqq \phantom{+}
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      \delta \phi^a
      \; \wedge \iota_{\partial_\mu} dvol_\Sigma
    \\
    & \phantom{=}
      +
      \left(
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu}
        -
        \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta \phi^a_{,\mu}
      \right)
    \wedge \iota_{\partial_\mu} dvol_\Sigma
    \\
    & \phantom{=} + \cdots
  \,,
  \end{aligned}
$$

where

$$
  \iota_{\partial_{\mu}} dvol_\Sigma
  \;\coloneqq\;
  (-1)^{\mu} d x^0 \wedge \cdots d x^{\mu-1} \wedge d x^{\mu+1} \wedge \cdots \wedge d x^p
$$

denotes the contraction of the volume form with the [[vector field]] $\partial_\mu$.

=--


+-- {: .proof}
###### Proof

Using $\mathbf{L} = L dvol_\Sigma$ and that $d \mathbf{L} = 0$ by degree reasons, we find

$$
  \begin{aligned}
    \mathbf{d}\mathbf{L}
    & =
    \left(
      \frac{\partial L}{\partial \phi^a} \delta \phi^a
      +
      \frac{\partial L}{\partial \phi^a_{,\mu}} \delta \phi^a_{,\mu}
      +
      \frac{\partial L}{\partial \phi^a_{,\mu_1 \mu_2}} \delta \phi^a_{,\mu_1 \mu_2}
      +
      \cdots
    \right)
    \wedge dvol_{\Sigma}
  \end{aligned}
  \,.
$$

The idea now is to have $d \Theta$ pick up those terms that would appear as [[boundary]] terms under the [[integral]]
$\int_\Sigma j^\infty(\Phi)^\ast \mathbf{d}L$ if we were to consider [[integration by parts]] to remove 
spacetime derivatives of $\delta \phi^a$.

We compute, using example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle},
the total horizontal derivative of $\Theta$ from (eq:StandardThetaForTrivialVectorFieldBundleOnMinkowskiSpacetime) as follows:

$$
  \begin{aligned}
    d \Theta
    & =
    \left(
      d 
      \left(
        \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a
      \right)
      +
      d
      \left(
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu}
        -
        \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{\mu \nu}}
        \delta \phi^a
      \right)
      +
      \cdots
  \right)
  \wedge \iota_{\partial_\mu} dvol_\Sigma
  \\
    & =
    \left(
      \left(
        \left( 
           d \frac{\partial L}{\partial \phi^a_{,\mu}}
        \right) \wedge  \delta \phi^a
        -
        \frac{\partial L}{\partial \phi^a_{,\mu}} \delta d \phi^a
      \right)
      +
      \left(
        \left(d \frac{\partial L}{\partial \phi^a_{,\nu \mu}}\right) \wedge \delta \phi^a_{,\nu}
        -
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}} \delta d \phi^a_{,\nu}
        -
        \left( d \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}} \right) \wedge
        \delta \phi^a
        +
        \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta d \phi^a
      \right)
          +
      \cdots
    \right)
    \wedge \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    -
    \left(
      \left(
        \frac{d}{d x^\mu} \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a
        +
        \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a_{,\mu}
      \right)
      +
      \left(
        \frac{d}{d x^\mu}
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}} 
        \delta \phi^a_{,\nu}
        +
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu \mu}
        -
        \frac{d^2}{ d x^\mu d x^\nu}
        \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta \phi^a
        -
        \frac{d}{d x^\nu}
        \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta \phi^a_{,\mu}
      \right)
      + \cdots
    \right)
    \wedge dvol_\Sigma
    \,,
  \end{aligned}
$$

where in the last line we used that

$$
  d x^{\mu_1} \wedge \iota_{\partial_{\mu_2}} dvol_\Sigma
  =
  \left\{
    \array{
      dvol_\Sigma &\vert& \text{if}\, \mu_1 = \mu_2
      \\
      0 &\vert& \text{otherwise}
    }
  \right.
$$

Here the two terms proportional to $\frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}} \delta \phi^a_{,\mu}$ 
cancel out, and we are left with

$$
  d \Theta
  \;=\;
    -
      \left(
        \frac{d}{d x^\mu} \frac{\partial L}{\partial \phi^a_{,\mu}}
        -
        \frac{d^2}{ d x^\mu d x^\nu}
        \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        +
        \cdots
      \right)
      \delta \phi^a \wedge dvol_\Sigma
        -
      \left(
        \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a_{,\mu}
        +
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu \mu}
        +
        \cdots
      \right)
      \wedge dvol_\Sigma
$$


Hence $-d \Theta$ shares with $\mathbf{d} \mathbf{L}$ the terms that are proportional to 
$\delta \phi^a_{,\mu_1 \cdots \mu_k}$ for $k \geq 1$,
and so the remaining terms are proportional to $\delta \phi^a$, as claimed:

$$
  \mathbf{d}L + d \Theta
  =
  \underset{
    \delta_{EL}\mathbf{L}
  }{
  \underbrace{
  \left(
    \frac{\partial L}{\partial \phi^a}
    -
    \frac{d}{d x^\mu}\frac{\partial L}{\partial \phi^a_{,\mu}}
    +
    \frac{d^2}{d x^\mu d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu\nu}}
    +
    \cdots
  \right)
  \delta \phi^a \wedge dvol_\Sigma
  }}
  \,.
$$


=--



#### Equations of motion


+-- {: .num_defn}
###### Definition
**([[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]])**

Given a [[field bundle]] $E$ over [[spacetime]] $\Sigma$ as in example \ref{TrivialVectorBundleAsAFieldBundle}
equipped with a [[local Lagrangian density]] $\mathbf{L} \in  \Omega^{p+1,1}(E)$ as in def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
then the corresponding _[[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]_
on fields $\Phi \in \Gamma_\Sigma(E)$ is the equation

$$
  j^\infty(\Phi)^\ast \left(\delta_{EL} \mathbf{L}\right) = 0
  \,,
$$

where $j^\infty(\Phi) \colon \Sigma \to J^\infty(E)$ denotes the [[jet prolongation]] of $\Phi$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), $j^\infty(E)^\ast$ the operation of
[[pullback of differential forms]] along this function, and $\delta_{EL}$ is the
[[Euler-Lagrange operator]] from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

By that same proposition this equation is
equivalently the [[differential equation]]

$$
  \left(
    \frac{\partial L}{\partial \phi^a}
      -
    \frac{d}{d x^\mu}
    \frac{\partial L}{\partial \phi^a_{,\mu}}
    +
    \frac{d^2}{d x^\mu d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu\nu}}
    -
    \cdots
  \right)
  \left(
     (x^\mu), (\Phi^a), \left( \frac{\partial \Phi^a}{\partial x^\mu}, \frac{\partial^2 \Phi^a}{\partial x^\mu \partial x^\nu} \right)
  \right)
  \;=\;
  0
  \,.
$$

We write

$$
  \Gamma_\Sigma(E)_{\delta_{EL} L = 0}
    \hookrightarrow
  \Gamma_\Sigma(E)
$$

for the [[smooth space|smooth]] subspace of the space of all field configurations on those that solve this
differential equation.

=--





### The traditional idea of field bundles and its problems
 {#IdeaOfFieldBundlesAndItsProblems}

A traditional approach to formalizing the notion of _physical field_ is to declare that the specification of a [[theory (physics)|theory in physics]]/[[physical system]] comes with a [[fiber bundle]] $E \to X$ over the [[spacetime]]/[[worldvolume]] $X$ (or better: naturally over all spacetimes, see at _[Locality](#IdeaLocality)_ below) called the ***[[field bundle]]*** and that a field configuration of the system is a [[section]] of this field bundle. This is for instance the basis for the theory of the [[variational bicomplex]], hence of [[BV-BRST formalism]] for expressing [[covariant phase spaces]], for standard [[multisymplectic geometry]], etc.

While this goes in the right direction, it cannot be quite the final answer, as it misses crucial properties that are demanded of a general notion of field. We now discuss these problems:

1. [Large gauge transformations](#IdeaLargeGaugeTransformations)

1. [Locality](#IdeaLocality)

1. [Spin structures and other G-structures](#IdeaSpinStructures)

1. [Background fields](#BackgroundFields)

1. [Higher gauge fields](#HigherGaugeFields)

In the course of discussing the problems we also motivate and indicate their solution by a more natural notion of field moduli in [[higher geometry]]. This is then discussed in full detail in the _[Definition](#Definition)_-section below.

#### Large gauge transformations 
 {#IdeaLargeGaugeTransformations}

In [[gauge theory]] specifically but in [[physics]] generally, physical fields come equipped with a notion of which [[field histories]], while possibly nominally different, are to be  regarded as [[equivalence|equivalent]], called _[[gauge equivalence|gauge equivalent]]_, and it is crucial to retain the information of gauge equivalences and not pass to [[equivalence classes]] of gauge equivalent fields. This means that, generically, for any [[physical theory]], even if field configurations are represented by [[sections]] of some [[field bundle]], many such sections are in fact to be regarded as being equivalent. Or more precisely, there should be a _[[groupoid]]_ and generally an _[[∞-groupoid]]_ of field histories of which the sections of the field bundle only form the space of [[objects]], while the [[gauge transformations]] form the [[morphisms]] and the [[higher gauge transformations]] of order $n$ form the [[n-morphisms]].

   To some extent this is dealt with in traditional [[variational calculus]]: after a choice of [[action functional]] on the space of field configurations, [[BV-BRST formalism]] spits out a [[derived L-∞ algebroid]] whose objects are field configurations, and whose 1-cells are infinitesimal invariances of the given [[action functional]]. 

   This goes in the right direction -- it is the [[Lie differentiation]] of the more encompassing [[smooth ∞-groupoid]] of fields and gauge transformations -- but has several problems, the main one being that it does not know about [[large gauge transformations]], those which are not connected to the identity (because it only sees infinitesimal data). 
These are important in the full quantum theory. 

Famous examples of the importance of [[large gauge transformations]] appear in

* [[2d CFT]], for which all standard theory would break down if the global [[conformal transformations]] were not considered as gauge transformations.

#### Locality 
 {#IdeaLocality}

Fields defined as sections of field bundles cannot capture gauge phenomena in a _local_ way, as is necessary for a manifestly local formulation such in [[extended prequantum field theory]], [[extended quantum field theory]] (sometimes called the "multi-tiered" formulation).

   Specifically, in [[Yang-Mills theory]] for [[gauge group]] $G$, a field configuration -- a _[[gauge field]] configuration_ -- is a combination of an [[instanton sector]] -- modeled by the [[equivalence class]] of a $G$-[[principal bundle]] $P$ -- and the "[[gauge potential]]", modeled by a [[connection on a bundle|connection on this bundle]] (see below at _[Gauge fields](#GaugeFields)_ for details).  There is a [[fiber bundle]] $E(P) \to X$ such that its [[sections]] are precisely the [[connection on a bundle|connections]] on $P \to X$, and so $\coprod_{c} E(P_c) \to X$, where $c$ ranges over the instanton sectors, is a field bundle for Yang-Mills fields on $X$. 

   But this construction is not local: if we consider this assignment of field bundles to all suitable manifolds $X$, and if $U \to X$ is a cover of $X$, then we cannot in general obtain the field bundle on $X$ by gluing the field bundle on the cover. This is because _locally_ every $G$-[[principal bundle]] has trivial class, so that locally there is always only a single (the trivial) instanton sector. 

This failure of locality is often not recognized in the literature, since many if not most descriptions of physics restrict to trivial spacetime topology and/or restrict to [[perturbation theory]] only. A formulation accurate and encompassing enough to see this issue is _[[AQFT on curved spacetimes]]_. A reference that explicitly runs into this non-locality issue of the field bundle in gauge theory in this context is ([Benini-Dappiaggi-Schenkel 13](field+bundle#BDS), [Schenkel 14](field+bundle#Schenkel14)): the authors define a [[functor]] from [[spacetimes]] equipped with a $G$-[[principal bundle]] that assigns the [[algebras of observables]] of the corresponding [[Yang-Mills fields]] built from the field bundle of connections on the given principal bundles; and they observe that the result fails to be a [[local net]] in that the inclusion of observables of a smaller spacetime into a larger patch may fail the isotony axiom ([BDS, remark 5.6](field+bundle#BDS)). The authors then try to circumvent this by restricting to trivial instanton sectors. The fix later appears in ([Benini-Schenkel-Szabo 15](#BeniniSchenkelSzabo15)), where the authors then consider proper [[stacks]] of fields.

But notice that instanton sectors is a non-negligible phenomenon. For instance the very [[vacuum]] in the [[standard model of particle physics]] is a [[superposition]] of all possible instanton sectors (see at _[[instanton in QCD]]_ for more on this).  And there are field theories where the fields consist entirely of "[[instanton sectors]]" and where there is no infinitesimal information about the gauge group at all: these are theories whose gauge group is a [[discrete group]], which includes notably [[Dijkgraaf-Witten theory]] and its higher analogy such as the [[Yetter model]]. This means that for these [[theory (physics)|theories]] a local field bundle formalism can see nothing of the actual fields and also traditional tools applied to a global field bundle (such as traditional [[BV-BRST formalism]]) see nothing of the actual fields. All this is fixed by the formulation that we discuss [below](#Definition).


   But this example already points to the general nature of the problem with field bundles, and also to its solution: while the [[instanton]]-component of [[Yang-Mills fields]] are not section of a bundle, they famously are sections of a _[[stack]]_ -- the "[[moduli stack]] $\mathbf{B}G$ of $G$-principal bundles", an object in [[higher geometry]].

   The problem with the locality of the [[field bundle]] for [[Yang-Mills theory]] is solved by passing from [[fiber bundles]] to [[fiber ∞-bundles]]: in the [[smooth ∞-groupoid|higher differential geometry]] there is an object $\mathbf{B}G_{conn}$  -- the [[moduli stack]] of $G$-[[principal connections]] (being the [[stackification]] of the [[groupoid of Lie algebra-valued forms]]) such that maps $X \to \mathbf{B}G_{conn}$ are equivalent to Yang-Mills fields on $X$ (even including their [[gauge transformations]]). This means that if we allow field bundles in higher geometry -- [[fiber ∞-bundles]], then that for Yang-Mills theory over $X$ is even a trivial field bundle, namely the [[projection]]

   $$
     X \times \mathbf{B}G_{conn} \to X
   $$

out of the [[product]] of [[spacetime]] with the [[moduli stack]] of fields.

   This is a differential refinement of what is called the trivial _$G$-[[gerbe]]_ on $X$, which is 

   $$
     X \times \mathbf{B}G \to X
   $$

   and hence the "field bundle for instanton sectors" of Yang-Mills fields.

   In summary: there cannot be a [[fiber bundle]] such that its [[sheaf]] of [[local sections]] is the sheaf of configurations of the Yang-Mills field. But there is a [[fiber infinity-bundle|fiber 2-bundle]] whose [[stack]] of sections is the stack of configurations of the Yang-Mills field.

   Judging from these examples one might be tempted to guess that the notion of field [[fiber bundle]] should simply be replaced by that of field [[fiber ∞-bundle]]. But in fact what the example rather suggests is that what matters directly is the [[moduli stack]] $\mathbf{Fields}$ of fields, which for $G$-[[Yang-Mills theory]] is simply

   $$
     \mathbf{Fields} = \mathbf{B}G_{conn}
     \,.
   $$

   This perspective, which we describe in detail [below](#Definition) also has the pleasant effect that it drastically simplifies and unifies notions of quantum field theory, for this says equivalently that if only we allow spaces in [[higher geometry]], then [[Yang-Mills theory]] is a _[[sigma-model]]_ quantum field theory: one whose fields are simply maps to a given [[target space]], only that this target space here is a [[stack]].

   But there are more advantages, slightly less obvious. These we come to in the following points.


#### Spin-structures and other $G$-structures
 {#IdeaSpinStructures}

Some fields in physics are (or involve) choices of _[[G-structure]]_ in the sense of [[reduction and lift of structure groups]]. Well-known examples include the choice of _[[orientation]]_ and of _[[Spin structure]]_ in field theories with [[fermion]] fields (discussed in detail in _[Fermions](#Fermions)_ below). Often in the literature the choice of [[orientation]] and [[Spin structure]] is treated as an external parameter, but detailed analysis at least in low-dimensional examples shows that in the full theory this is really a field configuration. For instance in [[path integral]] [[quantization]] for theories with fermions, part of the integral over all field configurations is a sum over Spin structures.

Now, a spin structure _is_ equivalently a section of something, but again not of a [[principal bundle]], but of an analog in [[higher geometry]], a [[principal 2-bundle]]. 

To see how this works, first recall the case of orientations, whose description as sections of the [[orientation bundle]] is familiar.

For a [[spacetime]] represented by a [[smooth manifold]] $X$ of [[dimension]] $n$, let 

$$
  \tau_X \;\colon\; X \to \mathbf{B}GL(n)
$$ 

be the map that [[modulating morphism|modulates]] its [[tangent bundle]] (discussed at [_geometry of physics - tangent bundle_](geometry+of+physics#TangentBundle)). Consider then the following diagram, which shows lifts of this map to the  [[classifying spaces]]/[[moduli stacks]] for various other groups (this is the _[[Whitehead tower]]_ of $\mathbf{B}O(n)$):

$$
  \array{
    && \vdots
    \\
    && \downarrow
    \\
    && \mathbf{B}Spin(n) &\stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to}& \mathbf{B}^3 U(1)
    \\
    &\mathllap{s_X}\nearrow& \downarrow
    \\
    && \mathbf{B}SO(n) &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
    \\
    &{}^{\mathllap{o_X}}\nearrow& \downarrow
    \\
    X & \stackrel{e_X}{\to}& \mathbf{B}O(n) &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B}\mathbb{Z}_2
    \\
    &{}_{\mathrlap{\tau_X}} \searrow& \downarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

A lift of the tangent bundle map $\tau_X$ to a map $e_X \colon X \to \mathbf{B}O(n)$ as indicated is a choice of [[orthogonal structure]] (a [[vielbein field]], discussed in detail below in _[Ordinary gravity](#OrdinaryGravity)_). For the present discussion assume that this is given.


Then a further lift to $o_X : X \to \mathbf{B}SO(n)$ is a choice of [[orientation]], and finally a lift to $s_X : X \to \mathbf{B}Spin(n)$ is a choice of [[spin structure]].

Now, every hook-shaped sub-[[diagram]] in the above of the form

$$
  \array{
    \mathbf{B}\hat G
    \\
    \downarrow
    \\
    \mathbf{B}G &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^n A
  }
$$

is a [[homotopy fiber sequence]]. By the [[universal property]] of the [[homotopy pullback]] this means that the "space" -- really: _[[homotopy type]]_ or just _[[type]]_, for short -- of lifts of a given map $X \to \mathbf{B}G$ to a map $X \to \mathbf{B}\hat G$ is equivalently the type of trivializations of the [[composition|composite]] $X \to \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^n A$. 

Now if we have an [[orthogonal structure]] $e_X : X \to \mathbf{B}O(n)$ given, then this composite map according to the above diagram is 

$$
  \mathbf{w}_1(e_X)
  \;\colon\;
  X \to \mathbf{B}\mathbb{Z}_2
  \,.
$$

This represents the [[first Stiefel-Whitney class]] $[w_1(\tau_X)] \in H^1(X, \mathbb{Z}_2)$ of $\tau_X$, and it classifies a $\mathbb{Z}_2$-[[principal bundle]], hence a [[double cover]] $\hat X \to X$ and this is precisely the [[orientation bundle]] of $X$. Sections of this bundle are choices of [[orientation]] on $X$, hence are "orientation-structure fields".

Assume then such orientation field $o_X$ is given.
Then in the next step the relevant composite map is

$$
  \mathbf{w}_2(o_X) \;\colon\; X \to \mathbf{B}^2 \mathbb{Z}_2
  \,.
$$

This now represents the [[second Stiefel-Whitney class]] $[w_2(\tau_X)] \in H^2(X, \mathbb{Z}_2)$ of $X$ and classifies a $(\mathbf{B}\mathbb{Z}_2)$-[[principal 2-bundle]] 

$$
  \array{
    \mathbf{B}\mathbb{Z}_2 &\to& P
    \\
    && \downarrow 
    \\
    && X
  }
  \,.
$$

This is sometimes called the _$Spin$-[[lifting bundle gerbe]]_ of $o_X$.
A choice of [[Spin structure]] is a choice of section of this 2-bundle.
Hence spin structures are parts of fields in physics which are not sections of a field 1-bundle. Again, this is faithfully captured only in [[higher geometry]].

This is only the most famous phenomenon in a large class of similar structures of fields in field theory. Notably in higher dimensional [[supergravity]] and in [[string theory]] there are fields which are ever higher lifts through this [[Whitehead tower]] -- [[higher spin structures]], such as [[String structures]] and [[Fivebrane structures]] in the next two steps. Accordingly, these are fields which are equivalently sections of [[principal 3-bundles]] (the "[[Chern-Simons circle 3-bundle]]") and [[principal infinity-bundle|principal 7-bundles]] (the "[[Chern-Simons circle 7-bundle]]").

#### Background fields
 {#BackgroundFields}

Comparison of the above discussions under _[Locality](#IdeaLocality)_ and _[Spin structures](#IdeaSpinStructures)_  shows that there we had a higher-geometric field bundle of [[Yang-Mills fields]] which was hower "trivial" in the sense that it was a projection out of the [[product]] of [[spacetime]] with a [[moduli stack]], so that a field configuration was equivalently of [[sigma-model]]-type, namely simply a map $\phi \colon : X \to \mathbf{B}G_{conn}$; whereas here the "spin-lifting 2-bundles" and its higher analogs are, in general, not of this product form, hence "Spin structure"-fields, at least superficially do not seem to be of [[sigma-model]]-type, even in [[higher geometry]].

But a closer inspection shows that in fact both situations are entirely analogous -- once we realize that here these Spin-structure fields are not really defined just on $X$, but on $X$ _equipped with its orientation_ $o_X$. Since, by the same logic as above, also the orientation is a "field", we may call it a ***[[background field]]***. It serves as "background" over which spin structure fields can be considered.

In [[higher geometry]] incarnated naturally as [[(∞,1)-topos theory|higher topos theory]], this state of affairs is naturally modeled and indeed yields again a _moduli stack of spin structure fields_ and makes spin-structures be [[sigma-model]]-type fields, as follows:

the natural way to regard both $X$ as well as its orientation structure $o_X$ as a single object is to regard the map $X \stackrel{o_X}{\to} \mathbf{B}SO(n)$ as an object in the [[slice (∞,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}SO(n)}$. In here an [[object]] is a map of [[stacks]] into $\mathbf{B}SO(n)$, and a morphism is map of the domains of these maps together with a [[homotopy]] filling the evident triangle [[diagram]]. Notably a lift of the orientation structure $o_X$ to a spin structure $s_X$ as above, hence a diagram of the form

$$
  \array{
    X &&\stackrel{s_X}{\to}&& \mathbf{B}Spin(n)
    \\
    & {}_{\mathllap{o_X}}\searrow &\swArrow_\simeq& \swarrow_{\mathrlap{\mathbf{SpinStruc}_n}}
    \\
    && \mathbf{B}SO(n)
  }
$$ 

is equivalently a map 

$$
  o_X \to \mathbf{SpinStruc}_n
$$

in $\mathbf{H}_{/\mathbf{B}SO(n)}$. This is again of the same simple form of the Yang-Mills fields on $X$, which are maps

$$
  X \to \mathbf{B}G_{conn}
  \,,
$$

but in the collection of stacks $\mathbf{H}$ itself, not in a [[slice (infinity,1)-topos|slice]].

The slice here encodes the presence of [[background fields]] -- namely orientations in this case -- whose [[moduli stack]] in turn is, in this case, $\mathbf{B}SO(n)$. 

Notice that also the field of [[gravity]] has a background field in this precise sense: as metioned above, a gravitational field configuration is a lift of $\tau_X$ through $\mathbf{B}O(n) \stackrel{\mathbf{OrthStruc}_n}{\to} \mathbf{B}GL(n)$, hence a map

$$
  \tau_X \to \mathbf{OrthStruc}_n
$$

in the slice $\mathbf{H}_{/\mathbf{B}GL(n)}$. (Discussed in detail in _[Ordinary gravity](#OrdinaryGravity)_ below.) Hence also [[gravity]] becomes a [[sigma-model]]-type field theory in [[higher geometry]]. Notice that here it is [[smooth structure]] on $X$, as embodied in $\tau_X$, which is the background.

Now, at least for the field of gravity one can of course emulate the fields also by sections of a field bundle (while already for the second next step in the Whitehead tower, Spin structures, this is no longer the case, as we have seen). But even so, the field bundle formalism clearly misses then the relation between fields and background fields.

In particular for two reasons

1. Typically the presence of background fields indicates that in a more comprehensive discussion background fields are also fields that vary;

1. Often background fields on one space affect fields on _another_ space.

An archetypical example for both these effects combined is 3d [[Chern-Simons theory]] with a compact, simple and simply connected [[gauge group]] $G$ in the presence of [[Wilson lines]]. This is a [[theory (physics)|theory]] on 3-dimensional [[spacetime]]/[[worldvolume]] $\Sigma$ whose fields are $G$-[[gauge fields]] as for [[Yang-Mills theory]] above, hence given by maps $\Phi \colon \Sigma \to \mathbf{B}G_{conn}$. At the same time, this theory has a "coupling" to a 1-dimensional [[theory (physics)|theory]] which describes [[particles]] propagating around [[knots]] $C : S^1 \to \Sigma$ in $\Sigma$ for which the restriction $\Phi|_C$ serves as the [[background gauge field]]. Specifically, a field configuration of this 1-dimensional theory is equivalently a map in the slice $\mathbf{H}_{/\mathbf{B}G_{conn}}$ which in $\mathbf{H}$ is given by a diagram of the form

$$
  \array{
   S^1 &&\to&& \Omega^1(-,\mathfrak{g}//T)
   \\
   & {}_{\mathllap{C}}\searrow &\swArrow& \swarrow_{\mathrlap{\mathbf{OrbitStruct}}}
   \\
   && \mathbf{B}G_{conn} 
  }
$$ 

for some map on the right which we discuss in detail below in _[Chern-Simons fields with Wilson line fields](#ChernSimonsWithWilsonLines)_.

Here considering just these fields in the background of a fixed $\Phi|_C$ produced a 1-dimensional [[quantum field theory]] whose [[partition function]] is that "[[Wilson loop]]" observable of $\Phi|_C$. But this is not considered in isolation. The whole point of the relation of [[Chern-Simons theory]] to the [[Jones polynomial]] [[knot invariant]] of the [[knot]] $C$ is that one consider also $\Phi$ as a dynamical field, not as a fixed background. Indeed, in the full theory of Chern-Simons with Wilson loops that includes both the fields on $\Sigma$ as well as those on the knot, a field configuration is the diagram as above but regarded as the square 

$$
  \array{
    S^1 &\to& \Omega^1(-,\mathfrak{g})//T
    \\
    {}^{\mathllap{C}}\downarrow 
    &\swArrow& \downarrow^{\mathrlap{\mathbf{OrbitStruc}}}
    \\
    \Sigma &\stackrel{\Phi}{\to}& \mathbf{B}G_{conn}
  }
  \,,
$$

hence, again, a single map

$$
  C \to \mathbf{OrbiStruc}
$$

but now in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$.

This subtle interplay of "bulk fields" and "[[QFT with defects|defect fields]]" which is here captured most naturally in terms of [[higher geometry]] cannot really be expressed accurately just in terms of field bundles.


#### Higher gauge fields
 {#HigherGaugeFields}

Above we have seen the generalization of field bundles to [[higher geometry]] already for traditional notions such as Yang-Mills fields and Spin-structures. But many [[theory (physics)|theories]] considered in theoretical physics have fields that are more "explicitly" entities in [[higher geometry]].

For instance the higher analog of the [[electromagnetic field]] which is called the _[[B-field]]_ or _[[Kalb-Ramond field]]_ is a [[circle n-bundle with connection|2-connection]] on a [[principal 2-bundle]]. There is no way to faithfully encode this as a section of any ordinary [[fiber bundle]]. It follows that for instance also the [magnetic charge anomaly](magnetic+charge#MagneticChargeAnomaly) (as discussed there) has no accurate description in terms of field bundles. Next the [[supergravity C-field]] is a [[circle n-bundle with connection|3-connection]] on a [[principal 3-bundle]], and so on.

There is a wide variety of [[higher dimensional Chern-Simons theories]] whose fields are such [[higher gauge fields]]. In some traditional literature one sees parts of this theory be discussed by standard [[BV-BRST formalism]] applied to [[field bundles]], namely by ignoring the non-trivial [[instanton sectors]] and pretending that a field configuration for these [[connection on an ∞-bundle|∞-connections]] are given by globally defined [[differential forms]]. In some special cases (for instance for [[spacetimes]]/[[worldvolumes]] of very special topology or low [[dimension]]) this can be sufficient to capture everything, but in general (for instance for $U(1)$-[[higher dimensional Chern-Simons theory]] and its [[holographic principle|holographically dual]] [[self-dual higher gauge theory]]) it is not.


### The solution: Field $\infty$-bundles and moduli $\infty$-stacks of fields

By the [above](#IdeaOfFieldBundlesAndItsProblems), defining a physical field to be a section of some bundle goes in the right direction, but misses crucial aspects of physical fields. These problems are fixed by passing to [[higher geometry]].

Below in _[Definition](#Definition)_ we discuss a natural unified formulation of the notion of physical field in terms of [[higher geometry]] (the central definition being def. \ref{FieldsInAnActionFunctional} ) and then we spell out many [Examples](#Examples).

This definition turns out to be equivalent, at least under mild conditions, to a formulation where fields are sections of an [[associated ∞-bundle]], hence a "field $\infty$-bundle". This we discuss in _[Properties -- Relation of fields to sections of ∞-bundles](#RelationOfFieldsToSections)_. But this is just one of several equivalent perspectives on physical fields, and not always the most transparent one. In fact, sections of higher associated bundles are best known in the literature on [[twisted cohomology]] and indeed one equivalent characterization of fields is as [[cocycles]] in [[twisted cohomology]] in the general sense of [[cohomology]] in an [[(∞,1)-topos]]. This we discuss below in _[Relation to twisted cohomology](#RelationToTwistedCohomology)_.

In summary we find and discuss that

| fields | $\simeq$ |  [[twisted cohomology|twisted]] [[relative cohomology|relative]] [[cohesion|cohesive]] [[cocycles]] |
|--|--|--|

## Definition 
 {#Definition}

We give a general abstract definition of physical fields in 

* _[Physical fields](#DefinitionPhysicalField)_

Then we consider some general abstract operations on fields in 

* _[Restriction and pullback of fields](#RestrictionAndPullback)_



### Physical fields
 {#DefinitionPhysicalField}

A notion of _field_ in physics is part of a specification of _[[theory (physics)|physical theory]]_ or _[[model (physics)|physical model]]_. We consider specifically the framework of [[prequantum field theory]]. Here a [[theory (physics)|theory]]/[[model (physics)|model]] is specified by (or at least comes with) an _[[action functional]]_. The _field_ content of the theory is part of the specification of the [[domain]] of the action functional. Therefore in def. \ref{FieldsInAnActionFunctional} below we define _action functionals_ and the fields relative to this notion.

We work in the following context.

+-- {: .num_defn}
###### Context

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]]. For many of the examples below it is furthermore assumed that $\mathbf{H}$ is equipped with [[differential cohesion]]. This implies in particular that there is a notion of [[smooth manifold]] [[internalization|internal]] to $\mathbf{H}$.

Fix $\mathbb{G} \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence a cohesive [[∞-group]].

=--



For the main definition below we need the following basic notation.

+-- {: .num_defn}
###### Definition

For $B \in \mathbf{H}$ any [[object]], and $X,A \in \mathbf{H}_{/B}$ two objects in the [[slice (∞,1)-topos]], write

$$
  [X,A]_{\mathbf{H}}
  \coloneqq
  \underset{B}{\prod} [X,A]
  \in \mathbf{H}
$$

for the $\mathbf{H}$-valued [[hom object]] between $X$ and $A$: the [[dependent product]] over $B \to *$ of the [[internal hom]] $[X, A] \in \mathbf{H}_{/B}$.

=--


The following defines the notion of _[[action functional]]_ and as part of the data it defines the notion of _physical field_.

+-- {: .num_defn #FieldsInAnActionFunctional}
###### Definition

Given an [[object]] $\mathbf{BgFields} \in \mathbf{H}$ and 
given two objects, to be denoted $\Phi_X, \mathbf{Fields}  \in \mathbf{H}_{/B}$, in the [[slice (∞,1)-topos|slice]] over $\mathbf{BgFields}$,
then an **[[action functional]]** in ($\mathbf{H}, \mathbb{G})$ "on fields on $X$" is a [[morphism]]

$$
  S \;\colon\; [\Phi_X, \mathbf{Fields}]_{\mathbf{H}} \to \mathbb{G}
  \,.
$$

In this context we say that

* the [[dependent sum]] $X \coloneqq \underset{\mathbf{BgField}}{\sum} \Phi_X$ is the **[[worldvolume]]** or **[[spacetime]]**;

* the morphism $\Phi_X \;\colon\; X \to \mathbf{BgFields}$ is the **[[background field]]**;

* the object $\mathbf{Fields}$ is the **[[moduli ∞-stack]] of fields**;

* the [[elements]] of $[\Phi_X,\mathbf{Fields}]_{\mathbf{H}}$, hence (see prop. \ref{GlobalPointsOfModuliOfFields} below) the morphisms

  $$
    \phi \;\colon\; \Phi_X \to \mathbf{Fields}
  $$

  in $\mathbf{H}_{/\mathbf{BgFields}}$, hence the [[diagrams]]

  $$
    \array{
       X &&\stackrel{\phi}{\to}&& \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields}
       \\
       & {}_{\mathllap{\Phi_X}}\searrow 
       &\swArrow& 
       \swarrow_{\mathrlap{\mathbf{Fields}}}
       \\
       && \mathbf{BgFields}
    }
  $$

  in $\mathbf{H}$, are the **fields** on $X$;

* a **[[gauge transformation]]** is a [[homotopy]] in $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$, hence a

  $$
    \phi \Rightarrow \phi'
  $$

* a **[[higher gauge transformation]]** is a [[higher homotopy]] in $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$.


=--

+-- {: .num_remark}
###### Remark

Definition \ref{FieldsInAnActionFunctional} provides a unified perspective on fields from several perspectives. 

On the one hand, it almost explicitly says that in [[higher geometry]] all fields are "[[sigma-model]] fields" (see below at _[Examples -- Scalar and Sigma-model fields](#SclarModuliFields)_): if we regard the [[moduli ∞-stack]] $\mathbf{Fields}$ as the _[[target space]]_ then fields are simply maps from their domain (when regarded as [[spacetime]] _and_ [[background field]]) to this target space.

On the other hand, we see below in _[Relation to sections of ∞-bundles](#RelationOfFieldsToSections)_ that from another perspective def. \ref{FieldsInAnActionFunctional} says that all fields are [[sections]] of an [[associated ∞-bundle]] to an  $\infty$-bundle modulated by the background fields. This means that in [[higher geometry]] all fields are "[[matter]] fields" (see below at _[Matter fields](#MatterFields)_) [[charge (physics)|charged]] under the [[background gauge field]].

Finally, we see below in  _[Relation to twisted cohomology](#RelationToTwistedCohomology)_ that from yet another perspective def. \ref{FieldsInAnActionFunctional} says that fields are equivalently [[cocycles]] in general [[twisted cohomology]]. This perspective is traditionally known for certain examples (see _[Examples -- Chan-Paton gauge fields](#ChanPatonGaugeFields)_ below), but we see below that it is useful in its full generality. For instance the field of [[gravity]] is in a precise sense a 0-cocycle with coefficients in the [[coset space]] $GL(n)/O(n)$ that is twisted by the [[tangent bundle]] of spacetime (which exhibits the background gauge structure for [[gravity]]: the [[smooth structure]] of [[spacetime]]). An inkling of this perspective is certainly visible in the traditional literature, notably in the generalization to [[type II geometry]] and [[T-duality]], and here we see how this is a precise mechanism on the same conceptual footing with the twisted K-theory seen over D-branes.

=--


### Restriction and pullback of physical fields
 {#RestrictionAndPullback}

It is familiar from basic examples that not every type of physical field on a [[spacetime]]/[[worldvolume]] $X$ can be pulled back (in the sense of pullback of functions) along any [[smooth function]] $f \;\colon\;Y \to X$. For instance the field of [[gravity]], a [[vielbein field]] or [[pseudo-Riemannian metric|pseudo]]-[[Riemannian metric]], discussed below in _[Ordinary graviry](#OrdinaryGravity)_ may be pulled back only along [[local diffeomorphisms]]. More generally, one needs other [[properties]] on $f$ to pull back a given field and in fact in general one needs [[extra structure]]. 

In view of def. \ref{FieldsInAnActionFunctional} above this is immediate: by that definition a field on $X$ in general does not just depend on $X$, but in fact also on the background field structure denoted $\Phi_X$. Accordingly, it can be pulled back only along maps that also carry this background field structure along.

+-- {: .num_remark #PullbackAlongGeneralizedLocalDiffeomorphisms}
###### Remark

Since by def. \ref{FieldsInAnActionFunctional} a physical field is a map $\phi \colon \Phi_X \to \mathbf{Fields}$ in 
$\mathbf{H}_{/\mathbf{BgFields}}$, it may be "pulled back" along maps  of [[spacetime]]/[[worldvolume]] $f \colon Y \to X$ when these are extended to maps $\Phi_Y \to \Phi_X$ in $\mathbf{H}_{/\mathbf{BgFields}}$ of the [[background fields]], hence to [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
    Y &&\stackrel{f}{\to}&& X
    \\
    & {}_{\mathllap{\Phi_Y}}\searrow &\swArrow_{\kappa}& \swarrow_{\mathrlap{Phi_X}}
    \\
    && 
    \mathbf{BgFields}
  }
  \,,
$$

hence maps $f : X \to Y$ equipped with a choice of [[equivalence]] 

$$
  \kappa ;\colon\; f^*\Phi_X \simeq \Phi_Y 
$$

between the [[background fields]].

=--

In standard _[Examples](#Examples)_ discussed below we see that this is a familar fact. For instance applied to the field of gravity (see _[Gravity](#OrdinaryGravity)_ below) it says that the gravitational field can be pulled back precisely along [[local diffeomorphisms]], or that spin structures on oriented manifolds (see _[Spin structures](#SpinStructures)_ below) can be pulled back along orientation-preserving maps. Or : for [[Chan-Paton gauge fields]] on [[D-branes]] (see _[Chan-Paton gauge fields](#ChanPatonGaugeFields)_) it reproduces the familiar gauge relation for the [[B-field]] on D-branes known in [[string theory]], which is already less trivial. But the statement applies in full generality.

### Boundary and defect fields
 {#BoundaryAndDefectFields}

In def. \ref{FieldsInAnActionFunctional} the [[background field]] $\Phi_X$ is a fixed datum of the domain ([[spacetime]]/[[worldvolume]]) on which the physical fields are defined. In some [[model (in theoretical physics)|models]] and for some of the fields this is precisely what one needs, but in other models one may need to be able to also regard the background fields as dynamical fields and to be able to switch between these perspectives, for instance to pass to a setup where what used to be a configuration of some field is now taken to be a fixed background field for the remaining fields. We now discuss how this more general setup is naturally formulated as a generalization of def. \ref{FieldsInAnActionFunctional}.


For $\mathbf{H}$ an [[(∞,1)-topos]] and $\mathbf{Fields} \colon \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields} \to \mathbf{BgFields}$ a morphism in $\mathbf{H}$, we may consider this also as an object in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$ (the [[(∞,1)-functor (∞,1)-category]] from the [[interval category]]/1-[[simplex]] to $\mathbf{H}$).

A generic object in $\mathbf{H}^{(\Delta^1)}$ here is a morphism $\iota_X$ in $\mathbf{H}$. When we think of this as a domain on which to define fields we will write this

$$
  \iota_X 
    \;\colon\;
  X_{def}
  \to 
  X_{bulk}
$$

where the subscripts are for "bulk" and for "defect" (as in _[[QFT with defects]]_). A field in $\mathbf{H}^{(\Delta^1)}$ which is given by a map

$$
  \phi 
   \;\colon\;
  \iota_X \to \mathbf{Fields}
$$

in $\mathbf{H}^{(\Delta^1)}$ is equivalently a [[diagram]] of the form

$$
  \array{
    X_{def} &\stackrel{\phi_{def}}{\to}& \mathbf{Fields}_{def}
    \\
    {}^{\mathllap{\iota_X}}\downarrow 
    &\swArrow& 
    \downarrow^{\mathrlap{\mathbf{Fields}}}
    \\
    X_{bulk} &\stackrel{\phi_{bulk}}{\to}& \mathbf{Fields}_{bulk}
  }
$$

in $\mathbf{H}$.

This we interpret as a configuration consisting of 

1. a bulk field configuration $\phi_{bulk}$ 

1. a defect field configuration $\phi_{def}$, 

1. a [[gauge transformation]] that relates the restriction (or more generally: pullback to $X_{def}$) of the bulk field to the embedding (or more generally: push-forward) of the defect field into the bulk field configuration on the defect.

+-- {: .num_remark }
###### Remark

If $\phi_{bulk}$ is regarded as fixed, then this is equivalently a field configuration as in def. \ref{FieldsInAnActionFunctional} defined on $X_{def}$ and for background field the composite 

$$
  \Phi_{X_{def}}
  \coloneqq
  \iota_X^* \phi_{bulk}
  \;\colon\;
  X_{def} \stackrel{\iota_X}{\to}
  X \stackrel{\phi_{bulk}}{\to}
  \mathbf{Fields}_{bulk}
  \,.
$$ 

=--

This "fixing of bulk fields to background fields for defect fields" we discuss in more detail below in _[Properties -- Moduli stacks of fields](#ModuliStacksOfFields)_.


We formalize the moduli $\infty$-stack of all bulk and boundary fields as follows

+-- {: .num_defn }
###### Definition

Write

$$
  \mathbf{H}^{(\Delta^1)}
  \stackrel{\overset{Disc_{\mathbf{H}}}{\leftarrow}}{\underset{\Gamma_{\mathbf{H}}}{\to}}
  \mathbf{H}
$$

for the canonical [[geometric morphism]].

=--

+-- {: .num_defn #ModuliOfBulkAndBoundaryFields}
###### Definition

For $\iota_X ;\colon\; X_{def} \to X_{bulk}$ and $\mathbf{Fields} \;\colon\; \mathbf{Fields}_{def} \to \mathbf{Fields}_{bulk}$ morphisms in $\mathbf{H}$, we say that

$$
  [\iota_X, \mathbf{Fields}]_{\mathbf{H}}
  \coloneqq
  \Gamma_{\mathbf{H}}[\iota_X, \mathbf{Fields}]
  \;\;
  \in \mathbf{H}
$$

is the [[moduli ∞-stack]] of bulk and boundary fields on $\iota_X$.

=--


Several examples of this are discussed below.




## Properties
 {#FieldsProperties}

The definition of fields in def. \ref{FieldsInAnActionFunctional} is in fact the central part of a general theory of _[[cohomology]]_ and _[[principal ∞-bundles]]_ in [[higher geometry]]/[[(∞,1)-topos theory]] and various insights into [[prequantum field theory]] follow by making this perspective explicit.  This is what we do here

1. [Moduli ∞-stacks of fields](#ModuliStacksOfFields)

1. [Relation of fields to sections of ∞-bundles](#RelationOfFieldsToSections)

1. [Relation of fields to twisted cohomology](#RelationToTwistedCohomology)

1. [Relation of fields to relative cohomology](#RelationToRelativeCohomology)

The central results that underlie these identifications are in ([NSS](#NSS)), also [dcct, section 3.6.10, 3.6.11, 3.6.12, 3.6.15](#dcct).

### Moduli $\infty$-stacks of fields
 {#ModuliStacksOfFields}

The object $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}} \in \mathbf{H}$
of def. \ref{FieldsInAnActionFunctional} we may call the 
[[moduli ∞-stack]] of fields. Here we discuss various properties of this object. 

+-- {: .num_prop #GlobalPointsOfModuliOfFields}
###### Proposition

The [[∞-groupoid]] of global [[elements]] of $[X, \mathbf{Fields}]_{\mathbf{H}}$ is 

$$
  \mathbf{H}(*,[\Phi_X, \mathbf{Fields}_{\mathbf{H}}])
  \simeq
  \Gamma [\Phi_X, \mathbf{Fields}]_{\mathbf{H}}
  \simeq
  \mathbf{H}_{/\mathbf{BgFields}}(\Phi_X, \mathbf{Fields})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using the [[adjunction]] [[equivalences]] we have

$$
  \begin{aligned}
    \mathbf{H}(*, [\Phi_X, \mathbf{Fields}]_{\mathbf{H}})
    & \simeq
    \mathbf{H}(*, \underset{\mathbf{BgFields}}{\prod} [\Phi_X, \mathbf{Fields}])
    \\
    & \simeq \mathbf{H}_{/\mathbf{BgFields}}(\mathbf{BgFields}^*(*), [\Phi_X, \mathbf{Fields}])
    \\
    & \simeq \mathbf{H}_{/\mathbf{BgFields}}(*, [\Phi_X, \mathbf{Fields}])
    \\
    & \simeq \mathbf{H}_{/\mathbf{BgFields}}(\Phi_X, \mathbf{Fields})
  \end{aligned}
$$

where the first line is the definition, the second is the $(\mathbf{BgFields}^* \dashv \underset{\mathbf{BgFields}}{\prod})$ [[adjunction]]-[[equivalence]], the third is the $(\underset{\mathbf{BgFields}}{\sum} \dashv \mathbf{BgFields}^*)$-adjunction implying that $\mathbf{BgFields}^*$ preserves the [[terminal object]], and finally the last line is the defining [[internal hom]] [[adjunction]]-[[equivalence]]. 

=--

+-- {: .num_prop #ModuliStackOfFieldsAsHomotopyFiber}
###### Proposition

The [[moduli ∞-stack]] of fields $[\Phi_X, \mathbf{BgFields}]_{\mathbf{H}}$ sits in a [[homotopy pullback]] [[diagram]] of the form

$$
  \array{
    [\Phi_X, \mathbf{Fields}]_{\mathbf{H}}
    &\stackrel{}{\to}&
    [X, \underset{\mathbf{BgFields}}{\sum}\mathbf{Fields}]
    \\
    \downarrow &\swArrow_{\kappa}& \downarrow
    \\
    {*}
    &\stackrel{\vdash \Phi_X}{\to}&
    [X, \mathbf{BgFields}]
  }
  \,.
$$

=--

These relations are discussed at _[[slice (∞,1)-topos]]_, and ([dcct, section 3.6.1](#dcct)).


+-- {: .num_remark }
###### Remark

Proposition \ref{ModuliStackOfFieldsAsHomotopyFiber} makes precise the heuristic idea that a field $\phi \in [\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$ is 

1. a configuration $\phi_X \;\colon\; X \to \underset{\mathbf{BgFields}}{\sum}\mathbf{Fields}$ on [[spacetime]]/[[worldvolume]] $X$;

1. together with a [[gauge transformation]] $\kappa_{\phi} \;\colon\;  \Phi_X \stackrel{\simeq}{\to} \mathbf{Fields}\circ \phi_X$ between the fixed [[background field]] and the background field induced by $\phi_X$.

=--

More generally, the moduli $\infty$-stacks of combined bulk/boundary-defect fields as in def. \ref{ModuliOfBulkAndBoundaryFields} is characterized as follows.

+-- {: .num_prop #ModuliOfBulkAndDefectFieldsAsPullback}
###### Proposition

The moduli stack $[\iota_X, \mathbf{Fields}]_{\mathbf{H}}$ of bulk and defect fields in def. \ref{ModuliOfBulkAndBoundaryFields} sits in an [[(∞,1)-pullback]] [[diagram]]

$$
  \array{
    [\iota_X, \mathbf{Fields}]_{\mathbf{H}}
    &\to&
    [X_{def}, \mathbf{Fields}_{def}]
    \\
    \downarrow && \downarrow^{\mathrlap{}}
    \\
    [X_{bulk}, \mathbf{Fields}_{bulk}]
    &\stackrel{}{\to}&
    [X_{def}, \mathbf{Fields}_{bulk}]
  }
  \,.
$$

=--

The following proposition expresses that fixing a bulk field gives rise to a background field for the remaining defect fields

+-- {: .num_prop }
###### Proposition

For $\phi_{bulk} \;\colon\; X_{bulk} \to \mathbf{Fields}_{bulk}$ a given bulk field, there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category|equivalence]]

$$
  [\iota_X^* \phi_{bulk}, \mathbf{Fields}]_{\mathbf{H}}
  \simeq
  [\iota_X, \mathbf{Fields}]_{\mathbf{H}}
  \underset{[X_{bulk}, \mathbf{Fields}_{bulk}]}{\times} \{\phi_{bulk}\}
  \,.
$$

=--

### Relation to sections of fiber $\infty$-bundles
 {#RelationOfFieldsToSections}

We discuss here how def. \ref{FieldsInAnActionFunctional} equivalently says that fields are [[sections]] of a [[fiber ∞-bundle]] which is  which is [[associated ∞-bundle|associated]] to a ([[principal ∞-bundle|principal]])  $\infty$-bundle modulated by the [[background field]].

For simplicity of the discussion first consider the case that $\mathbf{BgFields} \simeq \mathbf{B}G$ is the [[delooping]] of an [[∞-group]] $G \in Grp(\mathbf{H})$. (In typical applications in [[physics]] we instead have the differential refinement $\mathbf{B}G_{conn}$ (see below at _[Examples -- Gauge fields](#GaugeFields)_) and the following discussion is directly generalized to that case. )

1. [Background fields as principal ∞-bundles](#BriefReviewOfPrincipalInfinityBundlesAsBackgroundFields)

1. [Fields as sections of associated fiber ∞-bundles](#FieldsAsSectionsOfAssociatedBundles)

#### Background fields as principal $\infty$-bundles
 {#BriefReviewOfPrincipalInfinityBundlesAsBackgroundFields}

We briefly recall the central aspects of [[principal ∞-bundles]] in the [[(∞,1)-topos]] $\mathbf{H}$.

For $X \in \mathbf{H}$ any [[object]] and $x \colon * \to \X$ a [[global element]], the [[homotopy pullback]] ([[(∞,1)-pullback]]) of the point along itse is the based [[loop space object]]

$$
  \Omega_x X  \coloneqq \{x\} \underset{X}{\times} \{x\}
  \,.
$$

Via composition of loops, this canonically has the structure of an [[A-∞ algebra]] object such that the [[truncated object in an (∞,1)-category|0-truncation]] $\tau_0 \Omega_x X$ is a [[monoid object]] which is a [[group object]]. Such _groupal $A_\infty$-algebra objects_ are _[[group objects in an (∞,1)-category|group objects]]_ in $\mathbf{H}$: [[∞-groups]].

In fact every [[∞-group]] is of this form. Moreover, restricted to [[pointed object|pointed]] and [[connected object in an (∞,1)-topos|connected objects]], the [[looping and delooping|looping]] [[(∞,1)-functor]] $\Omega$ is an [[equivalence of (∞,1)-categories]]

$$
  Grp(\mathbf{H})
  \stackrel{\overset{\Omega}{\leftarrow}}{\underoverset{\mathbf{B}}{\simeq}{\to}}
  \mathbf{H}^{*/}_{\geq 1}
  \,.
$$

Its inverse $\mathbf{B}$ we call the [[delooping]] operation. Notice that this means that we can conveniently discuss all aspects of [[∞-groups]] without ever explicitly considering [[A-∞ algebra]] structure by instead working with the pointed connected objects $\mathbf{B}G$.

Notably one finds that a $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ is equivalently the [[homotopy fiber]] of a map $g \;\colon\; X \to \mathbf{B}G$

$$
  \array{
     fib(g) \simeq & P &\to& * & \simeq \mathbf{E}G
     \\
     & \downarrow && \downarrow
     \\
     & X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

This construction yields an [[equivalence of ∞-groupoids]]

$$
  G Bund(X)
  \stackrel{\overset{fib}{\leftarrow}}{\underoverset{}{\simeq}{\to}}  
  \mathbf{H}(X, \mathbf{B}G)
$$

between $G$-[[principal ∞-bundles]] with [[gauge transformations]] between them and $G$-[[cocycles]] with [[coboundaries]]. In particular this means that $G$-[[principal ∞-bundles]] are classified by $G$-[[cohomology]] in $\mathbf{H}$

$$
  G Bund(X)_{/\sim}
  \simeq
  \pi_0 G Bund(X)
  \stackrel{\simeq}{\to}
  \pi_0 \mathbf{H}(X, \mathbf{B}G)
  \simeq
  H^1(X,G)
  \,.
$$

Hence if $\mathbf{BgFields} \simeq \mathbf{B}G$ then a [[background field]] on $X$ is equivalently a $G$-[[principal ∞-bundle]] on $X$. 


#### Fields as sections of associated fiber $\infty$-bundles
 {#FieldsAsSectionsOfAssociatedBundles}



+-- {: .num_prop #EquivalenceOfActionCategoryWithSlice}
###### Proposition

For $G \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, the [[(∞,1)-functor]] that sends an [[∞-action]] $\rho$ of $G$ on some $V \in \mathbf{H}$ to the corresponding [[associated ∞-bundle]] of the $G$-[[universal principal ∞-bundle]] is an [[equivalence of (∞,1)-categories]]

$$
  (\mathbf{E}G)\times_G(-)
  \;\colon\;
  G Act(\mathbf{H})
  \stackrel{\simeq}{\to}
  \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

Moreover there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category|equivalence]]

$$
  (\mathbf{E}G)\times_G V
  \simeq
  {*} \times_G V
  \simeq
  V//G
$$

with the [[quotient]] of $V$ by the $G$-[[∞-action]] $\rho$ (this is the general abstract and version and geometric refinement of the traditional [[Borel construction]]). 

=--

+-- {: .num_defn }
###### Definition

For $\rho$ an [[∞-action]] of an [[∞-group]] $G \in Grp(\mathbf{H})$ on some $V \in \mathbf{H}$ we write

$$
  V//G \stackrel{\overline{\rho}}{\to} \mathbf{B}G
$$

for the image of $\rho$ under the equivalence of prop. \ref{EquivalenceOfActionCategoryWithSlice}.

=--

+-- {: .num_prop }
###### Proposition

The [[homotopy fiber]] of $\overline{\rho}$ is $V$, hence we have a [[homotopy fiber sequence]]

$$
  \array{
    V &\to& V//G
    \\
    && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    && \mathbf{B}G
  }
$$

identifying $\overline{\rho}$ with a $V$-[[fiber ∞-bundle]] over $\mathbf{B}G$. Moreover, this is the _[[universal associated ∞-bundle|universal rho-associated ∞-bundle]]_: for every $G$-[[principal ∞-bundle]] $P \to X$ with modulating map $g_X \;\colon\; X \to \mathbf{B}G$ there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category]]

$$
  P \times_G V \simeq g_X^*(\overline{\rho})
$$

in $\mathbf{H}_{/X}$.

=--

+-- {: .num_remark }
###### Remark

In summary this means that an [[∞-action]] $\rho$ of an [[∞-group]] $G$ on any object $V \in \mathbf{H}$ is equivalently a [[homotopy fiber sequence]] of the form

$$
  \array{
    V &\to& V//G 
    \\
    && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

Moreover, for $P \to X$ any $G$-[[principal ∞-bundle]] modulated by a map $g ;\colon\; X \to \mathbf{B}G$ and for $\rho$ an [[∞-action]] of $G$ on some $V$, there is an [[(∞,1)-pullback]] diagram

$$  
  \array{
    P \times_G V
    &\to&
    V//G
    \\
    \downarrow && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

=--



Due to the [[universal property]] of the [[(∞,1)-pullback]] this has the following consequence which, basic as it is, is fundamental for the interpretation of fields in def. \ref{FieldsInAnActionFunctional}.

+-- {: .num_prop }
###### Proposition

There is a canonical [[equivalence in an (∞,1)-category]] between the [[sections]] of the $\rho$-[[associated ∞-bundle]] $P \times_X G$ and maps $g_X \to \overline{\rho}$ in the slice, hence fields in the sense of def. \ref{FieldsInAnActionFunctional} with background field $g_X$ and moduli stack $\overline{\rho}$:

$$
  \mathbf{\Gamma}_X(P \times_G V)
  \simeq
  [g_X, \overline{\rho}]_{\mathbf{H}}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

This equivalence is constituted simply by forming the [[pasting diagram]] of the [[section]] with the above $(\infty,1)$-pullback

$$  
  \array{
    && P \times_G V
    &\to&
    V//G
    \\
    &{}^{\mathllap{\sigma}}\nearrow& \downarrow && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    X &\stackrel{id}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    X &&\stackrel{\sigma}{\to}&& V//G
    \\
    & {}_{\mathllap{g}}\searrow && \swarrow_{\overline{\rho}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--

The following further central property leads in the [following section](#RelationToTwistedCohomology) to an equivalent re-formulation of this in [[twisted cohomology]].

+-- {: .num_prop }
###### Proposition

Every $G$-[[principal ∞-bundle]] $P \to X$ in an [[(∞,1)-topos]] $\mathbf{H}$ is _locally trivizable_ in that there exists a [[1-epimorphism]] $p \;\colon\; U \to X$ and an [[(∞,1)-pullback]] [[diagram]] of the form

$$
  \array{
    U \times G &\to& P
    \\
    \downarrow && \downarrow
    \\
    U &\stackrel{p}{\to}& X
  }
$$

or equivalently a diagram

$$
  \array{
    U &\to& *
    \\   
    \downarrow^{\mathrlap{p}}
    &\swArrow_{\simeq}&
    \downarrow
    \\
    X & \stackrel{g}{\to} & \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Together the above facts imply that for 

$$
  \array{
     && P \times_G V &\to& V//G
     \\
     & {}^{\mathllap{\sigma}}\nearrow & \downarrow
     && \downarrow^{\mathrlap{\overline{\rho}}}
     \\
     X &\stackrel{id}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

a [[section]] of the [[associated ∞-bundle]], the restriction $\sigma|_U$ of the section along the trivializing cover $p \;\colon\; U \to X$ factors through $V \to V//G$:

$$
  \array{
     && V &\to& V//G
     \\
     & {}^{\mathllap{\sigma|_U}}\nearrow &  && \downarrow^{\mathrlap{\overline{\rho}}}
     \\
     U &\stackrel{p}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

This means that a section of an [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]] is locally a $V$-valued map, hence a [[cocycle]] in $\Omega V$-[[cohomology]].

=--

And so we say that _globally_ it is a "twisted" $\Omega V$-cocycle. This leads to the following equivalent description.



### Relation to twisted cohomology
 {#RelationToTwistedCohomology}

We discuss here how def. \ref{FieldsInAnActionFunctional} of fields has an entirely equivalent expression in terms of _[[cocycles]]_ in general _[[cohomology]]_ and in fact, if the background field is nontrivial, in _[[twisted cohomology]]_.
This follows by direct comparison with the corresponding notions in _[[cohomology]]_ and _[[twisted cohomology]]_ as discussed there ([NSS](#NSS)). The unification of notions seen this way gives a natural home for instance to the familiar observations such as that [[Chan-Paton gauge fields]] on [[D-branes]] are identified with [[cocycles]] in  ([[differential K-theory|differential]]) [[twisted K-theory]] (see _[Chan-Paton gauge fields](#ChanPatonGaugeFields)_ below).

First observe the following


+-- {: .num_remark}
###### Remark

For $\phi \;\colon\; \Phi_X \to \mathbf{Fields}$ a field configuration as in def. \ref{FieldsInAnActionFunctional} in the corresponding [[diagram]] in $\mathbf{H}$

$$
  \array{
     X &&\stackrel{\phi}{\to}&& \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields}
     \\
     & {}_{\mathllap{\Phi_X}}\searrow 
     &\swArrow& 
     \swarrow_{\mathrlap{\mathbf{Fields}}}
     \\
     && \mathbf{BgFields}
  }
$$

we have the following equivalently identifications when interpreting this as a [[cocycle]]:

* the object $\mathbf{Fields} \in \matbbf{H}_{/\mathbf{BgFields}}$ is the **[[local coefficient ∞-bundle]]**;

* the [[homotopy fiber]] $V$ of $\underset{\phi \in [X, \mathbf{Fields}]}{\sum}\mathbf{Fields} \to \mathbf{BgFields}$ is the **local [[coefficient]]** for a [[cohomology]] theory;

* the [[background field]] $\Phi_X$ is the **[[twisted cohomology|twist]]**

* the field $\phi \colon \Phi_X \to \mathbf{Fields}$ is 

  * a **[[cocycle]]** in $\Phi_X$-[[twisted cohomology]] on $X$ with local [[coefficients]] $V$

  * equivalently: a **$\Phi_X$-twisted [[G-structure|V-structure]]** on $X$;

* a [[gauge transformation]] is a **[[coboundary]]** in $\Phi_X$-twisted $V$-cohomology;

* the [[equivalence classes]] of fields are the $\Phi_X$-[[twisted cohomology|twisted]] $V$-[[cohomology]] of [[spacetime]] $X$

  $$
    H_{[\Phi_X]}(X,V) \simeq \tau_0\Gamma[X,\mathbf{Fields}]_{\mathbf{H}}
    \,.
  $$

=--

We see several illustrations of these identifications in the list of _[Examples](#Examples)_ below. More generally, there is a canonical identification of physical fields in the presence of background fields _and_ boundary/defect with twisted and _[[relative cohomology]]_. This we discuss below in _[Relation to relative cohomology](#RelationToRelativeCohomology)_.



### Relation to relative cohomology
 {#RelationToRelativeCohomology}


When we refine background fields to dynamical fields as
discussed above in _[Boundary and defect fields](#BoundaryAndDefectFields)_ then the identification of fields with [[cocycles]] in [[twisted cohomology]] as discussed above in 
_[Relation to twisted cohomology](#RelationToTwistedCohomology)_ accordingly generalized a bit: it becomes a combination of twisted cohomology and _[[relative cohomology]]_.

For consider the special case that the moduli of defect fields are trivial, hence that 

$$
  \mathbf{Fields} \colon * \stackrel{pt_Q}{\to} \mathbf{Fields}_{bulk}
$$

is the global point inclusion into the bulk field moduli (the trivial bulk field).  By prop. \ref{ModuliOfBulkAndDefectFieldsAsPullback} it follows that

+-- {: .num_prop }
###### Proposition

There is a natural equivalence

$$
  [\iota_X, pt_A]
  \simeq
  [X_{bulk}, A] \underset{[X_{def}, A]}{\times} {*}
  \,,
$$

hence a [[homotopy fiber sequence]]

$$
  [\iota_X, pt_A]
   \to 
  [X_{bulk}, A]
   \to 
  [X_{def}, A]
$$

=--

+-- {: .num_remark }
###### Remark

This identifies the equivalence classes of global points in $[\iota_X, pt_A]$ as the 
$\iota_X$-[[relative cohomology|relative A-cohomology]] of $X$.

=--

In general, if the defect fields are not trivial, the fields $\iota_X \to \mathbf{Fields}$ (hence ordinary cocycles in $\mathbf{H}^{(\Delta^1)}$) are a kind of cocycles in $\mathbf{H}$ that are a combination of relative and twisted cocycles: instead with their pullback to $X_{def}$ being equipped with a trivialization, it is equipped with a "twisted trivialization" in the sense of [[twisted differential c-structure|twisted c-structures]], discussed [below](#TwistedDifferentialcStructurs).


## Examples
 {#Examples}

We distinguish four broad classes of examples of physical fields, according to def. \ref{FieldsInAnActionFunctional}:

1. [Scalar and moduli fields](#SclarModuliFields)

   The simplest type of field is a ([[smooth function|smooth]]) [[function]] on [[spacetime]] $X$ with values in the [[real numbers]] or [[complex numbers]], called a _[[scalar field]]_. Slightly more generally there are fields which are [[functions]] into some other [[vector space]] or more general [[manifold]], often called _linear/non-linear [[sigma-model]]_ fields. Often that manifold is a space of parameters of some [[geometry]], for instance of a compact space in [[Kaluza-Klein compactification]], in which case these fields are often called _moduli fields_. Scalar fields may be _charged_ under force fields, which we turn to next.

1. [Force fields](#ForceFields)

   1. [Fields of gravity, G-structure and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry)

      In this case the [[background gauge field]] is a [[G-structure]], the [[moduli stack]] of fields is a [[delooping|delooped]] [[∞-group extension]] $\mathbf{B}\hat G \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G$ and a field is a generalized [[vielbein]] exhibiting a [[reduction and lift of structure groups|reduction/lift of structure group]].

   1. [Gauge fields](#GaugeFields)

      In this case $\mathbf{Fields}$ is a [[moduli space]] $\mathbf{B}G_{conn}$ of [[connections on an ∞-bundle|∞-connections]] on $G$-[[principal ∞-bundles]] for some [[gauge group]] $G \in Grpd(\mathbf{H})$.

1. [Matter fields](#MatterFields)

   In this case the [[background gauge field]] is a $G$-[[principal ∞-bundle]] $P$ for some [[gauge group]] $G \in Grp(\mathbf{H})$ and $\mathbf{Fields}$ is the univeral $\rho$-[[associated ∞-bundle]] $V//G \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G$ for $\rho$ an [[∞-action]] of $G$ on some $V \in \mathbf{H}$. A field is [[section]] of the [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]].

   
Not all examples fall squarely into one of these types, some are mixtures of these. Relevant examples we discuss in

* [Fields combining various of these properties](#FieldCombiningVariousProperties)

In particular the moduli stacks $\mathbf{B}G$ here are typically all differentially refined to moduli stacks $\mathbf{B}G_{conn}$ of [[connection on an ∞-bundle|∞-connections]] so that for instance every [[reduction and lift of structure groups]] goes along with a corresponding data of the reduction of an [[connection on an ∞-bundle|∞-connection]]. The archetypical example for this are [[spin connections]], see the example _[Ordinary gravity](#OrdinaryGravity)_ below.

+-- {: bluebox}
###### Examples ######

1. [Sigma-model fields](#SigmaModelFields)

   1. [Uncharged scalar particle](#UnchargedScalarField)

   1. [Particle trajectors](#ParticleTrajectory)

   1. [Brane trajectory](#BraneTrajectory)

   1. [Open string sigma-model](#OpenStringSigmaModelFields)

1. [Force fields](#ForceFields)

   1. [Fields of gravity, G-structure and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry)

   1. [General -- G-structure: twisted lift of structure group](##GStructure)

   1. [Gravity](#OrdinaryGravity)

   1. [Spin structures](#SpinStructures)

   1. [Spin-c structures](#SpinStructures)

   1. [Type II gravity, exceptional geometry](##TypeIIGravity)

   1. [Higher spin structures](#HigherSpinStructures)

   1. [Higher spin-c structures](#HigherSpincstructures)

1. [Gauge fields](#GaugeFields)

   1. [General -- Coefficients in differential cohomology: connections](#GaugeFieldsGeneral)

   1. [Electromagnetic field](#ElectromagneticField)

   1. [Yang-Mills field](#YangMillsField)

   1. [Kalb-Ramond B-field](#KalbRamondBField)

   1. [Supergravity C-field](#SupergravityCField)

1. [Matter fields](#MatterFields)

   1. [General -- Sections of associated bundles](#SectionsOfAssociatedBundles)

   1. [Fermions](#Fermions)

   1. [Tensor fields](#TensorFields)

1. [Fields combining these properties](##FieldCombiningVariousProperties)

   1. [General -- Twisted differential cocycles and c-structures](#TwistedDifferentialcStructurs)

   1. [Nonabelian charged particle trajectories -- Wilson lines](#NonabelianChargedParticle)

   1. [3d Chern-Simons field with Wilson line](#ChernSimonsWithWilsonLines)

   1. [Chan-Paton gauge bundles on D-branes: twisted differential K-cocycles](#ChanPatonGaugeFields)

   1. [Anomaly-free heterotic string background: differential String-c structures](#HeteroticStringBackgroundField)

=--


### **0)** Sigma-model fields
 {#SigmaModelFields}

Traditionally a [[sigma-model]] field is a type of fields given simply by ([[smooth function|smooth]]) [[functions]] $\Sigma \to X$ from a [[worldvolume]] $\Sigma$ to a [[target space]] $X$. Now, by the general unified definition def. \ref{FieldsInAnActionFunctional} and as shown in the following sections, in [[higher geometry]] _every_ type of field is of this form if we allow [[target space]] $X$ to be a general [[∞-stack]] and functions to be maps in a suitable [[slice (∞,1)-topos]]. Nevertheless, here we start with briefly indicating those examples that are [[sigma-model]] fields also in the traditional restrictive sense of the term.

#### Uncharged scalar field
 {#UnchargedScalarField}

A _[[scalar field]]_ is given simply by a [[function]] on [[spacetime]]/[[worldvolume]], typically with values in the [[real numbers]] $\mathbb{R}$ ("real scalar field") or the [[complex numbers]] $\mathbb{C}$ ("complex scalar field"). Hence this is the example of def. \ref{FieldsInAnActionFunctional} with trivial [[background fields]]

$$
  \mathbf{BgFields} \coloneqq *
$$

(the [[terminal object]]) and with the field moduli stack being the map

$$
  \mathbf{Fields} \;\colon\; \mathbb{R} \to *
$$

from (the [[smooth manifold]] underlying) the [[real numbers]] to the point, or else

$$
  \mathbf{Fields} \;\colon\; \mathbb{C} \to *
$$

regarded as an object in $\mathbf{H}_{/*} \simeq \mathbf{H}$.

[[scalar field|Scalar fields]] are, due to their simplicity, prominent in toy examples used to discuss general properties of [[quantum field theory]]. The only  fundamental scalar particle observed in nature to date is the [[Higgs particle]] (or presumably so, in [[technicolor]] models it is not actually fundamental but a composite of [[fermion]] particles, discussed [below](#Fermions)), but the Higgs field is, crucially, charged under the [[electroweak field|electroweak]] [[special unitary group|SU(2)]]-[[gauge field]]. A [[model (in theoretical physics)|model]] of relevance in [[phenomenology]] which crucially features an uncharged scalar particle is [[cosmic inflation]]. But the fundamental nature of the [[inflaton field]] is hypothetical (if it exists at all), it might well be the [[effective QFT|effective]] version of non-scalar fields.

#### Particle trajectory
 {#ParticleTrajectory}

The dynamics of a [[particle]] propagating in a [[spacetime]] $X$ is described by a field on the abstract [[worldline]] which is simply a [[smooth function]] $\mathbb{R} \to X$ to the [[target space]] $X$: a [[trajectory]] of the particle. The [[quantum mechanics]] that describes the [[dynamics]] of such a quantum particle is equivalently a 1-dimensional field theory on the [[worldline]], with these maps as its physical fields. 

Therefore such wordline [[sigma-model]] fields are given by the special case of def. \ref{FieldsInAnActionFunctional} with trivial [[background field]] $\mathbf{BgFields} \simeq *$ and with $\mathbf{Fields} \;\colon\; X \to * $ regarded as an object in $\mathbf{H}_{/*} \simeq \mathbf{H}$. 


#### Brane trajectory
 {#BraneTrajectory}

More generally, the [[worldvolume]] fields of any [[brane]] [[sigma-model]] with [[target space]] $X$ are given as [above](#ParticleTrajectory).

#### Open string sigma-model
 {#OpenStringSigmaModelFields}

+-- {: .num_remark}
###### Remark

A [[D-brane]] inclusion $Q \stackrel{\iota_X}{\to} X$ is the [[target space]] for an [[open string]] with [[worldsheet]] $\partial \Sigma \stackrel{\iota_\Sigma}{\hookrightarrow} \Sigma$: a [[field (physics)|field]] configuration of the open string [[sigma-model]] is a map

$$
  \phi \;\colon\; \iota_\Sigma \to \iota_X
$$

in $\mathbf{H}^{\Delta^1}$, hence a [[diagram]] of the form

$$
  \array{
    \partial \Sigma &\stackrel{\phi_{bdr}}{\to}& Q
    \\
    \downarrow^{\mathrlap{\iota_\Sigma}} 
     &\swArrow& 
    \downarrow^{\mathrlap{\iota_X}}
    \\
    \Sigma &\stackrel{\phi_{bulk}}{\to}& X
  }
  \,.
$$

For $X$ and $Q$ ordinary [[manifolds]] just says that a field configuration is a map $\phi_{bulk} \;\colon\; \Sigma \to X$ subject to the constraint that it takes the [[boundary]] of $\Sigma$ to $Q$. This means that this is a [[trajectory]] of an [[open string]] in $X$ whose endpoints are constrained to sit on the [[D-brane]] $Q \hookrightarrow X$.

If however $X$ is more generally an [[orbifold]], then the [[homotopy]] filling the above diagram imposes this constraint only up to orbifold transformations, hence exhibits what in the physics literature are called "orbifold twisted sectors" of open string configurations.

=--

+-- {: .num_prop #TheTypeIIOpenStringSigmaModelModuliStackOfFields}
###### Proposition

The [[moduli stack]] $[\iota_\Sigma, \iota_X]$ of such field configurations is the [[homotopy pullback]] 

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    \\
    \downarrow &\swArrow& \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
  }
  \,.
$$

=--

The [[background gauge field]] for such a [[sigma-model]] is a [[B-field]] on $X$ and a [[Chan-Paton gauge field]] on $Q \hookrightarrow X$.

### **I)** Force fields
 {#ForceFields}

We discuss examples for the two classes of [[force]] fields, which are:

* [Fields of gravity, G-structure and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry);

* [Gauge fields](#GaugeFields).


#### **I a)** Fields of gravity, $G$-Structure and generalized geometry
 {#FieldsOfGravityAndGeneralizedGeometry}

We discuss the example of the field of [[gravity]], below in _[Gravity](#OrdinaryGravity)_, and various closely related types of fields that all encode [[geometry]] in some sense, in fact all encode geometry in the sense of _[[G-structure]]_. This most general case we discuss in _[G-structure -- (twisted lift of structure ∞-groups)](#GStructure)_.

##### **General** -- $G$-structure: (twisted) lift of structure $\infty$-group
 {#GStructure}

Let 

$$
  A \to \hat G \stackrel{\mathbf{p}}{\to} G
$$

be an [[∞-group extension]] in $\mathbf{H}$. Then for $g_X \colon X \to \mathbf{B}G$ a given $G$-[[principal ∞-bundle]], a [[lift of the structure group]] from $G$ to $\hat G$ is a field

$$
  \phi \; \colon\; g_X \to \mathbf{B p}
  \,.
$$

If the [[∞-group extension]] is central in that it extends to a [[homotopy fiber sequence]] of the form

$$
  \mathbf{B}A \to \mathbf{B}\hat G \stackrel{\mathbf{Bp}}{\to} \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^2 A
$$

then a [[twisted differential c-structure|twisted c-structure]] is a map

$$
  \phi 
   \;\colon\;
  g_X \to \mathbf{c}
$$

in $\mathbf{H}_{/\mathbf{B}G}$.
These kinds of fields are interpreted as fields of [[gravity]] and its variants, as shown by the following examples.

For recognizing traditional constructions in this formulation, the following basic fact is important.

+-- {: .num_prop #CosetIsHomotopyFiberOfDeloopedInclusion}
###### Proposition

For $\iota \colon H \hookrightarrow G$ an [[subgroup]] inclusion of [[Lie groups]], we have a [[homotopy fiber sequence]]

$$
  G/H \to \mathbf{B}H \stackrel{\mathbf{B}\iota}{\to} \mathbf{B}G
$$

with the [[coset space]] on the left.

=--



##### Gravity
 {#OrdinaryGravity}

We discuss the formulation of the field of [[gravity]] as a special case of def. \ref{FieldsInAnActionFunctional}.

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, let 

$$
  \mathbf{Fields} 
  \;\colon\;
  \mathbf{B}O(n)
   \stackrel{\mathbf{OrthStruc}_n}{\to}
  \mathbf{B}GL(n)
$$

be the [[delooping]] of the [[Lie group|Lie]]-[[subgroup]] inclusion of the [[orthogonal group]] into the [[general linear group]] in [[dimension]] $n$ (the inclusion of the [[maximal compact subgroup]]).

For $X \in $ [[SmoothMfd]] $\hookrightarrow$ $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] a [[smooth manifold]] of [[dimension]] $n$, write

$$
  \Phi_X \coloneqq \tau_X \;\colon\; X \to \mathbf{B}GL(n)
$$

for the canonical map modulating the $GL(n)$-[[principal bundle]] to which the [[tangent bundle]] is canonically [[associated bundle|associated]].

=--

+-- {: .num_example #RiemannianVielbein}
###### Example

Morphisms

$$
  \phi \;\colon\; \tau_X \to \mathbf{OrthStruc}_n
$$

in $\mathbf{H}_{/\mathbf{B}GL(n)}$ hence [[diagrams]]

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B}O(n)
    \\
    & \searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

in $\mathbf{H}$ are equivalently [[vielbein]] fields $e$ exhibiting the [[reduction of the structure group]] from $GL(n)$ to $O(n)$. A [[gauge transformation]] is a local frame transformation. Hence 

$$
  [\tau_X, \mathbf{OrthStruc}_n]_{\mathbf{H}}
  \in 
  \mathbf{H}
$$

is the [[moduli stack]] of [[Riemannian metrics]] on $X$. Every such is a field configuration of ordinary [[gravity]] on $X$. (But see example \ref{GenerallyCovariantFieldOfGravity} below.)

According to 
remark \ref{PullbackAlongGeneralizedLocalDiffeomorphisms} such fields pull back along map $f \colon Y \to X$ that fit into a diagram

$$
  \array{
    Y &&\stackrel{f}{\to}&& X
    \\
    & {}_{\mathllap{\tau_Y}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\tau_X}}
    \\
    && \mathbf{B}GL(n)
  }
  \,.
$$ 

These are precisely [[local diffeomorphisms]] and indeed these are precisely the maps along which [[vielbein]] fields / [[pseudo-Riemannian metric]] fiedls pull back. (Pullback along [[smooth functions]] may not preserve the non-degeneracy of a metric tensor, but precisely the local diffeomorphisms do.)

=--


+-- {: .num_remark}
###### Remark

The [[smooth structure]] on $X$ as embodied by $\tau_X$ is the [[background field]] in example \ref{RiemannianVielbein}.

=--

+-- {: .num_remark #OrthogonalStructureIsTrivialInPlainHomotopyTheory}
###### Remark

Under [[geometric realization of cohesive infinity-groupoids|geometric realization]] 

$$
  {\vert-\vert}
  \;\colon\;
  \mathbf{H} \to \infty Grpd \simeq L_{whe} Top
$$

the map of [[moduli stacks]] $\mathbf{B}O(n) \to \mathbf{B}GL(n)$ becomes an [[equivalence]] (a [[weak homotopy equivalence]]) of [[classifying space]] $B O(n) \stackrel{\simeq}{\to} B GL(n)$.

This means that in plain [[homotopy theory]], hence ignoring the [[geometry]], a lift in 

$$
  \array{
    && B O(n)
    \\
    & \nearrow & \downarrow
    \\
    X &\stackrel{\tau_X}{\to}& B GL(n)
  }
$$

is no information, up to equivalence: it always exists and exists uniquely up to a contractible space of choices. In order for such a lift really to be equivalently an [[orthogonal structure]] it needs to be taken with geometry included, hence for [[moduli stacks]] (_[[cohesive (infinity,1)-topos|cohesive]]_ [[homotopy type]]) as above.

The analog statement is true for every delooping $\mathbf{B}H \to \mathbf{B}G$ of the inclusion $H \hookrightarrow G$ of a [[maximal compact subgroup]] into a [[Lie group]]. More examples of this kind we discuss below in _[Type II Gravity and generalized geometry](#TypeIIGravity)_.

=--

+-- {: .num_remark}
###### Remark

The [[homotopy fiber]] of $\mathbf{OrthStruc}_n$ is the [[coset space]] $GL(n)//O(n)$, hence we have a [[homotopy fiber sequence]] of [[moduli stacks]] of the form

$$
  GL(n)//O(n)
  \to
  \mathbf{B}O(n)
  \stackrel{\mathbf{OrthStruc}_n}{\to}
  \mathbf{B}GL(n)
$$

in $\mathbf{H}$. This means that locally, over a [[cover]] ([[1-epimorphism]]) $p \colon U \to X$ over which the [[tangent bundle]] has a trivialization $\tau_X|_U \simeq *$, the space of fields is simply $[U, GL(n)//O(n)]$.

=--

The next example is the differential refinement of the previous one.

+-- {: .num_example}
###### Example

Let 

$$
  \widehat \mathbf{OrthStruc}_n
  \;\colon\;
  \mathbf{B}O(n)_{conn}
  \to 
  \mathbf{B}GL(n)_{conn}
$$

be the canonical differential refinement of $\mathbf{OrthStruc}_n$, where now the [[moduli stacks]] of [[principal connections]] appear. For $X$ a manifold as above, let then

$$
  \hat \tau_X 
  \;\colon\;
  X 
  \to
  \mathbf{B}GL(n)_{conn}
$$

modulate an [[affine connection]] on the [[tangent bundle]]. A field 

$$
  \phi \;\colon\; \hat \tau_X \to \widehat \mathbf{OrthStruc}_n
$$

is now still equivalently just a [[vielbein]], but its component

$$
  \underset{\mathbf{B}GL(n)_{conn}}{\sum} \hat \tau_X
  \;\colon\;
  X \to \mathbf{B}O(n)_{conn}
$$

now captures the orthognal connection which in the physics literature is often called (inaccurately) the _[[spin connection]]_, denoted $\omega$. The [[vielbein]] then exhibits the original [[affine connection]] as that whose components are the [[Christoffel symbols]] $\Gamma$ of the [[Riemannian metric]] defined as above, a relation that is familiar from the physics literature in the form of the [[equation]]

$$
  \omega = e^{-1}\Gamma e + e^{-1} d e
$$

between local connection 1-form components.

=--

But both these examples do not fully accurately reflect the field content of [[gravity]] yet. This is because the [[theory (physics)|theory]] of [[gravity]] is supposed to by [[general covariance|generally covariant]]. This means that for two [[vielbein]] field configurations as in example \ref{RiemannianVielbein} such that one goes into the other under a [[diffeomorphism]] of [[spacetime]] $X$, there is a [[gauge transformation]] between them.

+-- {: .num_example #GenerallyCovariantFieldOfGravity}
###### Example

Write $\mathbf{Diff}(X) \coloneqq \mathbf{Aut}(X) \in Grp(\mathbf{H})$ for the [[diffeomorphism group]] of the [[smooth manifold]] $X$. There is then the canonical [[∞-action]] of the [[automorphism ∞-group]] $\mathbf{Diff}(X)$ on $X$ itself, exhibited by the universal [[associated ∞-bundle]]

$$
  \left(X // \mathbf{Diff}\left(X\right) \to \mathbf{B}\mathbf{Diff}\left(X\right) \right)
  \in 
  \mathbf{H}_{/\mathbf{B}\mathbf{Diff}\left(X\right)}
  \,.
$$

This induces also an [[∞-action]] also on the [[tangent bundle]].

Moreover the trivial bundle

$$
  \mathbf{Fields}
  \coloneqq
  (\mathbf{Diff}(X)\times \mathbf{OrthStruc} \to \mathbf{B}\mathbf{Diff}(X) )
  \in 
  \mathbf{H}_{/\mathbf{B}\mathbf{Diff}(X)}
$$

corresponds to the trivial action.

Then

$$
  \underset{\mathbf{B}Diff(n)}{\sum}
  \underset{\mathbf{B}(GL(n))}{\prod} 
  [\tau_X, \mathbf{Fields}]
 \in \mathbf{H}
$$

is the accurate space of [[general covariance|generally covariant]] fields of [[gravity]]. 

=--


##### $Spin$-structures
 {#SpinStructures}

In theories with [[fermions]] (discussed [below](#Fermions)) the field of [[gravity]] is more refined than just a [[vielbein field]] as [above](#OrdinaryGravity), hence an [[orthogonal structure]] on [[spacetime]]: it also involves an [[orientation structure]] and a [[spin structure]].

To see that these structures are really all (fields) of the same kind, observe that they are the lifts through the first step of the [[Whitehead tower]] of $\mathbf{B}GL$, as shown in the following table

[[!include higher spin structure - table]]

Notice, as in remark \ref{OrthogonalStructureIsTrivialInPlainHomotopyTheory}, that for the interpretation of the first step here it is crucial to interpret this in [[moduli ∞-stacks]] and not in [[classifying spaces]].

Hence if a background field of [[gravity]] is assumed, $\mathbf{BgFields} \colon \mathbf{B}O(n)$, $\Phi_X = e_X$, then the moduli stack for [[orientation structure]]-fields is

$$
  \mathbf{Fields} \colon \mathbf{B} SO(n) \to \mathbf{B}O(n)
$$

in $\mathbf{H}_{/\mathbf{B}O(n)}$. And if an orientation background field is assumed, $\mathbf{BgFields} \colon \mathbf{B}SO(n)$, $\Phi_X = o_X$, then the moduli stack for [[spin structure]]-fields is

$$
  \mathbf{Fields} \colon \mathbf{B} Spin(n) \to \mathbf{B}SO(n)
  \,.
$$

Evidently there is then also a notion of [[higher spin structure]]-fields. These appear as backgrounds when one passes from [[spinning particles]] to  [[spinning strings]] and then to further "spinning" [[branes]]. This we discuss below in _[Higher spin structures](#HigherSpinStructures)_.

##### $Spin^c$-structures
 {#SpinStructures}

Some [[theory (physics)|theories]] involve not plain [[spin structures]] but [[spin-c structures]] on their [[spacetime]]/[[worldvolume]] (for instance in [[Seiberg-Witten theory]] or in the [[gauge theory]] over [[D-branes]] in [[type II string theory]], see the example _[Chan-Paton gauge fields on D-branes](#ChanPatonGaugeFields)_ below). By the discussion there, the [[moduli stack]] $\mathbf{B}Spin^c(n)$ for 
[[spin^c group]]-[[principal bundles]] sits in the [[homotopy pullback]] diagram

$$
  \array{
    \mathbf{B}Spin^c &\to& \mathbf{B}U(1)
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 \,mod\, 2}}
    \\
    \mathbf{B}SO(n) &\stackrel{\mathbf{w}_2}{\to}&
   \mathbf{B}^2\mathbb{Z}_2
  }
 \,,
$$

where the right vertical map represents the universal [[first Chern class]] modulo 2. In other words this says that a [[spin^c-structure]] on some $X$ is a [[twisted differential c-structure|twisted w2-structure]] with twist the first Chern-class of a [[circle bundle]].

So if that circle bundle is regarded as a [[background field]]

$$
  \phi_X \coloneqq g_X \;colon\; X \to \mathbf{B}U(1)
$$

then a $Spin^c$-structure for that underlying circle bundle is a field

$$
  \phi 
    \;\colon\;
  \Phi_X \to \mathbf{w}_2
$$

in $\mathbf{H}_{/\mathbf{B}^2 \mathbb{Z}_2}$.

Or rather, if $X$ is a [[manifold]] as before and the $SO(n)$-principal bundle involved in the above is required to be a [[reduction of the structure group|reduction]] of the [[tangent bundle]] $\tau_X : X \to \mathbf{B}GL(n)$ as before, then the [[background field]] for $Spin^c$-structure fields is

$$
  \Phi_X 
   \;\colon\;
   X 
   \stackrel{(\tau_X, g_X \,mod\, 2)}{\to}
   \mathbf{B}GL(n) \times \mathbf{B}^2 \mathbb{Z}_2
  \,,
$$

and the field moduli stack is 

$$
  \mathbf{Fields} \;\colon\; 
  \mathbf{B}SO(n)
   \stackrel{(p, \mathbf{w}_2)}{\to}
  \mathbf{B}GL(n) \times \mathbf{B}
  \,.
$$



##### Type II gravity, exceptional geometry
 {#TypeIIGravity}

By remark \ref{OrthogonalStructureIsTrivialInPlainHomotopyTheory} above the ordinary field of [[gravity]] on some [[manifold]] $X$ is equivalently a [[reduction of the structure group]] from the [[general linear group]] to its [[maximal compact subgroup]], regarded as a field whose [[background field]] is the [[tangent bundle]] itself.

If one instead considers a variant of the [[tangent bundle]] as a [[background field]] -- a _[[generalized tangent bundle]]_ $\tau_X^{gen} : X \to \mathbf{B}G$ -- with some other structure [[Lie group]] $G$, then a field with values in 

$$
  \mathbf{Fields} 
    \;\colon\;
  \mathbf{B}H \to \mathbf{B}G
$$

in $\mathbf{H}_{/\mathbf{B}G}$ and for $H \hookrightarrow$ the inclusion of the [[maximal compact subgroup]], may be thought of as an accordingly  _generized field of gravity_ defining a _generalized_ [[Riemannian geometry]].

Such fields naturally appear in [[theory (physics)|theories]] of higher-dimensional [[supergravity]], where related to the [[T-duality]] and more generally [[U-duality]] structure of these [[theory (physics)|theories]].

Notably in manifestly [[T-duality]]-equivariant [[type II supergravity]] the [[generalized tangent bundle]] on the $n$-dimensional [[spacetime]] is an $O(n,n)$-[[principal bundle]] $\tau^{gen}_X \;\colon\; X \to \mathbf{B}O(n,n)$. The corresponding [[maximal compact subgroup]] inclusion yields the moduli stack of fields

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}(O(n)\times O(n))
  \to
  \mathbf{B}O(n,n)
$$

and a field $\phi \;\colon\; \tau_X^{gen} \to \mathbf{Fields}$ is equivalently the [[generalized vielbein]] for the generalized Riemannian geometry called  _[[type II geometry]]_ on $X$. 

In fact also the generalized tangent bundle itself should be regarded as a field: Notice that the canonical diagonal inclusion

$$
  GL(n) \hookrightarrow O(n,n)
$$

does not have a [[retraction]]. Write $GL(n) \hookrightarrow G_{geom} \hookrightarrow O(n,n)$ for the maximal subgroup for which a retrection to $GL(n)$ still exists, called the **geometric subgroup** in the context of [[type II geometry]]. Then a lift of the tangent bundle to $G_{geom}$

$$
  \array{
    X &&\stackrel{\tau_X^{gen}}{\to}&& \mathbf{B}G_{geom} & \hookrightarrow& \mathbf{B} O(n,n)
    \\
    & {}_{\athllap{\tau_X}}\searrow &\swArrow& \swarrow_{\mathrlap{\mathbf{p}}}
    \\
    && \mathbf{B}GL(n)
  }
  \,,
$$

hence a field 

$$
  e_X^{gen} \;\colon\; \tau_X \to \mathbf{p}
$$ 

is what is called a _geoemtric_ [[generalized tangent bundle]]. These are exactly the generalized tangent bundles primarily considered in the literature (see at _[[type II geometry]]_  for more).

In the [[Kaluza-Klein compactification]] of [[type II supergravity]] and of [[11-dimensional supergravity]] preserving some amount of global [[supersymmetry]] this generalized type II geometry is further enhanced to various flavors of what is called  [[exceptional generalized geometry]]. 

Here the [[generalized tangent bundle]] has as structure group an [[exceptional Lie group]] from the $E$-series $E_{n(n)}$ (for compactification on an $n$-dimensional compact space). The moduli stack of fields is then

$$
  \mathbf{Fields} 
  \;\colon\;
  \mathbf{B} K_{n}
  \to 
  \mathbf{B} E_{n(n)}
$$

and a field $ e_X^{gen} \;\colon\; \tau_X^{gen} \to \mathbf{Fields}$ is equivalently a [[generalized vielbein]]  for  [[exceptional generalized geometry]].



##### Higher spin structures
 {#HigherSpinStructures}

By the discussion of [Spin structure fields](#SpinStructures) above there are evident higher analogs, obtained by climbing through the [[Whitehead tower]] [[higher spin structure - table|of BO]].

In the next step we have _[[String structure]]_-fields which are maps to

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}String \to \mathbf{B}Spin
  \,.
$$

These appear as fields in [[heterotic supergravity]] with [[quantum anomaly]]-cancellation by the [[Green-Schwarz mechanism]] and for trivial [[gauge field]]. In the presence of a non-trivial gauge field these are further refined to _[Higher spin-c structrures](#HigherSpincstructures)_ discussed below. This field content of [[heterotic supergravity]] is discussed in more detail below in _[Anomaly-free heterotic supergravity fields -- differential String-c structures](#HeteroticStringBackgroundField)_.

Further up the [[Whitehead tower]] _[[Fivebrane structure]]_-fields are maps to

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Fivebrane \to \mathbf{B}String
$$

in $\mathbf{H}_{/\mathbf{B}String}$. These, or their twisted variants, appear in [[dual heterotic string theory]]. 


##### Higher $Spin^c$-structures
 {#HigherSpincstructures}

As discussed above, an ordinary [[spin-c structure]] is really a [[spin structure]] which is _[[twisted differential c-structure|twisted]]_ by the class of a $U(1)$-[[principal bundle]]. 

Similarly the [[higher spin structure]]-fields just discussed have further twistes by background unitary bundles. For

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \to \mathbf{B}^3 U(1)
$$

some [[universal characteristic map]] on [[moduli ∞-stacks]], for $\mathbf{B}^3 U(1)$ the moduli 3-stack of [[circle n-bundle with connection|circle 3-bundles]], hence [[circle 3-group]]-[[principal ∞-bundles]] we say that the [[smooth ∞-group]] $String^{\mathbf{c}}$ appearing in the [[homotopy pullback]] diagram

$$
  \array{
    \mathbf{B}String^{\mathbf{c}}
    &\to&
    \mathbf{B} G
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{c}}}
    \\
    \mathbf{B}Spin &\stackrel{\tfrac{1}{2}\mathbf{p}}{\to}&
    \mathbf{B}^3 U(1)
  }
$$

is a higher [[string 2-group]]-analog of [[spin^c]]. 

In particular, if $G$ is a compact, connected and simply connected [[simple Lie group]] (such as the [[spin group]] or the [[special unitary group]]) then 

$$
  \pi_0\mathbf{H}(\mathbf{B}G, \mathbf{B}^3 U(1)) 
  \simeq
  H^4(BG, \mathbb{Z}) 
  \simeq 
  \mathbb{Z}
$$

(the first equivalence is discussed at _[[Lie group cohomology]]_ as a special case of a theorem discussed at _[[smooth infinity-groupoid]]_). This means that there is an essentially unique map of higher moduli stacks

$$
  \mathbf{c}
  \;\colon\;
  \mathbf{B}G
  \to \mathbf{B}^3 U(1)
$$

which maps to the generator of $H^4(BG, \mathbb{Z})$ under [[geometric realization of cohesive infinity-groupoids]]. For $G = Spin$ this is the smooth refinement of the [[first fractional Pontryagin class]] $\tfrac{1}{2}\mathbf{p}_1$, discussed further at _[[twisted differential string structure]]_. 

Of interest in [[heterotic supergravity]] here is the case that $G = E_8 \times E_8$ (the product of the  [[exceptional Lie group]] $E_8$ with itself) and $\mathbf{c}$ is twice the canonical string class.

If then $g_X \;\colon\; X \to \mathbf{B}(E_8 \times E_8)$ is the [[instanton sector]] of the gauge field in [[heterotic supergravity]] regarded as a [[background gauge field]] for the field of heterotic [[gravity]], then with  

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin \stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to} \mathbf{B}^3 U(1)
$$

a map

$$
  g_X \to \mathbf{Fields}
$$

in $\mathbf{H}_{/\mathbf{B}^3 U(1)}$ is a $\mathbf{String}^{\mathbf{c}}$-structure on $X$ whose underlying gage bundle is the given $\Phi_X$. 

As before for $Spin^c$-structures, in applications one in addition demands that this $\mathbf{String}^{\mathbf{c}}$-structure is indeed a refinement of the field of [[gravity]] of the theory, which means that one takes the [[background field]] to be

$$
  \Phi_X
  \;\colon\;
  X
  \stackrel{(\tau_X, g_X)}{\to} \mathbf{B}GL(n) \times \mathbf{B}(E_8 \times E_8)
$$

and the moduli $\infty$-stack of fields to be

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin(n)
  \stackrel{(p, \tfrac{1}{2}\mathbf{p}_1)}{\to}
  \mathbf{B}GL(n) \times \mathbf{B}^3 U(1)
  \,.
$$

These are precisely the [[instanton sectors]] of the fields of [[Green-Schwarz mechanism|Green-Schwarz anomaly free]] [[heterotic supergravity]], discussed further below in _[Anomaly-free heterotic supergravity fields](#HeteroticStringBackgroundField)_. ([SSS](#SSS))

#### **I b)** Gauge fields
 {#GaugeFields}

##### **General** -- Coefficients in differential cohomology: $\infty$-connections
 {#GaugeFieldsGeneral}

The term _gauge field_ in _[[gauge theory]]_ with respect to a [[gauge group]] $G$ refers to fields which are modeled by [[connection on a bundle|connections]] either on $G$-[[principal bundles]] or on [[associated bundles]] for these. The notion of [[equivalence]] between two such fields (hence between [[connections on bundles]]) is the original meaning of the word _[[gauge transformation]]_, even though that term is also used for equivalences between fields which are not modeled by connections.

We discuss the general notion of gauge fields and then various special cases and variants. The following table gives an overview over the notions involved in the concept of gauge fields

[[!include gauge field - table]]

+-- {: bluebox}
###### Contents: ######

1. [Electromagnetic field](#ElectromagneticField)

1. [Yang-Mills field](#YangMillsField)

1. [Kalb-Ramond B-field](#KalbRamondBField)

1. [Supergeometric B-field](#SupergeometricBField)

1. [Supergravity C-field](#SupergravityCField)

=--


##### Electromagnetic field
 {#ElectromagneticField}

A field configuratiotion of the [[electromagnetic field]] is a [[circle n-bundle with connection|circle bundle with connection]] and a [[gauge transformation]] of the EM field is an equivalence of such connections.

Let therefore

$$
  \mathbf{B}U(1)_{conn}
  \coloneqq
  \Omega^1//U(1)
  \simeq
  DK(U(1) \stackrel{d log}{\to} \Omega^1)
$$

be the [[quotient stack]] of the [[action]] of $U(1)$ on the [[sheaf]] of [[differential 1-forms]], equivalently the image under the [[Dold-Kan correspondence]] of the sheaf of [[chain complexes]] given by the [[Deligne complex]] for degree-2 [[ordinary differential cohomology]], as indicated.

This is the [[moduli stack]] for $U(1)$-[[principal connections]]. Hence setting $\mathbf{BgFields} \simeq *$ and 

$$
  \mathbf{Fields} \coloneqq \mathbf{B}U(1)_{conn}
$$

in def. \ref{FieldsInAnActionFunctional} yields the type of the electromagnetic field.


##### Yang-Mills field
 {#YangMillsField}

More generally, let $G$ be a [[Lie group]], and $\mathfrak{g}$ its [[Lie algebra]]. Write $\Omega^1(-,\mathfrak{g})$ the sheaf of [[Lie algebra valued 1-forms]]

+-- {: .num_defn #ModuliStackOfGPrincipalConnection}
###### Definition

The **moduli stack of $G$-[[principal connections]]** is the [[quotient stack]]

$$
  \mathbf{B}G_{conn}
  \coloneqq
  \Omega^1(-,\mathfrak{g})//G
$$

of the [[action]] of $G$ on it [[Lie algebra valued differential forms]] by [[gauge transformations]] 

$$
  g \colon A^g \coloneqq \mapsto A^g Ad_g A + g^* \theta 
  \,.
$$ 

=--

This is the [[moduli stack]] of the $G$-[[Yang-Mills field]]. Hence setting $\mathbf{BgFields} \simeq *$ and

$$
  \mathbf{Fields} \coloneqq \mathbf{B}G_{conn}
$$

in def. \ref{FieldsInAnActionFunctional} yields [[Yang-Mills fields]].



##### Kalb-Ramond $B$-field
 {#KalbRamondBField}

Let 

$$
  \mathbf{B^2}U(1)_{conn}
  \coloneqq
  \Omega^{2 \leq \bullet \leq 1} // \mathbf{B}U(1)
  \simeq
  DK(U(1) \stackrel{d log}{\to} \Omega^1 \stackrel{d}{\to} \Omega^2)
$$

be the image under the [[Dold-Kan correspondence]] of the [[Deligne complex]] for degree-3 [[ordinary differential cohomology]]. This is the [[moduli infinity-stack|moduli 2-stack]] for [[circle n-bundle with connection|circle 2-bundle with connections]].

Setting $\mathbf{BgFields} \simeq *$ and

$$
  \mathbf{Fields} \coloneqq \mathbf{B}^2 U(1)_{conn}
$$

in def. \ref{FieldsInAnActionFunctional} yields the 2-form 
gauge field known as the _[[B-field]]_ or the _[[Kalb-Ramond field]]_.

##### Supergeometric $B$-field
 {#KalbRamondBField}

The [[B-field]] appears both in [[bosonic string theory]] as well as in [[type II superstring theory]]. In ([Distler-Freed-Moore](#Precis)) it was pointed out that for the [[superstring]] the plain formulation [above](#KalbRamondBField) needs to be refined. We discuss here the natural  formulation of this observation in [[smooth super infinity-groupoid|higher supergeometry]] as in ([FSS CSIntroAndSurvey, section 4.3](#FiorenzaSatiSchreiberCSIntroAndSurvey)).

Generally instead of the [[circle group]] $U(1)$ one can consider the [[multiplicative group]] $\mathbb{C}^\times$ of non-zero [[complex numbers]]. The canonical [[subgroup]] inclusion $U(1) \hookrightarrow \mathbb{C}^\times$ induces for each $n \in \mathbb{N}$ a canonical morphism of [[moduli ∞-stacks]]

$$
  \mathbf{B}^n U(1) \to \mathbf{B}^n \mathbb{C}^\times
  \,.
$$

This is not quite an [[equivalence]] of [[∞-stacks]] but it is a [[shape modality]]-equivalence in that [[geometric realization of cohesive ∞-groupoids]] sends it to an equivalence as

$$
  {\vert \mathbf{B}^n U(1)\vert}
  \simeq
  {\vert \mathbf{B}^n \mathbb{C}^\times\vert}
  \simeq
  K(\mathbb{Z}, n+1)
  \,.
$$

For instance smooth $U(1)$-[[principal bundles]] and $\mathbb{C}^\times$-[[principal bundles]] are both classified by the universal [[Chern class]] in $H^2(-, \mathbb{Z})$ but the [[gauge transformation|gauge]] [[automorphisms]] of the trivial $U(1)$-principal bundle form $C^\infty(-,U(1))$, while that of the trivial $\mathbb{C}^\times$-principal bundle form the larger $C^\infty(-,\mathbb{C}^\times)$.

Both versions of the moduli $n$-stack of $n$-bundles have their use. The version $\mathbf{B}^n \mathbb{C}^\times$ has the advantage that it is actually equivalent to the moduli $n$-stack of complex line $n$-bundles.

$$
  \mathbf{B}^n \mathbb{C}^\times \simeq n Line_\mathbb{C}
  \,.
$$

Specifically for $n = 2$ it is equivalent to the moduli 2-stack of [[line 2-bundles]]

$$
  \mathbf{B}^2 \mathbb{C}^\times \simeq 2 Line_\mathbb{C}
  \,.
$$

But now in [[supergeometry]] [complex super-line 2-bundle](http://ncatlab.org/nlab/show/line%202-bundle#SuperLine2BundlesAndTwistedK) have a richer classification that plain [[line 2-bundle]]. 
Explicitly, let now $\mathbf{H} \colon $ [[SmoothSuper∞Grpd]] be the ambient [[cohesive (∞,1)-topos]] for higher [[supergeometry]] and write

$$
  2\mathbf{sLine}_{\mathbb{C}}
  \in 
  \mathbf{H}
$$

for the 2-stack of [complex super-line 2-bundle](http://ncatlab.org/nlab/show/line%202-bundle#SuperLine2BundlesAndTwistedK). 

This has [[categorical homotopy groups in an (infinity,1)-topos|homotopy sheaves]] 

| $k$  | $\pi_k( 2 \mathbf{sLine})$ |
|--|--|
| 0 | $\mathbb{Z}_2$  |  
| 1 | $\mathbb{Z}_2$ |
| 3 | $\mathbb{C}^\times$ |

in the [[topos]] over [[supermanifolds]]. The $\pi_0(2 \mathbf{sLine}) \simeq \mathbb{Z}_2$ says that locally there is not just one super line 2-bundle, namely the standard line 2-bundle, but also its odd "superpartner". 

Under [[geometric realization of cohesive infinity-groupoids|geometric realization]] ${\vert-\vert} \;\colon\; \mathbf{H} \to \infty Grpd \simeq L_{whe} Top$ we have the [[homotopy type]] ${\vert 2 \mathbf{sLine}\vert}$ with [[homotopy groups]]

| $k$  | $\pi_k({\vert 2 \mathbf{sLine}\vert})$ |
|--|--|
| 0 | $\mathbb{Z}_2$  |  
| 1 | $\mathbb{Z}_2$ |
| 3 | $0$ |
| 4 | $\mathbb{Z}$ |

Since $2 \mathbf{sLine}$ is the [[Picard 3-group]] of the monoidal 2-stack $2 \mathbf{sVect}$ of super [[2-vector bundles]] it is a supergeometric [[3-group]]. Therefore there is the further [[delooping]] $\mathbf{B}2\mathbf{sLine}$ and hence the differential refinement $2\mathbf{sLine}_{conn}$ in the [[(∞,1)-pullback]] diagram

$$
  \array{
    2\mathbf{sLine}_{conn} &\to& \Omega^3_{cl}
    \\
    \downarrow && \downarrow
    \\
    2 \mathbf{sLine} &\stackrel{curv}{\to}& \flat_{dR} \mathbf{B}2 \mathbf{sLine}
  }
  \,.
$$

This is now the moduli 2-stack

$$
  \mathbf{Fields} \coloneqq 2\mathbf{2Line}_{conn}
  \;\;
  \in SmoothSuper\infty Grpd
$$

for the [[B-field]] in [[type II string theory]].



##### Supergravity $C$-field
 {#SupergravityCField}

Proceeding in this fashion, let 

$$
  \mathbf{B^3}U(1)_{conn}
  \coloneqq
  \Omega^{3 \leq \bullet \leq 1} // \mathbf{B}^2 U(1)
  \simeq
  DK(U(1) \stackrel{d log}{\to} \Omega^1 \stackrel{d}{\to} \Omega^2 \stackrel{d}{\to}\Omega^3)
$$

be the image under the [[Dold-Kan correspondence]] of the [[Deligne complex]] for degree-4 [[ordinary differential cohomology]]. This is the [[moduli infinity-stack|moduli 3-stack]] for [[circle n-bundle with connection|circle 3-bundle with connections]].

Fields whose moduli stack is

$$
  \mathbf{Fields} \;\colon\; \mathbf{B}^3 U(1)_{conn} \to *
$$ 

are one component of the [[supergravity C-field]].


### **II)** Matter fields
 {#MatterFields}

Fundamental [[matter]]-fields as they appear in the [[standard model of particle physics]], hence fundamental [[fermions]] such as [[electrons]], [[quarks]] and [[neutrinos]], are [[sections]] of a $G$-[[associated bundle]] $E \to X$ on [[spacetime]], where $G$ is the [[gauge group]] of the [[force]] fields that interact with the matter fields and where $E \to X$ is [[associated bundle|associated]] to the [[principal bundle]] underlying such a force [[gauge field]], as discussed in _[Gauge fields](#GaugeFields)_ above, and, if we are talking indeed about fermions, to the [[spin bundle]] given by the gravity-spin structure field discussed in _[Gravity and generalized geometry](#MatterFields)_ above.

More precisely, fermioninc matter fields are sections of these bundles regarded in [[supergeometry]] with the fibers regarded as odd-graded. (...)


#### **General** -- sections of associated fiber $\infty$-bundles
 {#SectionsOfAssociatedBundles}

We start by discussing the general mechanism by which [[sections]] of $\rho$-[[associated ∞-bundles]] are an example of the general definition \ref{FieldsInAnActionFunctional}.

For $G \in \Grp(\mathbf{H})$ a geometric [[∞-group]], there is an [[equivalence of (∞,1)-categories]]

$$
  G Act \simeq \mathbf{H}_{/\mathbf{B}G}
$$

between that of [[∞-actions]] of $G$ and the [[slice (∞,1)-topos]] of $\mathbf{H}$ over the [[delooping]] $\mathbf{B}G$ of $G$. Under this equivalence an [[∞-action]]/[[∞-representation]] of $G$ on some $V \in \mathbf{H}$ is equivalently a [[homotopy fiber sequence]] of the form

$$
  \array{
    V &\to& V//G
    \\
    && \downarrow^{\overline \rho}
    \\
    && \mathbf{B}G
  }
$$ 

in $\mathbf{H}$. This is the [[universal associated ∞-bundle|universal rho-associated ∞-bundle]]: for $P \to X$ any $G$-[[principal ∞-bundle]] with modulating map $g_X \;\colon\; X \to \mathbf{B}G$ the corresponding [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]] is naturally equivalent to the [[(∞,1)-pullback]] of $\overline{\rho}$ along $g$:

$$
  P \times_G V \simeq g_X^*(\overline{\rho})
  \,.
$$

From this and the [[universal property]] of the [[(∞,1)-pullback]] one finds that a [[section]] of the [[associated ∞-bundle]] $P \times_G V \to X$ is equivalently a map

$$
  \phi : g_X \to \overline{\rho}
$$
  
in $\mathbf{H}_{/\mathbf{B}G}$.

This means that such sections are fields in the sense of def. \ref{FieldsInAnActionFunctional} where

* $\mathbf{BgFields} \simeq \mathbf{B}G$;

* the [[background field]] is the moduli $g_X$;

* the [[moduli ∞-stack]] of fields is $\overline{\rho} \in \mathbf{H}_{/\mathbf{B}G}$.



#### Fermions
 {#Fermions}

[[fermion]]:

$S$ a [[spin representation]]

$$
  \mathbf{Fields} 
  \;\colon\;
  S//Spin
  \to 
  \mathbf{B}Spin
$$

in [[supergeometry]] (...)

* [[electron]], [[quark]]

* [[gravitino]] ([[Rarita-Schwinger field]]), [[gluino]]

#### Tensor fields
 {#TensorFields}

While the term _physical field_ probably orignates from _[[tensor field]]_, few fields are fundamentally given by tensor fields. Nevertheless, tensor fields, being [[sections]] of a [[tensor product]] of copies of the [[tangent bundle]] and the [[cotangent bundle]] are certainly examples of the general notion of field as in def. \ref{FieldsInAnActionFunctional}. Gere we spell this out.

For $X$ a [[smooth manifold]], a [[tensor field]] of rank $(p,q)$ is a [[section]] of the [[tensor product]] bundle

$$
  \Gamma(T X)^{\otimes_{C^\infty(X)} p} \otimes_{C^\infty(X)} \Gamma(T^* X)^{\otimes q}
  \,. 
$$

This is canonically the [[associated bundle]] to the $GL(n)$-[[principal bundle]] which to which the [[tangent bundle]] is also canonically associated, by the given [[representation]] of $GL(n)$ on $\mathbb{R}^{n(p+q)}$.

The [[universal associated ∞-bundle]] of this representation is 

$\mathbf{Fields} 
\;\colon\; \mathbb{R}^{n (p+q)}//GL(n) \to \mathbf{B}GL(n) $.

Hence for $\tau_X \colon X \to \mathbf{B}GL(n)$ the canonical map, the space of $(p,q)$-tensor fields on $X$ is

$$
  [\tau_X, \mathbf{Fields}]_{\mathbf{H}}
  \in
  \mathbf{H}
  \,.
$$

By passing to [[irreducible representations]] in the above, we obtain specifically the corresponding subclasses of tensor fields, such as [[differential forms]].




### Fields combining these properties
 {#FieldCombiningVariousProperties}

The above distinction of types of physical fields into into [Sigma-model fields](SigmaModelFields), [Force fields of gravity](#FieldsOfGravityAndGeneralizedGeometry), [Gauge force fields](#GaugeFields) and [Matter fields](#MatterFields) can be helpful for reasoning about fields and types of [[theories (physics)|theories in physics]], but is not fundamental. The general definition \ref{FieldsInAnActionFunctional} of which all these types are examples reflects that. In fact, one way to read that definition and the above list of examples is to say that it shows that in [[higher geometry]] _all_ types of fields are [[sigma-model]] fields: they are all given as maps $\Phi_X \to \mathbf{Fields}$ from a domain [[spacetime]]/[[worldvolume]]+[[background field]] $\Phi_X$ to a generalized [[target space]] $\mathbf{Fields}$ (the [[moduli ∞-stack]] of fields in the given [[slice (∞,1)-topos]] characterized by the nature of the [[background fields]]).

Accordingly, a general physical field in a general [[theory (physics)|theory]] does not fall squarely into one of the above categories, but combines aspects of all of these. Here we discuss such examples. 

#### **General** -- Twisted differential-cocycles and -$\mathbf{c}$-structures
 {#TwistedDifferentialcStructurs}

We have seen that the [[moduli ∞-stack]] of a field of plain [[gravity]] or general geometry is a map $\mathbf{c} \colon \mathbf{B}\hat G \to \mathbf{B}G$ of [[moduli ∞-stack]] of [[principal ∞-bundles]], regarded as an object in the [[slice (∞,1)-topos|slice]] $\mathbf{H}_{/\mathbf{B}G}$, and that the [[moduli ∞-stack]] of a plain $G$-[[gauge field]] is that of [[principal ∞-connections]] $\mathbf{B}G_{conn}$. These two concepts have an evident unification if $\mathbf{c}$ has a differential refinement $\at \mathbf{c}$ to a map of differential moduli stacks

$$  
  \array{
    \mathbf{B}\hat G_{conn} &\stackrel{\hat \mathbf{c}}{\to}&
   \mathbf{B}G_{conn}
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}\hat G &\stackrel{\mathbf{c}}{\to}&
     \mathbf{B}G
  }
  \,,
$$

regarded then as an object in the slice $\mathbf{H}_{/\mathbf{B}G_{conn}}$.

Since, as discussed [above](#GStructure), a field with coefficients in $\mathbf{c}$ is equivalently a _twisted $\mathbf{c}$-structure_, we may calla field with coefficients in $\hat \mathbf{c}$ a 
**[[twisted differential c-structure]]**.

Moreover, we have seen that [matter fields](#MatterFields) have 
[[moduli ∞-stacks]] coming not from a direct [[delooping]] $\mathbf{B}G \simeq *//G$ of an [[∞-group]] $G$, but from the [[homotopy quotient]] $V//G$ of an [[∞-action]] of $G$ on some object $V$. Combining this with differential refinement as above we consider fields whose [[moduli ∞-stacks]] are maps

$$
  (V//G)_{conn}
  \stackrel{\hat \mathbf{c}}{\to}
  (\mathbf{B}G)_{conn}
  \;\;\;\;
  \in \mathbf{H}_{/\mathbf{B}G_{conn}}
  \,.
$$

This is a differential refinement of fields which are [[cocycles]] in [[twisted cohomology]] with local [[coefficients]] $V$, hence **twisted differential cohomology**. The above case of [[twisted differential c-structures]] is a special case of this for $V \simeq \mathbf{B}A$ the [[delooping]] of the [[∞-group]] that [[∞-group extension|extended]] $G$ to $\hat G$.

Some further slight variants of these combinations appear in the examples below. 

#### Nonabelian charged particle trajectories -- Wilson line
 {#NonabelianChargedParticle}

We describe here a variant of the particle propagating on a spacetime $X$, where now the particle is charged under a [[background gauge field]] for a nonabelian [[gauge group]] $G$. 


Let $G$ be a [[simple Lie group]] which is connected, simply connected and [[compact Lie group|compact]].

Let $\rho$ be an [[irreducible representation|irreducible]] [[unitary representation]] of $G$ under which the particle is to be [[charge (physics)|charged]]. By the [[Borel-Weil-Bott theorem]] this corresponds equivalently to a [[weight (in representation theory)|weight]]

$$
  \langle \lambda, -\rangle
  \in
  \mathfrak{g}^*
  \,.
$$

Let $T \simeq G_\lambda \hookrightarrow G$ be the [[maximal torus]] which is the [[stabilizer subgroup]] that fixes this weight under the [[coadjoint action]] of $G$ on its dual [[Lie algebra]] $\mathfrak{g}^*$.

Set then in def. \ref{FieldsInAnActionFunctional} the [[moduli stack]] of [[background fields]] to be 

$$
  \mathbf{BgField} \colon \Omega^1(-,\mathfrak{g})//G \simeq \mathbf{B}G_{conn}
  \;\;\;
  \mathbf{H}
$$

as in def. \ref{ModuliStackOfGPrincipalConnection}. Moreover, let the moduli $\infty$-stack of fields in $\mathbf{H}_{/\mathbf{B}G_{conn}}$ be given by the canonical map

$$
  \mathbf{Fields} 
  \;\colon\;
  \Omega^1(-,\mathfrak{g})//T
  \to 
  \Omega^1(-,\mathfrak{g})//G
  \simeq
   \mathbf{B}G_{conn}
$$

which is induced by the defining inclusion of $T$.

+-- {: .num_remark}
###### Remark

For $U \in$ [[CartSp]] $\hookrightarrow \mathbf{H}$ a field $\phi \colon U \to \Omega^1(-,\mathfrak{g})//T$ is equivalently a [[Lie algebra valued form]] $A \in \Omega^1(U,\mathfrak{g})$, but a [[gauge transformation]] of such a field is constrained to be a smooth $T$-valued function $t \in C^\infty(U,T) \hookrightarrow C^\infty(U, G)$ instead of an arbitrary $G$-valued function.

=--

+-- {: .num_remark}
###### Remark

With these definitions we have for $X$ a [[manifold]] that

* a [[background gauge field]] $\Phi_X \;\colon\; X \to \mathbf{B}G_{conn}$ is equivalently a $G$-[[principal connection]] on $X$ (which if $G$ is assumed connected and simply connected and $\Sigma$ is of [[dimension]] at most 3 is equivalently just a [[Lie algebra valued form]]);

* a field configuration is a diagram in $\mathbf{H}$ of the form

  $$
    \array{  
      X &&\stackrel{\nabla^g}{\to}&& \Omega^1(-,\mathfrak{g})//T
      \\
      & {}_{\nabla}\searrow &\swArrow_{g}& \swarrow_{\mathrlap{\mathbf{Fields}}}
      \\
      && \mathbf{B}G_{conn}
    }
    \,,
  $$
  
  which is equivalently a differentially refined [[reduction of the structure group]] of the $G$-[[principal bundle]] underlying $\nabla$. If $\nabla$ is given by a globally defined connection form $A$ then this is equivalently just a smooth $G$-valued function $g$ on $X$ that takes $A$ to $A^g$ as indicated. 

=--

As a slight variant of prop. \ref{CosetIsHomotopyFiberOfDeloopedInclusion} we have

+-- {: .num_prop}
###### Proposition

We have a [[homotopy fiber sequence]]

$$
  \mathcal{O}_\lambda \simeq G/T \to \Omega^1(-,\mathfrak{g})//T
  \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G_{conn}
  \,,
$$

where on the left we have the [[coadjoint orbit]] of $\langle \lambda , -\rangle$.

=--

+-- {: .num_remark}
###### Remark

This implies that if $\nabla = 0$ is the trivial background field, than fields $\phi : X \to \mathbf{Fields}$ are equivalently maps to the coadjoint orbit

$$
  [X, \mathbf{Fields}]_{\mathbf{H}}|_{\Phi_X = 0}
  \simeq
  C^\infty(X, \mathcal{O}_\lambda)
  \,.
$$

Hence in this sector we have simply a [[sigma-model]] field as in [Sigma-models](#SigmaModelFields) above. 

=--


+-- {: .num_remark}
###### Remark

There is a canonical [[extended Lagrangian]] on $[X, \mathbf{Fields}]_{\mathbf{H}}$ with the above definitions, whose [[action functional]], if $X = S^1$ is the closed connected 1-dimensional manifold,  is that of a [[1d Chern-Simons theory]]. The [[partition function]] of the corresponding [[quantum field theory]] is the [[holonomy]] map  -- the "[[Wilson line]]" -- on the background gauge field connection $\nabla$.

=--

This is discussed further at [geometry of physics -- Prequantum gauge theory and gravity](#ActionFunctionalsForChernSimonsTypeGaugeTheories).


#### 3d Chern-Simons field with Wilson line
 {#ChernSimonsWithWilsonLines}

We discuss the field content of 3d [[Chern-Simons theory]] for a simple, simply connected compact Lie group with [[Wilson loops]].
This is an example of _[Bulk fields with defect fields](#BoundaryAndDefectFields)_.

Let $\Sigma_3 \in SmthMfd \hookrightarrow \mathbf{H}$ be a [[smooth manifold]] of [[dimension]] 3, and let

$$
  C_X \;\colon\; S^1 \to \Sigma^3
$$

be the [[submanifold|embedding]] of a [[knot]]. Let the moduli of fields be

$$
  \mathbf{Fields}
  : 
  \Omega^1(-,\mathfrak{c})//T \to \mathbf{B}G_{conn}
$$

as defined in _[Nonabelian charged particle trajectories -- Wilson lines](#NonabelianChargedParticle)_ above. Regarding the not inclusion as a defect in the 3-dimnensional manifold, a bulk-defect fiedl configuration according to def. \ref{ModuliOfBulkAndBoundaryFields} is a map

$$
  \phi 
   \;\colon\;
   C_X \to \mathbf{Fields}
$$

in $\mathbf{H}^{(\Delta^1)}$. This is equivalently a diagram

$$
  \array{
    S^1 &\stackrel{A|_{S^1}^g}{\to}& \Omega^1(-,\mathfrak{g})//T
    \\
    \downarrow^{\mathrlap{C}} &\swArrow_{g}& \downarrow
    \\
    \Sigma_3 &\stackrel{A}{\to}& \mathbf{B}G_{conn}
  }
$$

in $\mathbf{H}$. This in turn is equivalently

1. a [[Lie algebra valued form]] $A \in \Omega^1(\Sigma_3, \mathfrak{g})$ (the bulk [[gauge field]] of $G$-[[Chern-Simons theory]])

1. a $g$-valued function on the circle $g \in C^\infty(S^1, G)$

which determine a background gauge field $A|_{S^1}^g$ on the knot.

Moreover a [[gauge transformation]] between two such field configurations $\kappa \;\colon\; \phi \Rightarrow \phi'$ is equivalently a gauge transformaiton of $A$ and of $A|_{S^1}$ such that together they intertwine $g$ and $g'$. In particular if the bulk field is held fixed, then such a gauge transformation is a function $t \colon S^1 \to T$ such that $g' = t g$. This means that the gauge equivalence classes of field confiurations for fixed background gauge field are labeled by maps to the [[coadjoint orbit]] $\mathcal{O}_\lambda \simeq G/T$ as above.

This are the field confugurations for 3d [[Chern-Simons theory]] (see the discussion there) with Wilson lines ([FSS](#FiorenzaSatiSchreiberCSIntroAndSurvey)).


#### Chan-Paton gauge fields on D-branes: twisted differential K-cocycles
 {#ChanPatonGaugeFields}

We discuss the [[Chan-Paton gauge fields]] over [[D-branes]]
in [[type II string theory]].

The [[extension of groups]] $U(1) \to U(n) \to PU(n)$ sits in a long [[homotopy fiber sequence]] of $\infty$-stacks

$$
  U(1) \to U(n) \to PU(n) \to \mathbf{B}U(1)
  \to \mathbf{B}U(n) \to \mathbf{B}PU(n) \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
$$

Let

$$
  \mathbf{Fields}
  \colon
  (\mathbf{B}U(n)//\mathbf{B}U(1))_{conn}
  \to
  \mathbf{B}^2 U(1)_{conn}
$$

be the differential refinement of that universal [[Dixmier-Douady class]].

Let 

$$
  \iota_X   
    \;\colon\;
  Q \hookrightarrow X 
$$

be a [[submanifold]], to be thought of as a [[D-brane]] [[worldvolume]] in an ambient [[spacetime]] $X$.

 
Then a field configuration of the [[B-field]] on $X$ together with a compatible rank-$n$ gauge field on the [[D-brane]] is a map

$$
  \iota_X \to \mathbf{Fields}
$$

in $\mathbf{H}^{(\Delta^1)}$, hence a diagram in $\mathbf{H}$ of the form

$$
  \array{
    Q &\stackrel{}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))
    \\
    {}^{\iota_X}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\hat \mathbf{dd}_n}}
    \\
    X &\stackrel{\nabla_B}{\to}& \mathbf{B}^2 U(1)_{conn}
  }
$$

This identifies a  [[twisted bundle]] with connection on the D-brane whose twist is the class in $H^3(X, \mathbb{Z})$ of the bulk [[B-field]]. 

This relation is the Kapustin-part of the [[Freed-Witten-Kapustin anomaly]] cancellation for the [[bosonic string]] or else for the [[type II string]] on $Spin^c$ D-branes. ([FSS](#FiorenzaSatiSchreiberCSIntroAndSurvey))


+-- {: .num_remark }
###### Remark

If we regard the [[B-field]] as a [[background field]] for the [[Chan-Paton gauge field]], then remark \ref{PullbackAlongGeneralizedLocalDiffeomorphisms} determines along which maps of the B-field the Chan-Paton gauge field may be transformed. 

$$
  \array{
    Y &\stackrel{}{\to}& X &\stackrel{}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))_{conn}
    \\
    & \searrow & \downarrow & \swarrow
    \\
    &&\mathbf{B}^2 U(1)_{conn}
  }
  \,.
$$

On the local connection forms this acts as

$$
  A \mapsto A + \alpha
  \,.
$$

$$
  B \mapsto B + d \alpha
$$

This is the famous gauge transformation law known from the string theory literature.

=--


#### Anomaly-free heterotic string background: differential $String^c$-structure
 {#HeteroticStringBackgroundField}

Let

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin_{conn}
  \stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}
  \mathbf{B}^3 U(1)_{conn}
$$

Let 

$$
  \Phi_X \;\colon\; X \stackrel{g_X}{\to} \mathbf{B}(E_8 \times E_8)_{conn}
  \stackrel{\hat \mathbf{c}_2}{\to}
  \mathbf{B}^3 U(1)
$$

then fields are [[twisted differential string structures]] or equivalently
differential $\mathbf{String}^{\mathbf{c}}$-structure with underlying gauge bundle give by $\Phi_X$, the differential refinement of the discussion in _[Higher spin structure](#HigherSpinStructures)_ above. 

As in the discussion there, we implement the constraint that the string structure is on the tangent bundle $\tau_X \;\colol\; X \to \mathbf{B}GL(n)$ of the manifold by settting

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin_{conn}
  \stackrel{(p,\tfrac{1}{2}\hat \mathbf{p}_1)}{\to}
  \mathbf{B}GL(n)_conn \mathbf{B}^3 U(1)_{conn}
$$

and

$$
  \Phi_X
  \;\colon\;
  X
  \stackrel{(\nabla_X, \hat \mathbf{c}_2(g_X))}{\to}
  \mathbf{B}GL(n)_{conn} \times \mathbf{B}^3 U(1)_{conn}
  \,.
$$

Then a field $\phi \;\colon\; \Phi_X \to \mathbf{Fields}$ 
is the higher spin-connection version as discussed in _[Gravity](#OrdinaryGravity)_ above of a twisted differential string structure.

The moduli stack of these fields is that of background fields that satisfy the [[Green-Schwarz anomaly cancellation]] in [[heterotic supergravity]]. ([SSS](#SSS)).

## Related concepts

* [[field history]]

* [[field observable]]

[[prequantum field theory]]

* **physical field**

  [[free field]]

  [[gauge field]]

  [[superfield]]

  [[auxiliary field]]

  [[fiber bundles in physics]]

* [[BV-BRST formalism]]

  * [[antifield]], 

  * [[ghost]], [[antighost]]

* [[extended Lagrangian]], [[prequantum n-bundle]], [[action functional]]

* [[charge (physics)]]

* [[theory (physics)]]

* [[classical field theory]]

* [[quantum field theory]]

* [[perturbation theory]]

  * [[vacuum]], [[tachyon]]

[[!include holographic principle -- table]]

* [[concept with an attitude]]

## References

### Lecture notes and expositions

* _[[geometry of physics -- perturbative quantum field theory]]_, chaper _[3. Fields](https://ncatlab.org/nlab/show/geometry+of+physics+--+perturbative+quantum+field+theory#Fields)_

A survey of the main field species is given in 

* {#Kocic16} [[Mikica Kocic]], _Overview of the fields in QFT_, 2016 ([[FieldSpecies.pdf:file]])

Most of the above material as of 2013 was written as part of a lecture series

* [[Urs Schreiber]], _Higher Chern-Simons theory_, lecture series at _[Workshop on Topological Aspects of Quantum Field Theories, Singapore (14 - 18 Jan 2013)](http://www2.ims.nus.edu.sg/Programs/013wquantum/index.php)_ on the first sections at _[geometry of physics, II) Physics](geometry%20of%20physics#PHYSICS)_

A exposition specifically for gauge fields is also in 

* [[Urs Schreiber]], _[Examples for Prequantum field theories I: Gauge fields](https://www.physicsforums.com/insights/examples-prequantum-field-theories-gauge-fields/)_.

An exposition of the general formulation of fields in terms of [[moduli stacks]] in [[slice (∞,1)-toposes]] is in section 4 of 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_
 {#FiorenzaSatiSchreiberCSIntroAndSurvey}

Lecture notes on fields as discussed here with applications in [[string theory]] are in 

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, lecture notes at _[K-theory and Quantum Fields](http://maths-old.anu.edu.au/esi/2012/)_, ESI program June 2012

An introductory survey is also in section 1 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 {#dcct}


### Original articles on the general notion

For references on the tradtional formulation of physical fields by sections of _[[field bundles]]_ as discussed [above](#IdeaOfFieldBundlesAndItsProblems) see there references [[field bundle|there]].

The formulation of physical fields as [[cocycles]] in [[twisted cohomology]] in an [[(∞,1)-topos]] as in the _[Definition](#Definition)_-section above originates around

* [[Urs Schreiber]], _[[schreiber:Background fields in twisted differential nonabelian cohomology]]_, talk at _[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]_

Further articles since then are listed at 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

In particular the general notion of fields as [[twisted differential c-structures]] appears in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_ ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001))
 {#SSS}

and the general theory of [[cohomology]] and [[twisted cohomology]] with [[local coefficient ∞-bundles]] as referred to in _[Relation to twisted cohomology](#RelationToTwistedCohomology)_ above as well as the theory of [[associated ∞-bundles]] as in _[Sections of associated ∞-bundles](#SectionsOfAssociatedBundles)_ is laid out in

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_ ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

Some examples of fields in this sense are called "relative fields" in 

* [[Daniel Freed]], [[Constantin Teleman]], _Relative quantum field theory_ ([arXiv:1212.1692](http://arxiv.org/abs/1212.1692))
 {#FreedTeleman}

Discussion of [[AQFT]] with stacky fields and co-stacky [[local nets of observables]] is in 

* {#BeniniSchenkelSzabo15} [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Homotopy colimits and global observables in Abelian gauge theory_ ([arXiv:1503.08839](http://arxiv.org/abs/1503.08839))

### Original articles on special cases

The supergeometric nature of the [[B-field]] in [[type II string theory]] had been pointed out in 

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 {#Precis}

with a more detailed account in 

* [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_ ([pdf](http://www.ma.utexas.edu/users/dafr/ESI.pdf))
 {#FreedLectures}

The formulation of this in [[smooth super infinity-groupoids]] is ([FSS, section 4.3](#FiorenzaSatiSchreiberCSIntroAndSurvey)).

[[!redirects physical field]]
[[!redirects physical fields]]

[[!redirects quantum field]]
[[!redirects quantum fields]]

[[!redirects field (in physics)]]
[[!redirects fields (in physics)]]



