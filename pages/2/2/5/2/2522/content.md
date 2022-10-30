
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
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

A [[symmetry]] is (in most classical situations) invariance under a [[group]] [[action]], or [[infinitesimal space|infinitesimally]], invariance under a [[Lie algebra]] action.

In the general sense of the word, a **supersymmetry** is invariance under a [[supergroup]] action or a [[super Lie algebra]] action. 

In the stricter sense of the word as it originates in theoretical fundamental [[physics]], _supersymmetry_ refers specifically to [[Lie superalgebra]] extensions of the [[Poincaré Lie algebra]] -- the [[super Poincaré Lie algebra]], often called the **supersymmetry algebra** in this context. An odd element in this [[super Lie algebra]] is called a **supersymmetry generator**.

### Global supersymmetry and superparticles

By Wigner-Weyl theory we have in ordinary [[quantum field theory]] that [[unitary representations of the Poincare group]] correspond to the [[particle]]s in the theory. For a _globally_ supersymmetric quantum field theory the [[Poincare group]] here is replaced by the [[super Poincare group]] and accordingly particles are now [[irreducible representation]]s of this group. The new -- odd graded -- representations appearing this way are called the **superpartners** of the original _bosonic_ particles.

### Local supersymmetry: supergravity

To be distinguished from this _global supersymmetry_ is _local supersymmetry_ :  given a [[gauge theory]] whose fields are [[connection on a bundle|connections]] with values in the [[Poincaré Lie algebra]] -- the theory of [[gravity]] in its [[first order formulation of gravity|first order formulation]] -- a supersymmetric extension_ is similarly a [[gauge theory]] with fields being connections in the [[super Poincaré Lie algebra]] -- a theory of [[supergravity]]. A [[gauge transformation]] in such a theory is called a **local supersymmetry transformation**.

### The relation between local and global supersymmetry

The distinction between local and global supersymmetry is important when considering [[supergravity]] in [[perturbation theory]] where all fields are expanded around a fixed [[spacetime]] [[geometry]] and fixed [[background gauge fields]] that form a solution of the [[Euler-Lagrange equations]].

While the theory of supergravity as such has, by definition, local supersymmetry, a solution to it may but need not have any _global supersymmetry_ left. In fact, generically it will not.

To see this, it is maybe helpful to compare with the analogous statement in non-supersymmetric [[QFT]]:

the theory of [[gravity]] is _locally_ Poincar&#233;-symmetric: in [[first order formulation of gravity|first order formulation]] it is a [[Poincare group]] [[gauge theory]]. Nevertheless, any of its solutions -- which is a [[pseudo-Riemannian manifold]] -- may, but need not, have any Poincar&#233;-symmetry. It does have such a _global_ symmetry for every [[Killing vector]] on the [[spacetime]]. Such may or may not exist. Generically it does not exist.

