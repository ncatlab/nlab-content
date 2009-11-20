<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

Motivic cohomology was for a long time a hypothetical [[cohomology]] theory of [[scheme]]s whose hypothetical existence [[Alexander Grothendieck]] proposed in the 1960s should be the underlying reason for what are called the [[standard conjectures on algebraic cycles]].

In the mid 1990s [[Vladimir Voevodsky]] proposed a concrete definition of motivic cohomology of a smooth [[scheme]] $X$ over a field as the [[hypercohomology]] of certain [[complex of sheaves]] on the [[Zariski site|Zariski]] or [[etale cohomology|etale]] [[site]] of $X$ (an analog of the [[category of open subsets]] of a [[topological space]]). This complex is called the **motivic complex**; the existence of such a complex was predicted as part of the so-called Beilinson dream. 

Voevodsky gave a concrete definition of the [[derived category]] of the hypothetical category of [[mixed motive|mixed motives]]. The [[category of motives]] has not only more objects but also locally more morphisms than the category of schemes, and it comes with a [[functor]] from an appropriate category of schemes.  The morphisms are certain [[correspondence]]s, and Voevodsky has shown that the motivic complexes are realized as derived hom-complexes in his derived category of mixed motives.

Voevodsky's proposal has been shown to have most properties that Grothendieck and Beilinson had demanded of the hypothetical cohomology theory, except that to date it hasn't been shown yet that the cohomology groups vanish in negative degree, as they should.


## Voevodsky's definition ##

The **motivic complex** -- a [[chain complex]] of [[sheaf|sheaves]] with values in abelian groups -- is defined in [definition 3.1, page 33](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=33) of 

* Carlo Mazza, Vladimir Voevodsky and Charles Weibel, _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))

+-- {: .un_defn}
###### Definition
The motivic cohomology of a [[smooth scheme]] $X$ is the [[abelian sheaf cohomology]], more specifically hypercohomology, of the motivic complex of sheaves with transfers on the Zariski site. See [definition 3,4, page 22](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=34).
=--

The analogous definition with the Zariski [[site]] structure of $X$ replaced by the [[etale cohomology|etale site]] $Et(X)$ is in [lecture 10](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=87).


### As hom-sets of motives ###

Motivic cohomology computes certain derived hom-sets in the [[motive|category of motives]].

This is discussed in [lecture 14](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html). See [prop 14.16](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=126).


## References ##

* [[Carlo Mazza]], [[Vladimir Voevodsky]] and [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))


[[!redirects motivic complex]]