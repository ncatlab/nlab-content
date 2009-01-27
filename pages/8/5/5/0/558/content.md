The _homotopy hypothesis_ states that $n$-groupoids model homotopy $n$-types. As a slogan:

* $\infty$-groupoids are combinatorial models for spaces.

To some extent the homotopy hypothesis is not a hypothesis but a _requirement_ on the definition of [[infinity-groupoid]]: for every "good" definition of $\infty$-groupoid there should be an "obvious" morphism from the collection of all $\infty$-groupoids to (well behaved) topological spaces, and this map should be an equivalence in a "suitable" sense.

The homotopy hypothesis is known to be true for some definitions of "$\infty$-groupoid".  For example, there is a good case to be made that a [[Kan complex]] is a notion of $\infty$-groupoid, and it's been known for a long time in [[homotopy theory]] that Kan complexes model spaces, homotopically speaking.  However, for other notions of [[higher category theory|higher category]], it remains a hypothesis/requirement.

+--{.query}

[[Tim Porter|Tim]]: I would like to pose a question on the Homotopy Hypothesis.  Playing devil's advocate for the moment, since Kan complexes, and simplicially enriched categories, both satisfy the homotopy hypothesis, why bother to search for other models?  That is a bit severe of course so a more 'constructive' form of the question is what criteria should we be looking to be satisfied so as to say that a model of homotopy types is a good one?  (Perhaps things like that the basic homotopy operations, such as Whitehead or Samelson products, should have clear formulations and clear interpretations.  The higher operations could then be gradually required.  The relation between obstructions to interchange laws (interchangeator!) and the low dimensional Whitehead products are 'clear' even if not that immediately evident in most writing on the subject (and I include my own in that!), but in higher dimensions .... ?

_[[Mike Shulman|Mike]]_: My perspective is that we are looking for good notions of _$\infty$-category_ such that the _induced_ notion of $\infty$-groupoid satisfies the homotopy hypothesis.  If all you want is to do homotopy theory, then homotopy theorists have gotten along quite well for decades with topological spaces, Kan complexes, and the like (although one might certainly hope, as you suggest, to get information about homotopy operations out as well).  But as category theorists, we want a notion of $\infty$-category with not all cells necessarily invertible, which behaves well _categorically_ rather than homotopically, but whose induced notion of $\infty$-groupoid still satisfies the homotopy hypothesis as a "check" or "anchor."  It's hard to exhibit Kan complexes as the $(\infty,0)$-case of a notion of $\infty$-category; there are [[quasi-category|quasicategories]] for $(\infty,1)$-categories but beyond that it gets tricky (there is Street's original definition, but it's quite difficult to work with).

[[Urs Schreiber|Urs]]: Lurie is now talking in (electronic) print about $(\infty,n)$-categories, [here](http://www-math.mit.edu/~lurie/papers/cobordism.pdf).

_Mike_: When I glanced at that, it looked as though he was actually using [[Segal category|Segal categories]] for his $(\infty,n)$-categories rather than some generalization of quasicategories.

[[Tim Porter|Tim]] I think, Mike, you are missing my point. You use the word 'good' with regard to notion. My point is that the higher homotopy operations ARE categorical structures that WILL  BE there in the various models. For instance, there are formulae given in Curtis's old survey article for the Samelson product in a simplicial group.  (No proof is available in the literature.) This uses shuffle products and various combinatorial ideas that fit well from the categorical viewpoint. As category theorists we can hope to find new understanding of what makes the infinity groupoid models work and hence what the infinity category models should be. As these products DO use inverses the problem of interpreting their analogue in an infinity category is not easy.  I feel it has, from my perspective, something to do with the basic homotopy coherent cube and the free simplicial cat resolution of a category, but I am not sure how to handle it. 

_Mike_: I think we are talking past each other.  I was trying to answer your question "why bother to search for other models?" by saying that from my perspective, what we're doing isn't just searching for new models for spaces, but rather searching for a good notion of $\infty$-category that still reduces to a model for spaces.  I took your mention of higher homotopy operations as a proposed answer to the first question "why bother to search for other models?"  So I wasn't addressing homotopy operations specifically -- I don't have any disagreement with it -- just pointing out that there are also other answers to the first question.

[[Ronnie Brown|Ronnie]] What is wrong with strict $n$-fold groupoids as a model of homotopy $n$-types? This is a theorem, not an hypothesis! (Loday, Porter).  One advantage of these is that one can do some calculations with them, using a higher homotopy van Kampen theorem, which Grothendieck interpreted as integration of homotopy types. 
They are certainly a very rich structure, with other interpretations of special cases. My question is: what are the expected purposes of these other models? My aim since 1966 has been to find  models which seem to give a natural extension of group theory, and hence to work with strict structures. My hypothesis is that this can always be done, if you can find the means to make the lax conditions part of the algebra. 

What held me up for 9 years in constructing higher homotopy groupoids was to concentrate on spaces: when Philip Higgins and I started to look at pairs of spaces, then things quickly fell into place. Thus the clear functors from strict $n$-fold groupoids give rise to  _structured spaces_. What is wrong with that? 




=--

#Remarks#

* In analogy to the homotopy hypothesis, there are attempts to relate general [[infinity-category|infinity-categories]] which need not be groupoidal to [[directed space]]s, in which a morphism which is not invertible would model a path in the space that can only be traversed in one direction.

* ([[Ronnie Brown|Ronnie]] To elaborate on the above, what we have are some functors $\Xi:({diagrams of spaces })\leftrightarrow ({higher groupoids}):B  $
such that:
1. $\Xi$ is homotopically defined and preserves certain colimits;
1. $\Xi \circ B$ is equivalent to Id;
1. There is a natural transformation $Id \rightarrow B \circ \Xi$ preserving some homotopical information. 

The purpose of 1. is to be able to calculate some homotopical information. The purpose of 2. is to show that the diagrams used reflect the algebraic structure of the higher groupoids. Detailed references are in the Higher dimensional group theory web site. 

Trying to be more explicit about some colimits of certain higher groupoids has yielded some interesting algebraic constructions, for which some examples required computational group theory!
 
#References#

* John Baez, _The Homotopy Hypothesis_ ([web](http://math.ucr.edu/home/baez/homotopy/), [pdf](http://math.ucr.edu/home/baez/homotopy/homotopy.pdf))

* Ronnie Brown, _Higher dimensional group theory_ ([web](http://www.bangor.ac.uk/r.brown/hdaweb2.htm). See also the linked pages there. 
