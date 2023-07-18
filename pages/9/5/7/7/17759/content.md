
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[Grothendieck ring]] of every fusion category can be naturally viewed as an (algebraic) [[Z+ ring|fusion ring]]. The structure of this resulting ring is purely determined by the fusion rules of the staring category. Hence, it is known as the __fusion ring__ of the fusion category.

This ring encodes a large amount of the structure of the category, but not all of it. Namely, there are non-isomorphic fusion categories with isomorphic fusion rings. For example, the representation categories of the two non-isomorphic non-abelian groups of order eight have isomorphic fusion rings.

The strongest result in this direction is [[Ocneanu Rigidity]], which asserts that there are only finitely many isomorphism classes of categories which induce a given fusion ring. A standard approach towards classifications of fusion categories thus begins by first understanding fusion rings, and then understanding what categorifications can be imposed.

Such a choice of categorification amounts to a choice of associativity on the monoidal structure of your category. These associativity rules can be also described explicitely in terms of algebraic structure on your distinguished $\mathbb{Z}_+$ basis by using [[Wigner 6-j symbol | 6j symbols]].

## Definition

Let $\mathcal{C}$ be a [[fusion category]], i.e. a [[tensor category]] which is [[finite abelian category|finite]] and [[semisimple category | semisimple]] (i.e. it has a [[finite number]] of [[isomorphism classes]] $[X_i]$ of [[simple objects]], all finite [[direct sums]] of these exist, and every object is isomorphic to such).

Let $Gr(\mathcal{C})$ be the Grothendieck ring of $\mathcal{C}$. That is, the ring whose objects are isomorphism classes of objects in $\mathcal{C}$, whose addition is defined by $[X]+[Y]=[X\oplus Y]$, and whose multiplication is defined by $[X]\cdot [Y]=[X\otimes Y]$.

The set of simple objects of $\mathcal{C}$ give a [[Z+ ring |$\mathbb{Z}_+$-basis]] for $Gr(\mathcal{C})$. This follows immediately from the fact that every object is isomorphic to the direct sum of some integer number of copies of every simple objects.

The fact that the tensor unit is simple implies that $Gr(\mathcal{C})$ is moreover a unital $\mathbb{Z}_+$ring.

The rigidity structure $*$ on $\mathcal{C}$ induces an anti-involution on $Gr(\mathcal{C})$, which gives it the structure of a fusion ring.


## Related concepts

* [[Frobenius-Perron dimension]]

* [[Clebsch-Gordan coefficient]]

* [[Verlinde algebra]]

## References

* [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]] Tensor categories. Vol. 205. American Mathematical Soc., 2016.

* [[Sonia Natale]]. "On the classification of fusion categories." Proc. Int. Congr. Mathematicians, Rio de Janeiro (2018): 173-200.
