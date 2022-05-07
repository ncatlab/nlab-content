
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--


# Monoids
* table of contents
{:toc}

## Definitions

### Classical

Classically, a **monoid** is a set $M$ equipped with a binary operation $\mu: M \times M \to M$ and special element $1 \in M$ (the _[[neutral element]]_) such that $1$ and $x \cdot y = \mu(x,y)$ satisfy the usual axioms of an associative product with unit, namely the **[[associative law]]**:

$$ (x \cdot y) \cdot z = x \cdot (y \cdot z)$$

and the **left and right [[unit laws]]**: 

$$ 1 \cdot x = x = x \cdot 1 .$$


### In a monoidal category
{#inamonoidalcategory}

See [[monoid in a monoidal category]].

### In terms of string diagrams

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

### As a strict monoidal category

An alternate way to view a monoid as a category is as a discrete [[strict monoidal category]] $\mathbf{C}$ where the elements of the monoid are the objects of $\mathbf{C}$, the binary operation of the monoid provides the tensor product bifunctor, and the identity of the monoid is the unit object. Preordered monoids then yield (non-discrete) strict monoidal categories with the morphisms witnessing the preorder in the usual way.

### $\mathcal{O}$-Monoids over an $(\infty,1)$-Operad

The notion of _associative monoids_ discussed above are controled by the 
[[associative operad]]. More generally in [[higher algebra]], for $\mathcal{O}$ any [[operad]] or [[(infinity,1)-operad]], one can consider **$\mathcal{O}$-monoids**. ([Lurie, def. 2.4.2.1](#Lurie))

These are closely related to [[(infinity,1)-algebras over an (infinity,1)-operad]] with respect to $\mathcal{O}$ ([Lurie, prop. 2.4.2.5](#Lurie)).


## Examples

* A monoid in which every element has an inverse is a [[group]]. For that reason monoids are often known (especially outside category theory) as _semi-group_s. (But this term is often extended to monoids without identities, that is to sets equipped with any associative operation.)
* The set of [[endomorphism|endomorphisms]] of a given object in a category has a canonical monoid structure given by composition. 


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

## Related concepts

* [[monoid in a monoidal category]], [[category of monoids]]

* **monoid**, internal monoid/monoid object,

  * [[commutative monoid]], [[cancellative monoid]]

  * [[algebra in an (∞,1)-category|monoid object in a (∞,1)-category]]

* [[topological monoid]]

* [[comonoid]], [[cocommutative comonoid]]

* [[group]], [[group object]]

* [[ring]], [[ring object]]

* [[categorical algebra]]

## References

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_

Properties of monoids expressed through properties of their [[toposes]] of [[presheaves]]:

* Jens Hemelaer, Morgan Rogers, _Monoid Properties as Invariants of Toposes of Monoid Actions_, [arXiv:2004.10513](https://arxiv.org/abs/2004.10513).


[[!redirects monoid]]
[[!redirects monoids]]