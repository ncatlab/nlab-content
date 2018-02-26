
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

A comma double category is a generalization of a [[comma category]] to [[double categories]] and [[virtual double categories]]. For virtual double categories, it is a [[comma object]], but for double categories the comma double category $f/g$ can be constructed when $f : C \to E$ is an [[oplax functor]] $g : D \to E$ is a [[lax functor]] $g : D \to E$.

## Definition for Virtual Double Categories ##

For virtual double categories, the comma virtual double category has the universal property of a [[comma object]] in the 2-category of virtual double categories, functors and vertical transformations.

Explicitly, it is constructed as follows. Let $C, D, E$ be virtual double categories and $F : C \to E, G : D \to E$ be functors of virtual double categories. The comma double category $F / G$ is defined as

1. Its vertical category is the ordinary comma category $F_v/G_v$ of the vertical components of the functors. We write an object as $A : F A_C \to G A_D$.
2. A horizontal arrow $R$ from $A$ to $B$ consists of horizontal arrows $R_C : A_C \to B_C$ and $R_D : A_D \to B_D$ and a 2-cell in $E$ from $F R_C$ to $G R_D$ along $A,B$.
3. A 2-cell $\alpha$ from $R_1,\ldots,R_n$ to $S$ consists of a pair of 2-cells $\alpha_C : (R_{1C},\ldots,R_{nC}) \to S_C$ and $\alpha_D : (R_{1D},\ldots,R_{nD}) \to S_D$ such that $G(\alpha_D) \circ (R_1,\ldots,R_n) = S \circ F(\alpha_C)$.

## Representability ##

Next, we consider what properties are required of the input data to determine that a comma virtual double category has units and composites. An analogy with the double category case gives some guidance. Since functors of virtual double categories correspond to *lax* functors of double categories, we don't have any requirements for the functor $G$ on top of $D$ having composites or units. On the other hand, for $F$ to be "oplax", we require that it be normal for units or furthermore strong for composites.

The following are not yet verified

+-- {: .un_prop} 
###### Conjecture

If $C$ and $D$ have units and $F$ is a normal functor, then $F / G$ has units.
=--

+-- {: .un_prop} 
###### Conjecture

If $C$ and $D$ have composites and $F$ is a strong functor, then $F / G$ has composites.
=--


## Examples ##

1. A monad $T$ in the horizontal bicategory of a double category $C$ is equivalent to a lax functor $T : 1 \to C$ from the terminal double category. In this case we might call $Id_C / T$ the [[slice category|slice double category]].
2. The double category of [[decorated cospans]] is naturally constructed as a comma double category.
3. [[generalized multicategories]] can be constructed using a slice category when the monad $T$ is a [[polynomial monad]]. The slice over $T$ is equivalent to the "horizontal Kleisli category" presented in Crutwell-Shulman if $T$'s underlying object is the terminal object. $T$-multicategories are then monads in that comma double category.
4. [[poset-valued sets]] given by an endofunctor $F$ on $Rel$ and a poset $P$ can be viewed as the comma double category from $F$ to $P$, since a poset is a monad in $Rel$.

##References

An explicit description of the comma double category from an oplax to a lax functor is given in 

* [[Kenny Courser]], _A bicategory of decorated cospans_ ([arxiv](https://arxiv.org/abs/1605.08100))

