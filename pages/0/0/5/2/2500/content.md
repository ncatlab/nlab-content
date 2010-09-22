
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A [[quantum field theory]] of **supergravity** is similar to the theory of [[gravity]], but where (in [[first-order formulation of gravity|first order formulation]]) the latter is given by an [[action functional]] (the [[Einstein-Hilbert action]] functional) on the space of [[connection on a bundle|connection]]s (over [[spacetime]]) with values in the [[Poincare Lie algebra]] $\mathfrak{iso}(n,1)$, supergravity is defined by an extension of this to an action functional on the space connections with values in the [[super Poincare Lie algebra]] $\mathfrak{siso}(n,1)$:

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

More generally ([DAuriaFreCastellani](#DauriaFreCastellani)) have shows that at least some versions, such as the maximal 11-dimensional supergravity are naturally understood as _higher_ gauge theories whose fields are [[∞-Lie algebra-valued forms]] with values in [[∞-Lie algebra]]s such as the [[supergravity Lie 3-algebra]]. This is described in detail at [[D'Auria-Fre formulation of supergravity]].


## References

A systematic mathematical treatment of supersymmetry and of supergravity solutions is in 

* [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]], eds.  _Quantum fields and strings, A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

The original article that introduced the [[D'Auria-Fre formulation of supergravity]] is

* R. D'Auria, P. Fr&#233; _Geometric supergravity in $D = 11$ and its hidden supergroup_ [[GeometricSupergravity.pdf:file]]
 
The standard textbook monograph on supergravity and [[string theory]] using these tools is

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], [[Supergravity and Superstrings - A Geometric Perspective]]
{#DauriaFreCastellani}


A survey of the [[Chern-Simons theory]]-style action functionals for supergravity is in

* Jorge Zanelli, _Lecture notes on Chern-Simons (super-)gravities_ [arXiv:0502193](http://arxiv.org/abs/hep-th/0502193)
{#Zanelli}



Furher physics monographs on supergravity include

* I. L. Buchbinder, S. M. Kuzenko, _Ideas and methods of supersymmetry and supergravity; or A walk through superspace_, [googB](http://books.google.com/books?isbn=0750305061)

* [[Julius Wess]], Jonathan Bagger, _Supersymmetry and supergravity_, 1992

* [[Steven Weinberg]], _Quantum theory of fields_, volume III: supersymmetry

[[!redirects supergravities]]