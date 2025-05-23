
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* the following line creates the automatic table of contents
{: toc}

## Idea

Similarly to the presentation of [[groups]] by [[generators and relations]], a
category may be presented by a set of generating arrows subject to
certain relations.


## Definition

Let $G$ be a [[quiver|directed graph]], and let $R$ be a function that assigns to each pair $a,b$ of objects of the [[free category]] $F(G)$ a [[binary
relation]] $R_{a,b}$ on the [[hom-set]] $F(G)(a,b)$.  The
**category with generators $G$ and relations $R$** is the [[quotient category]] (as defined in [Mac Lane](#MacLane) or [Mitchell](#Mitchel), for example -- this is _not_ the nLab definition since it violates the [[principle of equivalence]]) $F(G)/R$. For a category $C$, an [[isomorphism of categories|isomorphism]] $C\to F(G)/R$ is called a **presentation** of $C$.


## Properties

Writing $can\colon F(G)\to F(G)/R$ for the canonical functor, it follows
from the universal property of the quotient category that for any
functor $S\colon F(G)\to D$ that respects the relation $R$ ($f
R_{a,b}g$ implies $S(f)=S(g)$), there exists a unique functor $S'\colon
F(G)/R\to D$ with $S = S'\circ can$.


## Examples

1. Every category $C$ has a presentation by generators and relations:
Take $G$ as the underlying graph of $C$, and for objects $a$, $b$,
let $R_{a,b}$ be the relation on $F(G)(a,b)$ consisting of all pairs
of paths from $a$ to $b$ in $G$ whose arrows have the same composition
in $C$. However, there are sometimes more economical presentations for a
category, as the following example shows.

2. The augmented simplex category $\Delta_a$ is generated by the face maps and the degeneracy maps, subject to the simplicial relations (see [[simplex category]] for details).  The existence of a functor from the quotient category to $\Delta_a$ follows from the fact that the arrows of $\Delta_a$ do satisfy the simplicial relations, and the fact that this functor is an isomorphism may be verified using the unique decomposition of an arrow of $\Delta_a$ as the composition of degeneracies of decreasing index followed by the composition of face maps of increasing index (see the lemma on p. 177 of [Mac Lane](#MacLane)). Similarly, the subcategory $(\Delta_a)_{inj}$ consisting of all monics (injective monotone functions in our case) is generated by the face maps subject to the single simplicial relation involving only face maps.


##2-cells

A useful way to think of the relations is as being 2-cells between parallel pairs of arrows, thus if $a, b$ are objects, and $(u,v)\in R_{a,b}$, we think of $(u,v)$ as a 2-cell (initially _from $u$ to $v$_).  In this way, one can encode [[rewriting]] systems of a certain kind in terms of the embryonic data for a 2-category. This is discussed more in the entry on [[computad]], which are also called [[polygraphs]].

## References

* [[Saunders Mac Lane]],   [[Categories Work|Categories for the Working Mathematician]], pp. 51-52 
{#MacLane}

* [[Barry Mitchell]], _Introduction to Category Theory and
Homological Algebra_, in P. Salmon (Ed.), _Categories and Commutative
Algebra_.  Springer, 2010. pp. 108-112.{#Mitchel}

* [[Barry Mitchell]], _Rings with several objects_, Advances in Mathematics 8 (1972), 1&#8211;161.


[[!redirects presentation of a category by generators and relations]]
[[!redirects presentations of a category by generators and relations]]
[[!redirects presentations of categories by generators and relations]]
