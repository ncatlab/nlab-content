
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $A$ a [[von Neumann algebra]] write $A'$ for its [[commutant]] in the ambient algebra $B(\mathcal{H})$ of [[bounded operator]]s.

+-- {: .num_defn}
###### Definition

A von Neumann algebra $A$ is called a **factor** if its [[center]] is trivial
$$
  Z(A) := A \cap A' = \mathbb{C}1
  \,.
$$

Equivalently: if $A$ and its [[commutant]] $A'$ generate the full algebra of [[bounded operators]] $B(\mathcal{H})$.

=--

## Properties

Every von Neumann algebra may be written as a [[direct integral]] over factors. ([von Neumann 49](#vNeumann49))


## Classification

Factors are classified in terms of the [[K-theory]] of their categories of finite [[W\*-modules]].
A [[W\*-module]] over a factor $A$ is _finite_ if it is not isomorphic to its proper submodule.

### Type I

Type I factors are characterized by the condition that the K-theory of finite modules
is isomorphic to $\mathbf{Z}$, the group of integers.
The only factors of this type are of the from $B(H)$, bounded operators on a Hilbert spacre~$H$.

### Type II

Type II factors are characterized by the condition that the K-theory of finite modules
is isomorphic to $\mathbf{R}$, the group of real numbers.

Type II factors are subdivided into two classes: type II$_1$ factors are characterized
by the condition that $A$ is a finite $A$-module,
whereas for a type II$_\infty$ factor $A$ is not a finite $A$-module. 

### Type III

Type III factors are characterized by the condition that the K-theory of finite modules
is trivial, i.e., only the zero module is finite.

Type III factors are further subdivided into three classes,
according to the structure of the center of their [[modular algebra]],
which is a commutative von Neumann algebra graded by purely imaginary numbers,
whose graded components are [[noncommutative L^p-spaces]].

By the [[von Neumann duality]] for commutative von Neumann algebras,
the spectrum of this center is a [[measurable space]] equipped with a σ-ideal
of negligible sets and the grading yields an action of $\mathbf{R}$, the group of real numbers.
This object is known as the [[noncommutative flow of weights]].

If the center is trivial (so the spectrum is a point), the factor has type III$_1$.
If the action of $\mathbf{R}$ is not periodic, then the factor has type III$_0$.
If the action is periodic with period $\lambda$, a positive real number,
then the factor has type III$_{\exp(-\lambda)}$.

## Related concepts

* [[C-star algebra]]

* [[uniformly hyperfinite algebra]]

## References

### General

The original sources are

* Murray, [[John von Neumann]], ...

* [[John von Neumann]], _On rings of operators, reduction theory_, Annals of Mathematics Second Series, Vol. 50, No. 2 (1949) ([jstor]( http://www.jstor.org/stable/1969463))
 {#vNeumann49}

* [[Alain Connes]], ...

Lecture notes include

* V.S. Sunder, _von Neumann algebras, $II_1$-factors, and their subfactors_ ([pdf](http://www.math.iitb.ac.in/seminar/archives/sunder_iitb3.pdf))

* Hideki Kosaki, _Type III factors and index theory_ (1993) ([pdf](http://pages.uoregon.edu/njp/lec-f.pdf))

### Subfactors

The mathematics of inclusions of _subfactors_ is giving deep structural insights. See also at _[[planar algebra]]_. 

* [[Vaughan Jones]], 

  _Index for subfactors_, Invent. Math. __72__, I (I983); 

  _A polynomial invariant for links via von Neumann algebras_, Bull. AMS __12__, 103 (1985); 

  _Hecke algebra representations of braid groups and link polynomials_, Ann. Math. __126__, 335 (1987)

* [[Vaughan Jones]], [[Scott Morrison]], [[Noah Snyder]], _The classification of subfactors of index at most 5_ ([arXiv:1304.6141](http://arxiv.org/abs/1304.6141))
* Vaughan F. R. Jones, David Penneys, _Infinite index subfactors and the GICAR categories_, [arxiv/1410.0856](http://arxiv.org/abs/1410.0856)

Symmetries of depth two inclusions of subfactors may be described via associative [[bialgebroid]]s,

* Lars Kadison, Kornél Szlachányi, _Bialgebroid actions on depth two extensions and duality_, Adv. Math. __179__:1 (2003) 75-121 <a href="https://doi.org/10.1016/S0001-8708(02)00028-2">doi</a>

### Relation to quantum field theory

* [[Jakob Yngvason]], _The role of type III factors in quantum field theory_ ([arXiv:math-ph/0411058](https://arxiv.org/abs/math-ph/0411058))


[[!redirects von Neumann algebra factors]]

[[!redirects von Neumann algebra subfactor]]
[[!redirects von Neumann algebra subfactors]]

[[!redirects subfactor]]
[[!redirects subfactors]]

