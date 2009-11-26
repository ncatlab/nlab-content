#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

The similarity of the behaviour of various [[cohomologies]] of [[algebraic variety|varieties]] over a field suggest that there is a universal one among them with values in an intermediate [[abelian category]], called the category of _motives_. Thus we should have a variety $X$, which maps to its motive $M(X)$, and good cohomologies would factor through that projection. Of course, not every motive is the image of a single variety. There is supposedly also a version with further filtrations (need to be more specific), the [[mixed motive]]s. 

So far there are realizations of [[pure motive]]s, and not of the mixed motives. However there are several equivalent definitions of a triangulated tensor category which has all conjectured structural properties of the derived category of mixed motives (except t-structure which would manifestly make it a derived category); hence it is denoted $D(\mathcal{M M})$.

Constructions of motives depend much on whether we work in prime [[characteristic]]s or in characteristic zero. Part of the formalism involves more general schemes than varieties. 

Another crucial idea leading to motives is that the various cohomologies lead to the same pieces of information; therefore there is a symmetry related to this, which is of Galois nature. For example, over the [[complex numbers]] one can compare the [[Betti cohomology]] and [[de Rham cohomology]] "realizations". Thus one has a motivic [[Galois group]], and as usually with representations one has a [[tensor category]] structure which is also [[rigid monoidal category|rigid]]. Thus one has in fact an [[monoidal abelian category|abelian tensor category]] of motives. The Tannakian reconstruction plays a major role; for pure motives we have neutral [[Tannakian category|Tannakian categories]], and for mixed motives we have mixed Tannakian categories. Functions on the [[torsor]] of the isomorphism between "realizations" correspond to the matrices of [[period]]s in [[Hodge theory]]. 

The category of motives is roughly something like an _abelianization_ and [[derived scheme|derivation]] of the category of [[scheme]]s:
a _motive_ is sometimes realized as a [[complex]] of [[sheaf|sheaves]] on a category whose objects are [[scheme]]s, but whose morphism are certain [[correspondence]]s between schemes (much like a [[groupoidification]] of the category of schemes).

$L$-functions (and $\zeta$-functions in particular) of varieties are also invariants of their motives. The [[Langlands program]] indirectly involves motives; in particular its essential part can be expressed as a general modularity conjecture relating $L$-functions to automorphic functions. Most of the deep properties of [[elliptic curve]]s are of motivic nature, and in particular a major step of the proof of [[Fermat's last theorem]] by Wiles and Taylor can be interpreted as a proof of a special case of the modularity conjecture (for elliptic curves). 


## Voevodsky motives ##

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

[[Madham Nori]] has an approach to the theory of motives based on a peculiar kind of Tannakian reconstruction, the so called _Nori's Tannakian theorem_. 


## Related entries##

* [[pure motive]]

* [[mixed motive]]

* [[Voevodsky motive]]


##Extensions##

Correspondences are interesting in [[noncommutative geometry]] of the [[operator algebra]] flavour. For example, KK-groups are in fact themselves sort of correspondences; Connes and Skandalis had an early reference very much paralleling some ideas from the algebraic world. More recently, motives in the operator algebraic setup have been approached by Connes, Marcolli and others. 

In derived [[noncommutative algebraic geometry]] based on $A_\infty$-categories, Kontsevich proposed a theory of [[noncommutative motive]]s. 

In [[birational geometry]], Bruno Kahn defined the appropriate version. In [[rigid analytic geometry]], $A^1$-homotopy theory is replaced by $B^1$-homotopy theory and the appropriate analogue of the Voevodsky's category of mixed motives has been constructed; the construction follows the same basic pattern. 


## References ##

Some pretty useful comments on motives are at this MathOverflow thead:

* [What's the "Yoga of Motives?"](http://mathoverflow.net/questions/2146/whats-the-yoga-of-motives/2230#2230)

A formal discussion of motives can be found in [lecture 14](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of

* [[Carlo Mazza]], [[Vladimir Voevodsky]] and [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))

There is also

*  James S. Milne, [Motives -- Grothendieck's Dream](http://www.jmilne.org/math/xnotes/MOT.pdf)

*  Mihnyong Kim, [Classical Motives: Motivic $L$-functions](http://www.ucl.ac.uk/~ucahmki/ihes3.pdf)

* Bruno Kahn, [pdf slides](http://www.aimath.org/WWN/motivesdessins/PaloAlto1.pdf) on pure motives


[[!redirects category of motives]]