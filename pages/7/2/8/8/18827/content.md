## Reduced phase space
 {#ReducedPhaseSpace}

Where for a [[Lagrangian field theory]] without [[infinitesimal gauge symmetries]] the [[covariant phase space]] is (the [[transgression of variational differential forms|transgression of]]) the plain [[shell]], the _[[reduced phase space]]_ in a theory with [[infinitesimal gauge symmetries]] is the [[homotopy quotient]] of the  [[shell]] by the [[gauge symmetries]].

In order to exhibit the key structure of the [[reduced phase space]] without getting distracted
by the local [[jet bundle]] geometry, we first discuss now the simple form in
which it would appear after [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
if [[spacetime]] were [[compact space|compact]], so that, by the [[principle of extremal action]] (prop. \ref{PrincipleOfExtremalAction}),
it would be the [[derived critical locus]] ($d S = 0$) of a globally defined [[action functional]] $S$.
This is example \ref{ArchetypeOfBVBRSTComplex} below.

This serves as a warmup to the true construction of the derived [[shell]] in the [[action Lie algebroid]] of the [[jet bundle]], where the
action functional is "de-transgressed" to the [[Lagrangian density]], which is invariant under gauge transformations
only up to horizontally exact terms. This culminates in example \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm} below.


$\,$

The key to understanding the "derived reduced prolonged shell", and hence the [[reduced phase space]], as a [[derived critical locus]] is first to exhibit the [[Euler-Lagrange form|Euler-Lagrange variation]] of the [[action functional]], or rather of the [[Lagrangian density]], as a [[section]] of the analog of a [[cotangent bundle]], but now in the realm of [[Lie ∞-algebroids]] (prop. \ref{ExteriorDifferentialOfGaugeInvariantFunctionIsSectionOfInfinitesimalCotangentLieAlgebroid} and prop. \ref{EulerLagrangeFormIsSectionOfLocalCotangentBundleOfJetBundleGaugeActionLieAlgebroid} below).

$\,$

We now discuss these topics:

* _[Derived critical loci inside Lie algebroids](#DerivedCriticalLocusInsideLieAlgebroids)_

* _[Schouten bracket on Lie algebroids](#SchoutenBracketAntibracket)_

* _[Derived critical loci in jet bundles -- the Local BV-BRST complex](#DerivedCriticalLocusOnJetBundle)_

$\,$

**[[derived critical loci]] inside [[Lie algebroids]]**
 {#DerivedCriticalLocusInsideLieAlgebroids}

By analogy with the algebraic formulation of [[smooth functions]] between [[Cartesian spaces]] (the [[embedding of smooth manifolds into formal duals of R-algebras|embedding of Cartesian spaces into formal duals of R-algebras]], prop. \ref{AlgebraicFactsOfDifferentialGeometry}) it is clear how to define a map ([[homomorphism]]) between [[Lie algebroids]]: 

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

such that this covers an algebra homomorphism on the function algebras:

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

(This is also called a "[[curved sh-map|non-curved sh-map]]".)

=--


+-- {: .num_example #GaugeInvariantFunctionsIntermsOfLieAlgebroids}
###### Example
**([[invariant]] [[functions]] in terms of [[Lie algebroids]])**

Let $\mathfrak{g}$ be a [[super Lie algebra]] equipped with a [[Lie algebra action]] (def. \ref{InfinitesimalActionByLieAlgebra})

$$
  \array{
    \mathfrak{g} \times X && \overset{R}{\longrightarrow} && T X
    \\
    & {}_{\mathllap{pr_2}}\searrow && \swarrow_{\mathrlap{rb}}
    \\
    && X
  }
$$

on a [[supermanifold]] $X$. Then there is a canonical homomorphism of [[Lie algebroids]] (def. \ref{HomomorphismBetweenLieAlgebroids})

$$
  \label{ProjectionMapForActionLieAlgebroid}
  \array{
    X &&& CE(X) &=& C^\infty(X) &\oplus& 0
    \\
    \downarrow^{\mathrlap{p}} 
      &\phantom{AAA}&& 
    \uparrow^{\mathrlap{p^\ast}}
      && 
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{0}}
    \\
    X/\mathfrak{g} 
      &&& 
    CE(X/\mathfrak{g}) 
      &=& 
    C^\infty(X) 
      &\oplus& 
    C^\infty(X) \otimes \wedge^\bullet \mathfrak{g}^\ast
  }
$$

from the manifold $X$ regarded as a Lie algebroid by example \ref{BasicExamplesOfLieAlgebroids} to the [[action Lie algebroid]] $X/\mathfrak{g}$ (example \ref{ActionLieAlgebroid}), which may be called the _[[homotopy quotient]] [[coprojection]] map_. The dual homomorphism of [[differential graded-commutative superalgebras]] is given simply by the identity on $C^\infty(X)$ and the [[zero map]] on $\mathfrak{g}^\ast$.
 
Next regard the [[real line]] [[manifold]] $\mathbb{R}^1$ as a Lie algebroid by example \ref{BasicExamplesOfLieAlgebroids}.
Then homomorphisms of Lie algebroids (def. \ref{HomomorphismBetweenLieAlgebroids}) of the form

$$
  S \;\colon\; X/\mathfrak{g} \longrightarrow \mathbb{R}^1
  \,,
$$

hence _smooth functions on the Lie algebroid_, are equivalently

* ordinary [[smooth functions]] $S \;\colon\; X \longrightarrow \mathbb{R}^1$ on the underlying [[smooth manifold]],

* which are [[invariant]] under the Lie algebra action in that $R(-)(S) = 0$.

In terms of the canonical [[homotopy quotient]] [[coprojection]] map $p$ (eq:ProjectionMapForActionLieAlgebroid) this says that a smooth function on $X$ [[extension]] extends to the [[action Lie algebroid]] precisely if it is [[invariant]]:

$$
  \array{
    X &\overset{S}{\longrightarrow}& \mathbb{R}^1
    \\
    {}^{\mathllap{p}}\downarrow 
      & 
    \nearrow_{ 
      \mathrlap{ 
          \text{exists precisely if} \; S \; \text{is invariant} 
      } 
     }
    \\
    X/\mathfrak{g}
  }
$$

=--


+-- {: .proof}
###### Proof

An $\mathbb{R}$-algebra homomorphism

$$
  CE( X/\mathfrak{g} )
    \overset{S^\ast}{\longleftarrow}
  C^\infty(\mathbb{R}^1)
$$

is fixed by what it does to the canonical [[coordinate function]] $x$ on $\mathbb{R}^1$, which is taken by
$S^\ast$ to $S \in C^\infty(X) \hookrightarrow CE(X/\mathfrak{g})$. For this to be a dg-algebra homomorphism it needs to respect the differentials on both sides. Since the differential on the right is trivial, the condition is that $0 = d_{CE} S = R(-)(f)$:

$$
  \array{
     \left\{ S \right\} 
       &\overset{S^\ast}{\longleftarrow}& 
     \left\{ x \right\}
     \\
     {}^{\mathllap{d_{CE(X/\mathfrak{g})}}}\downarrow 
       && 
     \downarrow^{\mathrlap{d_{CE(\mathbb{R}^1)} = 0 } }
     \\
     \left\{ 
       R(-)(S)
       =
       0
     \right\}
     &\underset{S^\ast}{\longleftarrow}&
     \left\{ 0 \right\}
  }
$$

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
on $Der(CE(\mathfrak{a}))$ being the graded [[commutator]] with the differential $d_{CE(\mathfrak{a})}$ on $CE(\mathfrak{a})$
(which is itself a graded derivation of degree +1):


$$
  \array{
    \mathllap{ d_{CE(T^\ast \mathfrak{a})} }
      &\mathrlap{ \vert_{\mathfrak{a}^\ast} }& 
      &
    \coloneqq & d_{CE(\mathfrak{a})}
  \\
  \mathllap{ d_{CE(T^\ast \mathfrak{a})} }
     & \mathrlap{ \vert_{Der(\mathfrak{a})} } & 
     \phantom{ \vert_{Der(\mathfrak{a})} }
     &
   \coloneqq & [d_{CE(\mathfrak{a})},-]
  }
$$

Just as for ordinary [[cotangent bundles]] (def. \ref{Differential1FormsOnCartesianSpaces}) there is a canonical homomorphism of Lie algebroids (def. \ref{HomomorphismBetweenLieAlgebroids}) from the infinitesimal cotangent Lie algebroid down to the base Lie algebroid:

$$
  \label{CotangentLieAlgebrpoidProjection}
  \array{
    T^\ast \mathfrak{a} 
       &\phantom{AAA}&& 
    CE(T^\ast \mathfrak{g})
     &=&
    CE(\mathfrak{a}) 
      &\oplus& 
    \wedge^{\bullet \geq 1}_{CE(\mathfrak{a})} Der(\mathfrak{a})
    \\
    \downarrow^{\mathrlap{cb}} &&& \uparrow^{\mathrlap{cb^\ast}}
      && \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{0}}
    \\
    \mathfrak{a} 
      &&& 
    CE(\mathfrak{a}) &=& CE(\mathfrak{a}) &\oplus& 0
  }
$$

given dually by the identity on the original generators.

=--


+-- {: .num_example #CotangentBundleOfActionLieAlgebroid}
###### Example
**([[automorphism ∞-Lie algebra|infinitesimal cotangent bundle]] of [[action Lie algebroid]])**

Let $X/\mathfrak{g}$ be an [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid}) whose [[Chevalley-Eilenberg differential]] is given in local coordinates by (eq:DifferentialOnActionLieAlgebroid)

$$
  d_{CE(X/\mathfrak{g})}
  \;=\;
  \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma \frac{\partial}{\partial c^\alpha}
  +
  c^\alpha R_a^\alpha  \frac{\partial}{\partial \phi^a}
  \,.
$$

Then its infinitesimal cotangent Lie algebroid $T^\ast (X/\mathfrak{g})$ (def. \ref{LieAlgebroidInfinitesimalCotangentBundle})
has the generators


$$
  \array{
    &
    \left(
      \frac{\partial}{\partial c^\alpha}
    \right)
    &
    \left(
      \phi^a
    \right)
    ,
    \left(
      \frac{\partial}{\partial \phi^a}
    \right)
    &
    \left(
      c^\alpha
    \right)
    \\
    deg =
    &
    -1
    &
    0
    &
    +1
  }
$$

and we find that CE-differential on the new derivation generators is given by

$$  \label{CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnGhostFieldCoordinates}
  \begin{aligned}
    d_{CE(T^\ast(X/\mathfrak{g}))}
    \left(
      \frac{\partial}{\partial c^\alpha}
    \right)
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
    d_{CE(T^\ast(X/\mathfrak{g}))}
    \left(
      \frac{\partial}{\partial \phi^a}
    \right)
    & \coloneqq
    \left[
      d_{CE(X/\mathfrak{g})},
      \frac{\partial}{\partial \phi^a}
    \right]
    \\
    & =
    -
    c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \frac{\partial}{\partial \phi^b}
  \end{aligned}
  \,.
$$

To amplify that the [[derivations]] _on_ $CE(X/\mathfrak{g})$, such as $\frac{\partial}{\partial \phi^a}$ and $\frac{\partial}{\partial c^\alpha}$, are now [[coordinate functions]] _in_ $CE(T^\ast(X/\mathfrak{g}))$ one writes them as 

$$
  \label{AntiNotationForDerivations}
  \phi^\ddagger_a \;\coloneqq\; \frac{\partial}{\partial \phi^a}
  \phantom{AAAAA}
  c\ddagger_\alpha \;\coloneqq\; \frac{\partial}{\partial c^\alpha}
  \,.
$$

so that the generator content then reads as follows:

$$
  \label{GeneratorsOfDerivedCriticalLocusInActionLieAlgebroid}
  \array{
    &
    \left(
      c^\ddagger_\alpha
    \right)
    &
      \left(
        \phi^a
      \right)
      ,
      \left(
        \phi^\ddagger_a
      \right)
    &
    \left(
      c^\alpha
    \right)
    \\
    deg =
    &
    -1
    &
    0
    &
    +1
  }
  \,.
$$

In this notation the full action of the CE-differential for $T^\ast(X/\mathfrak{g})$ is therefore the following:

$$
  \label{CEDifferentialOnGeneratorsForInfinitesimalCotangentBundleOfActionLieAlgebroid}
  \array{
    & d_{CE(T^\ast(X/\mathfrak{g}))}
    \\
    \phi^a
      &\mapsto&
    c^\alpha R^a_\alpha
    \\
    c^\alpha
      & \mapsto&
    \tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma
    \\
    \phi^\ddagger_a
      &\mapsto&
    - c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \phi^\ddagger_b
    \\
    c^\ddagger_\alpha
      &\mapsto&
    R_\alpha^a  \phi^\ddagger_a
      +
    \gamma^\beta{}_{\alpha \gamma} c^\gamma c^\ddagger_\beta
  }
$$


=--

With a concept of [[cotangent bundles]] for [[Lie algebroids]] in hand, we want to see next that their [[sections]] are [[differential 1-forms]] on a [[Lie algebroid]] in an appropriate sense:

+-- {: .num_prop #ExteriorDifferentialOfGaugeInvariantFunctionIsSectionOfInfinitesimalCotangentLieAlgebroid}
###### Proposition
**([[exterior differential]] of [[invariant]] function is [[section]] of [[automorphism ∞-Lie algebra|infinitesimal cotangent bundle]])**

For $\mathfrak{a}$ a [[Lie ∞-algebroid]] (def. \ref{LInfinityAlgebroid}) over some $X$;
and $S \;\colon\;\mathfrak{a} \longrightarrow \mathbb{R}$ a [[invariant]] smooth function on it (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids})
there is an induced [[section]] $d S$ of the infinitesimal cotangent Lie algebroid (def. \ref{LieAlgebroidInfinitesimalCotangentBundle})
bundle projection (eq:CotangentLieAlgebrpoidProjection):

$$
  \array{
    && T^\ast \mathfrak{a}
    \\
    & {}^{\mathllap{d S}}\nearrow & \downarrow^{\mathrlap{cb}}
    \\
    \mathfrak{a}
    &=&
    \mathfrak{a}
  }
  \,,
$$

given dually by the [[homomorphism]] of [[differential graded-commutative superalgebras]]

$$
  (d S)^\ast \;\colon\; CE(T^\ast \mathfrak{a}) \longrightarrow CE(\mathfrak{a})
$$

which sends

1. the generators in $\mathfrak{a}^\ast$ to themselves;

1. a [[vector field]] $v$ on $X$, regarded as a degree-0 [[derivation]] to
   $d S(v) = v(S) \in C^\infty(X)$;

1. all other derivations to zero.


=--

+-- {: .proof}
###### Proof

We discuss the proof in the special case that $\mathfrak{a} = X/\mathfrak{g}$ is an [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid}) hence where $T^\ast(\mathfrak{a}) = T^\ast(X/\mathfrak{g})$ is as in example \ref{CotangentBundleOfActionLieAlgebroid}. The general case is directly analogous.

Since $(d S)^\ast$ has been defined on generators, it is uniquely a homomorphism of graded algebras.
It is clear that if $(d S)^\ast$ is indeed a [[homomorphism]] of [[differential graded-commutative superalgebras]] in that it also respects the CE-differentials, then it yields a section as claimed, because by definition it is the identity on $\mathfrak{a}^\ast$. 
Hence all we need to check is that $(d S)^\ast$ indeed respects the CE-differentials.

On the original generators in $\mathfrak{a}^\ast$ this is immediate, since on these the CE-differential on both sides are by definition the same.

On the derivation $\phi^\ddagger_a \coloneqq \frac{\partial}{ \partial \phi^a}$ we find from (eq:CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnFieldCoordinates)

$$
  \array{
    \left\{
       \frac{\partial S}{\partial \phi^a}
    \right\}
      &\overset{(d S)^\ast}{\longleftarrow}&
    \left\{ \phi^\ddagger_a \right\}
    \\
    {}^{\mathllap{d_{CE(X/\mathfrak{g})}}}\downarrow 
      && 
    \downarrow^{\mathrlap{d_{CE(T^\ast (X/\mathfrak{g}))}}}
    \\
    \left\{
       -c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \frac{\partial S}{\partial \phi^b}
    \right\}
      &\underset{(d S)^\ast}{\longleftarrow}&
    \left\{
       -c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \phi^\ddagger_b
    \right\}
  }
$$

{#NoticeThatTheLeftVerticalMap} Notice that the left vertical map is indeed as shown, due to the invariance of $S$ (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids}), which allows an "[[integration by parts]]":

$$
  \begin{aligned}
    d_{CE(X/\mathfrak{g})}\left( \frac{\partial S}{\partial \phi_a} \right)
    & =
    c^\alpha R_\alpha^{b} \frac{\partial}{\partial \phi^b} \frac{\partial}{\partial \phi^a} S
    \\
    & =     
    \frac{\partial}{\partial \phi^a}
    \left(
      c^\alpha 
      \underset{
        = 0
      }{
      \underbrace{
        R_\alpha^b \frac{\partial S}{\partial \phi^b}  
      }
      }
    \right)
    \;-\;
    c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a}
    \frac{\partial S}{\partial \phi^b}
  \end{aligned}
$$

Similarly, on the derivation $c^\ddagger_\alpha \coloneqq \frac{\partial}{\partial c^\alpha}$ we find from (eq:CotangentLieAlgebroidDifferentialForActionLieAlgebroidOnGhostFieldCoordinates) and using the invariance of $S$ (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids})

$$
  \array{
    \left\{
      0
    \right\}
      &\overset{(d S)^\ast}{\longleftarrow}&
    \left\{
      c^\ddagger_\alpha
    \right\}
    \\
    {}^{\mathllap{d_{CE(X/\mathfrak{g})}}}\downarrow 
      && 
    \downarrow^{\mathrlap{d_{CE(T^\ast(X/\mathfrak{g}))}}}
    \\
    \left\{
      0 = R_\alpha^a \frac{\partial S}{\partial \phi^a}
    \right\}
      &\underset{(d S)^\ast}{\longleftarrow}&
    \left\{
      R_\alpha^a  \phi^\ddagger_a
      +
      \gamma^\beta{}_{\alpha \gamma} c^\gamma 
      c^\ddagger_\alpha
    \right\}
  }
  \,.
$$

This shows that the differentials are being respected.

=--

Next we describe the [[vanishing locus]] of $d S$, hence the [[critical locus]] of $S$. Notice that if $d S$ is regarded as an ordinary [[differential 1-form]] on an ordinary [[smooth manifold]] $X$, then its ordinary [[vanishing locus]] 

$$
  X_{d S = 0}
  \;=\;
  \left\{
     x \in X \;\vert\;
     d S(x) = 0
  \right\}
$$ 

is simply the [[fiber product]] of $d S$ with the [[zero section]] of the [[cotangent bundle]], hence the [[universal property|universal]] space that  makes the following [[commuting diagram|diagram commute]]:

$$
  \array{
    X_{d S = 0}
      &\overset{\phantom{AAA}}{\hookrightarrow}&
    X
    \\
    \downarrow && \downarrow^{\mathrlap{0}}
    \\
    X &\underset{d S}{\longrightarrow}& T^\ast X
  }
  \,.
$$

This is just the [[category theory|general abstract]] way to express the [[equation]] $d S = 0$.

In this [[category theory|general abstract]] form the concept of [[critical locus]] generalizes to [[invariant]] functions on [[super L-infinity algebra|super]] [[Lie algebroids]], where the vanishing of $d S$ is regarded only  _up to [[homotopy]]_, namely up to [[infinitesimal symmetry]] transformations by the [[Lie algebra]] $\mathfrak{g}$. In this [[homotopy theory|homotopy-theoretic]] refinement we speak of the _[[derived critical locus]]_. The following definition simply states what this comes down to in components. For a detailed derivation see at _[[derived critical locus]]_ and for general introduction to [[higher differential geometry]] and [[higher Lie theory]] see at _[[schreiber:Higher Structures|Higher structures in Physics]]_.

+-- {: .num_defn #DerivedCriticalLocusOfGaugeInvariantFunctionOnLieAlgebroid}
###### Definition
**([[derived critical locus]] of [[invariant]] function on [[Lie ∞-algebroid]])**

Let $\mathfrak{a}$ be a [[Lie ∞-algebroid]] (def. \ref{LInfinityAlgebroid}) over some $X$, let

$$
  S \;\colon\; \mathfrak{a} \longrightarrow \mathbb{R}
$$

be an [[invariant]] function (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids}) and consider
the [[section]] of its infinitesimal [[cotangent bundle]] $T^\ast \mathfrak{a}$ (def. \ref{CotangentBundleOfActionLieAlgebroid}) corresponding to its exterior derivative
via prop. \ref{ExteriorDifferentialOfGaugeInvariantFunctionIsSectionOfInfinitesimalCotangentLieAlgebroid}:

$$
  \array{
    \mathfrak{a} && \overset{d S}{\longrightarrow} && T^\ast \mathfrak{a}
    \\
    & {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{cb}}
    \\
    && \mathfrak{a}
  }
$$

Then the _[[derived critical locus]]_ of $S$ is the [[derived Lie algebroid]] (def. \ref{LInfinityAlgebroid})
to be denoted $\mathfrak{a}_{d S \simeq 0}$ which is the [[homotopy pullback]] of the section $d S$ along the [[zero section]]:

$$
  \array{
    \mathfrak{a}_{d S \simeq 0}
      &\longrightarrow&
    \mathfrak{a}
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{0}}
    \\
    \mathfrak{a}
      &\underset{d S}{\longrightarrow}&
    T^\ast \mathfrak{a}
  }
  \,.
$$

This means equivalently (details are at _[[derived critical locus]]_) that the Chevalley-Eilenberg algebra of $\mathfrak{a}_{d S \simeq 0}$ is like that of the infinitesimal cotangent Lie algebroid $T^\ast \mathfrak{a}$ (def. \ref{LieAlgebroidInfinitesimalCotangentBundle}) except for two changes:

1. all [[derivations]] are shifted down in degree by one;

1. the CE-differential on the derivations coming from vector fields $v$ on $X$ is that of the infinitesimal cotangent Lie algebroid $T^\ast \mathfrak{a}$ plus $d S(v) = v(S)$.


=--

We now make the general concept of [[derived critical locus]] inside an [[L-∞ algebroid]] (def. \ref{DerivedCriticalLocusOfGaugeInvariantFunctionOnLieAlgebroid}) explicit in our running example of an [[action Lie algebroid]]; the reader not concerned with the general idea of [[homotopy pullbacks]] may consider the following example as the definition of derived critical locus for the purposes of our running examples:

+-- {: .num_example #ArchetypeOfBVBRSTComplex}
###### Example
**([[derived critical locus]] inside [[action Lie algebroid]])**

Consider an [[invariant]] function (def. \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids})
on an [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid})


