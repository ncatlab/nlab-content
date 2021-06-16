
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


A [[topological space]] is called _fully normal_ if every [[open cover]] $\{U_i \subset X\}_{i \in I}$ is a __normal cover__, i.e., has a [[refinement]] by an open cover $\{V_j \subset X\}_{j \in J}$ such that every _star_ (eq:Star) in the latter cover is contained in a patch of the former.
Furthermore, the resulting cover $\{V_j\}_{j\in J}$ also admits such a star
refinement, and this process can be continued indefinitely.

Here, for $x \in X$ a point, the **star** of $x$ is the [[union]] of the patches that contain $x$:

\[
  \label{Star}
  star(x,\mathcal{V})
  \;\coloneqq\;
  \left\{
     V_j \in \mathcal{V} \;\vert\; x \in V_J 
  \right\}
\]

Normal covers are also known as [[numerable covers]],
since they are precisely the [[open covers]] that admit
a subordinate [[partition of unity]].

## In pointfree topology

Any [[completely regular locale]] has a largest [[uniformity]],
the [[fine uniformity]], which consists of all normal covers.

If a [[completely regular locale]] admits a [[complete uniformity]],
then the [[fine uniformity]] is complete.

A [[locale]] is [[paracompact]] if and only if it admits a [[complete uniformity]].
In this case, we can take the [[fine uniformity]].


## Examples

* [[metric spaces are fully normal]]

## Properties

* [[fully normal spaces are equivalently paracompact]]

## Related conceps

* [[numerable cover]]

* [[paracompact space]]

* [[paracompact locale]]

* [[separation axiom]]

[[!redirects fully normal topological spaces]]

[[!redirects fully normal space]]
[[!redirects fully normal spaces]]

