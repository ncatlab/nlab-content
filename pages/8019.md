
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### (0,1)-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Ordered groups
* table of contents
{: toc}

## Idea

An ordered group is both a [[poset]] and a [[group]] in a compatible way.  The concept applies directly to other constructs with group structure, such as ordered [[abelian groups]], ordered [[vector spaces]], etc.  However, for [[ordered ring]]s, [[ordered fields]], and so on, additional compatibility conditions are required.


## Definition

Let $G$ be a [[group]] (written additively but not necessarily [[abelian group|commutative]]), and let $\leq$ be a [[partial order]] on the [[underlying set]] of $G$.  Then $(G,\leq)$ is an __ordered group__ if this compatibility condition (*translation invariance*) holds:

*  If $a \leq b$, then $a + c \leq b + c$ and $c + a \leq c + b$.

More slickly, an ordered group is (up to [[equivalence of categories|equivalence]]) a [[thin category|thin]] [[groupal category]] (a groupal $(0,1)$-[[(0,1)-category|category]]). 

+-- {: .num_remark} 
###### Remark 
An ordered group is *not* the same thing as a [[group object]] in $Pos$. The trouble is that requiring the inversion map $x \mapsto x^{-1}$ to preserve order (i.e., to be monotone, not antitone) is much too restrictive. Rather, an ordered group is a [[monoid object]] in the [[cartesian monoidal category]] $Pos$ which has the [[stuff, structure, property|property]] that its underlying monoid in $Set$ is a group. 
=-- 

If $G$ is an [[abelian group]], then we have an __ordered abelian group__; in this case, only one direction of translation invariance needs to be checked.

It works just as well to talk of partially ordered [[monoids]], using the same condition of translation invariance.  Equivalently, an __ordered monoid__ is a thin [[monoidal category]], or a monoidal $(0,1)$-category.


## Properties

The order $\leq$ is determined entirely by the group $G$ and the [[positive cone]] $G^+$:
$$ G^+ \coloneqq \{x\colon G \;|\; 0 \leq x\} .$$
It\'s possible to *define* an ordered group in terms of the positive cone (by specifying precisely the conditions that the positive cone must satisfy); see [[positive cone]] for this.

However, this characterisation probably can\'t be made to work for ordered monoids (although I haven\'t checked for certain).


## Examples

The underlying additive group of any [[ordered field]] is an ordered group.

In particular, the underlying additive group of the field $\mathbb{R}$ of [[real numbers]] is an ordered group.

Although the field $\mathbb{C}$ of [[complex numbers]] is not an ordered field (since it is not *[[linear order|linearly]]* ordered), its underlying additive group is still an ordered group (where $a \leq b$ means that $b - a$ is a nonnegative real number).

Given a [[topological vector space]] $V$, we often consider its [[dual vector space]] $V^*$, consisting of the [[continuous map|continuous]] [[linear maps]] from $V$ to its [[base field]], which is usually either $\mathbb{R}$ or $\mathbb{C}$.  This inherits a partial order from the [[target]] field, and then the underlying additive group is an ordered group; in fact, we have an [[ordered algebra]].  (This is the main sort of example that I know of, but that probably just reflects my own limited knowledge.)

More generally, if $V$ is any [[set]], $G$ is any ordered group, and $F$ is any collection of [[functions]] from $V$ to $G$, as long as $F$ is a [[subgroup]] of the group of all functions from $V$ to $G$, then $F$ is an ordered group.

Non-abelian examples include free groups and torsion-free nilpotent groups.  The basics of the theory for both abelian and nonabelian ordered groups can be found in Birkhoff's Lattice Theory.

## Related concepts

* [[pseudolattice ordered abelian group]]

## References

*  English Wikipedia: [Partially ordered group](https://en.wikipedia.org/wiki/Partially_ordered_group).
   {#Wikipedia}


[[!redirects ordered group]]
[[!redirects ordered groups]]
[[!redirects partially ordered group]]
[[!redirects partially ordered groups]]
[[!redirects partially-ordered group]]
[[!redirects partially-ordered groups]]

[[!redirects ordered abelian group]]
[[!redirects ordered abelian groups]]
[[!redirects partially ordered abelian group]]
[[!redirects partially ordered abelian groups]]
[[!redirects partially-ordered abelian group]]
[[!redirects partially-ordered abelian groups]]

[[!redirects ordered monoid]]
[[!redirects ordered monoids]]
[[!redirects partially ordered monoid]]
[[!redirects partially ordered monoids]]
[[!redirects partially-ordered monoid]]
[[!redirects partially-ordered monoids]]
