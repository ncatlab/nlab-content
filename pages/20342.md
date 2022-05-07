

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

_Twisted Cohomotopy_ is the [[twisted cohomology]]-variant of the
the [[non-abelian cohomology]]-[[generalized cohomology theory|theory]] _[[Cohomotopy]]_, [[representable functor|represented]] by [[homotopy types]] of [[n-spheres]].

The [[coefficients]]/[[twisted cohomology|twist]] for twisted Cohomotopy are [[spherical fibrations]], and [[cocycles]] are [[sections]] of these. For those [[spherical fibrations]] arising as [[unit sphere bundles]] of [[real vector bundles]] the twist may be understood as given by the [[J-homomorphism]].

## Properties

Various classical theorems of [[differential topology]] are secretly theorems about [[twisted cohomotopy]]

<center>
<img src="https://ncatlab.org/nlab/files/TwistedCohomotopyAndDifferentialTopology.jpg" width="650">
</center>

> table grabbed from [FSS 19b](#FSS19b)

### Twisted Pontrjagin-Thom theorem
 {#TwistedPontrjaginThomTheorem}

The [[scanning map]]-equivalences on [[configuration spaces of points]] may be regarded as generalizations of the [Pontryagin-Thom theorem](cohomotopy#RelationToCobordismGroup) from [[sets]] of [[Cohomotopy]] [[cohomology class|classes]] to [[homotopy types]] of [[twisted Cohomotopy]] [[cocycles]]:

+-- {: .num_prop #ScanningMapEquivalenceOverClosedManifold}
###### Proposition

Let 

1. $X^n$ be a [[smooth manifold|smooth]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[scanning map]] constitutes a [[weak homotopy equivalence]]

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
    \text{scanning map}
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

Then the [[scanning map]] constitutes a [[weak homotopy equivalence]]

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
    \text{scanning map}
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

### Poincaré–Hopf theorem

See at

* [[Poincaré–Hopf theorem]]


### Equivariant Hopf degree theorem

On [[flat orbifolds]], twisted Cohomotopy becomes [[equivariant Cohomotopy]] and the twisted [[Hopf degree theorem]] becomes the

* [[equivariant Hopf degree theorem]]


## Related concepts

[[!include flavours of cohomotopy -- table]]


* [[twisted Pontrjagin theorem]]

## References

The concept is implicit in classical texts on [[differential topology]], for instance

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], Section 2 of: _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf), [[BoedigheimerStableSplittings87.pdf:file]])


Discussion of the [[twisted Pontrjagin theory]] and of twisted [[stable cohomotopy]] ([[framed manifold|framed]] [[cobordism cohomology theory]]):

* {#Cruickshank03} [[James Cruickshank]], Lemma 5.2 and Section 7 of: _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">doi:10.1016/S0166-8641(02)00183-9</a>)

Discussion of unstabilized twisted cohomotopy, with application to foundations of [[M-theory]] ([[schreiber:Hypothesis H]]):

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization|Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5-brane anomaly cancellation]]_ ([arXiv:2002.07737](https://arxiv.org/abs/2002.07737))

* {#FSS20a} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies twisted String structure on M5-branes]]_ ([arXiv:2002.11093](https://arxiv.org/abs/2002.11093))



[[!redirects twisted Cohomotopy]]

[[!redirects twisted cohomotopy theory]]
[[!redirects twisted Cohomotopy theory]]

[[!redirects twisted cohomotopy cohomology theory]]
[[!redirects twisted Cohomotopy cohomology theory]]
