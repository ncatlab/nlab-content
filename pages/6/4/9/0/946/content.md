The __specialisation topology__, also called the __Alexandroff topology__, is a way of turning any [[preorder]]ed set $P$ into a [[topological space]] (with the same underlying set).

A subset $A$ of $P$ is declared __open__ if it is upwards-closed.  That is, if $x \leq y$ and $x \in A$, then $y \in A$.  One may also use the convention that the open sets are the downwards-closed subsets; this is the specialisation topology on the [[opposite category|opposite]] $P^\op$.

Compare the [[Scott topology]], which is coarser.

# Examples

* [[Sierpinski space]] is the set of [[truth value]]s with the specialisation topology.

# Properties

$P$ is a [[partial order|poset]] if and only if its specialisation topology is $T_0$.

A function between preorders is order-preserving if and only if it is continuous with respect to the specialisation topology.  Thus, the specialization topology embeds the category $\Pros$ of preordered sets [[full subcategory|fully-faithfully]] in the category $\Top$ of topological spaces.  Its essential image can be characterized as the category of [[Alexandroff space]]s (spaces where an arbitrary intersection of open sets is open).  The corresponding preorder can be recovered from an Alexandroff space as its [[specialization order]].

If we restrict to a [[finite set|finite]] underlying set, then the categories $\Fin\Pros$ and $\Fin\Top$ of finite prosets and finite topological spaces are [[equivalence of categories|equivalent]] in this way.


[[!redirects specialisation topology]]
[[!redirects Alexandrov topology]]
[[!redirects Alexandroff topology]]
[[!redirects Alexandrov space]]
[[!redirects Alexandroff space]]
