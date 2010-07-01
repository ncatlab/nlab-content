# Specialisation topology
* table of contents
{: toc}


## Idea

The __specialisation topology__, also called the __Alexandroff topology__, is a way of turning any [[preordered set]] into a [[topological space]] (with the same [[underlying set]]).

Compare the [[Scott topology]], which is coarser.


## Definition

Let $P$ be a [[preordered set]].

A subset $A$ of $P$ is declared __open__ if it is upwards-closed.  That is, if $x \leq y$ and $x \in A$, then $y \in A$.  One may also use the convention that the open sets are the downwards-closed subsets; this is the specialisation topology on the [[opposite category|opposite]] $P^\op$.


## Examples

* [[Sierpinski space]] is the poset of [[truth values]] with the specialisation topology.


## Properties

$P$ is a [[partial order|poset]] if and only if its specialisation topology is $T_0$.

A function between preorders is order-preserving if and only if it is continuous with respect to the specialisation topology.  Thus, the specialization topology embeds the category $\Pros$ of preordered sets [[full subcategory|fully-faithfully]] in the category $\Top$ of topological spaces.  Its essential image can be characterized as the category of __Alexandroff spaces__ (spaces where an arbitrary [[intersection]] of [[open subsets]] is open).  The corresponding preorder can be recovered from an Alexandroff space as its [[specialization order]].

If we restrict to a [[finite set|finite]] underlying set, then the categories $\Fin\Pros$ and $\Fin\Top$ of finite prosets and finite topological spaces are [[equivalence of categories|equivalent]] in this way.


[[!redirects specialization topology]]
[[!redirects specialisation topology]]
[[!redirects Alexandrov topology]]
[[!redirects Alexandroff topology]]
[[!redirects Alexandrov space]]
[[!redirects Alexandrov spaces]]
[[!redirects Alexandroff space]]
[[!redirects Alexandroff spaces]]
