
#Contents#
* table of contents
{:toc}

## Idea

KK-theory is a "bivariant" version of [[operator K-theory]]: for $A, B$ two [[operator algebras]], the _KK-group_ $KK(A,B)$ is an equivalence class of $\mathbb{Z}_2$-[[graded vector space|graded]] $(A,B)$-[[Hilbert bimodules]] $\mathcal{H}$ equipped with a an adjointable founded operator $F \in \mathcal{B}_A(\mathcal{H})$ such that $\pi(a)(F^2 - 1) \in \mathcal{K}_A(\mathcal{H})$ and $[\pi(a), F] \in \mathcal{K}_A(\mathcal{H})$ for all $a \in A$

These KK-groups $KK(A,B)$ behave in the first argument as K-homology of $A$ and in the second as K-cohomology of $B$.


There is a [[stable (infinity,1)-category]] and in particular a [[triangulated category]] of operator algebras such that $KK(-,-)$ is the [[hom-set]] of the corresponding [[homotopy category]] ([Lean](#Lean))

Accordingly, the groups $KK(A,B)$ are now viewed as a "correct" hom-set among noncommutative operator algebras for the purpose of various homotopy-invariant functors. 

KK-theory was introduced by [[Gennady Kasparov]] in 1980, prompted by the advances in [[Brown-Douglas-Fillmore theory]], especially in the last 1977 article.

## Related concepts

* [[operator K-theory]]

  * [[E-theory]]

## References

The original article is

* [[Gennady Kasparov]], _The operator $K$-functor and extensions of $C^{\ast}$-algebras_, Izv. Akad. Nauk SSSR Ser. Mat. __44__  (1980), no. 3, 571&#8211;636, 719, [MR81m:58075](http://www.ams.org/mathscinet-getitem?mr=582160), [Zbl](http://www.zentralblatt-math.org/zmath/search/?an=Zbl%200464.46054%7CZbl%200448.46051), [abstract](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=im&paperid=1739&option_lang=eng), [english doi](http://dx.doi.org/10.1070%2FIM1981v016n03ABEH001320), free Russian original: [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=1739&volume=44&year=1980&issue=3&fpage=571&what=fullt&option_lang=eng)

A brief survey with an eye towards [[representation of a C-star algebra|C-star representations]] of [[groupoid convolution algebras]] is in 

* [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) [pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf)
 {#Bos}

The underlying [[triangulated category]] of KK-theory is discussed in 

* [[Ralf Meyer]], _KK-theory as a triangulated category_ (2009) ([pdf](http://wwwmath.uni-muenster.de/u/echters/Focused-Semester/lecturenotes/Meyer_--_KK-theory_as_a_triangulated_category.pdf))

* Rohan Lean, to appear [pdf]()
 {#Lean}
