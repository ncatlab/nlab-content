
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The notion of _virtual fundamental class_ is a generalization of that of _[[fundamental class]]_ from [[manifolds]] to more general spaces in [[higher geometry]], notably to [[orbifolds]] and their equivalent incarnations as [[stacks]], as well as to [[derived manifolds]].

This plays a central role when these stacks serve as [[moduli stacks]] for certain structures on some space (certain maps into that space regarded as a [[target space]], notably) and one is interested in the relevant "[[path integral]]" over all these structures (to produce [[invariants]] of target space). This is manifestly so for instance in the application to [[Gromov-Witten invariants]]. In these cases the pairing of [[cocycles]] against the virtual fundamental class plays the role of [[integration]] over the given moduli stack.



## Examples

### Moduli space of stable maps
 {#ModuliSpaceOfStableMaps}

Although the [[moduli space]] of [[stable maps]] is sometimes referred to as a compactifiaction of the space of maps, in analogy with the [[Deligne-Mumford compactification]] of the [[moduli space]] of curves, in
fact it typically has boundary components of higher dimension than the space it was supposed to compactify!

Take for example $\bar M_{1,0}(P^2,3)$.  It ought to be a compactification of the space of degree-3 maps from genus-1 curves to $P^2$, and indeed one of its components has a Zariski open subset birational to the $P^9$ of all plane cubics.  But there is also a 'boundary component' of
higher dimension, namely the boundary component consisting of maps whose domain is a genus-1 curve glued to a nodal rational curve: the nodal curve maps to a rational cubic in $P^2$, while the $g=1$ component contracts to a point on that nodal cubic.  

This boundary component has
dimension 10: namely, there are 8 parameters to specify the image nodal cubic, 1 paramenter to determine the point to which the $g=1$ component contracts, and finally there is 1 paramenter for the
[[j-invariant]] for the $g=1$ component.  The topological fundamental class lives in dimension 10 so it is rather useless to integrate against if all your cohomology classes are codimension 9 --- which is the
expected dimension.  

The virtual fundamental class always lives in the
expected dimension.

(The expected dimension is often the one you would expect(!) from
naive counts like the above.  More formally it can be computed as dim
$H^0(C,N_f)$, where $f:C\to P^2$ is a moduli point (with [[normal bundle]]
$N_f$) such that $H^1(C,N_f)=0$ (this is to say that the first order [[infinitesimal space|infinitesimal]] deformations are unobstructed).)

The situation is analogous (possibly in fact a special case of) the standard situation in intersection theory when a section of a [[vector bundle]] is not regular: its zero locus is then of too high dimension
and is of little use to intersect against.  The correct class to work with is then the top [[Chern class]] of the vector bundle (cf.
[Fulton] ch.14), which could be called the virtual class of the zero locus.

In the example above, I don't know right now if the virtual class in fact appears as a top Chern class of a vector bundle --- I think it should, because the excess is just a variation of the standard example $\bart M_{1,1}(X,0)$, and in that example it is true that the virtual class appears as a top [[Chern class]]: there is a so-called [[obstruction bundle]] which in this case is the dual of the [[Hodge bundle]]
from the factor $\bar M_{1,1}$ tensored with the [[tangent bundle]] from $X$.

(The Hodge bundle is the direct image bundle of the canonical bundle of the universal curve, hence of rank $g$, hence just a line bundle in this case.)  

The virtual fundamental class is the top Chern class of
the obstruction bundle (cap the topological fundamental class).

In this case, $dim \bar M_{1,1}(X,0) = 1 + dim X$, and the obstruction bundle has rank $dim X$, hence the virtual class has dimension 1.


Perhaps it should be mentioned also that the moduli space of maps can have components of too high dimension even before it is 'compactified', and even without involving contracting curves.  A
famous example is $M_{0,0}(Q,d)$ (no bar needed for this argument) where
$Q$ is a quintic three-fold.  Let's say $d=2$, so we are talking about conics on the quintic three-fold.  Since $Q$ has trivial [[canonical class]] it follows that the expected dimension is always 0 (i.e. in every
degree there ought to be a finite number of rational curves on Q).

But now, $M_{0,0}(Q,2)$ is a space of maps, not a space of curves, and for every one of the famous 2875 lines on $Q$ there is a 2-dimensional family of double covers of the line, which clearly count as stable
degree-2 maps, so $M_{0,0}(Q,2)$ contains 2875 components of dimension 2, in contrast to the virtual dimension 0.


## Related entries

* [[fundamental class]]

* [[Poincaré duality algebra]]

* Virtual fundamental classes play a central role in the theory of [[Gromov-Witten invariants]].

## References

The idea of virtual fundamental classes and corresponding picture of derived moduli spaces comes from

* [[Maxim Kontsevich]], _Enumeration of rational curves via torus actions_, in: The moduli space of curves (Texel Island, 1994), 335&#8211;368, Progr. Math. __129__, Birkh&#228;user 1995. MR1363062 (97d:14077), [hep-th/9405035](http://arxiv.org/abs/hep-th/9405035)

A quick overview of virtual fundamental classes for [[algebraic stacks]] is in section 4.4.3 of 

* [[Bertrand Toën]], _Higher and derived stacks: a global overview_ ([arXiv:math/0604504](http://arxiv.org/abs/math/0604504))

A more detailed overview with many pointers to the literature is in section 8 "Introduction to the virtual fundamental class" of

* Nicola Pagani, _Introduction to Gromov-Witten theory and quantum cohomology_ ([pdf](http://www2.iag.uni-hannover.de/~pagani/DOC/corsogw.pdf))

A review of virtual fundamental classes of [[orbifolds]] in [[differential geometry]] is around page 7 of 

* Andr&#233;s Angel, _When is a differentiable manifold the boundary of an orbifold?_ ([pdf](http://ems.math.uni-bonn.de/people/aangel79/files/boundary.pdf))

Detailed disucssion for the [[branched manifold]]-variant of [[orbifolds]] is in section 3.4 of 

* [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_ ([arXiv:math/0509664](http://arxiv.org/abs/math/0509664))

Virtual fundamental classs of [[derived manifolds]] are discussed in section 13.2 of 

* [[Dominic Joyce]], _D-manifolds and d-orbifolds: a theory of derived differential geometry_ ([pdf](http://people.maths.ox.ac.uk/joyce/dmbook.pdf))

Specifically for applications to [[Gromov-Witten theory]] see for instance

* Ch. Okonek, A. Teleman, _Computing virtual fundamental classes: gauge theoretical Gromov-Witten invariants for toric varieties_ ([arXiv:math/0205137](http://arxiv.org/abs/math/0205137))

The material in _[Moduli space of stable maps](#ModuliSpaceOfStableMaps)_ above originates in a blog discussion [here](http://golem.ph.utexas.edu/category/2009/09/a_seminar_on_gromovwitten_theo.html#c027000)

