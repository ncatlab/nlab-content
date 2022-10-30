
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _KR-theory_ ([Atiyah 66](#Atiyah66)) is variant of [[topological K-theory]] on [[spaces]] equipped with a $\mathbb{Z}_2$-[[action]] (by [[homeomorphism]], hence equipped with one [[involution|involutive]] homeomorphism -- a "[[real space]]").

In terms of [[cocycle]] models, classes of KR-theory are represented by [[complex vector bundles]] over $X$ on which the involution on their base space lifts to an _anti-linear_ involution of the total space. Over manifolds with trivial involution these are precisely the [[complexification]] of [[real vector bundles]] and hence over such spaces $KR$-theory reduces to [[KO]]-[[cohomology theory|theory]]. Conversely, over two copies $X \cup X$ lof $X$ equipped with the involution that interchanges the two, $KR$-theory reduces to [[KU]]-[[cohomology theory|theory]]. Finally over $X \times S^1$ with the involution the antipodal identification on the second ([[circle]]) factor , $KR$-theory reduces to the self-conjugate [[KSC-theory]] ([Anderson 64](#Anderson64)). So in general $KR$-theory interpolates between all these cases. For instance on $X \times S^1$ with the reflection-involution on the circle it behaves like $KO$-theory at the two involution fixed points (the two [[O-planes]]) and like $KU$ in their complement (a model that makes this very explicit is given in [DMR 13, section 4](#DMR13)).

More abstractly, complex conjugation of complex vecgtor bundles induces on the [[complex K-theory]] [[spectrum]] [[KU]] an involutive [[automorphism]]. $KR$ is the corresponding $\mathbb{Z}_2$-[[equivariant spectrum]], and $KR$-theory the corresponding $\mathbb{Z}_2$-[[equivariant cohomology]] theory.  In particular, the [[homotopy fixed point]] of [[KU]] under this automorphism is [[KO]]

$$
  KO \simeq (KU)^{\mathbb{Z}/2}
$$

and this way where in complex K-theory one has [[KU]]-[[modules]] ([[∞-modules]]), so in KR-theory one has $KO$-modules.

KR is an example of a [[real-oriented cohomology theory]], together with for instance [[MR-theory]] and [[BPR-theory]].

+-- {: .num_remark}
###### Remark on terminology

Hence $X$ here is equipped with an [[involution]] by a [[diffeomorphism]]. In this context this is often thought of as a non-linear [[real structure]] and so these spaces are called "real spaces". Following this, $KR$-theory is usually pronounced "real K-theory". But **beware** that this terminology easily conflicts with or is confused with [[KO]]-theory. For disambiguation the latter might better be called "orthogonal K-theory". But on abstract grounds maybe $KR$-theory would best be just called $\mathbb{Z}_2$-equivariant complex K-theory.

=--


## Related concepts

* [[real-oriented cohomology theory]]

  * [[MR-theory]]

  * [[BPR-theory]]

* [[orientifold]]

* [[KO-dimension]]

[[!include chromatic tower examples - table]]

[[!include string theory and cohomology theory -- table]]

## References

KR theory was introduced in

* {#Atiyah66} [[Michael Atiyah]], _K-theory and reality_, The Quarterly Journal of Mathematics. Oxford. Second Series 17 (1) (1966),: 367&#8211;386, doi:10.1093/qmath/17.1.367, ISSN 0033-5606, MR 0206940

The version of $KSC$-theory was introduced in 

* {#Anderson64} D. W. Anderson, _The real K-theory of classifying spaces_ Proc. Nat. Acad. Sci. U. S. A., 51(4):634&#8211;636, 1964.

The dual concept of KR-homology was defined in

* [[Gennady Kasparov]], _The operator K-functor and extensions of $C^\ast$-algebras,_ Izv. Akad. Nauk. SSSR Ser. Mat. 44, 571-636 (1980).

Further discussion includes

* [[Johan Dupont]], _Symplectic bundles and $KR$-theory_ (1967) ([pdf](http://www.mscand.dk/article.php?id=1908))

Reviews include

* Wikipedia, _[KR-theory](http://en.wikipedia.org/wiki/KR-theory)_

Discussion more in abstract [[stable homotopy theory]] and [[equivariant stable homotopy theory]] is in 

* Paolo Masulli, _Equivariant homotopy: $KR$-theory_, Master thesis (2011) ([pdf](http://www.math.ku.dk/~jg/students/masulli.msthesis.2011.pdf))

* [[Daniel Dugger]], _An Atiyah-Hirzebruch spectral sequence for $KR$-theory_ ([arXiv:0304099](http://arxiv.org/abs/math/0304099))

Remarks on homotopy-theoretic KR in the context of [[algebraic K-theory]] are in

* [[Vigleik Angeltveit]], [[Andrew Blumberg]], Teena Gerhardt, Michael Hill, _Algebraic K-theory and equivariant homotopy theory_, 2012 ([pdf](http://www.birs.ca/workshops/2012/12w5116/report12w5116.pdf))



Explicit [[groupoid]]/[[stack]] models for equivariant and twisted KR-theory theory are discussed in

* El-ka&#239;oum M. Moutuou, _Twistings of KR for Real groupoids_ ([arXiv:1110.6836](http://arxiv.org/abs/1110.6836))

* {#Freed12} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_, lectures at ESI Vienna, 2012 ([[FreedESI2012.pdf:file]])

This is with motivation from _[[orientifolds]]_, see the references given there for more. A long list of computations of twisted $KR$-classes on tori with applications to [[T-duality]] on [[orientifolds]] is in

* {#DMR13} Charles Doran, Stefan Mendez-Diez, [[Jonathan Rosenberg]], _T-duality For Orientifolds and Twisted KR-theory_ ([arXiv:1306.1779](http://arxiv.org/abs/1306.1779))

[[!redirects KR-homology]]

[[!redirects KR-theory]]