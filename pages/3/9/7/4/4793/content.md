
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A _quaternion_ or _Hamilton number_ is a kind of [[number]] similar to the [[complex numbers]] but with three instead of one [[square root]] of $(-1)$ adjoined, satisfying certain relations.

The __quaternions__ form the largest [[associative algebra|associative]] [[normed division algebra]], usually denoted  $\mathbb{H}$ after [[William Rowan Hamilton]] (since $\mathbb{Q}$ is taken for the [[rational numbers]]). 

## Properties

### Normed division algebra structure

The structure of $\mathbb{H}$ as an $\mathbb{R}$-[[associative unital algebra|algebra]] is given by a basis $\{1, i, j, k\}$ of the underlying [[vector space]] of $\mathbb{H}$, equipped with a multiplication table where $1$ is the [[identity element]] and otherwise uniquely specified by the equations 

$$i^2 = j^2 = k^2 = i j k = -1,$$ 

and extended by $\mathbb{R}$-linearity to all of $\mathbb{H}$. The norm on $\mathbb{H}$ is given by 

$${\|\alpha\|}^2 = \alpha \widebar{\alpha}$$ 

where given an $\mathbb{R}$-[[linear combination]] $\alpha = a 1 + b i + c j + d k$, we define the _conjugate_ $\widebar{\alpha} \coloneqq a 1 - b i - c j - d k$. A simple calculation yields 

$${\|\alpha\|}^2 = a^2 + b^2 + c^2 + d^2$$ 

whence for $\alpha \neq 0$, the multiplicative [[inverse]] is 

$$\alpha^{-1} = \frac1{{\|\alpha\|}^2} \widebar{\alpha}.$$ 

In this way $\mathbb{H}$ is a normed division algebra. 

### Modules and bimodules

We have canonical left and right [[module]] structures on $\mathbb{H}^n$, but as $\mathbb{H}$ is not commutative, if we want to talk about tensor products of modules, we need to consider [[bimodules]]. This also means that ordinary [[linear algebra]] as is used over a field is not quite the same when dealing with quaternions. For instance, one needs to distinguish between _left_ and _right_ [[eigenvalues]] of [[matrices]] in $M_n(\mathbb{H})$ (using the left and right module structures on $\mathbb{H}^n$ respectively), and only left eigenvalues relate to the [[spectrum]] of the associated linear operator.

Using the conjugation operation one can define an inner product $\langle q,p\rangle := \overline{q} p$ on $\mathbb{H}^n$ so that the corresponding [[orthogonal group of an inner product space|orthogonal group]] is the [[compact symplectic group]].

### Automorphisms

+-- {: .num_prop #AutomorphismsOfQUatrnionsAlgebraIsSO3}
###### Proposition

The [[automorphism group]] of the quaternions, as a real algebra, is [[special orthogonal group|SO(3)]], [[action|acting]] canonically  on their imaginary part (in generalization of how the product of [[complex numbers]] respects the [[complex conjugation]] action)

=--

See also at _[normed division algebra -- automorphism](normed+division+algebra#Automorphisms)_

(e.g. [Klimov-Zhuravlev, p. 85](#KlimovZhuravlev))



## Related concepts

* [[quaternionic vector space]]

* [[quaternionic vector bundle]]

* [[Dieudonné determinant]]

* [[SL(2,H)]]

[[!include exceptional spinors and division algebras -- table]]

* [[supersymmetry and division algebra]]

* [[quaternionic quantum mechanics]]

* [[quaternion group]], [[quaternionic unitary group]]

* [[tessarines]]

## References

Monographs:

* {#KlimovZhuravlev} D. M. Klimov, V. Ph. Zhuravlev, *Group-Theoretic Methods in Mechanics and Applied Mathematics*, Routledge (2004, 2020) &lbrack;[ISBN:9780367446987](https://www.routledge.com/Group-Theoretic-Methods-in-Mechanics-and-Applied-Mathematics/Klimov-Zhuravlev/p/book/9780367446987)&rbrack;


* [[Ernst Binz]], Sonja Pods, Ch 1 in: *The geometry of Heisenberg groups --- With Applications in Signal Theory, Optics, Quantization, and Field Quantization*, Mathematical Surveys and Monographs **151**, American Mathematical Society (2008) &lbrack;[ams:surv-151](https://bookstore.ams.org/surv-151)&rbrack; 

* [[Tevian Dray]], [[Corinne Manogue]], Section 3.1 of: _The Geometry of Octonions_, World Scientific (2015) &lbrack;[doi:10.1142/8456](https://doi.org/10.1142/8456)&rbrack;


See also:

* T. Y. Lam, _Hamilton's Quaternions_ ([ps](http://math.berkeley.edu/~lam/quat.ps))



[[!redirects quaternion]]
[[!redirects quaternions]]
[[!redirects quaternionic]]

[[!redirects quaternion number]]
[[!redirects quaternion numbers]]

[[!redirects Hamilton number]]
[[!redirects Hamilton numbers]]
