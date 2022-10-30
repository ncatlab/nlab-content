A better title might be "Unpacking a Concrete Category"

See also [[category of elements]]

category: redirect

##Example: Action Groupoid##

Given a vector space $V$, a group $G$, and a [[representation]] 

$$\rho:\mathbf{BG}\to Vect,$$

denote the image of $\rho$ by

$$V\nearrow G.$$

This has a nice pictorial depiction via

$$V\bullet\righttoleftarrow G.$$

The [[action groupoid]] $V//G$ is then given by

$$V//G=Explode(V\nearrow G).$$

##Example: Path Category##

+--{.query}

>[[Urs Schreiber|Urs]]: I am not sure what is meant with the following example!

>[[Eric Forgy|Eric]]: The idea needs fleshing out, but the basic concept was outlined <a href="http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017583">here</a> (and you partially approved <a href="http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017596">here</a>! :))

=--

Consider a category $X\nearrow\Gamma$ with one object, a set $X$, and one morphism

$\Gamma:X\to X$

for each "evolution map" in $X$. This category may be depicted as

$$X\bullet\righttoleftarrow\Gamma.$$

The [[path category]] $P_1(X)$ is given by

$$P_1(X)=Explode(X\nearrow\Gamma).$$

##References##

* [Exploding a Category](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017574)

##Discussion##

+-- {: .query}
Eric, what would you call $Explode(C)$ is words?: the 'explosion' of $C$, the 'exploding' of $C$, the 'exploded category' of $C$?  ---Toby

[[Eric Forgy|Eric]]: If the term '[[category of elements]]' is standard, then you could just call it that. I'm not excited by the notation $El(C)$ though. I'm still thinking about the best way to present this. I like the picture (see below) of "exploding" a category that is missing in the description of [[category of elements]] and is also not indicated by the notation $El(C)$. The image I get when I think of this is roughly like a fireworks display.

PS: For a field that is so "pictorial" in nature, the nCafe generally is sadly lacking in "pictures".

[[Urs Schreiber|Urs]]: I like the figures you included, and I do like the attitude to explain this concept -- and concepts in general -- in the kind of way you are doing here. I didn't mean to complain about your style of explaining this. We need much more of more "low brow", if you wish, explanations at $n$Lab entries, yes.

But why not put this low brow, intuitively more accesible description alongside with the entry that presents the concept from a more highbrow, more category-theoretic perspective? Isn't it best to have all perspectives joined in a single entry? So that every reader can find his or her own entry point and discover the other aspects from there? 

My suggestion would be to create in the entry [[category of generalized elements]] a section with your material here. It's great to tell the reader that he or she may find it helpful to think of a "category of elements" as an "exploded category". Nothing against that. 

=--

>[[Urs Schreiber|Urs]]: the following really describes this concept: given a category $C$ with a [[generator]] ${*}$ or some other singled out object such as a tensor unit if $C$ is monoidal, there is the category of [[generalized element]]s of $C$ with respect to ${*}$, which is the [[over category]] $(*/C)$. The term "exploding a category" is very non-standard and I don't really like it, to be frank. Could we move this here maybe to something like "category of elements", or the like? 

>[[Eric Forgy|Eric]]: It does no harm to keep this here. I'm not sure why you don't like it so much. I spent a lot of time trying to understand this and I think others (maybe non-mathematicians) would be served to see this concept explained on a low brow level. The picture **is** that of a category being "exploded" into pieces, so I think the term is accurately descriptive. Once again, it does no harm to keep this here. A pointer to [[category of generalized elements]] for the high brow version should suffice I think.