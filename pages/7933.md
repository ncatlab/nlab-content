
> under construction, for a more coherent account see ([hpqg](#FiorenzaSchreiber)).

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
| $n-1$ | $\exp(2 \pi i S(-)) : [\Sigma_{n-1}, X] \stackrel{[\Sigma_{n-1}, \mathbf{c}_{conn}]}{\to} [\Sigma_{n-1}, \mathbf{B}^n \mathbb{G}_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_{n-1}}(-))}{\to}  \mathbf{B}\mathbb{G}_{conn}  \,$  | ordinary (off-shell) [[prequantum circle bundle]] | 

The idea is to consider the higher geometric quantization not just of the low codimension transgressions, but of all transgressions of $\mathbf{c}_{conn}$.
The basic constructions that higher geometric quantization is concerned with are indicated in the following table. All of them have also a fundamental interpretation in [[twisted cohomology|twisted]] [[cohomology]] (independent of any interpretation in the context of [[quantization]]) this is indicated in the right column of the table:



| higher [[geometric quantization]]  | [[cohesive homotopy type theory]] |[[twisted cohomology]] | 
|--|--|--|
| [[n-plectic ∞-groupoid]]  | $X \stackrel{\omega}{\to} \Omega^{n+1}_{cl}(-,\mathbb{G})$ | [[twisted cohomology|twisting]] [[cocycle]] in [[de Rham cohomology]] |
| [[symplectomorphism group]] | $\mathbf{Aut}_{/\Omega^{n+1}(-,\mathbb{G})}(\omega) = \left\{ \array{ X &&\stackrel{\simeq}{\to}&& X \\ & {}_{\mathllap{\omega}}\searrow && \swarrow_{\mathrlap{\omega}} \\ && \Omega^{n+1}_{cl}(-,\mathbb{G})  } \right\}$ |   |
| [[prequantum circle n-bundle]] | $\array{ && \mathbf{B}^n \mathbb{G}_{conn} \\ & {}^{\mathllap{\mathbf{c}_{conn}}}\nearrow & \downarrow^{\mathrlap{curv}} \\ X &\stackrel{\omega}{\to}& \Omega^{n+1}(-,\mathbb{G})}$ | [[twisted cohomology|twisting]] [[cocycle]] in [[ordinary differential cohomology|differential cohomology]] |
| [[Planck's constant]] $\hbar$ | $\tfrac{1}{\hbar}\mathbf{c}_{conn} : X \to \mathbf{B}^n \mathbb{G}_{conn}$ | divisibility of twisting class  |
| [[quantomorphism group]] $\supset$ [[Heisenberg group]] | $\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}) = \left\{ \array{ X &&\stackrel{\simeq}{\to}&& X \\ & {}_{\mathllap{\mathbf{c}_{conn}}}\searrow &\swArrow_\simeq& \swarrow_{\mathrlap{\mathbf{c}_{conn}}} \\ && \mathbf{B}^n \mathbb{G}_{conn} }  \right\}$ | twist [[automorphism ∞-group]] |
| [[Hamiltonian]] [[quantum operator (in geometric quantization)|quantum observables]] with [[Poisson bracket]] | $Lie(\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}))$  | [[infinitesimal cohesion|infinitesimal]] twist automorphisms |
| [[Hamiltonian actions]] of a [[smooth ∞-group]] $G$ / dual [[moment maps]]| $ \mu : \mathbf{B}G \to \mathbf{B}\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn})$ | $G$-[[∞-action]] on the twisting |
| [[gauge reduction]] | $\mathbf{c}_{conn}//G \,:\, X//G \to \mathbf{B}^n \mathbb{G}_{conn}$ | $G$-[[∞-quotient]] of the twisting  | 
| [[Hamiltonian symplectomorphisms]] |  [[∞-image]] of $\mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}) \to \mathbf{Aut}_{/\Omega^{n+1}_{cl}(-,\mathbb{G})}(\omega)$  | twists in de Rham cohomology that lift to differential cohomology |
| [[∞-representation]] of [[n-group]] $\mathbf{B}^{n-1}\mathbb{G}$ on $V_n$| $\array{ V_n &\to& V_n//\mathbf{B}^{n-1}\mathbb{G} \\ && \downarrow^{\mathbf{p}} \\ && \mathbf{B}^n \mathbb{G} }$ | [[local coefficient bundle]] |
|[[prequantum space of states]] | $\mathbf{\Gamma}_X(E) := [\mathbf{c},\mathbf{p}]_{/\mathbf{B}^n \mathbb{G}} = \left\{ \array{ X &&\stackrel{\sigma}{\to}&& V//\mathbf{B}^{n-1}\mathbb{G} \\ & {}_{\mathllap{\mathbf{c}}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{p}}} \\ && \mathbf{B}^n \mathbb{G} } \right\} $ | [[cocycles]] in $[\mathbf{c}]$-[[twisted cohomology|twisted V-cohomology]] |
| [[prequantum operator]] | $\widehat{(-)} : \mathbf{\Gamma}_X(E) \times \mathbf{Aut}_{/\mathbf{B}^n \mathbb{G}_{conn}}(\mathbf{c}_{conn}) \to \mathbf{\Gamma}_X(E)$ | [[∞-action]] of twist automorphisms on twisted cocycles |
| [[trace]] to higher [[dimension]] | $\array{ [S^1, V_n//\mathbf{B}^{n-1}\mathbb{G}_{conn}] &\stackrel{tr\,hol_{S^1}}{\to}& V_{n-1}//\mathbf{B}^{n-2}\mathbb{G}_{conn}  \\  \downarrow^{\mathrlap{\mathbf{p}^{V_n}_{conn}}} && \downarrow^{\mathrlap{\mathbf{p}^{V_{n-1}}_{conn}}} \\ \mathbf{B}^n \mathbb{G}_{conn} &\stackrel{\exp(2 \pi i \int_{S^1}(-))}{\to}& \mathbf{B}^{n-1} \mathbb{G}_{conn} }$  | [[fiber integration in ordinary differential cohomology]] adjoined with one in nonabelian differential cohomology |



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

### Of non-integral 2-forms

While only integral [[presymplectic forms]] have a [[prequantization]] to a prequantum [[circle bundle with connection]], hence to a $(\mathbb{Z} \to \mathbb{R})$-[[principal 2-bundle]], a general 2-form has a higher prequantization given by a [[connection on a 2-bundle]] on a [[principal 2-bundle]] with structure-[[2-group]] that coming from the [[crossed module]] $(\Gamma \hookrightarrow \mathbb{R})$, where $\Gamma$ is the [[discrete group]] of [[periods]] of the 2-form.

This is discussed further at _[[prequantization of non-integral 2-forms]]_.

### Of 2-plectic $\infty$-groupoids

#### In codimension 2

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

#### In codimension 1

**Proposition** There is a lift of coefficient bundles to [[loop space]]

$$
  \array{
    [S^1,(\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}] &\stackrel{tr hol_{S^1}}{\to}& \mathbb{C}//U(1)_{conn}
    \\
    \downarrow^{\mathrlap{\mathbf{p}^{\mathbf{B}U}}}
    &&
    \downarrow^{\mathrlap{\mathbf{p}^{\mathbb{C}}}}
    \\
    [S^1,\mathbf{B}^2 U(1)_{conn}]
    &\stackrel{\exp(2 \pi i \int_{S^1}(-))}{\to}& \mathbf{B}U(1)_{conn}
  }
$$

where on the left we have [[loop space objects]] formed in $\mathbf{H}$ and on the bottom we have [[fiber integration in ordinary differential cohomology]].

Forming the pasting composite with this sends 2-states and 2-operators in codimension 2 to ordinary states and operators in codimension 1.

In particular it sends  [[twisted bundles]]  to sections of a line bundle. 

For $X$ a [[D-brane]] and $\mathbf{c}_{conn}$ the [[B-field]], this
reproduces [[Freed-Witten anomaly cancellation]] mechanism.

### $\infty$-Chern-Simons theory 

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

#### Extended $(4k+3)d$ abelian Chern-Simons theory

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

For $k = 1$ the total space of the [[prequantum circle n-bundle|prequantum circle 3-bundle]] of $U(1)$-Chern-Simons theory over the point is the [[smooth infinity-groupoid|smooth]] [[moduli infinity-stack|moduli 2-stack]] of [[T-Duality and Differential K-Theory|differential T-duality structures]].

#### Extended 3d $\mathrm{Spin}$-Chern-Simons theory

* [[prequantum circle n-bundle|prequantum circle 3-bundle]]:

  [[differential string structure|differential first fractional Pontryagin class]] 

  $\tfrac{1}{2}\hat \mathbf{p}_1 : \mathbf{B}Spin_{conn} \to \mathbf{B}^3 U(1)_{conn}$

So [[Planck's constant]] here is  $\hbar = 2$ (relative to the naive multiple).

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

See the discussion at 
_[Chern-Simons theory -- Geometric quantization -- In higher codimension](Chern-Simons%20theory#GeometricQuantHigher)_.

#### Extended 3d $G \times G$-Chern-Simons theory

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


#### Extended 7d $\mathrm{String}$-Chern-Simons theory

* [[prequantum circle n-bundle|prequantum circle 7-bundle]]:

  [[differential fivebrane structure|differential second fractional Pontryagin class]] 

  $\tfrac{1}{6}\hat \mathbf{p}_2 : \mathbf{B}String_{conn} \to \mathbf{B}^z U(1)_{conn}$

So [[Planck's constant]] here is  $\hbar = 6$ (relative to the naive multiple).


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

### $\infty$ Wess-Zumino-Witten theory

* [[schreiber:∞-Wess-Zumino-Witten theory]]

Differentially twisted looping of $\infty$-Chern-Simons theory

$$  
  \Omega \mathbf{c} : G \to \mathbf{B}^{n-1}\mathbb{G}
$$

#### Ordinary $G$-WZW model

* [[WZW model]]

$$
  \tilde\Omega \tfrac{1}{2}\mathbf{p}_1 :  G \to \mathbf{B}^2 U(1)_{conn}
$$

studied in ([Rogers PhD, section 4.2](#RogersPhD)).

#### $String$-WZW model

(...)

#### $Fivebrane$-WZW model

(...)

## Related concepts

[[!include Isbell duality - table]]


## References

2-geometric quantization over [[smooth manifolds]] is discussed in section 6 and section 7 of 

* {#RogersPhD} [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))
 

with further indications in

* {#Rogers} [[Chris Rogers]], _Higher geometric quantization_, at _Higher Structures 2011_ ([[RogersGottingen11.pdf:file]])
 

The special case of geometric quantization over infinitesimal [[action groupoids]] can be described in terms of [[BRST complexes]]. For references on this see _[Geometric quantization -- References -- Geometric BRST quantization](http://ncatlab.org/nlab/show/geometric+quantization#ReferencesBRST)_.


Higher geometric quantization in a [[cohesive (∞,1)-topos]] over [[smooth ∞-groupoids]] is discussed in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Chris Rogers]], _[[schreiber:infinity-geometric prequantization]]_

and the examples of higher Chern-Simons theories in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]] _[[schreiber:Higher geometric prequantum theory]]_
 {#FiorenzaSchreiber}

[[!redirects higher geometric prequantization]]

[[!redirects extended geometric quantization]]
