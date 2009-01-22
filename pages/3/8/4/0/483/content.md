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


#Discussion#

The above defined directed _topological_ spaces. My impression is that [[Eric Forgy|Eric]] was interested in more general concepts. But the above definition has a straightforward generalization away from topological spaces.  The general strategy is really: start with a category with [[interval object]] and consider then the category whose objects are pairs $(X, d X)$ for $X$ an object and $d X$ a subobject of $[I,X]$, and whose morpshism are morphisms $X \to Y$ that take $d X$ to $d Y$.

For instance, let's define **directed sets**: make the ordinary category [[Set]] a category with interval object by , say, taking the interval object to be the set $I := [n]$ of $n$ elements. A map from $I$ into any other set can be regarded as an $n$-step path in that set. Then pairs consisting of a set and a subset of all such maps model "directed sets".

_[[Eric Forgy|Eric]] says_: Yes, exactly :) That sounds like a good plan. By the way, what you say about $I := [n]$ reminds me a lot of simplicial sets.

_[[Eric Forgy|Eric]] says_: We have _directed spaces_ and we may soon have _directed sets_. This makes me wonder if we should have a **directed category** [[internal category|internal to]] another category? This way

* a directed space is a directed category in [[Top]]
* a directed set is a directed category in [[Set]]
* etc

Would that make sense?

[[Urs Schreiber|Urs]]: Let's see, before getting into this idea of realizing a directed space as a space internal to something else or the like,
I don't see what you want to mean by a "directed category". See, the point is that a category already _is_ supposed to be a combinatorial model for a directed space. Just as a groupoid is a combinaotrial model for an undirected space. This is the very motivation for defining directed spaces: to fill in the question marks in

* groupoid | space  || category | ?? .

This is why a directed space is defined such that its "thing of all paths in it" is not, in general, a [[fundamental groupoid]] but a [[fundamental category]].

Methinks that for the application which you have in mind you want to be studying [[poset]]s and these are special cases of categories and in particular naturally interpreted as combinatorial models for directed space, in exactly the way in which you are thinking of them as directed spaces! So 
it seems to me you don't actually need to be looking for what you seem to be looking for, since it is already quite easily there. But of course maybe I misunderstand what you are after.

_[[Eric Forgy|Eric]]_: I doubt that what I am looking for is new. If you could help put a name on it, that would be great. I'm not exactly sure what I mean by directed category either other than a "category with a direction" :|

[[Urs Schreiber|Urs]]: but a category _is_ directed! Recall that underlying every category is a [[directed graph]] (it is a directed graph equipped with a composition operation). So I am still puzzled by what you are looking for, because a "directed category" would have underlying it a "directed directed graph". What's that supposed to be? And why do you want it?

_[[Eric Forgy|Eric]]_: Sorry for being so dense. We can delete this once I get a clue. But for now, I'm still confused. Maybe what I wanted to say is more along the line (but probably still not correct)

"A directed space has a fundamental category"

"A directed set has a fundamental category"

"A directed object has a fundamental category"

Ack! *light bulb!* (those hurt sometimes)

I think that is probably precisely why you defined [[directed object]].

Could we say (and be correct!) that 

"a directed space is a directed object in Top"?

"a directed set is a directed object in Set"?

If so, I think I am making some progress.

[[Urs Schreiber|Urs]]: Yes, a directed space should be a directed object in the category of possibly directed topological spaces! (In [[Top]] itself there are no directed spaces. Every ordinary topological space is undirected). I think I listed that as a should-be example. To make it a proper example one will have to say a few more probabaly straightforward things about directed homotopies etc. But the idea is certainly this, yes, a directed space is a directed object in the category of possibly directed spaces.

And as for categories: the generic category is a directed object in the category of categories. Unless it happens to be a groupoid. In which case it is an undirected object there.

(All this with respect to the "canonical" choice of [[interval object]]. The notion of directedness depends on which interval object you choose to test with. For instance the point itself satisfies the axioms of an interval object. But using it of course everything will look undirected.)
