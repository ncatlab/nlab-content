
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
 

A **morphism of hyperrings** is a map $f : R_1 \to R_2$ such that

1. $\forall a,b \in R_1 : f(a + b) \subset f(a) + f(b)$;

1. $\forall a,b\in R_1 : f(a \cdot b) = f(a) \cdot f(b)$.

A **hyperfield** is a hyperring for which $(R - \{0\}, \cdot)$ is a [[group]].

## Examples

### Equivalence classes in a ring

We can form many examples of hyperrings by quotienting a ring $R$ by some subgroup $G \subset R^{\times}$ of its multiplicative group.   More precisely, an element of the hyperring $R/G$ is given by an equivalence class of elements of $R$, where $x \sim y$ if and only if $x = yg$ for some $g \in G$.   Multiplication descends straightforwardly from $R$ to $R/G$, while addition become multivalued: the sum of equivalence classes $[x]$ and $[y]$ is the set of all equivalence classes $[x + y]$.

In particular, if $R$ is a hyperfield so is $R/G$.

### The Krasner hyperfield $\mathbb{K}$

The *Krasner hyperfield* is the set $\mathbb{K} = \{0,1\}$ with multiplication given by 

* $0 \cdot x = 0$

* $1 \cdot x = x$

and with addition given by 

* $0 + x = x$

* $1+1 = \{0,1\}$

$\mathbb{K}$ is the quotient of the field of [[rational numbers]] or [[real numbers]] by its multiplicative subgroup consisting of all nonzero numbers: $0$ is the equivalence class containing $0$, while $1$ is the equivalence class containing all nonzero numbers.  The hyper-addition law above encodes how such equivalence classes behave under addition: for example, the sum of two nonzero numbers can be zero or nonzero.

### The sign hyperfield $\mathbb{S}$

The *sign hyperfield* is the set $\mathbb{S} = \{0,1,-1\}$ with multiplication given by 

* $0 \cdot x = 0$

* $1 \cdot x = 1$

* $-1 \cdot -1 = 1$

and with addition given by 

* $0 + x = x$

* $1+1 = \{1\}$

* $-1 + -1 = \{-1\}$

* $1 + -1 = \{-1, 0, 1\}$.

$\mathbb{S}$ is the quotient of the field of [[rational numbers]] or [[real numbers]] by its multiplicative subgroup of positive numbers: $1$ is the equivalence class containing the positive numbers, $0$ is the equivalence class containing $0$, and $-1$ as the equivalence class of the negative numbers.   Again, the hyper-addition law encodes how such equivalence classes behave under addition: most notably, the sum of a positive and a negative number can be positive, zero, or negative.

**Proposition**

To each element, $\phi$, of $Hom(\mathbb{Z}[X], \mathbb{S})$ there corresponds an extended real number, $Re(\phi) \in [-\infty, \infty]$ given as a Dedekind cut. This is a surjective mapping. The inverse image of each real algebraic number contains three elements, while that of a nonalgebraic number is a singleton. For real algebraic $\alpha$, the three homomorphisms from $\mathbb{Z}[X]$ to $\mathbb{S}$ are

$$
P(T) \mapsto \underset{\epsilon \to 0+} {lim} sign P(\alpha + t \epsilon), t \in \{-1, 0, 1\}.
$$

### The tropical hyperfield $\mathbb{T}$

The tropical hyperfield has as its underlying set $\mathbb{T} = [0,\infty]$.  The product of $a, b \in \mathbb{T}$ is defined to be the usual *sum* of nonnegative numbers for $a, b\in [0,\infty)$, and we define $a \cdot \infty = \infty$.   The sum of $a,b \in \mathbb{T}$ is defined to be $a \max b$ when $a \ne b$, but when $a = b$ it is defined to be the set $[0,a]$.

**Proposition.**  For any commutative ring $R$,  hyperring homomorphisms $\phi \colon R \to \mathbb{T}$ are the same as nonarchimedean valuations $\phi \colon R \to [0,\infty]$.

This was observed first by Viro, but a proof can be found in Lorscheid's _Tropical geometry over the tropical hyperfield_, Theorem 2.2.

## Related entries

* [[ring]]

* [[hypermagma]]

* [[hypermonoid]]

* [[hypergroup]]

* [[hypergraph]]

* [[canonical hypergroup]]

## Book

*  Bijan Davvaz and Violeta Leoreanu-Fotea, Hyperring Theory and Applications, International Academic Press, 2007.

*  Bijan Davvaz and Violeta Leoreanu-Fotea, Krasner Hyperring Theory, World Scientific, 2024.

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

For more on the tropical hyperfield see:

* Oliver Lorscheid, _Tropical geometry over the tropical hyperfield_ ([arXiv:1907.01037](https://arxiv.org/abs/1907.01037))


category: algebra

[[!redirects hyperring]]
[[!redirects hyperrings]]
[[!redirects hyper-ring]]
[[!redirects hyper-rings]]

[[!redirects hyperfield]]
[[!redirects hyperfields]]
[[!redirects hyper-field]]
[[!redirects hyper-fields]]
