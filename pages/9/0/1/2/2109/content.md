#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

Just as ordinary [[category theory]] provides a framework in which one can do "formal mathematics," one of the (many) purposes of [[higher category theory]] is to provide a framework in which one can do "formal category theory."  In particular, many concepts in ordinary category theory can be interpreted internally in a [[2-category]], in a way which specializes to the original concept in [[Cat]].  Examples of such concepts include [[adjunctions]], [[monads]], [[Grothendieck fibrations]], [[Kan extensions]], and [[fully faithful morphisms]].

However, these internalizations are not always "correct" in every 2-category.  For instance, in the 2-category $V Cat$ of [[enriched categories|categories enriched]] in a [[monoidal category]] $V$, internal adjunctions and monads give the correct notion of $V$-adjunction and $V$-monad, but internal fully-faithfulness for a $V$-functor is weaker than the "correct" notion of $V$-fully-faithfulness.  More technically, in many cases the naive notion of Kan extension is not sufficient and one needs "pointwise" Kan extensions; with some more work these can also be defined in a 2-category, but the resulting notion (though correct in $Cat$) is not always correct in $V Cat$.

Furthermore, some concepts of category theory are difficult to interpret at all in a 2-category.  The notion of [[limit]] in ordinary category theory can be interpreted in a 2-category by identifying the limit of a functor $D\to C$ as its Kan extension along the unique functor $D\to *$.  However, in enriched category theory the more important notion is that of [[weighted limit]], and there is no straightforward way to interpret this in $V Cat$.

What is missing is that the 2-category $V Cat$ doesn't natively supply any information about the $V$-valued hom-functors in a 2-category.  (In $Cat$ these hom-functors can be recovered by looking at [[comma categories]], which can be interpreted internally as [[comma objects]]---in some sense this is what all the above internalizations are secretly doing.)  Thus, all of these problems can be remedied by equipping a 2-category with extra structure which describes these hom-functors, or more generally describes a notion of [[profunctor]].

There are several not-quite-equivalent ways to describe this extra structure.  One due to Street and Walters, called a [[Yoneda structure]], involves assigning to each object $A$ a "presheaf object" $P A$ and a "Yoneda arrow" $A\to P A$; a profunctor $A\to B$ is then identified with an arrow $B \to P A$.  The notion of *equipment*, due to Wood, instead postulates an additional bicategory of "proarrows" and specifies their relationship to the ordinary arrows.  One can then define fully faithful morphisms, pointwise Kan extensions, weighted limits, etc. relative to this structure, in a way which specializes to the correct notions in $V Cat$.

## Definition ##

An **equipment** (or *proarrow equipment*) consists of:

* a 2-category $K$,
* a 2-category $M$, whose arrows are called *proarrows*, and
* a functor $(-)_\bullet: K\to M$ which is the identity on objects and locally fully faithful, such that
* for each arrow $f:A\to B$ in $K$, the proarrow $f_\bullet:A\to B$ has a right adjoint $f^\bullet$ in $M$.

As usual on the nLab, here by [[2-category]] we mean a weak 2-category (aka [[bicategory]]) and by [[functor]] we mean a weak 2-functor (aka [[pseudofunctor]]).  However, in many or most examples, $K$ is in fact a [[strict 2-category]].  We say that $M$ and $(-)_\bullet$ "equip $K$ with proarrows."

For example, if $V$ is a [[cosmos]], we define an equipment where $K= V Cat$ is the 2-category of $V$-enriched categories, $M=V Mod$ is the bicategory of $V$-enriched profunctors, and $f_\bullet$ and $f^\bullet$ are the two ways of regarding a $V$-functor $f:A\to B$ as a profunctor, namely $B(-,f-)$ and $B(f-,-)$.  Composition of $V$-profunctors is by [[tensor product]], i.e. [[coends]]; note that we require $V$ to be [[cocomplete category|cocomplete]] with colimist preserved by $\ten$ on both sides in order to form such associative tensor products.  We call this equipment simply $V Cat$.

With this example in mind, we sometimes use $B(1,f)$ and $B(f,1)$ (or $hom_B(1,f)$ and $hom_B(f,1)$) as alternate notations for $f_\bullet$ and $f^\bullet$.  For an arbitrary proarrow $H:B\to D$ and ordinary arrows $f:A\to B$ and $g:C\to D$, we write $H(g,f)$ or $g^* H f^*$ for the composite $g^\bullet H f_\bullet$, a proarrow from $A$ to $C$.  In $V Cat$, $H(g,f)$ is the result of precomposing the profunctor $H:D^{op}\otimes B \to V$ with $g^{op}\otimes f$.  We also write $U_A$, $A(1,1)$ or $hom_A$ for the identity proarrow $A\to A$.

