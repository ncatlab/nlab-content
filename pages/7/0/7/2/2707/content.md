
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The category of motives is something like an _abelianization_ and [[derived scheme|derivation]] of the category of [[scheme]]s:

a _motive_ is a complex of sheaves on a category whose objects are [[scheme]]s, but whose morphism are certain [[correspondence]]s between [[scheme]]s (much like a [[groupoidification]] of the category of schemes).

## Definition ##


Associated to a [[Noetherian scheme]] $S$ there is a [[category]] $Cor_S$ of [[correspondence]]s of [[scheme]]s, whose

* [[object]]s are schemes of finite type over $S$;

* [[morphism]]s $Cor_S(X,Y)$ form an abelian group of cycles on the [[fiber product]] $X \times_S Y$ that are "universally integral relative to $X$" and each of whose components are finite and and surjective over $X$.

Details are in [appendix 1A](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=19) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html).

The [[triangulated category]] of **motives** over a [[field]] $k$ is... 

...defined for instance in [lecture 14, def 14.1](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html).

It is a [[localization]] of the [[derived category]] of (bounded) complexes of sheaves on this category of correspondences, $Cor_S$.
 
## Motivic cohomology ##

The derived [[hom-set]]s in the category of motives, at least between special objects, compute what is called [[motivic cohomology]].

See [prop. 14.16, p. 114](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=126) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html).

## related entries ##

* [[pure motive]]

* [[mixed motive]]

* [[Voevodsky motive]]

## References ##

Some pretty useful comments on motives ar at this MathOverflow thead:

* [What's the "Yoga of Motives?"](http://mathoverflow.net/questions/2146/whats-the-yoga-of-motives/2230#2230)

A formal discussion of motives can be found in [lecture 14](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of

* [[Carlo Mazza]], [[Vladimir Voevodsky]] and [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))

There is also

*  James S. Milne, [Motives -- Grothendieck's Dream](http://www.jmilne.org/math/xnotes/MOT.pdf)

*  Mihnyong Kim, [Classical Motives: Motivic $L$-functions](http://www.ucl.ac.uk/~ucahmki/ihes3.pdf)

* Bruno Kahn, [pdf slides](http://www.aimath.org/WWN/motivesdessins/PaloAlto1.pdf) on pure motives
