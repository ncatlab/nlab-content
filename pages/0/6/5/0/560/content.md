# Idea #

Begin with a category of objects presumed [[undirected object|undirected]] and construct from that a supercategory of directed objects, much as Grandis developed [[directed space|directed topological spaces]] out of the usual undirected ones.

# Definition (tentative) #

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

# Examples #

* The category of [[directed space|directed topological spaces]] according to Grandis is of the above form $d_I{C}$ for $C = $ [[Top]], $I = [0,1]$ and $d_I = \{monotonic maps I \to I\}$.

#References#

The definition and study of directed topological spaces was undertaken in

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

Applications of categories regarded as models for directed spaces are discussed in

* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.

* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))

#Discussion#

Here is a leftover discussion which used to be at [[directed space]] (and also concerns [[undirected object]]) and is now probably mostly taken care of. 

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