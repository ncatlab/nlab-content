
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **derivator** is a refinement of a [[homotopy category]] which also includes information about [[homotopy limits]] and colimits.  In some cases derivators can be used where one might otherwise need to use [[(∞,1)-categories]], which can be helpful since their theory is much simpler and purely (2-)categorical.  They were invented by [[Grothendieck]] and Heller.

## Motivation

The notion of derivator can be motivated in several ways.

### As a halfway house

Suppose we start from the perspective that what we really study in [[homotopy theory]] are [[(∞,1)-categories]].  The [[homotopy category of an (∞,1)-category]] (the 1-category obtained by setting all equivalent 1-morphisms equal) is a fairly coarse invariant, but for some purposes it is sufficient.  On the other hand, sometimes we need more than merely the homotopy category, but doing everything with $(\infty,1)$-categories can be technically daunting.  Frequently, all we need from an $(\infty,1)$-category that is not present in its homotopy category is to know that we have well-behaved constructions of [[homotopy limit]]s and [[homotopy colimit]]s.

A *derivator* is thus a halfway-house, containing more information than a homotopy category, but easier to work with than an $(\infty,1)$-category.  It consists of a homotopy category together with extra structure that enables one to compute with homotopy limits and colimits.  Any $(\infty,1)$-category with sufficiently many limits and colimits has an underlying derivator, and working with these derivators suffices for a surprising number of things we may want to do with $(\infty,1)$-categories.  However, derivators are an essentially 1-categorical notion, so we can study them using ordinary [[2-category]] theory.  Thus derivators provide a "truncated" version of [[higher category theory]], which gives us the language to characterize higher category theory using only usual [[category theory]], without any emphasis on any particular model (in fact, without assuming we even know any such model).

For instance, it turns out that we can also express many convenient [[universal properties]] in terms of derivators. A striking example is the theory of [[triangulated category|triangulated categories]]: if $A$ is an [[abelian category]], its (bounded) [[derived category]] $D^b(A)$ is not defined by a universal property.  A natural statement would be that, given a triangulated category, the category of additive functors $A\to T$ which send [[short exact sequence]]s to distinguished triangles is equivalent to the category of triangulated functors $D^b(A)\to T$, but this statement is false, and in fact, does not even make sense (unless $A$ is [[semisimple category|semi-simple]]). But, in practice, everything behaves as if the above statement were meaningful and true. The 'reason' why this does not work is that the [[mapping cone|cone]] of a map in a triangulated category is not defined by a universal property. On the other hand, the cone of a morphism of complexes $X\to Y$ is canonically defined: this is the [[homotopy colimit]] of the diagram $0\leftarrow X \to Y$.  In the world of derivators, we can remedy this situation and recover a suitable universal property.


### As a motivation for $(\infty,1)$-categories

On the other hand, we may ask: Why do we take for granted that the [[homotopy theory]] of [[topological space|spaces]] provides a good notion (among others) of [[∞-groupoid]]?  And why should we expect everything to be [[enriched category|enriched]] in higher groupoids anyway?  A priori this may seem arbitrary (although it certainly works very well).  Instead we might ask: what is the mathematical structure over which everything is canonically enriched?  How can we even correctly formulate such a question?

The notion of *derivator* provides a way to correctly formulate such a question, and the answer turns out to be mostly what we expect.  Every type of "category theory" (at least, category theory without an *a priori* given [[enriched category|enrichment]]) that we might want to do is automatically and uniquely enriched in [[homotopy types]], i.e. in the homotopy category of [[CW-complexes]] or [[Kan complexes]].  (For ordinary 1-category theory, this enrichment is trivial, i.e. factors through sets considered as discrete homotopy types.)  A derivator is simply a structure with the characteristics of ordinary [[category theory]]: [[category|categories]], [[functor]]s, [[natural transformation]]s, [[Kan extension]]s, [[Grothendieck fibration]]s.  We can then show that any derivator acquires such an enrichment, so that homotopy types are a canonical enriching place for "category theories."


## Definition

### Prederivators

Let [[Cat]] denote the [[2-category]] of [[large category|large]] [[categories]] (not necessarily even [[locally small category|locally small]]), and let $Dia$ be some 2-category of [[small categories]], thought of as **[[diagram]]s**.  One common choice is the 2-category of *all* small categories (which generates $Cat$), but we might also choose the 2-category of finite categories.  A **prederivator** with domain $Dia$ is a strict [[2-functor]]

$$ Dia^{coop} \to Cat $$

As usual, $(-)^{coop}$ denotes the double dual of a 2-category, which reverses both 1-cells and 2-cells.  Thus, a prederivator is a "$Cat$-valued [[presheaf]]" on $Dia$.  Prederivators form a 2-category $PDer$ whose morphisms are [[pseudonatural transformations]] and whose 2-cells are [[modification]]s.

