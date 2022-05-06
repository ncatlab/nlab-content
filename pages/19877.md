


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

While the [[Goodwillie calculus of functors]] is an accurate [[(infinity,1)-category theory|(∞,1)-]][[categorification]] of ordinary [[differential calculus]], in that it obeys various analogous rules, such as notably the [[chain rule]], it is fails one such rule, in an interesting way:

While in ordinary [[differential calculus]] the [[derivative]] of the [[identity function]] $\mathbb{R}^1 \overset{id}{\to} \mathbb{R}^1$ on the [[real line]] is itself the identity, this is not the case for the [[Goodwillie derivative]] of the [[identity functor]] $Top^{\ast/} \overset{Id}{\to} Top^{\ast/}$ on the [[category]] of [[pointed topological spaces]]. 

But the Goodwillie [[chain rule]] implies then that the nontrivial Goodwillie derivatives $D_\bullet Id$ of the identity functor satisfy a good algebraic compositional law. Indeed, they form an [[operad]] in [[spectra]] ([Ching 05a](#Ching05a)).

## Properties
 {#Properties}


### Action on configuration spaces of points
 {#ActionOnConfigurationSpacesOfPoints}


For $X$ a [[parallelizable manifold]] of [[dimension]] $dim(X) \in \mathbb{N}$ (without [[manifold with boundary|boundary]]) and for $n \in \mathbb{N}$ any [[natural number]], the $n \cdot dim(X)$-shifted [[suspension spectrum]] of the [[configuration space of points|configuration space]] $Conf_n(X)$ of $n$ points in $X$ (whose elements are such configurations, and a basepoint is freely adjoined) is canonically an [[algebra over an operad|algebra]] over the operad of Goodwillie derivatives 

\[
  \label{ConfigurationSpaceAsAlgebraOverGodwillieDerivativesOfIdentity}
  \Sigma^{-n dim(X)}\Sigma^{\infty} Conf_n(X) 
    \;\in\; 
   Alg\big( 
     D_\bullet Id 
   \big)
  \,.
\]

([Ching 05b, Prop. 3.1](#Ching05b))


### Relation to the little $n$-disk operad

For each [[natural number]] $d \in \mathbb{N}$ is a canonical homomorphism of [[operads]] from the Goodwillie derivatives of the identity functor to the the $d$-fold [[looping]] of the [[little n-disk operad|little d-disk operad]], incarnated as the [[Fulton-MacPherson operad]]

\[
  \label{HomomorphismOfOperadsToLittleNDiskOperad}
  \phi \;\colon\; D_\bullet Id \longrightarrow \Sigma^{-d} E_d
\]

where the shifted operad on the right has component space in degree $k$ given by the iterated [[loop space]]

\[
  \label{HomomorphismToLittleNDiskOperad}
  \left( \Sigma^{-d}E_d \right)(k)
    \;\coloneqq\;
  \Omega^{d(k-1)} \left( E_n(k) \right)
  \,.
\]

([Ching 05b, below Lemma 4.1](#Ching05b))

Now the [[configuration space]] $Con_n(X)$ from [above](#ActionOnConfigurationSpacesOfPoints) is _also_ canonically an [[algebra over an operad|algebra]] over the [[little n-disk operad]] ([Markl 99](configuration+space+of+points#Markl99)):

\[
  \label{ConfigurationSpaceAsAlgebraOverLittleNDiskOperad}
  \Sigma^{-n dim(X)}\Sigma^{\infty} Conf_n(X) 
    \;\in\; 
  Alg\left( 
    \Sigma^{-dim(X)}E_{dim(X)}
  \right)
  \,.
\]

Conjecturally, the [[operad]]-[[homomorphism]] (eq:HomomorphismToLittleNDiskOperad), via its induced [[functor]] on [[algebras over an operad]]

$$
  \phi^\ast
  \;\colon\;
  Alg\left( 
    \Sigma^{-dim(X)}E_{dim(X)}
  \right)
    \longrightarrow  
   Alg\big( 
     D_\bullet Id 
   \big)
$$

identifies these two [[algebra over an operad]]-[[structures]] on shifted [[configuration spaces of points]] from (eq:ConfigurationSpaceAsAlgebraOverGoodwillieDerivativesOfIdentity) and from  (eq:ConfigurationSpaceAsAlgebraOverLittleNDiskOperad)

$$
  \Sigma^{-n dim(X)}\Sigma^{\infty} Conf_n(X) 
    \;\in\; 
  Alg\left( 
    \Sigma^{-dim(X)}E_{dim(X)}
  \right)  
    \overset{ \phi^\ast }{\longrightarrow}
   Alg\big( 
     D_\bullet Id 
   \big)
$$

([Ching 05b, Conjecture 4.2](#Ching05b))

## References

* {#AroneMahowald98} [[Gregory Arone]], [[Mark Mahowald]], _The Goodwillie tower of the identity functor and the unstable periodic homotopy of spheres_, Inventiones mathematicae February 1999, Volume 135, Issue 3, pp 743-788  ([pdf](http://hopf.math.purdue.edu/Arone-Mahowald/ArMahowald.pdf))

* {#AroneKankaanrinta95} [[Gregory Arone]], Marja Kankaanrinta,  _The Goodwillie tower of the identity is a logarithm_, 1995 ([[Arone95.pdf:file]], [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.8306))


* {#Ching05a} [[Michael Ching]], _Bar constructions for topological operads and the Goodwillie derivatives of the identity_, Geom. Topol. 9 (2005) 833-934 ([arXiv:math/0501429](https://arxiv.org/abs/math/0501429))

* {#Ching05b} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))


