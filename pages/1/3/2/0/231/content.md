A _monoidal category_ is a [[category]] $M$ equipped with a [[functor]]
$$ \otimes M \times M \to M $$
called the _tensor product_, an object
$$ 1 \in M $$
called the _unit object_, a natural isomorphism
$$ a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) $$
called the _associator_, a natural isomorphism
$$ \ell_x : 1 \otimes x \to x $$
called the _left unitor_, and a natural isomorphism 
$$  r_x : x \otimes 1 \to x $$
called the _right unitor_, which must satisfy a couple of equations, most notably the [[pentagon identity]].  

There is a [[strict 2-category]] MonCat with:

* monoidal categories as objects,
* [[monoidal functors]] as morphisms, 
* [[monoidal natural transformations]] as 2-morphisms.

For definitions of all these concepts, and a precise description of the 'couple of equations' alluded to here, see:

* John Baez, [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

For an elementary introduction to monoidal categories using string diagrams, see:

* John Baez and Mike Stay, [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

Eventually we should include all these definitions and diagrams here!

##Discussion##

_[[Eric Forgy|Eric]] says_: In the definitions I've seen, e.g. [here](http://unapologetic.wordpress.com/2007/06/28/monoidal-categories/) and [here](http://en.wikipedia.org/wiki/Monoidal_category), it seems like you say, "We want to have a monoid with a product that satisfies this and that" then there are several complicated looking diagrams that need to be satisfied. Is there some magic wand we can wave (probably via arrow theory) that makes all those conditions just pop out naturally?

_[[Eric Forgy|Eric]] says_: Oh oh! Looking at the [[General Discussion]], [[John Baez|John]] said (referring to graded algebras):

<blockquote>

It's a monoid in GradedVect, the monoidal category of graded vector spaces.

</blockquote>

So the magic wand must be [[internalization]] (?)

_[[Toby Bartels|Toby]] says_: Well, somewhat. But if you take a monoid internal to the category of categories, then you get a *strict* monoidal category, and hardly any of the examples in nature are strict. So there are subtleties in the coherence rules for the weakened version. (Of course, you could take a monoidal category internal to the bicategory of categories, but nobody knew how to define that until they knew what a monoidal category is!)

_[[John Baez|John]] says_: there is no magic wand that gives the "complicated looking diagrams" that Eric mentions.  Or rather, there _is_ a magic wand, but one so heavy that only the strongest of wizards can lift it: it's called **the theory of weak $n$-categories** --- monoidal categories are a puny special case!  

Luckily the "complicated looking diagrams" are completely obvious once they've been properly explained.  My paper with Mike Stay, linked to above may (or may not) do the job.

Toby is right, of course: [[monoid|monoids]] [[internalization|internal to]] [[Cat]] are *strict* monoidal categories.  But alas, these are not the fully general monoidal categories discussed on this page.  Internalization does not really get around the problem of guessing the diagrams --- such as the pentagon identity --- that make the definition of monoidal category interesting.