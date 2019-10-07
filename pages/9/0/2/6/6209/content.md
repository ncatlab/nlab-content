
> This entry is about the class of [[topological spaces]] satisfying the Baire category theorem. For *the* Baire space used in computable analysis, descriptive set theory, etc, see instead at _[[Baire space of sequences]]_.

# Baire spaces
* table of contents
{: toc}

## Idea

A Baire space is a [[topological space]] that satisfies the conclusion of the [[Baire category theorem]].

It should not be confused with the [[Baire space of sequences]] (which is an example of a Baire space in our sense but not a prominent one). Nor should it be confused with a [[Baire set]] (a [[subset]] somewhat analogous to a [[measurable set]] but defined by a topological property).


## Definition

A __Baire space__ is a [[topological space]] such that the [[intersection]] of any [[countable family]] of [[dense subspace|dense]] [[open subspace|open]] subspaces is also dense. Equivalently: a space such that a countable union of closed sets each with [[empty set|empty]] [[interior]] also has empty interior. 


## Examples

The classical [[Baire category theorem]] states that:

*  Any [[complete metric space]] (or rather its [[forgetful functor|underlying]] topological space, hence any completely metrizable topological space) is a Baire space. 

A second theorem, sometimes dubbed "BCT2" (as in Wikipedia):

*  Any [[locally compact Hausdorff space]], or indeed any locally compact [[sober space]] according to Wikipedia, is a Baire space. Moreover, any [[G-delta set]] of a locally compact Hausdorff space is a Baire space under the [[subspace]] topology. 

Furthermore:

*  Any [[open subspace]] of a Baire space is also a Baire space. 

*  Given a Baire space $X$, a _dense_ $G_\delta$ set in $X$ (i.e. a countable intersection of dense opens) is a Baire space under the subspace topology. See Dan Ma's blog, specifically Theorem 3 [here](https://dantopology.wordpress.com/2012/06/02/a-question-about-the-rational-numbers/). 

*  As mentioned above, the space of [[infinite sequences]] of [[natural numbers]], or equivalently (up to topology) the space [[irrational numbers]], is also known as '[[Baire space of sequences|Baire space]]'.  It is a Baire space in the present sense (since it admits a complete metric), but the coincidence of names appears to be just a coincidence.  (It is much more important that Baire space is a [[Polish space]] than that Baire space is a Baire space.  Of course, every Polish space is a Baire space too.)


[[!redirects Baire space]]
[[!redirects Baire spaces]]
