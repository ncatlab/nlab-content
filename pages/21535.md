> For the [[generalized smooth space]] of the same name see at [[Smith space (generalized smooth space)]].

#Contents#
* table of contents
{:toc}

## Idea



## Definition

In the context of [[functional analysis]], a **Smith space** is a [[complete topological vector space|complete]] [[locally convex topological vector space|locally convex]] topological $\mathbb{R}$-vector space $V$ that admits a [[compact object|compact]] [[absolutely convex]] subset $K \subset V$ such  that $V = \bigcup_{c \gt 0} c K$ with the induced [[compactly generated topological space|compactly generated topology]] on $V$.

## Examples

* For a compact absolutely convex set, $S$, the space of [[measures]], $M(S)$, with the compactly generated topology is a Smith space.

## Properties

The category of Smith spaces is [[equivalence of categories|equivalent]] to the opposite of the category of [[Banach spaces]]. More precisely, if $V$ is a Banach space, then $Hom(V,\mathbb{R})$ is a Smith space; and if $W$ is a Smith space, then $Hom(W,\mathbb{R})$ is a Banach space, where in both cases we endow the dual space with the compact-open topology. The corresponding biduality maps are isomorphisms.

Smith spaces are more natural than Banach spaces from the perspective of [[condensed mathematics]] because they are controlled by a nice compact subset instead of a nice open subset (the unit ball) as in the Banach setting. Also, Banach spaces are [[filtered colimits]] of Smith spaces while Smith spaces are [[filtered limits]] of Banach spaces. Filtered colimits have better algebraic and homological properties.

Smith spaces embed fully faithfully in condensed R-vector spaces, but Smith spaces do not form an [[abelian category]]. There is an induced functor from Waelbrock’s enlarged (abelian) category of quotients of Smith spaces, but that functor is not fully faithful.

Smith spaces are the same as Waelbrock dual spaces.

A Banach space is a Smith space if and only if it is finite-dimensional.

##References

The original treatment is in

* [[Marianne Smith]], _The Pontrjagin duality theorem in linear spaces_, Annals of Mathematics. 56(2): 248–253, ([doi:10.2307/1969798](https://doi.org/10.2307%2F1969798)).

In the context of [[condensed mathematics]], see

* [[Peter Scholze]], _Lectures on Analytic Geometry_, ([pdf](https://www.math.uni-bonn.de/people/scholze/Analytic.pdf))