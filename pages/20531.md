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

for the [[vector field]] on $P$ which is the [[derivative]] of the $G$-[[action]] $G \times P \overset{\rho}{\to} P$ along $v$, then differential form $\omega$ is _basic_ precisely if

1. it is annihilated by the contraction with $\hat v$
   
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

In this form the definition of basic forms makes sense more generally whenever a [[Cartan calculus]] is given, not necessarily exhibited by smooth vector fields on actual manifolds. This more general concept of basic differential forms appears notably in the construction of the Weil mdoel for [[equivariant de Rham cohomology]].

## Related concepts

* [[horizontal differential form]]


[[!redirects basic differential forms]]
