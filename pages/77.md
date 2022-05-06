+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Lie algebra_ is the [[infinitesimal object|infinitesimal]] approximation to a [[Lie group]]. 

## Definition

### Ordinary definition

A _Lie algebra_ is a [[vector space]] $\mathfrak{g}$ equipped with a bilinear skew-symmetric map $[-,-]  : \mathfrak{g} \wedge \mathfrak{g} \to \mathfrak{g}$ which satisfies the [[Jacobi identity]]:

$$
  \forall x,y,z \in \mathfrak{g} : \left[x,\left[y,z\right]\right] + \left[z,\left[x,y\right]\right] + \left[y,\left[z,x\right]\right] = 0
  \,.
$$

A [[homomorphism]] of Lie algebras is a linear map $\phi : \mathfrak{g} \to \mathfrak{h}$ such that for all $x,y \in \mathfrak{g}$ we have

$$
  \phi([x,y]_{\mathfrak{g}}) = [\phi(x),\phi(y)]_{\mathfrak{h}}
  \,.
$$

This defines the [[category]] [[LieAlg]] of Lie algebras.

### Internal to a general linear category
 {#InAGeneralLinearCategory}

The notion of _[[Lie algebra]]_ may be formulated [[internalization|internal to]] any [[linear category]]. This general definition subsumes variants of Lie algebras such as [[super Lie algebras]]. 

Consider a [[commutative unital ring]] $k$, and a (strict for simplicity) [[symmetric monoidal category|symmetric monoidal]] $k$-[[linear category]] $(\mathcal{C},\otimes,1)$ with [[braiding]] $\tau$.

A **[[Lie algebra object]]** in $(\mathcal{C},\otimes,1,\tau)$ is 

1. an [[object]] 

   $$
     L \in \mathcal{C}
   $$

1. [[morphism]] (the [[Lie bracket]])

   $$
     [-,-] \;\colon\; L \otimes L \to L
   $$

such that the following conditions hold:

1. [[Jacobi identity]]:

   $$
     \left[-,\left[-,-\right]\right]
       +
     \left[-,\left[-,-\right]\right]
     \circ(id_L\otimes\tau_{L,L})
     \circ(\tau\otimes id_L)
     +
     \left[-,\left[-,-\right]\right]
       \circ 
     (\tau_{L,L}\otimes id_L)\circ (id_L\otimes\tau_{L,L}) = 0
   $$ 

1. skew-symmetry:

   $$
     \begin{aligned}
       & 
       \phantom{+}
       [-,-]
       \\
       &
       +
       [-,-]\circ \tau_{L,L} 
       \\
       & = \phantom{+} 0
     \end{aligned}
   $$

Equivalently, Lie algebra objects  are the [[algebras over an operad]] over a certain quadratic [[operad]], called the [[Lie operad]], which is the [[Koszul dual]] of the [[commutative algebra operad]].


Examples of types of [[Lie algebra objects]]:

If $k$ is the ring $\mathbb{Z}$ of [[integers]] and $\mathcal{C} = $ $k$[[Mod]] = [[Ab]] is the [[category]] of [[abelian groups]] equipped with the [[tensor product of abelian groups]], then a Lie algebra object is called a _[[Lie ring]]_.

If $k$ is a [[field]] and $\mathcal{C} =$ [[Vect]] is the [[category]] of [[vector spaces]] over $k$ equipped with the [[tensor product of vector spaces]] then a Lie algebra object is an ordinary_[[Lie algebra|Lie k-algebra]]_. 

If $k$ is a [[field]] and $\mathcal{C}$ = [[sVect]] is the [[category]] of [[super vector spaces]] over $k$, then a Lie algebra object is a  _[[super Lie algebra]]_.



### General abstract perspective
 {#GeneralAbstractPerspective}

Lie algebras are equivalently groups in "[[infinitesimal space|infinitesimal]] geometry".

For instance in [[synthetic differential geometry]] then a Lie algebra of a [[Lie group]] is just the first-order infinitesimal neighbourhood of the unit element (e.g. [Kock 09, section 6](#Kock09)). 

More generally in geometric [[homotopy theory]], Lie algebras, being 0-truncated [[L-∞ algebras]] are equivalently "infinitesimal [[∞-group]] [[geometric ∞-stacks]]" (e.g. [here](infinitesimal+cohesive+(infinity,1)-topos#FormalModuliProblems)), also called [[formal moduli problems]] (see there for more). 

## Extra stuff, structure, properties

Notions of Lie algebras with extra [[stuff, structure, property]] includes

* extra property

  * [[abelian Lie algebra]]

  * [[simple Lie algebra]]

  * [[semisimple Lie algebra]]

  * [[reductive Lie algebra]]

* extra structure

  * [[super Lie algebra]]

* extra stuff

  * [[∞-Lie algebra]]

    * [[simplicial Lie algebra]]


  * [[∞-Lie algebroid]]

## Properties

### General

* [[PBW theorem]]

### Cohomology

See [[Lie algebra cohomology]].


### Lie theory

See

* [[Lie theory]]

  * [[Lie integration]]

  * [[Lie's three theorems]]



## Examples

* [[translation Lie algebra]], [[line Lie algebra]]

* [[derivation Lie algebra]]

* [[endomorphism Lie algebra]]

* [[general linear Lie algebra]]

* [[orthogonal Lie algebra]]

* [[special orthogonal Lie algebra]]

* [[special unitary Lie algebra]]

* [[Poincare Lie algebra]]

* [[super Poincare Lie algebra]]


## Related concepts

* **Lie algebra**

  * [[metric Lie algebra]]

  * [[universal enveloping algebra]], [[Cartan subalgebra]]

  * [[root (in representation theory)]], [[weight (in representation theory)]]

  * [[Lie algebra representation]]

  * [[Lie ideal]]
 
  * [[Chevalley basis]]

  * [[Kac-Moody algebra]]

  * [[complex Lie algebra]]

  * [[restricted Lie algebra]]

  * [[Lie group]]

  * [[Lie-Poisson structure]]

  * [[Lie algebra extension]]

    * [[semidirect product Lie algebra]]

  * [[Lie algebra contraction]]

* [[Leibniz algebra]]

* [[Lie 2-algebra]], [[Lie 2-group]]

* [[L-∞ algebra]], [[smooth ∞-group]]

* [[Lie algebroid]], [[Lie groupoid]]

* [[L-∞ algebroid]], [[smooth ∞-groupoid]]

* [[Lie coalgebra]]

[[!include infinitesimal and local - table]]

## References

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993

* [[Eckhard Meinrenken]], _Lie groups and Lie algebas_, Lecture notes 2010 ([pdf](http://www.math.toronto.edu/mein/teaching/lie.pdf))

Discussion with a view towards [[Chern-Weil theory]] is in 
chapter IV in vol III of 

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

Discussion in [[synthetic differential geometry]] is in 

*  {#Kock09} [[Anders Kock]], section 6 of _Synthetic Geometry of Manifolds_, 2009 ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))


[[!redirects Lie algebras]]

[[!redirects Lie bracket]]
[[!redirects Lie brackets]]