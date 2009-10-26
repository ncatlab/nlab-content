<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

In general, "folk model structures" are [[model category]] structures on the categories of some flavor of [[n-category|n-categories]] for $1\le n\le \infty$ (note that $n=\infty$ or $\omega$ is allowed).

While ultimately the collection of all [[n-category|n-categories]] should form an $(n+1)$-category, restricting that to just invertible higher morphisms will yield an [[(n,r)-category|(n+1,1)-category]]. So in general, given that $n$ may be $= \infty$, an [[(infinity,1)-category]].

A (folk) [[model category|model structure]] on the category of $n$-categories is a [[presentable (infinity,1)-category|presentation]] of this [[(infinity,1)-category]].


A _folk_ model structure is characterized by the fact that the [[(infinity,1)-category]] that it induces is really the expected one, in that [[weak equivalence|weak equivalences]] are the [[equivalence of categories|category-theoretic equivalences]].  

This is to be contrasted with [[Thomason model structure|Thomason model structures]] in which the weak equivalences are the morphisms that induce a [[model structure on simplicial sets|weak homotopy equivalence]] of [[nerve|nerves]].  This amounts to regarding each category, or rather its [[nerve]], as a placeholder for its _groupoidification_ (Kan fibrant replacement) and then considering the standard notion of equivalence.


In a folk model structure for some flavor of $n$-categories, usually

* a **fibration** is a functor that lifts [[equivalence|equivalences]] in all dimensions,
* an **acyclic fibration** is a functor which is [[k-surjective functor|k-surjective]] for all $0\le k\le n$,
* a **weak equivalence** is a functor which is [[k-surjective functor|essentially k-surjective]] for all $0\le k\le n$, and
* a **cofibration** is a functor which is injective on objects and "relatively free" on $k$-morphisms for $1\le k \lt n$.  These can also be described as the morphisms [[cofibrantly generated model structure|generated]] by the inclusions 
$\partial G_k \hookrightarrow G_k$ of the boundary of the $k$-[[globe]] into the $k$-[[globe]] for $0\le k \lt \infty$.

#References on particular cases#

* The folk model structure for 1-categories was known to experts for some time before being written down formally (hence the name).
   * It was apparently first published (for categories internal to a Grothendieck topos) by Joyal and Tierney, _Strong Stacks and Classifying Spaces_, Category theory (Como, 1990) Springer LNM 1488, 213-236.
   * A more elementary writeup by Charles Rezk can be found [here](http://www.math.uiuc.edu/~rezk/cat-ho.dvi).
   * A general internal version relative to a Grothendieck [[coverage]] can be found [here](http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html).
* The folk model structures for 2-categories and bicategories are due to Steve Lack.
   * _A Quillen Model Structure for 2-Categories_, K-Theory 26: 171&#8211;205, 2002. ([website](http://www.maths.usyd.edu.au/u/stevel/papers/qmc2cat.html))
   * _A Quillen Model Structure for Biategories_, K-Theory 33: 185-197, 2004. ([website](http://www.maths.usyd.edu.au/u/stevel/papers/qmcbicat.html))

* for $n = \omega$: 

   * Yves Lafont, Francois M&eacute;tayer, Krzysztof Worytkiewicz, _A folk model structure on omega-cat_ ([arXiv](http://arxiv.org/abs/0712.0617))

* for $n = \omega$ and all morphisms invertible, there is the [[model structure on strict omega-groupoids]]: 

   * R. Brown and M. Golasinski, _A model structure for the homotopy theory of crossed complexes_, Cah. Top. G&eacute;om. Diff. Cat. 30 (1989) 61-82 ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/RB-golskyrev.pdf))

#Internalization#

A common problem is to transport the (a) model structure on plain $\omega$-categories, i.e. $\omega$-categories [[internal category|internal to]] $Sets$ to another [[internalization|internal context]], notably for the case that $Sets$ is replaced with some kind of category of $Spaces$. This is relevant for the discussion of the homotopy theory of topological and smooth $\omega$-categories.

Usually, such internalization of model structures has the consequence that some properties invoked in the description of the original model structure, notably some of the lifting properties, will only continue to hold "locally".  One way to deal with this is to pass to a notion slightly weaker than that of a [[homotopy theory|model category]] called a [[category of fibrant objects]] as used in [[homotopical 
cohomology theory]].

But there are also full model structures for such situations. Notice that under a suitable [[nerve]] operation all [[n-category|n-categories]] usually embed into [[simplicial set]]s. The [[models for infinity-stack (infinity,1)-toposes]] given by the [[model structure on simplicial presheaves]] then serves to present the corresponding $(\infty,1)$-category of parameterized or internal $n$-categories. See for instance also [[smooth infinity-stack]].

#Cofibrant resolutions#


In 

* F. M&eacute;tayer, _Cofibrant complexes are free_ ([arXiv](http://arxiv.org/abs/math.CT/0701746))


it is shown that _cofibrant_ $\omega$-categories with respect to the folk model structure are precisely the "free" ones, where "free" here means "generated from a polygraph" as described in 

* F. M&eacute;tayer, _Resolutions by polygraphs_ ([tac](http://www.tac.mta.ca/tac/volumes/11/7/11-07.pdf))

(Polygraphs are equivalent to [[computad|computads]].)

We had some blog discussion about this at
[Freely generated omega-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html).
