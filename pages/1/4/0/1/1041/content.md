
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


##Idea#

An abelian category is a natural abstraction and slight generalization of the category of abelian groups. It includes $R Mod$ where $R$ is a ring and the category of sheaves of abelian groups as the other principal motivating examples. In abelian categories, like in categories of modules over rings much of linear algebra and [[homological algebra]] makes sense.  Abelian category is one concept in a sequence of [[additive and abelian categories]].  

While significantly different from [[topos]]es, there is an intimate relation between abelian categories and toposes. See [[AT category]] for more on that.

##Definition#

An **abelian category** is a [[pre-abelian category]] satisfying the following equivalent conditions.

1. For every [[morphism]] $f$, the canonical morphism $\bar{f} : coker(ker(f)) \to ker(coker(f))$ (described at [[pre-abelian category]]) is an [[isomorphism]].

1. Every [[monomorphism|monic]] is a [[kernel]] and every [[epimorphism|epic]] is a [[cokernel]].


##Remarks#

* The two conditions are equivalent as follows. Assuming (1), when $f$ is monic we obtain $f\cong \ker(\coker(f))$ so that $f$ is a kernel, and dually; thus (1) implies (2).  The converse can be found in, among other places, Chapter VIII of [[Categories Work]].

* The notion of abelian category is self-dual: [[opposite category|opposite]] of any abelian category is abelian. 

* In an abelian category every morphism decomposes [[generalized the|uniquely up to a unique isomorphism]] into the composition of an [[epimorphism]] and a [[monomorphism]], via the above decomposition.  Since every monic is [[regular monomorphism|regular]], hence [[strong monomorphism|strong]], it follows that (epi, mono) is an [[orthogonal factorization system]].  Furthermore, again since every monic is regular, every abelian category is [[balanced category|balanced]].

* The $Ab$-enrichment of an abelian category need not be specified a priori.  If an arbitrary (not necessarily pre-additive) [[locally small category|locally small]] category $C$ has a [[zero object]], binary products and coproducts, kernels, cokernels and the property that every monic is a kernel arrow and every epi is a cokernel arrow (so that all monos and epis are [[normal monomorphism|normal]]), then it can be equipped with a unique addition on the morphism sets such that composition is bilinear and $C$ is abelian with respect to this structure.  However, in most examples, the $Ab$-enrichment is evident from the start and does not need to be constructed in this way.  (A similar statement is true for [[additive categories]], although the most natural result in that case gives only enrichment over abelian [[monoids]]; see [[semiadditive category]].)

