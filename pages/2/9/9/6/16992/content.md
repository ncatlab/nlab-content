## Idea 

Let $G$ be a group or a discrete groupoid. Recall that an associative [[ring]] is a [[semigroup]] (if unital then monoid) in the category of abelian groups and a [[quantale]] a semigroup in the category of [[sup-lattice]]s.

While [[groupoid algebra|group(oid) ring]] $\mathbb{Z}G$ is the free abelian group with basis $G$ (resp. $Mor(G)$) with convolution product making it a ring, the groupoid quantale is the free sup-lattice with basis $G$ and the convolution product making it a quantale.

## Construction-definition

The free sup-lattice on a set $X$ is the power set $P(X)$ (set of subsets of $X$) with the infinite union and finite intersection as sup $\Vee$ (infinite join) and meet $\wedge$ respectively; or equivalently the set $2^X$ of boolean functions on $X$. 
If $X = Mor(C)$ is a morphism set of a category (special cases: semigroup, group, groupoid)
then $P(Mor(C))$ has the multiplication

$$
 A B = \{ a b \,|\, a\in A, b\in B, a\,\,\, and\,\,\, b\,\,\, compose \}
$$
or, in terms of functions (the characteristic function of the subsets of $C$) of $f,g\in 2^{Mor(C)}$, the __convolution product__

$$
(f \ast g)(c) = \Vee \{ f(a)\wedge f(b)\,|\, c = a b \}
$$

This way, $2^{Mor(C)}$ becomes a quantale denoted simply $2^C$, 
which may be called a category quantale. This
quantale is unital; namely the unit in $P(Mor(C))$ is the set of units $Ob(C) = C_0$ of the quantale which is canonically identified with a subset of $Mor(C)$. The unit for the convolution is, equivalently, the characteristic function of $C_0$.

If $C = G$ is a groupoid, then there is an additional involution $\star$ on $P(Mor(G))$ where

$$
X^\star = \{ g^{-1} \,|\, g\in X \}
$$

for $X \subset Mor(G)$. In terms of the convolution quantale $2^G$,

$$
f^*(g) = f(g^{-1}), \,\,\,\,f\in 2^{Mor(G)}, g\in G.
$$

This groupoid quantale is therefore an involutive unital quantale. 

## Literature

* [[Pedro Resende]], _&#201;tale groupoids and their quantales_, Advances in Mathematics 208 (2007) 147&#8211;209 [doi](http://dx.doi.org/10.1016/j.aim.2006.02.004)

