
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Higher geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Higher geometric quantization is meant to complete this table:

| [[classical mechanics]] | --[[quantization]]$\to$ | [[quantum mechanics]] |
|--|--|--|
| [[symplectic geometry]] | --[[geometric quantization]]$\to$ | [[quantum field theory]] |
| [[higher symplectic geometry]] | --higher geometric quantization$\to$ | [[extended quantum field theory]] | 

Being a concept in [[higher geometry]], higher geometric quantization is formulated naturally in [[(∞,1)-topos theory]]. More precisely, since it involves not just _[[cohomology]]_ but _[[differential cohomology]]_, it is formulated in _[[cohesive (∞,1)-topos|cohesive (∞,1)-topos theory]]_ ([[cohesive homotopy type theory]]).

In this context, write $\mathbf{B}^n \mathbb{G}_{conn} \in \mathbf{H}$ for the cohesive [[moduli ∞-stack]] of [[circle n-bundles with connection]], in the ambient [[cohesive (∞,1)-topos]] $\mathbf{H}$. Then for $X \in \mathbf{H}$ any object to be thought of as the [[moduli ∞-stack]] of fields or as the [[target space]] for a [[sigma-model]], a morphism

$$
  \mathbf{c}_{conn} : X \to \mathbf{B}^n \mathbb{G}_{conn}
$$

modulates a [[circle n-bundle with connection]] on $X$. We regard this as a _extended [[action functional]]_ in that for $\Sigma_{k} \in \mathbf{H}$ of [[cohomological dimension]] $k \leq n$ and sufficiently compact so that [[fiber integration in ordinary differential cohomology]] $\exp(2 \pi i \int_{\Sigma}_k(-))$ applies, the [[transgression]] of $\mathbf{c}_{conn}$ to low [[codimension]] reproduces the traditional ingredients

| $k = $ | [[transgression]] of $\mathbf{c}_{conn}$ to $[\Sigma_{n-1},X]$ | meaning in [[geometric quantization]] |
|--|--|--|
| $n$ | $\exp(2 \pi i S(-)) : [\Sigma_n, X] \stackrel{[\Sigma_n, \mathbf{c}_{conn}]}{\to} [\Sigma_n, \mathbf{B}^n \mathbb{G}_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_n}(-))}{\to}  \mathbb{G} $ |  [[action functional]] |
| $n-1$ | $\exp(2 \pi i S(-)) : [\Sigma_{n-1}, X] \stackrel{[\Sigma_{n-1}, \mathbf{c}_{conn}]}{\to} [\Sigma_{n-1}, \mathbf{B}^n \mathbb{G}_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_n}(-))}{\to}  \mathbf{B}\mathbb{G}_{conn}  \,$  | ordinary (off-shell) [[prequantum circle bundle]] | 

The idea is to consider the higher geometric quantization not just of the low codimension transgressions, but of all transgressions of $\mathbf{c}_{conn}$.
The basic constructions that higher geometric quantization is concerned with are indicated in the following table. All of them have also a fundamental interpretation in [[twisted cohomology|twisted]] [[cohomology]] (independent of any interpretation in the context of [[quantization]]) this is indicated in the right column of the table:



