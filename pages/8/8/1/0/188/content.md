
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


\tableofcontents

## Idea
 {#Idea}

In [[algebra]], by a *monoid* one means a collection ([[set]]) of elements equipped with a [[binary operation]] (a "multiplication operation") which is [[associativity|associative]] and has a [[unit element]].

Hence monoid structure on a set is a fairly rudimentary form of algebraic [[structure]] which [[underlying|underlies]] many familiar [[structures]] considered [[algebra]], such as that of *[[groups]]* (which are monoids with all [[inverse elements]]) and *[[rings]]* (which are [[abelian groups]] compatibly equipped with a *second* monoid structure). 

Therefore, in the algebraic literature monoids are, conversely, often called *unital [[semi-groups]]*. The root "mono-" in "monoid" refers to the  single [[binary operation]] (cf. *[[duoid]]* and *[[dioid]]*).

The terminology of *[[magmas]]* is meant to invoke this rudimemtary but foundational nature of basic algebraic structures: Monoids are precisely the [[unital magma|unital]] [[associative magmas]].

The [[categorification]] of the notion of monoids is that of *[[monads]]* whose ubiquitous role in [[mathematics]] (together with their [associated](adjoint+functor#RelationBetweenAdjunctionsAndMonads) [[adjoint functors]]) is hard to overstate.




## Definitions

### Elementary definition

The classical definition of monoids in [[Sets]], as a [[unital magma|unital]] [[associative magma]]:

\begin{definition}\label{MonoidsInSets}
A **monoid** is a [[set]] $M$ equipped with the [[structure]] if 

1. (**[[binary operation]]**) a [[map]] from the [[Cartesian product]] of the set with itself to itself

   $$
     (\text{-}) \cdot (\text{-}) 
       \,\colon\, 
     M \times M \to M
   $$ 

1. (**[[neutral element]]**) an [[element]] 

   $$1 \in M$$ 

such that the following [[equations]] are satisfied

1. (**[[associativity]]**)

   $$ 
     x, y, z \,\in\, M
     \;\;\;\;\;
       \vdash
     \;\;\;\;\;
     (x \cdot y) \cdot z 
       \;=\; 
     x \cdot (y \cdot z)
     \mathrlap{\,,}
   $$

* (**[[unitality]]**) 

  $$ 
    x \in M
     \;\;\;\;\;
       \vdash
     \;\;\;\;\;
    1 \cdot x 
      \;=\; 
    x 
      \;=\; 
    x \cdot 1
    \mathrlap{\,.}
  $$

\end{definition}


### In a monoidal category
{#inamonoidalcategory}

See *[[monoid in a monoidal category]]*.

### In terms of string diagrams

The data of a monoid may be written in [[string diagrams]] as:

[[monoid-data-labeled.png:pic]]

Thanks to the distinctive shapes, one can usually omit the labels:

[[monoid-data-unlabeled.png:pic]]

The axioms $\mu \cdot (\eta \otimes M) = 1_M = \mu \cdot (M \otimes \eta)$ and $\mu \cdot (M \otimes \mu) = \mu \cdot (\mu \otimes M)$ then appear as:

[[monoid-axioms-unlabeled.png:pic]]


### As a one-object category
 {#AsAOneObjectCategory}

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

## Properties

### Finite products (and sums)

Let $M$ be a monoid, and let $M^*$ be the [[free monoid]] on $M$ with canonical function $h:M \to M^*$ taking the elements of $M$ to the generators in $M^*$. The finite product operation on $M$ is a [[monoid homomorphism]] 

$$\prod_{i = 0}^{\mathrm{len}(-) - 1}(-)(i):M^* \to M$$ 

from $M^*$ to $M$, where:

$$\prod_{i = 0}^{\mathrm{len}(\epsilon) - 1} \epsilon(i) = 1$$

$$\prod_{i = 0}^{\mathrm{len}(h(a)) - 1} (h(a))(i) = a$$

$$\left(\prod_{i = 0}^{\mathrm{len}(a) - 1} a(i)\right) \cdot \left(\prod_{i = 0}^{\mathrm{len}(b) - 1} b(i)\right) = \prod_{i = 0}^{\mathrm{len}(a b) - 1} (a b)(i)$$

If $M$ is written additively $(+, 0)$ instead of multiplicatively $(\cdot, 1)$, the operation is called finite sum, and is defined as 

$$\sum_{i = 0}^{\mathrm{len}(-) - 1}(-)(i):M^* \to M$$ 

from $M^*$ to $M$, where:

$$\sum_{i = 0}^{\mathrm{len}(\epsilon) - 1} \epsilon(i) = 0$$

$$\sum_{i = 0}^{\mathrm{len}(h(a)) - 1} (h(a))(i) = a$$

$$\left(\sum_{i = 0}^{\mathrm{len}(a) - 1} a(i)\right) + \left(\sum_{i = 0}^{\mathrm{len}(b) - 1} b(i)\right) = \sum_{i = 0}^{\mathrm{len}(a b) - 1} (a b)(i)$$

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

* [[monoidal symmetric proset]]

* **monoid**, internal monoid/monoid object,

  * [[commutative monoid]], [[cancellative monoid]]

  * [[monoidal groupoid]], [[braided monoidal groupoid]], [[symmetric monoidal groupoid]]

  * [[k-tuply monoidal n-groupoid]]

  * [[algebra in an (∞,1)-category|monoid object in a (∞,1)-category]]

* [[topological monoid]]

* [[comonoid]], [[cocommutative comonoid]]

* [[duoid]]

* [[group]], [[group object]]

* [[ring]], [[ring object]]

* [[categorical algebra]]

* [[A3-type]]

[[!include oidification - table]]

## References

Beware that the term "monoid" was first used by

* [[Arthur Cayley]], *Second and Third Memoirs on Skew Surfaces*, Otherwise Scrolls, Phil. Trans. (1863 and 1869)

for certain [[surfaces]], quite unrelated to the modern meaning of the term.

Instead, what are now called *monoids* ([[unital magma|unital]] [[associative magmas]]) were called *groupoids* (now clashing with the modern use of *[[groupoid]]*) by

* [[Garrett Birkhoff]], *Hausdorff Groupoids*, Annals of Mathematics, Second Series **35** 2 (1934) 351-360 &lbrack;[jstor:1968437](https://www.jstor.org/stable/1968437), [doi:10.2307/1968437](https://doi.org/10.2307/1968437)&rbrack;

The modern terminology "monoid" for unital associative magmas is (according to [Hollings 2009, p. 529](#Hollings09)) due to 

* [[Nicolas Bourbaki]], [[Éléments de Mathématique]] (1943)

For more on the history of the notion:

* {#Hollings09} Christopher Hollings, *The Early Development of the Algebraic Theory of Semigroups*, Archive for History of Exact Sciences **63** (2009) 497–536 &lbrack;[doi:10.1007/s00407-009-0044-3](https://doi.org/10.1007/s00407-009-0044-3)&rbrack;

* Math.SE, *[Who invented Monoid?](https://mathoverflow.net/q/338281/381)*

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_

Properties of monoids expressed through properties of their [[toposes]] of [[presheaves]]:

* Jens Hemelaer, Morgan Rogers, _Monoid Properties as Invariants of Toposes of Monoid Actions_, [arXiv:2004.10513](https://arxiv.org/abs/2004.10513).

Formalization of [[monoid objects]] as [[mathematical structures]] in [[proof assistants]]:

in a context of plain [[Agda]]:

* [[Martín Escardó]], *[The Types of Magmas and Monoids](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#magmasandmonoids)*, §4 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

in a context of [[cubical type theory|cubical]] [[Agda]]:

* [[1lab]]: *[Algebra.Monoid](https://1lab.dev/Algebra.Monoid.html)*




[[!redirects monoid]]
[[!redirects monoids]]