
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Yang--Mills theory is a [[gauge theory]] on a given 4-[[dimensional]] ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian manifold|Riemannian]] [[manifold]] $X$ whose field is the [[Yang–Mills field]] -- a cocycle $\nabla \in \mathbf{H}(X,\bar \mathbf{B}U(n))$ in differential [[nonabelian cohomology]] represented by a [[vector bundle]] [[connection on a bundle|with connection]] -- and whose [[action functional]] is 

$$
  \nabla \mapsto
  \frac{1}{e^2 }\int_X F_\nabla \wedge \star F_\nabla  + i \theta \int_X F_\nabla \wedge F_\nabla
$$

for 

* $F_\nabla$ the [[field strength]], locally the [[curvature]] $\mathfrak{u}(n)$-[[Lie algebra valued differential form]] on $X$ ( with $\mathfrak{u}(n)$ the [[Lie algebra]] of the [[unitary group]] $U(n)$);

* $\star$ the [[Hodge star]] operator of the metric  $g$;

* $\frac{1}{e^2}$ and $\theta$ some [[real number]]s (see [[S-duality]])

## Applications

All gauge fields in the [[standard model of particle physics]] as well as in [[GUT]] models are Yang--Mills fields.

The matter fields in the standard model are spinors charged under the Yang-Mills field. See

* [[spinors in Yang-Mills theory]]

## Related concepts


* [[standard model of particle physics]]

  * [[electromagnetism]]

  * [[spinors in Yang-Mills theory]]

  * [[QED]], [[QCD]]

* [[super Yang-Mills theory]]

* [[S-duality]], [[Montonen-Olive duality]]

  * [[electric-magnetic duality]]

  * [[geometric Langlands duality]]

* [[Chern-Simons theory]]

* [[Yang-Mills instanton]]

## References

### General

* [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_ ([pdf](http://www.claymath.org/millennium/Yang-Mills_Theory/yangmills.pdf))

* [[Simon Donaldson]], _Yang-Mills theory and geometry_ (2005) [pdf](http://www2.imperial.ac.uk/~skdona/YMILLS.PDF)

For the relation to [[instanton Floer homology]] see also

* [[Simon Donaldson]], _Floer homology groups in Yang-Mills theory_ Cambridge University Press (2002) ([pdf](http://catdir.loc.gov/catdir/samples/cam031/2001035888.pdf))

### Classical solutions

Wu and Yang (1968) found a static solution to the sourceless $SU(2)$ Yang-Mills equations. Recent references include

* J. A. O. Marinho, O. Oliveira, B. V. Carlson, T. Frederico, _Revisiting the Wu-Yang Monopole: classical solutions and conformal invariance_ 

	
There is an old review, 

* Alfred Actor, _Classical solutions of $SU(2)$ Yang&#8212;Mills theories_, Rev. Mod. Phys. 51, 461&#8211;525 (1979), 

that provides some of the known solutions of $SU(2)$ gauge theory in [[Minkowski spacetime|Minkowski]] ([[monopoles]], plane waves, etc) and [[Euclidean space]] ([[instantons]] and their cousins). For general [[gauge groups]] one can get solutions by embedding $SU(2)$'s. For instantons the most general solution is known, first worked out by

* [[Michael Atiyah]], [[Nigel Hitchin]], [[Vladimir Drinfeld]], [[Yuri Manin]], _Construction of instantons_, Physics Letters 65 A, 3, 185--187 (1978) [pdf](http://www.new.ox.ac.uk/system/files/ADHM.pdf)

for the [[classical groups]] [[special unitary group|SU]], [[special orthogonal group|SO]] , [[Symplectic group|Sp]], and then by 

* C. Bernard, N. Christ, A. Guth, E. Weinberg, _Pseudoparticle Parameters for Arbitrary Gauge Groups_, Phys. Rev. __D16__, 2977 (1977)  

for exceptional groups. The latest twist on the instanton story is the construction of solutions with non-trivial [[holonomy]]: 

* Thomas C. Kraan, Pierre van Baal, _Periodic instantons with nontrivial holonomy_, Nucl.Phys. B533 (1998) 627-659, [hep-th/9805168](http://arxiv.org/abs/hep-th/9805168)

There is a nice set of lecture notes 

* David Tong, _TASI Lectures on Solitons_ ([hep-th/0509216](http://arxiv.org/abs/hep-th/0509216)), 

on topological solutions with different co-dimension (instantons, monopoles, vortices, domain walls). Note, however, that except for instantons these solutions typically require extra scalars and broken U(1)'s, as one  may find in [[super Yang-Mills theories]].

Some of the material used here has been taken from 

* [TP.SE](http://theoreticalphysics.stackexchange.com/), _[Which exact solutions of the classical Yang-Mills equations are known?](http://theoreticalphysics.stackexchange.com/questions/317/which-exact-solutions-of-the-classical-yang-mills-equations-are-known)_ 

Another model featuring Yang-Mills fields has been proposed by Curci and Ferrari, see [[Curci-Ferrari model]].

[[!redirects Yang--Mills theory]]
[[!redirects Yang–Mills theory]]
[[!redirects Yang-Mills action]]
[[!redirects Yang-Mills action functional]]