$$
  S \;\colon\; X/\mathfrak{g} \overset{\phantom{AAA}}{\longrightarrow} \mathbb{R}
$$ 

for the case that the underlying [[supermanifold]] $X$ is a [[super Cartesian space]] (def. \ref{SuperCartesianSpace}) with global [[coordinates]] $(\phi^a)$ as in example \ref{CotangentBundleOfActionLieAlgebroid}. Then the [[derived critical locus]] (def. \ref{DerivedCriticalLocusOfGaugeInvariantFunctionOnLieAlgebroid})

$$
  (X/\mathfrak{g})_{d S \simeq 0}
$$ 

is, in terms of its [[Chevalley-Eilenberg algebra]] $CE\left(  (X/\mathfrak{g})_{d S \simeq 0} \right)$ (def. \ref{LInfinityAlgebroid}) given as follows:

Its generators are those of $CE\left( T^\ast(X/\mathfrak{g}) \right)$ as in (eq:GeneratorsOfDerivedCriticalLocusInActionLieAlgebroid), except for a shift of degree of the [[derivation]]-generators down by one:

$$
  \array{
    &
    \left(
      c^\ddagger_{\alpha}
    \right)
    &
    \left(
      \phi^\ddagger_a
    \right)
    &
    \left(
      \phi^a
    \right)
    &
    \left(
      c^\alpha
    \right)
    \\
    deg = &
    -2
    &
    -1
    &
    0
    &
    +1
  }
