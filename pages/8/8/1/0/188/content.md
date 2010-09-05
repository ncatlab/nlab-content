# Monoids
* ten of clubs
{:toc}

## Definitions

### Classical

Classically, a **monoid** is a set $M$ equipped with a binary operation $\mu: M \times M \to M$ and special element $1 \in M$ such that $1$ and $x \cdot y = \mu(x,y)$ satisfy the usual axioms of an associative product with unit, namely the **associative law**:

$$ (x \cdot y) \cdot z = x \cdot (y \cdot z)$$

and the **left and right unit laws**: 

$$ 1 \cdot x = x = x \cdot 1 .$$


### In a monoidal category

More generally, we can define a monoid (sometimes called **monoid object**) in any [[monoidal category]] $(C,\otimes,I)$.  Namely, a **monoid in $C$** is an object $M$ equipped with a multiplication $\mu: M \otimes M \to M$ and a unit $\eta: I \to M$ satisfying the **associative law**:

![A pic](http://upload.wikimedia.org/wikipedia/commons/b/b1/Monoid_mult.png)

and the **left and right unit laws**:

![A pic](http://upload.wikimedia.org/wikipedia/commons/1/10/Monoid_unit.png)

Here $\alpha$ is the [[associator]] in $C$, while $\lambda$ and $\rho$ are the left and right [[unitor|unitors]].

Classical monoids are of course just monoids in [[Set]] with the [[cartesian product]].

By the [[microcosm principle]], in order to define monoid objects in $C$, $C$ itself must be a "categorified monoid" in some way.  The natural requirement is that it be a [[monoidal category]].  In fact, it suffices if $C$ is a [[multicategory]].  Contrast this with a [[group object]], which can only be defined in a [[cartesian monoidal category]] (or a [[cartesian multicategory]]).


### In string diagrams

The data of a monoid may be written in [[string diagrams]] as:

[[monoid-data-labeled.png:pic]]

Thanks to the distinctive shapes, one can usually omit the labels:

[[monoid-data-unlabeled.png:pic]]

The axioms $\mu \cdot (\eta \otimes M) = 1_M = \mu \cdot (M \otimes \eta)$ and $\mu \cdot (M \otimes \mu) = \mu \cdot (\mu \otimes M)$ then appear as:

[[monoid-axioms-unlabeled.png:pic]]


### As a one-object category

Equivalently, and more efficiently, we may say that a (classical) monoid is the [[hom-set]] of a [[category]] with a single [[object]], equipped with the structure of its unit element and composition. 

More tersely, one may say that a monoid *is* a category with a single object, or more precisely (to get the proper morphisms and $2$-morphisms) a [[pointed object|pointed]] category with a single object. 
But taking this too literally may create conflicts in notation.  To avoid this, for a given monoid $M$, we write $\mathbf{B}M$ for the corresponding category with single object $\bullet$ and with $M$ as its [[hom-set]]: the [[delooping]] of $M$, so that $M = Hom_{\mathbf{B}M}(\bullet, \bullet)$. This realizes every monoid as a monoid of [[endomorphism|endomorphisms]].

Similarly, a monoid in $(C,\otimes,I)$ may be defined as the [[hom-object]] of a $C$-[[enriched category]] with a single object, equipped with its composition and identity-assigning morphisms; and so on, as in the classical (i.e. $\mathbf{Set}$-enriched) case.

For more on this see also [[group]].


## Examples

* A monoid in which every element has an inverse is a [[group]]. For that reason monoids are often known (especially outside category theory) as _semi-group_s. (But this term is often extended to monoids without identities, that is to sets equipped with any associative operation.)
* A monoid object in [[Ab]] (with the usual tensor product of $\mathbb{Z}$-modules as the tensor product) is a [[ring]].
 A monoid object in the category of vector spaces over a field $k$ (with the usual tensor product of vector spaces) is an [[algebra]] over $k$.
* For a commutative ring $R$, a monoid object in the category of $R$-modules (with its usual tensor product) is an $R$-algebra.
* A monoid object in [[Top]] (with cartesian product as the tensor product) is a topological monoid.
* A monoid object in the category of monoids (with cartesian product as the tensor product) is a commutative monoid.  This is a version of the [[Eckmann-Hilton argument]].
* A monoid object in the category of complete join-[[semilattice]]s (with its tensor product that represents maps preserving joins in each variable separately) is a unital [[quantale]].
* Given any monoidal category $C$, a monoid in the monoidal category $C^{op}$ is called a [[comonoid]] in $C$.
* In a [[cocartesian monoidal category]], every object is a monoid object in a unique way.
* For any category $C$, the [[endofunctor]] category $C^C$ has a monoidal structure induced by composition of endofunctors, and a monoid object in $C^C$ is a [[monad]] on $C$.

These are examples of monoids internal to monoidal categories.  More generally, given any [[bicategory]] $B$ and a chosen object $a$, the [[hom-category]] $B(a,a)$ has the structure of a monoidal category.  So, the concept of monoid makes sense in any [[bicategory]] $B$: we define a **monoid in $B$** to be a monoid in $B(a,a)$ for some object $a \in B$.  This often called a [[monad]] in $B$.  The reason is that a monad in [[Cat]] is the same as monad on a category.

A monoid in a bicategory $B$ may also be described as the [[hom-object]] of a $B$-[[enriched category]] with a single object. 


## Remarks on notation

It can be important to distinguish between a $k$-tuply monoidal structure and the corresponding $k$-tuply degenerate category, even though there is a map identifying them. The issue appears here for instance when discussing the universal $G$-bundle in its groupoid incarnation.  This is 
$$
  G \to \mathbf{E}G \to \mathbf{B}G
$$
(where $\mathbf{E}G = G//G$ is the action groupoid of $G$ acting on itself). On the left we crucially have $G$ as a monoidal 0-category, on the right as a once-degenerate 1-category. Without this notation we cannot even _write down_ the universal $G$-bundle!

Or take the important difference between group [[representation]]s and group 2-algebras, the former being functors $\mathbf{B}G \to Vect$, the latter functors $G \to Vect$. Both these are very important.

Or take an abelian group $A$ and a codomain like $2Vect$. Then there are 3 different things we can sensibly consider, namely 2-functors
$$
  A \to 2Vect
$$
$$
  \mathbf{B}A \to 2Vect
$$
and
$$
  \mathbf{B}^2A \to 2Vect
  \,.
$$
All of these concepts are different, and useful. The first one is an object in the group 3-algebra of $A$. The second is a pseudo-representation of the group $A$. The third is a representations of the 2-group $\mathbf{B}A$. We have notation to distinguish this, and we should use it.

Finally, writing $\mathbf{B}G$ for the 1-object $n$-groupoid version of an $n$-monoid $G$ makes notation behave nicely with respect to nerves, because then realization bars $|\cdot|$ simply commute with the $B$s in the game: $|\mathbf{B}G| = B|G|$.

This behavior under nerves shows also that, generally, writing $\mathbf{B}G$ gives the right intuition for what an expression means. For instance, what's the "geometric" reason that a group representation is an arrow $\rho : \mathbf{B}G \to Vect$? It's because this is, literally, equivalently thought of as the corresponding classifying map of the vector bundle on $\mathbf{B}G$ which is $\rho$-associated to the universal $G$-bundle:

the $\rho$-associated vector bundle to the universal $G$-bundle is, in its groupoid incarnations,
$$
  \array{
    V
    \\
    \downarrow
    \\
    V//G
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
  \,,
$$
where $V$ is the vector space that $\rho$ is representing on, and this is classified by the representation $\rho : \mathbf{B}G \to Vect$ in that this is the pullback of the universal $Vect$-bundle
$$
  \array{
    V//G
    &\to&
    Vect_*
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{B}G
    &\stackrel{\rho}{\to}&
    Vect
  }
  \,,
$$

In summary, it is important to make people understand that groups can be identified with one-object groupoids. But next it is important to make clear that not everything that can be identified should be, for instance concerning the crucial difference between the category in which $G$ lives and the 2-category in which $\mathbf{B}G$ lives.


[[!redirects monoid]]
[[!redirects monoids]]

[[!redirects monoid object]]
[[!redirects monoid objects]]
[[!redirects internal monoid]]
[[!redirects internal monoids]]
