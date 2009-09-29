# Idea #

For any $n$, the category $Str n Cat$ of [[strict n-categories]] is [[cartesian closed category|cartesian closed]].  If $C$ and $D$ are strict $n$-categories, the objects of the [[exponential object]] $D^C$ are strict $n$-functors $C\to D$, its morphisms are *strict* $n$-natural transformations, and likewise its higher cells are *strict* higher [[transfors]].

On the other hand, one expects the weak $(n+1)$-category $n Cat$ of [[weak n-categories]] to be cartesian closed in the $(n+1)$-categorical sense, so that one has equivalences of hom-$n$-categories
\[n Cat(C\times D, E) \simeq n Cat(C, Hom(D,E)).\]
In this case, $Hom(D,E)$ should consist of weak functors, pseudo transformations (which are natural up to coherent [[equivalence]]), and pseudo higher transfors.  Note that although $C\times D$ (probably) means the same thing in the strict and weak worlds, $D^C$ and $Hom(D,E)$ are not the same, and in general not even [[equivalence of categories|equivalent]].

Gray tensor products are part of the general philosophy of trying to understand weak higher structures without getting bogged down in the theory of weaker higher-er structures.  One instance of this philosophy is the use of [[model categories]] (or more general types of [[homotopy theory]]) to use strict functors to model weak ones. Although not every weak functor is equivalent to a strict one (already when $n=2$), one expects this to become true if the domain is suitably [[cofibrant object|cofibrant]].  This is a theorem for small values of $n$ and can be regarded as a definition of "weak functor" for large values of $n$; see the [[folk model structure]] for 2-categories and [this paper](http://www.dpmms.cam.ac.uk/~rhgg2/Womaps/Womaps.html).

Gray tensor products attempt to extend this to deal with weak $k$-transfors for $k\gt 0$, starting with pseudo (or lax or oplax) natural transformations, by equipping higher categories of some sort with a non-cartesian [[monoidal category|monoidal]] and/or [[closed category|closed]] structure.  This began with John Gray, who showed that the category $Str2Cat$ is a non-symmetric [[closed monoidal category]] in which one internal-hom $Lax(C,D)$ consists of [[strict 2-functors]], [[lax natural transformations]], and [[modifications]] (the other contains oplax transformations instead).  A straightforward modification produces a closed symmetric monoidal structure based on *pseudo* natural transformations; the monoidal product is now called the [[Gray tensor product]].

Later various authors constructed analogous tensor products for [[strict ∞-categories]] and strict &#969;-groupoids, here called the [[Crans-Gray tensor product]].  Here the internal-homs consists of strict $\omega$-functors and lax/oplax $k$-transfors for $k\gt 0$.  (It appears to be unknown whether there is a pseudo version.)


# The Problem #

The (pseudo version of the) Gray tensor product of 2-categories is used to define [[Gray-categories]], which are a version of [[semistrict n-category|semistrict]] 3-categories.  This is very convenient because Gray-categories are just [[enriched category|categories enriched]] over $(Str2Cat,\otimes_{Gray})$, so that all of enriched category theory applies to them (as it does to 2-categories, being categories enriched over $Cat$).  Thus, it is natural to hope that one might be able to iterate this process, defining a "Gray tensor product" of semistrict $n$-categories and then defining semistrict $(n+1)$-categories to be categories enriched over semistrict $n$-categories.

However, there is a problem:

* _No category $SS n Cat$ of [[algebraic definition of higher category|algebraic]] $n$-categories with weak [[interchange law|interchange]] and strict functors can admit a [[closed category|biclosed structure]] that contains non-strict transformations._

Now there are lots of adjectives in this statement; for now just notice that the progression "categories, 2-categories, Gray-categories, Gray-cat-categories?" *is* producing categories of algebraic $n$-categories with weak interchange and strict functors.  So if this no-go statement is true, then Gray-cat does not admit a biclosed structure of the desired sort, and Gray-cat-categories probably can't be defined correctly.

To see why this no-go statement holds, imagine some hypothetical algebraic notion of semistrict $n$-category with weak interchange, and consider what sort of transformation (that is, 1-transfor) we want to model.  Let $C$ and $D$ be semistrict $n$-categories and $F,G:C\to D$ (strict) functors; then a transformation $\alpha:F\to G$ should probably consist of

* components $\alpha_x: F(x) \to G(x)$,
* equivalences $\alpha_f: G(f) \circ \alpha_x \simeq \alpha_y F(f)$ for $f:x\to y$,
* and higher data,
* satisfying axioms.

Now the question is, how is $\alpha_{g f}$ related to the composite of $\alpha_g$ and $\alpha_f$?  For pseudonatural transformations between 2-categories, they are equal (both being 2-cells, there is no room for anything weaker).  For a "fully weak" notion of transformation in higher dimensions, one might expect them to be only equivalent---but for the sorts of transfors used in the internal-hom for the Crans-Gray tensor product of $\omega$-categories, it turns out that they are also *equal*.  In fact, if the transformations are to give us a biclosed category of $n$-categories and strict functors, it turns out that they *must* be equal.

Consider the following: a transformation $F\Rightarrow G: C\to D$ should be the same as a functor $2 \to [C,D]$ where $2$ is the [[interval category|interval]] $n$-category.  But if we are to have a closed category $SS n Cat$, giving such a functor should be equivalent to giving a functor $C\to [2,D]$.  (This doesn't depend on symmetry, but if things are not symmetric then $[-,-]$ means something different in the two cases.)  Now inspection of how this would work reveals that the relationship of $\alpha_{g f}$ to $\alpha_g$ and $\alpha_f$ in the first picture corresponds to the *functoriality* of $C\to [2,D]$ in the second picture.  That is, if $\alpha_{g f} = \alpha_g . \alpha_f$ (and so on) then the functor $C\to [2,D]$ is a strict functor, while if it is only equivalent, then $C\to [2,D]$ will be only a weak functor.  Hence, if we allow only strict functors, then all our transformations must be "semistrict" in the sense that $\alpha_{g f} = \alpha_g . \alpha_f$.

Now, however, we meet the second horn of the dilemma: in an $n$-category with weak interchange, semistrict transformations need not be composable!  Suppose that $\alpha: F \to G$ and $\beta: G\to H$ are semistrict transformations.  Then we can define the components of a transformation $\beta.\alpha:F\to H$ in the obvious way, but is it semistrict?  If you try to prove that it is, you'll find that you need a strict interchange law.  (There is a pentagon involving all the ways to compose a 2x2 grid of square 2-cells, a picture of which can be found in Crans' paper cited below.)  So we are stuck.

What can we do?  Well, for one thing, the theorem is only about *closed* structures, not about *monoidal* structures.  And Sjoerd Crans did manage to construct a non-closed "Gray-like" monoidal structure on Gray-cat.  But it's not clear whether the resulting notion of "Gray-cat-category" is in fact semistrict (i.e. whether arbitrary 4-categories could be strictified to them).

Another way to escape would be to allow weak functors.  This is not much good all by itself, since algebraic $n$-categories and weak functors do not generally form very good categories.  They don't have many limits and colimits, for one thing, and the theory of enriched categories isn't much good when the enriching category doesn't have limits and colimits.  However, if we instead use a [[geometric definition of higher category]], then we can get well-behaved 1-categories containing weak functors.  And it is known for many nonalgebraic notions of higher category that there are good Gray-like tensor products; in fact, in many cases it is actually the cartesian product (an important exception being the lax version of the [[Verity-Gray tensor product]] of weak complicial sets).  This is one reason why non-algebraic notions of higher category are very attractive.

Finally, a third escape that suggests itself would be to look for a notion of algebraic semistrict $n$-categories which nevertheless has strict interchange.  As far as I know, the only work on strictly interchanging semistrict categories is one nonalgebraic notion which depends on weak units.  The prospects for algebraic notions don't seem that appealing, however, since the whole idea of the Gray-approach was to build in the semistrictness via the iterated enrichment, but while it is easy to imagine weakening interchange this way, it is hard to see how this could produce strict interchange but weak units.

# References

* [[Sjoerd Crans]], _A tensor product for $Gray$-categories_ ([TAC](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html))

* [[Joachim Kock]], _Weak identity arrows in higher categories_ (semistrict categories with weak units): [math/0507116](http://arxiv.org/abs/math/0507116)


* [[Michael Batanin]], Denis-Charles Cisinski, Mark Weber, _Algebras of higher operads as enriched categories II_
([arXiv](http://arxiv1.library.cornell.edu/abs/0909.4715))