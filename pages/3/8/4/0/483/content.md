#Idea#

A _directed space_ is a [[topological space]] $X$ in which not every singular cell $\Delta^n \to X$ (for $\Delta^n$ the standard topological [[simplex]]) is supposed to be _traversable_ in all directions, in some sense: instead these $k$-dimensional _paths_ may have a _direction_ .

+--{.query}
[[Eric]]: What does it mean for a $k$-cell to be _traversable_?

[[Urs Schreiber]]: notice that this here is the "idea" section, not a formal definition. The idea is that everyone has an idea of what "to traverse" means and that this gives a good idea  for what the direction in "directed space" is about"!

[[Eric]]: Unfortunately, not <i>everyone</i> has an idea of what it means to traverse a $k$-cell or I wouldn't ask :)  These $k$-cells must themselves be directed with directed boundaries, right? I can imagine a directed 2-cell might have 2 directed 1-cells for a boundary, but even with this simple case, I am capable of confusing myself and it is not obvious what traversing the 2-cell should look like.

Is the boundary of a directed $k$-cell a directed $(k-1)$-chain?

=--

So far there exists a well-developed theory for a notion of _directed spaces_ $X$ where 1-dimensional paths given by maps $[0,1] \to X$ from the [[interval]] into the space are equipped with a direction. See in particular the book by by [[Marco Grandis]] on [[Directed Algebraic Topology]] listed below. 

Note that a directed space is generalised space; not every directed space is a space in the old sense, in accordance with the [[red herring principle]].

Directed spaces are studied in [[directed homotopy theory]], a relatively young topic. In generalization of how a [[topological space]] has a [[fundamental groupoid]], a [[directed space]] has a [[fundamental category]].

+--{.query}
[[Tim Porter|Tim]]: Originally **directed space** was used to indicate a space together with a closed direceted partial order on it. If the space is nice enough then there are directed paths which cannot be traversed in both directions. It may be worth giving that definition as then the difference between directed and undirected homotopies between paths could be addressed. 

The notions of [[fundamental category]] and many of the applications of these notions by workers in directed homotopy theory have used the above definition at some point and  Marco's *d-space* is motivated by that. 

[[Urs Schreiber|Urs]]: thanks, I wasn't aware of that. Could you provide a reference? Or the detailed original definition itself?

_Toby_: While we await Tim\'s reply, I expect that he simply means a [[pospace]] such that the partial order is a [[direction]].

By the way, if there are different notions of directed space, then we can move the one below to [[d-space]].
=--



## homotopy-theoretic perspective

From a [[homotopy theory|homotopy theoretic]] perspective one would wish that notions of directed spaces serve to generalize the [[homotopy hypothesis]] -- which identifies ordinary (undirected) [[topological space]]s with [[∞-groupoid]]s, i.e. with [[(∞,0)-category|(∞,0)-categories]] -- to a more general context where [[(∞,0)-category|(∞,0)-categories]] are generalized to [[(∞,n)-category|(∞,r)-categories]] with $r \gt 0$: 

an [[(∞,r)-category]] in this context should correspond to a **$r$-directed topological space** , one that comes equipped with a notion of orientation of its $k$-cells for $0 \leq k \leq r$.

If such a definition exists, it will probably need to use [[filtered topological space]]s instead of bare topological spaces.

Even in the absence of a homotopy-theoretic definition of $r$-directed space in this sense, from the perspective of [[homotopy theory]] one might take the standpoint of the [[homotopy hypothesis]] and _define_ a (nice) $r$-diected space to be an [[(∞,n)-category|(∞,r)-category]], just as it makes good sense and is nowadays common practice in [[algebraic topology]] to _define_ a nice [[topological space]] to be an [[∞-groupoid]].

See [[(n,r)-category]] for more on that.

+--{.query}

[[Urs Schreiber]]: I haven't looked at Marco Grandis' book yet: does it say anything about the homotopy hypothesis in the context of the definition of directed space used there?

=--



#Definition#

A **directed topological space** or **d-space** is pair $(X, d X)$ consisting of a [[topological space]] $X$ and a subset $d X \subset C([0,1],X)$ of continuous maps from the interval into $X$ -- called _directed paths_ or d-paths -- satisfying the following conditions:

1. (constant paths) every constant map $I\to X$ is directed,

2. (reparametrisation) $dX$ is closed under composition with increasing maps $I\to I$,

3. (concatenation) $dX$ is closed under path-concatenation: if the d-paths $a, b$ are consecutive in $X$ $(a(1) = b(0))$, then their ordinary concatenation $a+b$ is also a d-path

$$(a+b)(t) = a(2t),\,\text{if}\, 0\le t\le \frac{1}{2},$$

$$(a+b)(t) = b(2t),\,\text{if}\, \frac{1}{2}\le t\le 1.$$

