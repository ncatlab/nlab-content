#Definition#

A **monoid** is the [[hom-set]] of a category with a single object. This is equivalent to whatever definition you may be used to. In partiocular, this means that a monoid is a set $A$ equipped with a binary operation $p : A \times A \to A$ and special element $e \in A$ such that $e$ and $p$ satisfy the usual axioms of an associative product $p$ with unit $e$.

Actually, one may wish to define a monoid to *be* a category with a single object, but taking this too literally will create conflicts in notation. Instead (for a given monoid $A$), let $\mathbf{B}A$ be the corresponding category with single object $\bullet$ and with $A$ as its [[hom-set]], so that $A = Hom_{\mathbf{B}A}(\bullet, \bullet)$. This realizes every monoid as a monoid of [[endomorphism|endomorphisms]].

#Remarks on notation
(originally from [[category algebra]])

It is important to _distinguish_ between a $k$-tuply monoidal structure and the corresponding $k$-tuply degenerate category, even though there is a map identifying them. The issue appears here for instance when discussing the universal $G$-bundle in its groupoid-incarnation. It is 
$$
  G \to \mathbf{E}G \to \mathbf{B}G
$$
(where $\mathbf{E}G = G//G$ is the action groupoid of $G$ acting on itself). On the left we crucially have $G$ as a monoidal 0-category, on the right as a once-degenerate 1-category. Without this notation we cannot even _write down_ the universal $G$-bundle!

Or take the important difference between group representations and group 2-algebras, the former being functors $\mathbf{B}G \to Vect$, the latter functors $G \to Vect$. This is important all over the place.

Or take an abelian group $A$ and a codomain like $2Vect$. Then there are 3 different things we can sensibly consider, namely 2-functors
$$
  A \to 2Vect
$$
$$
  \mathbf{B}A \to 2Vect
$$
$$
  \mathbf{B}^2A \to 2Vect
  \,.
$$
All of this is different. All of this is needed. The first one is the group 3-algebra of $A$. The second is pseudo-representations of the group $A$. The third is representations of the 2-group $\mathbf{B}A$. We have notation to distinguish this, and we should use it.

Finally, writing $\mathbf{B}G$ for the 1-object $n$-groupoid version of an $n$-monoid $G$ makes notation behave nicely with respect to nerves, because then realization bars $|\cdot|$ simply commute with the $B$s in the game: $|\mathbf{B}G| = B|G|$.

This behaviour under nerves shows also that, generally, writing $\mathbf{B}G$ gives the right intuition for what an expression means. For instance, what's the "geometric" reason that a group representation is an arrow $\rho : \mathbf{B}G \to Vect$? It's because this is, literally, equivalently thought of as the corresponding classifying map of the vector bundle on $\mathbf{B}G$ which is $\rho$-associated to the universal $G$-bundle:

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

In summary, it is important to make people understand that groups can be identified with one-object groupoids. But next it is important to make clear that not everything that can be identified is actually equal, for instance concerning the crucial difference between the category in which $G$ lives and the 2-category in which $\mathbf{B}G$ lives.

#Examples#

* A monoid in which every element has an inverse is a [[group]]. For that reason monoids are often addressed as _semi-group_s. (But this term is often extended to monoids without identities, that is to sets equipped with any associative operation.)

#Generalizations#

The concept _monoid_ makes sense in any [[monoidal category]] $(C, \otimes)$: a monoid in $C$ is an object $c$ equipped with a multiplication $\mu: c \otimes c \to c$ and a unit $\eta: I \to c$ satisfying evident associativity and unit axioms. Equivalently, a monoid is the [[hom-object]] of a $C$-enriched category with a single object.

For instance a "linear monoid" is a monoid in $Vect$, hence an [[algebra]]. 

Accordingly, the concept of monoid makes sense in any [[bicategory]] $B$: for any object $a$ of $B$, the local hom-category $B(a, a)$ carries a monoidal category structure, and a monoid in $B$ is a monoid $A: a \to a$ in such a monoidal category. A monoid in $B$ may also be described as the [[hom-object]] of a $B$-[[enriched category]] with a single object. Equivalently, this is the same as a [[monad]] in $B$.