| higher [[geometric quantization]]  | [[cohesive homotopy type theory]] |[[twisted cohomology]] | 
|--|--|--|
| [[n-plectic ∞-groupoid]]  | $X \stackrel{\omega}{\to} \Omega^{n+1}_{cl}(-,\mathbb{G})$ | [[twisted cohomology|twisting]] [[cocycle]] in [[de Rham cohomology]] |
| [[symplectomorphism group]] | $\mathbf{Aut}_{/\Omega^{n+1}(-,\mathbb{G})}(\omega) = \left\{ \array{ X &&\stackrel{\simeq}{\to}&& X \\ & {}_{\mathllap{\omega}}\searrow && \swarrow_{\mathrlap{\omega}} \\ && \Omega^{n+1}_{cl}(-,\mathbb{G})  } \right\}$ |   |
| [[prequantum circle n-bundle]] | $\array{ && \mathbf{B}^n \mathbb{G}_{conn} \\ & {}^{\mathllap{\mathbf{c}_{conn}}}\nearrow & \downarrow^{\mathrlap{curv}} \\ X &\stackrel{\omega}{\to}& \Omega^{n+1}(-,\mathbb{G})}$ | [[twisted cohomology|twisting]] [[cocycle]] in [[ordinary differential cohomology|differential cohomology]] |
| [[quantomorphism group]] | $\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}) = \left\{ \array{ X &&\stackrel{\simeq}{\to}&& X \\ & {}_{\mathllap{\mathbf{c}_{conn}}}\searrow &\swArrow_\simeq& \swarrow_{\mathrlap{\mathbf{c}_{conn}}} \\ && \mathbf{B}^n \mathbb{G}_{conn} }  \right\}$ | twist [[automorphism ∞-group]] |
| [[Hamiltonian actions]] of a [[smooth ∞-group]] $G$ / dual [[moment maps]]| $ \mu : \mathbf{B}G \to \mathbf{B}\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn})$ | $G$-[[∞-action]] on the twisting |
| [[Hamiltonian symplectomorphisms]] |  [[∞-image]] of $\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}) \to \mathbf{Aut}_{/\Omega^{n+1}_{cl}(-,\mathbb{G})}(\omega)$  | twists in de Rham cohomology that lift to differential cohomology |
| [[Hamiltonian]] [[quantum operator (in geometric quantization)|quantum observables]] | $Lie(\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}))$  | [[infinitesimal cohesion|infinitesimal]] twist automorphisms |
| [[∞-representation]] of $\mathbf{B}^{n-1}\mathbb{G}$ | $\array{ V &\to& V//\mathbf{B}^{n-1}\mathbb{G} \\ && \downarrow^{\mathbf{p}} \\ && \mathbf{B}^n \mathbb{G} }$ | [[local coefficient bundle]] |
|[[prequantum space of states]] | $\mathbf{\Gamma}_X(E) := [\mathbf{c},\mathbf{p}]_{/\mathbf{B}^n \mathbb{conn}} = \left\{ \array{ X &&\stackrel{\sigma}{\to}&& V//\mathbf{B}^{n-1}\mathbb{G} \\ & {}_{\mathllap{\mathbf{c}}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{p}}} \\ && \mathbf{B}^n \mathbb{G} } \right\} $ | [[cocycles]] in $[\mathbf{c}]$-[[twisted cohomology|twisted V-cohomology]] |
| [[prequantum operator]] | $\widehat{(-)} : \mathbf{\Gamma}_X(E) \times \mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}) \to \mathbf{\Gamma}_X(E)$ | [[∞-action]] of twist automorphisms on twisted cocycles |



## Examples



### Ordinary symplectic manifolds

* [[prequantum circle bundle]]

  $X \to \mathbf{B} U(1)_{conn}$

* [[local coefficient bundle]]

  $$
    \array{
      \mathbb{C} &\to& \mathbb{C}//U(1)
      \\
      && \downarrow
      \\
      && \mathbf{B} U(1)
    }
  $$

### Of 2-plectic $\infty$-groupoids

* [[prequantum circle n-bundle|prequantum circle 2-bundle]]

* [[local coefficient bundle]]

  $$
    \array{
      \mathbf{B}U(n) &\to& \mathbf{B}PU(n)
      \\
      && \downarrow^{\mathrlap{\mathbf{dd}_n}}
      \\
      && \mathbf{B}^2 U(1)
    }
  $$

* [[space of states]]: [[twisted bundles]]

### $\infty$-Chern-Simons theory generally

[[schreiber:∞-Chern-Simons theory]]

$G$ a [[smooth ∞-group]],

$$
  \mathbf{c}_{conn}
  : 
  \mathbf{B}G_{conn}
  \to 
  \mathbf{B}^n U(1)_{conn}
$$

a universal differential characteristic map.

The following examples are of this form.

### Extended $(4k+3)d$ abelian Chern-Simons theory

[[higher dimensional Chern-Simons theory]]

[[prequantum circle n-bundle|prequantum circle (4k+3)-bundle]] 
from [[Beilinson-Deligne cup product]]

$$
  \mathbf{B}^{2k+1}U(1)_{conn}
  \stackrel{(-)\cup (-)}{\to}
  \mathbf{B}^{4k+3}U(1)_{conn}
$$

The quantomorphism $\infty$-group of this should be

$$
  \mathbb{Z}_2 \simeq Aut(U(1))
  \,.
$$

For there is, up to equivalence, a unique autoequivalence

$$
  \mathbf{B}^{2k+1}U(1)_{conn} \stackrel{\simeq}{\to}
  \mathbf{B}^{2k+1}U(1)_{conn}
  \,,
$$

the one induced by the nontrivial automorphism of $U(1)$. Since the cup-product is strictly invariant under this, this extends to 

$$
  \array{
     \mathbf{B}^{2k+1}U(1)_{conn} &&\stackrel{\simeq}{\to}&&
     \mathbf{B}^{2k+1}U(1)_{conn}
     \\
     & {}_{\mathllap{(-)\cup(-)}}\searrow &\swArrow_\simeq& \swarrow_{\mathrlap{(-)\cup(-)}}
     \\
     && \mathbf{B}^{4k+3}U(1)_\conn
  }
  \,.
$$

But for any further nontrivial such autoequivalence in the slice we would need in particular a gauge transformation parameterized by $(2k+1)$-forms over test manifolds from $C \wedge d C$ to itself. But the only closed $2k$-forms that we can produce naturally from $C$ are multiples of $C \wedge C$. But these all vanish since $C$ is of odd degree $2k+1$.

### Extended 3d $\mathrm{Spin}$-Chern-Simons theory

* [[prequantum circle n-bundle|prequantum circle 3-bundle]]:

  [[differential string structure|differential first fractional Pontryagin class]] 

  $\tfrac{1}{2}\hat \mathbf{p}_1 : \mathbf{B}Spin_{conn} \to \mathbf{B}^3 U(1)_{conn}$

The total space of the prequantum 3-bundle is

$$
  \array{
    \mathbf{B}String_{conn'} &\to& \Omega^{1 \leq \bullet \leq 3} &\to& *
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    \mathbf{B}Spin_{conn} &\stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}& \mathbf{B}^3 U(1)_{conn} &\to& \mathbf{B}^3 U(1)
  }
$$

as it appears in [[schreiber:The moduli 3-stack of the C-field]].

But the quantomorphism group of this will be small, as the [[Chern-Simons form]] is far from being gauge invariant.

### Extended 3d $G \times G$-Chern-Simons theory

However, when we consider $G \times G$ CS theory given by

$$
  \mathbf{B}(G \times G)_{conn}
  \stackrel{\mathbf{c}^1_{conn}- \mathbf{c}^2_{conn}}{\to}
  \mathbf{B}^3 U(1)_{conn}
$$

then diagonal gauge transformations $\mathbf{B}(G \times G)_{conn}
 \to \mathbf{B}(G \times G)_{conn}$ have interesting extensions to quantomorphisms, because for $g : U \to G$ the given gauge transformation at stage of definition $U$, the Chern-Simons form transforms by an exact term

$$
  CS(A_1^g,A_2^g)
  =
  CS(A_1,A_2)
  + 
  d \langle A_1 - A_2, g^* \theta\rangle
  \,.
$$


### Extended 7d $\mathrm{String}$-Chern-Simons theory

* [[prequantum circle n-bundle|prequantum circle 7-bundle]]:

  [[differential fivebrane structure|differential second fractional Pontryagin class]] 

  $\tfrac{1}{6}\hat \mathbf{p}_2 : \mathbf{B}String_{conn} \to \mathbf{B}^z U(1)_{conn}$

The total space of the prequantum 7-bundle is

$$
  \array{
    \mathbf{B}Fivebrane_{conn'} &\to& \Omega^{1 \leq \bullet \leq 7} &\to& *
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    \mathbf{B}String_{conn} &\stackrel{\tfrac{1}{6}\hat \mathbf{p}_2}{\to}& \mathbf{B}^7 U(1)_{conn} &\to& \mathbf{B}^7 U(1)
  }
$$


## References

Higher geometric quantization over [[smooth manifolds]] is discussed in

* [[Chris Rogers]], _Higher geometric quantization_, at _Higher Structures 2011_ ([pdf](http://www.crcg.de/wiki/images/2/21/CR_Higherstruct_2011.pdf))

Higher geometric quantization in a [[cohesive (∞,1)-topos]] over [[smooth ∞-groupoids]] is discussed in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Chris Rogers]], _[[schreiber:infinity-geometric prequantization]]_

and the examples of higher Chern-Simons theories in 

* [[Domenico Fiorenza]], [[Urs Schreiber]] _[[schreiber:∞-Chern-Simons theory]]_
 {#FiorenzaSchreiber}

[[!redirects higher geometric prequantization]]
