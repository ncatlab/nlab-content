
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In general, **canonical model structures** are [[model category]] structures on the categories of some flavor of [[n-category|n-categories]] for $1\le n\le \infty$ (note that $n=\infty$ or $\omega$ is allowed), which are intended to capture the correct "categorical" theory of these categories.

The archetypical examples are 

* the _[[canonical model structure on categories]]_ 

* the _[[canonical model structure on groupoids]]_. 

In [[categorification]] of these, one has 

* [[canonical model structures on 2-categories]].

Canonical model structures are sometimes called "folk" model structures, but the appropriateness of this term is [questionable](https://nforum.ncatlab.org/discussion/649), especially in the cases $n \gt 1$.  Other alternatives are 'endogenous', 'standard', 'natural', and 'categorical'.

While ultimately the collection of all [[n-category|$n$-categories]] should form an $(n+1)$-category, restricting that to just invertible higher morphisms will yield an [[(n,r)-category|(n+1,1)-category]], and thus in particular an [[(∞,1)-category]].  It is this (∞,1)-category which is intended to be [[presentable (infinity,1)-category|presented]] by a canonical model structure.  In particular, the [[weak equivalences]] in a canonical model structure should be the [[equivalence of categories|category-theoretic equivalences]].  

This is to be contrasted with [[Thomason model structure|Thomason model structures]] in which the weak equivalences are the morphisms that induce a [[model structure on simplicial sets|weak homotopy equivalence]] of [[nerve|nerves]].  This amounts to regarding each category, or rather its [[nerve]], as a placeholder for its _groupoidification_ (Kan fibrant replacement) and then considering the standard notion of equivalence.


In a canonical model structure for some flavor of $n$-categories, usually

* a **fibration** is a functor that lifts [[equivalence|equivalences]] in all dimensions,
* an **acyclic fibration** is a functor which is [[k-surjective functor|k-surjective]] for all $0\le k\le n$,
* a **weak equivalence** is a functor which is [[k-surjective functor|essentially k-surjective]] for all $0\le k\le n$, and
* a **cofibration** is a functor which is injective on objects and "relatively free" on $k$-morphisms for $1\le k \lt n$.  These can also be described as the morphisms [[cofibrantly generated model structure|generated]] by the inclusions 
$\partial G_k \hookrightarrow G_k$ of the boundary of the $k$-[[globe]] into the $k$-[[globe]] for $0\le k \lt \infty$.




## Internalization

A common problem is to transport the (a) model structure on plain $\omega$-categories, i.e. $\omega$-categories [[internal category|internal to]] $Sets$ to another [[internalization|internal context]], notably for the case that $Sets$ is replaced with some kind of category of $Spaces$. This is relevant for the discussion of the homotopy theory of topological and smooth $\omega$-categories.

Usually, such internalization of model structures has the consequence that some properties invoked in the description of the original model structure, notably some of the lifting properties, will only continue to hold "locally".  One way to deal with this is to pass to a notion slightly weaker than that of a [[homotopy theory|model category]] called a [[category of fibrant objects]] as used in [[homotopical 
cohomology theory]].

But there are also full model structures for such situations. Notice that under a suitable [[nerve]] operation all [[n-category|n-categories]] usually embed into [[simplicial set]]s. The [[models for infinity-stack (infinity,1)-toposes]] given by the [[model structure on simplicial presheaves]] then serves to present the corresponding $(\infty,1)$-category of parameterized or internal $n$-categories. See for instance also [[smooth infinity-stack]].

## Cofibrant resolutions


In 

* [[Francois Métayer]], _Cofibrant complexes are free_ ([arXiv](http://arxiv.org/abs/math.CT/0701746))


it is shown that _cofibrant_ $\omega$-categories with respect to the canonical model structure are precisely the "free" ones, where "free" here means "generated from a [[polygraph]]" as described in 

* [[Francois Métayer]], _Resolutions by [[polygraphs]]_ ([tac](http://www.tac.mta.ca/tac/volumes/11/7/11-07.pdf))

We had some blog discussion about this at
[Freely generated omega-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html).

## Related concepts

* [[basic localizer]]

* [[canonical model structure on Cat]]

* [[canonical model structure on Grpd]]

* [[canonical model structure on 2Cat]]

* [[canonical model structure on Operad]]

* [[model structure on strict omega-categories]]

* [[2-trivial model structure]]


## References
 {#References}

The [[canonical model structure on categories]] was known to experts for some time before being written down formally (this is the origin of the adjective "folk", as in "[[folklore]]").

The [[canonical model structure on groupoids]] is claimed (but not proven)

* {#Anderson78} [[Donald W. Anderson]], p. 783 (12 of 37) in: *Fibrations and geometric realization*,  Bull. Amer. Math. Soc. **84** 5 (1978) 765-788 &lbrack;[euclid:1183541139](http://projecteuclid.org/euclid.bams/1183541139)&rbrack;

A published proof of this and the [[canonical model structure on categories]], in the further generality of [[internal category|categories internal]] to a [[Grothendieck topos]] (hence of [[2-sheaves]]) is due to

* {#JoyalTierney91} [[André Joyal]], [[Myles Tierney]], Thm. 2 (p. 221) *Strong stacks and classifying spaces*, in: *Category Theory* Lecture Notes in Mathematics **1488**, Springer (1991) 213-236 &lbrack;[doi:10.1007/BFb0084222](https://doi.org/10.1007/BFb0084222)&rbrack;

and more elementary proofs for the plain case (internal to [[Set]]) are given in

* [[Charles Rezk]], *A model category for categories* (1996) &lbrack;[dvi](http://www.math.uiuc.edu/~rezk/cat-ho.dvi), [[Rezk_ModelCategoryForCategories.pdf:file]]&rbrack;

* [[André Joyal]], _[[joyalscatlab:Model structures on Cat]]_ (2010)

and (for the [[canonical model structure on groupoids|case of groupoids]]) in

* {#Strickland00} [[Neil Strickland]], §6.1 of: _$K(n)$-local duality for finite groups and groupoids_ , Topology **39** 4 (2000) &lbrack;[arXiv:math/0011109](https://arxiv.org/abs/math/0011109), <a href="https://doi.org/10.1016/S0040-9383(99)00031-2">doi:10.1016/S0040-9383(99)00031-2</a>&rbrack;

Further generalization to [[internal category|categories internal]] to [[finitely complete categories]]:

* [[Tomas Everaert]], [[Rudger W. Kieboom]], [[Tim Van der Linden]], _Model structures for homotopy of internal categories_, Theory and Applications of Categories,  Vol. 15, CT2004, No. 3, pp 66-94. ([tac:15-03](http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html)).

though it seems that the assumptions in this article apply to ambient categories that are [[semiabelian categories]], but do not apply to ambient categories like [[Top]].

A brief summary, together with a generalization when one assumes only weaker versions of the [[axiom of choice]], can be found at _[[folk model structure on Cat]]_.

The [[canonical model structure on 2-categories|canonical model structures for 2-categories and bicategories]] are due to 

* [[Steve Lack]],

  _A Quillen Model Structure for 2-Categories_, K-Theory 26: 171&#8211;205, 2002. ([website](http://web.science.mq.edu.au/~slack/papers/qmc2cat.html))
   
  _A Quillen Model Structure for Bicategories_, K-Theory 33: 185-197, 2004. ([website](http://web.science.mq.edu.au/~slack/papers/qmcbicat.html))

and for $n=3$ ([[Gray-categories]]) in

* [[Steve Lack]], _A Quillen model structure for Gray-categories_ ([arxiv:1001.2366](http://arxiv.org/abs/1001.2366))

For $n = \omega$ ([[strict omega-categories]])

* [[Yves Lafont]], [[Francois Métayer]], Krzysztof Worytkiewicz, _A folk model structure on omega-cat_ ([arXiv](http://arxiv.org/abs/0712.0617))

For $n = \omega$ and all morphisms invertible, there is the [[model structure on strict omega-groupoids]]: 

* [[Ronnie Brown]] and M. Golasinski, _A model structure for the homotopy theory of crossed complexes_, Cah. Top. G&#233;om. Diff. Cat. 30 (1989) 61-82 ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/RB-golskyrev.pdf))

* [[Dimitri Ara]], [[Francois Metayer]], _The Brown-Golasinski model structure on ∞-groupoids revisited_ (pdf) Homology, Homotopy Appl. 13 (2011), no. 1, 121&#8211;142.


[[!redirects canonical model structures]]

[[!redirects folk model structure]]
[[!redirects folk model structures]]

[[!redirects natural model structure]]
[[!redirects natural model structures]]



