# Discrete spaces
* table of contents
{: toc}


## Idea

A __discrete space__ is, in general, an object of a [[concrete category]] of spaces that is [[free functor|free]] on its underlying set.  Every [[topological concrete category]] has discrete spaces; so do many other categories, such as [[Diff]] and [[Hausdorff space|Haus Top]].


## Definition

For this to make sense, we want the functor
$$ Set \stackrel{F}\to Sp \stackrel{U}\to Set $$
to be ([[natural isomorphism|naturally isomorphic]] to) the [[identity functor]] on [[Set]], where $F: Set \to Sp$ is [[adjoint functor|left adjoint]] to the [[forgetful functor]] $U: Sp \to Set$.  (This is true, for example, if $Sp$ is [[Top]], [[Diff]], [[Loc]], etc, although $Loc$ is not quite a concrete category since the forgetful functor from [[locale]]s is not faithful.)

Assuming that $U$ is [[faithful functor|faithful]] (as it should be when $Sp$ is a concrete category), we can characterise a discrete space $X$ as one such that every function from $X$ to $Y$ (for $Y$ any space) is a morphism of spaces.  (More precisely, this means that every function from $U(X)$ to $U(Y)$ is the image under $U$ of a morphism from $X$ to $Y$.)

A [[topological space]] is discrete in the sense above only if the [[diagonal map]] $X \times X \to X$ is [[open map|open]]; the converse holds if $X$ satisfies the $T_0$ [[separation axiom]].  In [[locale]] theory, the condition that a locale is discrete may be split into two parts: that $X \times X \to X$ is open and that $X \to 1$ is open.  A locale that satisfies the latter condition is called [[overt locale|overt]]; note that every locale is $T_0$ while every topological space is overt.  In [[Abstract Stone Duality]], a space is called __discrete__ if $X \times X \to X$ is open, which corresponds to the existence of an [[equality]] relation on $X$; discrete spaces as described above correspond to discrete *overt* spaces in ASD.


## Examples

The best known example is a discrete [[topological space]], that is one, $X$, in which all subsets of $X$ are open in the topology.  This same space serves as a discrete object in many subcategories and supercategories of $Top$, from [[convergence space]]s (where the only proper filter that converges to a point is the free ultrafilter at that point) to (say) paracompact Hausdorff spaces (because a discrete topological space has those properties).  It is also [[sober space|sobre]] and thus serves as a discrete [[locale]], whose corresponding [[frame]] is the [[power set]] of $X$; see [[CABA]].

A discrete [[uniform space]] $X$ has all reflexive relation as entourages, or equivalently all covers as uniform covers.  It is the only uniformity (on a given set) whose underlying topology is discrete.

Strictly speaking, there is no discrete [[metric space]] on any set with more than one element, because the forgetful functor has no left adjoint.  However, there is a discrete *extended* metric space, given by $d(x,y) = \infty$ whenever $x \ne y$.  More usually, the term 'discrete metric' is used when $d(x,y) = 1$ for $x \ne y$, which is discrete in the category of metric spaces of diameter at most $1$.  (Comparing the [[adjoint functor theorem]], the problem with $Met$ is that it generally lacks infinitary [[product]]s; in contrast, $Ext Met$ and $Met_1$ are [[complete category|complete]].)


[[!redirects discrete space]]
[[!redirects discrete spaces]]
[[!redirects discrete topology]]