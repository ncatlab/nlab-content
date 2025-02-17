
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An **algebraic number** is a [[root]] of a non-zero [[polynomial]] with [[integer]] [[coefficients]] (or, equivalently, with [[rational number|rational]] coefficients). Equivalently, an element $\alpha$ of a [[field extension]] $K$ of the [[rational numbers]] $\mathbb{Q}$ is *algebraic* if the [[subfield]] $\mathbb{Q}(\alpha)$ is a finite degree [[field extension|extension]], i.e., is [[finite dimensional vector space|finite-dimensional]] as a [[rational vector space]]. 

Since the [[rational numbers]] are a [[subfield]] of the [[complex numbers]], and since the [[complex numbers]] are an [[algebraically closed field]], algebraic numbers are naturally regarded as a sub-field of [[complex numbers]]

$$
  \mathbb{Q} \hookrightarrow \mathbb{C}
  \,.
$$

$,$

<center>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Algebraicszoom.png/1200px-Algebraicszoom.png" width="490"/>
</center>

> **Visualisation of the (countable) field of algebraic numbers in the complex plane.** Colours indicate degree of the polynomial the number is a root of (red = linear, i.e. the rationals, green = quadratic, blue = cubic, yellow = quartic...). Points becomes smaller as the integer polynomial coefficients become larger. View shows integers 0,1 and 2 at bottom right, $+i$ near top. 

> due to Stephen J. Brooks [here](https://en.wikipedia.org/wiki/File:Algebraicszoom.png)

But the collection of all algebraic numbers forms itself already an [[algebraically closed field|algebraically closed]] [[field]], typically denoted $\overline{\mathbb{Q}}$, as this is the [[algebraic closure]] of the field $\mathbb{Q}$ of [[rational numbers]]. This also follows easily from the equivalent definition of algebraic numbers in terms of finite degree extensions. The [[absolute Galois group]] $Gal(\overline{\mathbb{Q}}, \mathbb{Q})$ is peculiar, see [there](absolute+Galois+group#OfTheRationalNumbers).

Given a [[field]] $k$, an algebraic __[[number field]]__ $K$ over $k$ is a finite-degree extension of $k$. By default, the term "algebraic number field" means an algebraic number field over the rational numbers. If $\alpha$ is an algebraic number over $\mathbb{Q}$ then $\mathbb{Q}[\alpha]$ is a number field, however the field of all algebraic numbers is *not* a number field.

An [[algebraic integer]] is a root of a [[monic polynomial]] with integer coefficients. Equivalently, an element $\alpha$ of a field extension $K$ of $\mathbb{Q}$ is an algebraic integer if the [[ring]] $\mathbb{Z}[\alpha]$ is of finite [[rank]] as a $\mathbb{Z}$-module. It follows easily from this characterization that the collection of all algebraic integers forms a commutative ring. 

## Related concepts

* [[algebraic number theory]]

  * [[algebraic integer]]
 
  * [[number field]]

* [[transcendental number]]

* [[algebraic extension]]

## References

See also

* Wikipedia, _[Algebraic numbers](https://en.wikipedia.org/wiki/Algebraic_number)_

[[!redirects algebraic number]]
[[!redirects algebraic numbers]]