#Idea#

$\omega$-Categories are precisely those [[globular set|globular]] [[higher category theory|infinity-categories]] which are _strict_.

+-- {: .query}

[[Toby Bartels]]: Who actually uses the language this way? If anything, it should be the reverse, as 'omega' is Greek (like 'bi', 'tri', and 'tetra') and 'infinity' is not.  

[[John Baez]]: For a long time, for most category theorists, the default meaning of '$n$-category' has been 'strict globular $n$-category' &#8212; especially since weak $n$-categories had not yet been defined (except for very low $n$).   So when Street invented '$\omega$-categories' in his paper on orientals, he meant 'globular strict $\infty$-categories'.  Now there are many definitions of 'weak $n$-category', terminology is in flux, and people like [[Tom Leinster]] and myself advocate a new system in which '$n$-category' means 'some sort of possibly weak $n$-category' &#8212; at least until one has defined it more precisely in a specific context.  It is still true that most papers referring to $\omega$-categories mean 'globular strict $\infty$-categories'.

We may want to discuss whether the $n$Lab adopts traditional terminology, or takes this historic opportunity to play Bourbaki and choose consistent terminology for the future (while still explaining the traditional terms, or course).  In any event, globular strict $\omega$-categories are worth talking about, and that's what this page is about!

[[Toby Bartels]]: I agree with you and Tom about '$n$-category', and I agree that the strict globular case is worth talking about. I only question making a terminological distinction between '$\omega$-category' for the strict globular concept and '$\infty$-category' for the general weak case; (this seems to go against both the Greek-prefixes-for-the-weak-concept convention *and* the usual-name-for-the-weak-concept convention!). And I'm wondering if this distinction is established somewhere.

[[Urs Schreiber]]: I am not dogmatic about this, but I did not make this up, I think. I thought I followed the standard convention. 

I jumped on the $\omega$-category train after 

1. I learned about [Sjoerd Crans' work](http://crans.fol.nl/papers/comb.html) on $\omega$-categories from Todd. Sjoerd Crans uses the term "$\omega$-cvategory" for strict $\infty$-categories throughout;

and

2. after Mike Shulman pointed out that there is now an extension of the [[folk model structure]] to it, described by Lafont, M&#233;tayer and Worytkiewicz [here](http://arxiv.org/abs/0712.0617). They use the term "$\omega$-category" in this article and in all their other previous articles for strict $\infty$-catgeories.

Together with Ross Street's original work on $\omega$-categories this seems to say that _all_ the substantial work on the theory of strict $\infty$-categories uses the term "$\omega$-category" for them. 

I have added more references below, all of which use the term $\omega$-category exclusively for strict $\infty$-categories. Please have a look.

Finally, I thought that the terminology was actually a good idea: I was thinking of the "$\omega$" as indicating the (important) fact that $\omega$-categories are the directed limit of the iterated enrichment process

$$
  Cat \hookrightarrow
  2Cat = Cat-Cat
  \hookrightarrow
  2Cat = (Cat-Cat)-Cat
  \hookrightarrow
  3Cat = ((Cat-Cat)-Cat)-Cat
  \hookrightarrow 
  \cdots
  \,.
$$

=--

This means that 

 * all composition operations are strictly associative;

 * all composition operations strictly commute with all others (strict [[exchange law]]s);

 * all identity $k$-morphisms are strict identies under all compositons.

#Definition#

...

#Literature#

$\omega$-categories were introduced, together with [[oriental]]s, in 

* Ross Street, _The algebra of oriented simplices_,
J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)).


A review of some of the theory in the context of some of the history is given in 

* Ross Street, _An Australian conspectus of higher categories_ ([pdf](http://www.math.mq.edu.au/~street/Minneapolis.pdf))

and also in

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

The theory of $\omega$-categories was further developed by Sjoerd Crans in parts 2 and 3 of his [thesis](http://crans.fol.nl/papers/comb.html)

* Sjord Crans, _Pasting presentations for $\omega$-categories_ ([link](http://crans.fol.nl/papers/thpp.html))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([link](http://crans.fol.nl/papers/thten.html))

See also the 

* [Introduction](http://crans.fol.nl/papers/thintro.ps.gz) 

to his thesis, in particular section I.3 "$\omega$-categories".




#Further resources#

See also [[omega-groupoid]].