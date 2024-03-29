
# Indiscrete categories
* table of contents
{: toc}

## Definitions

An **indiscrete category** is a [[category]] $C$ in which there is a unique [[morphism]] from each [[object]] $x$ to each object $y$:
$$
  \forall x,y \in Obj(C) : C(x,y) = *
  \,,
$$
where $*$ is the [[point]].


The terms **chaotic category**, and **codiscrete category** are also used.

## Properties

This means that

* an indiscrete category is in fact a [[groupoid]], in fact a [[codiscrete groupoid]];
* any [[inhabited set|inhabited]] indiscrete category is [[equivalence of categories|equivalent]] to the [[terminal category]].

Therefore, up to [[equivalence of categories|equivalence]], an indiscrete category is simply a [[truth value]].

The functor $Ind\colon Set \to Str Cat$ sending a [[set]] $X$ to the indiscrete category with $X$ as its set of objects (viewed as a [[strict category]], that is up to [[isomorphism of categories|isomorphism]]) is [[adjoint functor|right adjoint]] to the [[forgetful functor]] $Ob\colon Str Cat \to Set$ sending a category to its set of objects.  (The [[adjoint functor|left adjoint]] $Disc$ to this forgetful functor sends a set $X$ to the [[discrete category]] on $X$.)

Of course, we can compose $Ind$ (or $Disc$) with the forgetful functor from $Str Cat$ to the [[2-category]] $Cat$, in which we consider categories up to [[equivalence of categories|equivalence]], as usual.  Then the composite
$$ Set \overset{Ind}\to Str Cat \to Cat $$
is [[natural equivalence|naturally equivalent]] to the composite
$$ Set \overset{Inh}\to TV \overset{Subs}\to Set \overset{Disc}\to Str Cat \to Cat ,$$
where $TV$ is the set (viewed a $2$-category) of [[truth values]], $Inh$ takes a set to the truth value of the statement that it is [[inhabited set|inhabited]], $Pt$ takes a truth value to a [[subsingleton]] ([[left adjoint]] to $Inh$), and $Disc$ is as above.

##Related concepts

* [[codiscrete groupoid]]

* [[category enriched in a bicategory]]

[[!redirects indiscrete category]]
[[!redirects indiscrete categories]]
[[!redirects chaotic category]]
[[!redirects chaotic categories]]