* The last point is of relevance in particular for [[infinity-category|higher categorical]] generalizations of additive categories. See for instance [remark 2.14, p. 5](http://www.math.harvard.edu/~lurie/papers/DAG-I.pdf#page=5) of [[Jacob Lurie]]'s [[Stable Infinity-Categories]].

* The exactness properties of abelian categories have many features in common with exactness properties of [[topos|toposes]] or of [[pretopos|pretoposes]]. In a fascinating post to the categories mailing list, Peter Freyd gave a sharp description of the properties shared by these categories, introducing a new concept called [[AT categories]] (for "abelian-topos"), and showing convincingly that the difference between the A and the T can be concentrated precisely in the difference of the behavior of the initial object. 

## Examples

* Of course, [[Ab]] is abelian, as is the category of [[modules]] over any [[ring]].

* Therefore in particular the category [[Vect]] of vector spaces is an abelian category.

* The category of [[sheaves]] of abelian groups on any [[site]] is abelian.

* The category of torsion-free abelian groups is pre-abelian, but not abelian: the monomorphism $2:\mathbb{Z}\to\mathbb{Z}$ is not a kernel.


## Categories of $R$-modules 

There are some interesting results about the extent to which we can pretend any abelian category is a category of left $R$-[[module]]s for some [[ring]] $R$.  Let us write $R Mod$ for such a category of modules.  

First of all, it's easy to see that not every abelian category is equivalent to $R Mod$ for some ring $R$.  The reason is that $R Mod$ has all [[small category]] [[limits]] and [[colimits]].  The category of [[finitely generated module|finitely generated]] $R$-modules is an abelian category that lacks these properties.

However, we have

+-- {: .un_thm}
###### Mitchell's Embedding Theorem
Every small abelian category admits a [[full functor|full]], [[faithful functor|faithful]] and [[exact functor|exact]] functor to the category $R Mod$ for some ring $R$.
=--

+-- {: .proof}
###### Proof
This result can be found as Theorem 7.34 on page 150 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=176).  His terminology is a bit outdated, in that he calls an abelian category "fully abelian" if admits a full and faithful exact functor to a category of $R$-modules.  See also the [Wikipedia article](http://en.wikipedia.org/wiki/Mitchell%27s_embedding_theorem) for the idea of the proof.
=--

See also [[Freyd-Mitchell embedding theorem]].

We can also characterize which abelian categories _are_ equivalent to a category of $R$-modules:

+-- {: .un_thm}
###### Theorem
Let $C$ be an abelian category.  If $C$ has all [[small category|small]] [[coproducts]] and has a [[compact object|compact]] [[projective object|projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any compact projective generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.
=--

+-- {: .proof}
###### Proof
This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=132).
The first part of this theorem can also be found as Prop. 2.1.7. of Victor Ginzburg's [Lectures on noncommutative geometry](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=4).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 
=--

One can characterize functors between categories of $R$-modules that are either (isomorphic) to functors of the form $B \otimes_R -$ where $B$ is a bimodule or those which look as Hom-modules. For the characterization of the tensoring functors see [[Eilenberg-Watts theorem]]. 

Going still further one should be able to obtain a nice theorem describing the image of the embedding of the weak 2-category of

* rings
* bimodules
* bimodule homomorphisms

into the strict 2-category of 

* abelian categories
* right exact functors
* natural transformations.

For more discussion see the [$n$-Cafe](http://golem.ph.utexas.edu/category/2007/08/questions_about_modules.html).

##References

Three classic references, now available online:

* Pierre Gabriel, [[Des Catégories Abéliennes]]

* Peter Freyd, [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3abs.html), originally published by Harper and Row, New York, 1964.

* A. Grothendieck, [[Tohoku]]

See also the [catlist 1999 discussion](http://www.mta.ca/~cat-dist/catlist/1999/atcat) on comparison between abelian categories and topoi ([[AT categories]]).

* N. Popescu, _Abelian categories with applications to rings and modules_, London Math. Soc. Monographs __3__, Academic Press 1973. xii+467 pp. [MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)

##Discussion

The following discussion is about whether a pre-abelian category in which (epi,mono) is a factorization system is necessarily abelian.

+--{: .query}
[[Mike Shulman|Mike]]: In [[Categories Work]], and on [Wikipedia](http://en.wikipedia.org/wiki/Abelian_category), an abelian category is defined to be (in the terms above) a pre-abelian category such that every monic is a kernel and every epi is a cokernel.  This implies that (epi, mono) is an [[orthogonal factorization system]], but I don't see why the converse should hold, as this seems to assert.

[[Zoran Skoda]] It is very late night here in Bonn, so check on my reasoning, but I think that the answer is 
simple. Let $f: A\to B$. The canonical map $\coker(\ker f)\to \ker (\coker f)$ exists as long as we have additive category admitting kernels and cokernels. The arrow from A to coker (ker f) is epi as every cokernel arrow, and the arrow of $\ker(\coker f) \to B$ is mono. Now canonical arrow in between the two is automatically both mono and epi. For all that reasoning I did not yet assume the axiom on uniquely unique factorization. Now assume it and you get
that the canonical map must be isomorphism because it is the unique iso between the two decompositions of $f$: one in which you take epi followed by (the composition of) two monics and another in which you have (the composition of) two epis followed by one monic. Right ?

Now do this for $f$ a monic and you get a decomposition into iso iso kernel and for $f$ an epi and you get 
the cokernel iso iso as required.

[[Mike Shulman|Mike]]: Why is the canonical comparison map mono and epi?  It's late for me too right now, but I think that maybe a counterexample is the "multiplication by 2" map $\mathbb{Z}\to \mathbb{Z}$ in the  category of torsion-free abelian groups.

However, if you assume explicitly that that comparison map is always an isomorphism, then I believe it for the reasons that you gave.

[[Zoran Skoda]] I do not see this as a counterexample, as this is not a pre-abelian category, you do not have cokernels in this category ? In a pre-abelian category always the canonical map from coker ker to ker coker has its own kernel 0 and cokernel 0.

[[Mike Shulman|Mike]]: Torsion-free abelian groups are reflective in abelian groups, and therefore cocomplete.  In particular, they have cokernels, although those cokernels are not computed as in [[Ab]].  In particular, the cokernel of $2:\mathbb{Z}\to\mathbb{Z}$ is 0.

[[Zoran Skoda]] Yes, I was thinking of this reflection argument (equivalence of torsion and localization argument), that is why I put question mark above. Now I tried to prove the assertion that in preabelian cat the canonical map has kernel 0 and cokernel 0 and I can't for more than an hour. But that would mean that for example Gelfand-Manin book is wrong -- it has the discussion on A4 axiom and it says exactly this. Popescu makes an example of preabelian category where canonical map is not iso, but emphasises in his example that it is bimorphism. On the other hand, later, he says that preabelian category is abelian iff it is balanced and the canonical map is bimorphism, hence he requires it explicitly. Let me think more... 

[[Zoran Skoda]] I have rewritten in minimalistic way, leaving just what I can prove, and assuming that you are right and Gelfand-Manin book has one wrong statement (that the canonical map in preabelian category is mono and epi). But let us leave the discussion here for some time, maybe we can improve the question of the difference between preabelian with factorization and abelian. 

[[Mike Shulman|Mike]]: I refactored the page to make clear what we know and what we don't, and include some examples.  Maybe someone will come along and give us a counterexample or a proof.  I wonder what the epimorphisms are in the category of torsion-free abelian groups, and in particular whether it is balanced (since if so, it would be a counterexample).

[[Mike Shulman|Mike]]: Okay, it's obvious: the epimorphisms in $tfAb$ are the maps whose cokernel (in $Ab$) is torsion.  Thus $2:\mathbb{Z}\to\mathbb{Z}$ is monic and epic, so $tfAb$ is not balanced.  And since $2:\mathbb{Z}\to\mathbb{Z}$ is its own canonical map, that canonical map _is_ monic and epic in $tfAb$, so this isn't a counterexample.

_Zoran_: &lt;http://www.uni-trier.de/fileadmin/fb4/INF/TechReports/semi-abelian_categories.pdf> says at one place that Palamodov's version of semi-abelian category is preabelian + canonical morphism is epi and mono.
=--

A discussion about to which extent abelian categories are a general context for [[homological algebra]] is archived at nForum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2052&Focus=17680#Comment_17680).

[[!redirects abelian categories]]