The other most common sort of generalized category, namely [[internal categories]] in some category $S$, also form an equipment called $Cat(S)$.  In this case, we require $S$ to have finite limits and coequalizers preserved by pullback in order for the bicategory of internal profunctors to have associative compositions. See "virtual equipments," below, for a context which avoids these restrictions on $V$ and $S$.


## Category theory in an equipment ##

We give here a few examples of how to do category theory internal to an equipment.

An arrow $f:A\to B$ in an equipment is said to be **fully faithful** if the canonical morphism $U_A\to B(f,f)$ is an isomorphism.  In $V Cat$ this recaptures the correct notion of $V$-fully-faithful $V$-functor.

If $f:A\to C$ is an arrow and $J:K\to A$ is a proarrow, then a **$J$-weighted colimit** of $f$ is an arrow $l:K\to C$ such that $l^\bullet$ is a right lifting of $f^\bullet$ along $J$ in the 2-category of proarrows.  (A right lifting is the dual concept of a right extension, the internalization of right Kan extension to a 2-category.)  In $V Cat$, if $K=I$ is the unit $V$-category (one object with endomorphisms the unit of $V$), then $J$ is a $V$-functor $A^{op}\to V$ and $J$-weighted colimits in this sense coincide with the usual notion of weighted colimits in enriched category theory.

If $j:A\to K$ is an arrow, then $j^\bullet$-weighted colimits are called **pointwise left extensions along $j$**.  It is easy to show that these are, in particular, left extensions in the 2-category of arrows, and that in $V Cat$ they reproduce the usual notion of pointwise left Kan extension.


## Discrete fibrations and codiscrete cofibrations ##

As noted above, in the case of ordinary categories, the profunctors can in fact be recovered from the 2-category $Cat$.  Specifically, profunctors $A\to B$ can be identified with two-sided discrete fibrations from $B$ to $A$ (that is, spans $B \leftarrow C \to A$ such that $C \to B$ is a [[Grothendieck fibration|(Grothendieck) fibration]], $C\to A$ is an opfibration, the two structures are compatible, and each fiber of $C\to B\times A$ is discrete).  The same is true for internal categories, but not for enriched categories.

However, for a cosmos $V$, the $V$-profunctors $A\to B$ can _also_ be recovered from the 2-category $V Cat$ in a different, and in fact dual, way: they are the two-sided _codiscrete cofibrations_ from $B$ to $A$, i.e. two-sided discrete fibrations in $(V Cat)^{op}$.  This was first noticed by Street and subsequently expanded on by other authors; one can write down axioms on a 2-category guaranteeing that its codiscrete cofibrations can be used to construct an equipment.


## Equipments and double categories ##

Given an equipment, we can construct a [[double category]] with the same objects, whose vertical 1-cells are the arrows, whose horizontal 1-cells are the proarrows, and whose squares
$$\array{A & \overset{H}{\to} & C \\
  ^f\downarrow & \Downarrow & \downarrow^g\\
  B& \underset{K}{\to} & D}
$$
are the 2-cells $g_\bullet H \to K f_\bullet$.  Note that if the arrows form a strict 2-category, then this is a [[pseudo double category]] (vertically strict and horizontally weak) while if the arrows and proarrows are both weak 2-categories, this double category is weak in both directions (like a [[double bicategory]]).

Double categories constructed in this way have the special property that every vertical 1-cell $f$ has both a [[companion]] (namely $f_\bullet$) and a [[conjoint]] (namely $f^\bullet)$.  Conversely, from any double category with this property, one can construct an equipment in the obvious way.  In this way equipments can be shown to be equivalent to a certain class of double categories.  While the definition given above is perhaps simpler, for some purposes it is preferable to *define* equipments to be certain double categories, for instance when one wants to collect them into a 2-category or 3-category---basically the only way to define transformations between functors of equipments is to view them as double categories, explicitly or implicitly.


## Virtual equipments ##

One can formulate a generalized notion of equipment which includes $V Cat$ for _any_ monoidal category $V$ (and in fact, any [[multicategory]]), and $Cat(S)$ for any category $S$ with pullbacks.  The precise definition is complicated, but the basic idea is not: we start from the double-category definition, and instead of composites of the horizontal (pro)arrows, we allow the squares to have domains that are arbitrary composable strings, like so:
$$\array{ & \to \to \dots \to &\\
  \downarrow & \Downarrow & \downarrow\\
  & \underset{}{\to}& .}$$
