+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For general submersions

Given a [[submersion]] $p\colon E\to B$, one may ask: which [[differential forms]] on $E$ are [[pullback of differential forms|pullbacks]] of [[differential forms]] on $B$?

If the [[fibers]] of $p$ are [[connected topological space|connected]] (otherwise the characterization given below is valid only locally in $E$), the answer is provided by the notion of a __basic form__: a differential form $\omega$ is basic if the following two conditions are met:

1. The [[tensor contraction|contraction]] of $\omega$ with any $p$-[[vertical vector field]] is [[zero]] (i.e.: $\omega$ is [[horizontal differential form|horizontal]]),

1. the [[Lie derivative]] of $\omega$ with respect to any $p$-[[vertical vector field]] is [[zero]].

Using [[Cartan's magic formula]], in the presence of the first condition, the second condition is equivalent to the following one:

* (2.) The [[tensor contraction|contraction]] of $d\omega$ (where $d$ is the [[de Rham differential]]) with any $p$-[[vertical vector field]] is zero.

### Via pullback to smooth principal bundles

Given a [[Lie group]] $G$ and a [[smooth manifold|smooth]] $G$-[[principal bundle]] $P \overset{p}{\longrightarrow} X$ over a base [[smooth manifold]] $X$, a [[differential form]] $\omega \in \Omega^\bullet\big( P \big)$ on the total space $P$ is called _basic_ if it is the [[pullback of differential forms]] along the [[bundle]] projection $p$ of a differential form $\beta \in \Omega^\bullet\big( X \big)$ of the base manifold

$$
  \omega \;=\; p^\ast(\beta)
  \,.
$$

### In terms of Cartan calculus

Equivalently, if $\mathfrak{g} \simeq T_e G$ denotes the [[Lie algebra]] of $G$, and for $v \in \mathfrak{g}$ we write 

$$
  \hat v
  \;\colon\;
  P 
  \overset{ (e,v), (-,0) }{\hookrightarrow}
  T G \times T P
  \simeq
  T ( G \times P )
  \overset{ \;\;\; d \rho \;\;\; }{\longrightarrow}
  T P
$$

for the [[vector field]] on $P$ which is the [[derivative]] of the $G$-[[action]] $G \times P \overset{\rho}{\to} P$ along $v$, then a differential form $\omega$ is _basic_ precisely if

1. it is annihilated by the [[tensor contraction|contraction]] with $\hat v$
   
   $$
     \iota_{\hat v} \omega = 0
   $$

1. it is annihilated by the [[Lie derivative]] along $\hat v$:

   $$
     \mathcal{L}_{\hat v}\omega 
       \;=\; 
     [d_{dR}, \iota_{\hat v}] \omega
       \;=\;
     0
   $$

   (where the first equality holds generally by [[Cartan's magic formula]], we are displaying it just for emphasis)

for all $v \in \mathfrak{g}$.

In this form the definition of basic forms makes sense more generally whenever a [[Cartan calculus]] is given, not necessarily exhibited by smooth vector fields on actual manifolds. This more general concept of basic differential forms appears notably in the construction of the Weil model for [[equivariant de Rham cohomology]].

## References

### Related concepts

* [[horizontal differential form]]
* [[Chern-Weil theory]]

### Articles

* Peter W. Michor, _Basic differential forms for actions of Lie groups_, Proc. Amer. Math. Soc. __124__ (1996), 1633--1642 [doi](https://doi.org/10.1090/S0002-9939-96-03195-4)


[[!redirects basic differential forms]]
