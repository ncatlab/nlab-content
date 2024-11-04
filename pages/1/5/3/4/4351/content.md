
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


\tableofcontents


## Idea 

A **hyperring** is like a [[ring]] but not with an [[underlying]] [[abelian group]] but with an underlying [[canonical hypergroup]], hence it is a *[[hypermonoid]]* with additional ring-like [[structure]].

This means that [[addition]] in a hyperring $R$  is a [[multi-valued function]].

## Definition

A **hyperring** is a [[inhabited set|non-empty]] [[set]] $R$ equipped with 

1. a *hyper-addition* $+ \,\colon\, R\times R \longrightarrow P^*(R)$ (where $P^*(R)$ is the set of non-empty subsets) 

1. a *multiplication $\cdot \,\colon\, R \times R \longrightarrow R$ 

1. chosen [[elements]] $0,1 \,\in\, R$ 

such that

1. $(R,+)$ is a [[canonical hypergroup]];

1. $(R,\cdot)$ is a [[monoid]] with [[identity element]] $1$;

1. $\forall r,s \in R \,\colon\, r(s+t) = r s + r t$ and $(s + t) r = s r + t r$;

1. $\forall r \in R \,\colon\, r \cdot 0 = 0 \cdot r = 0$;
 
{#ReferencesForTheDefinition} (e.g. [Nakassis 1987 Def. 4](Nakassis87), [Davvaz & Leoreanu-Fotea 2007 Def. 3.1.1](#DavvazLeoreanu-Fotea07); other authors require moreover that $0 \neq 1$, e.g. [Connes & Consani 2011 Def. 2.1](#ConnesConsani11), [Jun 2015 Def. 2.2](#Jun15))


A *[[homomorphism]] of hyperrings* is a [[map]] $f \,\colon\, R_1 \to R_2$ such that

1. $\forall a,b \in R_1 \,\colon\, f(a + b) \subset f(a) + f(b)$;

1. $\forall a,b\in R_1 \,\colon\, f(a \cdot b) = f(a) \cdot f(b)$.

A **hyperfield** is a hyperring for which $(R \setminus \{0\}, \cdot)$ is a [[group]] and $0 \ne 1$.


## Examples

### Equivalence classes in a ring

We can form many examples of hyperrings by [[quotient ring|quotienting]] a ring $R$ by some [[subgroup]] $G \subset R^{\times}$ of its [[group of units]].  More in detail, an element of the hyperring $R/G$ is given by an [[equivalence class]] of elements of $R$, where $x \sim y$ if and only if $x = y g$ for some $g \in G$.   Multiplication descends straightforwardly from $R$ to $R/G$, while addition become multivalued: the sum of equivalence classes $[x]$ and $[y]$ is the set of all equivalence classes $[x + y]$.

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


## References

The notion of hyperring and hyperfield is due to:

* [[Marc Krasner]]: *Approximation des corps valués complets de caractéristique $p \neq 0$ par ceux de caractéristique 0*,  in: *Colloque d’ Algébre Supérieure (Bruxelles 1956)*, Ceuterick Louvain (1957) 126-201

Another early reference is

* D. Stratigopoulos, *Hyperanneaux non commutatifs: Hyperanneaux, hypercorps, hypermodules, hyperespaces vectoriels  et leurs propriétés élémentaires*, C. R. Acad. Sci. Paris Sér. A-B **269** (1969) A489-A492

See also:

* {#Krasner83} [[Marc Krasner]]: *A class of hyperrings and hyperfields*, International Journal of Mathematics and Mathematical Sciences (1983) &lbrack;[doi:10.1155/S0161171283000265](https://doi.org/10.1155/S0161171283000265)&rbrack;


Review:

* {#Nakassis87} Anastase Nakassis: *Recent results in hyperring and hyperfield theory*, International Journal of Mathematics and Mathematical Sciences (1987) &lbrack;[doi:10.1155/S0161171288000250](https://doi.org/10.1155/S0161171288000250)&rbrack;

Monographs:

* {#DavvazLeoreanu-Fotea07} Bijan Davvaz, Violeta Leoreanu-Fotea, *Hyperring Theory and Applications*, International Academic Press (2007) &lbrack;[pdf](https://www.santilli-foundation.org/docs/Davvaz.pdf)&rbrack;

*  Bijan Davvaz, Violeta Leoreanu-Fotea, *Krasner Hyperring Theory*, World Scientific (2024) &lbrack;[doi:10.1142/13652](https://doi.org/10.1142/13652)&rbrack;


Applications to the geometry over the "[[field with one element]]":

* {#ConnesConsani11} [[Alain Connes]], [[Caterina Consani]], *The hyperring of adèle classes*, Journal of Number Theory **131** 2 (2011) 159-194 &lbrack;[arXiv:1001.4260](http://arxiv.org/abs/1001.4260), [doi:10.1016/j.jnt.2010.09.001](https://doi.org/10.1016/j.jnt.2010.09.001)&rbrack;

* [[Alain Connes]], [[Caterina Consani]]: *From monoids to hyperstructures: in search of an absolute arithmetic* &lbrack;[arXiv:1006.4810](http://arxiv.org/abs/1006.4810)&rbrack;

On [[algebraic geometry]] over hyperrings:

* {#Jun15} Jaiung Jun, *Algebraic geometry over hyperrings*, Advances in Mathematics **323** (2018) 142-192 &lbrack;[arXiv:1512.04837](http://arxiv.org/abs/1512.04837), [doi:10.1016/j.aim.2017.10.043](https://doi.org/10.1016/j.aim.2017.10.043)&rbrack;


On the tropical hyperfield:

* [[Oliver Lorscheid]], _Tropical geometry over the tropical hyperfield_ &lbrack;[arXiv:1907.01037](https://arxiv.org/abs/1907.01037)&rbrack;


category: algebra

[[!redirects hyperring]]
[[!redirects hyperrings]]
[[!redirects hyper-ring]]
[[!redirects hyper-rings]]

[[!redirects hyperfield]]
[[!redirects hyperfields]]
[[!redirects hyper-field]]
[[!redirects hyper-fields]]
