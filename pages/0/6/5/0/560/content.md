+--{.query}
There are really two separated (but related) concepts here.  In one case, you start with a category with interval object and carve out of that the subcategory of *undirected objects*.  In the other case, you start with a category with interval object, typically where every object is undirected in the above sense, and (by equipping the interval object with a submonoid of endomorphisms) extend that to a supercategory of *directed objects*.  I think that these should go on separate pages, and I\'ve written them as two articles below.  I\'ll move the first to [[undirected object]] if people agree.  &#8212;[[Toby Bartels|Toby]]
=--

#Undirected objects#

##Idea##

In a category with [[interval object]] one has for every object $X$ a notion of paths in $X$. (Indeed, the very definition of category with interval object is meant to guarantee that for every object there is its [[fundamental category]] in the [[Trimble n-category|Trimblean sense]]).

The idea is that if for all these paths in $X$ there is a _reverse_ path, then the object $X$ is _undirected_ or _groupoidal_. Otherwise it is _strictly directed_. 

##Definition (tentative)##

Let $V$ be a [[category] with an [[interval object]] $I$. Recall that there is for every object $X$ of $V$ a canonical morphism $X_0 \to [I,X]$ which embeds the points of $X$, $X_0 := [pt,X]$, as the constant paths into the "object of directed paths" $[I,X]$.

An object $X$ in $V$ is called **undirected** or an **undirected object** with respect to $I$, &#8211; or **$I$-undirected** &#8211; if this morphism is a weak equivalence:
$$
  (X is undirected) \Leftrightarrow
  ([\pt,X] \stackrel{\simeq}{\to} [I,X])
  \,;
$$
otherwise it is called **strictly directed** or a **strictly directed object** with respect to $I$, or **strictly $I$-directed**.

##Examples##

* $V = $  [[Top]] with its standard [[model category]] structure, and $I = [0,1]$ the standard interval. Then all objects are undirected since the interval is contractible.

* $V = \omega Cat$, [[strict omega-category|strict omega-categories]], equipped with the [[folk model structure]] and $I = \{a \to b\}$ the 1-[[globe]], the first [[oriental]]. Then
  * strict $\omega$-[[omega-groupoid]]s are undirected;
  * in particular the interval $I$ itself is strictly directed, as there is no weak equivalence from $I_0 = I$ to $[I,I] = \{a \to b \to c\}$; 
  * in general, the undirected objects should be precisely those for which every $j$-morphism is an $\omega$-[[equivalence]].  These should consist of those $\infty$-[[infinity-groupoid]]s that are strict as $\infty$-categories, or those objects that are weakly equivalent to a strict $\omega$-groupoid.

* Once we have a closed monoidal homotopical structure on the category $dTop$ of [[directed space|directed topological spaces]], it should be true that in $V = dTop$ with $I = I_d$ the standard directed interval, an object $(X, d X)$ is undirected precisely if it contains no nontrivial directed path.

##Remarks##

Whether or not an object is undirected depends on the choice of interval object. 

* For instance the terminal object $pt$ itself is always a an interval object, $I = pt$, but in a trivial way. Every object is $pt$-undirected. 

* A bit more generally, the interval object may be not equal to the terminal object, but still be _weakly equivalent_ to it.  For instance the standard (undirected) topological  interval $[0,1]$ is not equal to but is weakly equivalent to the point in the standard  [[model structure on topological spaces]]. This implies in particular that with  respect to the standard undirected topological interval even a [[directed space|directed topological space]] should undirected. (Well, we still need to specify the closed structure on $dTop$ to make this true...) It's only the standard _directed_ topological interval which can detect the directedness of a strictly directed topological space.

* Analogous statements are true in the example of [[strict  omega-category|strict omega-categories]], where the analogue of the standard directed topological interval is the 1-[[globe]] $I_{dir} = \{a \to b\}$, while the example of the standard undirected topological interval is the [[groupoid]] version of this, $I_{inv} = \{a \stackrel{\simeq}{\to} b\}$, where the morphism from $a$ to $b$ is an [[isomorphism]]. As opposed to $I_{dir}$ this $I_{inv}$ is weakly equivalent to the terminal category $pt = \{\bullet\}$ (the 0-[[globe]]) (with respect to the [[folk model structure]]). It should be true that every strict $\omega$-category is $I_{inv}$-undirected, even if it is $I_{dir}$-directed.

# Directed objects #

## Idea ##

This is a more 'constructive' (not in the sense of [[constructivism]]) version of directed object, one that doesn\'t just begin with a category of possibly directed objects and ask which are undirected, but instead begins with a category of (presumably) undirected objects and constructs *from* that a supercategory of directed objects, much as Grandis developed directed topological spaces out of the usual undirected ones.

## Definition (tentative) ##

Let $C$ be a category with an [[interval object]] $I$, and suppose that every object $X$ of $C$ is $I$-[[undirected object|undirected]].

To be explicit, fix a subset
$
  d_I \subset {}_{pt}hom(I,I)_{pt}
$
of the endomorphisms of the given [[interval object]] $I$ regarded as a cospan $pt \to I \leftarrow pt$ to be called the _directed endomorphisms_ of the interval object.

Then let an **$I$-directed object** of $C$ be an object $X$ of $C$ equipped with a [[subset]] $d$ or $d_X$ of the [[hom-set]] $I \to C$; elements of $d$ are called **directed paths** in $(X, d)$.  The directed paths must satisfy these conditions (following Grandis):
1. (constant paths) every map $I \to \pt \to X$ is directed;
2. (reparametrisation) For $\gamma \in d_X \subset hom(I,C)$  and every $\phi \in d_I \subset hom(I,I)$, also $\gamma \circ \phi$  is in $d_X$;
3. (concatenation) if $a, b: I \to X$ are consecutive in the sense that $\pt \to^{\tau} I \to^{a} X$ equals $\pt \to^{\sigma} I \to^{b} X$, then their concatenate $I \to X$ (which exists by the pushout properties of an interval object) is a directed path.

A morphism of such directed objects is a morphism of their underlying objects that preserves directed paths.  This defines a category $d_I{C}$ of which the original $C$ is a subcategory.

+--{.query}

_Eric_: I don't fully "grok" this constructive definition, but I like its flavor. Is it possible to formalize the procedure in a simple catchy phrase? In other words, when you begin with a "category $C$ with interval object $I$", but whose objects are otherwise undirected (like Top), you construct the "supercategory $d_I C$" with directed $C$-objected (even though no objects in $C$ are directed). I used the term "directed internalization", but is there a better term?

I just think this concept is important and should have some really slick arrow theoretic description and I'm not having any luck coming up with one myself.

=--

## Examples ##

* The category of [[directed space|directed topological spaces]] according to Grandis is of the above form $d_I{C}$ for $C = $ [[Top]], $I = [0,1]$ and $d_I = \{monotonic maps I \to I\}$.

#References#

The definition and study of directed topological spaces was undertaken in

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

Applications of categories regarded as models for directed spaces are discussed in

* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.

* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))

