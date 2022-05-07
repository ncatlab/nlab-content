
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

What is called _the line with two origins_ is the [[topological space]] which results by "gluing" a copy of the [[real line]] identically to itself, except at the origin. This is a basic example of a [[non-Hausdorff topological space]] (even a non-Hausdorff [[smooth manifold]]) and of the fact that [[quotient topological spaces]] of [[Hausdorff topological spaces]] need not be Hausdorff themselves.


## Definition

Consider the [[disjoint union]] $\mathbb{R} \sqcup \mathbb{R}$ of two copies of the [[real line]] $\mathbb{R}$ regarded with its [[metric topology]]. Moreover, consider the [[equivalence relation]] on the underlying set which identifies every
point $x_i$ in the $i$th copy of $\mathbb{R}$ ($i \in \{0,1\}$) with the corresponding point in the other, the $(1-i)$th copy, except when $x = 0$:

$$
  \left(
    x_i \sim y_j
  \right)
   \;\Leftrightarrow\;
  \Big(
    \left(
      x = y
    \right)
    \,\text{and}\,
    \big(
      (
        x \neq 0
      )
      \,\text{or}\,
      (
        i = j
      )
    \big)
  \Big)
  \,.
$$



The [[quotient topological space]] 

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/LineWithTwoOrigins.png" width="300">
</div>

$$
  \left(
    \mathbb{R} \sqcup \mathbb{R}
  \right)/\sim
$$

by this equivalence relation is called the **line with two origins**.


## Properties

The line with two origins is a [[non-Hausdorff topological space]]:

Because by definition of the [[quotient topological space|quotient space topology]], the [[open neighbourhoods]] of $0_i \in   \left( \mathbb{R} \sqcup \mathbb{R} \right)/\sim$ are precisely those that contain subsets of the form

$$
 (-\epsilon, \epsilon)_i
  \;\coloneqq\; 
 (-\epsilon,0) \cup \{0_i\} \cup (0,\epsilon)
 \,.
$$

But this means that the "two origins" $0_0$ and $0_1$ may not be [separated by neighbourhoods](separation+axioms#SeparatedByNeighbourhoods), since the intersection of 
$(-\epsilon, \epsilon)_0$ with $(-\epsilon, \epsilon)_1$ is always non-empty:

$$
  (-\epsilon, \epsilon)_0
   \cap
  (-\epsilon, \epsilon)_1
  \;=\;
  (-\epsilon, 0) \cup (0, \epsilon)
  \,.
$$



The [Hausdorff reflection](Hausdorff+space#HausdorffReflection)

$$
  H \;\colon\; Top \longrightarrow Top_{Haus}
$$

of the line with two origins is the [[real line]] itself:

$$
  H\left(
    \left(
      \mathbb{R} \sqcup \mathbb{R}
    \right)/\sim
  \right)
  \;\simeq\;
  \mathbb{R}
$$

However, the line with two origins is [[T1]] and [[sober space|sober]].

It is also a [[topological manifold]], even a [[smooth manifold]], except that one often requires such to be Hausdorff to rule out examples such as this.  In a similar vein, it is [[locally compact space|locally compact]] (and a [[compact space|compact]] version can be made by starting with $[{-1,1}]$ instead of $\mathbb{R}$), [[paracompact space|paracompact]], and so forth.


## Related concepts

* [[long line]]


## References

* Wikipedia, _[Line with two origins](https://topospaces.subwiki.org/wiki/Line_with_two_origins)_


[[!redirects line with two origins]]
[[!redirects lines with two origins]]
[[!redirects lines with two origins each]]
[[!redirects line with double origin]]
[[!redirects lines with double origin]]
[[!redirects lines with double origins]]
[[!redirects line with doubled origin]]
[[!redirects lines with doubled origin]]
[[!redirects lines with doubled origins]]
[[!redirects line with doubled point]]
[[!redirects lines with doubled point]]
[[!redirects lines with doubled points]]