The analog of these Killing vectors in [[supergravity]] are [[Killing spinor]]s: [[covariantly constant spinor]]s ([[section]]s of a 
[[spinor bundle]] annihilated by the [[spin connection]]'s [[covariant derivative]]).
For every such, the background has one global supersymmetry transformation. These may or may not exist. Generically they do not.

The most famous example of this is that of [[Calabi-Yau manifolds]]: a  standard assumption on [[phenomenological|phenomenology]] [[model building]] that used to be very popular around the turn of the millenium (but is maybe experimentally ruled out at the time of this writing) is that 

1. the [[spacetime]] we see around us locally looks like a product $M^4 \times Y^6$ of 4-dimensional [[Minkowski space]] times a tiny closed [[Riemannian manifold]] $Y^6$ (so tiny that it is not directly observable but manifests itself only by way of its lowest excitation modes that look like different [[particle]] species on the remaining $M^4$ -- see [[Kaluza-Klein mechanism]] );

1. such that on this product space a single covariant constant spinor exists, such that the resulting effective theory on $M^4$ has a single global supersymmetry ("$N=1$ supersymmetry").

One finds that this condition is solved precisely by $Y^6$ being a [[Calabi-Yau manifold]]. For more on this see the corresponding section at [[heterotic string theory]].

But notice that nothing in the theory of 10-dimensional [[supergravity]] _demands_ that its solutions have a global supersymmetry left (generically they will not) nor that they factor locally as $M^4 \times Y^6$. All this is an _ansatz_ a _phenomenological model_ . It only says that _if_ we make this ansatz, then $Y^6$ needs to be a Calabi-Yau space. In fact, it turns out to be nontrivial to check that with all the other fields taken into account, such a factor ansatz is indeed consistent. (This problem of "moduli stabilization" is discussed a little bit at [[landscape of string theory vacua]].)

Latest experimental results strongly suggest that this model of global $(N = 1)$-supersymmetry at observable energies is not a desription of our phenomenological reality. Still, it could well be that the underlying theory of the world is nevertheless not plain [[general relativity]] but [[supergravity]].

### Observed supersymmetry: on the worldline

To appreciate this point it is worthwhile to notice that supersymmetric quantum field theory in fact _has_ been observed in nature, already since a century ago. To see this, one needs to notice how [[fundamental particle]]s are described by [[sigma model]] quantum field theories (see there) on their [[worldvolume]]:

the $\sigma$-model action functional for the standard Dirac [[spinor]] particle -- such as [[electron]]s and [[quarks]], the particles that all the matter in the world is made of -- just happens to have [[worldline supersymmetry]]. This is discussed at _[[spinning particle]]_ . Notice that this is true for electrons and quarks in the non-supersymmetric [[standard model of particle physics]]: the [[target space]] theory is completely void of (global) supersymmetry, and still the [[worldvolume]] theory of any [[fermion]] is automatically supersymmetric.


### Conjectured supersymmetry: on spacetime and on the worldsheet
 {#SupersymmetryOnSpacetimeAndWorldsheet}

A similar statement as for the [[spinning particle]] and its automatic local [[worldline supersymmetry]] indeed also holds for the _[[spinning string]]_ : while it is a conjecture of [[string theory]] which has not been experimentally verified that fundamentally the [[sigma-model]] theories that describe the physics around us is defined not on 1-dimensional but on 2-dimensional [[worldvolume]]s, it remains a noteworthy fact that the standard [[action functional]] for the [[string]] [[sigma model]] with [[fermion]]s _on the [[worldsheet]]_ just happens to be locally supersymmetric. It is hard to avoid this! And indeed, this was how the abstract notion of supersymmetry in [[quantum field theory]] was realized in the west first: people wrote down action functionals for _[[spinning string]]s_ and noticed that these happened to have an interesting graded symmetry (see there for references).

So while it is an open conjecture of [[string theory]] that the particle [[worldline]]s that are experimentally observed are secretly really [[worldsheet]]s, assuming that this conjecture holds for [[fermion]]s automatically implies local worldsheet supersymmetry and the [[superstring]].

Now, the effective [[spacetime]] [[target space]] theories arising from [[second quantization]] of the [[superstring]] are fairly well understood: these are higher dimensional [[supergravity]] theories coupled to the various [[background gauge field|higher gauge fields]] that are also in the spectrum of the string (the [[Kalb-Ramond field]] and the [[RR-field]]s, notably). They are called _[[type II supergravity]]_ , [[heterotic supergravity]], etc. All of these are obtained by compactifications of [[11-dimensional supergravity]].

This means that the assumption of [[spinning string]] [[sigma-models]] automatically implies that the [[spacetime]] [[QFT]] that we observe also has _local_ supersymmetry.

Over the decades it has often been suggested that therefore the assumption of [[spinning string]]s "suggests" or "favours" the observation of superpartner particles in accelerators. However, this is not so:

in thes constructions the [[particle]] species seen in accelerators are [[Kaluza-Klein mechanism|KK-modes]] and/or brane-brane open string modes of the compactified locally supersymmetric theory. This means that they are determined by the compactification geometry. Only if that has a global [[Killing spinor]] is the effective 4-dimensional theory globally supersymmetric and exhibits superpartners. As was mentioned above, for spacetimes of the form $M^4 \times Y^6$ this is the case precisely if $Y^6$ is a [[Calabi-Yau manifold]].

But this is far from being the generic situation. This is clearl qualitatively (a generic solution to the super-[[Einstein equations]] will not have a [[Killing spinor]]). A mor sophisticated and quantitative argument to the same extend is for instance given in ([DLSW08](#DLSW)).





### In fundamental physics

Supersymmetric extensions of [[quantum field theories]] have been felt to be compelling in fundamental physics for _formal reasons_ : the simple step from [[Lie algebra]]s to [[super Lie algebra]]s

* make a pure theory of [[gravity]] seamlessly incorporate [[fermion]]s and [[gauge field]]s;

* leads to better [[renormalization]] properties (indeed the speculation that $N=8, D=4$ [[supergravity]] is fully renormalizable -- in stark contrast to ordinary [[gravity]] has more recently been checked up to high loop orders);

* produces a wealth of interesting mathematical structures. For instance 

  * [[Morse theory]] of a [[Riemannian manifold]] can naturally be understood in terms of [[supersymmetric quantum mechanics]] for [[superparticle]]s propagating on that manifold;

  * the interpretation of [[quantum field theories]] in terms of [[generalized cohomology]] theories only works for supersymmetric theories (see [[(1,1)-dimensional Euclidean field theories and K-theory
]] and [[(2,1)-dimensional Euclidean field theory]])

  * "topological twists" of supersymmetric field theories are a major source of examples of [[TQFT]]s, for instance the [[A-model]] and the [[B-model]] [[TCFT]] arise from such twists of 2-dimensional [[supergravity]] and there are deep connections between the [[geometric Langlands correspondence]] and topologically twisted [[super Yang-Mills theory]].

Moreover, since various observables in supersymmetric QFTs are easier to compute than in non-supersymmetric theories, supersymmetric quantum field theory is being used to _approximate_ certain aspects of other QFTs. For instance certain correlators in ordinary [[Yang-Mills theory]] coupled to [[spinors in Yang-Mills theory]] can be computed using an auxioary [[super Yang-Mills theory]].

Therefore, if nothing else, supersymmetric quantum field theories constitute a part of the whole space of quantum field theories which is useful for understanding general properties of that space. What is however still missing is any experimental evidence that the world is fundamentally described by a supersymmetric quantum field theory.

## Examples

* [[supergravity]]

* [[super Yang-Mills theory]]

* [[spinning particle]] (which happens to have [[worldline supersymmetry]])

* [[superparticle]]

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

* [[spinning string]] [[superstring]]

  * [[heterotic string]], [[type II superstring]]

  * [[(2,1)-dimensional Euclidean field theories and tmf]]


## History

The notion of Poincar&#233; supersymmetry was found in parallel by two groups in the 1970s (separated and isolated at that time by "Cold War" nuisances):

Neveu, [[Pierre Ramond]] and [[John Schwarz]] wrote down in 1971 the system called the [[spinning string]] -- a 2-dimensional [[quantum field theory]] with [[fermion]]s and notice that it just so happens to have an extra graded extension of 2-dimensional Poincar&#233; symmetry.

Around the same time Golfand and Likhtman in Russia wrote down the [[super Poincare Lie algebra]] in four dimensions. This then motivated [[Julius Wess]] and Zumino to study supersymmetric QFTs in four dimensions. (see the account by ([Schwarz](#Schwarz)))

## References

A decent textbook reference for the general theory is for instance

* V. S. Varadarajan, _Supersymmetry for mathematicians: An introduction _ AMS (2004)

An account of the history of the development of supersymmetry is in

* [[John Schwarz]], _String theory origins of supersymmetry_, Nucl. Phys. Proc. Suppl. 101 (2001) 54-61 ([arXiv:hep-th/0011078](http://arxiv.org/abs/hep-th/0011078))

A quantitative analysis showing that locally supersymmetric [[spacetime]] theories will generically not exhibit global spacetime supersymmetry is

* [[Keith Dienes]], Michael Lennek, David S&#233;n&#233;chal, Vaibhav Wasnik, _Is SUSY Natural?_ NewJ.Phys.10:085003,2008 ([arXiv:0804.4718](http://arxiv.org/abs/0804.4718))
 {#DLSW}

[[!redirects supersymmetries]]

[[!redirects supersymmetry algebra]]
[[!redirects supersymmetry algebras]]


[[!redirects local supersymmetry]]
[[!redirects global supersymmetry]]

[[!redirects local supersymmetries]]
[[!redirects global supersymmetries]]
