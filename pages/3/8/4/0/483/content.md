#Idea#

_Directed spaces_ are to general $\infty$-[[infinity-category|categories]] as ordinary [[topological space|topological spaces]] are to $\infty$-[[infinity-groupoid|groupoids]] via the [[homotopy hypothesis]].

Directed spaces are studied in [[directed homotopy theory]], a relatively young topic. In generalization of how a [[topological space]] has a [[fundamental groupoid]], a [[directed space]] has a [[fundamental category]].

+--{.query}

Can directed spaces be defined using [[interval object]]?

###Tentative (and Probably Wrong) Definition###

A **directed space** is a topological space with an [[interval object|interval]].

A **directed category** is a category with an [[interval object]].

[[Tim Porter|Tim]] :  Eric, can you be more precise about what you mean, say, with the first of these? 

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

=--

#Discussion#

_[[Eric Forgy|Eric]] says_: [[ericforgy:Discrete differential geometry on causal graphs|Urs and I]] wrote a paper a few years back, which essential starts with a [[directed graph]] and builds a [[ericforgy:differential envelope|graded differential algebra]], which in turn, specifies something that I would call a [[ericforgy:directed space|directed space (under construction)]]. I've been trying to understand this in the context of [[space and quantity]] as stated [[ericforgy:HomePage|here]]. Seeing your entry gives me hope that all this can be tied together, but my maths chops are not quite up to the task of seeing it myself.

Skimming the paper, it looks like a directed space should have some interpretation in terms of [[poset|posets]] or [[preorder|preorders]], which in turn, could have some physical interpretation in terms of causality. Oh! Thank goodness for search functions. "Preorder" appears many times and this seems to be exactly the answer to a question I was going to ask...

***

[(page 2)](http://arxiv.org/abs/math.AT/0111048)

Direction is quite different from orientation (1.3a); the links with ordering are more subtle. Various
$d$-spaces of interest derive from an ordinary space equipped with an order relation (1.4a), as in the
case of the _directed interval_ &#173;$\uparr\text{I} =\uparr [0, 1]$; or, more generally, from a space equipped with a _local preorder_ (1.4b), as for the directed circle &#173;$\uparr\mathbf{S}_1$.

***

This might help with a conjecture of mine I've been throwing around. Just as a smooth manifold can be triangulated, a directed space can be _diamondated_, i.e. discretized with directed cubes, so that it is locally cubic with a preferred directed. I THINK what I've been after might be consider a finitary/countable version of this notion of directed space.

Any thoughts to help me sort this out would be greatly appreciated.

_[[Tim Porter|Tim]]_ added:   Perhaps some stuff that I did may help in this. I do not claim to have done more than collect up some thoughts from different areas and apply them in a fairly coherent way, I came up with the paper (below).

If it would help I could cooperate on something for the nlab on this.  

_[[Eric Forgy|Eric]] says_: That would be awesome.

PS: I've struggled with whether to call the spaces I'm interested in "discrete" or "directed" because they they are both discrete (as opposed to continuum, but not in the topological sense) and directed. In light of the fact that the directed spaces discussed here are continuum spaces, I think I might start calling the spaces I'm interested in "discrete directed spaces".

Do directed spaces fit into [[space and quantity]] such that there is a "directed graded differential algebra" dual to them?

#References#

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))
* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.
* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))

