
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--





# Contents
* table of contents 
{:toc}

## Idea 

What is called the _AKSZ formalism_ -- after the initials of its four authors -- Alexandrov, [[Maxim Kontsevich]], [[Albert Schwarz]], Oleg Zaboronsky -- is a technique for constructing [[action functional]]s in [[BV-BRST formalism]]  for [[sigma model]] [[quantum field theories]] whose 
[[target space]] is an [[symplectic Lie n-algebroid]] $(\mathfrak{P}, \omega)$.

The [[action functional]] of AKSZ theory is that of [[∞-Chern-Simons theory]] induced from the [[Chern-Simons element]] that correspondonds to the [[invariant polynomial]] $\omega$. Details on this are at [∞-Chern-Simons theory -- Examples -- AKSZ theory](http://ncatlab.org/schreiber/show/infinity-Chern-Simons+theory+--+examples#ASKZTheory).

## Examples

* to a [[Poisson Lie algebroid]] corresponds the [[Poisson sigma-model]];

* the a [[Courant algebroid]] corresponds the [[Courant sigma-model]];

  in particular to a [[semisimple Lie algebra]] corresponds [[Chern-Simons theory]].

* [[BF-theory]]+[[topological Yang-Mills theory]], 


Als the [[A-model]] and the [[B-model]] topological 2d [[sigma-models]] are examples.


## Definition

A [[sigma-model]] [[quantum field theory]] is, roughly, one 

* whose fields are maps $\phi : \Sigma \to X$  to some space $X$;

* whose [[action functional]] is, apart from a 
  [[kinetic action|kinetic term]], the [[transgression]] 
  of some kind of [[cocycle]]  on $X$
  to the [[mapping space]] $\mathrm{Map}(\Sigma,X)$.

Here the terms "space", "maps" and "cocycles"
are to be made precise in a suitable context.
One says that $\Sigma$ is the _[[worldvolume]]_, 
$X$ is the _[[target space]]_ and the cocycle is
the _[[background gauge field]]_ .

For instance the ordinary charged [[particle]] 
(for instance an electron) is described by a $\sigma$-model 
where $\Sigma = (0,t) \subset \mathbb{R}$ is the abstract
_[[worldline]]_, where $X$ is a smooth
([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian manifold]]
(for instance our [[spacetime]]) and where the background cocycle
is a [[circle bundle]] with [[connection on a bundle|connection]] 
on $X$ (a degree-2 cocycle in [[ordinary differential cohomology]] of $X$, representing a background _[[electromagnetic field]]_ : 
up to a kinetic term the action functional is the [[holonomy]] of the connection over  a given [[curve]] $\phi : \Sigma \to X$. 

The $\sigma$-models to be considered here are 
_higher_ generalizations of this example,
where the background gauge field is a cocycle of higher degree
(a [[connection on an infinity-bundle|higher bundle with connection]]) 
and where the worldvolume is
accordingly higher dimensional -- and where $X$ is allowed to be 
not just a manifold but an approximation to a 
_higher [[orbifold]] (a [[smooth ∞-groupoid]]).

More precisely, here we take the [[category]] of [[space]]s
to be [[dg-geometry|smooth dg-manifolds]].
One may imagine that we can equip this 
with an [[internal hom]]
$\mathrm{Maps}(\Sigma,X)$ given by $\mathbb{Z}$-graded objects. 
Given [[dg-geometry|dg-manifolds]] $\Sigma$ and $X$ 
their canonical degree-1 vector fields
$v_\Sigma$ and $v_X$ acting on the mapping space from the
left and right. In this sense their linear combination 
$v_\Sigma + k \, v_X$ for some $k \in \mathbb{R}$
equips also $\mathrm{Maps}(\Sigma,X)$ with the structure of 
a differential graded smooth manifold.

Moreover, we take the "cocycle" on $X$ to be a 
graded [[symplectic structure]] $\omega$, 
and assume that there is a kind of Riemannian structure on $\Sigma$
that allows to form the [[transgression]]

$$
  \int_\Sigma \mathrm{ev}^* \omega
  :=
  p_! \mathrm{ev}^* \omega
$$

by [[integral transform|pull-push]] through the canonical 
[[correspondence]]

$$
  \mathrm{Maps}(\Sigma,X)
  \stackrel{p}{\leftarrow}
  \mathrm{Maps}(\Sigma,X) \times \Sigma
  \stackrel{ev}{\to}
   X
  \,,
$$

where on the right we have the [[evaluation map]].

Assuming that one succeeds in making precise sense of all this 
one expects to 
find that $\int_\Sigma \mathrm{ev}^* \omega$ is in turn a symplectic 
structure on the mapping space. This implies that the vector field
$v_\Sigma + k\, v_X$ on mapping space has a 
[[Hamiltonian]] 
$\mathbf{S} \in C^\infty(\mathrm{Maps}(\Sigma,X))$.
The grade-0 components $S_{\mathrm{AKSZ}}$ of $\mathbf{S}$ 
then constitute a functional on the space
of maps of graded manifolds $\Sigma \to X$. This is
the **AKSZ action functional** defining the AKSZ $\sigma$-model
with target space $X$ and background field/cocycle $\omega$.

In ([AKSZ](#AKSZ)) this procedure is indicated only somewhat vaguely. 
The focus of attention there is a discussion, from this perspective,
of the action functionals
of the 2-dimensional $\sigma$-models called the 
_[[A-model]]_ and the _[[B-model]]_ .

In ([Roytenberg](#Roytenberg)), a more detailed discussion of the general construction is given, including an explicit 
and general formula for $\mathbf{S}$ and hence for $S_{\mathrm{AKSZ}}$ . 
For $\{x^a\}$ a coordinate chart on $X$ that formula is
the following.


+-- {: .num_defn #TheAKSZAction}
###### Definition

For $(X,\omega)$ a [[symplectic Lie n-algebroid|symplectic dg-manifold]] of grade $n$, $\Sigma$ a smooth compact manifold of dimension $(n+1)$
and $k \in \mathbb{R}$, the
**AKSZ action functional**

$$
  S_{\mathrm{AKSZ},k} : 
   \mathrm{SmoothGrMfd}(\mathfrak{T}\Sigma, X)
  \to
  \mathbb{R}
$$

(where $\mathfrak{T}\Sigma$ is the shifted tangent bundle)

is

$$
  S_{\mathrm{AKSZ},k} 
   :
  \phi
  \mapsto
  \int_\Sigma 
  \left(
    \frac{1}{2}\omega_{ab} \phi^a \wedge d_{\mathrm{dR}}\phi^b
    + 
    k
    \,
    \phi^* \pi
  \right)
  \,,
$$

where $\pi$ is the [[Hamiltonian]] for $v_X$ with respect to $\omega$
and where on the right we are interpreting fields as forms on $\Sigma$.

=--

This formula hence defines an infinite class of $\sigma$-models
depending on the target space structure $(X, \omega)$, and on the 
relative factor $k \in \mathbb{R}$.  In ([AKSZ](#AKSZ)) it was
already noticed that ordinary [[Chern-Simons theory]] is a special
case of this for $\omega$ of grade 2,  as is the 
[[Poisson sigma-model]]
for $\omega$ of grade 1 (and hence, as shown there, also the [[A-model]]
and the [[B-model]]). 
The main example in ([Roytenberg](#Roytenberg)) is spelling out the
general case for $\omega$ of grade 2, which is called the
_[[Courant sigma-model]]_ there. 

One nice aspect of this construction is that it follows immediately
that the full Hamiltonian $\mathbf{S}$ on mapping space satisfies
$\{\mathbf{S}, \mathbf{S}\} = 0$. Moreover, using the standard formula
for the internal hom of chain complexes one finds that the cohomology
of $(\mathrm{Maps}(\Sigma,X), v_\Sigma + k v_X)$ in degree 0
is the space of functions on those fields that satisfy the 
[[Euler-Lagrange equations]] of $S_{\mathrm{AKSZ}}$. 
Taken together this implies that 
$\mathbf{S}$ is a solution of the "master equation"
of a [[BV-BRST complex]] for the quantum field theory
defined by $S_{\mathrm{AKSZ}}$. This is a crucial ingredient for the 
quantization of the model, and this is what the AKSZ construction
is mostly used for in the literature.

## Related concepts

* [[sigma-model]]

* [[schreiber:infinity-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[2d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[11d Chern-Simons theory]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

  * **AKSZ $\sigma$-model**

    * [[Poisson sigma-model]]

      * [[A-model]], [[B-model]]

    * [[Courant sigma-model]]

      * [[Chern-Simons theory]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References 

The original reference is 

* M. Alexandrov, [[Maxim Kontsevich|M. Kontsevich]], [[Albert Schwarz|A. Schwarz]], O. Zaboronsky, _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405--1429, 1997 ([arXiv:hep-th/9502010](http://arxiv.org/abs/hep-th/9502010))
 {#AKSZ}

Dmitry Roytenberg wrote a useful exposition of the central idea of the original work and studied the case of the [[Courant sigma-model]] in

* [[Dmitry Roytenberg]], _AKSZ-BV Formalism and Courant Algebroid-induced Topological Field Theories_ Lett.Math.Phys.79:143-159,2007 ([arXiv](http://arxiv.org/abs/hep-th/0608150)).
 {#Roytenberg}

Other reviews include

* [[Noriaki Ikeda]], _Deformation of graded (Batalin-Volkvisky) Structures_ in Dito, Lu, Maeda, Weinstein (eds.) _Poisson geometry in mathematics and physics_ Contemp. Math. 450, AMS (2008) 


* [[Noriaki Ikeda]], _Lectures on AKSZ Topological Field Theories for Physicists_ ([arXiv:1204.3714](http://arxiv.org/abs/1204.3714))

A cohomological reduction of the formalism is described in 

* F. Bonechi, P. Mn&#235;v, [[Maxim Zabzine]], _Finite dimensional AKSZ-BV-theories_ ([arXiv](http://arxiv.org/abs/0903.0995))

That the AKSZ action on bounding manifolds $\partial \hat \Sigma$ is the integral of the graded symplectic form over $\hat \Sigma$ is theorem 4.4 in 

* A. Kotov, T. Strobl, _Characteristic classes associated to Q-bundles_ ([arXiv:0711.4106v1](http://arxiv.org/abs/0711.4106v1))

The discussion of the AKSZ action functional as the [[nLab:∞-Chern-Simons theory]]-functional induced from a [[symplectic Lie n-algebroid]] in [[∞-Chern-Weil theory]] is due discussed in

* [[nLab:Domenico Fiorenza]], [[nLab:Chris Rogers]], [[nLab:Urs Schreiber]], _[[schreiber:AKSZ Sigma-Models in Higher Chern-Weil Theory]]_

In the broader context of smooth [[higher geometry]] this is discussed in section 4.3 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

See also

* Peter Bouwknegt, [[Branislav Jur?o]], _AKSZ construction of topological open p-brane action and Nambu brackets_, [arxiv/1110.0134](http://arxiv.org/abs/1110.0134)

* Theodore Th. Voronov, _Vector fields on mapping spaces and a converse to the AKSZ construction_, [arxiv/1211.6319](http://arxiv.org/abs/1211.6319)

[[!redirects AKSZ sigma-models]]
[[!redirects AKSZ sigma model]]
[[!redirects AKSZ functional]]
[[!redirects AKSZ model]]
[[!redirects AKSZ formalism]]
[[!redirects AKSZ theory]]
[[!redirects AKSZ]]