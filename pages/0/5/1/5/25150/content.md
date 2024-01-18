
\tableofcontents

## Idea

The Archimedean property states that every positive element in a [[strictly weakly ordered]] [[cancellative monoid|cancellative]] [[commutative monoid]] is bounded above by a [[natural number]].

So an object satisfying the Archimedean property has no infinite elements. If the [[strict weak order]] is additionally a [[connected relation]] and thus a [[pseudo-order]], every [[infinitesimal]] element is equal to zero.

## Definition

### In general

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers.  

Let $(A,\lt, +, 0)$ be a [[strictly ordered]] [[cancellative monoid|cancellative]] [[commutative monoid]]. The positive integers are embedded into the [[function algebra|function monoid]] $A \to A$; there is an injection $inj:\mathbb{N}^+\to (A \to A)$ such that $inj(1) = id_A$ and $inj(s(n)) = inj(n) + id_A$ for all $n:\mathbb{N}^+$.

The __archimedean property__ states that for every $a,b:A$ such that $0 \lt a$ and $0 \lt b$, then there exist $n:\mathbb{N}^+$ such that $a \lt inj(n)(b)$. 

By [[uncurrying]] $inj$ one gets an [[action]] $act: (\mathbb{N}^+\times A) \to A$ such that $act(1,a) = a$ and $act(s(n),a) = act(n,a) + a$ for all $n:\mathbb{N}^+$ and $a:A$. The archimedean property then states that for all $a,b:A$ such that $0 \lt a$ and $0 \lt b$, there exist $n:\mathbb{N}^+$ such that $a \lt act(n,b)$.

### For ordered fields

For [[ordered fields]] $F$, since $\mathbb{Q}$ is the initial ordered field, there exists a unique ordered field homomorphism $i:\mathbb{Q} \to F$ for all ordered fields $F$. Then the **archimedean property** for $F$ states that the rational numbers are [[dense]] in $F$:

* for all $x \in F$ and $y \in F$ such that $x \lt y$, there exists a rational number $q:\mathbb{Q}$ such that $x \lt i(q) \lt y$. 

## Archimedean structure

In [[dependent type theory]], both definitions of the usual archimedean property above use the phrase "there exists...". This existence in the definitions is mere existence; i.e. using the [[existential quantifier]] rather than the [[dependent sum type]]. The untruncated version of the archimedean property using dependent sum types can be called **archimedean structure**. 

### In general

Archimedean structure for [[strictly ordered]] [[cancellative monoid|cancellative]] [[commutative monoids]] $(A,\lt, +, 0)$ using the positive natural numbers says that 

* for every $x:A$, $y:A$ such that $0 \lt x$ and $0 \lt y$, then there exist as structure a positive natural number $n:\mathbb{N}^+$ such that $x \lt \mathrm{inj}(n)(y)$. 

$$\prod_{x:A} \prod_{y:A} (0 \lt x) \times (0 \lt y) \to \sum_{n:\mathbb{N}^+} x \lt \mathrm{inj}(n)(y)$$

Defining the type of positive elements in $A$ as $A^+ \coloneqq \sum_{x:A} 0 \lt x$, by [[uncurrying]] and using the [[type theoretic axiom of choice]], one gets the equivalent statement 

$$\prod_{x:A^+} \prod_{y:A^+} \sum_{n:\mathbb{N}^+} x \lt \mathrm{inj}(n)(y)$$

which by the type theoretic axiom of choice is the same as saying that 

* there exists as structure a function $M:(A^+ \times A^+) \to \mathbb{N}^+$ such that for every $x:A^+$ and $y:A^+$,  $x \lt \mathrm{inj}(M(x, y))(y)$

$$\sum_{M:(A^+ \times A^+) \to \mathbb{N}^+} \prod_{x:A^+} \prod_{y:A^+} x \lt \mathrm{inj}(M(x, y))(y)$$

These functions can be called the **archimedean modulus** in parallel to the [[modulus of convergence]] and [[modulus of continuity]] which are defined for the untruncated versions of the definitions of [[Cauchy sequence]] and [[continuous function]]. 

### For ordered fields

Similarly, archimedean structure for ordered fields states that 

* for all $x:F$ and $y:F$ such that $x \lt y$, there exists as structure a rational number $q:\mathbb{Q}$ such that $x \lt i(q) \lt y$. 

$$\prod_{x:F} \prod_{y:F} x \lt y \to \sum_{q:\mathbb{Q}} (x \lt i(q)) \times (i(q) \lt y)$$

One could construct archimedean structure for any Archimedean ordered field satisfying [[trichotomy]], that for all $x:F$ and $y:F$, exactly one of $x \gt y$, $x \lt y$, $x = y$ is true. 

Suppose the Archimedean ordered field $F$ has [[decidable equality]]. Then, the [[ceiling]] $x \mapsto \lceil x \rceil$ and [[floor]] $x \mapsto \lfloor x \rfloor$ are well defined functions over the entire domain of $F$. By definition of the ceiling and the fact that $x \lt y$, we have that 

$$\left\lceil\frac{2}{y - x}\right\rceil \geq \frac{2}{y - x}$$
and thus
$$\left\lceil\frac{2}{y - x}\right\rceil (y - x) = \left\lceil\frac{2}{y - x}\right\rceil y - \left\lceil\frac{2}{y - x}\right\rceil x \geq 2$$
so we have 
$$\left\lceil\frac{2}{y - x}\right\rceil x \lt \frac{\left\lceil \left\lceil\frac{2}{y - x}\right\rceil x \right\rceil + \left\lfloor \left\lceil\frac{2}{y - x}\right\rceil y \right\rfloor}{2} \lt \left\lceil\frac{2}{y - x}\right\rceil y$$
Since $x \lt y$, $0 \lt \left\lceil\frac{2}{y - x}\right\rceil$, and so it is possible to divide all sides by $\left\lceil\frac{2}{y - x}\right\rceil$ and keep the elements in the inequality in order. 

$$x \lt \frac{\left\lceil \left\lceil\frac{2}{y - x}\right\rceil x \right\rceil + \left\lfloor \left\lceil\frac{2}{y - x}\right\rceil y \right\rfloor}{2 \left\lceil\frac{2}{y - x}\right\rceil} \lt y$$

Thus, if the Archimedean ordered field has [[decidable equality]], then the Archimedean ordered field has Archimedean structure. In [[classical mathematics]], as well as in [[constructive mathematics]] in which the [[analytic LPO]] for the [[terminal object|terminal]] Archimedean ordered field is true, every Archimedean ordered field has Archimedean structure. 

## Examples

* [[Archimedean group]] 
* [[Archimedean ordered field]]
* [[Archimedean ordered integral domain]]
* [[Archimedean ordered local ring]]

## References

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Archimedean_property">Archimedean property</a>_

The alternative definition of the Archimedean property for ordered fields using the rational numbers is defined in section 11.2.1 of 

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

and in section 4.3 of

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects archimedean property]]
[[!redirects Archimedean property]]

[[!redirects archimedean structure]]
[[!redirects Archimedean structure]]