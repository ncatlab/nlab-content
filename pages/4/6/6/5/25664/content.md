# Contents
* 
{: toc}

## Idea

For a $k$-[[submanifold]] $U$ of an $n$-[[manifold]] $X$, an _orientation_ of $U$ is an [[orientation]] of $U$ itself as a $k$-manifold. A _pseudoorientation_, by contrast, can be thought of as an orientation of the remaining $n-k$ dimensions of how $X$ sits around $U$.

An orientation of $U$ may be visualized with a set of arrows lying within $U$. A pseudoorientation is properly visualized instead with a set of arrows passing through $U$, or circulating around it.


## Definition

\begin{definition}
Given a $k$-[[submanifold]] $U$ of an $n$-[[manifold]] $X$, a __pseudoorientation__ of $U$ is a map that, for each point $a$ on $U$, takes a local [[orientation]] of $X$ at $a$ to a local orientation of $U$ at $a$, continuously in $a$ and taking opposite orientations to opposite orientations.
\end{definition}


## Properties

A pseudoorientation is precisely the added structure one needs in order to [[integration of differential forms|integrate]] over $U$ a $k$-[[pseudoform]] on $X$. This is much like how if one has instead an (untwisted) $k$-[[differential form|form]] on $X$ and wants to integrate it over $U$, one needs an orientation of $U$. For details, see [[integration of differential forms]].

When one has an [[orientation]] of the containing manifold $X$, that gives a correspondence between orientations and pseudoorientations for any submanifold $U$. As a result, many treatments conflate orientations with pseudoorientations.


## Examples

### Canonical pseudoorientation for a top-dimension submanifold

When $k = n$, a local [[orientation]] of $X$ is the same thing as a local orientation of $U$. This correspondence makes a canonical pseudoorientation for $U$.

This canonical pseudoorientation is what makes the integration of $n$-[[pseudoforms]] the most fundamental kind of integration on a [[manifold]], as discussed at [[integration of differential forms]].



## References

Many useful explanations by [[Toby Bartels]] and [[John Baez]] in [this long Usenet thread](https://groups.google.com/g/sci.physics.research/c/aiMUJrOjE8A/m/0361hct91VsJ).


[[!redirects pseudoorientations]]
[[!redirects pseudooriented]]

[[!redirects pseudo-orientation]]
[[!redirects pseudo-orientations]]
[[!redirects pseudo-oriented]]

[[!redirects pseudorientation]]
[[!redirects pseudorientations]]
[[!redirects pseudoriented]]
