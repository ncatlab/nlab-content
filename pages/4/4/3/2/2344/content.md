
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Why do we take for granted that the [[homotopy theory]] of [[topological space|spaces]] provides a good notion (among others) of [[∞-groupoid]]? Why isn't this an arbitrary choice (apart from the very fact that it works so well)? But we may also question the notion of [[∞-groupoid]]: why should we expect everything to be [[enriched category|enriched]] in higher groupoids?

After all, the good question might be something like: what is the mathematical structure over which everything is canonically enriched? And, last but not least, how can we formulate correctly such a question?

Following [[Grothendieck]] and Heller, the notion of **derivator** provides a way to do this, and the good news are that the question even has an answer: everything is uniquely enriched in [[homotopy type]]s of [[CW-complex]]es or equivalently of [[Kan complex]]es, and there is no other choice at all. This may be seen using only ordinary [[category theory]].

We assume the characteristics of [[category theory]] is: [[category|categories]], [[functor]]s, [[natural transformation]]s, [[Kan extension]]s, [[Grothendieck fibration]]s. We also assume that we know enough about [[2-categories] to speak comfortably of the [[2-category]] [[Cat]] of categories.

So we have the 2-category of categories $Cat$ (categories are allowed to be [[large category|large]], which means their [[hom-set|Hom]]s might be [[class]]es, or non-small sets, depending on your favorite set theoretic preferences), and the 2-category of small categories $cat$, which generate $Cat$ (in the sense that any category is a (large) [[filtered colimit]] of [[small category|small]] ones). 


### Motivation from homotopical/homological algebra

We would like to enlarge the theory of categories, because we know by experience that [[model category|homotopical]] (or [[homological algebra|homological]]) algebra cannot be defined intrinsically in there. A striking example is the theory of [[triangulated category|triangulated categories]]: if $A$ is an [[abelian category]], its (bounded) [[derived category]] $D^b(A)$ is not defined by a universal property: a natural statement would be that, given a triangulated category, the category of additive functors $A\to T$ which send [[short exact sequence]]s to distinguished triangles is equivalent to the category of triangulated functors $D^b(A)\to T$; but this statement is false, and in fact, does not even make sense (unless $A$ is [[semisimple category|semi-simple]]). But, in practice, everything behaves as if the above statement were meaningful and true. The 'reason' why this does not work is that the [[mapping cone|cone]] of a map in a triangulated category is not defined by a universal property. On the other hand, the cone of a morphism of complexes $X\to Y$ is canonically defined: this is the [[homotopy colimit]] of the diagram $0\leftarrow X \to Y$.

### Prederivators

As the $2$-category of categories does not seem to be large enough to express intrinsically our favourite structures, there is a need to enlarge it. An apparently naive way to do so consists to consider [[presheaf|presheaves]] on $cat$. These are contravariant [[2-functor]]s from $cat$ to $Cat$ (contravariant means that it inverts 1-cells and 2-cells). Any category $C$ may considered a prederivator, by sending a small category $X$ to the category $Hom(X^{op},C)$ of presheaves on $X$ with values in $C$. This defines an embedding of $Cat$ into the 2-category $PDer$ of prederivators. 

If $C$ is a [[category with weak equivalences]], we may consider the prederivator $Ho(C)$ which sends a small category $X$ to the [[localization]]/[[homotopy category]] $Ho(C)(X)$ of $Hom(X^{op},C)$ by termwise weak equivalences (as we allowed Hom's to be large, these localization exist). 

This is an example of a non-representable prederivator. However, to do this, we don't need anything else than genuine (2-)[[category theory]]. 

### Derivators

If the category with weak equivalences $C$ is even a [[model category]] then the prederivator $Ho(C)$ is a **derivator** : 

this means that

* for any functor $u:X\to Y$ in $cat$, the [[inverse image]] functor $u^*:Ho(C)(Y)\to Ho(C)(X)$ admits a [[left adjoint]] $u_!$ and a [[right adjoint]] $u_*$; 

* that any map in $Ho(C)(X)$ which is termwise invertible is invertible

* and that we have nice formulas to compute $u_!$ and $u_*$. 

In the case the weak equivalences of $C$ are just the [[isomorphism]]s, this derivator structure is just the theory of [[colimit]]s and [[limit]]s in $C$ (as far as they are indexed by small categories). For a general model category, this structure of derivator just encodes the notion of [[homotopy colimit]] and of [[homotopy limit]]. Note however that this way of seeing homotopy (co)limits does not use anything else than usual category theory.

### The 2-category of derivators

We can consider now the 2-category $Der$ of derivators: 

* [[object]]s are derivators;

*  1-[[morphism]]s are (non-strict) [[transfor|morphisms of 2-functors]] $F:D\to D'$ which commute with the functors $u_!$ (i.e. with homotopy colimits), 

* and 2-cells are the natural transformations (modifications) between these. 

Given two derivators, let us denote by $Hom_!(D,D')$ the category of morphisms of derivators. Given a small category $X$, there is a $2$-functor, defined by evaluating at $X^{op}$
$$Der\to Cat \quad , \qquad D\mapsto D(X^{op}).$$
Note that, for any (pre)derivator $D$, the category $D(X^{op})$ is canonically equivalent to the category $Hom(X,D)$ of morphisms of prederivators from $X$ to $D$ (considering $X$ as a prederivator). This $2$-functor is representable. This means that there exists a derivator $\widehat{X}$, endowed with a morphism of prederivators $h:X\to \widehat{X}$ (called the Yoneda embedding), such that, for any derivator $D$, composing with h defines an equivalence of categories
$$Hom_!(\widehat{X},D)\simeq Hom(X,D)=D(X^{op}).$$

In other words, the map $h:X\to \widehat{X}$ is the "free completion of $X$ by homotopy colimits" in the sense of derivators.

Furthermore, $\widehat{X}$ can be described rather explicitely: this is the derivator associated to the [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $X$.

### Relation to $(\infty,1)$-category theory

This provides a first argument that the usual [[model structure on simplicial sets|homotopy theory of simplicial sets]] plays a central role (as $\widehat{*}$, where $*$ stands for the [[terminal object|terminal]] category), and for this, we didn't take for granted that [[homotopy type]]s should be that important: its universal property is formulated with category theory only. From there, you can see that any derivator is canonically enriched in the derivator $\widehat{*}\simeq Ho(SSet)$: as $*$ acts uniquely on any prederivator, $\widehat{*}\simeq Ho(SSet)$ acts uniquely on any derivator (as far as we ask compatibility with homotopy colimits). 

The [[homotopy hypothesis]] might be reformulated vaguely as: is therean algebraic model of $\widehat{*}$? And then, it looks like some notion of higher groupoid might do the job.

One might argue that the notion of derivator is much weaker than the one of [[(∞,1)-category]] (the latter providing much more interesting structures, whatever model you choose), but that is precisely the point; derivators provide a truncated version of [[higher category theory]] which gives us the language to characterize higher category theory using only usual category theory, without any emphasis on any particular model (in fact, without assuming we even know any).










## References

[[Grothendieck]] has sketched a new formalism for [[homotopy theory]] in his manuscript [[Pursuing Stacks]] and later left another manuscript on the main piece of that theory, the derivators. Independently there is a version due Heller

*  A. Heller, _Homotopy theories_ , Memoirs of the American Mathematical Society, Vol. 71, No 383 (1988).

A __prederivator__ is a strict 2-functor $\mathbb{D}:Dia^{op,co}\to Cat$ where $Dia$ is a full 2-subcategory of $Cat$ (often $Cat$ itself). Morphisms of prederivators are pseudonatural 2-transformations of prederivators. 

A derivator is a prederivator satisfying a longer list of axioms. Every localizer induces a derivator. 

See the Sevilla lectures by Maltsionitis on model categories and derivators:

* [Lecture I (Localizers)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_I_Localizers.pdf)

  [Lecture II (Model Categories)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_II_Model_Categories.pdf)

  [Lecture III (Derivators)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf)

  [Summary on Derivators](http://people.math.jussieu.fr/~maltsin/Seville/Summary_on_Derivators.pdf)

There is also a notion of a triangulated derivator. Being triangulated, is unlike for categories, a property and not a structure; the same for morphisms. 

A link for discussion and a list of source material for  'd&#233;rivateurs' can be found at

* [[Alexander Grothendieck]],  _[Les D&#233;rivateurs](http://people.math.jussieu.fr/~maltsin/groth/Derivateurs.html)_

This includes copies of the first thirteen chapters of a 2000 page manuscript of Grothendieck. 

* [[Georges Maltsiniotis]] has written an introduction to the topic (in French) which is listed near the bottom of his homepage: (G. Maltsiniotis , "Introduction &#224; la th&#233;orie des d&#233;rivateurs, d'apr&#232;s Grothendieck", Preprint (2001).) He also gave a [course](http://congreso.us.es/htag09/php/index.php?carga=courses) in Seville, Sep 2010, and part 3 is on derivators: [Lecture_III_Derivators.pdf](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf) (in English).

Part of the above material is reproduced from

* [[Denis-Charles Cisinski]], _[blog comment on derivators](http://golem.ph.utexas.edu/category/2010/03/a_perspective_on_higher_catego.html#c032227)_