$$

Moreover, on these generators the CE-differential is given by

$$
  \label{ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid}
  \array{
    & d_{CE\left((X/\mathfrak{g})_{d S \simeq 0}\right)}
    \\
    \phi^a
      &\mapsto&
    c^\alpha R^a_\alpha
    \\
    c^\alpha
      & \mapsto&
    \tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma
    \\
    \phi^\ddagger_a
      &\mapsto&
    \underset{
      new
    }{
    \underbrace{
      \frac{\partial S}{\partial \phi^a}
    }}
    -
    c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \phi^\ddagger_b
    \\
    c^\ddagger_\alpha
      &\mapsto&
    R_\alpha^a  \phi^\ddagger_a
      +
    \gamma^\beta{}_{\alpha \gamma} c^\gamma c^\ddagger_b
  }
$$

which is just the expression for the differential (eq:CEDifferentialOnGeneratorsForInfinitesimalCotangentBundleOfActionLieAlgebroid) in $CE\left( T^\ast(X/\mathfrak{g}) \right)$  from example \ref{CotangentBundleOfActionLieAlgebroid}, except for the fact that (the derivations are shifted down in degree and) the new term $\frac{\partial S}{\partial \phi^a}$ over the brace.

=--

The following example illustrates how the concept of [[derived critical locus]] $X_{d S \simeq 0}$ of $S$ is a [[homotopy theory|homotopy theoretic]] version of the ordinary concept of [[critical locus]] $X_{d S = 0}$:


