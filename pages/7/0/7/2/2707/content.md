
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The similarity of the behaviour of various cohomologies of varieties over a field suggest that there is a universal among them with values in an intermediate [[abelian category]], called the category of motives. Thus we should have variety $X$, which maps to its motive $M(X)$ and good cohomologies would factor through that projection. Of course, not every motive is the image of a single variety. There is supposedly also a version with further filtrations (need to be more specific), the mixed motives. 

So far there are realizations of [[pure motive]]s, and only a derived version of mixed motives. Constructions depend much on weather we work in prime characteristics or in characteristics zero. Part of the formalism involves more general schemes than varieties. 

Another crucial idea leading to the motives is that the various cohomologies lead to the same pieces of information; therefore there is a symmetry related to this, which is of Galois nature. For example, over complex numbers one can compare the Betti cohomology and de Rham cohomology "realizations". Thus one has a motivic Galois group, and as usually with representations one has a tensor category structure which is also rigid. Thus one has in fact an abelian tensor category of motives. The Tannakian reconstruction plays a major role; for the pure motives we have the neutral Tannakian categories and for the mixed motives mixed Tannakian categories. Functions on the torsor of the isomorphism between "realizations" correspond to the matrices of [[period]]s in Hodge theory. 

The category of motives is roughly something like an _abelianization_ and [[derived scheme|derivation]] of the category of [[scheme]]s:

a _motive_ is sometimes realized as a complex of sheaves on a category whose objects are [[scheme]]s, but whose morphism are certain [[correspondence]]s between [[scheme]]s (much like a [[groupoidification]] of the category of schemes).

L-functions (and zeta functions in particular) of varieties are also invariants of their motives. Langlands program indirectly involves motives; in particular its essential part can be expressed as a general modularity conjecture relating L-functions to automorphic functions. Most of the deep properties of elliptic curves are of motivic nature, and in particular a major step of the proof of Fermat's last theorem by Wiles and Taylor can be interpreted as proof of a special case of modularity conjecture (for elliptic curves). 

## Voevodsky's motives ##


Associated to a [[Noetherian scheme]] $S$ there is a [[category]] $Cor_S$ of "finite" [[correspondence]]s of [[scheme]]s, whose

* [[object]]s are schemes of finite type over $S$;

* [[morphism]]s $Cor_S(X,Y)$ form an abelian group of cycles on the [[fiber product]] $X \times_S Y$ that are "universally integral relative to $X$" and each of whose components are finite and and surjective over $X$.

Details are in [appendix 1A](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=19) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html).

The [[triangulated category]] of **motives** over a [[field]] $k$ is... 

...defined for instance in [lecture 14, def 14.1](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html).

It is a [[localization]] of the [[derived category]] of (bounded) complexes of sheaves on this category of correspondences, $Cor_S$.
 
## Motivic cohomology ##

The derived [[hom-set]]s in the category of motives, at least between special objects, compute what is called [[motivic cohomology]].

See [prop. 14.16, p. 114](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=126) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html).

##Nori motives##

Madham Nori has an approach to the theory of motives based on a peculiar kind of Tannakian reconstruction so called Nori Tannakian theorem. 

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

[[!redirects category of motives]]