#Idea#

A _directed space_ is a topological space in which not every path is traversable in both directions. 
Directed spaces are supposed to be to general $\infty$-[[infinity-category|categories]] as ordinary [[topological space|topological spaces]] are to $\infty$-[[infinity-groupoid|groupoids]] via the [[homotopy hypothesis]].

Directed spaces are studied in [[directed homotopy theory]], a relatively young topic. In generalization of how a [[topological space]] has a [[fundamental groupoid]], a [[directed space]] has a [[fundamental category]].


#Definition#

A **directed topological space** or d-space is pair $(X, d X)$ consisting of a [[topological space]] $X$ and a subset $d X \subset C([0,1],X)$ of continuous maps from the interval into $X$ -- called _directed paths_ or d-paths -- satisfying the following conditions:

1. (constant paths) every constant map $I\to X$ is directed,

2. (reparametrisation) $dX$ is closed under composition with increasing maps $I\to I$,

3. (concatenation) $dX$ is closed under path-concatenation: if the d-paths $a, b$ are consecutive in $X$ $(a(1) = b(0))$, then their ordinary concatenation $a+b$ is also a d-path

$$(a+b)(t) = a(2t),\,\text{if}\, 0\le t\le \frac{1}{2},$$

$$(a+b)(t) = b(2t),\,\text{if}\, \frac{1}{2}\le t\le 1.$$

A **morphism of directed topological spaces**  $f : (X, d X)\to (Y , d Y)$ is a morphism of topological spaces $f: X \to Y$ which preserves directed paths in that for every $\gamma: I \to X$ in $d X$ the path $f_* \gamma : I \stackrel{\gamma}{\to} X \stackrel{f}{\to} Y$ is in $d Y$.

#Examples#

* The _standard directed interval_ is $I_d = ([0,1], d I)$ with $d I $ the set of all _monotonic_ continuous maps $[0,1] \to [0,1]$.


#Remarks#

* If we can equip directed spaces with an internal hom, then a directed space with at least one directed path should be a [[directed object]] in the category of directed spaces, with respect to the standard directed interval as the [[interval object]], while an ordinary topological spaces regarded as a directed space should be an undirected object.

But for that to work we need the structure of a directed topological space on $C(I_d,(X,d X))$. This requires that $X$ has _directed homotopies_! Does Grandis discuss higher directed paths, too?


#References#

The above definition is from

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))



+--{.query}

The above defined directed _topological_ spaces. My impression is that [[Eric Forgy|Eric]] was interested in more general concepts. But the above definition has a straightforward generalization away from topological spaces.  The general strategy is really: start with a category with [[interval object]] and consider then the category whose objects are pairs $(X, d X)$ for $X$ an object and $d X$ a subobject of $[I,X]$, and whose morpshism are morphisms $X \to Y$ that take $d X$ to $d Y$.

For instance, let's define **directed sets**: make the ordinary category [[Set]] a category with interval object by , say, taking the interval object to be the set $I := [n]$ of $n$ elements. A map from $I$ into any other set can be regarded as an $n$-step path in that set. Then pairs consisting of a set and a subset of all such maps model "directed sets".

_[[Eric Forgy|Eric]] says_: Yes, exactly :) That sounds like a good plan. By the way, what you say about $I := [n]$ reminds me a lot of simplicial sets.

=--