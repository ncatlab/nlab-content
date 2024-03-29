
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be an [[(∞,1)-category]] and $X \in C$ an [[object]]. 

+-- {: .num_def}
###### Definition

A **subobject** of $X$ is a [[1-monomorphism]] $K \hookrightarrow X$ into $X$.

The [[(∞,1)-category]] $Sub(X)$ of **subobjects** of $X$ is the $(-1)$-[[truncated object in an (∞,1)-category|truncation]] of the [[slice-(∞,1)-category]] of $C$ over $X$

$$
  Sub(X) := \tau_{-1} C_{/X}
  \,.
$$

=--

This is the category whose objects are [[monomorphism in an (∞,1)-category|monomorphisms]] $U \hookrightarrow X$ in $C$ and whose morphisms are [[2-morphism]]s 

$$
  \array{
     U_1 &&\to&& U_2
     \\
     & \searrow &\swArrow& \swarrow
     \\
     && X
  }
$$

in $C$.

## Properties

+-- {: .num_prop}
###### Proposition

$Sub(X)$ is a [[(0,1)-category]] (a [[poset]]).

=--

This appears for instance in ([Lurie, section 6.2](#Lurie)).

+-- {: .num_prop}
###### Proposition

If $C$ is a [[locally presentable (∞,1)-category]] then $Sub(X)$ is a [[small category]].

=--

## Related concepts

* [[subobject]]

* **subobject in an $(\infty,1)$-category**

* [[n-image]], [[n-truncated object in an (∞,1)-category]]

## References

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
  {#Lurie}


[[!redirects subobject in an (∞,1)-category]]

[[!redirects subobjects in an (∞,1)-category]]
[[!redirects subobjects in an (infinity,1)-category]]

