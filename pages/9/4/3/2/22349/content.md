[[!redirects category of filters on sets]]
[[!redirects filter]]
[[!redirects filter]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# The category of filters
* table of contents
{: toc}

## Definition


_A [[filter]] $\mathfrak{F}$ on a set $X$_ is
 a set of of subsets of X which has the following properties: 

($F_I$) Every subset of X which contains a set of  $\mathfrak{F}$  belongs to  $\mathfrak{F}$. 

($F_{II}$) Every finite intersection of sets of  $\mathfrak{F}$ belongs to  $\mathfrak{F}$.
 
Subsets in $\mathfrak{F}$ are called _neighbourhoods_ or _$\mathfrak{F}$-big_.

A mapping of underlying sets of filters is _continuous_ iff 
the preimage of a neighbourhood is necessarily a neighbourhood.
Note that $\mathfrak{F}\cup \{\emptyset\}$ is a topology on $X$, 
but this notion of continuity is stronger: it means continuous with dense image.

Let &#x12CB; denote the category of filters and the continuous mappings of underlying sets.

## Idea

It is convenient to talk about _a filter on a set_
as _a filter structure on a set_
and think of it as _a space with a notion of smallness_, 
 in analogy to a topological structure on a set
and thinking of it as 
a (topological) space with a notion of nearness of points.


_A filter $\mathfrak{F}$ on a set $X$_ gives  a precise meaning 
to phrases ``a property $P(x)$ holds for all points small enough'' and 
``P holds for almost all elements of $X$'',
namely that  
$ \{ x : P(x) \} \in \mathfrak{F} $,
in the same way that the topology (topological structure) 
on a set gives 
a precise meaning to the phrase 
``a property $P(x)$ holds for all points sufficiently near a given point $x_0$'',
namely $\{ x : P(x) \} $ is a neighbourhood of $x_0$.

Thus, for example, in the neighbourhood filter of a point $x_0$ 
in a topological space, 
a point $x$ is small iff $x$ is near $x_0$: 
we think of $x$ near $x_0$ as an approximation to $x_0$
up to a small error. 

A number of elementary notions can be formulated using the [[situs|category of simplicial objects of the category of filters]]. 



## Application to analysis and topology


In a [[topological space]] $X$, a filter $\mathfrak{F}$ on $X$ __[[convergence|converges]]__ to a point $x$ of $X$ if every [[neighbourhood]] of $x$ belongs to $\mathfrak{F}$, i.e. the map from $\mathfrak{F}$ to the neighbourhood filter of $x$ is continuous.  The filter on the empty set is the initial object; the proper filter on a single point is the terminal object. 

The concepts of continuous function and uniformly continuous function may be defined quite nicely in terms of the continuity of maps of filters. 
A map of topological spaces is continuous iff it induces continuous maps of neighbourhood filters. A map of uniform spaces is continuous iff it induces a continuous map of the uniform structures (filters on $M\times M$). 

In a [[metric space]] $M$, a filter $\mathfrak{F}$ on $M$ is __Cauchy__ if it has elements of arbitrarily small diameter, i.e. the map $\mathfrak{F}\times \mathfrak{F}\to S\times S$ is continuous with respect to the uniformity (filter) on $S\times S$.  Then a [[sequence]] is a [[Cauchy sequence]] iff its eventuality filter is Cauchy, i.e. it induces a continuous map of certain filters.  This gives a diagram chasing meaning to the concept of completion of a metric space.

