+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
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
 
In the [[first order formulation of gravity]] the field of [[gravity]] is modeled by a [[connection]] with values in the [[Poincaré Lie algebra]]. Such a connection locally decomposes into a $\mathbb{R}^{d,1}$-[[Lie algebra valued 1-form]] called the _[[vielbein]]_ and a [[special orthogonal Lie algebra|so(d,1)]]-[[Lie algebra valued 1-form|valued 1-form]] called the _[[spin connection]]_ piece. 

There is a constraint on this data. Usually the $so(d,1)$-connection is required to be the [[Levi-Civita connection]] corresponding to the [[pseudo-Riemannian metric]] encoded by the vielbein, hence the unique metric compatible connection with vanishing [[torsion]] but in general non-vanishing curvature.

But to some extent one may instead impose a dual constraint and demand the connection to be the _[[Weitzenböck connection]]_, which has vanishing [[curvature]], but in general non-vanishing [[torsion]]. This formulation of gravity is called _teleparallel gravity_, because by flatness of the connection, its [[parallel transport]] is trivial and hence [[tangent vectors]] at different points of [[spacetime]] may consistently be compared without specifying a [[path groupoid|path]] between them, hence without first [[parallel transport|parallel transporting]] one to the other. This "parallelism at a distance" is what gives teleparallel gravity its name. 

Notice that under some conditions a manifold being flat (i.e. admitting a [[flat connection]] on its tangent bundle) implies that it is a [[parallelizable manifold]], hence that the tangent bundle is actually trivializable. Sufficient such condition is notably that the flat manifold is also [[simply connected topological space|simply connected]], but this may be relaxed ([Thorpe 65](#Thorpe65)). Some authors may explicitly assume for teleparallel gravity that the tangent bundle is trivialized by the [[vielbein field]] (making it a [[framed manifold]]), though authors in the physics literature tend to be vague on this point.

At least without coupling to matter, the teleparallel formulation is locally classically equivalent to the ordinary formulation in [[first order formulation of gravity]] in that inserting in the [[Euler-Lagrange equations]] for the [[vielbein]]+[[Weitzenböck connection]] the expression of the latter in terms of the [[Levi-Civita connection]] one reaobtains the ordinary [[Einstein equations]].

Despite this equivalence, the map of the formal field content of teleparallel gravity to its physical interpretation has a rather different feel to it than in the ordinary formulation. Where ordinarily the field of gravity does not quite affect the motion of bodies like an ordinary [[force]] in Newtonian physics, but instead by [[curvature]] causing non-trivial [[geodesics]], in the teleparallel description the curvature does vanish just as in newtonian physics, and instead the [[torsion]] of the connection acts like a genuine Newtonian force.


## References

Review and survey:

* J. Pereira, _Torsion and the description of the gravitational interaction_ ([pdf slides](http://www.phys.sinica.edu.tw/~heptheory/files/pereira.pdf))

* R. Aldrovandi, J. G. Pereira, K. H. Vu, _Gravitation without the equivalence principle_ ([arXiv:gr-qc/0304106](http://arxiv.org/abs/gr-qc/0304106))

* Manuel Hohmann, *Teleparallel gravity*, in *Signatures and experimental searches for modified and quantum gravity* &lbrack;[arXiv:2207.06438](https://arxiv.org/abs/2207.06438)&rbrack;


Further discussion:

* R. Aldrovandi, J. G. Pereira, and K. H. Vu, _Selected topics in teleparallel gravity_ Brazilian Journal of Physics, vol. 34, no. 4A, (2004) ([pdf](http://www.sbfisica.org.br/bjp/files/v34_1374.pdf))

The [[Schwarzschild spacetime]] in the context of teleparallel gravity is discussed in 

* Gheorghe Zet, _Schwarzschild solution on spacetime with torsion_ ([arXiv:gr-qc/0308078](http://arxiv.org/abs/gr-qc/0308078))


The relation between flat tangent connections and parallelizablity is discussed in 

* {#Thorpe65} [[John Thorpe]], _Parallelizablility and flat manifolds_, 1965 ([[ThorpeParallelizable.pdf:file]])