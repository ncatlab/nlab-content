

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
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The [[Bredon cohomology]]-[[equivariant cohomology|equivariant]] enhancement of [[cohomotopy]]-theory is _equivariant cohomotopy_: 

For $G$ a [[group]], $V$ a [[finite dimensional vector space|finite-dimensional]] [[real vector space|real]]  $G$-[[representation]] $G \to O(V)$ and writing $S^V$ for the corresponding [[representation sphere]], the _equivariant cohomotopy_ in [[RO(G)-degree]] $V$ of a [[G-space]] $X$ is the set of $G$-[[equivariant homotopy theory|equivariant]] [[homotopy classes]] of maps from $X$ to $S^V$:

$$
  \pi_G^V\big( X \big)
  \;\coloneqq\;
  \left[
    X, S^V
  \right]^G
  \,.
$$

For $V = \mathbb{R}^n$ the [[trivial representation]] of [[dimension]] $n$, this reduces to the definition of plain [[cohomotopy]]-sets

$$
  \pi^{\mathbb{R}^n}(X)
  \;=\;
  \pi^n(X)
  \;=\;
  \left[ X, S^n\right]
  \,.
$$


The [[stabilization]] of this construction, in the sense of [[equivariant stable homotopy theory]], yields the concept of _[[equivariant stable cohomotopy]]_.




## Properties

### Equivariant Pontryagin-Thom isomorphism
 {#EquivariantPontryaginThomIsomorphism}

+-- {: .num_prop #EquivariantPT}
###### Proposition

The [[Pontryagin-Thom construction]] generalizes from plain [[cohomotopy]] ([here](cohomotopy#RelationToCobordismGroup)), to equivariant cohomotopy. Here it identifies classes in $\pi^V(X)$ with [[cobordism classes]] of "partially $V$-franed" $d$-[[dimension|dimensional]] [[submanifolds]] $\Sigma \subset X^G$ inside the $G$-[[fixed point]]-locus $X^G \subset X$ for

$$
  d \;=\;  dim\left( X^G \right) - dim\left( V^G \right)
$$

hence with [[codimension]] relative to $X^G$ the dimension of the [[fixed point]]-locus of $V$.

(...)

=--

([Grady 18](#Grady18))

<br/>

(...)

> under construction

+-- {: .num_example #ASimpleExample}
###### Example
**(equivariant degree-1 Cohomotopy of the circle)**

Let $G = \mathbb{Z}_2$ be the [[cyclic group]] of [[order of a group|order]] 2. Consider the [[circle]] $S^1 =S(\mathbb{R}^2)$ equipped with the $\mathbb{Z}_2$-[[action]] whose [[involution]] [[reflection|reflects]] one of the two [[coordinate functions|coordinates]] of the ambient [[Cartesian space]] $\sigma \;\colon\; (x_1,x_2) \mapsto (x_1, -x_2)$.

This means that the [[fixed point space]] is the [[0-sphere]]

$$
  \big( S^1\big)^{\mathbb{Z}_2}
  \;\simeq\;
  S^0
$$

being two antipodal points on the circle, which we may call $\{0,1\} \simeq S^0$.

Take this circle to be both the [[domain]] space $X$ as well as the [[coefficient]] [[n-sphere|1-sphere]].


By Prop. \ref{EquivariantPT} the equivariant homotopy classes of maps $S^1 \to S^1$ correspond to [[submanifolds]] of $S^0$ of [[codimension]] 0 with respect to $S^0$, but equivariantly framed with respect to the ambient $S^1$ -- hence in lowest degree simply of [[subsets]] of $S^0$. 

Indeed, under passage to [[fixed points]] any

$$
  S^1 \overset{f}{\longrightarrow} S^1 \simeq \{0,1\}
$$

induces a map

$$
  S^0 
    \overset{
      \big( f\big)^{\mathbb{Z}_2}
    }{\longrightarrow} 
  S^0
$$

and we may regard this as encoding the [[subset]] of $S^0$ which is the [[preimage]] of the chosen non-[[basepoint]] $1 \in S^0$.

Hence

1. the [[empty set|empty]] subset $\varnothing \subset S^0$ corresponds to the [[constant function]] $S^1 \to \{0\} \hookrightarrow S^1$;

1. the full subset $S^0 = S^0$ corresponds to the [[constant function]] $S^1 \to \{1\} \hookrightarrow S^1$;

1. the intermediate subset $\{1\} \subset S^0$ corresponds to the [[identity function]] $S^1 \overset{id}{\longrightarrow} S^1$.

Notice that it is only the last case that is homotopically non-trivial after forgetting the equivariance.

(...)

=--

<br/>

## Related concepts

[[!include flavours of cohomotopy -- table]]

<br/>

## References

### General

* {#Wasserman69} [[Arthur Wasserman]], section 3 of _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))


* {#Cruickshank03} James Cruickshank, _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)

* {#Grady18} Daniel Grady, _Cobordisms of global quotient orbifolds and an equivariant Pontrjagin-Thom construction_ ([arXiv:1811.08794](https://arxiv.org/abs/1811.08794))

### For M-brane charge quantization

Discussion of [[M-brane]] [[charge quantization]] in [[equivariant cohomotopy]]:


* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

  ([[equivariant rational homotopy theory|rational equivariant]] cohomotopy)

* [Grady 18, section 4](#Grady18)
