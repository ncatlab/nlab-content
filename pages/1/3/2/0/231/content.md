Loosely speaking, a **monoidal category** is a category with a tensor product that's associative up to isomorphism.  The full definition is considerably longer, but someday you'll see it here.

##Discussion##

_[[Eric Forgy|Eric]] says_: In the definitions I've seen, e.g. [here](http://unapologetic.wordpress.com/2007/06/28/monoidal-categories/) and [here](http://en.wikipedia.org/wiki/Monoidal_category), it seems like you say, "We want to have a monoid with a product that satisfies this and that" then there are several complicated looking diagrams that need to be satisfied. Is there some magic wand we can wave (probably via arrow theory) that makes all those conditions just pop out naturally?

_[[Eric Forgy|Eric]] says_: Oh oh! Looking at the [[General Discussion]], [[John Baez|John]] said (referring to graded algebras):

<blockquote>

It's a monoid in GradedVect, the monoidal category of graded vector spaces.

</blockquote>

So the magic wand must be [[internalization]] (?)

_[[Toby Bartels|Toby]] says_: Well, somewhat. But if you take a monoid internal to the category of categories, then you get a *strict* monoidal category, and hardly any of the examples in nature are strict. So there are subtleties in the coherence rules for the weakened version. (Of course, you could take a monoidal category internal to the bicategory of categories, but nobody knew how to define that until they knew what a monoidal category is!)