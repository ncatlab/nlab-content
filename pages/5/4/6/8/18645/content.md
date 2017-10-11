

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


> this entry is going to be one chapter of _[[geometry of physics]]_

> relevant background on geometryis in the chapters on

> [[geometry of physics -- smooth sets]], [[geometry of physics -- differential forms|differential forms]];

> [[geometry of physics -- supergeometry]].

$\,$

#A first idea of quantum field theory#
* table of contents
{:toc}

$\,$

This chapter gives an expository but rigorous introduction to the basic concepts
of [[relativistic quantum field theory|relativistic]] [[quantum field theories]], specifically those
that arise as the [[perturbative quantum field theory|perturbative]] [[quantization]] of a _[[Lagrangian field theory]]_
-- such as [[quantum electrodynamics]], [[quantum chromodynamics]], and [[perturbative quantum gravity]]
appearing in the [[standard model of particle physics]].

First we consider
[[classical field theory]] (or rather [[prequantum field theory]]) and
then its [[deformation quantization]] via [[causal perturbation theory]] to [[perturbative quantum field theory]].
This mathematically rigorous (i.e. clear and precise) formulation of the traditional informal lore
has come to be known as _[[perturbative algebraic quantum field theory]]_.

We aim to give a _fully [[local field theory|local]]_ discussion, where all structures arise
on the "[[jet bundle]] over the [[field bundle]]" (introduced [below](#FieldVariations) ) and "[[transgression|transgress]]" from there to the [[spaces of field histories]] over [[spacetime]] (discussed [further below](#ObservablesAndStates)).
This "[[schreiber:Higher Prequantum Geometry]]" streamlines traditional constructions and serves the conceptualization in the theory.

In full beauty these concepts are extremely general and powerful; but the aim here is to give a first precise idea of the subject, not
a fully general account.
Therefore we begin in the following with the special case where [[spacetime]] is [[Minkowski spacetime]], where the [[field bundle]] (def. \ref{Fields} below) is an ordinary [[trivial vector bundle]] and hence the [[Lagrangian  density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below) is globally defined.

We do however consider the proper [[differential geometry]] of the resulting [[spaces of field histories]] in  terms of
"[[cohesion|cohesive]] [[functorial geometry]]" embodied by ([[formal smooth set|formal]]) [[smooth sets]]  (see [below](#Geometry)) and hence (which works verbatim the same way) [[super smooth sets]]. This seamlessly subsumes the case that there are [[fermion|fermionic]] fields in the theory (as in any realistic field theory).
Notice that this does _not_ mean that we consider "[[supersymmetry]]" (though of course we could):
plain [[supergeometry]] is but the mathematical
incarnation of the [[Pauli exclusion principle]] for [[fermions]], a key aspect of the [[stability of matter]] in the [[observable universe]].

This comparatively simple setup already subsumes what is considered in most traditional texts on the subject. In subsequent sections we eventually discuss more general situations, where spacetime is allowed to be [[globally hyperbolic Lorentzian manifold|globally hyperbolic]] and the [[field bundle]] to be a [[super L-infinity algebra|super]]-[[derived Lie algebroid]]. This is then sufficient generality to capture the established perturbative [[BV formalism|BRST-BV quantization]] of [[gauge fields]] coupled to [[fermions]] [[AQFT on curved spacetime|on curved spacetimes]]
-- which is the state of the art.
Further generalization, necessary for the discussion of global topological effects such as [[instanton]] configurations
of [[gauge fields]] will be discussed elsewhere (see at _[[homotopical algebraic quantum field theory]]_).

Throughout we use the case of the real [[scalar field]] as an illustrative running example, which we develop alongside with the theory,
and the [[free field theory|free]] [[electromagnetic field]] when it comes to [[gauge theory]]. The discussion of other types of [[field (physics)|fields]] that are of more genuine interest in applications is postponed to their dedicated chapters below.


## Geometry
 {#Geometry}

In [[field theory]] one is concerned with [[differential geometry]] on
[[spaces]] that are more general than [[smooth manifolds]] in several ways (a preview is in remark \ref{PreviewOfGenerlizedDifferentialGeometryAppearingInFieldTheory} below). The right concept
that neatly supports the necessary differential geometry turns out to be that of _[[smooth sets]]_
(in particulcar [[diffeological spaces]])
and their [[super formal smooth infinity-groupoid|generalization]] to [[supergeometry|super]]-, [[formal geometry|formal]]- and [[higher differential geometry]]. Here we briefly explain how this works.

(A more detailed introduction is at _[[geometry of physics]]_
in the chapters on _[[geometry of physics -- smooth sets|smooth sets]]_, _[[geometry of physics -- differential forms|differential forms]]_ and _[[geometry of physics -- supergeometry|supergeometry]]_, but the reader willing to trust that the theory works
need not bother and just take note of the following basic ideas.)

While the concept of _[[smooth sets]]_ is not advertised in traditional textbooks, it is actually simpler than
that of smooth manifolds and it is closer to the operational nature of physics:

A [[smooth set]] $X$ is defined simply by specifying, in a self-consistent way, what counts as a smooth function $U \to X$ (a "plot") from any [[Cartesian space]] $U$ ("[[coordinate systems]]"). Given two smooth sets $X$ and $Y$ then a [[smooth function]] $f \;\colon\; X \longrightarrow Y$ between them is a function that takes plots $U \overset{\phi}{\to} X$ of $X$ to plots $f \circ \phi \colon U \to Y$ of $Y$.
If we allow $U$ here to be a [[super Cartesian space]], then the same idea defines _[[super smooth sets]]_.
We will write $\mathbf{H}$ for the resulting differential geometric [[category]] of [[smooth sets]] or more generally
[[super formal smooth sets]].

For instance if $X$ happens to be an ordinary [[smooth manifold]], then it becomes a [[smooth set]] by declaring that
a function $f \colon U \to X$ from some $U = \mathbb{R}^n$ into it is smooth, precisely if it is a [[smooth function]]
in the ordinary sense (i.e. a function all whose [[derivatives]] exist).

A key example of a smooth set which is in general not a [[smooth manifold]] is the [[mapping space]] $[X,Y]$ between two smooth sets $X$ and $Y$, hence the set of all smooth functions $X \to Y$ equipped with a smooth structure itself. Here a plot $\phi_{(-)} \colon U \to [X,Y]$
of the mapping space is defined to be a smooth function $\phi_{(-)}(-) \colon U \times X \to Y$ out of the [[Cartesian product]] of $U$ with $X$ to $Y$, hence a "U-parameterized smooth family of smooth functions on $X$".

An example of a smooth set which is far from being a smooth manifold is for $n \in \mathbb{N}$ the smooth set $\mathbf{\Omega}^n$ which is the "smooth [[classifying space]]" for [[differential n-forms]], defined by the rule that a smooth function $\phi \colon U \to \mathbf{\Omega}^n$ is equivalently a smooth differential $n$-form on $U$ (to be thought of as the [[pullback of differential forms|pullback]] of a "universal $n$-form" on $\mathbf{\Omega}^n$ along $\phi$).
It follows from this in particular that for $X$ any [[smooth manifold]] then smooth functions $X \to \mathbf{\Omega}^n$ are equivalent to smooth $n$-forms on $X$. Accordingly we may say that for $X$ any [[smooth set]] (which may be far from being a smooth manifold) then a differential $n$-form on $X$ is equivalently a smooth function $X \to \mathbf{\Omega}^n$.
Under this identification the operation of [[pullback of differential forms]] along some smooth function $f \colon Y \to X$ is just [[composition]] of smooth functions $f^\ast \omega \colon Y \overset{f}{\to} X \overset{\omega}{\to} \mathbf{\Omega}^n$.

This means that a [[differential n-form]] $\omega \in \Omega^n(X)$ on any smooth set $X$ is by definition just a
compatible system of ordinary differential $n$-forms on Cartesian spaces mapping into $X$: For
$\phi \colon U \to X$ a function declared to be smooth, we have an ordinary $n$-form on $U$, suggestively denoted
$\phi^\ast \omega \in \Omega^n(U)$; and for $f \colon V \to U$ any ordinary smooth function between Cartesian spaces,
we require that $ (\phi \circ f)^\ast \omega = f^\ast (\phi^\ast\omega)$, just as it should be.

For example if $[X,Y]$ is a [[smooth set|smooth]] [[mapping space]] as above, then a [[differential n-form]]
$\omega \in \Omega^n([X,Y])$ is for each [[Cartesian space]] $U$ and each smooth function
$\Phi_{(-)}(-) \colon U \times X \to Y$ an ordinary [[differential n-form]] on $U$, suggestively denoted
$\left(\Phi_{(-)}\right)^\ast \omega \in \Omega^n(U)$, such that for every ordinary smooth function
$V \overset{f}{\to} U$ from another [[Cartesian space]] $V$, we have the evident consistency relation
$(\Phi_{f(-)})^\ast \omega = f^\ast  (\Phi_{(-)})^\ast \omega $ between ordinary differential forms on $V$.

This way the concept of [[smooth sets]] provides a systematic way to study [[differential forms]]
on [[generalized smooth spaces]] simply in terms of _compatible systems_ of differential forms
on plain [[Cartesian spaces]]. This means that we will be handling ordinary differential forms on
ordinary smooth manifolds a lot. For these we assume that the reader is familiar
with standard [[Cartan calculus]]:

For $v$ a [[vector field]] on a [[smooth manifold]] $X$, we write

$$
  \iota_v \;\colon\; \Omega^\bullet(X) \longrightarrow \Omega^{\bullet-1}(X)
$$

for the operation of evaluating differential forms on this vector field, normalized so that
this becomes a [[derivation]] (of degree -1) on the [[wedge product]] algebra of differential forms.

We will have ample use of [[Cartan's homotopy formula]], which says that if
$\exp(t v) \colon X \to X$ denotes the [[flow]] by [[diffeomorphisms]] along $v$ of parameter length $t$, then
the [[derivative]] of the [[pullback of differential forms]] along $\exp(t v)$, hence the [[Lie derivative]]
$\mathcal{L}_v \colon \Omega^\bullet(X) \to \Omega^\bullet(X)$
 is given by the [[anticommutator]] of $\iota_v$ with the [[de Rham differential]] $d$:

$$
  \begin{aligned}
    \mathcal{L}_v
      &\coloneqq
    \frac{d}{d t } \exp(t v)^\ast \omega
    \\
    & =
    \iota_v d \omega + d \iota_v \omega
    \,.
  \end{aligned}
$$

We also consider [[integration of differential forms]] over [[Cartesian products]] $U \times \Sigma$ of ordinary smooth manifolds:
if $\omega \in \Omega^{n + dim(\Sigma)}(U \times \Sigma)$ and $\Sigma$ is [[compact space|compact]], then

$$
  \int_\Sigma \omega \; \in \Omega^{n}(U)
  \,.
$$

This is particularly convenient for discussion of _[[transgression of differential forms]]_, which
is a process that controls much of [[Lagrangian field theory]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below):

Given a [[differential form]] $\omega$ of degree $n$ on some [[smooth space]] $X$ and given a [[compact space|compact]] [[smooth manifold]] $\Sigma$ of [[dimension]] $k \leq n$, then there is canonically induced a differential form $\tau_\Sigma \omega$ of degree $n-k$ on the [[mapping space]] $[\Sigma, X]$: its restriction to any smooth family $\Phi_{(-)}$ of smooth functions $\Phi_u \colon \Sigma \to X$ is the result of first forming the [[pullback of differential forms]] of $\omega$ along $\Phi_{(-)}$ and then forming the [[integration of differential forms]] of the result over $\Sigma$:

$$
  \tau_{\Sigma} \omega\vert_{\Phi_{(-)}}
    \coloneqq
  \int_\Sigma (\Phi_{(-)})^\ast \omega
  \,.
$$

This differential form $\tau_\Sigma \omega$ on the mapping space
is called the _[[transgression of differential forms|transgression]]_ of $\omega$ with respect to $\Sigma$.

We also need to consider [[infinitesimal]] spaces of various sorts. In order to describe these
we make use of the _three magic algebraic facts of differential geometry_


+-- {: .num_prop #AlgebraicFactsOfDifferentialGeometry}
###### Proposition
**(the three magic algebraic properties of [[differential geometry]])**

1. **[[embedding of smooth manifolds into formal duals of R-algebras]]**

   The [[functor]] that sends a [[smooth manifold]] $X$ to its $\mathbb{R}$-[[associative algebra|algebra]] 
   $C^\infty(X)$ of [[smooth functions]] with values in the [[real line]] is a [[fully faithful functor]];
   
   $$
     C^\infty(-)
     \;\colon\;
     SmthMfd \hookrightarrow \mathbb{R} Alg^{op}
     \,.
   $$
   
   This means that [[smooth functions]] $f \colon X \longrightarrow Y$ are in [[natural bijection]] with their
   induced algebra [[homomorphisms]] $C^\infty(X) \overset{f^\ast}{\longrightarrow} C^\infty(Y)$ so that 
   one may equivalently handle smooth manifolds entirely via their algebras of smooth functions.

1. **[[smooth Serre-Swan theorem|embedding of smooth vector bundles into formal duals of R-algebra modules]]**

   For a fixed [[smooth manifold]] $X$ the [[functor]] that sends a [[smooth vector bundle]] $E \to X$
   to its [[space of sections]] $\Gamma_X(E)$, regarded as a [[module]] over the [[algebra of functions|algebra of]]
   [[smooth function]] $C^\infty(X)$ is a [[fully faithful functor]]
   
   $$
     \Gamma_X(-) \;\colon\; VectBund_X \hookrightarrow C^\infty(X) Mod
   $$
   
   Its [[essential image]] consists of the [[finitely generated module|finitely generated]] [[projective modules]].
     
1. [[derivations of smooth functions are vector fields|vector fields are derivations of smooth functions]].

(Here all [[manifolds]] are assumed to have [[finite number|finite]] [[dimension]] and all [[vector bundles]] 
are assumed to have [[finite number|finite]] [[rank of a vector bundle]].)

=--


+-- {: .num_example #InfinitesimalNeighbourhood}
###### Example
**([[infinitesimal neighbourhood]])

For $x_0 \in \mathbb{R}^n$ a point and $k \in \mathbb{N}$, then 
the order-$k$ _[[infinitesimal neighbourhood]]_ $\mathbb{D}^k_{x_0}$ of $x_0$ 
is _defined_ to be the space whose [[algebra of functions]] is 
the [[polynomial algebra]] in the $n$ canonical [[coordinate]] functions,
modulo the relation which regards a product of more than $k$ of these as being zero:

$$
  C^\infty( \mathbb{D}^k_{x_0} )
  \;\coloneqq\;
  \mathbb{R}[ (x^1 - x_0^1), \cdots (x^n - x_0^n)  ]/( (x^1- x_0^1), \cdots (x^n - x_0^n)  )^{k+1}
  \,.
$$

Similarly the full [[infinitesimal neighbourhood]] $\mathbb{D}_{x_0}$ (without restriction on the order) is the 
the space whose [[algebra of functions]] is the [[formal power series algebra]]

$$
  C^\infty( \mathbb{D}_{x_0} )
  \;\coloneqq\;
  \mathbb{R}[ [ (x^1 - x_0^1), \cdots (x^n - x_0^n)  ] ]
  \,.
$$

=--


$\,$


$\,$

+-- {: .num_remark #PreviewOfGenerlizedDifferentialGeometryAppearingInFieldTheory}
###### Remark
**(preview of generalized differential geometry appearing in field theory)**

While we introduce many of the following terms from field theory only further below, some
readers may appreciate a quick preview of where in field theory differential geometry
beyond smooth manifolds appears:

The very _[[space of field histories]]_ of a field theory, hence the space of all ways
in which fields may behave in [[spacetime]], is a [[space of sections]] (namely of the "[[field bundle]]"),
which is akin to the [[mapping space]] of all [[smooth functions]] from [[spacetime]] to a "[[field fiber]]" space.
Even in rare cases where this [[space of trajectories]] happens to admit the structure of an [[infinite-dimensional manifold]]
(such as when the [[field fiber]] happens to be a [[smooth manifold]] and when one restricts attention to a [[compact subset]] of spacetime, see at _[[manifold structure of mapping spaces]]_) this structure may be unwieldy for the purposes of the theory.
For instance in order to handle [[differential forms]] on mapping spaces (such as the [[presymplectic form]]
on the "[[shell]]" inside the [[space of trajectories]] which constitutes the [[phase space]] of the theory), it
is sufficient just to know which
functions from [[Cartesian spaces]] (i.e. from [[coordinate systems]]) into the mapping spaces are [[smooth functions]].
This information gives the mapping space the structure of a "[[smooth set]]".

To properly define the [[phase space]] associated with a [[Cauchy surface]] in [[spacetime]],
one needs to consider the [[infinitesimal neighbourhood]] of that Cauchy surface (so that a field restricted
to that infinitesimal neighbourhood is specified by the value of all its spacetime-[[derivatives]] on the Cauchy surface).
Such [[infinitesimal]] aspects of differential geometry are captured by "[[formal smooth sets]]".

Generally the "[[field fiber]]" space (and hence the total space of the [[field bundle]]) is not a plain smooth manifold:
if [[fermion|fermionic]] fields are considered, then it is a [[supermanifold]], if [[gauge fields]] are considered then it is
a [[Lie algebroid]] or rather a [[smooth groupoid]], if [[higher gauge fields]] are considered then it is an
[[infinity-Lie algebra]] or rather a [[smooth ∞-groupoid]], and hence if the theory contains both
[[fermion|fermion fields]] as well as [[gauge fields]] (as is the case in examples of [[phenomenology|phenomenological]] interest)
then it is a [[super smooth ∞-groupoid]].

=--

$\,$


$\,$


##  Spacetime
  {#Spacetime}

[[relativistic field theory|Relativistic field theory]] takes place in (or on) _[[spacetime]]_. We briefly set up some notations
and conventions:

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
  x^\mu \;\colon\; \mathbb{R}^{p+1} \longrightarrow \mathbb{R}
$$

which we index starting at zero: $(x^\mu)_{\mu = 0}^p$.

We write

$$
  dvol_\Sigma
   \;\coloneqq\;
  d x^0 \wedge d x^1 \wedge \cdots \wedge d x^p
  \in \Omega^{p+1}(\mathbb{R}^{p,1})
$$

for the induced [[volume form]].

We use the [[Einstein summation convention]]: Expressions with repeated indices indicate [[sum|summation]] over the
range of indices.

For example a [[differential 1-form]] $\alpha \in \Omega^1(\mathbb{R}^{p,1})$ on Minkowski spacetime may be expanded as

$$
  \alpha = \alpha_\mu d x^\mu
  \,.
$$

Moreover we use square brackets around indices to indicate skew-symmetrization. For example a [[differential 2-form]]
$\beta \in \Omega^2(\mathbb{R}^{p,1})$ on Minkowski spacetime may be expanded as

$$
  \begin{aligned}
    \beta
    & = \beta_{\mu \nu} d x^\mu \wedge d x^\nu
    \\
    & = \beta_{[\mu \nu]} d x^\mu \wedge d x^\nu
  \end{aligned}
$$


## Fields
 {#FieldBundles}

A _[[field (physics)|field]] [[trajectory]]_ (field history) on a given [[spacetime]] $\Sigma$ is meant to be some kind of [[quantity]] assigned to each point of spacetime (each [[event]]), such that this assignment varies smoothly with spacetime points. For instance an _[[electromagnetic field]]_ [[trajectory]] (or "history") is at each point of spacetime a collection of [[vectors]] that encode the direction in which a [[charged particle]] passing through that point will feel a [[force]] (the [[Lorentz force]]).

This is readily formalized (def. \ref{Fields} below): If $F$ denotes the [[smooth set]] of "values" that the given kind of field may take at any spacetime point, then a field configuration $\Phi$ is modeled as a [[smooth function]] from spacetime to this space of values:

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

+-- {: .num_defn #Fields}
###### Definition
**([[field (physics)|fields]] and their [[space of histories]])**

Given a [[spacetime]] $\Sigma$, then a _[[type]] of [[field|fields]]_ on $\Sigma$
is a [[smooth set|smooth]] [[fiber bundle]]

$$
  \array{E \\ \downarrow^{\mathrlap{fb}} \\ \Sigma }
$$

called the _[[field bundle]]_,

Given a type of [[field|fields]] on $\Sigma$ this way, then a  _[[field (physics)|field]] [[trajectory]]_ (or _field history_) of that type on $\Sigma$
is a smooth  [[section]] of this [[bundle]], namely a [[smooth function]] of the form

$$
  \Phi \colon \Sigma \longrightarrow E
$$

such that composed with the [[projection]] map it is the [[identity function]], i.e. such that

$$
  fb \circ \Phi = id
  \phantom{AAAAAAA}
  \array{
    && E
    \\
    & {}^{\mathllap{\Phi}}\nearrow & \downarrow^{\mathrlap{fb}}
    \\
    \Sigma & = & \Sigma
  }
  \,.
$$

The corresponding _[[space of field histories]]_ is the [[smooth set|smooth]] [[space of sections|space of all these]], to be denoted

$$
  \label{SpaceOfFieldHistories}
  \Gamma_\Sigma(E) \in \mathbf{H}
  \,.
$$

This is a [[smooth set]] by declaring that a smooth family $\Phi_{(-)}$ of field configurations,
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


More generally, let $S \hookrightarrow \Sigma$ be a [[submanifold]] of spacetime. We write
$N_\Sigma(S) \hookrightarrow \Sigma$ for its [[infinitesimal neighbourhood]] in $\Sigma$.

If $E \overset{fb}{\to} \Sigma$ is a [[field bundle]]
then the _[[space of histories]] of fields restricted to $S$_, to be denoted

$$
  \label{SpaceOfFieldHistoriesInHigherCodimension}
  \Gamma_{S}(E) \coloneqq \Gamma_{N_\Sigma(S)}( E\vert_{N_\Sigma S} ) \in \mathbf{H}
$$

is the [[space of sections]] restricted to the [[infinitesimal neighbourhood]] $N_\Sigma(S)$.

There is a canonical [[evaluation]] [[smooth function]]

$$
  \label{FieldEvaluation}
  ev_S
   \;\colon\;
  N_\Sigma S \times \Gamma_{S}(E)
    \longrightarrow
  E
$$

which takes a [[pair]] consisting of an [[generalized element|element]] in $N_\Sigma S$
and a field configuration to the value of the field configuration at that point.

=--

For the time being, not to get distracted from the core idea of
field theory, we will focus on the following simple special case of field bundles:

+-- {: .num_example #TrivialVectorBundleAsAFieldBundle}
###### Example
**([[trivial vector bundle]] as a [[field bundle]])**

In applications the [[field fiber]] $F$ is often a [[finite number|finite]] [[dimension|dimensional]] [[Euclidean space]] and equipped with the structure of a [[vector space]]. In this case the trivial field bundle with fiber $F$ is of course a _[[trivial vector bundle|trivial]] [[vector bundle]]_.

Choosing any [[linear basis]] $(\phi^a)_{a = 1}^s$ of the field fiber, then over [[Minkowski spacetime]] we have canonical [[coordinates]] on the total space of the field bundle

$$
  ( (x^\mu), ( \phi^a ) )
  \,,
$$

where the index $\mu$ ranges from $0$ to $p$, while the index $a$ ranges from 1 to $s$.

If this trivial vector bundle is regarded as a [[field bundle]] according to def. \ref{Fields}, then
a field configuration $\Phi$ is equivalently an $s$-[[tuple]] of [[real number|real]]-valued [[smooth functions]]
$\Phi^a \colon \Sigma \to \mathbb{R}$ on spacetime:

$$
  \Phi = ( \Phi^a )_{a = 1}^s
  \,.
$$

=--

The following simplest special case of this simple class of special cases
serves as a good toy example for the general theory:

+-- {: .num_example #RealScalarFieldBundle}
###### Example
**([[field bundle]] for [[real scalar field]])**

If $\Sigma$ is a [[spacetime]] and if the [[field fiber]]

$$
  F \coloneqq \mathbb{R}
$$

is simply the [[real line]], then the corresponding trivial [[field bundle]] (def. \ref{Fields})

$$
  \array{
    \Sigma \times \mathbb{R}
    \\
    {}^{\mathllap{pr_1}}\downarrow
    \\
    \Sigma
  }
$$

is the _[[trivial fiber bundle|trivial]] [[real line bundle]]_ (a special case of example \ref{TrivialVectorBundleAsAFieldBundle}) and the corresponding [[field (physics)|field]] type (def. \ref{Fields}) is called the _[[real scalar field]]_ on $\Sigma$. A configuration of this field is simply a [[smooth function]] on $\Sigma$ with values in the [[real numbers]]:

$$
  \Gamma_\Sigma(\Sigma \times \mathbb{R})
    \;\simeq\;
  C^\infty(\Sigma)
  \,.
$$

=--


+-- {: .num_example #Electromagnetism}
###### Example
**([[field bundle]] for [[electromagnetic field]])

On [[Minkowski spacetime]] $\Sigma$, let the [[field bundle]] (def. \ref{Fields}) be given by the
[[cotangent bundle]]

$$
  E \coloneqq T^\ast \Sigma
  \,.
$$

This is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with canonical [[field (physics)|field]]
coordinates $(a_\mu)$.

A [[section]] of this bundle, hence a [[field (physics)|field]] [[trajectory]]/history, is a [[differential 1-form]]

$$
  A \in \Gamma_\Sigma(T^\ast \Sigma) = \Omega^1(\Sigma)
$$

on [[spacetime]]. Interpreted as the field of [[electromagnetism]] on $\Sigma$, this is often called the _[[vector potential]]_.
Then the [[de Rham differential]] of the [[vector potential]] is a [[differential 2-form]]

$$
  F \coloneqq d A
$$

known as the _[[Faraday tensor]]_. In the canonical coordinate basis 2-forms this may be expanded as

$$
  \label{TensorFaraday}
  F
  =
  \underoverset{i = 1}{p}{\sum}
  E_i d x^0 \wedge d x^i
  +
  \underoverset{i \lt j = 1}{p}{\sum}
  B_{i j} d x^i \wedge d x^j
  \,.
$$

Here $(E_i)_{i = 1}^p$ are called the components of the _[[electric field]]_, while $(B_{i j})$ are called the
components of the _[[magnetic field]]_.

=--



+-- {: .num_example #YangMillsFieldOverMinkowski}
###### Example
**([[field bundle]] for [[Yang-Mills theory|Yang-Mills]] [[field (physics)|field]])**

Let $\mathfrak{g}$ be a [[Lie algebra]] of [[finite number|finite]] [[dimension]] with [[linear basis]]
$(t_\alpha)$, in terms of which the [[Lie bracket]] is given by

$$
  \label{LieAlgebraStructureConstants}
  [t_\alpha, t_\beta]
  \;=\;
  C^\gamma{}_{\alpha \beta} t_\gamma
  \,.
$$

Over [[Minkowski spacetime]] $\Sigma$,
consider then the [[field bundle]] which is the [[cotangent bundle]] [[tensor product|tensored]] with the [[Lie algebra]] $\mathfrak{g}$

$$
  E \coloneqq T^\ast \Sigma \otimes \mathfrak{g}
  \,.
$$

This is the [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with induced [[field (physics)|field]] [[coordinates]]

$$
  ( a_\mu^\alpha )
  \,.
$$

A [[section]] of this bundle is a [[Lie algebra-valued differential 1-form]]

$$
  A \in \Gamma_\Sigma(T^\ast \Sigma \otimes \mathfrak{g}) = \Omega^1(\Sigma, \mathfrak{g})
  \,.
$$

with components

$$
  A^\ast(a_\mu^\alpha) = A^\alpha_\mu
  \,.
$$

This is called a field history for _[[Yang-Mills theory|Yang-Mills]] [[gauge theory]]_.

For $\mathfrak{g} = \mathbb{R}$ is the [[line Lie algebra]], this reduces to the case of the [[electromagnetic field]] (example \ref{Electromagnetism}).

For $\mathfrak{g} = \mathfrak{su}(2)$ this is a [[field (physics)|field]] history for the [[gauge field]] of the [[strong nuclear force]] in [[quantum chromodynamics]].


=--


## Field variations
 {#FieldVariations}

Given a [[field bundle]] as in def. \ref{Fields} above, then we know what type of quantities the corresponding fields assign to a given spacetime point ([[event]]). Among all consistent such field configurations, some are to qualify as those that "may occur in reality" if we think of the field theory as a means to describe parts of the [[observable universe]]. Moreover, if the reality to be described does not exhibit "action at a distance" then admissibility of its field configurations should be determined over arbitrary small spacetime regions, in fact over the [[infinitesimal neighbourhood]] of any spacetime point. This means equivalently that the realized field configurations should be those that satisfy a given _[[differential equation]]_, hence an [[equation]] between the value of the [[derivatives]] of the field
configuration at any spacetime point.

In order to formalize this, it is useful to first collect all the possible derivatives that a field may have at any given point into one big space of "field derivatives at spacetime points". This collection is called the _[[jet bundle]]_ of the [[field bundle]], given as def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below.

Moving around in this space means to change the possible value of fields and their derivatives, hence to _vary_ the fields. Accordingly _[[variational calculus]]_ of fields is just [[differential calculus]] on the [[jet bundle]] of the [[field bundle]], this we consider in def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} below.


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
     \,,\,
     \cdots
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
  J^\infty_\Sigma(E) \in \mathbf{H}
$$

is the [[direct limit]] over these finite order jet bundles,
formed in the [[category]] of [[smooth sets]]. This means that it is the [[smooth set]] which is defined
by the fact that a smooth function

$$
  U \overset{f}{\longrightarrow} J^\infty_\Sigma(E)
$$

from some [[Cartesian space]] $U$ is equivalently a system of ordinary smooth functions
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


+-- {: .num_defn #JetProlongation}
###### Definition
**([[jet prolongation]])**

The [[smooth function]] from the [[space of sections]] of the original bundle to the space of sections of the jet bundle which records the field $\Phi$ and all its spacetimes [[derivatives]] is called _[[jet prolongation]]_:

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

=--

So the canonical [[coordinates]] on the jet bundle are the spacetime-point-wise _possible_ values of fields and field derivates,
while the [[jet prolongation]] picks the actual collections of field derivatives that may occur for an actual field
history.

+-- {: .num_example #JetFaraday}
###### Example
**(universal [[Faraday tensor]]/[[field strength]] on [[jet bundle]])**

Consider the [[field bundle]] (def. \ref{Fields}) of the [[electromagnetic field]] (example \ref{Electromagnetism})
over [[Minkowski spacetime]] $\Sigma$, i.e. the [[cotangent bundle]] $E = T^\ast \Sigma$ with jet coordinates
$((x^\mu), (a_\mu), (a_{\mu,\nu}), \cdots )$. Consider the functions on its [[jet bundle]] given by the linear
combinations

$$
  \label{FaradayTensorJet}
  f_{\mu \nu}
    \;\coloneqq\;
  \tfrac{1}{2}\left(
    a_{\mu,\nu} - a_{\nu,\mu}
  \right)
$$

of the first order jets.

Then for an electromagnetic [[field (physics)|field]] history ("[[vector potential]]"), hence a [[section]]

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

The [[pullback of differential forms|pullback]] of the functions $f_{\mu \nu}$ (eqs:FaradayTensorJet)
along this jet prolongation are the components of the [[Faraday tensor]] of the field (eqs:TensorFaraday):

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

the [[field bundle]] for [[Yang-Mills theory]] from
example \ref{YangMillsFieldOverMinkowski}, consider the functions on the [[jet bundle]]
given by

$$
  D_\mu a_\nu^\alpha
   \;\coloneqq\;
  a^\alpha_{\nu,\mu}
  +
  \tfrac{1}{2}
    \gamma^{\alpha}{}_{\beta \gamma}
    a^\beta_{\mu}} a^\gamma_{\nu}
  -
  (\mu \leftrightarrow \nu)
$$

where $(\gamma^\alpha{}_{\beta \gamma})$ the structure constants of the Lie algebra as in (eqs:LieAlgebraStructureConstants)
and where the square brackets around the indices denote anti-symmetrization.
For $\mathfrak{g} = \mathbb{R}$ the [[line Lie algebra]] this reduces to the universal [[Faraday tensor]] (eqs:FaradayTensorJet) for
the [[electromagnetic field]] (example \ref{JetFaraday}).

For $A \in \Gamma_\Sigma(T^\ast \Sigma \otimes \mathfrak{g}) = \Omega^1(\Sigma,\mathfrak{g})$ a field history of
[[Yang-Mills theory]], hence a [[Lie algebra-valued differential 1-form]], then the value of this function on that field
are called the components of the _[[covariant exterior derivative]]_ or _[[field strength]]_

$$
  \begin{aligned}
    F_{\mu \nu}
     & \coloneqq
    A^\ast(D_\mu a_n)
    \\
    & =
    (d_A A)_{\mu \nu}
  \end{aligned}
$$

=--



While the [[jet bundle]] is not [[finite number|finite]] [[dimension|dimensional]],
reflecting the fact that there are arbitrarily high orders of spacetime derivatives of a field configurations,
it turns out that it is only very "mildly [[infinite dimensional manifold|infinite dimensional]]"
in that
[[smooth  functions]] on jet bundles turn out to _locally_ depend on only finitely many of the jet coordinates
(i.e. only on a finite order of spacetime derivatives). This is the content
of the following prop. \ref{JetBundleIsLocallyProManifold}.
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


Example \ref{JetFaraday} shows that the [[de Rham differential]] may be encoded in terms of
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

=--


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
  \label{SpacetimeTotalDerivativeOnSmoothFunctions}
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
  \delta \coloneqq \mathbf{d} - d
  \,.
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
|  | $\; \mathbf{d}$ | [[de Rham differential]]  | [[de Rham differential]] |
| \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}  | $\; d \coloneqq d x^\mu \frac{d}{d x^\mu}$ | [[total derivative|total spacetime derivative]]   | [[horizontal derivative]]  |
| \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} | $ \; \frac{d}{d x^\mu} \coloneqq \frac{\partial}{\partial x^\mu} +  \phi^a_{,\mu} \frac{\partial}{\partial \phi^a}  + \cdots $ | [[total derivative|total spacetime derivative]] along $\partial_\mu$  |  [[horizontal derivative]] along $\partial_\mu$ |
| \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} | $\; \delta \coloneqq \mathbf{d} - d$ | [[variational derivative]]  | [[vertical derivative]] |
| \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}  | $\; \delta_{EL} \mathbf{L} \coloneqq \mathbf{d}\mathbf{L} + d \Theta$ | [[Euler-Lagrange variational derivative|Euler-Lagrange variation]]  | [[Euler-Lagrange operator]] |
| \ref{BVComplexOfOrdinaryLagrangianDensity} | $\; s_{BV}$  | [[BV-differential]]  |  [[Koszul complex|Koszul differential]]  |
| \ref{LocalOffShellBRSTComplex} | $\; s_{BRST} $ | [[BRST differential]] |  [[Chevalley-Eilenberg complex|Chevalley-Eilenberg differential]]  |
| \ref{BVVariationalBicmplex} | $\; s $ | [[BV-BRST differential]] |  [[Chevalley-Eilenberg complex|Chevalley-Eilenberg]]-[[Koszul-Tate complex|Koszul-Tate]] differential |
| \ref{BVVariationalBicmplex} | $\; s - d $ | [[local BV-BRST differential]] |   |
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

* The spacetimes [[total derivatives]] /horizontal derivatives) of the variational derivative (vertical derivative) $\delta \phi$ of a field variable is the differential 2-form of horizontal degree 1 and vertical degree 2 given by

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


+-- {: .num_prop #PullbackAlongJetProlongationIntertwinesHorizontalDerivative}
###### Proposition
**([[pullback of differential forms|pullback]] along [[jet prolongation]] compatible with [[total derivative|total spacetime derivatives]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{Fields}),
with induced [[jet bundle]] $J^\infty_\Sigma(E)$

Then for $\Phi \in \Gamma_\Sigma(E)$ any field configuration, the [[pullback of differential forms]]

$$
  j^\infty_\Sigma(\Phi)^\ast
   \;\colon\;
  \Omega^\bullet(J^\infty_\Sigma(E))
    \longrightarrow
  \Omega^\bullet(\Sigma)
$$

along the [[jet prolongation]] of $\Phi$ (def. \ref{JetProlongation}):

1. intertwines the [[de Rham differential]] on [[spacetime]] with the [[total derivative|total]] spacetime derivative ([[horizontal derivative]]) on the [[jet bundle]]:

   $$
     d \circ j^\infty_\Sigma(\Phi)^\ast
     \;=\;
     j^\infty_\Sigma(\Phi)^\ast \circ d
     \,.
   $$

1. annihilates all [[vertical differential forms]]

   $$
     j^\infty_\Sigma(\Phi)^\ast\vert_{\Omega^{r, \geq 1}_\Sigma(E)} = 0
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Notice that generally the operation of [[pullback of differential forms]]
along any smooth function intertwines the full [[de Rham differentials]]. In particular
we have on general grounds that

$$
  d \circ j^\infty_\Sigma(\Phi)^\ast
  =
  j^\infty_\Sigma(\Phi)^\ast \circ \mathbf{d}
  \,.
$$

This means that the second statement immediately follows from the
first, by definition of the variational (vertical) derivative as the differece between
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
of the total spacetime derivative of $f$ (eqs:SpacetimeTotalDerivativeOnSmoothFunctions).


=--



## Lagrangians
  {#LagrangianFieldTheory}


Given any type of [[field (physics)|fields]] (def. \ref{Fields}), those field configurations that
are to be regarded as "physically realizable" (if we think of the field theory as a description of the [[observable universe]])
should satisfy some [[differential equation]] (the "[[equation of motion]]"), meaning that realizability of any field configuration may
be checked upon restricting the configuration to the [[infinitesimal neighbourhoods]] of each spacetime point.
This expresses the physical absence of "action at a distance" and is one aspect of what it means to have
a _[[local field theory]]_.

For many field theories of interest, their [[differential equation|differential]] [[equation of motion]]
is not a random [[partial differential equations]], but is of the special kind that exhibits the "[[principle of extremal action]]"
determined by a [[local Lagrangian density]]
(def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below). These are called _[[Lagrangian field theories]]_, and this is what we consider here.

Namely among all the variational differential forms (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
two kinds stand out, namley the 0-forms in $\Omega^{0,0}_\Sigma(E)$ -- the smooth functions -- and the horizontal $p+1$-forms
$\Omega^{p+1,0}_\Sigma(E)$ -- to be called the _[[Lagrangian densities]] $\mathbf{L}$_ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below) -- since these occupy the two "corners" of the [[variational bicomplex]] (eqs:VariationalBicomplexDiagram).
There is not much to say about the 0-forms, but the [[Lagrangian densities]] $\mathbf{L}$ do inherit special structure
from their special position in the [[variational bicomplex]].

Their [[variational derivative]]
uniquely decomposes as 1) the _[[Euler-Lagrange derivative]]_ $\delta_{EL}\mathbf{EL}$ which is proportional to the variation of the fields
(instead of their derivatives) and 2) the [[total derivative|total spacetime derivative]] $d \Theta$
of a potential $\Theta$ for a _[[presymplectic current]]_ $\Omega_{BFV} \coloneqq \delta \Theta$
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} below):

$$
  \delta_{EL} \mathbf{L} = \delta_{EL}\mathbf{L} - d \Theta
  \,.
$$

These two terms play a pivotal role in the theory: they induce the _[[covariant phase space]]_
of the [[field theory]]; this we discuss [below](#PhaseSpace). Before we get to that,
here we discuss the _symmetries_ of these terms, which will be important:

It turns out that every  [[infinitesimal symmetry of the Lagrangian density]] induces a
variational differential form called a _[[conserved current]]_ ([[Noether's theorem]], prop. \ref{NoethersFirstTheorem} below) and that
these conserved currents constitute an [[Lie algebra extension|extension]] of the [[Lie algebra]]
of symmetries, called the _[[Dickey bracket]]_.

In direct analogy, every infinitesimal symmetry of the [[presymplectic current|presymplectic potential]] $\Theta$
(called a _[[Hamiltonian vector field]]_) is witnessed by
a variational differential form, called a _[[Hamiltonian differential form]]_ (def. \ref{HamiltonianForms} below).
This is sometimes called the _[[Hamiltonian Noether theorem]]_.
The corresponding [[Lie n-algebra]] is the all-important _[[Poisson bracket Lie n-algebra|Poisson bracket Lie p+1-algebra]]_
of the Lagrangian field theory. In the simple special situation that we consider here, this is a
plain [[Lie algebra]] (prop. \ref{LocalPoissonBracket} below).

When we turn attention to the [[covariant phase space]] [below](#PhaseSpace)
the [[transgression of variational differential forms|transgression]]
of the [[Poisson bracket Lie n-algebra|Poisson bracket Lie p+1-algebra]] of [[Hamiltonian differential forms]]
yields the [[Poisson bracket Lie algebra]] on [[local observables]] on  [[covariant phase space]].
This is the all-important structure of the theory: the [[deformation quantization]] induced by this
bracket is the [[quantum physics|quantum]] aspect of the [[quantum field theory]].


$\,$

+-- {: .num_defn #LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[local Lagrangian density]])**

Given a [[field bundle]] $E$ over a $(p+1)$-dimensional [[Minkowski spacetime]] $\Sigma$ as in example \ref{TrivialVectorBundleAsAFieldBundle}, then a _[[local Lagrangian density]]_ $\mathbf{L}$ (for the type of field thus defined) is a [[horizontal differential form]] of degree $(p+1)$ (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}) on the corresponding [[jet bundle]]
(def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}):

$$
  \mathbf{L} \;\in \; \Omega^{p+1,0}_{\Sigma}(E)
  \,.
$$

By example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}
in terms of the given [[volume form]] on spacetimes, any such Lagrangian density may uniquely be written as

$$
  \mathbf{L} = L \, dvol_\Sigma
$$

where the [[coefficient]] function (the _Lagrangian function_)
is a smooth function on the spacetime and field coordinates:

$$
  L = L((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots )
  \,.
$$

where by prop. \ref{JetBundleIsLocallyProManifold} $L((x^\mu), \cdots)$ depends locally on an arbitrary but finite
order of derivatives $\phi^a_{,\mu_1 \cdots \mu_k}$.

We say that a [[field bundle]] $E \overset{fb}{\to} \Sigma$ (def. \ref{Fields}) equipped with a [[local Lagrangian density]] $\mathbf{L}$
is (or defines) a _[[prequantum field theory|prequantum]] [Lagrangian field theory]]_ on the [[spacetime]] $\Sigma$.

=--

(Over more general [[field bundles]] than we consider at the moment, the Lagrangian density may not exist
as a globally defined differential $(p+1)$-form, but as a [[circle n-bundle with connection|p-gerbe connection]].
This is the case for _[[locally variational field theories]]_ such as theories involving _[[higher WZW terms]]_.)



+-- {: .num_example #LagrangianForFreeScalarFieldOnMinkowskiSpacetime}
###### Example
**([[local Lagrangian density]] for [[free field|free]] [[real scalar field]] on [[Minkowski spacetime]])**

Consider the [[field bundle]] for the [[real scalar field]] from example \ref{RealScalarFieldBundle},
i.e. the [[trivial line bundle]] over [[Minkowski spacetime]].

According to def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
its [[jet bundle]] $J^\infty_\Sigma(E)$ has canonical coordinates

$$
  \{ \{x^\mu\}, \phi, \{\phi_{,\mu}\}, \{\phi_{,\mu_1 \mu_2}\}, \cdots \}
  \,.
$$

In these coordinates, the [[local Lagrangian density]] $L \in \Omega^{p+1,0}(\Sigma)$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
defining the [[free field|free]] [[real scalar field]] of [[mass]] $m \in [0,\infty)$ on $\Sigma$ is

$$
  L
    \coloneqq
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu} \phi_{,\mu} \phi_{,\nu}
    +
    m^2 \phi^2
  \right)
  \mathrm{dvol}_\Sigma
  \,.
$$

=--


+-- {: .num_example #ElectromagnetismLagrangianDensity}
###### Example
**([[local Lagrangian density]] for [[free field|free]] [[electromagnetism]] and [[Yang-Mills theory]])

Consider the [[field bundle]] $T^\ast \Sigma \to \Sigma$ for the [[electromagnetic field]] on [[Minkowski spacetime]] from example \ref{Electromagnetism},
i.e. the [[cotangent bundle]], which over Minkowski spacetime happens to be a [[trivial vector bundle]] of [[rank of a vector bundle|rank]]
$p+1$. With [[fiber]] coordinates taken to be $(a_\mu)_{\mu = 0}^p$, the induced fiber coordinates on the
corresponding [[jet bundle]] $J^\infty_\Sigma(T^\ast \Sigma)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) are
$( (x^\mu), (a_\mu), (a_{\mu,\nu}), (a_{\mu,\nu_1 \nu_2}), \cdots )$.

Consider then the [[local Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) given by

$$
  \label{ElectromagnetismLagrangian}
  \mathbf{L}
    \;\coloneqq\;
  \tfrac{1}{2}
  f_{\mu \nu} f^{\mu \nu} dvol_\Sigma
  \;\in\;
  \Omega^{p+1,0}_\Sigma(T^\ast \Sigma)
  \,,
$$

where $f_{\mu \nu} \coloneqq \tfrac{1}{2}(a_{\mu,\nu} - a_{\nu,\mu})$ are the components of the universal [[Faraday tensor]] on the [[jet bundle]] from example \ref{JetFaraday}.

This is the [[Lagrangian density]] that defines the Lagrangian field theory of _[[free field|free]] [[electromagnetism]]_.

Here for $A \in \Gamma_\Sigma(T^\ast \Sigma)$ an [[electromagnetic field]] history ([[vector potential]]),
then the [[pullback of differential forms|pullback]] of $f_{\mu \nu}$ along its [[jet prolongation]] (def. \ref{JetProlongation})
is the corresponding component of the [[Faraday tensor]] (eqs:TensorFaraday):

$$
  \begin{aligned}
    \left(
      j^\infty_\Sigma(A)
    \right)^\ast(f_{\mu \nu})
    & =
    (d A)_{\mu \nu}
    \\
    & = F_{\mu \nu}
  \end{aligned}
$$

It follows that the pullback of the Lagrangian (eqs:ElectromagnetismLagrangian) along the
jet prologation of the electromagnetic field is

$$
  \begin{aligned}
    \left(
      j^\infty_\Sigma(A)
    \right)^\ast \mathbf{L}
    & =
    \tfrac{1}{2}
    F_{\mu \nu} F^{\mu \nu} dvol_\Sigma
    \\
    & =
    \tfrac{1}{2} F \wedge_\eta \star F
  \end{aligned}
$$

Here $\star_\eta$ denotes the [[Hodge star operator]] of [[Minkowski spacetime]].

More generally, for $\mathfrak{g}$ a [[Lie algebra]] and $E = T^\ast \Sigma \otimes \mathfrak{g}$
the field bundle for [[Yang-Mills theory]] as in example \ref{YangMillsFieldOverMinkowski}.



=--


The beauty of [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) is that a choice of [[Lagrangian density]] determines
both the [[equations of motion]] of the fields as well as a [[presymplectic manifold|presymplectic structure]]
on the space of solutions to this equation (the "[[shell]]"), making it the "[[covariant phase space]]" of the theory.
All this we discuss [below](#PhaseSpace). But in fact all this key structure of the field theory is
othing but the shadow (under "[[transgression of variational differential forms]]", def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below)


+-- {: .num_prop #EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}
###### Proposition
**([[Euler-Lagrange variational derivative]] and [[presymplectic current]])**

Given a [[Lagrangian density]] $\mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)$ as in def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}, then its de Rham differential has a _unique_ decomposition as a sum of two terms

$$
  \label{dLDecomposition}
  \mathbf{d} \mathbf{L}
  =
  \delta_{EL} \mathbf{L}
  -
  d \Theta
$$

such that $\delta EL$ is proportional to the [[variational derivative]] of the fields (but not their derivatives, called a "[[source form]]"):

$$
  \delta_{EL} \mathbf{L}
    \;\in\;
  \Omega^{p+1,0}_{\Sigma}(E) \wedge \delta C^\infty(E)
    \;\subset\;
  \Omega^{p+1,1}_{\Sigma}(E)
  \,.
$$

The map

$$
   \delta_{EL} \;\colon\; \Omega^{p+1,0}_{\Sigma}(E) \longrightarrow \Omega^{p+1,0}_{\Sigma}(E) \wedge \delta \Omega^{0,0}_{\Sigma}(E)
$$

thus defined is called the _[[Euler-Lagrange operator]]_ and is explicitly given by

$$
  \begin{aligned}
    \delta_{EL} L \, dvol_\Sigma
    & \coloneqq
    \frac{\delta_{EL} L}{\delta \phi^a}
    \delta \phi^a \wedge dvol_\Sigma
    \\
    & \coloneqq
    \left(
      \frac{\partial L}{\partial \phi^a}
      -
      \frac{d}{d x^\mu}
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      +
      \frac{d^2}{d x^{\mu_1} d x^{\mu_2}}
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

The [[smooth space|smooth subspace]] of the [[jet bundle]] on which the [[Euler-Lagrange form]]
vanishes

$$
  \label{ShellInJetBundle}
  \mathcal{E}
   \;\coloneqq\;
  \left\{
    x \in J^\infty_\Sigma(E)
    \;\vert\;
    \delta_{EL}\mathbf{L}\vert_x = 0
  \right\}
  \;\subset\;
  J^\infty_\Sigma(E)
  \,.
$$

or rather the smaller subspace on which also all [[total spacetime derivatives]]
vanish (the "[[formally integrable PDE|formally integrable prolongation]]")
is called the _[[shell]]_

$$
  \label{ProlongedShellInJetBundle}
  \mathcal{E}^\infty
   \;\coloneqq\;
  \left\{
    q \in J^\infty_\Sigma(E)
    \;\vert\;
    \left(
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \delta_{EL}\mathbf{L}
    \right)\vert_x = 0
  \right\}
  \;\subset\;
  J^\infty_\Sigma(E)
  \,.
$$


Saying something holds  "[[on-shell]]" is to mean that it holds after restriction to this
subspace. For example a [[variational differential form]] $\alpha \in \Omega^{\bullet,\bullet}_\Sigma(E)$
is said to _vanish on shell_ if $\alpha\vert_{\mathcal{E}^\infty} = 0$.

The remaining term $d \Theta$ in (eqs:dLDecomposition) is unique, while the "presymplectic potential"

$$
  \label{PresymplecticPotential}
  \Theta \in \Omega^{p,1}_{\Sigma}(E)
$$

is unique only up to terms $d \alpha$ in the image of $d$.
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

The [[vertical derivative]] of a chosen $\Theta$ is called a _[[pre-symplectic current]]_ for $\mathbf{L}$:

$$
  \Omega_{BFV} \coloneqq \delta \Theta \;\;\; \in \Omega^{p,2}_{\Sigma}(E)
  \,,
$$

which, by the above, is unique up to addition of a total spacetime derivative $d \delta \alpha$.

Given a choice of $\Theta$ then the sum

$$
  \label{TheLepage}
  \mathbf{L} + \Theta \;\in\; \Omega^{p+1,0}_\Sigma(E) \oplus \Omega^{p,1}_\Sigma(E)
$$

is called the corresponding _[[Lepage form]]_. Its de Rham derivative is the sum of
the Euler-Lagrange variation and the presymplectic current:

$$
  \label{DerivativeOfLepageForm}
  \mathbf{d}( \mathbf{L} + \Theta )
  \;=\;
  \delta_{EL} \mathbf{L} + \Omega_{BFV}
  \,.
$$

=--


+-- {: .proof}
###### Proof

Using $\mathbf{L} = L dvol_\Sigma$ and that $d \mathbf{L} = 0$ by degree reasons (example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}), we find

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
$\int_\Sigma j^\infty_\Sigma(\Phi)^\ast \mathbf{d}L$ if we were to consider [[integration by parts]] to remove
spacetime derivatives of $\delta \phi^a$.

We compute, using example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle},
the total horizontal derivative of $\Theta$ from (eqs:StandardThetaForTrivialVectorFieldBundleOnMinkowskiSpacetime) as follows:

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
    = \delta_{EL}\mathbf{L}
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



+-- {: .num_example #FreeScalarFieldEOM}
###### Example
**([[Euler-Lagrange operator|Euler-Lagrange variational derivative]] and [[presymplectic current]] for [[free field|free]] [[real scalar field]])**


Consider the [[Lagrangian field theory]] of the [[free field|free]] [[real scalar field]]
from example  \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

Then the [[Euler-Lagrange operator|Euler-Lagrange form]] and [[presymplectic current]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) are

$$
  \label{RealScalarFieldLEForm}
  \delta_{EL}\mathbf{L}
  \;=\;
  \left(\eta^{\mu \nu} \phi_{,\mu \nu} + m^2 \right) \delta \phi \wedge dvol_\sigma
  \;\in\;
  \Omega^{p+1,1}_{\Sigma}(E)
  \,.
$$

and

$$
  \Omega_{BFV}
  \;=\;
  \left(\eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
  \;\in\;
  \Omega^{p,2}_{\Sigma}(E)
  \,,
$$

respectively.

=--

+-- {: .proof}
###### Proof

We need to show that [[Euler-Lagrange operator]] $\delta_{EL} \colon \Omega^{p+1,0}(\Sigma) \to \Omega^{p+1,1}_S(\Sigma)$ takes the [[local Lagrangian density]] for the [[free field|free]] [[scalar field]] to

$$
  \delta_EL L
  \;=\;
  \left(
    \eta^{\mu \nu} \phi_{,\mu \nu}  + m^2 \phi
  \right)
  \delta \phi \wedge \mathrm{dvol}_\Sigma
  \,.
$$

First of all, the result of applying the [[variational derivative]] ([[vertical derivative]]) to the local Lagrangian density is

$$
  \delta L
    \;=\;
  \left(
    \eta^{\mu \nu} \phi_{,\mu} \delta \phi_{,\nu}
      +
    m^2 \phi \delta \phi
  \right)
  \wedge \mathrm{dvol}_\Sigma
  \,.
$$

By definition of the [[Euler-Lagrange operator]], in order to find $\delta_{EL}\mathbf{L}$ and $\Theta$, we need to exhibit this as the
sum of the form $(-) \wedge \delta \phi  - d \Theta$.

The key to find $\Theta$ is  to realize $\delta \phi_{,\nu}\wedge \mathrm{dvol}_\Sigma$ as a
[[total derivative|total spacetime derivative]] ([[horizontal derivative]]). Since $d \phi = \phi_{,\mu} d x^\mu$ this is accomplished by

$$
  \delta \phi_{,\nu} \wedge \mathrm{dvol}_\Sigma
  =
  \delta d \phi \wedge \iota_{\partial_\nu} \mathrm{dvol}_\Sigma
$$

Hence we may take the presymplectic potential (eqs:PresymplecticPotential) of the free scalar field to be

$$
  \label{PresymplecticPotentialOfFreeScalarField}
  \Theta
    \coloneqq
  \eta^{\mu \nu} \phi_{,\mu} \delta \phi \wedge \iota_{\partial_\nu}
  \mathrm{dvol}_\Sigma
  \,,
$$

because with this we have

$$
  d \Theta
  =
  \eta^{\mu \nu}
  \left(
    \phi_{,\mu \nu} \delta \phi
    -
    \eta^{\mu \nu} \phi_{,\mu} \delta \phi_{,\nu}
  \right) \wedge \mathrm{dvol}_\Sigma
  \,.
$$

In conclusion this yields the decomposition of the vertical differential of the Lagrangian density

$$
  \delta L
  =
  \underset{
    = \delta_{EL} \mathcal{L}
  }{
  \underbrace{
    \left(
      \eta^{\mu \nu} \phi_{,\mu \nu}  + m^2 \phi
    \right)
    \delta \phi \wedge \mathrm{dvol}_\Sigma
  }
  }
  -
  d \Theta
  \,,
$$

which shows that $\delta_{EL} L$ is as claimed, and that $\Theta$ is a presymplectic potential current (eqs:PresymplecticPotential).
Hence the presymplectic current itself is

$$
  \begin{aligned}
    \Omega_{BFV} &\coloneqq \delta \Theta
    \\
    & =
    \delta \left( \eta^{\mu \nu} \phi_{,\mu} \delta \phi \wedge \iota_{\partial_\nu} \mathrm{dvol}_\Sigma \right)
    \\
    & =
    \left(\eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
  \end{aligned}
  \,.
$$

=--


+-- {: .num_example #ElectromagnetismEl}
###### Example
**([[Euler-Lagrange variational derivative]] for [[free field|free]] [[electromagnetism]])

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]] from example \ref{ElectromagnetismLagrangianDensity}.

The [[Euler-Lagrange variational derivative]] is

$$
  \delta_{EL} \mathbf{L}
  \;=\;
  \frac{d}{d x^\mu} f^{\mu \nu} \delta a_\nu
  \,.
$$

Hence the [[shell]] (eqs:ShellInJetBundle) in this case is

$$
  \mathcal{E}
    =
  \Sigma \times \left\{ (\phi, (\phi_{,\mu}), (\phi_{,\mu \nu}) \cdots) \;\vert\;  \eta^{\mu \nu} \phi_{,\mu \nu} + m^2  = 0 \right\}
  \;\subset\;
  J^\infty_\Sigma(\Sigma \times \mathbb{R})
  \,.
$$


=--

Example \ref{FreeScalarFieldEOM} is a special case of the following
important situation.

+-- {: .num_prop #ShellForSpacetimeIndependentLagrangians}
###### Example
**([[Euler-Lagrange operator|Euler-Lagrange variation]] for [[spacetime]]-independent [[Lagrangian densities]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] $E \simeq \Sigma \times F$ over [[Minkowski spacetime]] $\Sigma$
(example \ref{TrivialVectorBundleAsAFieldBundle}).

In general the [[Lagrangian density]] $\mathbf{L}$ is a function of all the spacetime and field coordinates

$$
  \mathbf{L} = L((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots) dvol_\Sigma
  \,.
$$

Consider the special case that $\mathbf{L}$ is _[[spacetime]]-independent_ in that the Lagrangian funtion $L$
is independent of the spacetime coordinate $(x^\mu)$.
Then the same evidently holds for the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).
Therefore in this case the [[shell]] (eqs:ProlongedShellInJetBundle) is itself a [[trivial bundle]] over spacetime.

In this situation every point $\varphi$ in the jet fiber defines a constant section of the shell:

$$
  \label{ConstantSectionOfTrivialShellBundle}
  \Sigma \times \{\varphi\} \subset \mathcal{E}^\infty
  \,.
$$


=--


The following fact is immediate from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime},
but of central importance:


+-- {: .num_prop #HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}
###### Proposition
**([[total derivative|total spacetime derivative]] of [[presymplectic current]] vanishes [[on-shell]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).
Then the [[Euler-Lagrange form]] $\delta_{EL} \mathbf{L}$ and the [[presymplectic current]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) are related by

$$
  d \Omega_{BFV} = - \delta(\delta_{EL}\mathbf{L})
  \,.
$$

In particular this means that the [[total derivative|total spacetime derivative]] of the
presymplectic current vanishes [[on-shell]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

$$
  d \Omega_{BFV}\vert_{\mathcal{E}} \;=\; 0
  \,.
$$

This means that the presymplectic current is indeed a _[[conserved current]]_ (def. \ref{SymmetriesAndConservedCurrents} below) with values in differential 2-forms, whence the name.

=--

+-- {: .proof}
###### Proof

By prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} we have

$$
  \delta \mathbf{L} = \delta_{EL} \mathbf{L} - d \Theta
  \,.
$$

The claim follows from applying the [[variational derivative]] $\delta$ to both sides,
using $\delta^2 = 0$ and $\delta \circ d = - d \circ \delta$.

=--

$\,$


## Symmetries


+-- {: .num_defn #Variation}
###### Definition
**(variation)**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{Fields}).


A _variation_ is a [[vertical vector field]] $v$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) hence a vector field which
vanishes when evaluated in the [[horizontal differential forms]].

In the special case that the [[field bundle]] is [[trivial vector bundle]] over [[Minkowski spacetime]] as in example \ref{TrivialVectorBundleAsAFieldBundle},
a variation is of the form

$$
  v = v^a \partial_{\phi^a} + v^a_{,\mu} \partial_{\phi^a_{,\mu}} + v^a_{\mu_1 \mu_2} \partial_{\phi^a_{\mu_1 \mu_2}} + \cdots
$$

=--

The concept of variation in def. \ref{Variation} is very general, in that it allows to vary the
field coordinates independently from the corresponding jets. This generality is necessary for
discussion of symmetries of [[presymplectic currents]] in def. \ref{HamiltonianForms} below.
But for discussion of symmetries of [[Lagrangian densities]] we are interested in
explicitly varying just the [[field (physics)|field]] coordinates (def. \ref{EvolutionaryVectorField} below)
and inducing from this the corresponding variations of the field derivatives (prop. \ref{EvolutionaryVectorFieldProlongation}) below.

In order to motivate the following definition \ref{EvolutionaryVectorField}
of _[[evolutionary vector fields]]_ we follow remark \ref{ReplacingBundleMorphismsByDifferentialOperators}
saying that concepts in [[variational calculus]] are obtained from their analogous concepts
in plain [[differential calculus]] by replacing plain [[bundle morphisms]] by morphism out of
the [[jet bundle]]:

Given a [[fiber bundle]] $E \overset{fb}{\to} \Sigma$, then a _[[vertical vector field]]_ on $E$ is
of course a [[section]] of its [[vertical vector bundle]] $V_\Sigma E$, hence is a [[bundle morphism]]
as shown here on the left:

$$
  \array{
    E && \overset{\text{vertical vector field}}{\longrightarrow} && V_\Sigma E
    \\
    & {}_{\mathllap{id}}\searrow && \swarrow
    \\
    && E
  }
  \phantom{AAAAAAAAA}
  \array{
    J^\infty_\Sigma E && \overset{\text{evolutionary vector field}}{\longrightarrow} && V_\Sigma E
    \\
    & {}_{\mathllap{id}}\searrow && \swarrow
    \\
    && E
  }
$$

The variational version replaces the vector bundle on the left here with its jet bundle:

+-- {: .num_defn #EvolutionaryVectorField}
###### Definition
**([[evolutionary vector fields]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]]. Then an [[evolutionary vector field]] $v$ on $E$ is a
a "variational vertical vector field" on $E$, hence a smooth [[bundle]] [[homomorphism]]
out of the [[jet bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})



$$
  \array{
    J^\infty_\Sigma E
    && \overset{v}{\longrightarrow} &&
    V_\Sigma E
    \\
    & {}_{\mathllap{jb_{\infty,0}}}\searrow && \swarrow_{\mathllap{}}
    \\
    && E
  }
$$

to the [[vertical vector bundle]] $V_\Sigma E \overset{}{\to} \Sigma$ of $E \overset{fb}{\to} \Sigma$.

We write

$$
  \Gamma_E^{ev}\left( V_\Sigma E \right)
  \;\in\;
  \Omega^{0,0}_\Sigma(E) Mod
$$

for the space of evolutionary vector fields,
regarded as a [[module]] over the $\mathbb{R}$-[[associative algebra|algebra]]

$$
  \Omega^{0,0}_\Sigma(E)
  \;=\;
  C^\infty\left( J^\infty_\Sigma(E) \right)
$$

of [[smooth functions]] on the [[jet bundle]].


=--

An [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField}) describes
an infinitesimal change of field values _depending_ on, possibly, the point in spacetime and the values of the field
and all its derivatives (locally to finite order, by prop. \ref{JetBundleIsLocallyProManifold}).
This induces a corresponding infinitesimal change of the derivatives of the fields, called the _prolongation_
of the evolutionary vector field:


+-- {: .num_prop #EvolutionaryVectorFieldProlongation}
###### Proposition
**(prolongation of [[evolutionary vector field]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]].

Given an [[evolutionary vector field]] $v$ on $E$ (def. \ref{EvolutionaryVectorField})
there is a unique [[vector field]] $\hat v$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) such that

1. $\hat v$ agrees on field coordinates (as opposed to field derivatives) with $v$:

   $$
     (jb_{\infty,0})_\ast(\hat v) = v
     \,;
   $$

1. contraction with $\hat v$ anti-commutes with the [[total derivative|total spacetime derivative]]:

   $$
     \label{ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative}
     \iota_{\hat v} \circ d + d \circ \iota_{\hat v} = 0
     \,.
   $$

In particular [[Cartan's homotopy formula]]
for the [[Lie derivative]] $\mathcal{L}_{\hat v}$ holds with respect to the [[variational derivative]] $\delta$:

$$
 \label{HomotopyFormulaForLieDerivativeAlongProlongationOfEvolutionaryVectorField}
  \mathcal{L}_{\hat v} = \delta \circ \iota_{\hat v} + \iota_{\hat v} \circ \delta
$$

In the special case that the fiber bundle is a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with [[field (physics)|field]] coordinates $\phi^a$, so that
$v$ has the expansion

$$
  v = v^a \partial_{\phi^a}
$$

then $\hat v$ is given by

$$
  \hat v = \underoverset{n = 0}{\infty}{\sum} \frac{d^n v^a}{ d x^{\mu_1} \cdots d x^{\mu_n} } \partial_{\phi^a_{\mu_1 \cdots \mu_n}}
  \,.
$$


=--

+-- {: .proof}
###### Proof

It is sufficient to prove the coordinate version of the statement.
We prove this by [[induction]] over the maximal jet order $k$. Notice that the coefficient of $\partial_{\phi^a_{\mu_1 \cdots \mu_k}}$
in $\hat v$ is given by the contraction $\iota_{\hat v} \delta \phi^a_{\mu_1 \cdots \mu_k}$.

Similarly (at "$k = -1$") the component of $\partial_{\mu_1}$ is given by $\iota_{\hat v} d x^{\mu}$. But by the second condition
above this vanishes:

$$
  \begin{aligned}
    \iota_{\hat v} d x^\mu
    & =
    d \iota_{\hat v} x^\mu
    \\
    & =
    0
  \end{aligned}
$$

Moreover, the coefficient of $\partial_{\phi^a}$ in $\hat v$ is fixed by the first condition above to be

$$
  \iota_{\hat v} \delta \phi^a
  =
  v^a
  \,.
$$

This shows the statement for $k = 0$. Now assume that the statement is true up to some $k \in \mathbb{N}$.
Observe that the coefficients of all $\partial_{\phi^a_{\mu_1 \cdots \mu_{k+1}}}$ are fixed by the
contractions with $\delta \phi^a_{\mu_1 \cdots \mu_{k} \mu_{k+1}} \wedge d x^{\mu_{k+1}}$. For this we find again from the second
condition and using $\delta \circ d + d \circ \delta = 0$ as well as the induction assumption that

$$
  \begin{aligned}
    \iota_{\hat v} \delta \phi^a_{\mu_1 \cdots \mu_{k+1}} \wedge d x^{\mu_{k+1}}
    & =
    \iota_{\hat v}  \delta d \phi^a_{\mu_1 \cdots \mu_k}
    \\
    & =
    d \iota_{\hat v} \delta \phi^a_{\mu_1 \cdots \mu_k}
    \\
    &
    = d \frac{d^k v^a}{d x^{\mu_1} \cdots d x^{\mu_k}}
    \\
    & =
    \frac{d^{k+1}v^a }{d x^{\mu_1} \cdots d x^{\mu_{k+1}}} d x^{\mu_{k+1}}
    \,.
  \end{aligned}
$$

This shows that $\hat v$ satisfying the two conditions given exists uniquely. Finally
the formula for the [[Lie derivative]] follows from the second of the two conditions with [[Cartan's homotopy formula]]
$\mathcal{L}_{\hat v} = \mathbf{d} \circ \iota_{\hat v} + \iota_{\hat v} \circ \mathbf{d}$
together with $\mathbf{d} = \delta + d$ (eqs:VariationalDerivative).

=--


+-- {: .num_prop #EvolutionaryVectorFieldLieAlgebra}
###### Proposition
**([[evolutionary vector fields]] form a [[Lie algebra]])

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]]. For any two [[evolutionary vector fields]]
$v_1$, $v_2$ on $E$ (def. \ref{EvolutionaryVectorField}) the [[Lie bracket]] of [[vector fields]]
of their prolongations $\hat v_1$, $\hat v_2$ (def. \ref{EvolutionaryVectorFieldProlongation})
is itself the prolongation $\widehat{[v_1, v_2]}$ of a unique evolutionary vector field $[v_1,v_2]$.

This defines the structure of a [[Lie algebra]] on evolutionary vector fields.

=--

+-- {: .proof}
###### Proof

It is clear that $[\hat v_1, \hat v_2]$ is still [[vertical vector field|vertical]], therefore by
prop. \ref{EvolutionaryVectorFieldProlongation} it is sufficient to show that contraction with this
vector field anti-commutes with the [[horizontal derivative]] $d$,
hence that $[d, \iota_{[\hat v_1, \hat v_2]}] = 0$.

Now $[d, \iota_{[\hat v_1, \hat v_2]}]$ is an
operator that sends vertical 1-forms to horizontal 1-forms and vanishes on
horizontal 1-forms. Therefore it is sufficient to see that this operator
in fact also vanishes on all vertical 1-forms. But for this it is
sufficient that it commutes with the vertical derivative.
This we check by [[Cartan calculus]], using $[d,\delta] = 0$ and $[d, \iota_{\hat v_i}]$, by assumption:

$$
  \begin{aligned}
    [\delta, [d,\iota_{[\hat v_1, \hat v_2]}] ]
    & =
    - [d, [\delta, \iota_{[\hat v_1, \hat v_2]}]]
    \\
    & =
    - [d,  \mathcal{L}_{[\hat v_1, \hat v_2]}]
    \\
    & =
    -[d, [\mathcal{L}_{\hat v_1}, \iota_{\hat v_2}]  ]
    \\
    & =
    - [d, [ [\delta, \iota_{\hat v_1}], \iota_{\hat v_2}  ]]
    \\
    & =
    0
    \,.
  \end{aligned}
$$



=--

Now given an evolutionary vector field, we want to consider the [[flow]] that it
induces on the [[space of field histories]]:

+-- {: .num_defn #FlowOfFieldHistoriesAlongEvolutionaryVectorField}
###### Definition
**([[flow]] of [[field (physics)|field]] [[trajectory|histories]] along [[evolutionary vector field]])

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{Fields})
and let $v$ be an [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField})
such that the ordinary [[flow]] of its prolongation $\hat v$ (prop. \ref{EvolutionaryVectorFieldProlongation})

$$
  \exp(t \hat v)
  \;\colon\; J^\infty_\Sigma(E) \longrightarrow J^\infty_\Sigma(E)
$$

exists on the [[jet bundle]] (e.g. if the order of derivatives of field coordinates that it depends
on is bounded).


For $\Phi \in \Gamma_\Sigma(E)$ a [[field (physics)|field]] history,
hence a point in the [[space of field histories]] (eqs:SpaceOfFieldHistories), the _[[flow]]_ of $v$
through $\Phi$ is the [[smooth function]]

$$
  \mathbb{R}^1
   \overset{\exp(v)(\Phi)}{\longrightarrow}
  \Gamma_\Sigma(E)
$$

whose unique factorization $\widehat{\exp(v)}(\Phi)$ through the space of jets of field histories

$$
  \array{
    && im(j^\infty_\Sigma) &\hookrightarrow& \Gamma_\Sigma(J^\infty_\Sigma(E))
    \\
    & {}^{\mathllap{\widehat{\exp(v)}(\Phi)}} \nearrow& \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbb{R}^1
      &\underset{ \exp(v)(\Phi) }{\longrightarrow}&
    \Gamma_{\Sigma}(E)_{}
  }
$$

takes a plot $t_{(-)} \;\colon\; U \to \mathbb{R}^1$ of the [[real line]], regarded as a [[smooth space]], to the plot

$$
  \label{LocalDataForFlowOfImplicitInfinitesimalGaugeSymmetry}
  (\exp(t(-) \hat v) \circ j^\infty_\Sigma(\Phi(-))
    \;\colon\:
  U \times \Sigma \longrightarrow J^\infty_\Sigma E )
$$

of the [[smooth space|smooth]] [[space of sections]] of the [[jet bundle]].

(That $\exp(t(-) \hat v)$ indeed flows jet prolongations $j^\infty_\Sigma(\Phi(-))$ again to jet prolongations
is due to its defining relation to the [[evolutionary vector field]] $v$ from prop. \ref{EvolutionaryVectorFieldProlongation}.)

=--



+-- {: .num_defn #SymmetriesAndConservedCurrents}
###### Definition
**([[infinitesimal symmetries of the Lagrangian]] and [[conserved currents]])

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then

1. an _[[infinitesimal symmetry of the Lagrangian]]_ is a variation $v$ (def. \ref{Variation})
   which arises as the prolongation $\hat v$ (prop. \ref{EvolutionaryVectorFieldProlongation})
   of  an [[evolutionary vector field]] $v$ (def. \ref{EvolutionaryVectorField}) such that the [[Lie derivative]] $\mathcal{L}_v$ of the Lagrangian density along $\hat v$ is a [[total derivative|total spacetime derivative]]

   $$
     \mathcal{L}_v \mathbf{L} = d \tilde J_v
   $$


1. an _[[on-shell]] [[conserved current]]_ is a horizontal $p$-form $J \in \Omega^{p,0}_\Sigma(E)$
   whose [[total derivative|total spacetime derivative]] vanishes on the [[shell]] (eqs:ShellInJetBundle)

   $$
     d J\vert_{\mathcal{E}} = 0
     \,.
   $$

=--




+-- {: .num_prop #NoethersFirstTheorem}
###### Proposition
**([[Noether's theorem]] I)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If $v$ is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
with $\mathcal{L}_v \mathbf{L} = d \tilde J_v$, then

$$
  J_v \coloneqq \tilde J_v - \iota_v \Theta
$$

is an [[on-shell]] [[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}), for $\Theta$
a presymplectic potential (eqs:PresymplecticPotential) from def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

=--

+-- {: .proof}
###### Proof

By [[Cartan's homotopy formula]] for the [[Lie derivative]] and using (eqs:dLDecomposition)
and the fact that the variation vector field $v$ vanishes on horizontal differential forms
we may re-express the defining equation for the symmetry as

$$
  \begin{aligned}
    d \tilde J
    & =
    \mathcal{L}_v \mathbf{L}
    \\
    & =
    \iota_v \underset{= \delta_{EL}\mathbf{L} - d \Theta}{\underbrace{\mathbf{d} \mathbf{L}}}
    +
    \mathbf{d} \underset{= 0}{\underbrace{\iota_v \mathbf{L}}}
    \\
    & =
    \iota_v \delta_{EL} \mathbf{L}
    + d \iota_v \Theta
  \end{aligned}
$$

which is equivalent to

$$
  d(\underset{= J_v}{\underbrace{\tilde J - \iota_v \Theta}}) = \iota_v \delta_{EL}\mathbf{L}
$$

Since by definition of $\mathcal{E}$ the form $\frac{\delta_{EL} \mathbf{L}}{\delta v}$ vanishes on $\mathcal{E}$
this yields the claim.

=--


+-- {: .num_prop #FlowAlongImplicitInfinitesimalGaugeSymmetryPreservesOnShellSpaceofFieldHistories}
###### Proposition
**([[flow]] along [[infinitesimal symmetry of the Lagrangian]] preserves [[on-shell]] [[space of field histories]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

For $v$ an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
the [[flow]] on the [[space of field histories]] that it induces by def. \ref{FlowOfFieldHistoriesAlongEvolutionaryVectorField}
preserves the space of [[on-shell]] field histories (from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

$$
  \array{
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
      &\hookrightarrow&
    \Gamma_\Sigma(E)
    \\
    {}^{\mathllap{\exp(\hat v)\vert_{\delta_{EL}\mathbf{L} = 0}  }}
    \uparrow
      &&
    \uparrow^{\mathrlap{\exp(\hat v)}}
    \\
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
      &\hookrightarrow&
    \Gamma_\Sigma(E)
  }
$$

=--


+-- {: .proof}
###### Proof

By def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} a field history
$\Phi$ is [[on-shell]] precisely if

$$
  j^\infty_\Sigma(\Phi(-))^\ast(\delta_{EL}\mathbf{L}) = 0
$$

and by prop. \ref{PrincipleOfExtremalAction} this is the case precisely if for
all [[bump functions]] $b \in C^\infty_{cp}(\Sigma)$ the [[integration of differential forms|integral]]
against $b dvol_\Sigma$ vanishes

$$
  \int_\Sigma j^\infty_\Sigma(\Phi(-))^\ast(\delta_{EL}\mathbf{L}) \, b dvol_\Sigma
  \;=\;
  0
  \,.
$$


Hence we need to show that this holds true also for all values $t$ of the flow parameter
if it holds at $t = 0$, hence that the above implies for  all bump functions $b$ that

$$
  \begin{aligned}
    \int_\Sigma
    \left(
      \exp(t \hat v)
        \circ
      j^\infty_\Sigma(\Phi(-))
    \right)^\ast (\delta_{EL}\mathbf{L})
    \, b dvol_\Sigma
    & =
    \int_\Sigma
      (j^\infty_\Sigma(\Phi(-)))^\ast
      \exp(t \hat v)^\ast
      (\delta_{EL}\mathbf{L})
      \,
      b dvol_\Sigma
    \\
    & =
    0
  \end{aligned}
$$

for all $t \in \mathbb{R}^1$. But since we know it holds true at one point $t = 0$,
it is in fact sufficient to show that the [[derivative]] of this smooth family of
differential forms with respect to $t$ vanishes at all $t$. This argument in turn is
the same at $t = 0$ as at any other value, so we consider the derivative at $t = 0$.

Now by definition of [[Lie derivatives]], the derivative of the above expression with respect to $t$ at $t = 0$ is given
by the Lie derivative $\mathcal{L}_{\hat v}$ via

$$
    \frac{d}{d t }
    \int_\Sigma
    \left(
        (j^\infty_\Sigma(\Phi(-)))^\ast
        \exp(t \hat v)^\ast
        (\delta_{EL}\mathbf{L})
    \right)
    \, b dvol_\Sigma
    \vert_{t = 0}
    =
    \int_\Sigma
    (j^\infty_\Sigma(\Phi(-)))^\ast
    \underset{= d (\iota_{\hat v} -\delta J_v)  \Omega_{BFV} }{
    \underbrace{
     \mathcal{L}_{\hat v}
     \delta_{EL}\mathbf{L}
     }}
     \,
     b dvol_\Sigma
  \,.
$$

We compute that the Lie derivative has the value indicated under the braces as follows:

$$
  \begin{aligned}
     \mathcal{L}_{\hat v} \delta_{EL}\mathbf{L}
     & =
     \iota_{\hat v}
       \underset{ = - d\Omega_{BFV} }{\underbrace{\delta \delta_{EL} \mathbf{L}} }
     + \delta \,\underset{= d J_v}{\underbrace{\iota_{\hat v} \delta_{EL}\mathbf{L}}}
     \\
     & =
     - \iota_{\hat v} d\Omega_{BFV}  + \delta d J_v
     \\
     & =
     d \left(\iota_{\hat v} \Omega_{BFV} - \delta J_v \right)
  \end{aligned}
$$

Here we first used [[Cartan's homotopy formula]] for evolutionary vector fields (eqs:HomotopyFormulaForLieDerivativeAlongProlongationOfEvolutionaryVectorField),
then, under the braces,
the [[conserved current]] property of the presymplectic current (prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}) as well as [[Noether's theorem|Noether's theorem I]] (prop. \ref{NoethersFirstTheorem}),
and finally
the defining verticality condition of prolongations of evolutionary vector fields (prop. \ref{EvolutionaryVectorFieldProlongation})
as well as the anti-commutativity of $\delta$ and $d$.

Hence continuing the computation of the derivative above we have

$$
  \begin{aligned}
    \frac{d}{d t }
    \int_\Sigma
    \left(
        (j^\infty_\Sigma(\Phi(-)))^\ast
        \exp(t \hat v)^\ast
        (\delta_{EL}\mathbf{L})
    \right)
    \, b dvol_\Sigma
    \vert_{t = 0}
    & =
    -
    \int_\Sigma
    (j^\infty_\Sigma(\Phi(-)))^\ast
    d (\iota_{\hat v} \Omega_{BFV} - \delta J_v)
    \,
    b dvol_\Sigma
    \\
    & =
    - \int_\Sigma d j^\infty_\Sigma(\Phi(-))^\ast (\iota_{\hat v}\Omega_{BFV} -  \delta J_v) \, b dvol_\Sigma
    \\
    & = 0
  \end{aligned}
$$

by prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative}.


=--


+-- {: .num_example #ScalarFieldEnergyMomentum}
###### Example
**([[energy-momentum]] of the [[scalar field]])

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[scalar field]] from def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}:

$$
  \mathbf{L}
  \;=\;
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu}\phi_{,\mu} \phi_{,\nu}
    +
    m^2 \phi^2
  \right)
  dvol_\Sigma
  \,.
$$

For $\nu \in \{0, 1, \cdots, p\}$ consider the vector field on the jet bundle given by

$$
  v_\nu
  \;\coloneqq\;
  \phi_{,\nu} \partial_{\phi}
  +
  \phi_{,\mu \nu} \partial_{\phi_{,\mu}}
  +
  \cdots
  \,.
$$

This describes infinitesimal translations of the fields in the direction of $\partial_\nu$.

And this is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}), since

$$
  \iota_{v_\nu} \mathbf{d}\mathbf{L}
  =
  d L \wedge \iota_{\partial_\nu} dvol_\Sigma
  \,.
$$

With the formula (eqs:PresymplecticPotentialOfFreeScalarField) for the presymplectic potential

$$
  \Theta
    =
  \eta^{\mu \nu} \phi_{,\mu} \delta \phi \iota_{\partial_{\nu}} dvol_\Sigma
$$

it hence follows from [[Noether's theorem]] (prop. \ref{NoethersFirstTheorem}) that the corresponding
[[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}) is

$$
  \begin{aligned}
    T_\nu
     & =
     L \, \iota_{\partial_\nu} dvol_\Sigma
     -
     \iota_{v_\nu}\Theta
     \\
     &
     =
     L \, \iota_{\partial_\nu} dvol_\Sigma
     -
     \eta^{\rho \mu} \phi_{,\rho} \phi_{,\nu}
     \,
     \iota_{\partial_\mu} dvol_\Sigma
     \\
     &  =
     (
     \underset{=: T^\mu_\nu}{
     \underbrace{
       \delta^\mu_\nu  L
       -
       \eta^{\rho \mu} \phi_{,\rho} \phi_{,\nu}
     }
     }
     )
     \,
     \iota_{\partial_\mu} dvol_\Sigma
   \end{aligned}
   \,.
$$

This [[conserved current]] is called the _[[energy-momentum tensor]]_.


=--


Evidently [[Noether's theorem|Noether's theorem I]] in [[variational calculus]] (prop. \ref{NoethersFirstTheorem})
is the special case for horizontal $p+1$-forms of a more general phenomenon relating
symmetries of variational forms to forms that are closed up to a contraction. The same phenomenon applied instead
to the [[presymplectic current]] yields the following:


+-- {: .num_defn #HamiltonianForms}
###### Definition
**([[Hamiltonian vector fields|infinitesimal symmetry of the presymplectic potential]] and [[Hamiltonian differential forms]])

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] with presymplectic potential $\Theta$ (eqs:PresymplecticPotential).
Write $\mathcal{E} \hookrightarrow J^\infty_\Sigma(E)$ for the [[shell]] (eqs:ShellInJetBundle).

1. An [[on-shell]] variation $v$ (def. \ref{Variation}) is an _infinitesimal symmetry of the Lepage form_
   or _[[Hamiltonian vector field]]_ if [[on-shell]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) its [[Lie derivative]] along $v$ is a [[variational derivative]]:

   $$
     \mathcal{L}_v  \Theta  = \delta \tilde H_v
     \phantom{AAA}
     \text{on}\, \mathcal{E}
   $$

   for some variational form $\tilde H_v$.

1. A _[[Hamiltonian differential form]]_ $H$ (or _local Hamiltonian current_) is a variational form on the shell such that there
   exists a variation $v$ with

   $$
     \delta H = \iota_v \Omega_{BFV}
     \phantom{AA}
     \,
     \text{on}\, \mathcal{E}
     \,.
   $$

We write

$$
  \Omega^{p,0}_{\Sigma, Ham}(E)
  \;\coloneqq\;
  \left\{
    (H,v)
    \;\vert\;
    v \, \text{is a variation and}\,
    \iota_v \Omega_{BFV} = J
  \right\}
$$

for the space of pairs consisting of a Hamiltonian differential forms [[on-shell]] and a corresponding variation.

=--

+-- {: .num_prop #HamiltonianDifferentialForms}
###### Proposition
**([[Hamiltonian Noether's theorem]])**

A variation $v$ is an infinitesimal symmetry of the presymplectic potential (def. \ref{HamiltonianForms})
with $\mathcal{L}_v ( \Theta ) = \delta \tilde H_v$ precisely if

$$
  H_v \coloneqq \tilde H_v - \iota_v \Theta
$$

is a [[Hamiltonian differential form]] for $v$.


=--

+-- {: .proof}
###### Proof

By [[Cartan's homotopy formula]] for the [[Lie derivative]] we have

$$
  \begin{aligned}
    \mathcal{L}_v  \Theta
    & =
    \underset{
      = \delta \iota_v \Theta - \iota_v d \Theta
    }{
      \underbrace{
        \mathbf{d} \iota_v \Theta
      }
    }
    +
    \underset{
      \iota_v \delta \Theta + \iota_v d \Theta
    }{
    \underbrace{
    \iota_v \mathbf{d} \Theta
    }}
    \\
    & =
    \delta \iota_v \Theta + \iota_v \underset{ = \Omega_{BFV}}{\underbrace{\delta \Theta}}
    \,.
  \end{aligned}
$$

This directly implies the claim.

=--

$\,$

**[[Noether theorem]] and [[Hamiltonian Noether theorem]]**

| $\,$ [[variational differential forms|variational form]] $\,$  |   $\,$ [[symmetry]] $\,$ | $\,$ [[Cartan's homotopy formula|homotopy formula]] $\,$ | $\,$ physical quantity $\,\,\,$ | $\,$ [[Lie n-algebra|local symmetry algebra]] $\,$ |
|----|----------|----------------------------|---------------------------------|------|
| [[Lagrangian density]] $\mathbf{L}$  | $\mathcal{L}_v \mathbf{L} = d \tilde J$  | $\Leftrightarrow d(\underset{= J_v}{\underbrace{\tilde J - \iota_v \Theta}}) = \iota_v \, \delta_{EL}\mathbf{L}$ | [[conserved current]] $J_v$ | [[Dickey bracket]] |
| [[presymplectic current]] $\Omega_{BFV}$ | $\mathcal{L}_v \Theta = \delta \tilde H$ | $\Leftrightarrow \delta(\underset{= H_v}{\underbrace{\tilde H_v - \iota_v \Theta}}) = \iota_v \Omega_{BFV}$ | [[Hamiltonian differential form|Hamiltonian form]] $H_v$ | [[Poisson bracket Lie n-algebra|local Poisson bracket]] |



$\,$


Since therefore both the [[conserved currents]] from [[Noether's theorem]] as well as
the [[Hamiltonian differential forms]] are generators of infinitesimal [[symmetries]] of certain variational forms
(namely of the [[Lagrangian density]] and of the [[presymplectic current]], respectively) they
form a [[Lie algebra]]. For the conserved currents this is sometimes known as the _[[Dickey bracket]] Lie algebra_.
For the Hamiltonian forms it is the _[[Poisson bracket Lie n-algebra|Poisson bracket Lie p+1-algebra]]_. Since here for simplicity
we are considering just vertical variations, we have just a plain [[Lie algebra]].
The [[transgression of variational differential forms|transgression]] of this Lie algebra of Hamiltonian forms
on the jet bundle to [[Cauchy surfaces]] yields a [[presymplectic structure]] on [[phase space]], this we discuss
[below](#PhaseSpace).


+-- {: .num_example #LocalPoissonBracket}
###### Proposition
**([[Poisson bracket Lie n-algebra|local Poisson bracket]])

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

On the space $\Omega^{p,0}_{\Sigma,Ham}(E)$ pairs $(H,v)$ of [[Hamiltonian differential forms]] $H$ with compatible variation $v$ (def. \ref{HamiltonianForms}) the following operation constitutes a [[Lie bracket]]:

$$
  \label{LocalPoissonLieBracket}
  \left\{(H_1, v_1),\, (H_2, v_2)\right\}
  \;\coloneqq\;
  (\iota_{v_1} \iota_{v_2} \Omega_{BFV},\, [v_1,v_2])
  \,.
$$

(Here $[v_1, v_2]$ denotes the ordinary Lie bracket of [[vector fields]].)

We call this the _local Poisson Lie bracket_.

=--


+-- {: .proof}
###### Proof

First we need to check that the bracket is well defined in itself. It
is clear that it is linear and skew-symmetric, but what needs proof is that
it does indeed land in $\Omega^{p,0}_{\Sigma,Ham}(E)$, hence that the following
equation holds:

$$
  \delta \iota_{v_2} \iota_{v_1} \Omega_{BFV}
  \;=\;
  \iota_{[v_1, v_2]} \Omega_{BFV}
  \,.
$$

To see this we use [[Cartan calculus]]:

Since the variation $v$ is purely vertical, by definition, contraction with $v$ anti-commutes with
the total horizontal derivative:

$$
  d \circ \iota_{v} + \iota_v \circ d = 0
  \,.
$$

This makes [[Cartan's homotopy formula]] for the [[Lie derivative]]

$$
  \mathcal{L}_v = \mathbf{d} \circ \iota_v + \iota_v \circ \mathbf{d}
$$

have an analogue with the full de Rham differential replaced by the [[variational derivative]] ([[vertical derivative]])
$\delta = \mathbf{d} - d$:

$$
  \mathcal{L}_v = \delta \circ \iota_v + \iota_v \circ \delta
  \,.
$$


With this we compute as follows:


$$
  \begin{aligned}
    \delta \iota_{v_1} \iota_{v_2} \Omega_{BFV}
    & =
    \tfrac{1}{2} \delta \iota_{v_1} \iota_{v_2} \Omega_{BFV}
    -
    \tfrac{1}{2} (v_1 \leftrightarrow v_2)
    \\
    & =
    \tfrac{1}{2}
    \left(
      \mathcal{L}_{v_1} \iota_{v_2} \Omega_{BFV}
      -
      \iota_{v_1} \delta \iota_{v_2} \Omega_{BFV}
    \right)
    -
    \tfrac{1}{2} (v_1 \leftrightarrow v_2)
    \\
    & =
    \tfrac{1}{2}
    \left(
      \mathcal{L}_{v_1} \iota_{v_2} \Omega_{BFV}
      -
      \iota_{v_1} \mathcal{L}_{v_2} \Omega_{BFV}
      +
      \iota_{v_1} \iota_{v_2} \underset{= 0}{\underbrace{\delta \Omega_{BFV}}}
    \right)
    -
    \tfrac{1}{2} (v_1 \leftrightarrow v_2)
    \\
    & =
    [\mathcal{L}_{v_2}, \iota_{v_1}] \Omega_{BFV}
    \\
    & =
    \iota_{[v_1, v_2]} \Omega_{BFV}
    \,.
  \end{aligned}
$$

This shows that the bracket is well defined.

It remains to see that the bracket satifies the [[Jacobi identity]]:

$$
\left\{ (H_1, v_1), \left\{ (H_2, v_2), (H_3,v_3) \right\} \right\}
  \;+\; (cyclic)
   \;=\;
  0
$$

hence that

$$
  \left(  \iota_{v_1} \iota_{[v_2,v_3]}  \Omega_{BFV} ,\,   [v_1, [v_2, v_2]] \right)
  \;+\; (cyclic)
  \;=\; 0
  \,.
$$

Here $ [v_1, [v_2, v_3]] + (cyclic) = 0 $ is the ordinary Jacobi identity for [[vector fields]],
and hence what needs to be shown is that

$$
  \iota_{v_1} \iota_{[v_2, v_3]}   \Omega_{BFV} + (cyclic) = 0
$$

We check this by repeated uses of [[Cartan calculus]], using in addition
that

1. $\delta \iota_{v_i} \Omega_{BFV} = 0$

   (since $\iota_{v_i} \Omega_{BFV} = \delta H_i$ by $v_i$ being Hamiltonian)

1. $\mathcal{L}_{v_i} \Omega_{BFV} = 0$

   (since in addition $\delta \Omega_{BFV} = 0$)

1. $\iota_{v_1} \iota_{v_2} \iota_{v_3} \Omega_{BFV} = 0$

   (since $\Omega_{BFV} \in \Omega^{p,2}_\Sigma(E)$ is of vertical degree 2, and since all variations $v_i$ are vertical by assumption).

So we compute as follows (a special case of [FRS 13b, lemma 3.1.1](#Poisson+bracket+Lie+n-algebra#FRS13b)):

$$
  \begin{aligned}
    0
    & =
    \delta \iota_{v_1} \iota_{v_2} \iota_{v_3} \Omega_{BFV}
    \\
    & =
    \mathcal{L}_{v_1} \iota_{v_2} \iota_{v_3} \Omega_{BFV}
    -
    \iota_{v_1} \delta \iota_{v_2} \iota_{v_3} \Omega_{BFV}
    \\
    & =
    \iota_{[v_1, v_2]} \iota_{v_3} \Omega_{BFV}
    +
    \iota_{v_2} \mathcal{L}_{v_1} \iota_{v_3} \Omega_{BFV}
    -
    \iota_{v_1} \mathcal{L}_{v_2} \iota_{v_3} \Omega_{BFV}
    +
    \iota_{v_1} \iota_{v_2} \delta \iota_{v_3} \Omega_{BFV}
    \\
    & =
    \iota_{[v_1, v_2]} \iota_{v_3} \Omega_{BFV}
    +
    \iota_{v_2} \iota_{[v_1,v_3]} \Omega_{BFV}
    -
    \iota_{v_1} \iota_{[v_2, v_3]} \Omega_{BFV}
    \\
    & =
    -
    \iota_{v_1} \iota_{[v_2, v_3]} \Omega_{BFV}
    -
    \iota_{v_2} \iota_{[v_3, v_1]} \Omega_{BFV}
    -
    \iota_{v_3} \iota_{[v_1, v_2]} \Omega_{BFV}
    \,.
  \end{aligned}
$$

=--

$\,$

The [[Poisson bracket Lie n-algebra|local Poisson bracket]] [[Lie algebra]] $(\Omega^{p,0}_{\Sigma,Ham}(E), [-,-])$ from prop.
\ref{LocalPoissonBracket} is but the lowest stage of
a [[higher Lie theory|higher Lie theoretic]] structure called the _[[Poisson bracket Lie n-algebra|Poisson bracket Lie p-algebra]]_.
Here we will not go deeper into this [[schreiber:Higher Structures|higher structure]] (see at _[[schreiber:Higher Prequantum Geometry]]_
for more), but below we will need the following simple shadow of it:

+-- {: .num_lemma #HorizontallyExactFormsDropOutOfLocalLieBracket}
###### Lemma

The horizontally exact Hamiltonian forms constitute a [[Lie ideal]] for the
local Poisson Lie bracket (eqs:LocalPoissonLieBracket).

=--

+-- {: .proof}
###### Proof

Let $E$ be a horizontally exact Hamiltonian form, hence

$$
  E = d K
$$

for some $K$. Write $e$ for a [[Hamiltonian vector field]] for $E$.

Then for $(H,v)$ any other pair consisting of a Hamiltonian form and a corresponding
Hamiltonian vector field, we have

$$
  \begin{aligned}
    \iota_v \, \iota_e \, \Omega_{BFV}
    & =
    \phantom{-}\iota_v \, \delta E
    \\
    & =
    \phantom{-}\iota_v \, \delta \, d \, K
    \\
    & =
    - \iota_v \, d \, \delta K
    \\
    & =
    \phantom{-}d \, \iota_v \, \delta \, K
    \,.
  \end{aligned}
$$

Here we used that the horizontal derivative anti-commutes with the
vertical one by construction of the [[variational bicomplex]], and
 that $\iota_e$ anti-commutes with the horizontal derivative $d$ since the variation $e$ (def. \ref{Variation}) is
by definition vertical.

=--



+-- {: .num_example #LocalPoissonBracketForRealScalarField}
###### Example
**([[Poisson bracket Lie n-algebra|local Poisson bracket]] for [[real scalar field]])**

Consider the [[Lagrangian field theory]] for the [[free field|free]] [[real scalar field]] from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

By example \ref{FreeScalarFieldEOM} is [[presymplectic current]] is

$$
  \Omega_{BFV}
   =
  \eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \wedge \iota_{\partial_\mu} dvol_\Sigma
  \,
$$

The corresponding [[Poisson bracket Lie n-algebra|Poisson bracket Lie (p+1)-algebra]] (prop. \ref{LocalPoissonBracket}) has in degree 0
[[Hamiltonian forms]] (def. \ref{HamiltonianDifferentialForms}) such as

$$
  Q \coloneqq \phi \iota_{\partial_0} dvol_\Sigma \in \Omega^{p,0}(E)
$$

and

$$
  P \coloneqq \eta^{\mu \nu} \phi_{,\mu} \iota_{\partial_\nu} dvol_{\Sigma} \in \Omega^{p,0}(E)
  \,.
$$

The corresponding [[Hamiltonian vector fields]] are

$$
 v_P = \partial_{\phi_{,0}}
$$

and

$$
  v_Q = - \partial_{\phi}
  \,.
$$

Hence the corresponding [[Poisson bracket Lie n-algebra|local Poisson bracket]] is

$$
  \{Q,P\} = \iota_{v_Q} \iota_{v_P} \omega = \iota_{\partial_0} dvol_\Sigma
  \,.
$$

More generally for $b_1, b_2 \in C^\infty_{cp}(\Sigma)$ two [[bump functions]] then

$$
  \{ b_1 Q, b_2 P \} = b_1 b_2 \iota_{\partial_0} dvol_\Sigma
  \,.
$$

=--










+-- {: .num_prop #LocalHeisenbergAlgebra}
###### Definition
**([[Heisenberg Lie n-algebra|local Heisenberg Lie algebra]])

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ whose [[field bundle]] $E$ is a [[trivial vector bundle]]
as in example \ref{TrivialVectorBundleAsAFieldBundle}, its [[jet bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) inherits the structure of a
trivial vector bundle (this is the only case we have been making explicit here anyway, def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}). Hence addition in the [[fibers]]
gives it the structure of a [[group]], by translation.

If the [[presymplectic current]] is [[left invariant differential form|left invariant]] with respect to this
group structure, then it makes sense to ask for that sub Lie algebra
of the [[Poisson bracket Lie n-algebra|local Poisson bracket Lie algebra]] (def. \ref{LocalPoissonBracket}) which covers these
translations. This is the corresponding _[[Heisenberg Lie n-algebra|local Heisenberg algebra]]_.

=--


$\,$


## Observables
 {#ObservablesAndStates}


Given a [[field theory]] as above, then an _[[observable]] quantity_ (or just _[[observable]]_, for short) is a [[smooth function]]

$$
  A \;\colon\; \Gamma_\Sigma(E)_{\delta_{EL} = 0} \longrightarrow \mathbb{C}
$$

on the space of [[on-shell]]
field [[trajectories]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}). We think
of this function as assigning to each physically realizable field history $\Phi$ the value $A(\Phi)$ of the given quantity as exhibited by
that field history. For instance concepts like "avarage field amplitude in spacetime region $\mathcal{O}$" should be
observables.

In _[[local field theory]]_ the idea is that both the [[equations of motion]] as well as the observations
are fully determined by their restriction to [[infinitesimal neighbourhoods]] of spacetime points ([[events]]).
For the equations of motion this means that they are [[partial differential equations]] as we have seen
[above](#EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime). For the observables
it should mean that they must be averages over regions of spacetime of functions of the value of the field histories and their derivatives
_at any point_ of spacetime.
Now a "smooth function of the value of the field field histories and their derivatives at any point"
is precisely a smooth function on the [[jet bundle]] of the [[field bundle]] (example \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
pulled back via [[jet prolongation]] (def. \ref{JetProlongation}).
If this is to be averaged over spacetime it needs to be the coefficient of a horizontal $p+1$-form (prop. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}).

In mathematical terminology these desiderata say that the [[local observables]] in a local field theory should be precisely the
"[[transgression of variational differential forms|transgressions]]" (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below) of horizontal variational $p+1$-forms
(with compact spacetime support, def. \ref{SpacetimeSupport} below) to the [[space of field histories]]. This is
def. \ref{LocalObservables} below.

A key example of a [[local observable]] in [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) is the _[[action functional]]_ (example \ref{ActionFunctional} below). This is the [[transgression of variational differential forms|transgression]]
of the [[Lagrangian density]] itself, or rather of its product with an "[[adiabatic switching]] function" that
localizes its [[support]] in a compact spacetime region. In typical cases the physical quantity whose observation is
represented by the action functional is the difference of the [[kinetic energy|kinetic]] energy-momentum minus the [[potential energy]]
of a field history averaged over the given region of spacetime.

The [[equations of motion]] of a [[Lagrangian field theory]] say that those field histories
are physically realized which are [[critical points]] of this [[action functional]] observable. This is
the _[[principle of extremal action]]_ (prop. \ref{PrincipleOfExtremalAction} below).

This formalizes what it means for a [[field (physics)|field]] history $\Phi$ to be "realizable" (physically admissible)
(a solution to the [[Euler-Lagrange equations]], def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime})
and what the ([[local observable|local]]) [[observable]] quantities on field histories are (def. \ref{LocalObservables}).
It remains to formalize what it means for the [[physical system]] to be in some definite _[[state]]_
so that the [[observable]] quantities take some definite value, reflecting the properties of that state.

Whatever formalization for _[[states]]_ of a [[field theory]] one considers, at the very least
the [[space of states]] $States$ should come with a pairing [[linear map]]

$$
  \array{
    Obs \otimes States & \longrightarrow&  \mathcal{C}
    \\
    \left( A , \langle - \rangle \right) &\mapsto& \langle A \rangle
  }
$$

which reads in an [[observable]] quantity $A$ and a state, to be denoted $\langle - \rangle$,
and produces the [[complex number]] $\langle A \rangle$
which is the "value of the observable quantity $A$ in the case that the physical system is in the state $\langle -\rangle$".

One might imagine that
it is fundamentally possible to pinpoint the exact [[field (physics)|field]] history that the
[[physical system]] is found in. From this perspective fixing a [[state]] should simply mean to
pick an element in the [[on-shell]] [[space of field histories]] $\Phi \in \Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$.
If we write $\langle -\rangle_{\Phi}$ for this state, its pairing map with the states would simply be
[[evaluation]] of the observable, being a function on the field history space, on that particular element in this space:

$$
  \langle A \rangle_{\Phi} \coloneqq A(\Phi)
  \,.
$$

However, in the practice of [[experiment]] a field history can never be known precisely, without remaining uncertainty.
Moreover, [[quantum physics]] (to which we finally come [below](#QuantumObservables)), suggests that this is
true even in principle. Therefore we should allow [[states]] to be a kind of [[probability distributions]]
on the [[space of field histories]], and regard the pairing $\langle A \rangle$ of a state $\langle - \rangle$ with an observable
$A$ as a kind of _[[expectation value]]_ of the function $A$ averaged with respect to this probability distribution.
Specifically if the observable quantity $A$ is (a smooth approximation to) a [[characteristic function]]
of a [[subset]] $S \subset \Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$ of the [[space of field histories]], then its value in a given state should be the [[probability]] to find the [[physical system]] in that that subset of field histories.

But, moreover, the [[superposition principle]] of [[quantum physics]] says that the actually observable observables
are only those of the form $A^\ast A$ (for $A^\ast$ the image under the star-operation on the [[star algebra]]
of observables.

This finally leads to the definition of _[[states]]_ in def. \ref{States} below.


$\,$

+-- {: .num_defn #SpacetimeSupport}
###### Definition
**(spacetime support)**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{Fields}),
with induced [[jet bundle]] $J^\infty_\Sigma(E)$

For every [[subset]] $S \subset \Sigma$ let

$$
  \array{
    J^\infty_\Sigma(E)\vert_S
      &\overset{\iota_S}{\hookrightarrow}&
    J^\infty_\Sigma(E)
    \\
    \downarrow &(pb)& \downarrow
    \\
    S &\hookrightarrow& \Sigma
  }
$$

be the corresponding restriction of the [[jet bundle]] of $E$.

The _spacetime support  _ $supp_\Sigma(A)$ of a [[differential form]] $A \in \Omega^\bullet(J^\infty_\Sigma(E))$
on the [[jet bundle]] of $E$ is the [[topological closure]] of the maximal subset $S \subset \Sigma$
such that the restriction of $A$ to the jet bundle restrited to this subset vanishes:

$$
  supp_\Sigma(A) \coloneqq Cl( \{ x \in \Sigma |  \iota_{\{x\}^\ast A = 0} \} )
$$

We write

$$
  \Omega^{r,s}_{\Sigma,cp}(E)
  \coloneqq
  \left\{
    A \in \Omega^{r,s}_\Sigma(E)
    \;\vert\;
    supp_\Sigma(A) \, \text{is compact}
  \right\}
    \;\hookrightarrow\;
  \Omega^{r,s}_\Sigma(E)
$$

for the subspace of differential forms on the jet bundle whose spacetime support is a [[compact subspace]].

=--

+-- {: .num_defn #TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}
###### Definition
**([[transgression of variational differential forms]] to [[space of field histories]])


Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{Fields}).
and let
$$
  \Sigma_r \hookrightarrow \Sigma
$$

be a [[submanifold]] of [[spacetime]] of dimension $r \in \mathbb{N}$. Recall the [[space of field histories]]
restricted to its [[infinitesimal neighbourhood]], denoted $\Gamma_{\Sigma_r}(E)$ (def. \ref{Fields}).


Then the operation of _[[transgression of variational differential forms]]_ to $\Sigma_r$ is the [[linear map]]

$$
  \tau_{\Sigma_r}
   \;\colon\;
  \Omega^{\bullet,\bullet}_{\Sigma,cp}(E)
    \overset{  }{\longrightarrow}
  \Omega^\bullet\left(
    \Gamma_{\Sigma_r}(E)
   \right)
$$

that sends a variational differential form $A \in \Omega^{\bullet,\bullet}_{\Sigma,cp}(E)$
to the differential form $\tau_{\Sigma_r} \in \Omega^\bullet(\Gamma_{\Sigma_r}(E))$
which to a smooth family on field configurations

$$
  \Phi_{(-)}(-) \;\colon\; U \times N_\Sigma \Sigma_r \longrightarrow E
$$

assigns the differential form given by first forming the [[pullback of differential forms]] along the family of [[jet prolongation]] $j^\infty_\Sigma(\Phi_{(-)})$ followed by the [[integration of differential forms]] over $\Sigma_r$:

$$
  (\tau_{\Sigma}A)_\Phi
    \;\coloneqq\;
  \int_{\Sigma_r}  (j^\infty_\Sigma(\Phi_{(-)}))^\ast A
  \;\in\;
  \Omega^\bullet(U)
  \,.
$$


=--


+-- {: .num_remark #TransgressionToDimensionrSupportedOnHorizontalrForms}
###### Remark
**([[transgression of variational differential forms|transgression]] to dimension $r$ picks out hiorizontal $r$-forms)

In def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}
we regard [[integration of differential forms]] over $\Sigma_r$ as an operation defined on differential forms
of all degrees, which vanishes except on forms of degree $r$, and hence transgression of variational differential forms
to $\Sigma_r$ vanishes except on the subspace

$$
  \Omega^{r,\bullet}_\Sigma(E)
  \;\subset\;
  \Omega^{\bullet,\bullet}_\Sigma(E)
$$

of forms of horizontal degree $r$.

=--

+-- {: .num_example #ActionFunctional}
###### Example
**([[adiabatic switching|adiabatically switched]] [[action functional]])

Given a [[field bundle]] $E \overset{fb}{\longrightarrow} \Sigma$,
consider a [[local Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})

$$
  \mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)
  \,.
$$

For any [[bump function]] $b \in C^\infty_{cp}(\Sigma)$, the [[transgression of variational differential forms|transgression]] of $b \mathbf{L}$
(def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}) is called the _[[action functional]]_

$$
  \mathcal{S}_b \mathbf{L}
    \coloneqq
  \tau_{\Sigma}
  \left(
    b \mathbf{L}
  \right)
  \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \mathbb{R}
$$

induced by $\mathbf{L}$, "[[adiabatic switching|adiabatically switched]]" by $b$.

Specifically if the field bundle is a [[trivial vector bundle]] as in example \ref{TrivialVectorBundleAsAFieldBundle},
such that the Lagrangian density may be written in the form

$$
  \mathbf{L}
    \;=\;
  L
  \left(
    (x^\mu), (\phi^a), (\phi^a_{,\mu}),
    \cdots
  \right)
  \,
  b dvol_\Sigma
   \;\in\;
  \Omega^{p+1,0}_{\Sigma,cp}( E )
  \,.
$$

then its action functional takes a field history $\Phi$ to the value

$$
  \mathcal{S}_{b \mathbf{L}}(\Phi)
  \:\colon\;
  \int_\Sigma
    L
    \left(
      x,
      \left( \Phi^a(x) \right),
      \left(\frac{\partial \Phi^a}{\partial x^\mu}(x)\right),
      \cdots
    \right)
    \,
  b(x)
  dvol_\Sigma(x)
$$

=--


+-- {: .num_prop #TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}
###### Proposition
**([[transgression of variational differential forms|transgression]] compatible with [[variational derivative]])

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{Fields})
and let $\Sigma_r \hookrightarrow \Sigma$ be a [[submanifold]] possibly [[manifold with boundary|with boundary]]
$\partial \Sigma_r \hookrightarrow \Sigma_r$. Write

$$
  \Gamma_{\Sigma_r}(E) \overset{(-)\vert_{\partial \Sigma_r}}{\longrightarrow} \Gamma_{\partial \Sigma_r}(E)
$$

for the boundary restriction map.

Then the operation of [[transgression of variational differential forms]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})

$$
  \tau_{\Sigma} \;\colon\; \Omega^{\bullet,\bullet}_{\Sigma,cp}(E) \longrightarrow \Omega^\bullet\left(\Gamma_{\Sigma_r}(E)\right)
$$

is compatible with the [[variational derivative]] $\delta$ and with the [[total derivative|total spacetime derivative]] $d$
in the following way:

1. On variational forms that are in the image of the total spacetime derivative
   a transgressive [[Stokes' theorem]] holds:

   $$
     \tau_{\Sigma_r}(d \alpha) \;=\; ((-)\vert_{\partial \Sigma})^\ast \tau_{\partial \Sigma_r}( \alpha)
   $$

1. Transgression intertwines, up to a sign, the [[variational derivative]] $\delta$ on variational differential forms with the
   plain de Rham differential on the space of field histories:

   $$
     \tau_{\Sigma}\left(
       \delta \alpha
     \right)
     \;=\;
     (-1)^{p+1}\, d \,\tau_{\Sigma}(\alpha)
     \,.
   $$

=--


+-- {: .proof}
###### Proof

Regarding the first statement, consider a horizontally exact variational form

$$
  d \alpha \in \Omega^{r,s}_{\Sigma,cp}(E)
  \,.
$$

By prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative} the pullback of this form
along the jet prolongation of fields is exact in the $\Sigma$-direction:

$$
  (j^\infty_\Sigma\Phi_{(-)})^\ast(d \alpha )
  \;=\;
  d_\Sigma (j^\infty_\Sigma\Phi_{(-)})^\ast \alpha
  \,,
$$

(where we write $d = d_U + d_\Sigma$ for the de Rham differential on $U \times \Sigma$).
Hence by the ordinary [[Stokes' theorem]] restricted to any $\Phi_{(-)} \colon U \to \Gamma_{\Sigma_r}(E)$
with restriction $(-)\vert_{\partial \Sigma_r} \circ \Phi_{(-)} \colon U \to \Gamma_{\Sigma_r}(E)$
the relation

$$
  \begin{aligned}
    (\Phi_{(-)})^\ast \tau_{\Sigma_r}(d \alpha)
    & =
    \int_{\Sigma_r}
      d_{\Sigma_r} (j^\infty_\Sigma\Phi_{(-)})^\ast\alpha
    \\
    & = \int_{\partial \Sigma_r} (j^\infty_\Sigma\Phi_{(-)})^\ast\alpha
    \\
    & = \int_{\partial \Sigma_r} (j^\infty_\Sigma ( (-)\vert_\Sigma \circ \Phi_{(-)}) )^\ast\alpha
    \\
    & =
    ( (-)\vert_\Sigma \circ \Phi_{(-)} )^\ast \tau_{\partial \Sigma_r}(\alpha)
    \\
    & =
    (\Phi_{(-)})^\ast ((-)\vert_{\Sigma_r})^\ast \tau_{\partial \Sigma_r}(\alpha)
    \,.
  \end{aligned}
  \,.
$$


Regarding the second statement: by the [[Leibniz rule]] for de Rham differential
([[product law]] of [[differentiation]]) it is sufficient to check the claim on variational
derivatives of local coordinate functions

$$
  \delta \phi^a_{\mu_1 \cdots \mu_k} b
  \in
  \Omega^{0,1}_\Sigma(E)
  \,.
$$

The [[pullback of differential forms]]
along $j^\infty_\Sigma(\Phi_{(-)}) \colon U \times \Sigma \to J^\infty_\Sigma(E)$ has two contributions:
one from the variation along $\Sigma$, the other from variation along $U$:


1. By prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative},
for _fixed_ $u \in U$ the pullback of $\delta \phi^a_{\mu_1 \cdots \mu_k}$ along the jet prolongation vanishes.

1. For  fixed $x \in \Sigma$, the pullback of the full de Rham differential $\mathbf{d} \phi^a_{\mu_1\cdots \mu_k}$ is

   $$
     \begin{aligned}
       (\Phi_{(-)}(x))^\ast( \mathbf{d} \phi^a_{\mu_1\cdots \mu_k} )
       & =
       d_U (\Phi_{(-)}(x))^\ast(\phi^a_{\mu_1\cdots \mu_k})
       \\
       & =
       d_U \frac{ \partial^k \Phi_{(-)}(x)}{\partial x^{\mu^1} \cdots \partial x^{\mu_k}}
     \end{aligned}
   $$

   (since the full de Rham differentials always commute with pullback of differential forms),
   while the pullback of the horizontal derivative
$d \phi^a_{\mu_1\cdots \mu_k} = \phi^a_{\mu_1 \cdots \mu_{k} \mu_{k+1}} \mathbf{d}x^{\mu_{k+1}}$
vanishes at fixed $x \in \Sigma$.

This implies over the given smooth family $\Phi_{(-)}$ that

$$
  \begin{aligned}
    \tau_\Sigma\left(
      \delta \phi^a_{,\mu_1 \cdots \mu_k} b
    \right)\vert_{\Phi_{(-)}}
    & =
    \tau_\Sigma\left(
       \mathbf{d} ( \phi^a_{,\mu_1 \cdots \mu_k} b)
    \right)
    \vert_{\Phi_{(-)}}
      -
    \underset{ = 0 }{
    \underbrace{
    \tau_\Sigma
    \left(
      d (\phi^a_{,\mu_1 \cdots \mu_k} b)
    \right)\vert_{\Phi_{(-)}}
    }}
    \\
    & =
    \int_\Sigma d_U (\Phi_{(-)})^\ast ( \phi^a_{\mu_1\cdots \mu_k} b )
    \\
    & = (-1)^{p+1} d_U \int_\Sigma  (\Phi_{(-)})^\ast ( \phi^a_{\mu_1\cdots \mu_k} b )
    \\
    & = (-1)^{p+1} d_U \tau_{\Sigma}( \Phi_{(-)} )^\ast ( \phi^a_{\mu_1 \cdots \mu_k} )
    \,.
  \end{aligned}
$$

and since this holds covariantly for all smooth families $\Phi_{(-)}$, this implies the claim.

=--


+-- {: .num_example #VariationOfTheActionFunctional}
###### Example
**([[variational derivative|variation]] of the [[action functional]])**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
then the derivative of its [[adiabatic switching|adiabatically switched]] [[action functional]]
(def. \ref{ActionFunctional}) equals the [[transgression of variational differential forms|transgression]]
of the [[Euler-Lagrange variational derivative]] $\delta_{EL} \mathbf{L}$ (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

$$
  d \mathcal{S}_{b \mathbf{L}}
  \;=\;
  \tau_\Sigma( b \delta_{EL}\mathbf{L} )
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the second statement of prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative} we have

$$
  d \mathcal{S}_{b \mathbf{L}}
  \;=\;
  \tau_\Sigma( \delta ( b \mathbf{L} )  )
  \,.
$$

By prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} this is

$$
  \begin{aligned}
    \cdots
    & =
    \tau_\Sigma( b \, \delta_{EL} \mathbf{L} + d \Theta_b )
    \\
    & =
    \tau_\Sigma( b \, \delta_{EL} \mathbf{L} ) + \underset{= 0}{\underbrace{\tau_\Sigma( d \Theta_b )}}
  \end{aligned}
  \,,
$$

where the second term vanishes by the first statement of prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}.

=--


+-- {: .num_defn #EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}
###### Definition
**([[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]])**

Given a [[field bundle]] $E$ over [[spacetime]] $\Sigma$ as in example \ref{TrivialVectorBundleAsAFieldBundle}
equipped with a [[local Lagrangian density]] $\mathbf{L} \in  \Omega^{p+1,1}_{\Sigma}(E)$ as in def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
then the corresponding _[[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]_
on fields $\Phi \in \Gamma_\Sigma(E)$ is the equation

$$
  j^\infty_\Sigma(\Phi)^\ast \left(\delta_{EL} \mathbf{L}\right) = 0
  \,,
$$

where $j^\infty_\Sigma(\Phi) \colon \Sigma \to J^\infty_{\Sigma}(E)$ denotes the [[jet prolongation]] of $\Phi$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), $j^\infty_{\Sigma}(\Phi)^\ast$ the operation of
[[pullback
of differential forms]] along this function, and $\delta_{EL}$ is the
[[Euler-Lagrange operator]] from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

In the case that the field bundle is a trivial vector bundle over Minowski spacetime as in example \ref{TrivialVectorBundleAsAFieldBundle}
this equation is
equivalently the following [[differential equation]] (again using prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

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
     (x^\mu),
     (\Phi^a),
     \left( \frac{\partial \Phi^a}{\partial x^\mu}\right),
     \left( \frac{\partial^2 \Phi^a}{\partial x^\mu \partial x^\nu} \right),
     \cdots
  \right)
  \;=\;
  0
  \,.
$$

We write

$$
  \label{OnShellFieldHistories}
  \Gamma_\Sigma(E)_{\delta_{EL} L = 0}
    \hookrightarrow
  \Gamma_\Sigma(E)
$$

for the [[smooth space|smooth subspace]] of the [[space of field histories]] (eqs:SpaceOfFieldHistories) on those that solve this
differential equation.

This is another incarnation of the "[[shell]]" (eqs:ProlongedShellInJetBundle).

Similarly for $\Sigma_r \hookrightarrow \Sigma$ a [[submanifold]] of [[spacetime]], we write

$$
  \label{OnShellFieldHistoriesInHigherCodimension}
  \Gamma_{\Sigma_r}(E)_{\delta_{EL} L = 0}
    \hookrightarrow
  \Gamma_{\Sigma_r}(E)
$$

for the subspace of on-shell field histories restricted to the [[infinitesimal neighbourhood]]
of $\Sigma_r$ in $\Sigma$ (eqs:SpaceOfFieldHistoriesInHigherCodimension).


=--

+-- {: .num_prop #EquationOfMotionOfFreeRealScalarField}
###### Example
**([[equation of motion]] of [[free field|free]] [[real scalar field]] is [[Klein-Gordon equation]])

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[real scalar field]]
from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

By example \ref{FreeScalarFieldEOM} its [[Euler-Lagrange form]] is

$$
  \delta_{EL}\mathbf{L}
    \;=\;
  \left(\eta^{\mu \nu} \phi_{,\mu \nu} + m^2 \right) \delta \phi \wedge dvol_\sigma
$$

Hence for $\Phi \in \Gamma_\Sigma(E) = C^\infty(X)$ a field trajectory,
its [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]
according to def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} is

$$
  \eta^{\mu \nu} \frac{\partial^2 }{\partial x^\mu \partial x^\nu} \Phi + m^2 \Phi \;=\; 0
$$

often abbreviated as

$$
  (\Box + m^2) \Phi \;=\; 0
  \,.
$$

This [[PDE]] is called the _[[Klein-Gordon equation]]_ on Minowski spacetime. If the [[mass]] $m$
vanishes, $m = 0$, then this is the _relativistic [[wave equation]]_.

=--


+-- {: .num_prop #MaxwellVacuumEquation}
###### Example
**([[equations of motion]] of [[free field|free]] [[electromagnetism]] -- [[vacuum]] [[Maxwell equations]])**

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]]
on [[Minkowski spacetime]] from example \ref{ElectromagnetismLagrangianDensity}.

By example \ref{ElectromagnetismEl} its [[Euler-Lagrange form]] is

$$
  \delta_{EL}\mathbf{L}
    \;=\;
  \frac{d}{d x^\mu}f^{\mu \nu} \delta a_\nu
  \,.
$$

Hence for $A \in \Gamma_{\Sigma}(T^\ast \Sigma) = \Omega^1(\Sigma)$ a field trajectory ("[[vector potential]]"),
its [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]
according to def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} is

$$
  \begin{aligned}
    & \frac{\partial}{\partial x^\mu} F^{\mu \nu} = 0
    \\
    \Leftrightarrow\;\;  &
    d \star_\eta F = 0
  \end{aligned}
  \,,
$$

where $F = d A$ is the [[Faraday tensor]] (eqs:TensorFaraday).
(In the coordinate-free formulation in the second line "$\star_\eta$" denotes
the [[Hodge star operator]] induced by the [[pseudo-Riemannian metric]] $\eta$ on [[Minkowski spacetime]].)

These [[PDEs]] are called the _[[vacuum]] [[Maxwell's equations]]_.

=--


+-- {: .num_prop #PrincipleOfExtremalAction}
###### Proposition
**([[principle of extremal action]])**


Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then the [[de Rham differential]] of the [[action functional]] (def. \ref{VariationOfTheActionFunctional})
vanishes for all [[adiabatic switchings]] $b \in C^\infty_{cp}(\Sigma)$ on a [[field (physics)|field]] history $\Phi$
precisely if $\Phi$ solves the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]
(def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}):

$$
  \left(
  \underset{b \in C^\infty_{cp}(\Sigma)}{\forall}
  \left(
     d \mathcal{S}_{b \mathbf{L}}(\Phi) = 0
  \right)
  \right)
  \;\Leftrightarrow\;
  \left(
    j^\infty_\Sigma(\Phi(-))^\ast ( \delta_{EL} \mathbf{L} ) = 0
  \right)
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative} we have
for each fixed adiabatic switching $b$ the equivalence

$$
  \left(
    d \mathcal{S}_{b \mathbf{L}}(\Phi) \;=\; 0
  \right)
  \;\Leftrightarrow\;
  \left(
    \int_\Sigma
      j^\infty_\Sigma(\Phi(-))^\ast (  \delta_{EL} \mathbf{L} )(x) \, b(x) dvol_\Sigma(x)
    \;=\;
    0
  \right)
  \,.
$$

But if the right hand side holds for all $b$, then $(j^\infty_\Sigma(\Phi(-)))^\ast (\delta_{EL}\mathbf{L}) = 0$.
Because suppose that $j^\infty_\Sigma(\Phi)^\ast (  \delta_{EL} \mathbf{L} )$ does not vanish at some $x \in \Sigma$,
then by continuity it is non-vanishing also on some [[neighbourhood]] of $x$ and hence the integral
of any one of its components
against a non-negative or non-positive bump function $b$ supported inside this neighbourhood is non-vanishing.

=--



+-- {: .num_defn #LocalObservables}
###### Definition
**([[local observables]])**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) with  [[on-shell]] [[space of histories]] $\Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0}$
(eqs:OnShellFieldHistories)
then the space

$$
  \label{GlobalObservables}
  Obs_\Sigma(E)
  \;\coloneqq\;
  C^\infty( \Gamma_\Sigma(E) )
$$

of _[[observables]]_ is simply the space of [[complex numbers|complex]]-valued [[smooth functions]]

$$
  A \;\colon\;  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \longrightarrow \mathbb{C}
$$

on the [[on-shell]] [[space of field histories]].
This is a [[star-algebra]] under pointwise [[complex conjugation]].

(That we consider functions with values in [[complex numbers]] instead of [[real numbers]] is a
reflection of the [[superposition principle]] in [[quantum physics]], more about this below.)

On the other hand the _[[local observables]]_ are the [[horizontal differential form|horizontal p+1-forms]]

1. of compact spacetime support (def. \ref{SpacetimeSupport})

1. modulo [[total spacetime derivatives]]

1. restricted to the [[shell]] $\mathcal{E}^\infty$ (eqs:ProlongedShellInJetBundle):

$$
  LocObs_\Sigma(E) \;\coloneqq\; \left(\Omega^{p+1,0}_{\Sigma,cp}(E)/(im(d))\right)\vert_{\mathcal{E}^\infty}
$$

which we may identify with the subspace of all observables (eqs:GlobalObservables)
on those that arise as the [[image]] under
[[transgression of variational differential forms]] $\tau_\Sigma$ (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
of local observables to [[functionals]] on the [[on-shell]] [[space of field histories]]:

$$
  LocObs_\Sigma(E)
    \overset{\tau_\Sigma}{\hookrightarrow}
  \in
  C^\infty\left( \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \right)
  \,.
$$

This is a sub-vector space inside all observables which is in general not closed under the product of functions. We write

$$
  \mathcal{F}
    \;\coloneqq\;
  \langle LocObs_\Sigma \rangle_{C^\infty\left(\Gamma_\Sigma(E)\right)_{\delta_{EL}\mathbf{L} = 0}}
$$

for the smallest subalgebra of observables, under the pointwise product, that contains all the local observables.
This is called the algebra of _multilocal observables_.

> maybe better consider formal power series of observables around a background solution

=--


+-- {: .num_example }
###### Example
**([[local observables]] of the [[real scalar field]])**

Consider the [[field bundle]] of the [[real scalar field]] (example \ref{RealScalarFieldBundle}).

A typical example of [[local observables]] (def. \ref{LocalObservables}) in this case is
the "field amplitude averaged over a given spacetime region"
determined by a [[bump function]] $b \in C^\infty_{cp}(\Sigma)$. On an on-shell  field configuration $\Phi$ this observable
takes as value the integral

$$
  \tau_\Sigma(b \phi)(\Phi) \;=\;  \int_\Sigma \Phi(x) b(x) dvol_\Sigma(x)
  \,.
$$

=--


+-- {: .num_example }
###### Example
**([[local observables]] of the [[electromagnetic field]])

Consider the [[field bundle]] for [[free field theory|free]] [[electromagnetism]] on [[Minkowski spacetime]] $\Sigma$.

Then for $b \in C^\infty(\Sigma)$ a [[bump function]] on [[spacetime]], the [[transgression of variational differential forms|transgression]]
of the universal [[Faraday tensor]] (def. \ref{JetFaraday}) against $b$ times the [[volume form]] is a [[local observable]]
(def. \ref{LocalObservables}), namely the _[[field strength]]_ (eqs:TensorFaraday) of the [[electromagnetic field]]
averaged over spacetime.

=--

The definition of [[local observables]] in def. \ref{LocalObservables} uses explicit restriction to the [[shell]],
hence, by the [[principle of extremal action]] (prop. \ref{PrincipleOfExtremalAction}) to the
the "[[critical locus]]" of the [[action functional]]. Such [[critical loci]] are often hard to
handle explicitly. It often helps to consider a "[[homological resolution]]" given, in good circumstances, by  the corresponding
"[[derived critical locus]]".

In order to have good control over these resolutions, we now consider the first _[[perturbative quantum field theory|perturbative]]_
aspect of [[field theory]], namely we consider the restriction of [[local observables]] to just an
[[infinitesimal neighbourhood]] of a background [[on-shell]] field history:

+-- {: .num_defn #LocalObservablesOnInfinitesimalNeighbourhood}
###### Definition
**([[local observables]] around [[infinitesimal neighbourhood]] of background [[on-shell]] field history)


Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eqs:ConstantSectionOfTrivialShellBundle)
as in example \ref{ShellForSpacetimeIndependentLagrangians}.

Then we write

$$
  LocObs_\Sigma(E,\varphi)
$$

for the restriction of the [[local observables]] (def. \ref{LocalObservables}) to the fiberwise
[[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of $\Sigma \times \{\varphi\}$.

Explicitly, this means the following:

First of all, by prop. \ref{JetBundleIsLocallyProManifold} the dependence of the Lagrangian density $\mathbf{L}$
on the order of field derivatives is bounded by some $k \in \mathbb{N}$ on some [[neighbourhood]] of $\varphi$ and hence,
by the spacetime independence of $\mathbf{L}$, on some neighbourhood of $\Sigma \times \{\varphi\}$.

Therefore we may restrict without loss to the order-$k$ jets. By slight abuse of notation we still write

$$
  \mathcal{E} \hookrightarrow J^k_\Sigma(E)
$$

for the corresponding shell. It follows then that the restriction of the ring $\Omega^{0,0}_{\Sigma,cp}(E)$ of smooth functions
on the jet bundle to the infinitesimal neighbourhood
is equivalently the [[formal power series ring]] over $C^\infty_{cp}(\Sigma)$
in the variables

$$
  ((\phi^a- \varphi^a),
   (\phi^a_{,\mu}- \varphi^a_{,\mu}),
   \cdots,
   (\phi^a_{,\mu_1 \cdots \mu_k} - \varphi^a_{,\mu_1 \cdots \mu_k})
  )
$$

We denote this by

$$
  \label{FunctionsOnInfNbh}
  \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
    \;\coloneqq\;
  C^\infty_{cp}(\Sigma)\left[ \left[ (\phi^a - \varphi^a ), (\phi^a_{,\mu} -\varphi^a_{,\mu}), \cdots, (\phi^a_{,\mu_1 \cdots \mu_k}- \varphi^a_{,\mu_1 \cdots \mu_k}) \right] \right]
  \,.
$$

A key consequence is that the further restriction of this ring to the [[shell]] $\mathcal{E}^\infty$ (eqs:ProlongedShellInJetBundle)
is now simply the further [[quotient ring]] by the ideal generated by the [[total spacetime derivatives]]
of the components $\frac{\partial_{EL}L}{\delta \phi^a}$ of
the [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).

$$
  \label{ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber}
  \begin{aligned}
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}}
      & \coloneqq
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
      /
    \left(
      \frac{d^k}{ d x^{\mu_1} \cdots d x^{\mu_l}} \frac{\delta_{EL} L}{\delta \phi^a}
    \right)_{ { a \in \{1, \cdots, s\} }  \atop { { l \in \{1, \cdots, k\} } \atop { \mu_r \in \{0, \cdots, p\} }   } }
    \\
    & =
  C^\infty_{cp}(\Sigma)\left[ \left[ (\phi^a - \varphi^a ), (\phi^a_{,\mu} -\varphi^a_{,\mu}), \cdots, (\phi^a_{,\mu_1 \cdots \mu_k}- \varphi^a_{,\mu_1 \cdots \mu_k}) \right] \right]
   /
  \left(
    \frac{d^k}{ d x^{\mu_1} \cdots d x^{\mu_l}} \frac{\delta_{EL} L}{\delta \phi^a}
  \right)_{ { a \in \{1, \cdots, s\} }  \atop { { l \in \{1, \cdots, k\} } \atop { \mu_r \in \{0, \cdots, p\} }   } }
  \end{aligned}
  \,.
$$

Finally the [[local observables]] restricted to the infinitesimal neighbourhood is the module

$$
  LocObs_\Sigma(E,\varphi)
    \;\simeq\;
  \left(
     \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}} \langle dvol_\Sigma \rangle
  \right)/(im(d))
  \,.
$$


=--



+-- {: .num_defn #BVComplexOfOrdinaryLagrangianDensity}
###### Definition
**(local [[BV-complex]] of ordinary [[Lagrangian density]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}^\infty$ be a constant section of the shell (eqs:ConstantSectionOfTrivialShellBundle).

In correspondence with def. \ref{LocalObservablesOnInfinitesimalNeighbourhood}, write

$$
  \Gamma_{\Sigma,cp}(V_\Sigma J^\infty^\Sigma E,\varphi)
  \simeq
  \Gamma_{\Sigma,cp}(J^\infty^\Sigma V_\Sigma E,\varphi)
  \;\in\;
  \Omega^{0,0}_{\Sigma,cp}(E) Mod
$$

for the restriction of [[vertical vector fields]] on the [[jet bundle]] to the fiberwise [[infinitesimal neighbourhood]] 
(example \ref{InfinitesimalNeighbourhood}) of $\Sigma \times {\varphi}$.

Now we regard this as a _[[graded module]]_ over $\Omega^{0,0}_{\Sigma,cp}(E,\varphi)$ (eqs:FunctionsOnInfNbh) concentrated in degree $-1$:

$$
  \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma E,\varphi)[-1]
  \;\in\;
  \Omega^{0,0}_{\Sigma,cp}(E) Mod^{\mathbb{Z}}
  \,.
$$

This is called the module of _[[antifields]]_ corresponing the given [[type]] of [[field (physics)|fields]] encoded by $E$.

If the [[field bundle]] is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with field coordinates
$(\phi^a)$, then we write

$$
  \label{AntifieldCoordinates}
  \overline{\phi}_{a,\mu_1 \cdots \mu_l}
  \;\coloneqq\;
  \left(
     \partial_{(\phi^a_{\mu_1 \cdots \mu_l})}
  \right)[-1]
  \;\in\;
  \Gamma_{\Sigma,cp}(V_\Sigma J^\infty_\Sigma E,\varphi)[-1]
$$

for the vector field generator that takes derivatives along $\partial_{\phi^a_{,\mu_1 \cdots \mu_k}}$, but regarded now in degree -1.

Evaluation of vector fields in the
[[total spacetime derivatives]] $\frac{d^l}{d x^{\mu_1} \cdots d x^{\mu_l}} \delta\mathbf{L} \in \Omega^{p,0}_\Sigma(E) \wedge \delta \Omega^{0,0}_\Sigma(E)$ of the [[variational derivative]]  (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) yields a [[linear map]]
over $\Omega^{\bullet,\bullet}_{\Sigma,cp}(E,\varphi)$ (eqs:ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber)

$$
  \iota_{(-)}\delta_{EL} \mathbf{L}
   \;\colon\;
  \Gamma_{\Sigma,cp}( J^\infty_\Sigma V_\Sigma E,\varphi)[-1]
    \longrightarrow
  \Omega^{p+1,0}_{\Sigma,cp}(E,\varphi)
  \,.
$$

If we use the [[volume form]] $dvol_\Sigma$ on [[spacetime]] $\Sigma$ to induce an identification

$$
  \Omega^{p+1,0}_\Sigma(E) \;\simeq\; C^\infty(J^\infty_\Sigma(E))\langle dvol_\sigma\rangle
$$

with respect to which the [[Lagrangian density]] decomposes as

$$
  \mathbf{L} = L dvol_\Sigma
$$

then this is a $\Omega^{0,0}_\sigma(E,\varphi)$-[[linear map]] of the form

$$
  \iota_{(-)}{\delta L_{EL}}
    \;\colon\;
  \Gamma_{\Sigma,cp}^{ev}(V_\Sigma E,\varphi)[-1]
    \longrightarrow
  \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
  \,.
$$

In the special case that the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]]
(example \ref{TrivialVectorBundleAsAFieldBundle}) with [[field (physics)|field]] coordinates $(\phi^a)$
so that the Euler-Lagrange variational derivative has the coordinate expansion

$$
  \delta_L
  \;=\;
  \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a} \delta \phi^a
$$

then this map is given on the [[antifield]] basis elements (eqs:AntifieldCoordinates) by

$$
  \iota_{(-)} {\delta L_{EL}}
  \;\colon\;
  \overline{\phi}_{a,\mu_1 \cdots \mu_l}
    \;\mapsto\;
  \frac{d^l}{d x^{\mu_1} \cdots d x^{\mu_l}} \frac{\delta_{EL} L}{\delta \phi^a}
  \,.
$$

Consider then the [[symmetric algebra|graded symmetric algebra]]

$$
  C^\infty( J^\infty_\Sigma((V_\Sigma E)[-1] \times_\Sigma E, \varphi) )
  \;\coloneqq\;
  Sym_{\Omega^{0,0}_{\Sigma,cp}(E,\varphi)}\left(
    \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma E,\varphi)[-1]
  \right)
$$

which is generated over $\Omega^{0,0}_{\Sigma,cp}(E,\varphi)$ from the module of vector fields in degree -1.

If we think of a single vector field as a fiber-wise [[linear function]] on the [[cotangent bundle]],
and of a [[multivector field]] similarly as a [[multilinear function]] on the cotangent bundle, then we may
think of this as the algebra of functions on the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of $\varphi$
inside the [[graded manifold]] $(V_\Sigma E)[-1] \times_\Sigma E$.


Let now

$$
  \label{BVDifferentialForOrdinaryLagrangian}
  s_{BV}
  \;\colon\;
  C^\infty( J^\infty_\Sigma((V_\Sigma E)[-1] \times_\Sigma E, \varphi) )
    \;\longrightarrow\;
  C^\infty( J^\infty_\Sigma((V_\Sigma E)[-1] \times_\Sigma E, \varphi) )
$$

be the unique extension of the linear map $\iota_{(-)}{\delta_{EL} L}$ to an $\mathbb{R}$-linear [[derivation]] of degree +1 on this algebra.


The resulting [[differential graded-commutative algebra]] over $\mathbb{R}$

$$
  \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}_{BV}}
    \;\coloneqq\;
  \left(
  C^\infty( J^\infty_\Sigma((V_\Sigma E)[-1] \times_\Sigma E, \varphi) )
    \,,\,
    s_{BV}
  \right)
$$

we call the _[[local BRST cohomology|local]] [[BV-complex]]_ (an example of a [[Koszul complex]]) of the Lagrangian field theory
at the background solution $\varphi$.

There are canonical homomorphisms of [[dgc-algebras]], one from the
algebra of functions $\Omega^{0,0}_{\Sigma,cp}(E,\varphi)$ on the [[infinitesimal neighbourhood]]
of the background solution $\varphi$ (eqs:FunctionsOnInfinitesimalNeighbourhoodOfBackgroundSolution) support to the local BV-complex
and from there to the
local observables on the  neighbourhood of the background solution $\varphi$ (eqs:ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber), all considered
with compact spacetime support:

$$
  \label{ComparisonMorphismFromOrdinaryBVComplexToLocalObservables}
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
      \longrightarrow
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}_{BV}}
      \longrightarrow
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}}
$$

such that the composite is the canonical [[quotient]] [[coprojection]].

(...)


Similarly we obtain a factorization for the entire [[variational bicomplex]]:

$$
  \label{ComparisonMorphismFromOrdinaryBVComplexToLocalObservables}
    \Omega^{\bullet,\bullet}_\Sigma(E,\varphi)
      \longrightarrow
    \Omega^{\bullet,\bullet}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}
      \longrightarrow
    \Omega^{\bullet,\bullet}_\Sigma(E,\varphi)\vert_{\mathcal{E}}
    \,,
$$

where $\Omega^{\bullet,\bullet}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}$
is now triply graded, with three anti-commuting differentials $d$ $\delta$ and $s_{BV}$.

By construction this is now such that the local observables (def. \ref{LocalObservables})
are the [[cochain cohomology]] of this complex in horizontal form degree p+1, vertical degree 0
and BV-degree 0:

$$
  LocObs_\Sigma(E) \simeq \Omega^{p+1,0}_{\Sigma,cp}(E)/(im(s_{BV} + d))
  \,.
$$

=--








+-- {: .num_defn #States}
###### Definition
**([[states]])**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$, then a (classical) _[[state]]_ is a [[function]] from
the space $Obs_\Sigma$ of [[observables]] to the complex numbers

$$
  \langle -\rangle
  \;\colon\;
  Obs_\Sigma \longrightarrow \mathbb{C}
$$

such that

1. (linearity) this is a [[linear map]];

1. (positivity) for any $A \in Obs$ we have that $\langle A^\ast A \rangle \geq 0$

=--

(Below we consider _quantum states_. These are defined formally in just the same way, only that
now the algebra of observables is equipped with another product, which changes the meaning of
the product expression $A^\ast A$.)

$\,$

## Phase space
  {#PhaseSpace}

A remarkable aspect of [[Lagrangian field theory]] is that the [[de Rham differential]] of the [[local Lagrangian density]] $\mathbf{L}$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) decomposes into
_two_ kinds of [[variational differential forms]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

On the one hand the [[Euler-Lagrange variational derivative]]
$\delta_{EL}\mathbf{L} \in \Omega^{p+1,1}_\Sigma(E)$ appears. This being of horizontal degree $p+1$
its [[transgression of variational differential forms|transgression]] implies a [[differential 1-form]]
on the [[space of field histories]] over all of [[spacetime]]. We have seen that this is the derivative
of the [[action functional]] (def. \ref{ActionFunctional}) which embodies the _[[principle of extremal action]]_
(prop. \ref{PrincipleOfExtremalAction}) and with it a structure in full [[spacetime]] [[dimension]] $p+1$: the
[[on-shell]] [[space of field histories]] $\Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$ (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}).

But there is a second contribution: The [[presymplectic current]] $\Omega_{BFV} \in \Omega^{p,2}_{\Sigma}(E)$.
Since this is of horizontal degree $p$,
its [[transgression of variational differential forms|transgression]] implies a further structure on the [[space of field histories]]
of restricted to [[spacetime]] [[submanifolds]] of dimension $p$ (i.e. of spacetime "[[codimension]] 1").
There may be such submanifolds such that this restriction does not actually change the [[on-shell]] [[space of field histories]],
these are called the _[[Cauchy surfaces]]_ (def. \ref{CauchySurface} below).

Moreover,
we have seen that, via the [[Noether theorem]] (prop. \ref{NoethersFirstTheorem}) and the [[Hamiltonian Noether theorem]] (prop. \ref{HamiltonianDifferentialForms}),
the [[infinitesimal symmetries of the Lagrangian]] and of the [[presymplectic potential]]
induce special classes of [[variational differential forms]] that are also in  horizontal degree $p$:
the [[conserved currents]] (def. \ref{SymmetriesAndConservedCurrents}) and
the [[Hamiltonian differential form]] (def. \ref{HamiltonianForms}). By [[transgression of variational differential forms|transgression]]
this impplies that the corresponding [[Lie n-algebras|Lie (p+1)-algebras]] of local infinitesimal symmetries, namely the
[[Dickey bracket Lie algebra]] and the [[Poisson bracket Lie n-algebra|local Poisson bracket]] (prop. \ref{LocalPoissonBracket}),
induce [[Lie algebra]] structure on physical quantities in spacetime dimension $p$
called [[conserved charges]] (prop. \ref{ConservedCharge} below)
and _Hamiltonian local observables_ (def. \ref{HamiltonianLocalObservables} below), the actual _[[Poisson bracket]]_
(def. \ref{PoissonBracketOnHamiltonianLocalObservables} below).

This structure in spacetime codimension 1, i.e. the restriction of the [[on-shell]] [[space of field histories]]
to a [[Cauchy surface]] and equipped via [[transgression of variational differential forms|transgression]] with the induced [[presymplectic form]] and [[Poisson bracket]] on
Hamiltonian [[local observables]] is called the _[[phase space]]_ of the [[Lagrangian field theory]] (def. \ref{PhaseSpaceAssociatedWithCauchySurface} below),
or the _[[covariant phase space]]_, to amplify that it does not actually depend on the choice of
[[Cauchy surface]] (prop. \ref{CovariantPhaseSpace} below).




+-- {: .num_defn #CauchySurface}
###### Definition
**([[Cauchy surface]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), then a
_[[Cauchy surface]]_ is a [[submanifold]] $\Sigma_p \hookrightarrow \Sigma$ such that the
restriction map from the [[on-shell]] [[space of field histories]] $\Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}$
(eqs:OnShellFieldHistories) to the space (eqs:OnShellFieldHistoriesInHigherCodimension) of on-shell field histories
restricted to the [[infinitesimal neighbourhood]] of $\Sigma_p$ is an [[isomorphism]]:

$$
  \label{CauchySurfaceIsomorphismOnHistorySpace}
  \Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0 }
    \underoverset{\simeq}{(-)\vert_{N_\Sigma \Sigma_p}}{\longrightarrow}
  \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}
  \,.
$$

=--


+-- {: .num_defn #PhaseSpaceAssociatedWithCauchySurface}
###### Definition
**([[phase space]] associated with a [[Cauchy surface]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
and given a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{CauchySurface})
then the corresponding _[[phase space]]_ is

1. the [[smooth space]] $\Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}$ (eqs:OnShellFieldHistoriesInHigherCodimension)
   of [[on-shell]] field histories restricted to the [[infinitesimal neighbourhood]] of $\Sigma_p$;

1. equipped with the [[presymplectic form]]

   $$
     \label{TransgressionOfPresymplecticCurrentToCauchySurface}
     \omega_{\Sigma_p}
     \;\coloneqq\;
     \tau_{\Sigma_p}\left(\Omega_{BFV}\right)
     \;\in\;
     \Omega^2\left(
       \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}
     \right)
   $$

   which is the [[transgression of variational differential forms|transgression]]
   of the [[presymplectic current]] $\Omega_{BFV}$ (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).



=--

+-- {: .num_example #PresymplecticFormForFreeRealScalarField}
###### Example
**([[presymplectic form]] for [[free field|free]] [[real scalar field]])

Consider the [[Lagrangian field theory]] for the [[free field|free]] [[real scalar field]]
from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

Its [[space of field histories]] is simply the smooth space $C^\infty(\Sigma)$ of [[smooth functions]]
with [[real number|real]] values on [[Minkowski spacetime]]. This is naturally a [[vector space]].
Since the [[equation of motion]] is the [[Klein-Gordon equation]] $(\Box + m^2) \Phi = 0$
(example \ref{EquationOfMotionOfFreeRealScalarField}) which is a [[linear differential operator]],
also the [[on-shell]] [[space of field histories]] is still canonically a vector space.


The [[presymplectic form]] on the [[phase space]] (def. \ref{PhaseSpaceAssociatedWithCauchySurface})
associated with a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$
takes two [[smooth function]] $w_1,w_2 \in C^\infty(\Sigma)$, regarded as [[tangent vectors]] at zero to

$$
  \omega_{\Sigma_p}(w_1, w_2)
    \;=\;
    \int_{\Sigma_{p}}
    \left(
      (\partial_n w_1) w_2
      -
      w_1 \partial_n w_2
    \right)
    dvol_{\Sigma_{p}}
    \,,
$$

where $dvol_{\Sigma_p}$ is the [[volume form]] on the [[Cauchy surface]] which is induced from the
ambient metric on Minkowski spacetime, and $n \in N \Sigma_p$ denotes the [[normal bundle|normal vector field]]
of the embedding.

=--


+-- {: .proof}
###### Proof

By example \ref{FreeScalarFieldEOM} the
[[presymplectic current]] is

$$
  \Omega_{BFV}
  \;=\;
  \left(\eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
  \;\in\;
  \Omega^{p,2}_{\Sigma}(E)
  \,.
$$

Hence its [[transgression of variational differential forms|transgression]] is

$$
  \begin{aligned}
    \omega_{\Sigma_{p}}(w_1, w_2)
    & =
    \left(
    \int_{\Sigma_p}
      \left(
        \eta^{\mu \nu} \delta \partial_\mu \phi \wedge \delta \phi
      \right)
      \iota_{\partial_\nu} dvol_\Sigma
    \right)
    (w_1, w_2)
    \\
    & =
    \int_{\Sigma_{p}}
    \left(
      (\partial_n w_1) w_2
      -
      w_1 \partial_n w_2
    \right)
    dvol_{\Sigma_{p}}
  \end{aligned}
$$



=--

Since by definition of [[Cauchy surface]] (def. \ref{CauchySurface})
the underlying [[smooth space]] of the [[phase space]] associated with it (def. \ref{PhaseSpaceAssociatedWithCauchySurface})
is [[isomorphism|isomorphic]] to the [[on-shell]] [[space of field histories]], and hence also to the phase spaces
associated with any other Cauchy surface, a natural question is whether their [[presymplectic forms]]
are compatible with these isomorphisms, so that all phase spaces are in fact isomorphic as
[[presymplectic smooth spaces]]. The following proposition says that this is the case.
Therefore one speaks of the _[[covariant phase space]]_ of a [[Lagrangian field theory]]:

+-- {: .num_prop #CovariantPhaseSpace}
###### Proposition
**([[covariant phase space]])**

Consider $(E, \mathbf{L})$ a [[Lagrangian field theory]] on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Let

$$
  \Sigma_{tra} \overset{tra}{\hookrightarrow} \Sigma
$$

be a [[submanifold]] [[manifold with boundary|with two boundary components]]
$\partial \Sigma_{tra} = \Sigma_{in} \sqcup \Sigma_{out}$ ,
both of which are [[Cauchy surfaces]] (def. \ref{CauchySurface}).

Then the corresponding inclusion diagram

$$
  \array{
    && \Sigma_{tra}
    \\
    & {}^{\mathllap{in}}\nearrow && \nwarrow^{\mathrm{out}}
    \\
    \Sigma_{in}
    && &&
    \Sigma_{out}
  }
$$

induces a [[Lagrangian correspondence]] between the associated [[phase spaces]] (def. \ref{PhaseSpaceAssociatedWithCauchySurface})

$$
  \array{
    && \Gamma_{\Sigma_{tra}}(E)_{\delta_{EL} \mathbf{L} = 0}
    \\
    & {}^{\mathllap{ (-)\vert_{in} }}\swarrow && \searrow^{\mathrlap{ (-)\vert_{out} }}
    \\
    \Gamma_{\Sigma^{(in)}}(E)_{\delta_{EL}\mathbf{L}= 0}
    && &&
    \Gamma_{\Sigma^{(out)}}(E)_{\delta_{EL}\mathbf{L}= 0}
    \\
    & {}_{\mathllap{\omega_{in}}}\searrow && \swarrow_{\mathrlap{\omega_{out}}}
    \\
    && \mathbf{\Omega}^{2}
  }
$$

in that the [[pullback of differential forms|pullback]] of the
two [[presymplectic forms]] (eqs:TransgressionOfPresymplecticCurrentToCauchySurface) coincides on the
space of field histories:

$$
  \left( (-)\vert_{in}\right)^\ast\left( \omega_{in}\right)
  \;=\;
  \left( (-)\vert_{out} \right)^\ast \left( \omega_{out} \right)
  \phantom{AAAA}
  \in
  \Omega^2
  \left(
    \Gamma_{\Sigma_{tra}}(E)_{\delta_{EL} \mathbf{L} = 0}
  \right)
  \,.
$$

Hence there is a well defined [[presymplectic form]]

$$
  \omega \in \Omega^2\left(  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L}} = 0 \right)
$$

on the genuine [[space of field histories]], given by $\omega \coloneqq i^\ast \omega_{\Sigma_p}$
for any Cauchy surface $\Sigma_p \overset{i}{\hookrightarrow} \Sigma$. This [[presymplectic smooth space]]

$$
  \left(
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L}}
    \,,\,
    \omega
  \right)
$$

is therefore called the _[[covariant phase space]]_ of the [[Lagrangian field theory]] $(E,\mathbf{L})$.

=--


+-- {: .proof}
###### Proof

By prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell} the
total spacetime derivative $d \Omega_{BFV}$ of the [[presymplectic current]] vanishes [[on-shell]]:

$$
  d \Omega_{BFV} = - \delta \delta_{EL} \mathbf{L}
  \,.
$$

This means that the transgression of $d \Omega_{BFV}$ to $\Gamma_{\Sigma_{tra}}(E)_{\delta_{EL}\mathbf{L} = 0}$ vanishes.
But then the claim follows with prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}:

$$
  \begin{aligned}
    0
    & =   \tau_{\Sigma_{tra}}(d \Omega_{BFV})
    \\
    & = ((-)\vert_{\Sigma_{tra}})^\ast \tau_{\partial \Sigma_{tra}} \Omega_{BFV}
    \,.
  \end{aligned}
$$






=--


+-- {: .num_defn #HamiltonianLocalObservables}
###### Definition
**(Hamiltonian local observables)**

Let $(E, \mathbf{L})$ be a [[Lagrangian field theory]]  (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Consider a [[local observable]] (def. \ref{LocalObservables})

$$
  \tau_\Sigma(A)
    \;\colon\;
  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
    \longrightarrow
  \mathbb{C}
  \,,
$$

hence the [[transgression of variational differential forms|transgression]] of a variational horizontal
$p+1$-form $A \in \Omega^{p+1,0}_{\Sigma,cp}(E)$ of compact spacetime support.

Given a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{CauchySurface})
we say that $\tau_\Sigma (A)$ is _[[Hamiltonian]]_ if it is also the transgression of a
[[Hamiltonian differential form]] (def. \ref{HamiltonianForms}), hence if there exists

$$
  (H,v) \in \Omega^{p,0}_{\Sigma, Ham}(E)
$$

whose transgression over the Cauchy surface $\Sigma_p$ equals the transgression of $A$ over all of
spacetime $\Sigma$, under the isomorphism (eqs:CauchySurfaceIsomorphismOnHistorySpace)

$$
  \array{
    \Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0 }
      && \underoverset{\simeq}{(-)\vert_{N_\Sigma \Sigma_p}}{\longrightarrow} &&
    \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}
    \\
    & {}_{\mathllap{\tau_\Sigma}(A)}\searrow && \swarrow_{\mathrlap{ \tau_{\Sigma_p}(H) }}
    \\
    && \mathbf{\Omega}^2
  }
$$

=--

Beware that the [[local observable]] $\tau_{\Sigma_p}(H)$ defined by a [[Hamiltonian differential form]]
$H \in \Omega^{p,0}_{\Sigma,Ham}(E)$ as in def. \ref{HamiltonianLocalObservables}  does in general depend
not just on the choice of $H$, but also on the choice $\Sigma_p$ of the Cauchy surface.
The exception are those Hamiltonian forms which are _[[conserved currents]]_:


+-- {: .num_defn #ConservedCharge}
###### Proposition
**([[conserved charges]] -- [[transgression of variational differential forms|transgression]] of [[conserved currents]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If a [[Hamiltonian differential form]] $J \in \Omega^{p,0}_{\Sigma,Ham}(E)$ (def. \ref{HamiltonianForms}) happens to be a
[[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}) in that its [[total derivative|total spacetime derivative]]
vanishes [[on-shell]]

$$
  d J \vert_{\mathcal{E}} \;= \; 0
$$

then the induced Hamiltonian [[local observable]] $\tau_{\Sigma_p}(J)$ (def. \ref{HamiltonianLocalObservables})
is independent of the choice of [[Cauchy surface]] $\Sigma_p$ (def \ref{CauchySurface})
in that for $\Sigma_p, \Sigma'_p \hookrightarrow \Sigma$ any two Cauchy surfaces which are [[cobordism|cobordant]],
then

$$
  \tau_{\Sigma_p}(J) = \tau_{\Sigma'_p}(J)
  \,.
$$

The resulting [[constant function|constant]] is called the
_[[conserved charge]]_ of the conserved current, traditionally denoted

$$
  Q \;\coloneqq\; \tau_{\Sigma_p}(J)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition the [[transgression of variational differential forms|transgression]] of $d J$
vanishes on the [[on-shell]] [[space of field configurations]]. Therefore the result
is given by [[Stokes' theorem]].

=--


+-- {: .num_defn #PoissonBracketOnHamiltonianLocalObservables}
###### Definition
**([[Poisson bracket]] of Hamiltonian [[local observables]] on  [[covariant phase space]])**

The _[[Poisson bracket]]_ on Hamiltonian local observables (def. \ref{HamiltonianLocalObservables})
is the [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
of the [[Poisson bracket Lie n-algebra|Poisson bracket Lie (p+1)-algebra]] (def. \ref{LocalPoissonBracket})
of the corresponding [[Hamiltonian differential forms]] (def. \ref{LocalPoissonBracket})
to the [[covariant phase space]] (def. \ref{CovariantPhaseSpace}).

Explicitly: for $\Sigma_p \hookrightarrow \Sigma$ a choice of [[Cauchy surface]] (def. \ref{CauchySurface})
then the Poisson bracket between two local Hamiltonian observables
$\tau_{\Sigma_p}((H_i, v_i))$ is

$$
  \label{PoissonBracketTransgressedToCauchySurface}
  \left\{
    \tau_{\Sigma_p}((H_1, v_1))
    \,,\,
    \tau_{\Sigma_p}( (H_2, v_2) )
  \right\}
  \;\coloneqq\;
  \tau_{\Sigma_p}( \{ (H_1, v_1), (H_2, v_2) \} )
  \,,
$$

where on the right we have the transgression of the Poisson bracket of Hamiltonian forms
on the jet bundle.

=--

+-- {: .proof}
###### Proof

We need to see that equation (eqs:PoissonBracketTransgressedToCauchySurface) is well defined,
in that it does not depend on the choice of Hamiltonian form $(H_i, v_i)$
representing the local Hamiltonian observable $\tau_{\Sigma_p}(H_i)$.

It is clear that all the transgressions involved depend only on the restriction
of the Hamiltonian forms to the pullback of the jet bundle to $N_\Sigma \Sigma_p$.
Moreover the Poisson bracket on the jet bundle (eqs:LocalPoissonLieBracket)
respects this restriction.

Now after this restriction, a Hamiltonian form is in the [[kernel]] of the transgression
relative to $\Sigma_p$ precisely if it is horizontally exact. Therefore the claim
follows with the statement that horizontally exact forms constitute a
Lie ideal for the Poisson bracket on the jet bundle (lemma \ref{HorizontallyExactFormsDropOutOfLocalLieBracket}).

=--




+-- {: .num_example #PoissonBracketForRealScalarField}
###### Example
**([[Poisson bracket]] of the  [[real scalar field]] -- the [[Peierls bracket]])

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[scalar field]]
(example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}),
and consider the [[Cauchy surface]] defined by $x^0 = 0$.

By example \ref{LocalPoissonBracketForRealScalarField} the local Poisson bracket
of the [[Hamiltonian forms]]

$$
  Q \coloneqq \phi \iota_{\partial_0} dvol_\Sigma \in \Omega^{p,0}(E)
$$

and

$$
  P \coloneqq \eta^{\mu \nu} \phi_{,\mu} \iota_{\partial_\nu} dvol_{\Sigma} \in \Omega^{p,0}(E)
  \,.
$$

is

$$
  \{Q,P\} = \iota_{v_Q} \iota_{v_P} \omega = \iota_{\partial_0} dvol_\Sigma
  \,.
$$


Upon [[transgression of variational differential forms|transgression]] according to def. \ref{PoissonBracketOnHamiltonianLocalObservables}
 this yields the following [[Poisson bracket]]

$$
  \left\{
    \int_{\Sigma_p} b_1(\vec x) \phi(t,\vec x) \iota_{\partial_0} dvol_\Sigma(x)
    d^p \vec x
    \;,\;
    \int_{\Sigma_p} b_2(\vec x) \partial_0 \phi(t,\vec x) \iota_{\partial_0} dvol_\Sigma(\vec x)
  \right\}
  \;=\;
  \int_{\Sigma_p} b_1(\vec x) b_2(\vec x) \iota_{\partial_0} dvol_\Sigma(\vec x)
  d^p \vec x
  \,.
$$

where

$$
  \phi(x), \partial_0 \phi(x) : PhaseSpace(\Sigma_p^t) \to \mathbb{R}
$$

denote the point-evaluation functions ([[functionals]]), which act on a field configuration $\Phi \in \Gamma_\Sigma(E) = C^\infty(\Sigma)$ as

$$
 \phi(x)(\Phi) \coloneqq \Phi(x)
 \phantom{AAAAAAAA}
 \partial_0 \phi(x) (\Phi) \coloneqq \partial_0 \Phi(x)
 \,.
$$

Notice that these point-evaluation functions themselves do not arise
as the transgression of elements in $\Omega^{p,0}(E)$, only their smearings such as $\int_{\Sigma_p} b_1 \phi dvol_{\Sigma_p}$ do.
Nevertheless we may express the above Poisson bracket conveniently via the [[integral kernel]]

$$
  \label{PoissonBracketOfScalarFieldPointEvaluationOnMinkowskiSpacetime}
  \{\phi(t,\vec x), \phi(t,\vec y) \}
  =
  \delta(\vec x - \vec y)
  \,.
$$

This integral kernel is the _[[causal propagator]]_

$$
  \Delta
    \;\in\;
  \mathcal{D}'(\Sigma \times \Sigma)
$$

(also known as the _[[Pauli-Jordan distribution]]_ or _[[Peierls bracket]]_)
on Minkowski spacetime:

$$
  \begin{aligned}
    \{ \phi(x), \phi(y) \}
    & =
    \Delta(x,y)
    \\
    & \coloneqq
    -i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)}\left(
    e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)}
    -
    e^{+ i E(\vec k) (x-y)^0 + \vec k \cdot (\vec x - \vec y)}
  \right) d^p \vec k
    \\
    & =
   -i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) sgn( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
    \,.
  \end{aligned}
$$


=---

+-- {: .proof}
###### Proof


By [[Fourier transform]] the general solution to the [[Klein-Gordon equation]] (example \ref{EquationOfMotionOfFreeRealScalarField}) may be expressed in the form

$$
  \Phi(x)
    \;=\;
  (2\pi)^{-p} \int  Amp(k) e^{- i k_\mu x^\mu } \delta( k_\mu k^\mu + m^2 ) d^{p+1} k
  \,,
$$

where $Amp(k) \in \mathbb{C}$ is the _complex amplitude_ of the $k$th mode $(k \in \mathbb{R}^{p+1})$.

We may split this into the contributions with positive and those with negative [[energy]] $k_0$
by decomposing the integral over $k_0$ as

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(k_0, \vec k) e^{- i k_0 x^0 - i \vec k \cdot \vec x} \delta(- k_0^2 + \vec k + m^2) d^p \vec k \, d k_0
    \\
    & \phantom{=} +
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(-k_0, \vec k) e^{+ i k_0 x^0 - i \vec k \cdot \vec x} \delta(-k_0^2 + \vec k^2 + m^2) d^p \vec k \, d k_0
    \,.
  \end{aligned}
$$

By [[changing integration variables]] via $k_0 = +\sqrt{ h }$ this yields

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(\sqrt{h}, \vec k) e^{- i \sqrt{h} x^0 - i \vec k \cdot \vec x} \delta(- h + \vec k + m^2) d^p \vec k \, \frac{d h}{2\sqrt{h}}
    \\
    & \phantom{=} +
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(- \sqrt{h}, \vec k) e^{+ i \sqrt{h} x^0 - i \vec k \cdot \vec x} \delta(- h + \vec k^2 + m^2) d^p \vec k \, \frac{d h}{2 \sqrt{h}}
    \\
    & = \phantom{+}
    (2\pi)^{-p/2}
    \int Amp(E(\vec k), \vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x} d^p \vec k
    \\
    & \phantom{=} +
    (2\pi)^{-p/2}
    \int Amp(-E(\vec k), \vec k) e^{+ i E(\vec k) x^0 - i \vec k \cdot \vec x} d^p \vec k
  \end{aligned}
$$

where we defined the _on-shell [[energy]]_

$$
  E(\vec k) \coloneqq + \sqrt{ \vec k^2 + m^2 }
  \,.
$$

It is convenient to also change variables $\vec k \mapsto - \vec k$ in the second integral. This yields

$$
  \begin{aligned}
    \Phi(x)
    &= \phantom{+}
      (2\pi)^{-p/2}
      \int Amp(E(\vec k), \vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x} d^p \vec k
      \\
      & \phantom{=} +
      (-1)^p
      (2\pi)^{-p/2}
      \int Amp(-E(\vec k), \vec k) e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x} d^p \vec k
  \end{aligned}
    \,.
$$

Since $\Phi$ is real-valued, it follows that under [[complex conjugation]] $(-)^\ast$
the amplitudes are related by

$$
  Amp(E(\vec k), \vec k)^\ast = (-1)^p Amp(-E(\vec k), \vec k)
  \,.
$$

We abbreviate (cf. [Scharf 01 (1.1.18)](#Scharf01))

$$
  A(\vec k) \coloneqq E(\vec k) Amp(E(\vec k), \vec k)
  \,,
$$

where the prefactor just serves to make some of the following formulas come out conveniently.

With this the general solution to the Klein-Gordon equation is finally of the form

$$
  \label{FourierModeExpansionOfScalarFieldOnminkowskiSpacetime}
  \Phi(x)
  =
    (2\pi)^{-p/2}
    \int \frac{1}{\sqrt{2 E(\vec k)}}
      \left(
        A(\vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x}
        +
        A(\vec k)^\ast e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x}
      \right)
    d^p \vec k
    \,.
$$

and hence its time derivative is

$$
  \partial_0 \Phi(x)
  =
    (2\pi)^{-p/2}
    \int -i \sqrt{E(k)/2}
      \left(
        A(\vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x}
        -
        A(\vec k)^\ast e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x}
      \right)
    d^p \vec k
    \,.
$$

This allows to express the modes in terms of the value of the field and its time derivative at $t = 0$:

$$
  A(\vec k)
  =
   (2 \pi)^{-p/2}
   \int
     \left( \sqrt{E(k)/2}\Phi(0,\vec x) + i \frac{1}{2\sqrt{E(k)}} \partial_0 \Phi(0,\vec x)\right) \exp( i \vec k \cdot \vec x )
   d^p \vec x
   \,.
$$

As in example \ref{PoissonBracketForRealScalarField} we denote the corresponding evaluation functional

$$
  a(\vec k) \;\colon\; C^\infty(\Sigma) \longrightarrow \mathbb{C}
$$

by the corresponding lower case symbol:

$$
  a(\vec k)
   \;\coloneqq\;
   (2 \pi)^{-p/2}
   \int
     \left( \sqrt{E(k)/2}\phi(\vec x) + i \frac{1}{\sqrt{2 E(k)}} \partial_0 \phi(\vec x)\right) \exp( i \vec k \cdot \vec x )
   d^p \vec x
   \,.
$$

With the Poisson bracket kernel $\{\phi(\vec x), \phi(\vec y)\} = \delta(\vec x - \vec y)$ from example \ref{PoissonBracketForRealScalarField} (eqs:PoissonBracketOfScalarFieldPointEvaluationOnMinkowskiSpacetime),
it follow that the  (integral kernel for the) Poisson bracket of these mode functionals is
that of the [[canonical commutation relations]]:

$$
  \begin{aligned}
    \label{CanonicalPoissonCommutationOfModesOfFreeScalarFieldOnMinkowskiSpacetime}
    \{ a(\vec k_1), a(\vec k_2)^\ast  \}
    & =
    -i
    (2\pi)^{-p}
    \int \delta(\vec x_1 - \vec x_2) e^{i  ( \vec k_1 \cdot \vec x_1 - \vec k_2 \cdot \vec x_2) } d \vec x_1 d\vec x_2
    \\
    & =
    -i
    (2\pi)^{-p}
    \int e^{i (\vec k_1 - \vec k_2) \cdot \vec x } d \vec x
    & =
    \\
    & =  -i \delta(\vec k_1 - \vec k_2)
    \,,
  \end{aligned}
$$

where in the last step we used the [[Fourier transform]] representation of the [[delta distribution]] ([this prop.](Dirac+distribution#FourierTransform)).

In order to finally compute $\{\phi(x), \phi(y)\}$, it is convenient to break this up into two contributions:
Write

$$
  \phi^{(+)}(x)
  \;\coloneqq\;
    (2\pi)^{-p/2}
    \int \frac{1}{\sqrt{2 E(\vec k)}}
        a(\vec k)^\ast e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x}
    d^p \vec k
  \phantom{AAAA}
  \phi^{(-)}(x)
  \;\coloneqq\;
    (2\pi)^{-p/2}
    \int \frac{1}{\sqrt{2 E(\vec k)}}
        a(\vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x}
    d^p \vec k
$$

for the positive and negative energy contributions from the Fourier expansion in (eqs:FourierModeExpansionOfScalarFieldOnminkowskiSpacetime), so that

$$
  \phi(x) = \phi^{(-)}(x)  + \phi^{(+)}(x)
  \,.
$$

Using the [[canonical commutation relation]] of the mode functions (eqs:CanonicalPoissonCommutationOfModesOfFreeScalarFieldOnMinkowskiSpacetime), we find

$$
  \label{2PointFunctionFreeScalarFieldOnMinkowski}
  \begin{aligned}
    -i \omega(x,y)
     & \coloneqq
     \{ \phi^{(-)}(x), \phi^{(+)}(y) \}
    \\
    &=
    -i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
    \\
    & =
    -i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) \Theta( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
    \,,
  \end{aligned}
$$

where in the last line we again applied [[change of integration variables]].
This $\omega$ is known as the _[[2-point function]]_ or _[[Hadamard propagator]]_ on Minkowski spacetime.
Similarly

$$
  \begin{aligned}
  \{ \phi^{(+)}(x), \phi^{(-)}(y) \}
  & =
  + i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{i E(\vec k) (x-y)^0 + \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
  \\
  & =
  + i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) \Theta( -k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
  \\
  \end{aligned}
  \,.
$$

In particular this says that

$$
  \{ \phi^{(+)}(x), \phi^{(-)}(y) \}
  =
  - \omega(y,x)
  \coloneqq
  -
  \{ \phi^{(-)}(y), \phi^{(+)}(x) \}
  \,.
$$


With this we finally obtain the expression for the [[causal propagator]] as the skew-symmetrization
of the [[2-point function]]:

$$
  \begin{aligned}
  \{
    \phi(x),
    \phi(y)
  \}
  & =
  \{ \phi^{(-)}(x), \phi^{(+)}(y) \}
  +
  \{\phi^{(+)}(x), \phi^{(-)}(y)\}
  \\
  & =
  \omega(x,y) - \omega(y,x)
  \\
  & =
  -i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)}\left(
    e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)}
    -
    e^{+ i E(\vec k) (x-y)^0 + \vec k \cdot (\vec x - \vec y)}
  \right) d^p \vec k
  \\
  & =
  -i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) sgn( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
 \,.
  \end{aligned}
$$

=--


So far we have discussed the [[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) in terms of
explicit restriction to the [[shell]].  We now turn to the more flexible perspective where
a [[homological resolution]] of the [[shell]] in terms of  "[[antifields]]" is used (def. \ref{BVComplexOfOrdinaryLagrangianDensity}).

+-- {: .num_example #BVPresymplecticCurrent}
###### Example
**(BV-presymplectic current)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eqs:ConstantSectionOfTrivialShellBundle).

Then in the BV-variational bicomplex (eqs:ComparisonMorphismFromOrdinaryBVComplexToLocalObservables)
there exists the _BV-presymplectic current_

$$
  \Omega_{BV} \coloneqq \delta \overline{\phi}_a \wedge \delta \phi^a \wedge dvol_{\Sigma}
  \;\;\;
  \in \Omega^{p,2}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}
  \,,
$$

where $(\phi^a)$ are the given [[field (physics)|field]]
[[coordinates]], $\overline{\phi}_a$ the corresponding [[antifield]] coordinates (eqs:AntifieldCoordinates)
and $\frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}$ the corresponding components of the [[Euler-Lagrange form]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).


=--

+-- {: .num_example #}
###### Example
**(derived [[presymplectic current]] of [[real scalar field]])

Consider a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
without any non-trivial implicial [[infinitesimal gauge transformations]] (def. \ref{ImplicitInfinitesimalGaugeSymmetry});
for instance the [[real scalar field]] (def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}).

Inside its [[variational BV-bicomplex]] (def. \ref{BVVariationalBicmplex}) we may form the linear combination of

1. the [[presymplectic current]] $\Omega_{BFV}$ (example \ref{FreeScalarFieldEOM})

1. the BF-presymplectic current $\Omega_{BV}$ (example \ref{BVPresymplecticCurrent}).

This yields a vertical 2-form

$$
  \Omega \;\coloneqq\; \Omega_{BV} + \Omega_{BFV} \;\; \in \Omega^{p,2}_\Sigma(E)\vert_{\mathcal{E}_{BV}}
$$

which is closed under the BV-horizontal derivative $d - s$:

$$
  \begin{aligned}
    (d - s) (\Omega_{BV} + \Omega_{BFV})
    & =
    \underset{= 0}{\underbrace{d \Omega_{BFV} - s \Omega_{BV}}} + d \Omega_{BV} - s \Omega_{BFV}
    \\
    & = 0
  \end{aligned}
$$

Here the first term vanishes via the local BV-BFV relation (prop. \ref{ResolutionOfCovariantPhaseSpaceCorrespondence})
while the other two terms vanish simply by degree reasons.

=--


+-- {: .num_prop #ResolutionOfCovariantPhaseSpaceCorrespondence}
###### Proposition
**(local BV-BFV relation)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eqs:ConstantSectionOfTrivialShellBundle).

Then the BV-presymplectic current $\Omega_{BV}$ (def. \ref{BVPresymplecticCurrent})
witnesses the [[on-shell]] vanishing (prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}) of the [[total derivative|total spacetime derivative]] of the genuine [[presymplectic current]] $\Omega_{BFV}$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) in that the [[total derivative|total spacetime derivative]]
of $\Omega_{BFV}$ equals the BV-differential $s_{BV}$  of $\Omega_{BV}$:

$$
  d \Omega_{BFV} = s \Omega_{BV}
  \,.
$$

Hence if $\Sigma_{tra} \hookrightarrow \Sigma$ is a [[submanifold]] of [[spacetime]] of full dimension $p+1$
[[manifold with boundary|with boundary]] $\partial \Sigma_{tra} = \Sigma_{in} \sqcup \Sigma_{out}$

$$
  \array{
    && \Sigma_{tra}
    \\
    & {}^{\mathllap{in}}\nearrow && \nwarrow^{\mathrm{out}}
    \\
    \Sigma_{in}
    && &&
    \Sigma_{out}
  }
$$

then the [[pullback of differential forms|pullback]] of the
two [[presymplectic forms]] (eqs:TransgressionOfPresymplecticCurrentToCauchySurface)
on the incoming and outgoing [[spaces of field histories]], respectively, differ by the
BV-differential of the transgression of the BV-presymplectic current:

$$
  \left( (-)\vert_{in}\right)^\ast\left( \omega_{in}\right)
  \;-\;
  \left( (-)\vert_{out} \right)^\ast \left( \omega_{out} \right)
  =
  \tau_{\mathbb{D} \times \Sigma_{tra}} ( s \Omega_{BV} )
  \phantom{AAAA}
  \in
  \Omega^2
  \left(
    \Gamma_{\Sigma_{tra}}(E)_{\delta_{EL} \mathbf{L} = 0}
  \right)
  \,.
$$

This [[homological resolution]] of the [[Lagrangian correspondence]] that exhibits the "covariance" of the
[[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) is known as the _BV-BFV relation_
([Cattaneo-Mnev-Reshetikhin 12 (9)](BV-BRST+formalism#CattaneoMnevReshetikhin12)).

=--


+-- {: .proof}
###### Proof

For the first statement we compute as follows:

$$
  \begin{aligned}
   s \Omega_{BV}
    & =
  - \delta (s \overline{\phi}_a) \delta \phi^a \wege dvol_{\Sigma}
  \\
    & =
  - \delta \frac{\delta_{EL}L }{\delta \phi^a}  \delta \phi^a dvol_{\Sigma}
  & =
  - \delta \delta_{EL}\mathbf{L}
  \\
  & =
  d \Omega_{BFV}
  \,,
  \end{aligned}
$$

where the first steps simply unwind the definitions, and where the last step is prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}.

With this the second statement follows by immediate generalization of
the proof of prop. \ref{CovariantPhaseSpace}.

=--


$\,$


## Gauge symmetries
 {#GaugeSymmetries}

The existence of the [[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) of a [[Lagrangian field theory]]
requires the existence of [[Cauchy surfaces]] (def. \ref{CauchySurface}) for its [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]. In general these may not exist. An [[obstruction]] to their existence turns out to be (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} below)
the presence of [[infinitesimal symmetries of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
that have compact spacetime support (def. \ref{SpacetimeSupport}).

This obstruction is neatly
captured by the [[cochain cohomology]] of a [[cochain complex]] which is induced by the [[equations of motion]],
called the _local [[BV-complex]]_ (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) of the Lagrangian theory.
This may be understood as the [[algebra of functions]] on an extension of the [[jet bundle]] from a
(locally pro-finite dimensional, prop. \ref{InfinitesimalActionByLieAlgebra}) [[smooth manifold]] to
a [[differential graded manifold]].
This appearance of [[homotopy theory]] in the guise of [[homological algebra]] in Lagrangian field theory
paves the way to understanding the cause of the obstruction: It disappears when the
[[field bundle]] (or more generally its [[jet bundle]]) is promoted to its _infinitesimal [[homotopy quotient]]_
by the [[action]] of these compactly supported symmetries (the "[[action Lie algebroid]]", def. \ref{ActionLieAlgebroid} below).

Passing to this homotopy quotient
means to hard-wire into the geometry of the  types of [[field (physics)|field]] their _[[equivalence]]_ under these symmetries: in physics this is called _[[gauge equivalence]]_.  The result is called the "[[reduced phase space]]", which we turn to further [below](#ReducedPhaseSpace).

Therefore the presence of [[infinitesimal symmetries of the Lagrangian]] with compact spacetime support is a defect of the theory
which however implies its own solution, by indicating which [[relations]] ought to be promoted
to "[[gauge equivalences|gauge]]" [[equivalences]]. Therefore we call these the _implicit [[infinitesimal gauge symmetries]]_
(remark \ref{ImplicitGaugeTransformationTerminology} below).

An obvious candidate class of such implicit infinitesimal gauge transformations are
[[infinitesimal symmetries of the Lagrangian]] which appear
linearly _parameterized_  by arbitrary [[sections]] (and their [[derivatives]]) of some [[vector bundle]] on [[spacetime]]:
Because then for every such section of [[compact support]] the corresponding symmetry will have
compact spacetime support and hence be an implicit gauge symmetry. Therefore such sections are
called _[[gauge parameters]]_ (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} below). In applications typically all implicit [[infinitesimal gauge transformations]]
come from [[gauge parameters]] this way, notably so for the theory of [[electromagnetism]] (example \ref{InfinitesimalGaugeSymmetryElectromagnetism}) and more generally [[Yang-Mills theory]].


$\,$


+-- {: .num_defn #ImplicitInfinitesimalGaugeSymmetry}
###### Definition
**(implicit [[infinitesimal gauge symmetry]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}),
then an _implicit [[infinitesimal gauge symmetry]]_ is an [[infinitesimal symmetry of the Lagrangian]]
(def. \ref{SymmetriesAndConservedCurrents}) with compact spacetime support  (def. \ref{SpacetimeSupport}).

=--


There always exist "trivial" implicit infinitesimal gauge transformations:

+-- {: .num_example #TrivialImplicialInfinitesimalGaugeTransformations}
###### Example
**(trivial implicit [[infinitesimal gauge symmetries]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then every [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField}) of the special form

$$
  \epsilon
    \coloneqq
  \frac{\delta L }{\delta \phi^a} \kappa^{[a b]} \partial_{\phi^a}
  \;\in\;
  \Gamma_E^{ev}( V_\Sigma E )
$$

for a collection of smooth functions with compact spacetimes support

$$
  (\kappa^{[a b]} \in \Omega^{0,0}_\Sigma(E))
  \;\;\;\;
  \in \Omega^{0,0}_{\Sigma,cp}(E)
$$

which is skew-symmetric in its indices ($\kappa^{[a b]} = - \kappa^{[b a]}$) is an
implicit infinitesimal gauge symmetry (def. \ref{ImplicitInfinitesimalGaugeSymmetry}).

This is so for a "trivial reason" namely just that skew symmetry:

$$
  \iota_\epsilon \delta_{EL} \mathbf{L}
  =
  \underset{= 0}{
  \underbrace{
   \left( \frac{\delta L }{\delta \phi^a} \right)
   \left( \frac{\delta L }{\delta \phi^b} \right)
   \kappa^{[a b]}
  }
  }
  \,
  dvol_\Sigma
$$

These are called the _trivial infinitesimal gauge transformation_.

Moreover, by prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} the [[action]] of
these implicit infinitesimal gauge symmetries  $\epsilon$ vanishes [[on-shell]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
up to a [[total derivative|total horizontal derivative]] and hence indeed
act trivially on on-shell local observables.


=--



+-- {: .num_remark #ImplicitGaugeTransformationTerminology}
###### Remark
**(terminology)**

The literature on the [[variational bicomplex]] knows a more refined concept
of infinitesimal gauge transformations than the "implicit" infinitesimal gauge transformations of
def. \ref{ImplicitInfinitesimalGaugeSymmetry}, namely in terms of [[differential operators]]
taking values in infinitesimal symmetries of the Lagrangian.
But for the purpose of constructing the [[covariant phase space]] of a [[gauge theory]],
def. \ref{ImplicitInfinitesimalGaugeSymmetry} is what needs to be considered (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} below).

We do say "implicit" here to distinguish from their "explicit" incarnations
[[action Lie algebroid|acting]] on [[field (physics)|fields]]:
the morphisms in the [[action Lie algebroid]] whose [[Chevalley-Eilenberg algebra]]
is the _[[BRST complex]]_ ([below](#ReducedPhaseSpace)).

Since the point of quantization of [[gauge field theory]] via [[causal perturbation theory]]
is that it does _not apply_ as long as there are non-trivial implicit infinitesimal gauge symmetries
present (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} below),
but only applies once all implicit infinitesimal
gauge symmetries have been made explicit (by the [[BV-BRST complex]]) the distinction is important.

=--



+-- {: .num_prop #NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces}
###### Proposition
**(non-trivial implicit [[infinitesimal gauge symmetries]] [[obstruction|obstruct]] existence of [[Cauchy surfaces]])

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]].

If there exists a single implicit infinitesimal gauge transformation $\epsilon$ (def. \ref{ImplicitInfinitesimalGaugeSymmetry})
that does not vanish [[on-shell]] (not a trivial one, example \ref{TrivialImplicialInfinitesimalGaugeTransformations})
then there does not exist any [[Cauchy surface]] (def. \ref{CauchySurface}) for the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) outside of $supp_\Sigma(v)$.

=--

+-- {: .proof}
###### Proof


By prop. \ref{FlowAlongImplicitInfinitesimalGaugeSymmetryPreservesOnShellSpaceofFieldHistories}
the flow along $\hat \epsilon$ preserves the on-shell space of field histories.

But if $\hat \epsilon$ is non-trivial, in that it does not vanish on-shell,
then the flow along $\epsilon$ continuously changes solutions away from the would-be Cauchy surface.
This means that there are infinitely many solutions to the equations of motion that restrict to the
same solution on the would-be Cauchy surface, which contradicts the defining property of an
actual Cauchy surface.

=--


After these generalities on implicit [[infinitesimal gauge symmetries]] we turn attention to a more
structured special class of them. To that end, recall that an [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField})
is a bundle homomorphism of the form

$$
  \array{
    J^\infty_\Sigma(E)
    && \overset{v}{\longrightarrow} &&
    V_\Sigma E
    \\
    & {}_{\mathllap{jb_{\infty,0}}}\searrow && \swarrow_{\mathllap{}}
    \\
    && E
  }
$$

and that this is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}) if $\iota_v \delta_{EL}\mathbf{L}$ is horizontally exact.

We now parameterize such morphisms by another bundle:

+-- {: .num_defn #GaugeParametrizedInfinitesimalGaugeTransformation}
###### Definition
**(irreducible closed [[gauge parameters]])

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then a collection of _irreducible closed [[gauge parameters]]_ for $(E,\mathbf{L})$ is

1. a [[vector bundle]] $\mathcal{G} \overset{gb}{\longrightarrow} \Sigma$ over [[spacetime]] $\Sigma$;
   the [[sections]] $\epsilon$ of which are to be called the _[[gauge parameters]]_;

1. a [[bundle morphism]] $R$ from the
   [[jet bundle]] of the  [[fiber product]] $\mathcal{G} \times_\Sigma E$ with the [[field bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
   to the [[vertical tangent bundle]] of $E$:

   $$
     \array{
       J^\infty_\Sigma( \mathcal{G} \times_\Sigma E )
         && \overset{R}{\longrightarrow} &&
       V_\Sigma E
         & \overset{i}{\hookrightarrow} &
       V_\Sigma (\mathcal{G} \times_\Sigma E)
       \\
       & \searrow && \swarrow
       \\
       && E
     }
   $$

such that

1. $R$ is [[linear map|linear]] in the first argument;

1. $i \circ R$ is an [[evolutionary vector field]] on $\mathcal{G} \times_\Sigma E$ (def. \ref{EvolutionaryVectorField});

1. $R(e,-)$ is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
   for every point in $e \in J^\infty_\Sigma(\mathcal{G})$ (i.e. for every jet of a gauge parameter);

1. $\mathcal{G}$ is closed under the [[Lie bracket]] of [[evolutionary vector fields]] (prop. \ref{EvolutionaryVectorFieldLieAlgebra})
   in that for $e_1, e_2$ two points in the same fiber of $J^\infty_\Sigma(E)$ then there
   exists a unique $[e_1,e_2] \in J^\infty_\Sigma(E)$ in that fiber such that

   $$
     \left[\widehat R(e_1,-), \widehat R(e_1,-)\right] = \widehat R([e_1, e_2],-)
     \,.
   $$

   We call this the corresponding  _irreducible closed gauge Lie algebra_ of the Lagrangian theory (if it exists).


In components this means that, if the [[field bundle]] $E$ is a [[trivial vector bundle]] with [[field (physics)|field]] [[fiber]] coordinates
$(\phi^a)$ (example \ref{TrivialVectorBundleAsAFieldBundle})
and also $\mathcal{G}$ happens to be a [[trivial vector bundle]]

$$
  \mathcal{G} = \Sigma \times \mathfrak{g}
$$

so that $R$ is a bundle morphism of the form

$$
  R \;\colon\; J^\infty_\Sigma(\mathfrak{g} \times E ) \longrightarrow V_\Sigma E
$$

then for $\epsilon \in \Gamma_{\Sigma}(\mathcal{G}) = C^\infty(\Sigma,\mathcal{g})$ a [[gauge parameter]], $v_\epsilon$ is of the form

$$
  \label{CoordinateExpressionForGaugeParameterized}
  v_\epsilon
    \;=\;
  \left(
    \epsilon^\alpha R^a_\alpha
    +
    \frac{d \epsilon^\alpha}{d x^\mu} R^{a \mu}_\alpha
    +
    \frac{d^2 \epsilon^\alpha}{d x^{\mu_1} d x^{\mu_2}} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \partial_{\phi^a}
  \,,
$$

where the $R^{a \mu_1 \cdots \mu_k}_\alpha$ are smooth functions on the jet bundle of $E$,
locally of finite order (prop. \ref{JetBundleIsLocallyProManifold}).

=--



+-- {: .num_prop #NoetherIdentities}
###### Proposition
**([[Noether identities]])

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

A [[gauge parameter|gauge parameterized]] [[evolutionary vector field]] (eqs:CoordinateExpressionForGaugeParameterized)

$$
  v_\epsilon
  \;=\;
  \left(
    \epsilon^\alpha R^a_\alpha
    +
    \frac{d \epsilon^\alpha}{d x^\mu} R^{a \mu}_\alpha
    +
    \frac{d^2 \epsilon^\alpha}{d x^{\mu_1} d x^{\mu_2}} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \partial_{\phi^a}
$$

is a [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge transformation]]
(def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) precisely if the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
satisfies the following relation:

$$
  \left(
    R^{a}_\alpha \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    -
    R^{a \mu}_\alpha \frac{d}{d x^\mu} \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    +
    R^{a \mu_1 \mu_2}_\alpha \frac{d^2}{d x^{\mu_1} d x^{\mu_2}} \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    -
    \cdots
  \right)
  \;=\;
  0
  \,.
$$

These are called _[[Noether identities]]_ of the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] (def \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}).

=--

+-- {: .proof}
###### Proof

We need to show that $v_\epsilon$ is a gauge symmetry as claimed precisely if

$$
  \iota_{v_\epsilon} \delta_{EL}\mathbf{L} = d(\cdots)
$$

vanishes for all choices of $\epsilon$ up to a horizontally exact term. From (eqs:CoordinateExpressionForGaugeParameterized) this
means that

$$
  \begin{aligned}
    \iota_{v_\epsilon} \delta_{EL} \mathbf{L}
    & =
    \underset{k \in \mathbb{N}}{\sum}
      \frac{d^k \epsilon^\alpha}{d x^{\mu_1} \cdot d x^{\mu_k}} R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
    \\
    & =
    \epsilon^\alpha
    \underset{k \in \mathbb{N}}{\sum}
      (-1)^k  R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
    +
    d J_{v_\epsilon}
  \end{aligned}
$$


=--


+-- {: .num_example #InfinitesimalGaugeSymmetryElectromagnetism}
###### Example
**(implicit [[infinitesimal gauge symmetry]] of [[electromagnetism]])

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]]
on [[Minkowski spacetime]] $\Sigma$ from example \ref{ElectromagnetismLagrangianDensity}.

Let $\mathcal{G} \coloneqq \Sigma \times \mathbb{R}$ be the [[trivial line bundle]], regarded as a
[[gauge parameter]] bundle (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}).
Then the [[gauge parameter|gauge parametrized]] [[evolutionary vector field]] (eqs:CoordinateExpressionForGaugeParameterized) given on a gauge parameter

$$
  \epsilon \in \Gamma_\Sigma(\mathcal{G}) = C^\infty(\Sigma)
$$

by

$$
  \label{EMImplicitGaugeSymmetry}
  v_\epsilon \coloneqq \frac{d \epsilon}{d x^\mu} \partial_{a_\mu}
$$

is a gauge paramterized implicit [[infinitesimal gauge transformation]] according to
def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}.

This is because the [[Euler-Lagrange form]]

$$
  \delta_{EL}\mathbf{L}
  \;=\;
  \frac{d}{d x^\mu }f^{\mu \nu} \delta_{a_\nu} dvol_\Sigma
$$

of the theory (example \ref{ElectromagnetismEl}),
corresponding to the [[vacuum]] [[Maxwell equations]] (example \ref{MaxwellVacuumEquation}),
satisfies the following evident [[Noether identity]] (prop. \ref{NoetherIdentities}):

$$
  \frac{d}{d x^\mu} \frac{d}{d x^\nu} f^{\mu \nu} = 0
  \,.
$$

This is simply because $f^{\mu \nu} = -f^{\nu \mu}$ is skew-symmetric by definition (eqs:FaradayTensorJet),
while [[partial derivatives]] commute with each other.

This is the archetypical _[[infinitesimal gauge symmetry]]_ that gives [[gauge theory]] its name.

The prolongation (prop. \ref{EvolutionaryVectorFieldProlongation}) of the vector field $v_\epsilon$ (eqs:EMImplicitGaugeSymmetry)
is

$$
  \label{EMProlongedSymmetryVectorField}
  \hat v_\epsilon
    \;=\;
  \frac{d \epsilon}{d x^\mu} \partial_{a_\mu}
  +
  \frac{d^2 \epsilon}{d x^\mu d x^\nu} \partial_{a_{\mu,\nu}}
  +
  \frac{d^3 \epsilon}{d x^\mu d x^{\nu_1} d x^{\nu_2}} \partial_{a_{\mu, \nu_1 \nu_2}}
  +
  \cdots
$$

This shows that the [[Lagrangian density]] of free electromagnetism is in fact strictly
gauge invariant (not just up to a horizontally exact piece)

$$
  \mathcal{L}_{\hat v_\epsilon} \mathbf{L}_{EM} = 0
$$

as is its [[Euler-Lagrange form]]

$$
  \mathcal{L}_{\hat v_{\epsilon}} \delta_{EL}\mathbf{L} = 0
  \,.
$$


=--









Making the _implicit_ [[infinitesimal gauge symmetries]] _explicit_ means
to make explicit how they _[[action|act]]_ on the fields. To this end consider
the general concept of an [[action]] of a [[Lie algebra]] by [[infinitesimal]] [[diffeomorphisms]]:


+-- {: .num_defn #InfinitesimalActionByLieAlgebra}
###### Definition
**([[action]] of [[Lie algebra]] by [[infinitesimal]] [[diffeomorphism]])

Let $X$ be a [[smooth manifold]] or more generally a [[locally pro-manifold]] (prop. \ref{JetBundleIsLocallyProManifold}), and let $\mathfrak{g}$ be a [[Lie algebra]].

An _[[action]]_ of $\mathfrak{g}$ on $X$ by
[[infinitesimal]] [[diffeomorphisms]], is a [[homomorphism]]
of Lie algebras

$$
  \rho \;\colon \mathfrak{g} \longrightarrow ( Vect(X), [-,-] )
$$

to the smooth [[vector fields]] on $X$.

Equivalently -- to bring out the relation to
the [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge transformations]] in def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} -- this is a $\mathfrak{g}$-parameterized [[section]]

$$
  \array{
     \mathfrak{g} \times X && \overset{\rho}{\longrightarrow} && T X
     \\
     & {\mathllap{pr_2}}\searrow && \swarrow_{\mathrlap{p}}
     \\
     && X
  }
$$

of the [[tangent bundle]], such that for all pairs of points $e_1, e_2$ in $\mathfrak{g}$
we have

$$
  \left[\rho(e_1,-), \rho(e_2,-)\right] = \rho([e_1,e_2],-)
$$

(with the [[Lie bracket]] of [[vector fields]] on the left).

=--

+-- {: .num_example #ActionOfGaugeParameterizedInfinitesimalGaugeSymmetriesOnJetBundle}
###### Example
**([[action]] of irreducible closed [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge symmetries]] on [[field (physics)|fields]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), and let
$\mathcal{G} =  \overset{gb}{\to} \Sigma$ be a bundle of irreducible closed [[gauge parameters]]
for the theory (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with
bundle morphism

$$
  \array{
    J^\infty_\Sigma( \mathcal{G} \times_\Sigma E )
    && \overset{R}{\longrightarrow} &&
    V_\Sigma E
    \\
    & \searrow && \swarrow
    \\
    && E
  }
$$

exhibiting the corresponding parameterized implicit [[infinitesimal gauge symmetries]].

By passing from these [[evolutionary vector fields]] $R(e)$ (def. \ref{EvolutionaryVectorField})
to their prolongations $\widehat{R(e)}$ to actual vector fields on the jet bundle (prop. \ref{EvolutionaryVectorFieldProlongation})
we obtain a bundle morphism of the form

$$
  \array{
    J^\infty_\Sigma(\mathcal{G}) \times_\Sigma J^\infty_\Sigma E
     && \overset{\widehat{R(e)}}{\longrightarrow} &&
    V_\Sigma J^\infty_\Sigma(E)
    \\
    & \searrow && \swarrow
    \\
    && J^\infty_\Sigma(E)
  }
  \,.
$$

In the case that $\mathcal{G} = \mathfrak{g} \times \Sigma$ is a [[trivial vector bundle]], with [[fiber]] $\mathfrak{g}$, then so is its [[jet bundle]] $J^\infty_\Sigma(\mathfrak{g} \times \Sigma) = \mathfrak{g}^\infty \times \Sigma$, and so in this case the above becomes of the form

$$
  \array{
    \mathfrak{g}^\infty \times J^\infty_\Sigma E
     && \overset{\widehat{R(e)}}{\longrightarrow} &&
    V_\Sigma J^\infty_\Sigma(E)
    \\
    & \searrow && \swarrow
    \\
    && J^\infty_\Sigma(E)
  }
  \,.
$$

By def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} and def. \ref{InfinitesimalActionByLieAlgebra}
this now exhibits an [[action]]

$$
  \widehat{\rho}
  \;\colon\;
  \mathfrak{g}^\infty \longrightarrow \Gamma_{J^\infty_\Sigma(E)}\left( T(J^\infty_\Sigma(E)) \right)
$$

of a [[Lie algebra]] $\mathfrak{g}^\infty$ on the [[jet bundle]]
of the [[field bundle]] by [[infinitesimal]] [[diffeomorphisms]].

=--

We have seen that the presence of non-trivial _implicit_ [[infinitesimal gauge transformations]]
(def. \ref{ImplicitInfinitesimalGaugeSymmetry}) in a [[Lagrangian field theory]] [[obstruction|obstructs]] the existence of the [[covariant phase space]] of the theory (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces}). But these
implicit infinitesimal gauge symmetries become _explicit_ by hard-wiring into the very [[geometry]] of the types of [[field (physics)|fields]] their _[[equivalence]]_ under these symmetries: In physics this is called _[[gauge equivalence]]_.

Mathematically this means to pass to the infinitesimal [[homotopy quotient]] of the [[action]] of the gauge symmetries on the [[shell]],
represented by the [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid} below).
This is called the _local [[reduced phase space]]_ of the theory.
Such "[[schreiber:Higher Structures|higher structures]]" exist in the
unification of [[differential geometry]] with [[homotopy theory]] called _[[higher differential geometry]]_.
The ("[[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]]"-)[[algebra of functions]] on this "field bundle with infinitesimal gauge symmetries made explicit" is called the _[[BRST complex]]_.
In this [[cochain complex]] the formerly _implicit_ [[infinitesimal gauge symmetries]] appear _explicitly_ in the guise of [[field (physics)|field]] variables of positive (i.e. "higher") degree in a [[differential graded-commutative algebra]]. These are called _[[ghost fields]]_.


$\,$


+-- {: .num_defn #LInfinityAlgebroid}
###### Definition
**([[Lie algebroid]])**

Let $X$ be an [[infinitesimally thickened point]] and write $C^\infty(X)$ for its [[algebra of functions]].
Then  a _connected [[Lie ∞-algebroid]]_ $\mathfrak{a}$ over $X$ of [[finite type]] is a

1. a sequence $(\mathfrak{a}_k)_{ k = 1 }^\infty$ of [[free modules]] of [[finite number|finite]] [[rank]] over $C^\infty(X)$, hence a
   [[graded module]] $\mathfrak{a}_\bullet$ in degrees $k \in \mathbb{N}$; $k \geq 1$

1. a [[differential]] $d_{CE}$ that makes the [[graded-commutative algebra]] $Sym_{C^\infty(X)}(\mathfrak{a}^\ast_\bullet)$
   into a cochain [[differential graded-commutative algebra]] (hence with $d_{CE}$ of degree +1) over $\mathbb{R}$
   (not necessarily over $C^\infty(X)$), to be called the _[[Chevalley-Eilenberg algebra]]_ of $\mathfrak{a}$:

   $$
     \label{CEAlgebra}
     CE(\mathfrak{a})
      \;\coloneqq\;
     \left(
       Sym_{C^\infty(X)}(\mathfrak{a}^\ast_\bullet)
       \,,\,
       d_{CE}
     \right)
     \,.
   $$

If we allow $\mathfrak{a}_\bullet$ to also have terms in non-positive degree, then we speak of a _[[derived Lie algebroid]]_.
If $\mathfrak{a}_\bullet$ is _only_ concentrated in negative degrees, we also speak of a _[[derived manifold]]_.

With $C^\infty(X)$ canonically itself regarded as a [[dgc-algebra]], there is a canonical
dg-algebra homomorphism

$$
  CE(\mathfrak{a}) \longrightarrow C^\infty(X)
$$

which is the identity on $C^\infty(X)$ and zero on $\mathfrak{a}^\ast_{\neq 0}$.

=--


+-- {: .num_remark #dgManifolds}
###### Remark
**([[Lie algebroids]] as [[differential graded manifolds]])**

Definition \ref{LInfinityAlgebroid} of _[[derived Lie algebroids]]_ is an encoding in [[higher algebra]]
([[homological algebra]], in this case) of a situation that is usefully thought of in terms of
[[higher differential geometry]].

To see this, recall the magic algebraic properties of ordinary [[differential geometry]] (prop. \ref{AlgebraicFactsOfDifferentialGeometry})

1. [[embedding of smooth manifolds into formal duals of R-algebras]];

1. [[smooth Serre-Swan theorem|embedding of smooth vector bundles into formal duals of modules]]

Together these imply that we may think of the [[graded algebra]] underlying a [[Chevalley-Eilenberg algebra]]
as being the [[algebra of functions]] on a [[graded manifold]]

$$
  \cdots \times \mathfrak{a}_2 \times \mathfrak{a}_1 \times X \times \mathfrak{a}_{-1} \times \cdots
$$

which is [[infinitesimal]] in non-vanishing degree.

The "higher" in [[higher differential geometry]] refers to the degrees higher than zero. See at
_[[schreiber:Higher Structures]]_ for exposition.
Specifically if $\mathfrak{a}_\bullet$ has components in negative degrees,
these are also called _[[derived manifolds]]_.

=--

+-- {: .num_example #BasicExamplesOfLieAlgebroids}
###### Example
**(basic examples of [[Lie algebroids]])

Two basic examples of [[Lie algebroids]] are:

1. For $X$ any [[smooth manifold]], then setting $\mathfrak{a}_{\neq 0 } \coloneqq 0$ and $d_{CE} \coloneqq 0$
   makes it a Lie algebroid. We will just still just write $X$ for the manifold trivially regarded
   as a Lie alebroid this way.

1. For $\mathfrak{g}$ a [[finite number|finite]] [[dimension|dimensional]] [[Lie algebra]]
   we obtain a Lie algebroid denoted $\ast/\mathfrak{g}$ or $B \mathfrak{g}$ by taking the base manifold
   to be the point, taking $\mathfrak{a}$ to be concentrated in degree 1 on $\mathfrak{g}$, and
   taking the differential to be given by the linear dual of the [[Lie bracket]]

   $$
     d_{CE} \;\colon\; \mathfrak{g}^\ast \overset{[-,-]^\ast}{\longrightarrow} \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
     \,.
   $$

   If $(t_\alpha)$ is a [[linear basis]] for $\mathfrak{g}$ and $(t^\alpha)$ a corresponding dual basis for $\mathfrak{g}^\ast$,
   then this is given by

   $$
     d_{CE} t^\alpha -\tfrac{1}{2} C^\alpha_{\beta \gamma} t^\beta \wedge t^\gamma
     \,,
   $$

   where on the right we have the structure constants of the [[Lie bracket]] in this basis:

   $$
     [t^\beta, t^\gamma] = t_\alpha C^\alpha{}_{\beta \gamma}
     \,.
   $$

   The resulting [[dgc-algebra]]

   $$
     \left(
       \wedge^\bullet \mathfrak{g}^\ast, d_{CE} = [-,-]^\ast
     \right)
   $$

   is the standard [[Chevalley-Eilenberg algebra]] from basic [[Lie theory]], whence the name of the general concept.


=--

The two basic examples \ref{BasicExamplesOfLieAlgebroids} are unified by the concept of _[[action Lie algebroid]]_
(def. \ref{ActionLieAlgebroid} below),
which is the one of central relevance for the discussion of [[gauge theory]]: the local [[BRST complex]] (def. \ref{LocalOffShellBRSTComplex} below).





+-- {: .num_defn #ActionLieAlgebroid}
###### Definition
**([[action Lie algebroid]])**

Given an [[infinitesimal]] [[action]] of a [[Lie algebra]] $\mathfrak{g}$
on a manifold $X$ (def. \ref{InfinitesimalActionByLieAlgebra}) the _[[action Lie algebroid]]_ $X/\mathfrak{g}$
is the [[Lie algebroid]] (def. \ref{LInfinityAlgebroid}) whose underlying space is $X$;
whose $C^\infty(X)$-module is concentrated in degree 1 on the [[free module]] $C^\infty(X) \otimes_{\mathbb{R}} \mathfrak{g}$
and whose [[Chevalley-Eilenberg algebra|CE-differential]] is given

* on functions $f \in C^\infty(X)$ by the Lie algebra action

  $$
    d_{CE} f \coloneqq \rho(-)(f) \in C^\infty(X) \otimes \mathfrak{g}^\ast
  $$

* on dual Lie algebra elements $\omega \in \mathfrak{g}^\ast$ by the [[linear dual]] of the [[Lie bracket]]

  $$
    d_{CE} \omega \coloneqq \omega([-,-]) \;\in \; \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
    \,.
  $$

In terms of [[coordinates]] this means the following. Assume that $X = \mathbb{R}^n$ is a [[Cartesian space]]
with coordinates $(\phi^a)$ and let $\{t_\alpha\}$ be a [[linear basis]] for $\mathfrak{g}$
with dual basis $(c^\alpha)$ for $\mathfrak{g}^\ast$. Then the
Lie action has components

$$
  d_{CE} \phi^a = \rho^{a}_{\alpha} c^\alpha
$$

$$
  d_{CE} c^\alpha = -\tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} c^\beta \wedge c^\gamma
$$

where on the right we have the structure constants of the Lie algebra in this basis:

$$
  [t_\beta, t_\gamma] = \gamma^\alpha{}_{\beta \gamma} t_\alpha
  \,.
$$

That the differential $d_{CE}$ thus defined indeed squares to 0 is

* in degree 0 the action property: $\rho([t, t']) = [\rho(t), \rho(t')]$

* in degree 1 the [[Jacobi identity]].

=--


+-- {: .num_example #HorizontalTangentLieAlgebroid}
###### Example
**(horizontal [[tangent Lie algebroid]])**

Let $\Sigma$ be a [[smooth manifold]] or more generally a [[locally pro-manifold]] (prop. \ref{JetBundleIsLocallyProManifold}).
Then we write $\Sigma/T\Sigma$ for the [[Lie algebroid]] over $X$ and whose [[Chevalley-Eilenberg algebra]] is generated
over $C^\infty(X)$ in degree 1
from the [[module]]

$$
  \mathfrak{a}_1^\ast \coloneqq (\Gamma(T \Sigma))^\ast \simeq\Gamma(T^\ast \Sigma) = \Omega^1(\Sigma)
$$

of [[differential 1-forms]] and whose [[Chevalley-Eilenberg differential]] is the [[de Rham differential]],
so that the [[Chevalley-Eilenberg algebra]] is the [[de Rham dg-algebra]]

$$
  CE( \Sigma/T\Sigma ) \coloneqq (\Omega^\bullet(\Sigma), d_{dR})
  \,.
$$

This is called the _[[tangent Lie algebroid]]_ of $\Sigma$.
As a [[graded manifold]] (via remark \ref{dgManifolds}) this is called the "[[shifted tangent bundle]]" $T[1] \Sigma$ of $X$.

More generally, let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]] over $\Sigma$. Then there is a [[Lie algebroid]]
$J^\infty_\Sigma(E)/T\Sigma$ over the [[jet bundle]] of $E$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
defined by its [[Chevalley-Eilenberg algebra]] being the [[horizontal derivative|horizontal]] part of the
[[variational bicomplex]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

$$
  CE\left(
    J^\infty_\Sigma(E)/T\Sigma
  \right)
  \;\coloneqq\;
  \left(\Omega^{\bullet,0}_\Sigma(E), d\right)
  \,.
$$

The underlying [[graded manifold]] of $J^\infty_\Sigma(E)/T\Sigma$ is the [[fiber product]]
$J^\infty_\Sigma(E)\times_\Sigma T[1]\Sigma$ of the [[jet bundle]] of $E$ with the [[shifted tangent bundle]]
of $\Sigma$.

There is then a canonical homomorphism of Lie algebroids (def. \ref{HomomorphismBetweenLieAlgebroids})

$$
  \array{
    J^\infty_\Sigma(E)/T\Sigma
    \\
    \downarrow
    \\
    \Sigma/T\Sigma
  }
$$

=--


+-- {: .num_example #LocalOffShellBRSTComplex}
###### Example
**(local [[BRST complex]] and [[ghost fields]] for irreducible closed [[gauge parameters]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), and let
$\mathcal{G} =  \overset{gb}{\to} \Sigma$ be a bundle of irreducible closed  [[gauge parameters]]
for the theory (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with
bundle morphism

$$
  \array{
    J^\infty_\Sigma( \mathcal{G} \times_\Sigma E )
    && \overset{R}{\longrightarrow} &&
    V_\Sigma E
    \\
    & \searrow && \swarrow
    \\
    && E
  }
  \,.
$$

Assuming that the gauge parameter bundle is [[trivial vector bundle|trivial]], $\mathcal{G} = \mathfrak{g} \times \Sigma$,
then by example \ref{ActionOfGaugeParameterizedInfinitesimalGaugeSymmetriesOnJetBundle} this
induces an [[action]] $\hat R$
of a Lie algebra $\mathfrak{g}^\infty$ on $J^\infty_\Sigma E$ by [[infinitesimal]] [[diffeomorphisms]].

The corresponding [[action Lie algebroid]] $J^\infty_\Sigma(E)/\mathfrak{g}^\infty$
(def. \ref{ActionLieAlgebroid}) has as underlying [[graded manifold]] (remark \ref{dgManifolds})

$$
  \mathfrak{g}^\infty[1] \times J^\infty_\Sigma(E)
  \;\simeq\;
  J^\infty_\Sigma( \mathcal{G}[1] \times_\Sigma E  )
$$

the [[jet bundle]] of the _[[graded manifold|graded]] [[field bundle]]_

$$
  E_{BRST} \coloneqq \mathcal{G}[1]  \times E
$$

which regards the [[gauge parameters]] as [[field (physics)|fields]] in degree 1.
As such these are called _[[ghost fields]]_:

$$
  \left\{
    \text{ghost field histories}
  \right\}
   \;\coloneqq\;
  \Gamma_\Sigma( \mathcal{G}[1] )
  \,.
$$

Therefore we write suggestively

$$
  E/\mathcal{G}
  \;\coloneqq\;
  J^\infty_\Sigma(E)/\mathfrak{g}^\infty
$$

for the [[action Lie algebroid]] of the [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge symmetries]]
on the [[jet bundle]] of the [[field bundle]].

The Chevalley-Eilenberg [[differential]] of the [[BRST complex]] is traditionally denoted

$$
  s_{BRST} \coloneqq d_{CE}
  \,.
$$

To express this in [[coordinates]], assume that the [[field bundle]] $E$ as well as the [[gauge parameter]]
bundle are [[trivial vector bundles]] (example \ref{TrivialVectorBundleAsAFieldBundle})
with $(\phi^a)$ the [[field (physics)|field]] coordinates on the [[fiber]] of $E$
with induced jet coordinates $((x^\mu), (\phi^a), (\phi^a_{\mu}), \cdots)$ and
$(c^\alpha)$ are [[ghost field]] coordinates on the fiber of $\mathcal{G}[1]$ with induced
jet coordinates $((x^\mu), (c^\alpha), (c^\alpha_\mu), \cdots)$.

Then in terms of the
corresponding coordinate expression for the gauge symmetries $R$ (eqs:CoordinateExpressionForGaugeParameterized)
the [[BRST differential]] is given on the [[field (physics)|fields]] by

$$
  s_{BRST} \, \phi^a
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
    R^{a \mu_1 \cdots \mu_k}_{\alpha} c^\alpha_{\mu_1 \cdots \mu_k}
$$

and on the [[ghost fields]] by

$$
  s_{BRST} \, c^\alpha = \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma
  \,,
$$

and it extends from there, via prop. \ref{EvolutionaryVectorFieldProlongation},
to jets of fields and ghost fields by (anti-)commutativity with the [[total derivative|total spacetime derivative]].

Moreover, since the action of the [[infinitesimal gauge symmetries]] is by definition via
prolongations (prop. \ref{EvolutionaryVectorFieldProlongation}) of [[evolutionary vector fields]] (def. \ref{EvolutionaryVectorField}) and hence compatible with the [[total derivative|total spacetime derivative]] (eqs:ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative) this construction
descends to the horizontal tangent Lie algebroid $J^\infty_\Sigma(E)/T\Sigma$ (example \ref{HorizontalTangentLieAlgebroid})
to yield

$$
  E/(\mathcal{G}\times_\Sigma T \Sigma)
  \;\coloneqq\;
  \left(J^\infty_\Sigma(E)/T\Sigma\right)/\mathfrak{g}^\infty
$$

The [[Chevalley-Eilenberg differential]] on $E/(\mathcal{G}\times_\Sigma T \Sigma)$ is

$$
  d - s_{BRST}
$$

The [[Chevalley-Eilenberg algebra]] of functions on this [[differential graded manifold]] (eqs:CEAlgebra)
is called the off-shell _[[local BRST complex]]_ ([Barnich-Brandt-Henneaux 94](#BarnichBrandtHenneaux94)).

We may pass from the [[local BRST complex]] on the [[jet bundle]] to the "global" BRST
complex by [[transgression of variational differential forms]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}):

Write $Obs_\Sigma(E \times\Sigma \mathcal{G}[1])$ for the induced graded [[algebra of observables]] (def. \ref{LocalObservables}).
For $A \in \Omega^{p+1,\bullet}_\Sigma(E \times_\Sigma \mathcal{G}[1])$ with corresponding [[local observable]]
$\tau_\Sigma(A) \in LocObs_\Sigma(E \times_\Sigma \mathcal{G}[1])$ its BRST differential is defined by

$$
  s_{BRST} \tau_{\Sigma}(A) \;\coloneqq\; \tau_{\Sigma}(s_{BRST} A)
$$

and extended from there to $Obs_\Sigma(E \times_\Sigma \mathcal{G}[1])$ as a graded derivation.

=--

+-- {: .num_prop #}
###### Example
**([[local BRST complex]] for [[free field|free]] [[electromagnetism]] on [[Minkowski spacetime]])

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]] on [[Minkowski spacetime]] (example \ref{ElectromagnetismLagrangianDensity}) with its [[gauge parameter]] bundle as in
example \ref{InfinitesimalGaugeSymmetryElectromagnetism}.

By (eqs:EMProlongedSymmetryVectorField) the action of the [[BRST differential]] is the derivation

$$
  s_{BRST}
   \;=\;
  c_{,\mu} \frac{\partial}{\partial a_\mu}
  +
  c_{, \mu \nu} \frac{\partial}{\partial a_{\mu, \nu}}
  +
  \cdots
  \,.
$$

In particular the [[Lagrangian density]] is BRST-closed

$$
  \begin{aligned}
    s_{BRST} \mathbf{L}
    & =
    s_{BRST} f_{\mu \nu} f^{\mu \nu} dvol_\Sigma
    \\
    & =
    c_{,\mu \nu} f^{\mu \nu} dvol_\Sigma
    \\
    & =
    0
  \end{aligned}
$$

as is the [[Euler-Lagrange form]] (due to the symmetry $c_{,\mu \nu} = c_{,\nu \mu}$ and in contrast to the
skew-symmetry $f_{\mu \nu} = - f_{\nu \mu}$).


=--







$\,$

## Reduced phase space
 {#ReducedPhaseSpace}



Where the ordinary [[shell]] of a [[Lagrangian field theory]] is the _[[critical locus]]_ of the [[Lagrangian density]] with respect to
[[Euler-Lagrange variational derivative|Euler-Lagrange variation]]
inside the ordinary [[jet bundle]] manifold (see [above](#CriticalLocusShell)),
the analog of the concept of [[critical locus]] in the [[homotopy theory|homotopy theoretic]]
"[[higher differential geometry]]" or "[[derived geometry]]" is called the _[[derived critical locus]]_.
Hence the correct incarnation of the [[shell]] when all implicit [[infinitesimal gauge symmetries]] have been made explicit
(as [above](#GaugeSymmetries))
is the _[[derived critical locus]]_ of the [[Lagrangian function]] regarded now as a function on the [[action Lie algebroid]] of gauge symmetries
acting on the [[field bundle]] (hence an element of the [[BRST complex]], example \ref{LocalOffShellBRSTComplex}). The [[algebra of functions]] on this "derived shell" is called the _[[BV-BRST complex]]_ of the theory.

(...)


for derived crit loc on j^infty, have to adjust commutator on  Der(O(X)) so that 
\overline{\phi}_a \mapsto \delta_EL really a Lie algebroid homomorphism is. 
This fixes the commutator to be {s_BRST,-}_alt

We now first discuss the construction of the reduced phase space in the simple form in 
which it would appear after [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
if [[spacetime]] were [[compact space|compact]], so that, by the [[principle of extremal action]] (prop. \ref{PrincipleOfExtremalAction}),
it would be the [[derived critical locus]] ($d S = 0$) of a globally defined [[action functional]] $S$.

This serves as a warmup to the true construction of the derived [[shell]] in the [[jet bundle]], where the 
action functional is "de-transgressed" to the [[Lagrangian density]], which is invariant under gauge transformations
only up to horizontally exact terms.


With [[L-infinity algebroid|Lie algebroids]] in hand, we now turn to discussion of the "maps" between them, their
_[[homomorphisms]]_ (def. \ref{HomomorphismBetweenLieAlgebroids}) below.
This makes manifest in which sense [[L-infinity algebroid|higher Lie algebroids]] make [[gauge symmetry]] _explicit_,
since functions out of an [[action Lie algebroid]] $X/\mathfrak{g}$ (def. \ref{ActionLieAlgebroid})
turn out to be _necessarily_ gauge invariant (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids} below).




+-- {: .num_defn #HomomorphismBetweenLieAlgebroids}
###### Definition
**([[homomorphism]] between [[Lie algebroids]])**

Given two [[derived Lie algebroids]] $\mathfrak{a}$, $\mathfrak{a}'$ (def. \ref{LInfinityAlgebroid}), then a [[homomorphism]]
between them

$$
  f \;\colon\; \mathfrak{a} \longrightarrow \mathfrak{a}'
$$

is a [[dg-algebra]]-[[homomorphism]] between their [[Chevalley-Eilenberg algebras]] going the other way around

$$
  CE(\mathfrak{a}) \longleftarrow CE(\mathfrak{a}') \;\colon\; f^\ast
$$

such that this covers an algebra homomorphism on the function algebras (a "[[curved sh-map|non-curved sh-map]]")

$$
  \array{
    CE(\mathfrak{a}) &\overset{f^\ast}{\longleftarrow}& CE(\mathfrak{a}')
    \\
    \downarrow && \downarrow
    \\
    C^\infty(X) &\underset{(f\vert_X)^\ast}{\longleftarrow}& C^\infty(Y)
  }
  \,.
$$

=--


+-- {: .num_example #GaugeInvariantFunctionsIntermsOfLieAlgebroids}
###### Example
**([[gauge invariance|gauge invariant]] [[functions]] in terms of [[Lie algebroids]])

Let $X/\mathfrak{g}$ be an [[action Lie algebroid]] (example \ref{ActionLieAlgebroid})
and regard the [[real line]] $\mathbb{R}^1$ as a Lie algebroid by example \ref{BasicExamplesOfLieAlgebroids}.
Then homomorphisms of Lie algebroids (def. \ref{HomomorphismBetweenLieAlgebroids}) of the form

$$
  f \;\colon\; X/\mathfrak{g} \longrightarrow \mathbb{R}^1
  \,,
$$

hence _smooth functions on the Lie algebroid_, are equivalently

* ordinary [[smooth functions]] $f \colon X \longrightarrow \mathbb{R}^1$ on the underlying [[smooth manifold]],

* which are [[invariant]] under the Lie action in that $\rho(-)(f) = 0$.

=--


+-- {: .proof}
###### Proof

An $\mathbb{R}$-algebra homomorphism

$$
  CE( X/\mathfrak{g} )
    \longleftarrow
  C^\infty(\mathbb{R}^1)
$$

is fixed by what it does to the canonical coordinate function on $\mathbb{R}^1$, which is taken by
$f^\ast$ to $f \in C^\infty(X) \hookrightarrow CE(X/\mathfrak{g})$. For this to be a dg-algebra
homomorphism it needs to respect the differentials on both sides. Since the differential
on right right is trivial, the condition is that $0 = d_{CE} f = \rho(-)(f)$.

=--


Given a gauge invariant function, hence a function $S \colon X/\mathfrak{g} \to \mathbb{R}$ on a Lie algebroid (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids}), its [[exterior derivative]] $d S$ should be a
[[section]] of the [[cotangent bundle]] of the Lie algebroid. Moreover, if all field variations are
infinitesimal (as in def. \ref{LocalObservablesOnInfinitesimalNeighbourhood}) then it should in fact be
a section of the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of the [[zero section]] inside the [[cotangent bundle]], the _infinitesimal cotangent bundle_ $T^\ast(X/\mathfrak{g})$ of the Lie algebroid (def. \ref{LieAlgebroidInfinitesimalCotangentBundle} ebelow).

To motivate the definition \ref{LieAlgebroidInfinitesimalCotangentBundle} below of _infinitesimal cotangent bundle of a Lie algebroid_ 
recall from example \ref{InfinitesimalNeighbourhood} that the [[algebra of functions]]
on the infinitesimal cotangent bundle should be fiberwise the [[formal power series algebra]] in the [[linear functions]].
But a fiberwise linear function on a [[cotangent bundle]] is by definition a [[vector field]].
Finally observe that [[derivations of smooth functions are vector fields|vector fields are equivalently derivations of smooth functions]] (prop. \ref{AlgebraicFactsOfDifferentialGeometry}). This leads to the following definition:

+-- {: .num_defn #LieAlgebroidInfinitesimalCotangentBundle}
###### Definition
**([[automorphism ∞-Lie algebra|infinitesimal cotangent Lie algebroid]])**

Let $\mathfrak{a}$ be a [[Lie ∞-algebroid]] (def. \ref{LInfinityAlgebroid}) over some manifold $X$.
Then its _infinitesimal cotangent bundle_ $T^\ast \mathfrak{a}$ is the [[Lie ∞-algebroid]] over $X$
whose underlying [[graded module]] over $C^\infty(X)$ is the [[direct sum]] of the original module
with the [[derivations]] of the graded algebra underlying $CE(\mathfrak{a})$:

$$
 (T^\ast \mathfrak{a})^\ast_\bullet
 \;\coloneqq\;
 \mathfrak{a}^\ast_\bullet \oplus Der(CE(\mathfrak{a}))_\bullet
$$

with [[differential]] on the summand $\mathfrak{a}$ being the original differential and
on $Der(CE(\mathfrak{a}))$ being the [[commutator]] with the differential on $CE(\mathfrak{a})$
(which is itself a graded derivation of degree +1):


$$
  d_{CE(T^\ast \mathfrak{a})}\vert_{\mathfrak{a}^\ast} \;\coloneqq\; d_{CE(\mathfrak{a})}
$$

$$
  d_{CE(T^\ast \mathfrak{a})}\vert_{Der(\mathfrak{a})} \;\coloneqq\; [d_{CE(\mathfrak{a})},-]
  \,.
$$

There is a canonical homomorphism of Lie algebroids (def. \ref{HomomorphismBetweenLieAlgebroids})

$$
  \label{CotangentLieAlgebrpoidProjection}
  T^\ast \mathfrak{a} \longrightarrow \mathfrak{a}
$$

given dually by the identity on the original generators.

=--


+-- {: .num_example #CotangentBundleOfActionLieAlgebroid}
###### Example
**([[automorphism ∞-Lie algebra|infinitesimal cotangent bundle]] of [[action Lie algebroid]])**

Let $X/\mathfrak{g}$ be an [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid})
where 

* $X = \mathbb{R}^n$ is a [[Cartesian space]] with [[coordinates]] $(\phi^a)$;

* $\mathfrak{g}$ is a [[Lie algebra]] with [[linear basis]] $(c_\alpha)$
  and corresponding structure constants $(\gamma^{\alpha}{}_{\beta \gamma})$;

* the infinitesimal [[action]] is given in components by

  $$
    d_{CE} \;\phi^a\; = R^a_\alpha c^\alpha
  $$
  
  for smooth functions $R^a_\alpha$ on $X$.

Then the infinitesimal cotangent Lie algebroid $T^\ast (X/\mathfrak{g})$ (def. \ref{LieAlgebroidInfinitesimalCotangentBundle})  
has as underlying cochain complex 

$$
  \array{
    \left\langle
      \frac{\partial}{\partial c^a}
    \right\rangle
    &
    \overset{[d_{\mathfrak{a}}, -]}{\to}
    &
    \left\langle
      \frac{\partial}{\partial x^i}
    \right\rangle
    \oplus
     \left\langle
       c^a \frac{\partial}{\partial c^b}
     \right\rangle
    \\
    -1 && 0
  }
$$

and the CE-differential on these is given by

$$
  \label{CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnGhostFieldCoordinates}
  \begin{aligned}
    d_{CE(T^\ast(X/\mathfrak{g}))} \frac{\partial}{\partial c^\alpha}
    & \coloneqq
    \left[d_{CE(X/\mathfrak{g})}, \frac{\partial}{\partial c^\alpha} \right]
    \\
     & =
     R_\alpha^a  \frac{\partial}{\partial \phi^a}
      +
     \gamma^\beta{}_{\alpha \gamma} c^\gamma \frac{\partial}{\partial c^\beta}
  \end{aligned}
$$

and

$$
  \label{CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnFieldCoordinates}
  \begin{aligned}
    d_{CE(T^\ast(X/\mathfrak{g}))}  \frac{\partial}{\partial \phi^a}
    \left[
      d_{CE(X/\mathfrak{g})}, 
      \frac{\partial}{\partial \phi^a}
    \right]
     =
    c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \frac{\partial}{\partial \phi^b}
  \end{aligned}
  \,.
$$


=--


+-- {: .num_prop #ExteriorDifferentialOfGaugeInvariantFunctionIsSectionOfInfinitesimalCotangentLieAlgebroid}
###### Proposition
**([[exterior differential]] of [[gauge invariant]] function is [[section]] of [[automorphism ∞-Lie algebra|infinitesimal cotangent bundle]])**

For $\mathfrak{a}$ an [[Lie ∞-algebroid]] (def. \ref{LInfinityAlgebroid}) over some $X$;
and $S \;\colon\;\mathfrak{a} \longrightarrow \mathbb{R}$ a [[gauge invariant]] smooth function on it (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids});
there is an induced [[section]] $d S$ of the infinitesimal cotangent Lie algebroid (def. \ref{LieAlgebroidInfinitesimalCotangentBundle}) 
bundle projection (eq:CotangentLieAlgebrpoidProjection:

$$
  \array{
    && T^\ast \mathfrak{a}
    \\
    & {}^{\mathllap{d S}}\nearrow & \downarrow
    \\
    \mathfrak{a}
    &=&
    \mathfrak{a}
  }
  \,,
$$

given dually

$$
  (d S)^\ast \;\colon\; CE(T^\ast \mathfrak{a}) \longrightarrow CE(\mathfrak{a})
$$

by the map which sends

1. the generators in $\mathfrak{a}^\ast$ to themselves;

1. a [[vector field]] $v$ on $X$, regarded as a degree-0 [[derivation]] to 
   $d S(v) = v(S) \in C^\infty(X)$;
   
1. all other derivations to zero.


=--

+-- {: .proof}
###### Proof

We discuss the proof in the special case of example \ref{CotangentBundleOfActionLieAlgebroid}.
The general case is directly analogous.

We need to check that $(d S)^\ast$ respects the CE-differentials. 

On the original generators in 
$\mathfrak{a}^\ast$ this is immediate, since on these the CE-differential on both sides
are by definition the same.

On the derivation $\frac{\partial}{ \partial \phi^a}$ we find from (eq:CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnFieldCoordinates)

$$
  \array{
    \left\{
       \frac{\partial S}{\partial \phi^a}
    \right\}
      &\overset{(d S)^\ast}{\longleftarrow}& 
    \left\{ \frac{\partial}{\partial \phi^a} \right\}
    \\
    {}^{\mathllap{d_{CE(\mathfrak{a})}}}\downarrow && \downarrow^{\mathrlap{d_{CE(T^\ast \mathfrak{a})}}}
    \\
    \left\{
       c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \frac{\partial S}{\partial \phi^b}
    \right\}
      &\underset{(d S)^\ast}{\longleftarrow}&
    \left\{
       c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \frac{\partial}{\partial \phi^b}
    \right\}
  }
$$

and on the derivation $\frac{\partial}{\partial c^\alpha}$ we find from (eq:CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnGhostFieldCoordinates)
and using the gauge invariance of $S$

$$
  \array{
    \left\{
      0
    \right\}
      &\overset{(d S)^\ast}{\longleftarrow}&
    \left\{
      \frac{\partial}{\partial c^\alpha}
    \right\}
    \\
    \downarrow && \downarrow    
    \\
    \left\{
      0 = R_\alpha^a \frac{\partial S}{\partial \phi^a}
    \right\}
      &\overset{(d S)^\ast}{\longleftarrow}&
    \left\{ 
      R_\alpha^a  \frac{\partial}{\partial \phi^a}
      +
      \gamma^\beta{}_{\alpha \gamma} c^\gamma \frac{\partial}{\partial c^\beta}
    \right\}
  }
  \,.
$$

=--


+-- {: .num_defn #DerivedCriticalLocusOfGaugeInvariantFunctionOnLieAlgebroid}
###### Definition
**([[derived critical locus]] of [[gauge invariant]] function on [[Lie ∞-algebroid]])

Let $\mathfrak{a}$ be a [[Lie ∞-algebroid]] (def. \ref{LInfinityAlgebroid}) over some $X$, let

$$
  S \;\colon\; \mathfrak{a} \longrightarrow \mathbb{R}
$$

be a [[gauge invariant]] function (exmaple \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids}) and consider
the section of of its infinitesimal cotangent bundle $T^\ast \mathfrak{a}$ (def. \ref{CotangentBundleOfActionLieAlgebroid}) corresponding to its exterior derivative
via prop. \ref{ExteriorDifferentialOfGaugeInvariantFunctionIsSectionOfInfinitesimalCotangentLieAlgebroid}.

$$
  \mathfrak{a} && \overset{d S}{\longrightarrow} && T^\ast \mathfrak{a}
  \\
  & \searrow && \swarrow
  \\
  && \mathfrak{a}
$$

Then the _[[derived critical locus]]_ of $S$ is the [[derived Lie algebroid]] (def. \ref{LInfinityAlgebroid})
$\mathfrak{a}_{d S \simeq 0}$ which is the [[homotopy pullback]] of the section $d S$ along the [[zero section]]:

$$
  \array{
    \mathfrak{a}_{d S \simeq 0} 
      &\longrightarrow&
    \mathfrak{a}
    \\
    \downarrow &(hpb)& \downarrow^{\mathrlap{0}}
    \\
    \mathfrak{a}
      &\underset{d S}{\longrightarrow}&
    T^\ast \mathfrak{a}
  }
  \,.
$$

This means equivalently (details are at _[[derived critical locus]]_) that the Chevalley-Eilenberg algebra of $\mathfrak{a}_{d S \simeq 0}$ is like that of
$T^\ast \mathfrak{a}$ except for two changes: 

1. all [[derivations]] are shifted down in degree by one;

1. the CE-differential on the derivations coming from vector fields $v$ on $X$ is that of $T^\ast \mathfrak{a}$
   plus $d S(v) = v(S)$.
   

=--

+-- {: .num_example}
###### Example

Consider again example \ref{CotangentBundleOfActionLieAlgebroid} of a gauge invariant function $S \colon X/\mathfrak{g} \to \mathbb{R}$
on an [[action Lie algebroid]], with [[corrdinate]] generators for the 
[[Chevalley-Eilenberg algebra]] given by $((\phi^a), (c^\alpha))$. We denote the corresponding degree-shifted
copies of the derivations with respect to these coordinates by 

$$
  \overline{\phi}_a \;\coloneqq\; \frac{\partial}{\partial \phi^a}[-1]
$$

$$
  \overline{c}_\alpha \;\coloneqq\; \frac{\partial}{\partial c^\alpha}[-1]
$$


=--

+-- {: .num_defn}
###### Definition

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over some [[spacetime]] $\Sigma$, and let $\mathcal{G} \overset{gb}{\to} \Sigma$ be
a bundle of closed irreducible [[gauge parameters]] (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}),
inducing via example \ref{LocalOffShellBRSTComplex} the [[Lie algebroid]]

$$
  E / ( \mathcal{G} \times_\Sigma T \Sigma )
  \;=\;
  \left(
    J^\infty_\Sigma( E \times_\Sigma (\mathcal{G}[1]) )
    ,
    s_{BRST} \in \Gamma( T( J^\infty_\Sigma( E \times_\Sigma (\mathcal{G}[1]) ) ) ) )
  \right)
$$

whose [[Chevalley-Eilenberg algebra]] is the [[local BRST complex]] of the field theory.

(...)


=--



+-- {: .num_defn #WeilAlgebra}
###### Definition
**([[Weil algebra]] of a [[Lie algebroid]])**

Given a [[Lie algebroid]] $\mathfrak{a}$ over some $X$ (def. \ref{LInfinityAlgebroid}), its [[Weil algebra]] is

$$
  W(\mathfrak{a})
    \;\coloneqq\;
  \left(
    Sym_{C^\infty(X)}( \Gamma(T^\ast X) \oplus \mathfrak{a}_\bullet \oplus \mathfrak{a}[1]_\bullet )
     \;,\;
    \mathbf{d}_W \coloneqq \mathbf{d} + d_{CE}
  \right)
  \,,
$$

where $\mathbf{d}$ acts as the de Rham differential $\mathbf{d} \colon C^\infty(X) \to \Gamma(T^\ast X)$
on functions, and as the degree shift operator $\mathbf{d} \colon \mathfrak{a}_\bullet \to \mathfrak{a}[1]_\bullet$
on the graded elements.

=--


+-- {: .num_example }
###### Example

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
equipped with a closed irreducible [[gauge parameter]]  bundle $\mathcal{G}$ (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}).
Consider the [[Lie algebroid]] $E/(\mathcal{G} \times_\Sigma T \Sigma)$ from example \ref{LocalOffShellBRSTComplex},
whose [[Chevalley-Eilenberg algebra]] is the [[local BRST complex]] of the theory.

Then its [[Weil algebra]] $W(E/(\mathcal{G} \times_\Sigma T \Sigma))$ (def. \ref{WeilAlgebra})
has as differential the [[variational derivative]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
plus the [[BRST differential]]

$$
  \begin{aligned}
    d_{W}
    & = \mathbf{d} - (d - s_{BRST})
    \\
    & =
    \delta + s_{BRST}
  \end{aligned}
  \,.
$$

Therefore we speak of the _[[variational BRST-bicomplex]]_ and write

$$
  \Omega^\bullet_\Sigma( E/(\mathcal{G} \times_\Sigma T \Sigma) )
  \,.
$$

Now pass to the [[derived critical locus]] of $E/(\mathcal{G} \times_\sigma T \Sigma)$
at the elements $\frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}$.
The resulting [[derived Lie algebroid]] has as [[Weil algebra]] the variational BV-bicomplex
with differential $\mathbf{d} - (d- s))$.

(...)

=--





+-- {: .num_prop #dWCohomology}
###### Proposition
**($d_W$-cohomology)**

The $d_W$-closed elements in degree $(p,0)$ are precisely pairs $(v,J_v)$
consisting of an implicit infinitesimal local gauge symmetry $v$ and a conserved current $J_v$ for it.

The $d_W$-exact elements in this degree are sums of

1. $d$-exact currents;

1. on-shell vanishing implicit gauge transformations;

1. on-shell vanishing currents with their horizontally exact gauge transformations


=--

+-- {: .proof}
###### Proof


The $d_W$-closed element are
the implicit infinitesimal gauge symmetries $v$ regarded as an [[antifield]] $v^a \overline{\phi}_a$
multiplied with the [[volume form]] $dvol_\Sigma$
together with their Noether current $J_v \in \Omega^{p,0}_\Sigma(E)$ (prop. \ref{NoethersFirstTheorem})


$$
  \array{
    \{J_v\} &\overset{d}{\longrightarrow}& \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \uparrow\mathrlap{s_{BV}}
    \\
    && \{ v^a \overline{\phi}_a dvol_\Sigma\}
  }
$$



Such a pair is exact if

$$
  \array{
    \{K\}
     &\overset{d}{\longrightarrow}&
    \{ d K + v^{a \mu} \frac{\delta_{EL}L}{\delta \phi^a} \iota_{\partial_\mu} dvol_\Sigma   \} &\overset{d}{\longrightarrow}& \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \mathllap{s_{BV}}\uparrow && \uparrow\mathrlap{s_{BV}}
    \\
    && v^{a \mu} \overline{\phi}_a \iota_{\partial_\mu} dvol_\Sigma
      &\underset{-d}{\longrightarrow}&
    \{ v^a \overline{\phi}_a dvol_\Sigma\}
    \\
    && && \uparrow\mathrlap{s_{BV}}
    \\
    &&
    && \kappa^{a b } \overline{\phi}_a \overline{\phi}_b dvol_\Sigma
  }
$$

(...)

=--



So now we define, in analogy to what we did in the underived case, the derived vertical derivative to be what
remains of the [[Weil algebra]] derivative once we subtract the derived horizontal derivative:

$$
  \delta_W \coloneqq \mathbf{d}_W - d_W
  \,.
$$

This way now the local [[BV-BRST complex]] given as the [[derived critical locus]]
of the BRST complex gets a bigrading: the "derived variational bicomplex" or something.



+-- {: .num_example }
###### Example
**(gauge symmetries modulo EOMs are $(d-s)$-exact)


An  [[infinitesimal gauge symmetry]] $v_\epsilon$  of [[gauge parameter]] $(\epsilon^\alpha)$ is a vector field on the jet bundle with components of the form

$$
  \mathcal{L}_{v_\epsilon} \phi^a
   \;\coloneqq\;
  R^a_\alpha \epsilon^\alpha
    +
  R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
$$

such that this is an [[infinitesimal symmetry of the Lagrangian]] in that

$$
  \begin{aligned}
    \iota_{v_\epsilon} \delta_{EL} \mathbf{L}
    & =
    v^a \frac{\delta_{EL} L}{\delta \phi^a} dvol_\Sigma
    \\
    & =
    \epsilon^\alpha
    \left(
       R^a_\alpha \frac{\delta_{EL} L}{ \delta \phi^a}
       -
       \frac{d}{d x^\mu}
       \left(
          R^{a \mu}_\alpha \frac{\delta_{EL} L}{\delta \phi^a}
       \right)
    \right)
    dvol_\Sigma
    +
    d\left(
       \epsilon^\alpha R^{a \mu}_\alpha \frac{\delta_{EL} L}{\delta \phi^a}
    \right)
    \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    0 + d(...)
  \end{aligned}
$$

for all $(\epsilon^\alpha)$.

The corresponding [[antifield|anti]] [[ghost field]] $\overline{c}_\alpha$ are taken by the BV-BRST differential to the antifield-preimage of the term on the left:

$$
  s\left(\overline{c}_\alpha\right)
  \;=\;
  R^a_\alpha \overline{\phi}_a
  -
  \frac{d}{d x^\mu}
  \left(
    R^{a \mu}_\alpha \overline{\phi}_a
  \right)
  \,.
$$

Moreover, an [[on-shell]] vanishing [[infinitesimal symmetry of the Lagrangian]] is a vector field with components of the form

$$
  \kappa^{a b} \frac{\delta_{EL} L}{\delta \phi^a}
$$

for $\kappa^{a b} = - \kappa^{b a}$ a skew-symmetric system of smooth functions on the jet bundle.

The linear combination of such an infinitesimal gauge symmetry and an on-shell vanishing infinitesimal symmetry is $(s+d)$-exact:


$$
  \begin{aligned}
    v^a dvol_\Sigma
    & =
    \left(
      R^a_\alpha \epsilon^\alpha
      +
      R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
      +
      \kappa^{a b} \frac{\delta_{EL} L }{ \delta \phi^a }
    \right)
    dvol_\Sigma
    \\
    & =
    s
    \left(
      \epsilon^\alpha \overline{c}_\alpha
      -
      \tfrac{1}{2}\kappa^{a b} \overline{\phi}_a \overline{\phi}_b
    \right) dvol_\sigma
    +
    d\left(
      \epsilon^\alpha R^{a \mu}_\alpha
    \right)
    \iota_{\partial_\mu} dvol_\Sigma
  \end{aligned}
$$

([Barnich-Brandt-Henneaux 94, p. 20](#BarnichBrandtHenneaux94))


It may be useful to organize this expression into the $s+d$-[[bicomplex]] like so:

$$
  \array{
    \{K\}
     &\overset{d}{\longrightarrow}&
     \{ d K
       +
     \epsilon^\alpha R^{a \mu}_\alpha \frac{\delta_{EL}\mathbf{L}}{ \delta \phi^a}
     \}
     &\overset{d}{\longrightarrow}&
    \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \mathllap{s}\uparrow && \uparrow\mathrlap{-s}
    \\
    &&
    \epsilon^\alpha R^{a \mu}_\alpha \overline{\phi}_a
    \iota_{\partial_\mu} dvol_\Sigma
      &\underset{d}{\longrightarrow}&
    \left\{
      d\left(
        \epsilon^\alpha R^{a \mu}_\alpha \overline{\phi}_a
      \right)
      \iota_{\partial_\mu} dvol_\Sigma
      +
      \left(
        R^a_\alpha \epsilon^\alpha
        +
        R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
        +
        \kappa^{a b} \frac{\delta_{EL} L }{ \delta \phi^a }
      \right)
      \overline{\phi}_a
      \,
      dvol_\Sigma
    \right\}
    \\
    && && \uparrow\mathrlap{-s}
    \\
    &&
    &&
    \left(
       - \epsilon^\alpha \overline{c}_\alpha
       +
      \tfrac{1}{2}\kappa^{a b } \overline{\phi}_a \overline{\phi}_b
    \right)
    dvol_\Sigma
  }
$$

But beware that this uses a convenient abuse of notation: A horizontal derivative of an antifield, such as

$$
  d( b^\mu \overline{\phi}_a ) \iota_{\partial_\mu} dvol_\Sigma
$$

which looks like it should be taken by the BV-BRST differential $s$ to

$$
  - d( b^\mu \frac{\delta_{El} L}{\delta \phi^a} ) \iota_{\partial_\mu} dvol_\Sigma
$$

should rather be regarded as shorthand for the element

$$
  ( b^\mu \frac{\delta_{El} L}{\delta \phi^a} ) \iota_{\partial_\mu} dvol_\Sigma
$$

which is taken by the horizontal differential $d$ to the same expression. This way no horizontal derivatives of antifields apear as actual coordinate functions: the antifields are the coordinates not on the full [[tangent bundle]] of the [[jet bundle]], but just on the bundle of [[evolutionary vector fields]], which locally are functions on the jet bundle with coefficients just the $\overline{\phi}_a$.



=--



## Gauge fixing

In good cases the resulting combined [[BV-BRST complex]] is [[quasi-isomorphism|quasi-isomorphic]]
to a [[derived Lie algebroid]] version of the [[shell]], degreewise compatible with
the [[Poisson bracket Lie n-algebra|local Poisson bracket]] (from prop. \ref{LocalPoissonBracket})
and degreewise admitting [[Cauchy surfaces]]. To this therefore the construction of [[covariant phase spaces]]
and then the construction of local observabes applies degree-wise.

$$
  \array{
     \left\{
        \array{
           \text{Lagrangian field theory with}
           \\
           \text{implicit infinitesimal gauge transformations}
        }
     \right\}
     &\overset{\text{adjoin ghost fields}}{\longrightarrow}&
     \left\{
        \array{
           \text{graded Lagrangian field theory with}
           \\
           \text{explicit infinitesimal gauge transformations}
           \\
           \text{ embodied by BV-BRST differential }
        }
     \right\}
     \\
     \Big\downarrow
     && \Big\downarrow\mathrlap{\text{gauge fixing}}
     \\
     \left\{
       \array{
         \text{gauge invariant}
         \\
         \text{local observables}
       }
     \right\}
     &\underset{\text{pass to cohomology}}{\longleftarrow}&
     \left\{
        \array{
           \text{graded observables with}
           \\
           \text{explicit infinitesimal gauge transformations}
           \\
           \text{embodied by BV-BRST differential }
        }
     \right\}
  }
$$




(...)


Proposition \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} implies
that we need a good handle on determining whether the space of implicit
[[infinitesimal gauge symmetries]] modulo trivial ones is non-zero. This
[[obstruction]] turns out to be neatly captured by methods of [[homological algebra]]
applied to the [[local BV-complex]] (def. \ref{BVComplexOfOrdinaryLagrangianDensity}):

+-- {: .num_example #InterpretationCohomologyOfBVComplex}
###### Example
**([[cochain cohomology]] of local [[BV-complex]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}),
and let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eqs:ConstantSectionOfTrivialShellBundle).

By inspection we find that the [[cochain cohomology]] of the local [[BV-complex]]
$\Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}_{BV}}$ (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) has the following interpretation:

In degree 0 the [[image]] of the [[BV-differential]] coming from degree -1 and modulo $d$-exact terms

$$
  im\left( \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma(E,\varphi)) \overset{s_{BV}}{\to} \Omega^{0,0}_\Sigma(E,\varphi)/im(d) \right)
$$

is the ideal of functions modulo $im(d)$ that vanish [[on-shell]]. Since the differential going _from_ degree 0 to degree 1 vanishes,
the [[cochain cohomology]] in this degree is the [[quotient ring]]

$$
  \begin{aligned}
    H^0\left(\Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}_{BV}}\vert d\right)
      & \simeq
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}}/im(d)
  \end{aligned}
$$

of functions on the [[shell]] $\mathcal{E}$ (eqs:ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber).

In degree -1 the [[kernel]] of the [[BV-differential]] going to degree 0

$$
  ker\left( \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma(E,\varphi)) \overset{s_{BV}}{\to} \Omega^{0,0}_\Sigma(E,\varphi)\right)
$$

is the space of implicit [[infinitesimal gauge symmetries]] (def. \ref{ImplicitInfinitesimalGaugeSymmetry})
and the [[image]] of the differential coming from degree -2

$$
  im\left(
    \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma E,\varphi)
       \wedge_{\Omega^{0,0}_{\Sigma,cp}(E,\varphi)}
    \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma E,\varphi)
      \overset{s_{BV}}{\longrightarrow}
    \Gamma_{\Sigma,cp}(J^\infty_\Sigma V_\Sigma E,\varphi)
  \right)
$$

is the trivial implicit infinitesimal gauge transformations (example \ref{TrivialImplicialInfinitesimalGaugeTransformations}).

Therefore the [[cochain cohomology]] in degree -1 is the [[quotient space]] of implicit infinitesimal gauge transformations
modulo the trivial ones:

$$
  \label{NegativeOneCohomologyBV}
  H^{-1}\left( \Omega^{0,0}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}} \right)
    \simeq
  \frac{
    \left\{
      \text{implicit infinitesimal gauge transformations}
    \right\}
  }
  {
    \left\{
      \text{ trivial implicit infinitesimal gauge transformations}
    \right\}
  }
$$

=--



+-- {: .num_prop #BVComplexIsHomologicalResolutionPreciselyIfNoNonTrivialImplicitGaugeSymmetres}
###### Proposition
**(local [[BV-complex]] is [[homological resolution]] of the [[shell]] precisely if there are no non-trivial implicit [[infinitesimal gauge symmetries]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians})
and let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eqs:ConstantSectionOfTrivialShellBundle).
Furthermore assume that $\mathbf{L}$ is at least quadratic in the vertical coordinates around $\varphi$.

Then the local [[BV-complex]] $\Omega^{0,0}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}$ of local observables (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) is a [[homological resolution]] of the the algebra of functions on the [[infinitesimal neighbourhood]] of $\varphi$ in the [[shell]] (example \ref{ShellForSpacetimeIndepefLindentLagrangians}),
hence the canonical comparison morphisms (eqs:ComparisonMorphismFromOrdinaryBVComplexToLocalObservables)
is a [[quasi-isomorphism]]
precisely if there is no non-trivial (example \ref{TrivialImplicialInfinitesimalGaugeTransformations}) implicit [[infinitesimal gauge symmetry]] (def. \ref{ImplicitInfinitesimalGaugeSymmetry}):

$$
  \left(
    \Omega^{0,0}_{\Sigma}(E,\varphi)\vert_{\mathcal{E}_{BV}}
      \overset{\simeq}{\longrightarrow}
    \Omega^{0,0}_{\Sigma}(E,\varphi)\vert_{\mathcal{E}}
  \right)
  \;\Leftrightarrow\;
  \left(
    \array{
      \text{there are no non-trivial}
      \\
      \text{implicit infinitesimal gauge transformations}
    }
  \right)
  \,.
$$


=--

+-- {: .proof}
###### Proof

By example \ref{InterpretationCohomologyOfBVComplex} the vanishing of non-trivial implicit infinitesimal
gauge symmetries is equivalent to the vanishing of the cochain cohomology of the local BV-complex in degree -1 (eqs:NegativeOneCohomologyBV).

Therefore the statement to be proven is
equivalently that the [[Koszul complex]] of the sequence of elements

$$
  \left(
    \frac{\delta_{EL} L}{\delta \phi^a} \in \Omega^{0,0}_{\Sigma,\varphi}(E)
  \right)_{a = 1}^s
$$

is a [[homological resolution]] of $\Omega^{0,0}_\Sigma(E,\varphi)\vert_{\mathcal{E}}$, hence has vanishing cohomology in all negative degrees,
already if it has vanishing cohomology in degree -1.

By a standard fact about [[Koszul complexes]] ([this prop.](Koszul+complex#KoszulResolutionForNoetherianRngAndElementsInJacobson))
a sufficient condition for this to be the case is that

1. the ring $\Omega^{0,0}_{\Sigma}(E,\varphi)$ is the tensor product of $C^\infty(\Sigma)$ with a [[Noetherian ring]];

1. the elements $\frac{\delta_{EL} L }{\delta \phi^a}$ are contained in its [[Jacobson radical]].

The first condition is the case since $\Omega^{0,0}_{\Sigma}(E,\varphi)$ is by definition a [[formal power series ring]] over a [[field]]
tensored with $C^\infty(\Sigma)$
(by [this example](noetherian+ring#PolynomialAlgebraOverNoetherianRingIsNoetherian)).
Since the Jacobson radical of a power series algebra consists of those elements whose constant term
vanishes (see [this example](Koszul+complex#KoszulComplexForFormalPowerSeriesAlgebras)),
the assumption that $\mathbf{L}$ is at least quadratic, hence that $\delta_{EL}\mathbf{L}$
is at least linear in the fields, guarantees that all $\frac{\delta_{EL}L}{\delta \phi^a}$ are contained
in the Jacobson radical.

=--

Prop. \ref{BVComplexIsHomologicalResolutionPreciselyIfNoNonTrivialImplicitGaugeSymmetres} 
says what [[gauge fixing]] has to accomplish: given a [[local BV-BRST complex]] we need
to find a [[quasi-isomorphism]] to another complex which is such that it comes from a 
_graded_ Lagrangian density whose BV-cohomology vanishes in degree -1
and hence induces a graded covariant phase space, and such that
the remaining BRST differential respects the Poisson bracket on this graded covariant phase space.

(...)



$\,$

## Quantization
 {#QuantumObservables}

Given any [[space]] with [[infinitesimal symmetries]] acting on it, there is the corresponding [[homotopy quotient]]
by these infinitesimal symmetries. For the [[covariant phase space]] of a [[Lagrangian field theory]], as [above](#PhaseSpace) with its [[Poisson Lie algebra]] of infinitesimal symmetries (def. \ref{PoissonBracketOnHamiltonianLocalObservables}),
this infinitesimal [[homotopy quotient]] is known as the _[[Poisson Lie algebroid]]_ and the corresponding genuine
[[homotopy quotient]] is known as the _[[symplectic groupoid]]_. As one passes from [[phase space]] to its [[symplectic groupoid]],
the [[algebra of functions]] on phase space -- hence the [[algebra of observables]] $Obs$ (def. \ref{LocalObservables}) -- which is always a [[commutative algebra]] _[[deformation quantization|deforms]]_ to the corresponding algebra of functions on a [[Lie groupoid]]
called the ([[polarization|polarized]]) [[convolution algebra of a Lie groupoid]]. This is now a [[non-commutative algebra]]
called the _[[algebra of quantum observables]]_ $Obs_{\hbar}$; and this passage from
[[phase space]] to its [[symplectic groupoid]] [[homotopy quotient]] by  Hamiltonian symmetries is called _[[quantization]]_
(specifically: "[[geometric quantization of symplectic groupoids]]").
Here the strength of the non-commutativity is measured by a [[deformation]] parameter called _[[Planck's constant]]_ $\hbar$.

Since the product in the [[algebra of quantum observables]] $Obs_\hbar$ differs from that in $Obs$, the
positivity condition $\langle A^\ast A\rangle \geq 0$ in the definition of  _[[states]]_ $\langle - \rangle$
of a field theory (def. \ref{States}) acquires a different meaning. The states after [[quantization]] are called
_[[quantum states]]_ and their difference witnesses that after [[quantization]] the [[Lagrangian field theory]] is of a different nature:
one says that it is no longer a _[[classical field theory]]_, but a _[[quantum field theory]]_
and that the objects whose states are expressed by these new [[quantum states]] are _[[quantum fields]]_.

Unfortunately, explicitly constructing the [[algebra of quantum observables]] of a [[Lagrangian field theory]] and hence "constructing the [[quantum field theory]]" turns out to be extremely hard, unless some simplifying assumptions are made.

One kind of simplification occurs when the  [[spacetime]] [[dimension]] is very low. For instance if the spacetime dimension is taken to be $p+1 = 1$ -- modelling the approximation where one completely ignores the variation of fields in space
and retains just their time evolution -- then one speaks of [[quantum mechanics]], which is well understood.
Another simplification occurs when the field theory is a _[[free field theory]]_, meaning that its [[equation of motion]]
is a [[normally hyperbolic differential operator|normally hyperbolic]] [[linear differential operator]].
In this case the [[quantum field theory]] is fully understood as long as the underlying [[spacetime]] is a
[[time orientation|time-orientable]] and [[globally hyperbolic spacetime|globally hyperbolic]]. But, as the
name indicates, this captures only the case where there is no [[interaction]] among the [[field (physics)|fields]].

Since the [[algebra of quantum observables]] $Obs_\hbar$ is a _[[deformation]]_ with strength $\hbar$ of the commutative algebra of classical
observables $Obs$ controlled by the [[Poisson Lie algebra]], another simplification occurs if one
gives up on the demand to understand the full deformation at finite value of [[Planck's constant]] $\hbar$
and considers just [[infinitesimal]] values of $\hbar$. Since this means that the resulting [[quantum observables]]
are no longer actual [[smooth functions]] of $\hbar$, but just _[[formal power series]]_, this is called
_[[formal deformation quantization]]_. The resulting "infinitesimally quantized" [[field theory]] is called
_[[perturbative quantum field theory]]_.

For [[interaction|interacting]] [[field theories]] in [[spacetime]] dimension $p+1 \geq 3+1$
their quantization has been constructed to date only in [[perturbation theory]] this way.
The construction of full [[non-perturbative quantum field theory]] (in dimension $\geq 3+1$ with
non-vanishing [[interaction]]) is, at the time of this writing, a wide open problem.

But [[perturbative quantum field theory]] is well understood. This we turn to next...


(...)

* examples

  [[Moyal deformation quantization]]

  [[Fedosov deformation quantization]]


[[free field theory]]

* [[differential operator]], [[normally hyperbolic differential operator]]

* [[Green function]], [[distribution]], [[wave front set]]

* [[causal propagator]], [[advanced propagator]], [[retarded propagator]]

* [[Hadamard state]]


* [[Wick algebra]] and [[normal-ordered product]]

  $\mathcal{F}_{loc} \overset{:-:}{\longrightarrow} \mathcal{F}_{mc}[ [ \hbar ] ]$


[[S-matrix]]

* [[causal additivity]]

* [[time-ordered product]]

* [[causally local net of quantum observables]]

...


[[Feynman diagrams]]

* [[Feynman propagator]]

* [[loop order]]

[[renormalization]]

* [[extension of distributions]]

* [[main theorem of perturbative renormalization]]

...



***


[[!redirects A first idea of quantum field theory]]
