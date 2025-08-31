
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In general, the _center_ (or _centre_) of an [[algebra|algebraic]] [[object]] $A$ is the collection of [[elements]] of $A$ which "commute with all elements of $A$."  This has a number of specific incarnations.

## Definitions

### Of groups and monoids
 {#OfGroupsAndMonoids}

The original example is the __center__ $Z(G)$ of a [[group]] $G$, which is defined to be the [[subgroup]] consisting of all elements $g\in G$ such that for all elements $h\in G$ the equality $g h=h g$ holds.  The center is an [[abelian group|abelian]] subgroup, but not every abelian subgroup is in the center.  See also [[centralizer]].

This notion of the center of a group can be generalized to the center of a [[monoid]] in an obvious way.

+-- {: .num_defn}
###### Definition

Let $C$ be an object in a [[2-category]]. The center of $C$, $Z(C)$ is the [[monoid]] of [[endomorphisms]] of the identity morphism, $id_C : C \rightarrow C$.
=--

One can invoke the [[Eckmann-Hilton argument]] to prove that vertical and horizontal composition agree on $Z(C)$ and are commutative. 

### Of rings

The __center__ $Z(R)$ of a [[ring]] $R$ is defined to be the [[multiplicative subset]] consisting of all elements $r \in R$ such that for all elements $s \in R$, $r \cdot s = s \cdot r$ is true. $R$ is a [[commutative ring]] if $R$ is isomorphic to $Z(R)$. 

### Of Lie algebras

The __center of a [[Lie algebra]]__ $L$ is an abelian Lie subalgebra $Z(L)$, consisting of all elements $ z\in L$ such that $[l,z]=0$ for all $l\in L$. There are generalizations for some other kinds of algebras.


### Of (higher) categories
  {#OfCategories}

#### Of general categories

The notion of the *[[center]] of a [[monoid]]* has a [[horizontal categorification]] to a notion of the *[[center of a category]]*.
 
For $C$ a category, its center is defined to be the [[commutative monoid]] 

$$
  Z(C)
  \;\coloneqq\;
  [C,C](Id_C,Id_C)
$$ 

of [[endomorphism|endo]]-[[natural transformations]] of the [[identity functor]] $Id_C \,\colon\, C \to C$, i.e. the [[endomorphism monoid]] of $Id_C$ in the [[functor category]] $[C,C]$.  

It is straightforward to check that this reduces to the usual definition of the center of a monoid $D$ in the case that $C = \mathbf{B}(A,\cdot)$ is the corresponding [[delooping]].

* For a [[generator]] $G$ of a category $\mathcal{C}$, there is an embedding of $Z(\mathcal{C})$ into the monoid $Hom(G,G)$ given by $\eta\mapsto\eta _G$. In particular, if $Hom(G,G)$ or $Z(Hom(G,G))$ is trivial, as happens, e.g., for $Set$ with $G=\ast$, then so is $Z(\mathcal{C})$ 
&lbrack;[Hoffmann (1975)](#Hoffmann75)&rbrack;

* For [[Cauchy completion|Cauchy complete]] $\mathcal{C}$, the idempotent elements of $Z(\mathcal{C})$ correspond precisely to the _quintessential localizations_ of $\mathcal{C}$ &lbrack;[Johnstone (1996)](#Johnstone96)&rbrack;


#### Of abelian categories

If a category carries further [[structure]], then this may be inherited by its center. Notably, the center of an [[additive category]] is not just a [[commutative monoid]] but a [[commutative ring]] (the [[endomorphism ring]] of its [[identity functor]]).

For more on this, see *[[center of an abelian category]]*.


#### Of higher categories

The notion of a center also has a [[vertical categorification]]. It is easy to categorify the notion of the center of a category as defined above: if $C$ is an [[n-category]], then its _center_ is the monoidal $(n-1)$-category $[C,C](Id_C,Id_C)$ of endo-transformations of its identity functor.  One expects that, in general, this center will actually admit a natural structure of a *braided* monoidal $(n-1)$-category, just as the center of a category is actually a commutative monoid, not merely a monoid.

For instance, if $C = \mathbf{B}_\otimes \mathcal{C}$ is the [[delooping]] of a [[monoidal category]], then this center is called the _[[Drinfeld center]]_ of $(C, \otimes)$.

Generally, we can obtain a notion of the center of a monoidal $n$-category by regarding it as a one-object $(n+1)$-category, according to the [[delooping hypothesis]].  It follows that the center of a monoidal $n$-category should naturally be a braided monoidal $n$-category.  This is known to be true when $n=0$ (the center of a monoid is a commutative monoid) and also for $n=1$ and $n=2$.

Note that a monoidal $n$-category has two different centers: if we regard it as a one-object $(n+1)$-category, then its center is a braided monoidal $n$-category, but if we regard it merely as an $n$-category, then its center is a braided monoidal $(n-1)$-category. The latter construction makes no reference to the monoidal structure. Likewise, a braided monoidal $n$-category has three different centers, depending on whether we regard it as an $n$-category, a connected $(n+1)$-category, or a 2-connected $(n+2)$-category, and so on (a $k$-tuply monoidal $n$-category has $k+1$ different centers).

It seems that, in applications, one is usually most interested in the sort of center of a monoidal $n$-category $C$ obtained by regarding it as a one-object $(n+1)$-category, thereby obtaining a braided monoidal $n$-category.  It is in this case, and seemingly this case only, that the center comes with a natural forgetful functor to $C$, corresponding to the classical inclusion of the center of a monoid.  (For $n\gt 0$, however, this functor will not be an inclusion; the objects of the center of $C$ are objects of $C$ equipped with additional [[stuff, structure, property|structure]].)

Moreover, one expects that if we perform this "canonical" operation on a [[k-tuply monoidal n-category]] (for $k\ge 1$), the resulting braided monoidal $n$-category will actually be $(k+1)$-tuply monoidal.  This is known to be true in the cases $n\le 4$: the center of a braided monoidal category is symmetric monoidal, the center of a braided monoidal 2-category is sylleptic, and the center of a sylleptic monoidal 2-category is symmetric.

Finally, if we decategorify further, we find that the center of a [[set]] (i.e. a [[0-category]]) is a monoidal [[(-1)-category]], i.e. the [[truth value]] "true."  This is what we ought to expect, since when $C$ is a set, there is precisely one endo-transformation of its identity endofunction (namely, the identity).


### Of $\infty$-groups

See *[[center of an ∞-group]].


## Related concepts

* [[center of a category]]

  [[center of an additive category]]

  [[Drinfeld center]]

* [[central product of groups]]

## References

See also

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Center_(group_theory)">Center (group theory)</a>_


On the notion of [[center of a category]]:

* {#Hoffmann75} [[Rudolf-E. Hoffmann]], *Über das Zentrum einer Kategorie*, Math. Nachr. **68** (1975) 299-306 &lbrack;[doi:10.1002/mana.19750680122](https://doi.org/10.1002/mana.19750680122)&rbrack;

* {#Johnstone96} [[Peter Johnstone]], _Remarks on Quintessential and Persistent Localizations_, TAC **2** 8 (1996) 90-99 &lbrack;[tac:2-08](http://www.tac.mta.ca/tac/volumes/1996/n8/2-08abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf)&rbrack;

and of an [[enriched category]]:

* [[Harald Lindner]]. _Center and trace_, Archiv der Mathematik 35 (1980): 476-496. ([doi:10.1007/BF01235372](https://doi.org/10.1007/BF01235372))


[[!redirects centre]]
[[!redirects centers]]
[[!redirects centres]]



[[!redirects center of a group]]
[[!redirects center of a monoid]]



