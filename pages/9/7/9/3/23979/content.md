+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

A **Bézout ring** is a [[commutative ring]] $R$ where every finitely generated ideal is a [[principal ideal]], or where every ideal with 2 generators is a [[principal ideal]]: for every element $a \in R$ and $b \in R$, there exists elements $x \in R$, $y \in R$ called **Bézout coefficients** and $g \in R$ called a **common divisor**, such that $a \cdot x + b \cdot y = g$ and there exist $a^{'} \in R$ and $b^{'} \in R$ such that $a = g \cdot a^{'}$ and $b = g \cdot b^{'}$.

One could posit, instead of the property that for every element $a \in R$ and $b \in R$, there exists elements $x \in R$, $y \in R$ and $g \in R$, such that $a \cdot x + b \cdot y = g$ and there exist $a^{'} \in R$ and $b^{'} \in R$ such that $a = g \cdot a^{'}$ and $b = g \cdot b^{'}$; that the integral domain has the [[structure]] of Bézout coefficient functions $\beta_0:R \times R \to R$ and $\beta_1:R \times R \to R$ and common divisor function $\gamma:R \times R \to R$ such that for every element $a \in R$ and $b \in R$, 
$$a \cdot \beta_0(a, b) + b \cdot \beta_1(a, b) = \gamma(a, b)$$ 
and there exist $a^{'} \in R$ and $b^{'} \in R$ such that $a = \gamma(a, b) \cdot a^{'}$ and $b = \gamma(a, b) \cdot b^{'}$ There might be multiple such triples of Bézout coefficient functions and common divisor function. 

If the commutative ring is a [[GCD ring]] and the common divisor is the [[greatest common divisor]], then the Bézout ring condition is called the **Bézout identity**. 

## See also ##

* [[commutative ring]]

* [[Euclidean ring]]

* [[prefield]]

* [[Bézout domain]]

## References

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* Wikipedia, _[Bézout's identity](http://en.wikipedia.org/wiki/Bézout's_identity)

[[!redirects Bézout rings]]

[[!redirects Bezout ring]]
[[!redirects Bezout rings]]

[[!redirects Bézout's identity]]
[[!redirects Bezout's identity]]

[[!redirects Bézout coefficient]]
[[!redirects Bézout coefficients]]
[[!redirects Bezout coefficient]]
[[!redirects Bezout coefficients]]