+--{: .query}
[[Mike Shulman]]: Is it universal to use $Dia^{coop}$ here?  It seems *much* more natural to me to use $Dia^{op}$, since we usually take limits and colimits of covariant functors, not contravariant ones.
=--

There are two main motivating examples.  Firstly, any category $C$ defines a "representable" prederivator by the assignation $X\mapsto Hom(X^{op},C)$, sending $X\in Dia$ to the category of functors $X^{op}\to C$.  This defines an embedding of $Cat$ into $PDer$.

Secondly, if $C$ is any [[category with weak equivalences]], there is a prederivator $Ho(C)$ which sends $X\in Dia$ to the [[localization]]/[[homotopy category]] $Ho(C)(X)$ of $Hom(X^{op},C)$ relative to the [[model structure on functors|objectwise weak equivalences]] (as we allowed categories in $Cat$ to have large [[hom-set]]s, these localization exist).  In general, this is a non-representable prederivator, although of course if the weak equivalences are just the [[isomorphism]]s, it reduces to the representable case.  Note that to construct it, we don't need anything besides ordinary [[2-category|(2-)]][[category theory]]. 

### Derivators

A **derivator** is a prederivator $D$ which satisfies a list of axioms.  These axioms are of two sorts.

The first set of axioms says that there exist well-behaved homotopy limits and colimits, and more generally [[homotopy Kan extension]]s.  Specifically, we require the following.

* For any functor $u : X\to Y$ in $Dia$, the [[inverse image]] functor $u^*:D(Y)\to D(X)$ admits a [[left adjoint]] $u_!$ and a [[right adjoint]] $u_*$.  These can be understood as [[homotopy Kan extension]]s

  $$
    (u_! \dashv u^* \dashv u_*) 
    :
    D(Y)
      \stackrel{
         \overset{u_!}{\to}
      }
      {
        \stackrel{
          \overset{u^*}{\leftarrow}
        }{
          \underset{u_*}{\to}
        }
      }
    D(X)
  $$

* For any [[comma square]]
  $$\array{A & \overset{g}{\to} & B \\
  ^f\downarrow &\Downarrow& \downarrow^v\\
  C& \underset{u}{\to} & D}$$
  in $Dia$, the Beck-Chevalley transformations
  $$ f_! g^* \to u^* v_! \quad \text{and} \quad v^* u_* \to g_* f^* $$
  are isomorphisms.  Intuitively, this says that the Kan extensions in question are *pointwise*.  In the presence of the second set of axioms, it suffices to require this when $C$ is the [[terminal category]] (for the first case) and when $D$ is so (for the second).

The second set of axioms are "[[sheaf]]" conditions.  Of course, we cannot assert that $D$ is exactly a sheaf (in the appropriate [[stack|2-categorical sense]]), since the terminal category in $Dia$ is dense and so any sheaf on it is representable (and represented by $D(1)$), whereas we want to also allow non-representable derivators.  But we do need some sheaf-like properties in order to do category theory.  All of the following axioms can be understood as asserting that for some [[cover|covering family]] $\{Y_i \to X\}$ in $Dia$, the canonical map $D(X) \to Desc(D,\{Y_i\})$ from $D(X)$ to the category of [[descent]] data for the covering, while not an [[equivalence of categories|equivalence]], has some weaker good properties.

The standard axioms are:

* $D\colon Dia^{coop} \to Cat$ takes [[coproduct]]s to products.  Sometimes we require this only for finite coproducts.  In particular, we have $D(\emptyset) = 1$.

* For any $X\in Dia$, consider the family of functors $x\colon 1\to X$ determined by the objects of $X$.  Then the induced functor
  $$ D(X) \overset{(x^*)}{\to} \prod_x D(1)$$
  is [[conservative functor|conservative]] (though not generally faithful).  This in turn implies that the same is true for any jointly [[essentially surjective functor|essentially surjective]] family of functors.

* For any $X\in Dia$, if $I$ denotes the [[interval category]], then the induced functor
  $$ D(X\times I) \to Hom(I,D(X)) $$
  is [[essentially surjective functor|essentially surjective]] and [[full functor|full]] (though again, it is not generally faithful).  Sometimes it is convenient to assume this property when $I$ is any (perhaps finite) [[free category]].

+--{: .query}
[[Mike Shulman]]: It's clear to me that these are desirable requirements, which are moreover satisfied by all derivators of the form $Ho(C)$, but I would really like a conceptual explanation for why these axioms are *sufficient*.
=--

It is easy to see that if $C$ has pointwise left and right Kan extensions along all functors in $Dia$, then its representable prederivator is a derivator.  Somewhat more difficult to prove is that if $C$ is a [[model category]] (or more generally, has well-behaved homotopy Kan extensions), then the prederivator $Ho(C)$ is also a derivator.  Thus the derivator encodes the notions of [[homotopy colimit]] and of [[homotopy limit]].  Note again that this way of seeing homotopy (co)limits does not use anything besides usual (2-)category theory.


