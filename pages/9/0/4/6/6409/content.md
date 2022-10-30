## Idea

Wikipedia says very succinctly

> valuation is a function on a field that provides a measure of size or multiplicity of elements of the field. They generalize to commutative algebra the notion of size inherent in consideration of the degree of a pole or multiplicity of a zero in complex analysis, the degree of divisibility of a number by a prime number in number theory, and the geometrical concept of contact between two algebraic or analytic varieties in algebraic geometry.

## Definition

Given a totally ordered abelian group $G$ a $G$-valued __valuation__ $v$ on a (commutative) [[field]] $K$ is a (typically required to be surjective) function $v:K\to G\cup \infty$ such that $v(K^\times)\subset G$ and 

* $v$ defines the homomorphism of groups $v|_K : K^\times\to G$ where $K^\times$ is the multiplicative group of $K$

* $v(0) = \infty$

* $v(x+y) \geq min\{ v(x),v(y)\}$

with usual conventions for $\infty$. Field equipped with a valuation is a __valued field__. 

If the abelian group is the group of integers $\mathbf{Z}$ then we talk about [[discrete valuation]]s.

Sometimes one also discusses *exponential* (or *multiplicative*) *valuations* (also called valuation functions, and viewed as generalized absolute values) which look more like norms, and their equivalence classes, places. See [[discrete valuation]] and [[valuation ring]].

## Properties

In [[algebraic geometry]] there are very important theorems due Chevalley, [[valuative criterion of properness]] and [[valuative criterion of separatedness]].

## Literature 

* wikipedia [valuation (algebra)](http://en.wikipedia.org/wiki/Valuation_%28algebra%29)
* A. Fr&#246;hlich, J. W. S. Cassels (editors), _Algebraic number theory_, Acad. Press 1967, with many reprints; Fr&#246;hlich, Cassels, Birch, Atiyah, Wall, Gruenberg, Serre, Tate, Heilbronn, Rouqette, Kneser, Hasse, Swinerton-Dyer, Hoechsmann, systematic lecture notes from the instructional conference at Univ. of Sussex, Brighton, Sep. 1-17, 1965. (Especially chapters 1,2)
* Serge Lang, _Algebraic number theory_, GTM __110__, Springer 1970, 2000

[[!redirects valuations]]
[[!redirects valued field]]
[[!redirects valued fields]]