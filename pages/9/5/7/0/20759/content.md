
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Cohomotopy charge map_ is the [[function]] that assigns to a [[configuration space of points|configuration of points]] their total [[charge]] as measured in [[Cohomotopy]]-[[generalized cohomology|cohomology theory]].

This is alternatively known as the "electric field map" ([Salvatore 01](#Salvatore01) following [Segal 73, Section 1](#Segal73), see also [Knudsen 18, p. 49](#Knudsen18)) or the "scanning map" ([Kallel 98](#Kallel98)).


For $D \in \mathbb{N}$ the _Cohomotopy charge map_ is the  [[continuous function]]

\[
  \label{CohomotopyChargeMapOnEuclideanSpace}
  Conf\big( \mathbb{R}^D \big)
  \overset{cc}{\longrightarrow}
  \mathbf{\pi}^D
  \Big( 
    \big( \mathbb{R}^D \big)^{cpt}
  \Big)
  =
  Maps^{\ast/\!}\Big( \big(\mathbb{R}^D\big)^{cpt} , S^D\big)
  =
  \Omega^{D} S^D
\]

from the [[configuration space of points]] in the [[Euclidean space]] $\mathbb{R}^D$ to the $D$-[[Cohomotopy]] [[cocycle space]] [[vanishing at infinity]] on the [[Euclidean space]](which is equivalently the [[space of maps|space of pointed maps]] from the [[one-point compactification]] $S^D \simeq \big( \mathbb{R}^D \big)$ to itself, and hence equivalently the $D$-fold [[iterated based loop space]] of the [[n-sphere|D-sphere]]), which sends a configuration of points in $\mathbb{R}^D$, each regarded as carrying unit [[charge]] to their total [[charge]] as measured in  [[Cohomotopy]]-[[generalized cohomology|cohomology theory]] ([Segal 73, Section 3](#Segal73)).

This has evident generalizations to other manifolds than just Euclidean spaces, to spaces of labeleed configurations and to [[equivariant Cohomotopy]]. The following graphics illustrates the Cohomotopy charge map on [[G-space]] [[tori]] for $G = \mathbb{Z}_2$ with values in $\mathbb{Z}_2$-[[equivariant Cohomotopy]]:

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=24">
<img src="https://ncatlab.org/schreiber/files/EquivariantCohomotopyTadpoleCancellationN.jpg" width="700">
</a>
</center>

> graphics grabbed from [SS 19](#SatiSchreiber19)

## Properties

### Characterization of point configurations by their Cohomotopy charge

In some situations the [[Cohomotopy charge map]] is a [[weak homotopy equivalence]] and hence exhibits, for all purposes of [[homotopy theory]], the [[Cohomotopy]] [[cocycle space]] of Cohomotopy charges as an equivalent reflection of the [[configuration space of points]]. 

#### On Euclidean spaces via plain Cohomotopy


+-- {: .num_prop #GroupCompletionOfConfigurationSpaceIsIteratedBasedLoopSpace}
###### Proposition
**([[group completion]] on [[configuration space of points]] is [[iterated based loop space]])**

The [[Cohomotopy charge map]] (eq:CohomotopyChargeMapOnEuclideanSpace)

$$
  Conf
  \big(
    \mathbb{R}^D
  \big)
  \overset{
    cc
  }{\longrightarrow}
  \Omega^D S^D
$$

from the full unordered and unlabeled configuration space ([here](configuration+space+of+points#eq:UnorderedUnlabeledConfigurationSpace)) of [[Euclidean space]] $\mathbb{R}^D$  to the $D$-fold [[iterated based loop space]] of the [[n-sphere|D-sphere]], exhibits the [[group completion]] ([here](configuration+space+of+points#eq:GroupCompletionOfConfigurationSpaceMonoid)) of the configuration space monoid 

$$
  \Omega B_{{}_{\sqcup}\!} 
  Conf
  \big(
    \mathbb{R}^D
  \big)
  \overset{
    \simeq
  }{\longrightarrow}
  \Omega^D S^D
$$

=--

([Segal 73, Theorem 1](#Segal73))

+-- {: .num_prop #CohomotopyChargeMapIsEquivalenceOnSPhereLabeledConfihgurationSpace}
###### Proposition
**([[Cohomotopy charge map]] is [[weak homotopy equivalence]] on sphere-labeled [[configuration space of points]])**

For $D, k \in \mathbb{N}$ with $k \geq 1$, the [[Cohomotopy charge map]] (eq:CohomotopyChargeMapOnEuclideanSpace)

$$
  Conf
  \big(
    \mathbb{R}^D,
    S^k
  \big)
  \underoverset{\simeq}{cc}{\longrightarrow}
  \Omega^D S^{D + k}
$$

is a [[weak homotopy equivalence]] from the configuration space ([here](configuration+space+of+points#eq:UnorderedLabeledCOnfigurationSpace)) of unordered points with labels in $S^k$ and vanishing at the base point of the label space to the $D$-fold [[iterated loop space]] of the [[n-sphere|D+k-sphere]].

=--

([Segal 73, Theorem 3](#Segal73))


#### On closed manifolds via twisted Cohomotopy

The May-Segal theorem \ref{ScanningMapEquivalenceOverCartesianSpace} generalizes from [[Euclidean space]] to [[closed manifold|closed]] [[smooth manifolds]] if at the same time one passes from plain [[Cohomotopy]] to [[twisted Cohomotopy]], twisted, via the [[J-homomorphism]], by the [[tangent bundle]]:

+-- {: .num_prop #ScanningMapEquivalenceOverClosedManifold}
###### Proposition

Let 

1. $X^n$ be a [[smooth manifold|smooth]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[Cohomotopy charge map]] constitutes a [[weak homotopy equivalence]]

$$
  \underset{
    \color{blue}
    { \phantom{a} \atop \text{ J-twisted Cohomotopy space}}
  }{
    Maps_{{}_{/B O(n)}}
    \Big(
      X^n 
      \;,\; 
      S^{
        \mathbf{n}_{def} + \mathbf{k}_{\mathrm{triv}}    
      }
      \!\sslash\!
      O(n)
    \Big)
  }
  \underoverset
  {\simeq}
  {
    \color{blue}
    \text{Cohomotopy charge map}
  }
  {\longleftarrow}
  \underset{
    \mathclap{
    \color{blue}
      {
        \phantom{a}
        \atop
        {
          \text{configuration space}
          \atop 
          \text{of points}
        }
      }
    }
  }{
    Conf
    \big(
      X^n,
      S^k
    \big)
  }
$$

between 

1. the [[J-homomorphism|J]]-[[twisted Cohomotopy|twisted (n+k)-Cohomotopy]] space of $X^n$, hence the [[space of sections]] of the $(n + k)$-[[spherical fibration]] over $X$ which is [[associated fiber bundle|associated]] via the [[tangent bundle]] by the [[O(n)]]-[[action]] on $S^{n+k} = S(\mathbb{R}^{n} \times \mathbb{R}^{k+1})$

1. the [[configuration space of points]] on $X^n$ with labels in $S^k$.

=--

([Bödigheimer 87, Prop. 2](#Boedigheimer87), following [McDuff 75](#McDuff75))

+-- {: .num_prop #ScanningMapEquivalenceOverClosedFramedManifold}
###### Remark

In the special case that the [[closed manifold]] $X^n$ in Prop. \ref{ScanningMapEquivalenceOverClosedManifold} is [[parallelizable manifold|parallelizable]], hence that its [[tangent bundle]] is [[trivial bundle|trivializable]], the statement of Prop. \ref{ScanningMapEquivalenceOverClosedManifold} reduces to this:

Let

1. $X^n$ be a [[parallelizable manifold|parallelizable]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[Cohomotopy charge map]] constitutes a [[weak homotopy equivalence]]

$$
  \underset{
    \color{blue}
    { \phantom{a} \atop \text{ Cohomotopy space}}
  }{
    Maps
    \Big(
      X^n 
      \;,\; 
      S^{
       n + k    
      }
    \Big)
  }
  \underoverset
  {\simeq}
  {
    \color{blue}
    \text{Cohomotopy charge map}
  }
  {\longleftarrow}
  \underset{
    \mathclap{
    \color{blue}
      {
        \phantom{a}
        \atop
        {
          \text{configuration space}
          \atop 
          \text{of points}
        }
      }
    }
  }{
    Conf
    \big(
      X^n,
      S^k
    \big)
  }
$$

between 

1. $(n+k)$-[[Cohomotopy]] space of $X^n$, hence the [[space of maps]] from $X$ to the [[n-sphere|(n+k)-sphere]]

1. the [[configuration space of points]] on $X^n$ with labels in $S^k$.

=--



## References

The concept goes back to

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Springer 1972 ([pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))

* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

with comprehensive review in

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf), [[BoedigheimerStableSplittings87.pdf:file]])

See also:

* {#Kallel98} [[Sadok Kallel]], _Particle Spaces on Manifolds and Generalized Poincaré Dualities_ ([arXiv:math/9810067](https://arxiv.org/abs/math/9810067)) 

* {#Salvatore01} [[Paolo Salvatore]], _Configuration spaces with summable labels_, In: Aguadé J., Broto C., [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel, 2001 ([arXiv:math/9907073](https://arxiv.org/abs/math/9907073))

* {#Knudsen18} [[Ben Knudsen]], _Configuration spaces in algebraic topology_ ([arXiv:1803.11165](https://arxiv.org/abs/1803.11165))

* {#SatiSchreiber19} [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))

[[!redirects cohomotopy charge map]]
[[!redirects cohomotopy charge maps]]

[[!redirects Cohomotopy charge map]]
[[!redirects Cohomotopy charge maps]]

[[!redirects scanning map]]
[[!redirects scanning maps]]

[[!redirects scanning map equivalence]]
[[!redirects scanning map equivalences]]

[[!redirects cohomotopy charge]]
[[!redirects cohomotopy charges]]

[[!redirects Cohomotopy charge]]
[[!redirects Cohomotopy charges]]




