
> This page is about Boolean semirings as defined by Ivan Chajda and Miroslav Kotrle. For other notions of "Boolean semirings", see [[Boolean semiring]]. 

> This page is about the notion of _skeleton_ of a [[semiring]] as defined by Ivan Chajda and Miroslav Kotrle. For other notions of *skeleton* in [[mathematics]], see at [[skeleton]]. 


\tableofcontents

## Definition

The authors [Chadja & Kotrle 1994](#CK94) assume that [[semirings]] are non-unital in that they do not have either the [[absorbing element|multiplicatively absorptive]] [[neutral element|additive unit]] $0$ or the multiplicative unit $1$ that define [[rigs]]. Instead, their semirings only have an element $0$ such that $0 \cdot a = 0$. 

[Chadja & Kotrle 1994](#CK94) defined the **skeleton** $S(A)$ of a [[semiring]] $A$ to be the [[subset]] of all elements $c \in A$ such that $c$ is the sum of two elements $a \in A$ and $b \in A$. 

A [[semiring]] $A$ is a **Boolean semiring** if:

* the semiring $A$ is **skeletal**: the skeleton $S(A)$ of the semiring is a [[subobject|sub]][[rng]] of $A$. 

* for all $a$ and $b$, $a \cdot a = a + 0$ and $a \cdot b + 0 = a \cdot b$. By definition, $0 = 0 \cdot (a + a) = 0 \cdot a + 0 \cdot a = 0 + 0$ is an element of $S(A)$. 

* there exists an element $1$ such that for all $a$ and $b$, $(a \cdot b) \cdot 1 = a \cdot b$ and $1 \cdot (a \cdot b) = a \cdot b$

## Properties

Every boolean semiring is [[commutative]]. 

## Related concepts

* [[semiring]]

## References

* {#CK94} [[Ivan Chajda]], [[Miroslav Kotrle]], *Boolean semirings*, Czechoslovak Mathematical Journal, Volume 44, Issue 4, pp. 763-767, 1994. &lbrack;[doi:10.21136/CMJ.1994.128495](http://dx.doi.org/10.21136/CMJ.1994.128495), [pdf](https://dml.cz/bitstream/handle/10338.dmlcz/128495/CzechMathJ_44-1994-4_15.pdf)&rbrack;

[[!redirects skeletal semiring]]
[[!redirects skeletal semirings]]

[[!redirects Boolean semiring (Chajda & Kotrle)]]
[[!redirects Boolean semirings (Chajda & Kotrle)]]
[[!redirects boolean semiring (Chajda & Kotrle)]]
[[!redirects boolean semirings (Chajda & Kotrle)]]