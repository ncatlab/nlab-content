
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
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

What is called _Einstein-Yang-Mills theory_  in [[physics]] is the [[theory (physics)|theory]]/[[model (in theoretical physics)|model]] describing [[gravity]] together with [[Yang-Mills fields]] such as the [[electroweak field]] or the [[strong nuclear force]] of [[quantum chromodynamics]]. For the special case that the [[gauge group]] is the [[circle group]] this reproduces [[Einstein-Maxwell theory]].

Einstein-Yang-Mills theory is a [[local Lagrangian]] [[field (physics)|field]] theory defined by the [[action functional]] which is the [[Einstein-Hilbert action]] plus the [[Yang-Mills action functional]] involving the given metric,

$$
  S_{G+YM}
  \;
   \colon
  \;
  (e, \nabla)
  \mapsto
  \int_{X} R(e) vol(e)
  + 
  \int_X \langle F_\nabla \wedge \star_e F_\nabla\rangle
  \,,
$$

where 

* $X$ is the [[compact topological space|compact]] [[smooth manifold]] underlying [[spacetime]], 

* $e$ is the [[vielbein field]] which encodes the [[field (physics)|field]] of [[gravity]] 

* $\nabla$ is the $G$-[[principal connection]] which encodes the [[Yang-Mills field]], 

* $vol(e)$ is the [[volume form]] induced by $e$;

* $R(e)$ is the [[scalar curvature]] of $e$;

* $F_\nabla$ is the [[field strength]]/[[curvature]] [[differential 2-form]] of $\nabla$;

* $\star_e$ is the [[Hodge star]] operator induced by $e$.

* $\langle -,-\rangle$ is the given [[invariant polynomial]] on the [[Lie algebra]] of the [[gauge group]].

## Related concepts

[[!include Yang-Mills theory -- table]]

* [[charged black hole]]

* [[Einstein-Hilbert action]]

* [[Einstein-Maxwell theory]]

[[!include standard model of fundamental physics - table]]


## References

Section _[Prequantum gauge theory and Gravity](geometry+of+physics#ActionFunctionalsForChernSimonsTypeGaugeTheories)_ in 

* _[[geometry of physics]]_

On [[Yang-Mills monopoles]]:

* Jefferson Bjoraker, [[Yutaka Hosotani]], *Monopoles, Dyons and Black Holes in the Four-Dimensional Einstein-Yang-Mills Theory*, Phys. Rev. D **62** 043513 (2000) &lbrack;[arXiv:hep-th/0002098](https://arxiv.org/abs/hep-th/0002098), [doi:10.1103/PhysRevD.62.043513](https://doi.org/10.1103/PhysRevD.62.043513)&rbrack;

Solutions in [[Einstein-Yang-Mills theory]]:

* {#BartnikMcKinnon88} [[Robert Bartnik]], [[John McKinnon]], _Particle-like solutions of the Einstein-Yang-Mills equations_, Phys. Rev. Lett., **61**, pp. 141-144 (1988) &lbrack;[doi:10.1103/PhysRevLett.61.141](https://doi.org/10.1103/PhysRevLett.61.141) [bibcode:1988PhRvL..61..141B](https://ui.adsabs.harvard.edu/abs/1988PhRvL..61..141B/abstract)&rbrack;

* {#SmollerWassermanYauMcLeod92} [[Joel Smoller]], [[Arthur Wasserman]], [[Shing-Tung Yau]], J. Bryce McLeod, _Smooth static solutions of the Einstein-Yang/Mills equation_, Bull. Amer. Math. Soc. (N.S.) **27**, pp. 239-242 (1992) &lbrack;[arXiv:math/9210226](https://arxiv.org/abs/math/9210226) [doi:10.1007/BF02097002](https://doi.org/10.1007/BF02097002)&rbrack;

*  {#SmollerWasserman93} [[Joel Smoller]], [[Arthur Wasserman]], _Existence of infinitely-many smooth, static global solutions of the Einstein-Yang-Mills equations_, Commun. Math. Phys. **51**, pp. 303-325 (1993) &lbrack;[doi:10.1007/BF02096771](https://link.springer.com/article/10.1007/BF02096771) [pdf](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-151/issue-2/Existence-of-infinitely-many-smooth-static-global-solutions-of-the/cmp/1104252139.pdf)&rbrack;

* {#SmollerWassermanYau93} [[Joel Smoller]], [[Arthur Wasserman]], [[Shing-Tung Yau]], _Existence of black hole solutions for the Einstein-Yang-Mills equations_, Commun. Math. Phys. **154**, pp. 377-401 (1993) &lbrack;[doi:10.1007/BF02097002](https://link.springer.com/article/10.1007/BF02097002) [pdf](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-154/issue-2/Existence-of-black-hole-solutions-for-the-Einstein-Yang-Mills/cmp/1104252975.pdf)&rbrack;

* {#SmollerWasserman93} [[Joel Smoller]], [[Arthur Wasserman]], _Regular solutions of the Einstein Yang-Mills equations_, J. Math. Phys. **36**, pp. 4301-4323 (1995) &lbrack;[doi:10.1063/1.530963](https://pubs.aip.org/jmp/article/36/8/4301/230386/Regular-solutions-of-the-Einstein-Yang-Mills)&rbrack;

* {#SmollerWasserman95} [[Joel Smoller]], [[Arthur Wasserman]], _Uniqueness of extreme Reissner-Nordstrom solution in SU(2) Einstein-Yang-Mills theory for spherically symmetric space-time_, Phys. Rev., D **52**, pp. 5812-5815 (1995) &lbrack;[doi:10.1103/PhysRevD.52.5812](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.52.5812)&rbrack; 

* {#SmollerWasserman95} [[Joel Smoller]], [[Arthur Wasserman]], _Investigation of the Interior of Colored Black Holes and the Extendability of Solutions of the Einstein-Yang/Mills Equations_, Commun. Math. Phys. **194** pp. 707-732 (1998) &lbrack;[arXiv:gr-qc/9706039](https://arxiv.org/abs/gr-qc/9706039) [doi:10.1007/s002200050375](https://doi.org/10.1007/s002200050375)&rbrack;

* {#FisherOliynyk11} [[Mark Fisher]], [[Todd Oliynyk]], _There are no magnetically charged particle-like solutions of the Einstein Yang-Mills equations for Abelian models_, Commun. Math. Phys. **312**, pp. 137-177 (2012) &lbrack;[arXiv:1104.0449](https://arxiv.org/abs/1104.0449) [doi:10.1007/s00220-011-1388-5](https://doi.org/10.1007/s00220-011-1388-5)&rbrack;

[[!redirects Einstein-Yang-Mills theories]]
