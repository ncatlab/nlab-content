

> This is a sub-entry of [[smooth ∞-groupoid -- structures]]. See there for more context.

--

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In every [[cohesive (∞,1)-topos]] there is a notion of <a href="http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#ConcreteObjects">concrete cohesive ∞-groupoids</a>. Here we discuss concrete [[nLab:smooth ∞-groupoid]]s. These are the [[(∞,1)-category theory|higher generalization]] of [[nLab:diffeological space]]s.

## Definition

The general abstract definition is:

+-- {: .num_defn}
###### Definition

A **concrete smooth $\infty$-groupoid** is a <a href="http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#ConcreteObjects">concrete cohesive ∞-groupoids</a> in [[Smooth∞Grpd]].

=--

We will compare this intrinsic definition with more concrete models:

+-- {: .num_defn #DiffeologicalSpace}
###### Definition

A [[diffeological space]] is a [[concrete sheaf]] on the [[site]] [[CartSp]]${}_{smooth}$.

Write

$$
  DiffeolSpace \hookrightarrow Sh(CartSp)
$$

for the [[full subcategory]] on diffeological spaces. Notice that is a [[quasitopos]].

=--


+-- {: .num_defn #DiffeologicalGroupoid}
###### Definition

A **diffeological groupoid** is an [[internal groupoid]] in the [[category]] of [[diffeological space]]s.

=--

(...)


## Special cases

We discuss the special cases of [[n-truncated]] concrete smooth $\infty$-groupoids:

* 0-truncated: [diffeological space](0TruncAndDiffeolSpace)

* 1-truncated: [diffeological groupoids](#1TruncDiffolGroupoid).

### Diffeological spaces
 {#0TruncAndDiffeolSpace}


+-- {: .num_prop #Concrete0TruncatedIsDiffeological}
###### Proposition

Concrete smooth 0-groupoids are equivalently [[diffeological space]]s.

More in detail, write $Conc(\tau_{\leq 0} Smooth \infty Grpd)$ for the full [[subcategory]] on the [[concrete sheaf|concrete]] [[0-truncated]] objects. This is [[equivalence of categories|equivalent]] to the category of [[diffeological space]]s

$$
  DiffeolSp 
   \simeq 
  Conc(\tau_{\leq 0} Smooth \infty Grpd)
  \,.
$$

=--


+-- {: .proof}
###### Proof

Let $X \in Sh(CartSp) \hookrightarrow Smooth \infty Grpd$ be a [[sheaf]] on $CartSp$. The condition for it to be concrete is that the [[unit of an adjunction|unit]]

$$
  X \to coDisc \Gamma X
$$

is a [[monomorphism]]. Since monomorphisms of sheaves are detected objectwise (see [[category of sheaves]]) this is equivalent to the statement that for all $U \in CartSp$ the morphism

$$
  X(U) \simeq Smooth\infty Grpd(U, X) \to Smooth \infty Grpd(U, coDisc \Gamma X)
  \simeq
  \infty Grpd(\Gamma U, \Gamma X)
$$

is a monomorphism of sets, where in the first step we used the [[(∞,1)-Yoneda lemma]] and in the last one the $(\Gamma \dashv coDisc)$-[[adjunction]]. 

That this morphism is indeed $\Gamma : Sh(U,X) \to Set(\Gamma(U), \Gamma(X)) \hookrightarrow \infty Grpd(\Gamma(U), \Gamma(X))$ follows by chasing the identity on $\Gamma X$ through the adjunction naturality square for any morphism $f : U \to X$

$$
  \array{
    Set(\Gamma X, \Gamma X) &\stackrel{\simeq}{\to}&
    Sh(X, coDisc \Gamma X)
    \\
    \downarrow^{\mathrlap{\Gamma(f)^*}} && \downarrow^{\mathrlap{f^*}}
    \\
    Set(\Gamma U, \Gamma X) &\stackrel{\simeq}{\leftarrow}& Sh(U, coDisc \Gamma X)
  }
  \,.
$$

So this is indeed the defining condition for [[concrete sheaves]] that defines [[diffeological space]]s.

=--

+-- {: .num_cor}
###### Corollary

The canonical embedding $SmoothMfd \hookrightarrow Smooth \infty Grpd$
from [above](#EmbeddingOfSmoothManifolds) factors through [[diffeological spaces]]: we have a sequence of [[full and faithful (∞,1)-functor]]s

$$
  SmoothMfd \hookrightarrow DiffeolSp \hookrightarrow Smooth \infty Grpd
  \,.
$$

=--



### Diffeological groupoids
 {#1TruncDiffolGroupoid}

We want to say the following

+-- {: .num_prop}
###### Proposition

Concrete [[1-truncated]] smooth $\infty$-groupoids are equivalent to diffeological groupoids, def. \ref{DiffeologicalGroupoid}.

(...)

=--

+-- {: .proof}
###### Proof

Let $A$ be 1-truncated and concrete. Then by definition there is
a concrete 0-truncated object $A_0$ and an [[effective epimorphism]] $A_0 \to A$ -- an [[atlas]] -- , such that the [[(∞,1)-pullback]] 

$$
  A_1 :=  A_0 \times_A A_0
$$ 

is itself concrete.

Since $A$ is assumed to be [[1-truncated]], it follows that $A_1$ is [[0-truncated]]. By [[Giraud's axioms]] in the [[(∞,1)-topos]] [[Smooth∞Grpd]] we have that $A$ is [[equivalence in an (∞,1)-category|equivalent]] to the [[groupoid object in an (∞,1)-category]] $A_1 \stackrel{\to}{\to} A_0$:

\[
  A \simeq \lim_\to (A_1 \stackrel{\to}{\to} A_0)
  \,.
\]

Now by prop. \ref{Concrete0TruncatedIsDiffeological} both $A_0$ and $A_1$ are [[diffeological space]]s. Hence the above exhibits $A$ as equivalent to a diffeological groupoid.

(...)

=--

## Transgression of differential cocycles to mapping spaces
 {#TransgressionOfDifferentialCocycles}


For $n \in \mathbb{N}$, write $\mathbf{B}^n U(1)_{conn} \in Smooth\infty Grpd$ for the smooth $\infty$-groupoid given under the [[Dold-Kan correspondence]] by the [[Deligne complex]]. Over [[smooth manifold]]s this is the coefficient object for [[circle n-bundles with connection]].

At [[schreiber:∞-Chern-Simons theory]] the following fact is proven:

+-- {: .num_prop #IntrinsicHolonomyTakingValuesInDiscrete}
###### Proposition

Let $\Sigma$ be a closed [[smooth manifold]] of [[dimension]] $dim \Sigma \leq n$. Then there is an equivalence

$$
  hol
    :
  \tau_{n - dim \Sigma} \mathbf{H}(\Sigma, \mathbf{B}^n U(1)_{conn})
   \to 
  B^{n-dim \Sigma} U(1)
$$

of [[discrete ∞-groupoid]]s such that for $dim \sigma  = n$ this computes the $n$-volume [[holonomy]] of circle $n$-bundles with connection.

=--

Using concretization we want to refine this from discrete to smooth $\infty$-groupoids.

Write $[\Sigma, \mathbf{B}^n U(1)_{conn}]$ for the [[internal hom]] in the [[(∞,1)-topos]] (see there).

We first look at this for $n = dim \Sigma$

+-- {: .num_prop}
###### Proposition

For $dim \Sigma = n$ there is an equivalence

$$
  hol 
   : 
  Conc \tau_0 [\Sigma, \mathbf{B}^nU(1)_{conn}]
   \to 
   U(1)
$$

in [[Smooth∞Grpd]].

=--

+-- {: .proof}
###### Proof

Since $\tau_0 [\Sigma, \mathbf{B}^n U(1)_{conn}]$ is [[0-truncated]], hence a [[sheaf]], concretification is that discussed at [[concrete sheaves]]:

$$
  Conc(F)(U) = image( F(U) = \mathbf{H}(U,F) \to 
  \mathbf{H}(U, coDisc \Gamma F) =  Set(\Gamma(U), \Gamma(F)) )
  \,.
$$

So for $U = *$ first of all we have by prop. \ref{IntrinsicHolonomyTakingValuesInDiscrete} that 

$$
  Conc \tau_0 \mathbf{H}(\Sigma, \mathbf{B}^n U(1)_{conn})(*) = U(1)
$$ 

in $Set$.

Generally $Conc \tau_0 \mathbf{H}(\Sigma, \mathbf{B}^n U(1)_{conn})(U)$
is therefore a subset of the set of functions of sets $U \to U(1)$. We need to show that it is precisely the set of smooth such functions.

But this is clear: holonomy of a smoth family of smoth circle $n$-bundles is a smooth function. Moreover, every smooth function arises this way: for $f : U \to U(1)$ any smooth function, pick a trivial family of trivial circle $n$-bundles with connection and then rescale the connection form using $f$.

=--

## Related concepts

* [[concrete sheaf]], [[concrete (∞,1)-sheaf]]

* [[diffeological space]], [[Lie groupoid]]

## References

Many of the ideas involved here are due to [[Dave Carchedi]].

A writeup of some aspects is in section 3.3.1 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects concrete smooth ∞-groupoid]]

[[!redirects concrete smooth infinity-groupoid]]
[[!redirects concrete smooth infinity-groupoids]]

[[!redirects diffeological ∞-groupoid]]
[[!redirects diffeological infinity-groupoid]]

[[!redirects diffeological ∞-groupoids]]
[[!redirects diffeological infinity-groupoids]]
