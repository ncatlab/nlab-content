#Idea#

_Directed spaces_ are to general $\infty$-[[infinity-category|categories]] as ordinary [[topological space|topological spaces]] are to $\infty$-[[infinity-groupoid|groupoids]] via the [[homotopy hypothesis]].

Directed spaces are studied in [[directed homotopy theory]], a relatively young topic. In generalization of how a [[topological space]] has a [[fundamental groupoid]], a [[directed space]] has a [[fundamental category]].

#Definition: directed object (tentative)#

Let $V$ be a 
[[interval object|category with interval object]], with the interval object denoted $I$. Recall that there is for every object $X$ of $V$ a canonical morphism
$X_0 \to [I,X]$ which embeds the points of $X$, $X_0 := [pt,X]$ as the constant paths into the "object of directed paths" $[I,X]$. Assume now that $X_0 \simeq X$.

An object $X$ is called _undirected_ or an _undirected object_ if this morphism is a weak equivalence:

$$
  (X undirected) \Leftrightarrow
  (X \stackrel{\simeq}{\to} [I,X])
  \,;
$$

otherwise it is called _directed_ or a _directed object_.

+--{.query}

Can we find something a little more constructive? In other words, instead of testing objects in a category to see whether they are directed, could we construct the category of directed spaces?

[[Urs Schreiber|Urs]]: sombody please extract from Grandis' article linked to below the definition of directed topological space!

=--


#Examples#

* $V = $  [[Top]] with its standard [[model category]] structure, and $I = [0,1]$ the standard interval. Then all objects are undirected.

* $V = \omega Cat$, [[strict omega-category|strict omega-categories]], equipped with the [[folk model structure]] and $I = \{a \to b\}$ the 1-[[globe]], the first [[oriental]]. Then

  * the "generic" $\omega$-category is _directed_;

  * in particular the interval $I$ itself is directed, as there is no weak equivalence from $I$ to $[I,I] = \{a \to b \to c\}$; 

  * $\omega$-categories which are strict [[omega-groupoid]]s are _undirected_;

  * the general undirected $\omega$-categories should be precisely those for which every $k$-morphism is a an $\omega$-equivalence.

* (...somebody please add the example of directed topological spaces...)


#References#

The definition and study of directed topological spaces was undertaken in

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

Applications of categories regarded as models for directed spaces are discussed in

* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.

* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))





***


#Discussion#

+--{.query}

Can directed spaces be defined using [[interval object]]?

###Tentative (and Probably Wrong) Definition###

A **directed space** is a topological space with an [[interval object|interval]].

A **directed category** is a category with an [[interval object]].

=--

[[Tim Porter|Tim]] (re: a tentative definition of directed space):  Eric, can you be more precise about what you mean, say, with the first of these? 

My approach would be first to see what the examples of things that we need as directed spaces:  spaces with a (local?) closed partial order for instance, Marco Grandis' $d$-spaces, Lorentz manifolds (no specific time direction, but can't go backwards, (so _time slice_ will be something that needs to be 'formulateable'), causal sets in their various forms, and so on. We want both physics and computer science as inspirations I think.

Have a look at Martin Raussen and Lizbeth Fajstrup's work as well, then Philip Gaucher's flows, which although I think that they are too near the Computer Science applications for our needs, have some very interesting aspects. Finally look at Sanjeevi's pages at [LIX](http://www.lix.polytechnique.fr/~sanjeevi/).

There were a lot of talks at [ATMCS08](http://www.lix.polytechnique.fr/~sanjeevi/atmcs/), last summer on this sort of thing.

[[Urs Schreiber|Urs]]: 
Eric, in the way people usually think about "directed spaces", such as the references below, there is no good reason to speak of a "directed category". On the contrary: just as an ordinary space has a [[fundamental groupoid]] because one can traverse every path in both directions, a _directed space_ is supposed to be something such that paths in it form not a groupoid in general, but just a category: its [[fundamental category]]. Maybe we should chat about the definition of directed spaces as in the literature given below (which I would have to remind myself of) and in the sense which you are trying to develop (which is only vaguely clear to me at the moment!) on the blog.

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

_[[Eric Forgy|Eric]] says_: Now we're getting somewhere! Thanks Tim and Urs. It seemed to me that the [[interval object]] should come into play here and now it seems we can bring it in. I'll try to pull something out of Urs' statement, but was there a typo? Should a strict $\omega$-catgeory that is not an $\omega$-groupoid be _directed_?

_[[Urs Schreiber|Urs]]_: yes, typo. I have stated the definition now above the way I imagined it.

