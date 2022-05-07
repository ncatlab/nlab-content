
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Coproducts
* tic
{: toc}

## Idea

The notion of _coproduct_ is a generalization to arbitrary [[categories]] of the notion of [[disjoint union]] in the category [[Set]].


## Definition

For $C$ a [[category]] and $x, y \in Obj(C)$ two [[object]]s, their **coproduct** is an object $x \coprod y$ in $C$ equipped with two [[morphism]]s

$$
  \array{
    x &&&& y
    \\
    & {}_{\mathllap{i_x}}\searrow && \swarrow_{\mathrlap{i_y}}
    \\
    && x \coprod y
  }
$$

such that this is [[universal property|universal]] with this property, meaning such that for any other object with maps like this

$$
  \array{
    x &&&& y
    \\
    & {}_{\mathllap{f}}\searrow && \swarrow_{\mathrlap{g}}
    \\
    && Q
  }
$$

there exists a _unique_ morphism $(f,g) :  x \coprod y \to Q$ such that we have a [[commuting diagram]]

$$
  \array{
    x &\stackrel{i_x}{\to}& x \coprod y &\stackrel{i_y}{\leftarrow}&
    y
    \\
    & {}_{\mathrlap{f}}\searrow & \downarrow^{\mathrlap{(f,g)}} & \swarrow_{\mathrlap{g}}
    \\
    && Q
  }
  \,.
$$

This morphism $(f,g)$ is called the __[[copairing]]__  of $f$ and $g$.  The morphisms $x\to x\coprod y$ and $y\to x\coprod y$ are called [[coprojections]] or sometimes "injections" or "inclusions", although in general they may not be [[monomorphisms]].


**Notation.** The coproduct is also denoted $a+b$ or $a\amalg b$, especially when it is [[disjoint coproduct|disjoint]] (or $a \sqcup b$ if your fonts don\'t include '$\amalg$'). The copairing is also denoted $[f,g]$ or (when possible) given vertically: $\left\{{f \atop g}\right\}$.


A coproduct is thus the [[colimit]] over the [[diagram]] that consists of just two objects. 

More generally, for $S$ any [[set]] and $F : S \to C$ a collection of objects in $C$ indexed by  $S$, their **coproduct** is an object

$$
  \coprod_{s \in S} F(s)
$$

equipped with maps

$$
  F(s)  \to \coprod_{s \in S} F(s)
$$

such that this is [[universal property|universal]] among all objects with maps from the $F(s)$. 

## Examples

*  In [[Set]], the coproduct of a [[family of sets]] $(C_i)_{i\in I}$ is the [[disjoint union]] $\coprod_{i\in I} C_i$ of sets.

   This makes the coproduct a [[categorification]] of the operation of addition of [[natural number]]s and more generally of [[cardinal]] numbers: for $S,T \in FinSet$ two finite sets and $|-| : FinSet \to \mathbb{N}$ the [[cardinality]] operation, we have

   $$
     |S \coprod T| = |S| + |T|
     \,.
   $$

*  In [[Top]], the coproduct of a family of spaces $(C_i)_{i\in I}$ is the space whose set of points is $\coprod_{i\in I} C_i$ and whose open subspaces are of the form $\coprod_{i\in I} U_i$ (the internal [[disjoint union]]) where each $U_i$ is an [[open subspace]] of $C_i$.  This is typical of [[topological concrete categories]].

*  In [[Grp]], the coproduct is the [[free product]], whose underlying set is *not* a disjoint union.  This is typical of [[algebraic category|algebraic categories]].

*  In [[Ab]], in [[Vect]], the coproduct is  the [[subobject]] of the [[product]] consisting of those tuples of elements for which only finitely many are not 0.

*  In [[Cat]], the coproduct of a family of categories $(C_i)_{i\in I}$ is the category with
   $$Obj(\coprod_{i\in I} C_i) = \coprod_{i\in I} Obj(C_i)$$
   and
   $$
     Hom_{\coprod_{i\in I} C_i}(x,y) = 
     \left\{
       \begin{aligned}
         Hom_{C_i}(x,y) & if x,y \in C_i
         \\
         \emptyset & otherwise
       \end{aligned}
     \right.
   $$ 

*  In [[Grpd]], the coproduct follows [[Cat]] rather than [[Grp]].  This is typical of [[oidifications]]: the coproduct becomes a disjoint union again.


## Properties

* A coproduct in $C$ is the same as a [[product]] in the [[opposite category]] $C^{op}$.

* When they exist, coproducts are unique up to unique canonical isomorphism, so we often say "[[generalized the|the]] coproduct."

* A coproduct indexed by the [[empty set]] is an [[initial object]] in $C$.

## Related concepts

* [[sum type]]

* [[base change]]

  * [[dependent sum]], [[dependent product]]

  * [[dependent sum type]], [[dependent product type]]

## References

Textbook account:

* [[Francis Borceux]], Section 2.2 in Vol. 1: *Basic Category Theory* of: *[[Handbook of Categorical Algebra]]*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))



[[!redirects coproducts]]