#Discussion#

Here is a leftover discussion which used to be at [[directed space]] and is now probably mostly taken care of. 

_[[Eric Forgy|Eric]] asks about how best to define directed spaces that involves [[interval object]]_

[[Tim Porter|Tim]]: My approach would be first to see what the examples of things that we need as directed spaces:  spaces with a (local?) closed partial order for instance, Marco Grandis' $d$-spaces, Lorentz manifolds (no specific time direction, but can't go backwards, (so _time slice_ will be something that needs to be 'formulateable'), causal sets in their various forms, and so on. We want both physics and computer science as inspirations I think.

Have a look at Martin Raussen and Lizbeth Fajstrup's work as well, then Philip Gaucher's flows, which although I think that they are too near the Computer Science applications for our needs, have some very interesting aspects. Finally look at Sanjeevi's pages at [LIX](http://www.lix.polytechnique.fr/~sanjeevi/).

There were a lot of talks at [ATMCS08](http://www.lix.polytechnique.fr/~sanjeevi/atmcs/), last summer on this sort of thing.

[[Urs Schreiber|Urs]]: 
Ah, now that I re-read what you say above, maybe this is what you are getting at:

suppose I hand you a space and don't tell you whether it is directed or not. How do you decide if it is? One way might be: you map the directed _interval_ into the space -- i.e. look at the collection of paths in the space -- and check if every path can be contracted _in both directions_ to a point. If not, the space must be directed.

I have a proposal for how to formalize this in terms of [[interval object]]s which you link to: in case the category from which we pick our spaces is equipped with a notion of weak equivalences (for instance if it is a [[model category]]) and with an [[interval object]] which is itself not weakly equivalent to the point, then for every object $X$ in the category we can look at the canonical map $X \to [I,X]$ which embeds $X$ into its "path space" as the space of constant paths. I am proposing that we should call $X$ _directed with respect to $I$_ iff this map is not a weak equivalence.

$$
  (X not directed) \Leftrightarrow
  (X \stackrel{\simeq}{\to} [I,X])
$$

Notice that for instance in a [[category of fibrant objects]] the map $X \stackrel{\simeq}{\to} [I,X]$ is _required_ to be a weak equivalence. And indeed, these categories behave much like categories of (ordinary) topological spaces.

For instance if we take $I = G_1 = \{a \to b\}$ the 1-[[globe]] aka the first [[oriental]] then
all strict $\omega$-groupoids are undirected with respect to this definition, while a [[strict omega-category]] which is not an $\omega$-groupoid will be undirected with respect to this definition. The way it is supposed to be.

[[Tim Porter|Tim]]: One thought is that we might think about what directed homotopy should give us. By Thomason's result from way back, categories themselves model all homotopy types, so getting a model of  a directed homotopy type that is a category may not be a 'big deal' unless it really tells us something immediate and 'useful' about the directed situation.  

The work of various of the directed homotopyists who are trying to look fo deadlocks, inaccessible points, bifurcations etc. seem to me to be definitely going in the right sort of direction. i.e. those are types of phenomenon that are important for applications, intrinsic to directed homotopy (i.e. don't make much sense for the un-directed case) and somehow look as if they do work with the directed object idea, since they are directed points where the forward cone changes its homotopy type. (Again look at some of Raussen and Fajstrup, in particular, perhaps more than Grandis, although there are similar ideas in his articles as well.)

I think, Urs, you asked about directed cubes based on an interval object. 
The idea of using directed cubes is there in the literature.  (I would have to check, but Marco has thought about this I know and I think that is in his work. It was in his ATMCS talk I know.) I have used  directed simplices, but it is not clear how to get such things in an abstract setting.

A final point is that Gaucher uses semicategories (i.e. without identities) because identities are problematic in the computer scientific applications (for the same sort of reason as they cause problems in cobordism theory).

_[[Mike Shulman|Mike]]_: I think that Thomason's modeling of homotopy types with categories is not really relevant because the modeling happens in a very different way.  For Thomason, a category models a homotopy type via its [[nerve]], which corresponds categorically to constructing an $\infty$-groupoid from a category by forcibly inverting all the arrows up to homotopy.  What we are looking for here is instead a directed analogue of the way that groupoids model all (undirected) 1-types, which is quite different: the morphisms in the groupoid are precisely the paths in the space, and they are already invertible because the space is undirected.  We want a "fundamental category" of a directed space which directly generalizes the fundamental groupoid of an undirected space.

[[Tim Porter|Tim]] : You may like to look at the paper I wrote 

Enriched categories and models for spaces of evolving states, Theoretical Computer 
Science, 405, (2008), pp. 88 - 100. 

I put forward simplicially enriched categories as one possible model for a direct space.  There is a fundamental category that generalises the fundamental groupoid and I think coincides with the similar concept defined by Raussen and Fajstrup. I should point out that my construction uses a nerve like construction!