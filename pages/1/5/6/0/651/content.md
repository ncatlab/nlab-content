{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

* [Idea](#idea)
* [Basics](#basics)
* [[examples of Frölicher spaces|Examples]]
* [[Frölicher spaces and Isbell envelopes|Relationship]] to [[Isbell envelope]]
* [[topological notions of Frölicher spaces|Topological Matters]]
* [[tangential notions of Frölicher spaces|Tangential Structures]]
* [References](#refs)


# Idea
{#idea}

A Fr&#246;licher space is one flavour of a [[generalized smooth space]]. 

Fr&#246;licher smooth spaces are determined by a rule for 

* how to map the real line smoothly into it, 

* and how to map out of the space smoothly to the real line.

In the general context of [[space and quantity]], Fr&#246;licher spaces take an intermediate symmetric position: they are both [[presheaf|presheaves]] as well as copresheaves on their test domain (which here is the full [[subcategory]] of manifolds on the real line) and both of these structures determine each other.

The general abstract idea behind this is described at [[Isbell envelope]].

+-- {: goal}
###### Goal
The intention for these pages is to develop the basic tools of differential topology for Fr&#246;licher spaces.
This means taking the basic pieces of "ordinary" differential topology and considering what they might look like for Fr&#246;licher spaces; including what looks the same and what looks different.

This project will both record existing structure and develop new ideas.
It is intentionally in the main area of the $n$-Lab to encourage contributions.
=--

# Basics
{#basics}

+-- {: mynumdef #FroelicherSpace}
###### Definition
A _Fr&#246;licher Space_ is a triple $(X,C_X,F_X)$ where

1. $X$ is a set;
2. $C_X$ is a set of _curves_ in $X$; that is, $C_X \subseteq Set(\mathbb{R},X)$;
3. $F_X$ is a set of _functionals_ on $X$; that is, $F_X \subseteq Set(X, \mathbb{R})$;

subject to the following saturation conditions

1. if $c : \mathbb{R} \to X$ is a set map with the property that $f c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $f \in F_X$ then $c \in C_X$, and
2. if $f : X \to \mathbb{R}$ is a set map with the property that $f c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $c \in C_X$ then $f \in F_X$.

A _morphism_ of Fr&#246;licher spaces, say $(X,C_X,F_X) \to (Y,C_Y,F_Y)$ is a set map $g : X \to Y$ satisfying the following (equivalent) conditions:

1. $g c \in C_Y$ for all $c \in C_X$,
2. $f g \in F_X$ for all $f \in F_Y$,
3. $f g c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $f \in F_Y$ and $c \in C_X$.
=--

Fr&#246;licher spaces and their morphisms form a category with an obvious faithful functor to the category of sets.
The properties of this category are as follows.

+-- {: .num_theorem #FroelicherCategory}
###### Theorem
The [[category]] of Fr&#246;licher spaces is [[complete category|complete]], [[cocomplete category|cocomplete]], and [[cartesian closed category|cartesian closed]].  It is [[topological category|topological]] over $Set$.  It is an [[concrete category|amnestic, transportable construct]].
=--

To its eternal shame, the category of Fr&#246;licher spaces is __not__ [[locally cartesian closed category|locally cartesian closed]].


# References
{#refs}

A detailed discussion of the category of Fr&#246;licher spaces and their relation to other notions of [[generalized smooth space]]s is given in

* Andrew Stacey, _Comparative Smootheology_ ([arXiv](http://arxiv.org/abs/0802.2225))

This also lists all the relevant further references. 

A discussion of [[Lie algebra]]s on Fr&#246;licher [[group]]s ([[group object]]s [[internalization|internal to]] the category of Fr&#246;licher spaces) is in

* Martin Laubinger, _A Lie algebra for Fr&#246;licher groups_ ([arXiv](http://arxiv.org/abs/0906.4486))


[[!redirects Frölicher space]]
[[!redirects Frölicher spaces]]
[[!redirects Frolicher space]]
[[!redirects Frolicher spaces]]
[[!redirects Froelicher space]]
[[!redirects Froelicher spaces]]
[[!redirects Frölicher Space]]
[[!redirects Frölicher Spaces]]
[[!redirects Frolicher Space]]
[[!redirects Frolicher Spaces]]
[[!redirects Froelicher Space]]
[[!redirects Froelicher Spaces]]
