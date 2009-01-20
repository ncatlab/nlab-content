#Idea#

In a category with [[interval object]] one has for every object $X$ a notion of paths in $X$. (Indeed, the very definition of category with interval object is meant to guarantee that for every object there is its [[fundamental category]] in the [[Trimble's notion of weak n-category|Trimblean sense]]).

The idea is that if for all these paths in $X$ there is a _reverse_ path, then the object $X$ is _undirected_ or _groupoidal_. Otherwise it is _directed_. 


#Definition (tentative)#

Let $V$ be a 
[[interval object|category with interval object]], with the interval object denoted $I$. Recall that there is for every object $X$ of $V$ a canonical morphism
$X_0 \to [I,X]$ which embeds the points of $X$, $X_0 := [pt,X]$ as the constant paths into the "object of directed paths" $[I,X]$. Assume now that $X_0 \simeq X$.

An object $X$ in $V$ is called **undirected** or an **undirected object** (with respect to $I$) if this morphism is a weak equivalence:

$$
  (X undirected) \Leftrightarrow
  (X \stackrel{\simeq}{\to} [I,X])
  \,;
$$

otherwise it is called **directed** or a **directed object**.


#Examples#

* $V = $  [[Top]] with its standard [[model category]] structure, and $I = [0,1]$ the standard interval. Then all objects are undirected.


* $V = \omega Cat$, [[strict omega-category|strict omega-categories]], equipped with the [[folk model structure]] and $I = \{a \to b\}$ the 1-[[globe]], the first [[oriental]]. Then

  * the "generic" $\omega$-category is _directed_;

  * in particular the interval $I$ itself is directed, as there is no weak equivalence from $I$ to $[I,I] = \{a \to b \to c\}$; 

  * $\omega$-categories which are strict [[omega-groupoid]]s are _undirected_;

  * the general undirected $\omega$-categories should be precisely those for which every $k$-morphism is a an $\omega$-equivalence.

* Once we have a closed monoidal homotopical structure on the category $dTop$ of [[directed space|directed topological spaces]], it should be true that in $V = dTop$ with $I = I_d$ the standard directed interval, an object $(X, d X)$ is a directed object in the above sense precisely if it contains a nontrivial directed path.

#Remarks#

* Whether or not an object is undirected depends on the choice of interval object. For instance if in the example of $\omega$-groupoids above we take instead of the first [[oriental]] (which is _oriented_, i.e. directed) the free groupoid on it, i.e the groupoid $I_{inv} = \{a \stackrel{\simeq}{\to} b\}$ then this interval object $I_{inv}$ is itself undirected. 

 


#References#

The definition and study of directed topological spaces was undertaken in

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

Applications of categories regarded as models for directed spaces are discussed in

* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.

* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))





***

Here is a leftover discussion which used to be at [[directed space]] and is now probably mostly taken care of. 

#Discussion#

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