## The 2-category of derivators

We can consider now the 2-category of derivators.  Actually, there are several different ways to define such a 2-category, depending on whether we require morphisms to preserve homotopy colimits, limits, both, or neither.  Let us write $Der_!$ for the 2-category whose morphisms preserve colimits.  Thus:

* its [[object]]s are derivators,

* its 1-[[morphism]]s are [[pseudonatural transformations]] $F:D\to D'$ which commute with the functors $u_!$ (i.e. the canonical comparison maps for these are isomorphisms),

* its 2-cells are the [[modifications]] between these.

We write $Hom_!(D,D') = Der_!(D,D')$ for hom-categories in this 2-category.

### Free cocompletions

Now, given a small category $X$, there is a $2$-functor, defined by evaluating at $X^{op}$
$$Der_!\to Cat \quad , \qquad D\mapsto D(X^{op}).$$
Note that, for any (pre)derivator $D$, the category $D(X^{op})$ is canonically equivalent to the category $Hom(X,D)$ of morphisms of *prederivators* from $X$ to $D$ (considering $X$ as a representable prederivator).  Of course, $X$ will usually not itself be a derivator, but nevertheless this $2$-functor is *representable* in the 2-category $Der_!$.

Thus, there exists a derivator $\widehat{X}$, endowed with a morphism of prederivators $h:X\to \widehat{X}$ (called the Yoneda embedding), such that, for any derivator $D$, composing with h defines an equivalence of categories
$$Hom_!(\widehat{X},D)\simeq Hom(X,D)=D(X^{op}).$$
In other words, the map $h:X\to \widehat{X}$ is the "free completion of $X$ by homotopy colimits" in the sense of derivators.

Furthermore, $\widehat{X}$ can be described rather explicitly: it is the derivator associated to the [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $X$.  In particular, the usual [[model structure on simplicial sets|homotopy theory of simplicial sets]] gives rise to the derivator $\widehat{*}$, where $*$ stands for the [[terminal object|terminal]] category.  Note that in order to conclude this, we didn't take for granted that [[homotopy type]]s should be important: its universal property is formulated purely with ordinary category theory.

From there, you can see that any derivator is canonically enriched in the derivator $\widehat{*}\simeq Ho(SSet)$: as $*$ acts uniquely on any prederivator, $\widehat{*}\simeq Ho(SSet)$ acts uniquely on any derivator (as far as we ask compatibility with homotopy colimits).  Thus the [[homotopy hypothesis]] might be reformulated vaguely as: is there an algebraic model of $\widehat{*}$?  Then one may guess that some notion of higher groupoid might do the job.


## Related pages

* [[pointed derivator]]
* [[stable derivator]]
* [[monoidal derivator]]


## References

[[Grothendieck]] has sketched a new formalism for [[homotopy theory]] in his manuscript [[Pursuing Stacks]] and later left another manuscript on the main piece of that theory, the derivators. Independently there is a version due to Heller

*  A. Heller, _Homotopy theories_ , Memoirs of the American Mathematical Society, Vol. 71, No 383 (1988).

See the Sevilla lectures by Maltsionitis on model categories and derivators:

* [Lecture I (Localizers)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_I_Localizers.pdf)

  [Lecture II (Model Categories)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_II_Model_Categories.pdf)

  [Lecture III (Derivators)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf)

  [Summary on Derivators](http://people.math.jussieu.fr/~maltsin/Seville/Summary_on_Derivators.pdf)

A link for discussion and a list of source material for  'd&#233;rivateurs' can be found at

* [[Alexander Grothendieck]],  _[Les D&#233;rivateurs](http://people.math.jussieu.fr/~maltsin/groth/Derivateurs.html)_

This includes copies of the first thirteen chapters of a 2000 page manuscript of Grothendieck. 

* [[Georges Maltsiniotis]] has written an introduction to the topic (in French) which is listed near the bottom of his homepage: (G. Maltsiniotis , "Introduction &#224; la th&#233;orie des d&#233;rivateurs, d'apr&#232;s Grothendieck", Preprint (2001).) He also gave a [course](http://congreso.us.es/htag09/php/index.php?carga=courses) in Seville, Sep 2010, and part 3 is on derivators: [Lecture_III_Derivators.pdf](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf) (in English).

Part of the above material is adapted from

* [[Denis-Charles Cisinski]], _[blog comment on derivators](http://golem.ph.utexas.edu/category/2010/03/a_perspective_on_higher_catego.html#c032227)_

[[!redirects derivators]]
[[!redirects prederivator]]
[[!redirects prederivators]]
[[!redirects derivateur]]
[[!redirects dérivateur]]
[[!redirects derivateurs]]
[[!redirects dérivateurs]]
