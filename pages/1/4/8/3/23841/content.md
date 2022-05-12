
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

Arithmetic for [[closed interval]]s of an [[ordered field]]. 

## Definition

Let $F$ be an [[ordered field]]. The closed intervals of $F$ can be represented by a [[subset]] of the [[Cartesian product]] set $F \times F$:

$$\mathcal{I}(F) \coloneqq \{(a, b) \in F \times F \vert (a \leq b)\}$$

The elements $[a, b] \in \mathcal{I}(F)$ of the [[set]] are the endpoints of the closed intervals, which we shall call **intervals** for short. 

There is an [[embedding]] $i:F \to \mathcal{I}(F)$ defined by 

$$i(a) \coloneqq [a, a]$$

Equality of intervals is defined as

$$([a, b] = [c, d]) \coloneqq (a = c) \times (b = d)$$

If $R$ has [[decidable equality]], then $\mathcal{I}(R)$ has decidable equality as well. 

### Relation to the zero interval ###

A positive interval is defined by 

$$([0, 0] \lt [a, b]) \coloneqq (0 \lt a)$$

A negative interval is defined by 

$$([0, 0] \gt [a, b]) \coloneqq (0 \gt b)$$

A indefinite interval is defined by 

$$([0, 0] \sim [a, b]) \coloneqq \neg(0 \lt a) \wedge \neg(0 \gt b)$$

### Arithmetic of intervals ###

Zero is defined by 

$$0 \coloneqq [0, 0]$$

Addition is defined by 

$$[a, b] + [c, d] \coloneqq [a + c, b + d]$$

Negation is defined by 

$$-[a, b] \coloneqq [-b, -a]$$

Subtraction is defined by 

$$[a, b] - [c, d] \coloneqq [a, b] + (-[c, d]) = [a - d, b - c]$$

Intervals do not form an [[abelian group]] because $[a, b] - [a, b] = [a - b, b - a]$, and $[a - b, b - a] = 0$ if and only if $a = b$. However, they do form a [[commutative monoid]] under zero and addition. 

One is defined by 

$$1 \coloneqq [1, 1]$$

Multiplication is defined by 

$$[a, b] \cdot [c, d] \coloneqq [\min(ac, ad, bc, bd), \max(ac, ad, bc, bd)]$$

Intervals form a [[commutative monoid]] under one and multiplication. Zero and multiplication also form an [[absorption monoid]]. Multiplication does not distribute over addition: 

$$[1, 2] \cdot ([1, 3] + [-1, 3]) = [1, 2] \cdot [0, 6] = [\min(0, 6, 0, 12), \max(0, 6, 0, 12)] = [0, 12]$$

$$[1, 2] \cdot [1, 3] + [1, 2] \cdot [-1, 3] = [\min(1, 2, 3, 6), \max(1, 2, 3, 6)] + [\min(-1, -2, 3, 6), \max(-1, -2, 3, 6)] = [1, 6] + [-2, 6] = [-1, 12]$$

$$[0, 12] \neq [-1, 12]$$

The reciprocal is only defined for intervals that are positive or negative: $0 \lt [a, b]$ or $0 \gt [a, b]$, and is defined by 

$$1/[a, b] \coloneqq [1/b, 1/a]$$

Division is only defined for intervals in the denominator that are positive or negative: $0 \lt [c, d]$ or $0 \gt [c, d]$, and is defined by 

$$[a, b]/[c, d] \coloneqq [a, b] \cdot [1/d, 1/c] = [\min(a/c, a/d, b/c, b/d), \max(a/c, a/d, b/c, b/d)]$$

However, division of an interval by itself does not return the constant one: if $0 \lt [a, b]$ or $0 \gt [a, b]$, then 

$$[a, b]/[a, b] = [\min(a/a, a/b, b/a, b/b), \max(a/a, a/b, b/a, b/b)] = [a/b, b/a]$$

and $[a/b, b/a] = 1$ if and only if $a = b$. 

### Ordering of the intervals ###

The [[linear order]] of the rational intervals is defined as 

$$([a, b] \lt [c, d]) \coloneqq (b \lt c)$$

The [[opposite]] linear order of the rational intervals is defined as 

$$([a, b] \gt [c, d]) \coloneqq (a \gt d)$$

The [[subset|containment]] [[relation]] of the rational intervals is defined as 

$$([a, b] \subseteq [c, d]) \coloneqq (a \geq c) \wedge (b \leq d)$$

The opposite containment relation of the rational intervals is defined as 

$$([a, b] \supseteq [c, d]) \coloneqq (a \leq c) \wedge (b \geq d)$$

## See also ##

* [[arithmetic]]

* [[interval]]

* [[ordered field]]

* [[interval cut]]

* [[Dedekind cut]]