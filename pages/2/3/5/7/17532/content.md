
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

This entry is about the category of [[G-set|continuous G-sets]], for a [[topological group]] $G$. Continuous $G$-sets are sets $X$ with an action of $G$ that is continuous when $X$ is given the discrete topology.

The category of continuous $G$-sets is a [[Grothendieck topos]], and is closely related to [[Fraenkel-Mostowski models]].

## Definition

Let $G$ be a topological group.

+-- {: .num_defn}
###### Definition

The **category of continuous $G$-sets** is the [[category]] of sets $X$ equipped with a continuous $G$-action $\mu: G \times X \to X$, where $X$ is given the discrete topology, and the morphisms are the $G$-invariant maps. We write the category as $G Set$. In this page, we always let $G$ act on the left.
=--

There is a simple characterization of when a $G$-action is continuous.

+-- {: .num_prop}
###### Proposition
Let $G$ be a topological group, and $X$ be a set with a $G$ action $\mu: G \times X \to X$. Then the action is continuous if and only if the stabilizer of each element is open.
=--

+-- {: .proof}
###### Proof
See [[G-sets#ContinuousCharacterization|G-sets]].
=--


## Properties

+-- {: .num_defn}
###### Notation
For a topological group $G$, we write $G^\delta$ for the discrete version of $G$. Every $G$-set can be viewed as a $G^\delta$ set in the obvious way.
=--

+-- {: .num_prop}
###### Proposition

The inclusion $i_G \colon G Set \to G^\delta Set$ has a [[right adjoint]] $r_G: G^\delta \to G Set$
such that for $X\in G Set$, the continuous $G$-set $r_G X$ is the subset of $X$ consisting of those points with open stabilizer.

=--

+-- {: .proof}
###### Proof
This follows from the observation that if $f: X \to Y$ is a $G$-invariant function between $G$-sets, then for each $x \in X$, the stabilizer of $f(x)$ includes the stabilizer of $x$.
=--

+-- {: .num_prop}
###### Proposition
The forgetful functor $U: G^\delta Set \to Set$ creates all [[small limit|small]] [[limits]] and [[colimits]].
=--

+-- {: .proof}
###### Proof
This follows from the general fact that limits and colimits in [[presheaf categories]] are computed pointwise.

Alternatively, there is an obvious $G$-action we can put on the limits or colimits of the underlying sets of the $G$-sets.

The creating limits part also comes from the fact that the forgetful functor is [[monadic]].
=--

+-- {: .num_prop}
###### Proposition
The inclusion $i_G: G Set \to G^\delta Set$ creates all finite limits and all colimits.
=--

+-- {: .proof}
###### Proof
This follows from the observation that the finite limits and colimits created by $U: G^\delta Set \to Set$ have a continuous action if each factor has a continuous action, using the fact that finite intersections and arbitrary unions of open sets are open.
=--

+-- {: .num_cor}
###### Corollary
The category $G Set$ has all [[finite limits]] and arbitrary [[colimits]].
=--

+-- {: .num_cor}
###### Corollary
The adjunction $i_G \dashv r_G$ is a geometric morphism.
=--

+-- {: .num_cor}
###### Corollary
A map in $G Set$ is a [[monomorphism]] if and only if it is injective; [[epimorphism]] if and only if it is surjective.
=--

+-- {: .proof}
###### Proof
A map is monic if and only if its kernel pair is an isomoprhism, and similarly for epic, and the forgetful functor to $Set$ preserves all finite limits and colimits.
=--

+-- {: .num_cor}
###### Corollary
The [[subobject classifier]] of $G Set$ is $\Omega = 2$, the two-point set
with the trivial $G$-action.
=--

+-- {: .num_prop}
###### Proposition
The [[exponential object]] in $G^\delta Set$ is defined by $Y^X = \{\text{functions}\;X \to Y\}$, with the $G^\delta$-action given by
$$
  g \cdot f = g \circ f \circ g^{-1}.
$$
The exponential object $Y^X$ in $G Set$ is given by the subset of the functions $X \to Y$ that have an open stabilizer, ie.
$$
  Y^X = r_G(i_G(Y)^{i_G(X)}).
$$
=--

+-- {: .proof}
###### Proof
Let $A, X, Y$ be $G^\delta$-sets. Given a map $f:A \times X \to Y$, we obtain $\hat{f}:A \to Y^X$ by
$$
  \hat{f}(a)(x) = f(a, x).
$$
We now check that $\hat{f}$ is $G^\delta$-invariant --- we have
$$
  (g \cdot \hat{f}(a))(x) = g \cdot \hat{f}(a)(g^{-1}\cdot x) = g \cdot f(a, g^{-1}x) = f(g \cdot a, x) = \hat{f}(g \cdot a)(x).
$$
So we get
$$
  g \cdot \hat{f}(a) = \hat{f}(g \cdot a).
$$
Conversely, given a $\hat{f}: A \to Y^X$, we obtain $f: A \times X \to Y$ by $f(a, x) = \hat{f}(a)(x)$, and we have
$$
  g \cdot f(a, x) = g \cdot \hat{f}(a)(x) = (g \cdot \hat{f}(a))(g\cdot x) = \hat{f}(g \cdot a)(g \cdot x) = f(g \cdot a, g \cdot x).
$$
So $f$ is $G^\delta$-invariant. It is clear that these operations are inverses to each other, and straightforward computations show that this is natural in $A$, $X$ and $Y$.

Then in general, if $A, X, Y$ are in fact $G$-sets, then we can compute
$$\begin{aligned}
  G Set\left(A, r_G(i_G(Y)^{i_G(X)})\right) &= G^\delta Set \left(i_G(A), i_G(Y)^{i_G(X)}\right)\\
  &= G^\delta Set\left(i_G(A) \times i_G(X), i_G(Y)\right)\\
  &= G^\delta Set\left(i_G(A \times X), i_G(Y)\right)\\
  &= G Set\left(A \times X, Y\right),
\end{aligned}$$
using the fact that $r_G(i_G(X)) = X$ for all $X \in G Set$.
=--

+-- {: .num_cor}
###### Corollary
The [[power object]] of $X \in G Set$ is given by the subsets of $X$ that have an open stabilizer.
=--

In conclusion we have:

+-- {: .num_theorem #GSetsIsAnElementaryTopos}
###### Theorem

The category $G Set$ is an [[elementary topos]].

=--

## Equivalent characterizations

### As a Grothendieck topos

+-- {: .num_theorem}
###### Theorem
Let $G$ be a topological group. Then the category $G Set$ is [[equivalence of categories|equivalent]] to the topos of [[sheaves]] on the [[atomic site|atomic]] [[site]] $(S(G), At)$, where the objects of $S(G)$ are the open subgroups of $G$, and the morphisms $H \to K$ are the left cosets $a K$ such that $H \subseteq a K a^{-1}$, and all non-empty [[sieves]] are covering.

Alternatively, it is the full subcategory of $G Set$ containing objects of the form $G/U$, where $U$ is an open subgroup. 
=--

+-- {: .proof}
###### Proof
See [MacLane and Moerdijk, Chapter III.9](#MaclaneMoerdijk).
=--

More generally, by the [[comparison lemma]], we have

+-- {: .num_theorem}
###### Theorem
Let $G$ be a topological group, and $\mathcal{U}$ be a cofinal set of open subgroups, ie. every open subgroup contains a member of $\mathcal{U}$. Then the category $G Set$ is equivalent to the topos of sheaves on the atomic site $(S(G, \mathcal{U}), At)$, where the objects of $S(G, \mathcal{U})$ are the open subgroups in $\mathcal{U}$, and the morphisms $H \to K$ are the left cosets $a K$ such that $H \subseteq a K a^{-1}$, and all non-empty sieves are covering.

Alternatively, it is the full subcategory of $G Set$ containing objects of the form $G/U$, where $U \in \mathcal{U}$.
=--

In particular, if $G$ is a discrete group, then the [[trivial subgroup]] itself is a cofinal set of open subgroups. So $G Set$ is the category of sheaves on the category with only one object, whose morphisms are the elements of $G$. This is the usual characterization of $G Set$ as the [[functor category]] $Set^G$.

### As a comonad algebra
To be included.

### As a classifying topos
To be included.

## For internal group actions
 {#InternalGroupActions}

The above construction of the category $G Set$ -- of [[G-sets]] for a [[discrete group]] $G$ in the [[topos]] [[Set]] of [[sets]] -- generalizes to [[group objects]] $G \in Groups(\mathcal{E})$ in any [[topos]] $\mathcal{E}$:

The resulting category $G\mathcal{E}$ -- of [[objects]] of $\mathcal{E}$ equipped with [[internalization|internal]] $G$-[[action]] and with $G$-[[equivariant function|equivariant]] [[morphisms]] between them -- is itself a [[topos]], by the same proof as above Thm \ref{GSetsIsAnElementaryTopos}. 

A particularly interesting case of this is an [[internal group]] $H$ in the topos $G Set$ itself, for $G$ a [[discrete group]] (a "$G$-[[equivariant group]]", see there for more): 

Seen externally this is equivalently a discrete group $H$ equipped with a [[group homomorphism]] $G \to \Aut(H)$ to the [[automorphism group]] of $H$. Notice that this data induces the corresponding [[semidirect product group|semidirect product]] $H \rtimes G$. With that, we have:

+-- {: .num_prop}
###### Proposition

Let $G$ be a [[discrete group]], and let $H$ be a [[group object]] in $G Set$. Then the category $H (G Set)$ is [[equivalence of categories|equivalent]] to $(H \rtimes G) Set$. 

=--

+-- {: .proof}
###### Proof sketch

This is a straightforward computation. Given an $X \in H (G Set)$, we write $\mu \colon H \times X \to X$ for the [[action]] morphism, and denote the action of $G$ merely by a dot. Then we define the action of $H \rtimes G$ by

$$
  ((h, g), x) \mapsto \mu(h, g \cdot x)
  \,.
$$

Conversely, given an object $X$ with an $H \rtimes G$ action, we give it a $G$ action by $g \cdot x = (e, g) \cdot x$, and an $H$-action by $\mu(h, x) = (h, e) \cdot x$.

=--

The case of [[topological groups]] is more complicated, because an internal topology $T$ on a space $X$ is an internally complete lattice $T \subseteq P(X)$, which is not necessarily closed under infinite external unions. However if we do the rather unnatural (?) thing of closing it under all external unions, then we make $X$ an external topological space. Then we have the following result:

+-- {: .num_prop}
###### Proposition

Let $G$ be a [[topological group]], and let $H$ be a topological group object in $G Set$. Then $H (G Set)$ is equivalent to $(H \rtimes G) Set$, where $H \rtimes G$ is given the product topology.

=--

The **proof** is a straightforward check that the continuity conditions match up.


## Related concepts

* [[G-set]]

* [[topological G-space]]

* [[permutation representation]]

* [[Fraenkel-Mostowski model]]

* [[class equation]]

## References

Some elementary properties of continuous $G$-sets can be found in books such as

* {#MaclaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]

The formal correspondence between permutation models of [[ZFA]] and toposes of continuous $G$-sets can be found in

* [[Michael Fourman]], _Sheaf models for set theory_, Journal of Pure and Applied Algebra, **19** (1980) pp 91-101, doi:[10.1016/0022-4049(80)90096-1](http://dx.doi.org/10.1016/0022-4049%2880%2990096-1), ([publisher pdf](http://www.sciencedirect.com/science/article/pii/0022404980900961/pdf?md5=0de18da810657bf1ba9de7399d224ec5&pid=1-s2.0-0022404980900961-main.pdf))



[[!redirects category of G sets]]
[[!redirects category of G set]]
[[!redirects category of G-set]]
[[!redirects category-of-G-sets]]

[[!redirects categories of G-sets]]
[[!redirects categories of G sets]]
[[!redirects categories of G-set]]
[[!redirects categories of G set]]


[[!redirects category of continuous G sets]]
[[!redirects category of continuous G-sets]]
[[!redirects category of continuous G set]]
[[!redirects category of continuous G-set]]
[[!redirects categories of continuous G-sets]]
[[!redirects categories of continuous G sets]]
[[!redirects categories of continuous G-set]]
[[!redirects categories of continuous G set]]
[[!redirects topos of G-sets]]
[[!redirects topos of G sets]]
[[!redirects topos of G-set]]
[[!redirects topos of G set]]
[[!redirects topos of continuous G sets]]
[[!redirects topos of continuous G-sets]]
[[!redirects topos of continuous G set]]
[[!redirects topos of continuous G-set]]
[[!redirects GSet]]

