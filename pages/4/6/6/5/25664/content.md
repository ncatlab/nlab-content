# Contents
* 
{: toc}

## Idea

A _pseudoorientation_ of a [[submanifold]] $U \subset X$ is an orientation of how the ambient [[manifold]] $X$ lies around the submanifold.

This contrasts with an [[orientation]] of the submanifold itself: neither a pseudoorientation nor an orientation for a submanifold necessarily provides the other, unless one has an orientation for the ambient manifold.

An orientation of $U$ may be visualized with a set of arrows lying within $U$. A pseudoorientation is properly visualized instead with a set of arrows passing through $U$, or circulating around it.

A pseudoorientation is sometimes also called a __transverse orientation__, and the term is also spelled __pseudo-orientation__ or __pseudorientation__.


## Definition

\begin{definition}
For a [[submanifold]] $U$ of a [[manifold]] $X$, a __pseudoorientation__ of $U$ is a map that, for each point $a$ on $U$, takes a local [[orientation]] of $X$ at $a$ to a local orientation of $U$ at $a$, continuously in $a$ and taking opposite orientations to opposite orientations.
\end{definition}

An equivalent, more explicitly geometrical definition justifies the synonym _transverse orientation_:

\begin{definition}
For a [[submanifold]] $U$ of a [[manifold]] $X$, a __pseudoorientation__ of $U$ is an [[orientation]] of the [[vector bundle]] $T_U(X) / T_U(U)$, a bundle on $U$ whose [[fiber]] at each $x \in U$ is the [[quotient vector space|quotient]] $T_x(X) / T_x(U)$ of the [[tangent space]] to $X$ at $x$ by the tangent space to $U$ at $x$.
\end{definition}


## Properties

### Relation to orientations

When one has an [[orientation]] of the containing manifold $X$, that gives a correspondence between orientations and pseudoorientations for any submanifold $U$. As a result, many treatments conflate orientations with pseudoorientations.


### Integration

A pseudoorientation is precisely the added structure one needs in order to [[integration of differential forms|integrate]] over $U$ a $k$-[[pseudoform]] on $X$. This is much like how if one has instead an (untwisted) $k$-[[differential form|form]] on $X$ and wants to integrate it over $U$, one needs an orientation of $U$. For details, see [[integration of differential forms]].


## Examples

### Canonical pseudoorientation for a top-dimension submanifold

When $k = n$, a local [[orientation]] of $X$ is the same thing as a local orientation of $U$. This correspondence makes a canonical pseudoorientation for $U$.

This canonical pseudoorientation is what makes the integration of $n$-[[pseudoforms]] the most fundamental kind of integration on a [[manifold]], as discussed at [[integration of differential forms]].


## Related concepts

* An [[absolute differential form]] can be integrated on an entirely unoriented [[submanifold]], with neither an [[orientation]] nor a pseudoorientation.


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
