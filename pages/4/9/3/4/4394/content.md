
# Bitopological space
* table of contents
{: toc}

## Definitions

Recall that a [[topological space]] is a [[set]] $X$ equipped with a [[topological structure]] $\mathcal{T}$.  Well, a __bitopological space__ is simply a set equipped with *two* topological structures $(X, \mathcal{T}, \mathcal{T}^*)$.  Unlike with [[bialgebras]], no compatibility condition is required between these structures.

A __bicontinous map__ is a [[function]] between bitopological spaces that is [[continuous map|continuous]] with respect to each topological structure.

Bitopological spaces and bicontinuous maps form a [[category]] $BiTop$.

## Compatibility conditions for topologies


+-- {: .num_defn}

###### Definition
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}$ is __regular with respect to__ $\mathcal{T}^*$ if  one of the following two equivalent conditions holds

1. There is a $\mathcal{T}$-[[neighborhood base]] consisting  of $\mathcal{T}^*$-closed sets; 
1. for all $x\in X$ and all $\mathcal{T}$-opens containing $x$ there is a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood $V$ such that $ V \subset U$.

A bitopological space $(X, \mathcal{T}, \mathcal{T}^*)$ is called __pairwise regular__ if $\mathcal{T}$ is regular with respect to $\mathcal{T}^*$ and wise versa.
=--

Let $Cl$ denote the [[closure operator]] with respect to $\mathcal{T}$ and let $Cl^*$ denote the closure operator with respect to $\mathcal{T}^*$.

+-- {: .num_defn}

###### Definition
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}^*$ is __coupled to__ $\mathcal{T}^*$ if one of the following two equivalent conditions holds

1. $Cl^*(O) \subset Cl(O)$ for each $\mathcal{T}^*$-open $O$; 
1. for all $x\in X$ and all $\mathcal{T}$-neighborhoods $U$ of $x$ the closure $Cl^*(U)$ is a $\mathcal{T}$-neighborhood.
=--

## Remarks

It is interesting and perhaps surprising that many advanced topological notions can be described using bitopological spaces, even when you would not na&#239;vely think that there are two topologies around.  (At least, that\'s my vague memory of what they were good for.  I think that this was in some article by Isbell.)

## Related Articles

* [[cotopology]]
* [[topologically complete space]]


## References

* [Wikipedia entry](http://en.wikipedia.org/wiki/Bitopological_space)

* [[Jiri Adamek]], [[Horst Herrlich]], and [[George Strecker]], _Abstract and Concrete Categories: The Joy of Cats_ , Dover New York 2009. ([pdf](http://katmat.math.uni-bremen.de/acc/acc.pdf)) pp.59-60,278

* B. Dvalishvili, _Bitopological Spaces: Theory, Relations with Generalized Algebraic Structures and Applications_ , Elsevier Amsterdam 2005.

* [[Peter Johnstone]], _Collapsed Toposes as Bitopological Spaces_ , pp.19-35 in _Categorical Topology_ , World Scientific Singapore 1989.

* O. K. Klinke, A. Jung, A. Moshier, _A bitopological point-free approach to compactications_ (2011). ([preprint](http://www.cs.bham.ac.uk/~axj/pub/papers/compactifications.pdf))

* R. Kopperman, _Asymmetry and duality in topology_ , Topology Appl. **66** no.1 (1995) pp.1-39.

The notions of respective regularity, being coupled, etc. were introduced in

* J. D. Weston, _On the comparison of topologies_ 1956, Journal of the London Mathematical Society, vol. s1-32 no. 3, pp. 342-354,

* J. C. Kelly, _Bitopological spaces_ , Proc. London Math. Soc. **13** no.3 (1963) pp.71-89.

[[!redirects bitopological space]]
[[!redirects bitopological spaces]]
[[!redirects Bitop]]
[[!redirects BiTop]]
[[!redirects Bi Top]]
