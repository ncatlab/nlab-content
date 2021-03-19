
#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A **hyperring** is like a [[ring]] not with an underlying [[abelian group]] but an underlying [[canonical hypergroup]]. 

It is a [[hypermonoid]] with additional ring-like [[stuff, structure, property|structure and properties]].

This means that in a hyperring $R$ addition is a multi-valued operation.

## Definition

A **hyperring** is a non-empty [[set]] $R$ equipped with a hyper-addition $+ : R\times R \to P^*(R)$ (where $P^*(R)$ is the set of non-empty subsets) and a multiplication $\cdot : R \times R \to R$ and with elements $0,1 \in R$ such that

1. $(R,+)$ is a [[canonical hypergroup]];

1. $(R,\cdot)$ is a [[monoid]] with identity element $1$;

1. $\forall r,s \in R : r(s+t) = r s + r t$ and $(s + t) r = s r + t r$;

1. $\forall r \in R : r \cdot 0 = 0 \cdot r = 0$;

1. $0 \neq 1$.

We can form many examples of hyperrings by quotienting a ring $R$ by a subgroup $G \subset R^{\times}$ of its multiplicative group. 

A **morphism of hyperrings** is a map $f : R_1 \to R_2$ such that

1. $\forall a,b \in R_1 : f(a + b) \subset f(a) + f(b)$;

1. $\forall a,b\in R_1 : f(a \cdot b) = f(a) \cdot f(b)$.

A **hyperfield** is a hyperring for which $(R - \{0\}, \cdot)$ is a [[group]].

## Examples

### Hyperfield extension of field with one element

The **hyperfield extension of the [[field with one element]]** is 

$$
  \mathbf{K} := (\{0,1\}, +, \cdot)
$$

with additive neutral element $0$ and the hyper-addition rule

$$
  1 + 1 = \{0,1\}
  \,.
$$

This is to be thought of as the hyperring of [[integer]]s modulo the relation "is 0 or not 0": think of $0 \in \mathbf{K}$ as being the integer 0 and of $1 \in \mathbf{K}$ as being _any_ non-zero integer, then the addition rule says that 0 plus any non-zero integer is non-zero, and that the sum of a non-zero integer with another non-zero integer is either zero or non-zero.

### The signature hyperfield $\mathbf{S}$

Let $\mathbf{S} = \{0,1,-1\}$ be the hyperfield with multiplication induced from $\mathbb{Z}$ and with addition given by 0 being the additive unit and the laws

* $1+1 = \{1\}$;

* $-1 + -1 = \{-1\}$

* $1 + -1 = \{-1, 0, 1\}$.

This we may think of as being the hyperring of [[integer]]s modulo the relation "is positive or negative or 0": think of $1$ as being any positive integer, $0$ as being the integer $0$ and $-1$ as being any negative integer. Then the hyper-addition law above encodes how the signature of integers behaves under addition.

**Proposition**

To each element, $\phi$, of $Hom(\mathbb{Z}[X], \mathbf{S})$ there corresponds an extended real number, $Re(\phi) \in [-\infty, \infty]$ given as a Dedekind cut. This is a surjective mapping. The inverse image of each real algebraic number contains three elements, while that of a nonalgebraic number is a singleton. For real algebraic $\alpha$, the three homomorphisms from $\mathbb{Z}[X]$ to $\mathbf{S}$ are

$$
P(T) \mapsto \underset{\epsilon \to 0+} {lim} sign P(\alpha + t \epsilon), t \in \{-1, 0, 1\}.
$$

## Related entries

* [[hypergroup]]

* [[canonical hypergroup]]

* [[hypermonoid]]

## Book

* B. Davvaz and V. Leoreanu-Fotea, Hyperring Theory and Applications, International Ackademic Press, USA, 2007.

## References

The notion of hyperring and hyperfield is due to Marc Krasner:

* M. Krasner, _Approximation des corps valu&#233;s complets de caract&#233;ristique $p\neq 0$ par ceux de caract&#233;ristique
0_ , pp.126-201 in _Colloque d' Alg&#233;bre Sup&#233;rieure (Bruxelles), 1956_ , Ceuterick Louvain 1957.

Another early reference is

* D. Stratigopoulos, _Hyperanneaux non commutatifs: Hyperanneaux, hypercorps, hypermodules, hyperespaces vectoriels et leurs propri&#233;t&#233;s &#233;l&#233;mentaires_ (French) C. R. Acad. Sci. Paris S&#233;r. A-B 269 (1969) A489&#8211;A492.

Modern applications in connection to the [[field with one element]] are discussed in 

* [[Alain Connes]], [[Caterina Consani]], _The hyperring of ad&#232;le classes_ ([arXiv:1001.4260](http://arxiv.org/abs/1001.4260))

* [[Alain Connes]], [[Caterina Consani]], _From monoids to hyperstructures: in search of an absolute arithmetic_ ([arXiv:1006.4810](http://arxiv.org/abs/1006.4810))

An overview is in

* Jaiung Jun, _Algebraic geometry over hyperrings_, [arXiv:1512.04837](http://arxiv.org/abs/1512.04837)

category: algebra

[[!redirects hyperring]]
[[!redirects hyperrings]]
[[!redirects hyper-ring]]
[[!redirects hyper-rings]]

[[!redirects hyperfield]]
[[!redirects hyperfields]]
[[!redirects hyper-field]]
[[!redirects hyper-fields]]
