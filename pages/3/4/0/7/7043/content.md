
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Wess-Zumino-Witten theory
+--{: .hide}
[[!include infinity-Wess-Zumino-Witten theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[infinity-Wess-Zumino-Witten theory - contents|higher dimensional WZW models]] the following 1-dimensional [[sigma-models]] are seen to be examples:

* the free [[non-relativistic particle]];

* the massive [[Green-Schwarz action functional|Green-Schwarz]] [[superparticle]] (the [[D0-brane|D0]] [[super p-brane]]).

([Azcarraga-Izqierdo 95, section 8.3 and 8.7](#AzcarragaIzqierdo)) .

## Examples

### Free massive non-relativistic particle

Write 

$$
  H \coloneqq G/R
$$

for the [[coset]] obtained as the [[quotient]] of the [[Galilei group]] in some [[dimension]] $d$ by the [[rotation group|group of]] [[rotations]]. This $H$ has a canonical global [[coordinate chart]] $(t,x, \dot x)$. We may regard it as the first order [[jet bundle]] to the [[bundle]] $\mathbb{R}^d \times \mathbb{R} \to \mathbb{R}$ whose [[sections]] are [[trajectories]] in [[Cartesian space]] $\mathbb{R}^d$ (the [[field bundle]] for the 1d [[sigma-model]] with [[target space]] $\mathbb{R}^d$).

Among the $H$-[[left invariant differential 2-forms]] on $H$ is 

$$
  \omega_m \coloneqq m (d_{dR} x - \dot x d_{dR} t) \wedge d_{dR} \dot x
$$

for some $m \in \mathbb{R}$ (where a contraction of vectors is understood).

This is a representative of a degree-2 [[cocycle]] in the [[Lie algebra cohomology]] of $Lie(H)$. We may regard this as the [[curvature]] of a [[connection on a bundle|connection]] [[differential 1-form|1-form]]

$$
  A \coloneqq m \dot x (d_{dR} x - \frac{1}{2} \dot x d_{dR} t)
  \,.
$$

Hence the value of the [[action functional]] of the corresponding 1d pure (topological) WZW model on a field configuration is 

$$
   m \int_{\Sigma_1} \dot  x (d_{dR} x - \frac{1}{2} \dot x d_{dR} t)
   =
   m \int_{\Sigma_1} \frac{\partial L}{ \partial \dot x}(d x - \dot x)+ L d t
  \,,
$$

where $L(x, \dot x) d t = \frac{1}{2}m \dot x^2 d t$ is the [[Lagrangian]] of the the free [[non-relativistic particle]] of [[mass]] $m$.

Evaluated on [[jet prolongations]] of [[sections]] of the [[field bundle]], for which the relation $d x = \dot x d t$ holds, then the first term of this expression vanishes and so the resulting WZW-type [[action functional]] is that of the free [[non-relativistic particle]].

See ([Azcarraga-Izqierdo, section 8.3](#AzcarragaIzqierdo)) for a useful account.

## References


* {#AzcarragaIzqierdo} [[José de Azcárraga]], J. Izqierdo, sections 8.3 and 8.7 of  _[[Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics]]_, Cambridge monographs of mathematical physics, (1995)
 
[[!redirects 1d WZW models]]