+-- {: .num_example #OrdinaryCriticalLocusAsCohomologyOfDerivedCriticalLocus}
###### Example
**(ordinary [[critical locus]] is [[cochain cohomology]] of [[derived critical locus]] in degree 0)**

Let $X$ be an [[superpoint]] (def. \ref{SuperCartesianSpace}) or more generally the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of a point in a [[super Cartesian space]] (def. \ref{SuperCartesianSpace}) with [[coordinate functions]] $(\phi^a)$, so that its [[algebra of functions]] $C^\infty(X)$ is a truncated [[polynomial algebra]] or [[formal power series algebra]] in the [[variables]] $\phi^a$.

Consider for simplicity the special case that $\mathfrak{g} = 0$ so that there is no [[Lie algebra action]] on $X$.

Then the [[Chevalley-Eilenberg algebra]] of the [[derived critical locus]] $X_{d S \simeq 0}$ of $S$ (example \ref{ArchetypeOfBVBRSTComplex}) has generators

$$
  \array{
    &
    &
    \left(
      \phi^\ddagger_a
    \right)
    &
    \left(
      \phi^a
    \right)
    &
    \\
    deg = &
    &
    -1
    &
    0
    &
  }
$$

and [[differential]] given by

$$
  \array{
     & d_{CE\left( X_{d S \simeq 0} \right)}
     \\
     \phi^a &\mapsto& 0
     \\
     \phi^\ddagger_a &\mapsto& \frac{\partial S}{\partial \phi^a}
  }
  \,.
$$

Hence the [[cochain cohomology]] of the [[Chevalley-Eilenberg algebra]] of the derived critical locus indegree 0 is the [[quotient]] of $C^\infty(X)$ by the ideal which is generated by $\left( \frac{\partial S}{\partial \phi^a} \right)$

$$
  H^0\left( 
     CE\left( X_{d S \simeq 0}  \right)
  \right)
  \;=\;
  C^\infty(X)/\left( \frac{\partial S}{\partial \phi^a} \right)
  \,.
$$

But under the assumption that $X$ is a [[superpoint]] or [[infinitesimal neighbourhood]] of a point, this quotient algebra is just the [[algebra of functions]] on the ordinary  [[critical locus]] $X_{d S = 0}$. 

(The quotient says that every function on $X$ which vanishes where $\frac{\partial S}{\partial \phi^a}$ vanishes is [[zero]] in the quotient. This means that the quotient algebra consists of the functions on $X$ modulo the [[equivalence relation]] that identifies two if they agree on the critical locus $X_{d S = 0}$, which is the functions on $X_{d S = 0}$.)

Hence the [[derived critical locus]] yields the ordinary [[critical locus]] in [[cochain cohomology]]:

$$
  H^0\left(
   CE\left( X_{d S \simeq 0} \right)
  \right)
  \;\simeq\;
  C^\infty\left( X_{d S = 0} \right)
  \,.
$$

However, it is not in general the case that the [[derived critical locus]] is a [[resolution]] of the ordinary [[critical locus]], in that all its cohomology in [[negative number|negative]] degree vanishes. Instead, the cohomology of the [[Chevalley-Eilenberg algebra]] of a [[derived critical locus]] in [[negative number|negative]] degree detects [[Lie algebra action]] and more generally [[L-∞ algebra action]] on $X$ under which $S$ is invariant. If this action is incorporated into $X$ by bassing to the [[action Lie algebroid]] by passing to the [[action Lie algebroid]] $X/\mathfrak[g}$ and then forming the [[derived critical locus]] $(X/\mathfrak{g})_{d S \simeq 0}$ in there, as in example \ref{ArchetypeOfBVBRSTComplex}. 

This issue we discuss in detail in the chapter _[Gauge fixing](#GaugeFixing)_, see prop. \ref{BVComplexIsHomologicalResolutionPreciselyIfNoNonTrivialImplicitGaugeSymmetres} below.

=--

In order to generalize the statement of example \ref{OrdinaryCriticalLocusAsCohomologyOfDerivedCriticalLocus} to the case that a [[Lie algebra action]] is taken into account, we need to realize the [[Chevalley-Eilenberg algebra]] of a [[derived critical locus]] in a [[Lie algebroid]] is the [[total complex]] of a [[double complex]]:

spring

$\,$

**[[Schouten bracket]]/[[antibracket]]**
 {#SchoutenBracketAntibracket}

Since the infinitesimal cotangent Lie algebroid $T^\ast \mathfrak{a}$ has function algebra given by tensor products of [[tangent vector fields]]/[[derivations]], we expect that a graded analogue of the [[Lie bracket]] of ordinary [[tangent vector fields]] exists on the [[Chevalley-Eilenberg algebra]] $CE\left( T^\ast \mathfrak{a}\right)$. This is indeed the case, and crucial for the theory:

+-- {: .num_defn #SchoutenBracketAndAntibracket}
###### Definition
**([[Schouten bracket]] and [[antibracket]] for [[action Lie algebroid]])**

Consider a [[derived critical locus]] $(X/\mathfrak{g})_{d S \simeq 0}$ inside an [[action Lie algebroid]] $X/\mathfrak{g}$ as in example \ref{ArchetypeOfBVBRSTComplex}.

Then the graded [[commutator]] of graded [[derivations]] of the [[Chevalley-Eilenberg algebra]] of $X/\mathfrak{g}$

$$
  [-,-]
  \;\colon\;
   Der(CE(X/\mathfrak{g})) 
    \otimes 
   Der(CE(X/\mathfrak{g})) 
    \longrightarrow
   Der(CE(X/\mathfrak{g})) 
$$

uniquely [[extension|extends]], by the graded [[Leibniz rule]], to a graded bracket of degree $(1,even)$ on the CE-algebra of the [[derived critical locus]] $(X/\mathfrak{g})_{d S \simeq 0}$

$$
  \left\{ -,-\right\}
    \;\colon\;
   CE\left( (X/\mathfrak{g})_{d S \simeq 0} \right) 
    \otimes 
   C\left( (X/\mathfrak{g})_{d S \simeq 0} \right)
    \longrightarrow
   CE\left( (X/\mathfrak{g})_{d S \simeq 0} \right)
$$

such that this is a graded [[derivation]] in both arguments.

This is called the _[[Schouten bracket]]_.

There is an elegant way to rewrite this in terms of components: With the notation (eq:AntiNotationForDerivations) for the coordinate-derivations the [[Schouten bracket]] is equivalently given by

$$
  \label{Antibracket}
  \begin{aligned}
    \left\{ f,g \right\}  
    & =
    \phantom{+}
    \frac{\overset{\leftarrow}{\partial} f}{\partial \phi^\ddagger_a}  
    \frac{\overset{\rightarrow}{\partial} g}{\partial {\phi}^a}
    -
    \frac{\overset{\leftarrow}{\partial} f}{\partial \phi^a}
    \frac{\overset{\rightarrow}{\partial} g}{\partial \phi^\ddagger_a} 
    \\
    &
    \phantom{=}
    + 
    \frac{\overset{\leftarrow}{\partial} f}{\partial c^\ddagger_\alpha}  
    \frac{\overset{\rightarrow}{\partial} g}{\partial {c}^\alpha}
    -
    \frac{\overset{\leftarrow}{\partial} f}{\partial c^\alpha}
    \frac{\overset{\rightarrow}{\partial} g}{\partial c^\ddagger_\alpha} 
  \end{aligned}
  \,,
$$

where the arrow over the [[partial derivative]] indicates that we we pick up signs via the [[Leibniz rule]] either as usual, going through products from left to right (for $\overset{\rightarrow}{\partial}$) or by going through the products from right to left (for $\overset{\leftarrow}{\partial}$).


In this form the [[Schouten bracket]] is called the _[[antibracket]]_.

=--

The great power of the [[Schouten bracket]]/[[antibracket]] rests in the fact that it makes the [[Chevalley-Eilenberg differential]] on a [[derived critical locus]] $(X/\mathfrak{g})_{d S \simeq 0}$ become a [[Hamiltonian vector field]], for "[[Hamiltonian]]" the sum of $S$ with the [[Chevalley-Eilenberg differential]] of $X/\mathfrak{g}$:

+-- {: .num_example #ChevalleyEilenbergDifferentialOnDerivedCriticalLocusIsHamiltonianViaAntibracket}
###### Example
**([[Chevalley-Eilenberg differential]] of [[derived critical locus]] is [[Hamiltonian vector field]] for the [[Schouten bracket]]/[[antibracket]])**

Let $(X/\mathfrak{g})_{d S \simeq 0}$ be a [[derived critical locus]] inside an [[action Lie algebroid]] as in example \ref{ArchetypeOfBVBRSTComplex}. 

Then the CE-differential (eq:ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid) of the [[derived critical locus]] $X/\mathfrak{g}\vert_{S \simeq 0}$ is simply the [[Schouten bracket]]/[[antibracket]] (def. \ref{SchoutenBracketAndAntibracket}) with the [[sum]] of the CE-differential of $X/\mathfrak{g}$ and the function $-S$:

$$
  d_{CE\left( (X/\mathfrak{g})_{d S \simeq 0} \right) }(-)
  \;=\;
  \left\{
    - S + d_{CE(X/\mathfrak{g})}
    \,,\,
    (-)
  \right\}
  \,.
$$

In coordinates, using the expression for $d_{CE(X/\mathfrak{g})}$ from (eq:DifferentialOnActionLieAlgebroid) and using the notation for derivations from (eq:AntiNotationForDerivations) this means that 

$$
  d_{CE\left( (X/\mathfrak{g})_{d S \simeq 0} \right)}(-)
  \;=\;
  \left\{
     - S 
     +
     c^\alpha R_\alpha^a \phi^\ddagger_a
      -
     \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma 
     c^\ddagger_\alpha
     \,,\,
     (-)
  \right\}
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is a simple straightforward computation, but we spell it out for illustration of the general principle. The result is to be compared with (eq:ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid):

for $\phi^a$:

$$
  \begin{aligned}
  \left\{
     - S 
     +
     c^\alpha R_\alpha^{a'} \phi^\ddagger_{a'}
      -
     \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma 
     c^\ddagger_\alpha
     \,,\,
     \phi^a
  \right\}
  &
  =
  \left\{
   c^\alpha R_\alpha^{a'} \phi^\ddagger_{a'} \,,\, \phi^a
  \right\}
  \\
  & =
  c^\alpha R_\alpha^{a'} 
  \underset{
    \delta_{a'}^a
  }{
  \underbrace{
  \left\{
   \phi^\ddagger_{a'} \,,\, \phi^a
  \right\}
  }
  }
  \\
  & =
  c^\alpha R_\alpha^{a}
  \end{aligned}
$$

for $c^\alpha$:

$$
  \begin{aligned}
  \left\{
     - S 
     +
     c^\alpha R_\alpha^{a} \phi^\ddagger_{a}
      -
     \tfrac{1}{2}\gamma^{\alpha'}{}_{\beta \gamma} c^\beta c^\gamma 
     c^\ddagger_{\alpha'}
     \,,\,
     c^\alpha
  \right\}
  & =
  \left\{
     \tfrac{1}{2}\gamma^{\alpha'}{}_{\beta \gamma} c^\beta c^\gamma 
     c^\ddagger_{\alpha'}
     \,,\,
     c^\alpha
  \right\}
  \\
  & =
  \tfrac{1}{2}\gamma^{\alpha'}{}_{\beta \gamma} c^\beta c^\gamma 
  \underset{
    \delta_{\alpha'}^\alpha
  }{
  \underbrace{
  \left\{
     c^\ddagger_{\alpha'}
     \,,\,
     c^\alpha
  \right\}
  }
  }
  \\
  & =
  \tfrac{1}{2}\gamma^{\alpha}{}_{\beta \gamma} c^\beta c^\gamma 
  \end{aligned}
$$

for $\phi^\ddagger_a$:

$$
  \begin{aligned}
  \left\{
     - S 
     +
     c^\alpha R_\alpha^{a'} \phi^\ddagger_{a'}
      -
     \tfrac{1}{2}\gamma^{\alpha}{}_{\beta \gamma} c^\beta c^\gamma 
     c^\ddagger_{\alpha}
     \,,\,
     \phi^\ddagger_a
  \right\}
  & =
  -
  \underset{
   = -\frac{\partial S}{\partial \phi^a}
  }{
  \underbrace{
  \left\{
    S \,,\, \phi^{\ddagger}_a
  \right\}
  }
  }
  +
  \left\{
    c^\alpha R_\alpha^{a'} \phi^\ddagger_{a'}
    \,,\,
    \phi^\dagger_a
  \right\}
  \\
  & =
  \frac{\partial S}{\partial \phi^a}
   + c^\alpha 
    \underset{
      = -\frac{\partial R_\alpha^{a'}}{\partial \phi^a}
    }{
    \underbrace{
      \left\{ R_\alpha^{a'} \,,\, \phi^\ddagger_a \right\} 
    }
    }
   \phi^\ddagger_{a'}
  \\
  & =
   \frac{\partial S}{\partial \phi^a}
   -
   c^\alpha \frac{\partial R_\alpha^{a'}}{\partial \phi^a}
   \phi^\ddagger_{a'}
  \end{aligned}
$$

for $c^\ddagger_\alpha$:

$$
  \begin{aligned}
  \left\{
     - S 
     +
     c^{\alpha'} R_{\alpha'}^{a} \phi^\ddagger_{a}
      -
     \tfrac{1}{2}\gamma^{\alpha'}{}_{\beta \gamma} c^\beta c^\gamma 
     c^\ddagger_{\alpha'}
     \,,\,
     c^\ddagger_\alpha
  \right\}
  & =
  \left\{ 
    c^{\alpha'} R_{\alpha'}^a \phi^{\ddagger}_a
    \,,\,
    c^\ddagger_{\alpha}
  \right\}
  \;+\;
  \left\{
    \tfrac{1}{2} \gamma^{\alpha'}{}_{\beta \gamma} c^\beta c^\gamma 
    c^\ddagger_{\alpha'}
    \,,\,
    c^\ddagger_\alpha
  \right\}
  \\
  & =
  \left\{ 
    c^{\alpha'} 
    \,,\,
    c^\ddagger_{\alpha}
  \right\}
  R_{\alpha'}^a \phi^{\ddagger}_a
  \;-\;
  \tfrac{1}{2} \gamma^{\alpha'}{}_{\beta \gamma} 
  \underset{ = c^\beta \delta_{\alpha}^\gamma - \delta_{\alpha}^\beta c^\gamma}{
  \underbrace{
  \left\{
    c^\beta c^\gamma 
    \,,\,
    c^\ddagger_\alpha
  \right\}
  }}
  c^\ddagger_{\alpha'}
  \\
  & = 
  R_\alpha^a \phi^\ddagger_{a}
  +
  \gamma^{\alpha'}{}_{\alpha \gamma} c^\gamma c^\ddagger_{\alpha'}
  \end{aligned}
$$

Hence these values of the [[Schouten bracket]]/[[antibracket]] indeed all agree with the values of the CE-differential from (eq:(eq:ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid)).


=--

$\,$

Next we turn to applying these considerations about [[derived critical loci]] to [[Lagrangian densities]] defined on the [[homotopy quotient]] of a [[jet bundle]] by [[infinitesimal gauge symmetries]]. 

$\,$

**[[derived critical locus]] on [[jet bundle]] -- the [[local BV-BRST complex]]**
  {#DerivedCriticalLocusOnJetBundle}

If we think of the function $S$ as being the [[action functional]] (example \ref{ActionFunctional})
of a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) over a [[compact space|compact]] [[spacetime]] $\Sigma$,
with $X$ the  [[space of field histories]] (or rather an [[infinitesimal neighbourhood]] therein),
hence with $\mathfrak{g}$ a Lie algebra of [[gauge symmetries]] acting on the field histories, then
the [[Chevalley-Eilenberg algebra]] $CE\left((X/\mathfrak{g})_{d S \simeq 0}\right)$ of the [[derived critical locus]] of $S$ is called the
_[[BV-BRST complex]]_ of the theory.


In applications of interest, the spacetime $\Sigma$ is _not_ [[compact space|compact]].
In that case one may still appeal to a construction on the [[space of field histories]]
as in example \ref{ArchetypeOfBVBRSTComplex} by considering the action functional for all
[[adiabatic switching|adiabatically switched]] $b \mathbf{L}$ Lagrangians, with $b \in C_{cp}^\infty(\Sigma)$.
This approach is taken in ([Fredenhagen-Rejzner 11a](BV-BRST+formalism#FredenhagenRejzner11a)).

Here we instead consider now the "local lift" or "de-transgression" of the above construction from the
[[space of field histories]] to the [[jet bundle]] of the field bundle of the theory, refining the
[[BV-BRST complex]] to the _[[local BV-BRST complex]]_, corresponding to the [[local BRST complex]] from example \ref{LocalOffShellBRSTComplex} ([Barnich-Brandt-Henneaux 00](local+BRST+cohomology#BarnichBrandtHenneaux00)).

This requires a slight refinement of the construction that leads to example \ref{ArchetypeOfBVBRSTComplex}:
In contrast to the [[action functional]] $S = \tau_\Sigma(g\mathbf{L})$ (example \ref{ActionFunctional}),
the [[Lagrangian density]] $\mathbf{L}$ is not strictly _invariant_ under [[infinitesimal gauge transformations]], in general,
rather it may change up to a horizontally exact term (by the very definition \ref{GaugeParameters}). The same is then true, in general, for its
[[Euler-Lagrange variational derivative]] $\delta_{EL} \mathbf{L}$ (unless we have already restricted to the [[shell]], by prop. \ref{InfinitesimalSymmetriesOfLagrangianAreAlsoSymmetriesOfTheEquationsOfMotion}). This means that $\delta_{EL} \mathbf{L}$
is, [[off-shell]], not a section of the infinitesimal cotangent bundle (def. \ref{LieAlgebroidInfinitesimalCotangentBundle}) of the
gauge action Lie algebroid on the jet bundle. But it turns out that it still is a section of local refinement of the cotangent bundle, which is twisted by horizontally exact terms. This is what we now describe.

The following definition \ref{LocalInfinitesimalCotangentLieAlgebroid} is the local refinement of
def. \ref{LieAlgebroidInfinitesimalCotangentBundle}:

+-- {: .num_defn #LocalInfinitesimalCotangentLieAlgebroid}
###### Definition
**(local infinitesimal cotangent Lie algebroid)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over some [[spacetime]] $\Sigma$, and let $\mathcal{G} \overset{gb}{\to} \Sigma$ be
a bundle of [[gauge parameters]] (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) which are closed (def. \ref{GaugeParametersClosed}),
inducing via example \ref{LocalOffShellBRSTComplex} the [[Lie algebroid]]

$$
  E / ( \mathcal{G} \times_\Sigma T \Sigma )
  \;=\;
  \left(
    J^\infty_\Sigma( E \times_\Sigma (\mathcal{G}[1]) )
    ,
    s_{BRST} )
  \right)
$$

whose [[Chevalley-Eilenberg algebra]] is the [[local BRST complex]] of the field theory.

Consider the case that both the [[field bundle]] $E \overset{fb}{\to} \Sigma$ (def. \ref{FieldsAndFieldBundles})
as well as the [[gauge parameter]] bundle $\mathcal{G} \overset{gb}{\to} \Sigma$ are [[trivial vector bundles]]
(example \ref{TrivialVectorBundleAsAFieldBundle}) over [[Minkowski spacetime]]
with [[field (physics)|field]] coordinates $(\phi^a)$ and [[gauge parameter]] coordinates $(c^\alpha)$.

Then the vertical infinitesimal cotangent Lie algebroid (def. \ref{LieAlgebroidInfinitesimalCotangentBundle}) has
coordinates as in (eq:GeneratorsOfDerivedCriticalLocusInActionLieAlgebroid) as well as all the corresponding jets
and including also the horizontal differentials:

$$
  \array{
    &
    \left(
      \overline{c}_{\alpha,\mu_1 \cdots \mu_k}
    \right)
    &
      \left(
        \phi^a_{,\mu_1 \cdots \mu_k}
      \right)
      ,
      \left(
        \overline{\phi}_{a,\mu_1 \cdots \mu_k}
      \right)
    &
    \left(
      c^\alpha_{,\mu_1 \cdots \mu_k}
    \right),
    \left(
      d x^\mu
    \right)
    \\
    deg =
    &
    -1
    &
    0
    &
    +1
  }
  \,.
$$

Recall the global [[antibracket]] on an [[action Lie algebroid]] from def. \ref{SchoutenBracketAndAntibracket}. On the jet bundle we consider the following modification:

$$
  \label{LocalCommutatorOfDerivationsOnJetBundle}
  \begin{aligned}
    \left\{
      f dvol_\Sigma,
      g
    \right\}
    & \coloneqq
    \phantom{+ (-1)^{\vert f \vert + (p+1)}}
    \left(
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \left(
        \frac{\delta_{EL} f}{\delta \phi^a}
      \right)
    \right)
    \left(
      \frac{\partial g}{\partial \overline{\phi}_{a,\mu_1 \cdots \mu_k}}
    \right)
    -
    \left(
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \left(
        \frac{\delta_{EL} f}{\delta \overline{\phi}_a}
      \right)
    \right)
    \left(
      \frac{\partial g}{\partial \phi^a_{,\mu_1 \cdots \mu_k}}
    \right)
    \\
    &
    \phantom{=} + (-1)^{\vert f \vert + (p+1)}
    \left(
    \left(
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \left(
        \frac{\delta_{EL} f}{\delta c^\alpha}
      \right)
    \right)
    \left(
      \frac{\partial g}{\partial \overline{c}_{\alpha,\mu_1 \cdots \mu_k}}
    \right)
    -
    \left(
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \left(
        \frac{\delta_{EL} f}{\delta \overline{c}_\alpha}
      \right)
    \right)
    \left(
      \frac{\partial g}{\partial c^\alpha_{,\mu_1 \cdots \mu_k}}
    \right)
    \right)
  \end{aligned}
$$

where $\frac{\delta_{EL}}{\delta \phi^a}$ denotes the [[Euler-Lagrange variational derivative]] (eq:EulerLagrangeEquationGeneral) ([Barnich-Henneaux 96 (2.12)-(2.13)](local+BRST+cohomology#BarnichHenneaux96)).



We define the CE-differential on functions on $T^\ast( E/(\mathcal{G} \times_\Sigma T \Sigma) )$ to be

$$
  d_{CE(T^\ast_\Sigma( E/(\mathcal{G} \times_\Sigma T \Sigma) ))}
  \;\coloneqq\;
  \left\{
    s_{BRST} dvol_\Sigma, -
  \right\}
$$

This defines an $L_\infty$-algebroid to be denoted

$$
  T^\ast_\Sigma( E/(\mathcal{G} \times_\Sigma T \Sigma) )
  \,.
$$

=--

The local refinement of prop. \ref{ExteriorDifferentialOfGaugeInvariantFunctionIsSectionOfInfinitesimalCotangentLieAlgebroid} is now this:

+-- {: .num_prop #EulerLagrangeFormIsSectionOfLocalCotangentBundleOfJetBundleGaugeActionLieAlgebroid}
###### Proposition
**([[Euler-Lagrange form]] is [[section]] of local cotangent bundle of [[jet bundle]] [[gauge symmetry|gauge]]-[[action Lie algebroid]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over some [[spacetime]] $\Sigma$, and let $\mathcal{G} \overset{gb}{\to} \Sigma$ be
a bundle of closed irreducible [[gauge parameters]] (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}),
inducing via example \ref{LocalOffShellBRSTComplex} the [[Lie algebroid]] $E / ( \mathcal{G} \times_\Sigma T \Sigma )$
and via def. \ref{LocalInfinitesimalCotangentLieAlgebroid} its local cotangent [[Lie ∞-algebroid]]
$T^\ast_\Sigma(E / ( \mathcal{G} \times_\Sigma T \Sigma ))$.

Then the [[Euler-Lagrange variational derivative]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) constitutes
a [[section]] of the local cotangent Lie ∞-algebroid (def. \ref{LocalInfinitesimalCotangentLieAlgebroid})

$$
  \array{
    && T^\ast_\Sigma\left( E/(\mathcal{G} \times_\Sigma T \Sigma) \right)
    \\
    & {}^{\mathllap{ \delta_{EL} \mathbf{L} }}\nearrow & \downarrow^{\mathrlap{cb}}
    \\
    E/(\mathcal{G} \times_\Sigma T \Sigma)
    &=&
    E/(\mathcal{G} \times_\Sigma T \Sigma)
  }
$$

given dually

$$
  CE(E/(\mathcal{G} \times_\Sigma T\Sigma))
    \overset{(\delta_{EL}\mathbf{L})^\ast}{\longleftarrow}
  CE(T^\ast(E/(\mathcal{G}\times_\Sigma T \Sigma)))
$$

by

$$
  \array{
    \left\{
      \phi^a_{,\mu_1 \cdots \mu_k}
    \right\}
      &\longleftarrow&
    \left\{
      \phi^a_{,\mu_1 \cdots \mu_k}
    \right\}
    \\
    \left\{
      c^\alpha_{,\mu_1 \cdots \mu_k}
    \right\}
      &\longleftarrow&
    \left\{
      c^\alpha_{,\mu_1 \cdots \mu_k}
    \right\}
    \\
    \left\{
       \frac{d^k}{ d x^{\mu_1} \cdots d x^{\mu_k}}
       \left(
         \frac{\delta_{EL} L}{\delta \phi^a}
       \right)
    \right\}
      &\longleftarrow&
    \left\{
      \overline{\phi}_{a,\mu_1 \cdots \mu_k}
    \right\}
    \\
    \left\{
      0
    \right\}
      &\longleftarrow&
    \left\{
      \overline{c}_{\alpha,\mu_1 \cdots \mu_k}
    \right\}
  }
$$

=--

+-- {: .proof}
###### Proof

The proof of this proposition is a special case of the
observation that the differentials involved are part of the local BV-BRST differential;
this will be a direct consequence of the proof of prop. \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm} below.

=--


The local analog of def. \ref{DerivedCriticalLocusOfGaugeInvariantFunctionOnLieAlgebroid} is now the following
definition \ref{DerivedProlongedShell} of the "derived prolonged shell" of the theory (recall the ordinary prolonged shell
$\mathcal{E}^\infty \hookrightarrow J^\infty_\Sigma(E)$ from (eq:ProlongedShellInJetBundle)):

+-- {: .num_defn #DerivedProlongedShell}
###### Definition
**(derived reduced prolonged [[shell]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over some [[spacetime]] $\Sigma$, and let $\mathcal{G} \overset{gb}{\to} \Sigma$ be
a bundle of closed irreducible [[gauge parameters]] (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}),
inducing via prop. \ref{EulerLagrangeFormIsSectionOfLocalCotangentBundleOfJetBundleGaugeActionLieAlgebroid}
a section $\delta_{EL} L$ of the local cotangent Lie algebroid of the jet bundle gauge-action Lie algebroid.

Then the _derived prolonged shell_ $\mathcal{E}^\infty_{BV}$ is the [[derived critical locus]]
of $\delta_{EL} L$, hence the [[homotopy pullback]] of $\delta_{EL} L$
along the zero section of the local cotangent Lie $\infty$-algebroid:

$$
  \array{
    \mathcal{E}^\infty_{BV}
      &\longrightarrow&
    E/( \mathcal{G} \times_\Sigma T \Sigma )
    \\
    \downarrow && \downarrow^{\mathrlap{0}}
    \\
    E/(\mathcal{G} \times_\Sigma T \Sigma)
     &\underset{\delta_{EL} L}{\longrightarrow}&
    T^\ast_\Sigma\left(
      E/( \mathcal{G} \times_\Sigma T \Sigma )
    \right)
  }
$$

=--



The local refinement of example \ref{ArchetypeOfBVBRSTComplex} is now the following:

+-- {: .num_prop #LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm}
###### Proposition
**([[local BV-BRST complex]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] with bundle of closed irreducible [[gauge parameters]]
$\mathcal{G}$...

.... the [[Chevalley-Eilenberg algebra]] of the derived prolonged shell $\mathcal{E}^\infty_{BV}$
(def. \ref{DerivedProlongedShell}) is the [[local BV-BRST complex]]...

=--

+-- {: .proof}
###### Proof

By unwinding the definitions analogous to the proof of example \ref{CotangentBundleOfActionLieAlgebroid},
the CE-differential is given by the modified bracket of derivations (eq:LocalCommutatorOfDerivationsOnJetBundle)
with the sum of the BRST-differential and the Lagrangian density:

$$
  d_{CE( T^\ast_\Sigma(E/(\mathcal{G} \times_\Sigma T\Sigma)) )}
  \;=\;
  \left\{
    \left(L + L_{BRST}\right) dvol_\Sigma
    \;,\;
    -
  \right\}
$$

only that in the homotopy fiber $\mathcal{E}^\infty_{BV}$ the derivations receive a degree-shift by -1 compared to
their degree in $T^\ast(E /( \mathcal{G} \times_\Sigma T \Sigma ))$.

This operation is the local BV-BRST differential by ([Barnich-Henneaux 96 (2.12)-(2.13)](local+BRST+cohomology#BarnichHenneaux96)).

=--



+-- {: .num_example #DerivedProlongedShellInAbsenceOfExplicitGaugeSymmetries}
###### Example
**(derived prolonged shell in the absence of explicit gauge symmetry -- the [[local BV-complex]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
with _no_ non-trivial [[infinitesimal gauge symmetries]] made explicit (possibly because there are none,
as for the [[scalar field]]), hence with no [[ghost fields]] introduced. Then the
local [[derived critical locus]] of its [[Lagrangian density]] (def. \ref{DerivedProlongedShell})
is the [[local BV-complex]] of def. \ref{BVComplexOfOrdinaryLagrangianDensity}.

=--


+-- {: .num_example #LocalBVComplexOfVacuumElectromagnetismOnMinkowskiSpacetime}
###### Example
**([[local BV-complex]] of [[vacuum]] [[electromagnetism]] on [[Minkowski spacetime]])**

Consider the [[Lagrangian field theory]] of [[free field theory|free]] [[electromagnetism]]
on [[Minkowski spacetime]] (example \ref{ElectromagnetismLagrangianDensity})
with [[gauge parameter]] as in example \ref{InfinitesimalGaugeSymmetryElectromagnetism}.
With the [[field (physics)|field]] and [[gauge parameter]] coordinates as chosen in these examples

$$
  \left(
    (a_\mu), c
  \right)
$$

then the [[local BV-BRST complex]] (prop. \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm})
has generators

$$
  \array{
    & \overline{c} & \overline{a}^\mu & a_\mu & c
    \\
    deg =
    &
    -2 & -1 & 0 & 1
  }
$$

together with their [[total spacetime derivatives]],
and the local BV-BRST differential $s$ acts on these generators as follows:

$$
  s
  \;\colon\;
  \left\{
  \array{
    \overline{a}^\mu &\mapsto&  f^{\nu \mu}_{,\nu}  & \text{(equations of Motion -- vacuum Maxwell equations)}
    \\
    \overline{c} &\mapsto& \overline{a}^\mu_{,\mu} & \text{(Noether identity)}
    \\
    a_\mu &\mapsto& c_{,\mu} & \text{(infinitesimal gauge transformation)}
  }
  \right.
$$


=--


$\,$

So far the discussion yields just the [[algebra of functions]] on the derived reduced prolonged shell.
We now discuss the derived analog of the full [[variational bicomplex]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
to the derived reduced shell.

The analog of the [[de Rham complex]] of a [[derived Lie algebroid]] is called the _[[Weil algebra]]_:

+-- {: .num_defn #WeilAlgebra}
###### Definition
**([[Weil algebra]] of a [[Lie algebroid]])**

Given a [[derived Lie algebroid]] $\mathfrak{a}$ over some $X$ (def. \ref{LInfinityAlgebroid}), its [[Weil algebra]] is

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

| [[smooth manifolds]] | [[derived Lie algebroids]] |
|----------------------|----------------------------|
| [[algebra of functions]] | [[Chevalley-Eilenberg algebra]] |
| algebra of [[differential forms]] | [[Weil algebra]] |


+-- {: .num_example #ClassicalWeilAlgebra}
###### Example
**(classical [[Weil algebra]])**

Let $\mathfrak{g}$ be a [[Lie algebra]] with corresponding
[[Lie algebroid]] $B \mathfrak{g}$ (example \ref{BasicExamplesOfLieAlgebroids}).
Then the Weil algebra (def. \ref{WeilAlgebra}) of $B \mathfrak{g}$ is
the traditional Weil algebra of $\mathfrak{g}$ from classical [[Lie theory]].

=--

+-- {: .num_defn #BVVariationalBicomplex}
###### Definition
**([[variational BV-bicomplex]])**

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

Similarly, the Weil algebra of the derived prolonged shell $\mathcal{E}^\infty_{BV}$ (def. \ref{DerivedProlongedShell})
has differential

$$
  \begin{aligned}
    d_W
      & =  \mathbf{d} - (d - s)
    \\
    & = \delta + s
  \end{aligned}
  \,.
$$

Since $s$ is the [[BV-BRST differential]] (prop. \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm})
this defines the "variational BV-BRST-bicomplex".

(...)

=--








$\,$


It turns out that the [[local BV-BRST cohomology]] (prop. \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm})
of the "derived reduced prolonged shell" very neatly captures all the aspects of [[Lagrangian field theory]]
that we have been discussing so far:


+-- {: .num_example #dWCohomology}
###### Example
**([[Noether's theorem|Noether theorem I]] in terms of [[local BRST cohomology]])**

The $d-s$-closed elements in degree $(p,0)$ are precisely pairs $(v,J_v)$
consisting of an implicit infinitesimal local gauge symmetry $v$ and a conserved current $J_v$ for it.

The $d_W$-exact elements in this degree are sums of

1. $d$-exact currents;

1. on-shell vanishing implicit gauge transformations;

1. on-shell vanishing currents with their horizontally exact gauge transformations

(...)


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





+-- {: .num_example }
###### Example
**([[infinitesimal gauge symmetry]] via [[local BRST cohomology]])**

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

([Barnich-Brandt-Henneaux 94, p. 20](local+BRST+cohomology#BarnichBrandtHenneaux94))


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


=--

$\,$


This concludes our discussion of the [[reduced phase space]] of a [[Lagrangian field theory]] exhibited, [[formal dual|dually]] by its
[[local BV-BRST complex]]. In the [next chapter](#GaugeFixing) we finally turn to the key implication of this construction:
the [[gauge fixing]] of a [[Lagrangian field theory|Lagrangian]] [[gauge theory]] which makes the collection of [[field (physics)|fields]]
and [[auxiliary fields]] ([[ghost fields]] and [[antifields]]) jointly have a (differential-graded) [[covariant phase space]].
