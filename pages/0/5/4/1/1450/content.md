#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

In _synthetic differential geometry_ one formulates differential geometry in a [[topos]] of [[space and quantity|generalized spaces]] which has an object $T$ (often also denoted $D$) that behaves like an [[infinitesimal object|infinitesimal interval]], so that for instance for $X$ another object regarded as a smooth space, the tangent bundle of $X$, is, again as an object of the topos, just the [[internal hom]] $T X := [T,X]$.

In [[topos]]es satisfying the [[Kock-Lawvere axiom|axioms of synthetic differential geometry]] it is possible to give precise well-defined meaning to many of the familiar computations -- wide-spread in particular in the [[physics]] literature -- that compute with supposedly "infinitesimal" quantities.

As quoted by Anders Kock in his book (see below), Sophus Lie once said that he found his main theorems in [[Lie theory]] using "synthetic reasoning", but had to write them up in non-synthetic style (see [[analytic versus synthetic]]) through lack of a formalized language.  Synthetic differential geometry now provides this formalized language.

In the book

* Moerdijk--Reyes, _[[Models for Smooth Infinitesimal Analysis]]_ 

a realization of a [[topos]] for synthetic differential geometry is constructed in terms of [[structured generalized space|structured generalized spaces]] modeled on [[generalized smooth algebra]]s. Among other things, the book describes in detail how the familiar but ill-defined "infinitesimal reasoning" in standard differential geometry finds its precise formulation in such a topos.

In this vein, Anders Kock, in a long series of articles, reformulates large parts of differential geometry using synthetic reasoning. In his work he particularly makes use of the fact that as sophisticated as a synthetic [[topos]] may be when explicitly constructed, being a [[topos]] means that one can reason inside it almost literally as in [[Set]]. Using this Kock's work gives descriptions of synthetic differential geometry which are entirely intuitive and have no topos-theoretic flavor. All he needs is the assumption that the _Kock-Lawvere axiom_ is satisfied for "numbers". Here "numbers" is really to be interpreted in the topos, but if one just accepts that they satisfy the KL axiom, one may work with infinitesimals in this context in essentially precisely the naive way, with the topos theory in the background just ensuring that everything makes good sense.



# Variations #

## higher categoricalversions ##

* Synthetic differential geometry may be thought of as embedded in the general theory of [[derived smooth manifold]]s and, generally, that of [[generalized scheme]].

## supergeometry  versions ##

The notion of synthetic differential geometry extends to the context of [[supergeometry - contents|supergeometry]]. See

* [[synthetic differential supergeometry]] .


# Related entries #

* [[infinitesimal singular simplicial complex]]

  * [[differential forms in synthetic differential geometry]]

  * [[Chevalley-Eilenberg algebra in synthetic differential geomet|Chevalley-Eilenberg algebra in synthetic differential geometry]]

# References #

## Books ##

*  Online first edition of [Synthetic Differential Geometry](http://home.imf.au.dk/kock/sdg99.pdf) by [[Anders Kock]]

*  A preprint of [[Anders Kock]]'s new book _Synthetic Geometry of Manifolds_ is available at his [homepage](http://home.imf.au.dk/kock/).

* Moerdijk--Reyes, _[[Models for Smooth Infinitesimal Analysis]]_ 


## Exposition ##

*  [Mike Shulman](http://www.math.uchicago.edu/~shulman/exposition/sdg/pizza-seminar.pdf)

*  [John Bell](http://publish.uwo.ca/~jbell/invitation%20to%20SIA.pdf)



# Discussion #

+-- {: .query}

[[Eric]]: Mike, have you ever looked into [stochastic calculus](http://en.wikipedia.org/wiki/It%C5%8D%27s_lemma)? I was looking at your "pizza seminar" and was left with the thought that stochastic calculus might also be presented in terms of synthetic differential geometry. To do so, you need a slightly different class of elements $\delta$ such that that $\delta^2\in D$ and $d\delta = 0$. Then the 2-dimensional Taylor expansion becomes the [Ito lemma](http://en.wikipedia.org/wiki/It%C5%8D%27s_lemma):

$$f(t+d,w+\delta) =  f(t,w) + \left(\frac{\partial f}{\partial t} + \frac{1}{2}\frac{\partial^2 f}{\partial w^2}\right) d + \frac{\partial f}{\partial w} \delta.$$

Just curious...

[[Eric]]: On second thought, $d\delta = 0$ is probably too strong. You could probably get away with $d\delta = -\delta d$.

[[Mike Shulman]]: No, I haven't looked into stochastic calculus; that's an interesting idea.  But I don't know what $d\delta$ means.

[[David Roberts]]: the product, presumably. So Eric seems to be proposing a second lot of infinitesimals $D'$ such that the product of two things in $D'$ are in $D$ and (in the first version) the product of something in $D$ and something in $D'$ vanishes, or in the second version that the product $D\times D' \to R$ is antisymmetric.

[[Mike Shulman]]: Sorry, I guess I wasn't quite awake enough to guess that Eric meant "for any $d\in D$."  The usual models of SDG do contain pretty much any sort of infinitesimal you want; you can make that precise by talking about polynomial rings of nilpotents.
=--