So far this is analogous to the generalization from monoidal categories to multicategories, and gives the notion of [[fc-multicategory]] (aka "virtual double category").  We then impose a condition analogous to the existence of companions and conjoints to obtain the notion of **virtual equipment** (see references).  Most of  category theory can be done in a virtual equipment just as well as in an equipment.


## Categories enriched in an equipment ##

For any equipment $W$ one can define a notion of **$W$-enriched category**.  This consists of

* a collection $ob(C)$ of objects,
* for each object $x$ an *extent* $e(x)$ which is an object of $W$,
* for each pair of objects $x,y$ a proarrow $hom_C(x,y):e(x)\to e(y)$,
* composition and identity-assigning 2-cells obeying associativity and unit axioms.

So far we have not used the ordinary arrows, so many authors have studied only the notion of "category enriched in a bicategory."  (Note that any 2-category $M$ can be regarded as the proarrow 2-category of an equipment in which the only ordinary arrows are identites.)  However, we need the extra structure when we define a *functor* $f:C\to D$ between $W$-enriched categories, which consists of:

* a function $f:ob(C)\to ob(D)$,
* for each object $x$ of $C$ an arrow $f_x:e(x)\to e(f(x))$ in $W$,
* for each pair of objects $x$ and $y$, a square
$$\array{e(y) & \overset{hom_C(x,y)}{\to} & e(x)\\
  ^{f_y}\downarrow & \Downarrow & \downarrow^{f_x}\\
  e(f(y))& \underset{hom_D(f(x),f(y))}{\to} & e(f(x))}$$
* satisfying functoriality axioms.

Finally, we define a *natural transformation* between such functors $f,g:C\to D$ to consist of

* squares
$$\array{e(x) & \overset{U_{e(x)}}{\to} & e(x)\\
  ^{g_x}\downarrow & \Downarrow & \downarrow^{f_x}\\
  e(g(x))& \underset{hom_D(f(x),f(y))}{\to} & e(f(x))}$$
* satisfying a naturality axiom.

By choosing $W$ appropriately, categories enriched in an equipment include most types of generalized category:

* If $W$ is a monoidal category $V$, regarded as a one-object bicategory and thence as an equipment with only one ordinary arrow (so the objects of $V$ are the proarrows of $W$), then $W$-enriched categories, functors, and natural transformations are the same as $V$-enriched ones.

* If $S$ has pullbacks, there is an equipment $Span(S)$ whose objects  and arrows are those of $S$ and whose proarrows are spans.  A category enriched in $Span(S)$ which has one object is the same as an internal category in $S$, and likewise for functors and transformations.  (Here it is essential to use an equipment, rather than merely a bicategory, to get the right notion of functor.)

* Arbitrary $Span(S)$-enriched categories can be identified with "locally small fibrations" over $S$, aka "locally internal categories" over $S$.

Other choices of $W$ give "categories which are both enriched and internal," for example:

* For a suitably nice category $S$ (such as a [[Grothendieck topos]]) there is an equipment $Ab(S)$ whose objects and arrows are those of $S$, and whose proarrows $A\to B$ are internal abelian group objects in $S/(B\times A)$.  An $Ab(S)$-enriched category with one object can be regarded as an "internal [[Ab-enriched category]]" in $S$.


## References ##



* R.J. Wood, "Abstract Proarrows I" and "Proarrows II" (the original definitions)

* [[Ross Street]], "Fibrations in bicategories" (Construction of $V Mod$ from $V Cat$.)

* [[Aurelio Carboni]], Scott Johnson, Ross Street, and Dominic Verity, "Modulated bicategories" (Improved construction of $V Mod$ from $V Cat$.)

* [[Dominic Verity]], "Enriched categories, internal categories, and change of base", Ph.D. Thesis.  (The connection with double categories.)

* [[Michael Shulman]], "Framed bicategories and monoidal fibrations".  (The equivalence with certain double categories, there called *framed bicategories*, and a general way to construct equipments such as $Ab(S)$.)

* G.S.H Cruttwell and Michael Shulman, "A unified framework for generalized multicategories" (currently the only reference for virtual equipments).

* [[Renato Betti]], Aurelio Carboni, Ross Street, and [[Robert Walters]], "Variation through enrichment."  (Locally small fibrations as $Span$-enriched categories.)


A blog post surveying ideas in equipments is

* [[Mike Shulman]], _Equipments_ ([blog](http://golem.ph.utexas.edu/category/2009/11/equipments.html#c029531))


[[!redirects equipments]]
