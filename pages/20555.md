# Novikov fields

* table of contents
{: toc}

## Idea

A *Novikov field* (or Novikov ring) is a field of generalized [[formal power series]] that allows non-integer exponents.  In contrast to a [[Hahn series]] field, in a Novikov field the series are only $\omega$-long rather than transfinitely long.  This requires a "left-finiteness" condition on the exponents to ensure closure under multiplication.

## Definition

There are many variant definitions of Novikov fields in the literature, see e.g. [this question](https://mathoverflow.net/q/13203).  Here we give a reasonable-seeming general and abstract definition.

Let $k$ be a [[commutative ring]] and $G$ a [[linear order|linearly]] [[ordered abelian group]].

+--{: .un_defn}
###### Definition
The **Novikov ring** of $k$ with value group $G$ is the ring of functions $f:G\to k$ such that for any $y\in G$ the set $\{ x\in G \mid x \lt y \wedge f(x)\neq 0\}$ is finite.  Such functions are added pointwise, and multiplied by the formula
$$ (f\cdot g)(z) = \sum_{x+y=z} f(x) \cdot g(y). $$
=--

Left-finiteness of the support of $f$ and $g$ implies that the above sum is finite.  Specifically, if $g\neq 0$ then since $G$ is totally ordered, there is a least $y_0$ such that $g(y_0)\neq 0$.  Then the set $\{ x\mid x \le z-y_0 \wedge f(x)\neq 0\}$ is finite, and hence so is its subset $\{ x \mid \exists y. x+y = z \wedge f(x)\neq 0 \wedge g(y)\neq 0 \}$.  Note that this depends on the fact that $G$ is totally ordered and a group; a partially ordered monoid would not suffice.

Notationally, we write such a function as $\sum_{x\in G} f(x)\, t^x$ for $t$ a formal variable.  If $k$ is a [[field]], then so is the Novikov ring.


## Examples

* When $G=\mathbb{R}$, the Novikov field is sometimes called the "universal Novikov field".

* When $G=\mathbb{Q}$ and $k =\mathbb{R}$, the Novikov field is known as the **Levi-Civita field**.


## Characterizations

The Novikov field embeds into the [[Hahn series]] field $k[[t^G]]$.  It can (probably) be characterized therein as

* The set of Hahn series with order type $\omega$ that converge to themselves in the valuation topology.

* The closure of the field $k(t^G)$ of [[generalized rational functions]] inside the Hahn series field.

It can also (probably) be characterized abstractly as

* The Cauchy completion of $k(t^G)$ in its valuation [[uniform space|uniformity]].

* The completion of $k(t^G)$ as a valued field, i.e. the unique (up to isomorphism) dense valued field extension without proper dense valued field extension.


## Applications

* The universal Novikov field of $\mathbb{R}$ is a natural context in which to relate [[magnitude homology]] of finite [[metric spaces]] to their [[magnitude]].  (Hahn series also suffice, but all the action actually takes place in the Novikov field.)

* In the [[Fukaya category]], the chain complexes defining Hom's between objects are defined over a Novikov ring.

## Related pages

Other rings of generalized power series include:

* [[Puiseux series]]
* [[Hahn series]]
* [[Ribenboim power series]]

Hahn series are a special kind of Ribenboim power series, but Puiseux and Novikov series are not.  However, they are all instances of the linearization of a [[finiteness space]].


## References

* [Wikipedia: Novikov ring](https://en.wikipedia.org/wiki/Novikov_ring)
* [Wikipedia: quantum cohomology](https://en.wikipedia.org/wiki/Quantum_cohomology)
* [MathOverflow: definitions of Novikov field](https://mathoverflow.net/q/13203)


[[!redirects Novikov field]]
[[!redirects Novikov fields]]
[[!redirects Novikov ring]]
[[!redirects Novikov rings]]
[[!redirects Novikov series]]
[[!redirects universal Novikov field]]
[[!redirects universal Novikov fields]]
[[!redirects universal Novikov ring]]
[[!redirects universal Novikov rings]]
[[!redirects Levi-Civita field]]
