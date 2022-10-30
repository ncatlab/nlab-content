
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
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

A [[quantum field theory]] of **supergravity** is similar to the theory of [[gravity]], but where (in [[first-order formulation of gravity|first order formulation]]) the latter is given by an [[action functional]] (the [[Einstein-Hilbert action]] functional) on the space of [[connection on a bundle|connection]]s (over [[spacetime]]) with values in the [[Poincare Lie algebra]] $\mathfrak{iso}(n,1)$, supergravity is defined by an extension of this to an action functional on the space connections with values in the [[super Poincare Lie algebra]] $\mathfrak{siso}(n,1)$. One says that supergravity is the theory of _local_ (Poincar&#233;) [[supersymmetry]] in the same sense that ordinary [[gravity]] is the theory of "local Poincar&#233;-symmetry". These are [[gauge theories]] for the [[Poincare Lie algebra]] and the [[super Poincare Lie algebra]], respectively:

if we write $\mathfrak{siso}(n,1)$ as a [[semidirect product]] of the translation Lie algebra $\mathbb{R}^{(n,1)}$, the [[special orthogonal Lie algebra]] $\mathfrak{so}(n,1)$ and a [[spin group]] [[representation]] $\Gamma$, then locally a connection is a [[Lie algebra valued 1-form]] 

$$
  A : T X \to \mathfrak{siso}(n,1)
$$

that decomposes into three components, $A = (E, \Omega, \Psi)$:

* a $\mathbb{R}^{n,1}$-valued 1-form $E$ -- the [[vielbein]] 

  (this encodes the [[pseudo-Riemannian metric]] and hence the field of [[gravity]]);

* a $\mathfrak{so}(n,1)$-valued 1-form $\Omega$ -- called the [[spin connection]];

* a $\Gamma$-valued 1-form $\Psi$ -- called the [[gravitino]] field.

Typically in fact the field content of supergravity is larger, in that a field $A$ is really an [[∞-Lie algebra-valued differential form]] with values in an [[∞-Lie algebra]] such as the [[supergravity Lie 3-algebra]] ([DAuriaFreCastellani](#DAuriaFreCastellani)) $\mathfrak{sugra}(10,1)$. Specifically such a field

$$
  A : T X \to \mathfrak{sugra}(10,1)
$$

has one more component

* a 3-form $C$ -- the [[supergravity C-field]].

The [[gauge transformation]]s on the space of such connections that are parameterized by the elements of $\Gamma$ are called [[supersymmetries]].

The condition of [[gauge invariance]] of an action functional on $\mathfrak{siso}$-connections is considerably more restrictive than for one on $\mathfrak{iso}$-connections. For instance there is, under mild assumptions, a _unique_ maximally supersymmetric supergravity extension of the ordinary [[Einstein-Hilbert action]] on a 4-dimensional manifold. This in turn is obtained from the _unique_ (under mild assumptions) maximally supersymmetric supergravity action functional on a (10,1)-dimensional [[spacetime]] by thinking of the 4-dimensional action function as being a [[dimensional reduction]] of the 11-dimensional one.

This uniqueness (under mild conditions) is one reason for interest in supergravity theories. Another important reason is that supergravity theories tend to remove some of the problems that are encountered when trying to realize [[gravity]] as a [[quantum field theory]]. Originally there had been high hopes that the maximally supersymmetric supergravity theory in 4-dimensions is fully [[renormalizable]]. This couldn't be shown computationally -- until recently: triggered by new insights recently there there has been lots of renewed activity on the renormalizability of maximal supergravity. 


## As a gauge theory

The non-spinorial part of [[action functional]]s of supergravity theories are typically given in [[first-order formulation of gravity|first order formulation]] as functional on a space of [[connection on a bundle|connections]] with values in the [[Poincare Lie algebra]] $\mathfrak{iso}(n,1)$. Including the fermionic fields, this becomes connections with values in the [[super Poincare Lie algebra]] $\mathfrak{siso}(10,1)$. 

This might suggest that supergravity is to be thought of as a [[gauge theory]]. There are indeed various action functionals of [[Chern-Simons theory]]-form for supergrvaity theories ([Zanelli](#Zanelli)). These yield theories whose bosonic action functional is the [[Einstein-Hilbert action]] in certain conctraction limits.

More generally ([DAuriaFreCastellani](#DauriaFreCastellani)) have shown that at least some versions, such as the maximal 11-dimensional supergravity are naturally understood as _higher_ gauge theories whose fields are [[∞-Lie algebra-valued forms]] with values in [[∞-Lie algebra]]s such as the [[supergravity Lie 3-algebra]]. This is described in detail at [[D'Auria-Fre formulation of supergravity]].

## Solutions with global supersymmetry
 {#SolutionsWithGlobalSupersymmetry}

A solution to the bosonic [[Einstein equations]] of ordinary [[gravity]] -- some [[Riemannian manifold]] -- has a _global symmetry_ if it has a [[Killing vector]].

Accordingly, a configuration that solves the supergravity [[Euler-Lagrange equations]] is a _[[global supersymmetry]]_ if it has a [[Killing spinor]]: a [[covariantly constant spinor]].

Here the notion of [[covariant derivative]] includes the usual [[Levi-Civita connection]], but also in general [[torsion]] components and contributions from other [[background gauge fields]] such as a [[Kalb-Ramond field]] and the [[RR-field]]s in [[type II string theory|type II supergravity]] or [[heterotic string theory|heterotic supergravity]].

Of particular interest to phenomenologists around the turn of the millenium (but maybe less so today with new experimental evidence) has been in solutions of spacetime manifolds of the form $M^4 \times Y^6$ for $M^4$ the locally observed [[Minkowski spacetime]] (that plays a role as the background for all available particle accelerator experiments) and a small closed 6-dimensional [[Riemannian manifold]] $Y^6$. 

In the absence of further fields besides gravity, the condition that such a configuration has precisely one [[Killing spinor]] and hence precisely one [[global supersymmetry]] turns out to tbe precisely that $Y^6$ is a [[Calabi-Yau manifold]]. This is where all the interest into these manifolds in [[string theory]] comes from. (Notice though that nothing in the theory itself demands such a compactification. It is only the phenomenological assumption of the factorized spacetime compactification together with $N = 1$ supersymmetry that does so).

More generally, in the presence of other [[background gauge field]]s, the Calabi-Yau condition here is deformed. One also speaks of [[generalized Calabi-Yau space]]s. (For instance ([GMPT05](#GMPT))).

For more see 

* [[supersymmetry and Calabi-Yau manifolds]]


## Examples

For supergravity Lagrangians "of ordinary type" it turns out that  

* $N = 1$ [[11-dimensional supergravity]] 

is the highest dimensional possible. All lower dimensional theories in this class appear as compactifications of this theory or otherwise derived from it, such as

* 10-dimensional [[type II supergravity]], [[heterotic supergravity]]

* [[7-dimensional supergravity]]

In dimension $(1+0)$ supergravity coupled to [[sigma-model]] fields is the [[spinning particle]].

In dimension $(1+1)$ supergravity coupled to [[sigma-model]] fields is the [[spinning string]]/[[NSR superstring]].

## Related concepts

* [[gauged supergravity]]

[[!include table of branes]]


## References

### General

A modern reference for the diverse flavours of supergravity theories is

* Antoine Van Proeyen, _Structure of supergravity theories_ ([arXiv:hep-th/0301005](http://arxiv.org/abs/hep-th/0301005))

A fair bit of detail on [[supersymmetry]] and on supergravity is in 

* [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

The original article that introduced the [[D'Auria-Fre formulation of supergravity]] is

* R. D'Auria, P. Fr&#233; _Geometric supergravity in $D = 11$ and its hidden supergroup_ [[GeometricSupergravity.pdf:file]]
 
The standard textbook monograph on supergravity and [[string theory]] using these tools is

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], [[Supergravity and Superstrings - A Geometric Perspective]]
{#DauriaFreCastellani}


### Gauged supergravity

* Natxo Alonso-Alberca; and Tom&#225;as Ort&#237;n, _Gauged/Massive supergravities in diverse dimensions_ ([pdf](http://digital.csic.es/bitstream/10261/38952/1/ARTICULOS302400%5B1%5D.pdf))

### Chern-Simons supergravity

A survey of the [[Chern-Simons gravity]]-style action functionals for supergravity is in

* Jorge Zanelli, _Lecture notes on Chern-Simons (super-)gravities_ ([arXiv:0502193](http://arxiv.org/abs/hep-th/0502193))
{#Zanelli}


### Related

Further physics monographs on supergravity include

* I. L. Buchbinder, S. M. Kuzenko, _Ideas and methods of supersymmetry and supergravity; or A walk through superspace_, [googB](http://books.google.com/books?isbn=0750305061)

* [[Julius Wess]], Jonathan Bagger, _Supersymmetry and supergravity_, 1992

* [[Steven Weinberg]], _Quantum theory of fields_, volume III: supersymmetry


The [[Cauchy problem]] for classical solutions of simple supergravity has been discussed in

* [[Yvonne Choquet-Bruhat]], 
  _[[The Cauchy Problem in Classical Supergravity]]_
  Letters in Mathematical Physics 7 (1983) 459-467. 0377

A canonical textbook reference for the role of Calabi-Yau manifolds in compactifications of 10-dimensional [[supergravity]] is volume II, starting on page 1091 in

* [[P. Deligne]], [[P. Etingof]], [[D. Freed]], L. Jeffrey, [[D. Kazhdan]], J. Morgan, D. R. Morrison and [[E. Witten]], eds. _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

Discussion of solutions with $N = 1$ global supersymmetry left and their relation to Calabi-Yau compactifications are for instance in 

* Mariana Gra&#241;a, Ruben Minasian, Michela Petrini, Alessandro Tomasiello, _Generalized structures of $N=1$ vacua_, [arXiv:hep-th/0505212](http://arxiv.org/abs/hep-th/0505212)
  {#GMPT}

[[!redirects supergravities]]