A **morphism of directed topological spaces**  $f : (X, d X)\to (Y , d Y)$ is a morphism of topological spaces $f: X \to Y$ which preserves directed paths in that for every $\gamma: I \to X$ in $d X$ the path $f_* \gamma : I \stackrel{\gamma}{\to} X \stackrel{f}{\to} Y$ is in $d Y$.

#Examples#

* The _standard directed interval_ is $I_d = ([0,1], d I)$ with $d I$ the set of all _monotonic_ continuous maps $[0,1] \to [0,1]$.

* Any [[pospace]] $X$ gives rise to a directed space by taking the directed paths to be, well, directed paths, i.e. continuous order-preserving maps from $I_d$ to $X$.

#Remarks#

* If we can equip directed spaces with an internal hom, then a directed space with at least one directed path should be a strictly directed object in the category of directed spaces, with respect to the standard directed interval as the [[interval object]], while an ordinary topological space regarded as a directed space should be an [[undirected object]].

+--{.query}
But for that to work we need the structure of a directed topological space on $C(I_d,(X,d X))$. This requires that $X$ has _directed homotopies_! Does Grandis discuss higher directed paths, too? &#8212;Urs

_Toby_: I don\'t think that you need internal homs and all that.  But see my edits to [[directed object]].

[[Urs Schreiber|Urs]]: I think we need directed homotopies to check if a "constructed" directed space is actually a directed object in the original definition: that original definition asks us to check if the internal hom $[I,X]$ is weakly equivalent to $X$. Well, I made up this definition because I think it is the right abstraction, but there is room of course to debate this. But if we accept it then we should try to define the internal hom of Grandis' directed spaces. There is an obvious solution which one should check the details of: namely a directed topological space should be one which singles out not only subsets of $hom(I,X)$ but subsets of $hom(I^{\times n}, X)$ for all $n$, closed under the obvious reparameterization and gluing. This would induce an obvious notion of directed homotopies and should induce in an obvious way an internal hom for directed topological spaces. I'd think. But I don't feel like investing much time into finalizing this idea right now...

=--

#References#

The above definition is from

* [[Marco Grandis]], _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

This has now developed into a book

* [[Marco Grandis]], _[[Directed Algebraic Topology]], Models of non-reversible worlds_ , Cambridge University Press


A discussion of reparameterization of directed paths in directed topological spaces is in

* Ulrich Fahrenberg and Martin Raussen, _Reparametrizations of Continuous Paths_ ([arXiv](http://arxiv.org/abs/0706.3560), ([blog](http://golem.ph.utexas.edu/category/2006/09/fahrenberg_and_raussen_on_cont.html)))

Further references atre given in [[directed homotopy theory]].



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
I don't see what you want to mean by a "directed category". See, the point is that a category already _is_ supposed to be a combinatorial model for a directed space. Just as a groupoid is a combinatorial model for an undirected space. This is the very motivation for defining directed spaces: to fill in the question marks in

* groupoid | space  || category | ?? .

This is why a directed space is defined such that its "thing of all paths in it" is not, in general, a [[fundamental groupoid]] but a [[fundamental category]].

Methinks that for the application which you have in mind you want to be studying [[partial order|posets]] and these are special cases of categories and in particular naturally interpreted as combinatorial models for directed space, in exactly the way in which you are thinking of them as directed spaces! So 
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

_[[Eric Forgy|Eric]]_: Ugh. I didn't want a directed space to be a directed object in the category of directed spaces. That is boring :) A set is an object in the Set too, but it doesn't tell you anything. Hmm. It looks like what I wanted isn't going to work as is, i.e. a directed space is not a directed object in Top because there are no directed objects in Top apparently.

[[Urs Schreiber|Urs]]: I think you do want that. Just don't let the terminology let mix you up. An ordinary space is already called a space. While from your perspective an ordinary space ought to be called an _undirected space_.  Then "space" could be assigned to mean "not-necessarily but possibly directed space" and then a directed space could be called a directed object in spaces.

But convention is different. So a directed space is a directed object in the category of "not necessarily but possibly drected spaces".

_Toby_: Even here, I don\'t think that you\'re really using the terminology ideally.  The proper term for what you\'re calling a "not-necessarily but possibly directed space" is just *directed space*!  Much like a non-associative algebra might happen to be associative, so a directed space might happen to be undirected.  (In terms of Grandis\'s definition, any space $X$ defines a directed space where $d$ consists of only the constant paths.)

[[Urs Schreiber|Urs]]: Right, Toby, I think that is my point. I was just trying to convince Eric that there is nothing wrong or cheating or boring about the fact that "a directed space is a directed object in the category of directed spaces".

But maybe the the true issue is whether we want to speak of "directed objects" over at [[directed object]] or rather restrict to speaking about _undirected objects_. Then every object would be a directed object, possibly with trivial direction information, while those objects which are propertly directed would be the _not undirected objects_. 

I consider you as an authority on such issues of logical rigour. You should say how we should fix the terminology and we'll implement that.

_Toby_: I\'ll discuss this at [[directed object]].


[[!redirects d-space]]