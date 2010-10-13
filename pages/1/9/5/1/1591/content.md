
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


# Discrete spaces
* table of contents
{: toc}


## Idea

A __discrete space__ is, in general, an object of a [[concrete category]] $Sp$ of spaces that is [[free functor|free]] on its underlying set.  Every [[topological concrete category]] has discrete spaces; so do many other categories, such as [[Diff]] and [[Hausdorff space|Haus Top]].  Non-concrete categories of spaces, such as [[Loc]], usually also have discrete spaces; the concept makes sense as long as there is a given [[forgetful functor]] from $Sp$ to [[Set]].

The dual notion is that of a [[codiscrete space]].

## Definition

We want the functor
$$ Set \stackrel{F}\to Sp \stackrel{U}\to Set $$
to be ([[natural isomorphism|naturally isomorphic]] to) the [[identity functor]] on [[Set]], where $F: Set \to Sp$ is [[adjoint functor|left adjoint]] to the [[forgetful functor]] $U: Sp \to Set$.  (This is true, for example, if $Sp$ is [[Top]], [[Diff]], [[Loc]], etc.)

Assuming that $U$ is [[faithful functor|faithful]] (as it should be when $Sp$ is a concrete category), we can characterise a discrete space $X$ as one such that every function from $X$ to $Y$ (for $Y$ any space) is a morphism of spaces.  (More precisely, this means that every function from $U(X)$ to $U(Y)$ is the image under $U$ of a morphism from $X$ to $Y$.)

A [[topological space]] is discrete in the sense above only if the [[diagonal map]] $X \times X \to X$ is [[open map|open]]; the converse holds if $X$ satisfies the $T_0$ [[separation axiom]].  In [[locale]] theory, the condition that a locale is discrete may be split into two parts: that $X \times X \to X$ is open and that $X \to 1$ is open.  A locale that satisfies the latter condition is called [[overt locale|overt]]; note that every locale is $T_0$ while every topological space is overt.  In [[Abstract Stone Duality]], a space is called __discrete__ if $X \times X \to X$ is open, which corresponds to the existence of an [[equality]] relation on $X$; discrete spaces as described above correspond to discrete *overt* spaces in ASD.


## Examples

### Discrete topological spaces

The best known example is a discrete [[topological space]], that is one, $X$, in which all subsets of $X$ are [[open subset|open]] in the topology. This is the [[discrete topology]] on $X$.  

This same space serves as a discrete object in many subcategories and supercategories of $Top$, from [[convergence space]]s (where the only proper filter that converges to a point is the free ultrafilter at that point) to (say) paracompact Hausdorff spaces (because a discrete topological space has those properties).  It is also [[sober space|sober]] and thus serves as a discrete [[locale]], whose corresponding [[frame]] is the [[power set]] of $X$; see [[CABA]].

A discrete [[uniform space]] $X$ has all [[reflexive relations]] as [[entourages]], or equivalently all [[covers]] as [[uniform cover]]s.  It is the only uniformity (on a given set) whose underlying topology is discrete.

### Discrete extended metric spaces

Strictly speaking, there is no discrete [[metric space]] on any set with more than one element, because the forgetful functor has no left adjoint.  However, there is a discrete *extended* metric space, given by $d(x,y) = \infty$ whenever $x \ne y$.  More usually, the term 'discrete metric' is used when $d(x,y) = 1$ for $x \ne y$, which is discrete in the category of metric spaces of diameter at most $1$.  (Comparing the [[adjoint functor theorem]], the problem with $Met$ is that it generally lacks infinitary [[product]]s; in contrast, $Ext Met$ and $Met_1$ are [[complete category|complete]].)

### Discrete cohesive spaces

A general axiomatization of the notion of space is as an object in a [[cohesive topos]]. This comes by definition with an underlying-set-functor (or similar) and a [[left adjoint]] that produces discrete cohesive structure. See there for details.

[[!redirects discrete space]]
[[!redirects discrete spaces]]

[[!redirects discrete topology]]
[[!redirects discrete topologies]]
[[!redirects discrete topological structure]]
[[!redirects discrete topological structures]]
[[!redirects discrete topological space]]
[[!redirects discrete topological spaces]]

[[!redirects discrete uniformity]]
[[!redirects discrete uniformities]]
[[!redirects discrete uniform structure]]
[[!redirects discrete uniform structures]]
[[!redirects discrete uniform space]]
[[!redirects discrete uniform spaces]]

[[!redirects discrete metric]]
[[!redirects discrete metrics]]
[[!redirects discrete metric space]]
[[!redirects discrete metric spaces]]
[[!redirects discrete extended metric]]
[[!redirects discrete extended metrics]]
[[!redirects discrete extended metric space]]
[[!redirects discrete extended metric spaces]]

[[!redirects discrete locale]]
[[!redirects discrete locales]]
