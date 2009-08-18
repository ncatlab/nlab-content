# Idea

Just as ordinary [[category theory]] provides a framework in which one can do "formal mathematics," one of the (many) purposes of [[higher category theory]] is to provide a framework in which one can do "formal category theory."  In particular, many concepts in ordinary category theory can be interpreted internally in a [[2-category]], in a way which specializes to the original concept in [[Cat]].  Examples of such concepts include [[adjunctions]], [[monads]], [[Grothendieck fibrations]], [[Kan extensions]], and [[fully faithful morphisms]].

However, these internalizations are not always "correct" in every 2-category.  For instance, in the 2-category $V Cat$ of [[enriched categories|categories enriched]] in a [[monoidal category]] $V$, internal adjunctions and monads give the correct notion of $V$-adjunction and $V$-monad, but internal fully-faithfulness for a $V$-functor is weaker than the "correct" notion of $V$-fully-faithfulness.  More technically, in many cases the naive notion of Kan extension is not sufficient and one needs "pointwise" Kan extensions; with some more work these can also be defined in a 2-category, but the resulting notion (though correct in $Cat$) is not always correct in $V Cat$.

Furthermore, some concepts of category theory are difficult to interpret at all in a 2-category.  The notion of [[limit]] in ordinary category theory can be interpreted in a 2-category by identifying the limit of a functor $D\to C$ as its Kan extension along the unique functor $D\to *$.  However, in enriched category theory the more important notion is that of [[weighted limit]], and there is no straightforward way to interpret this in $V Cat$.

What is missing is that the 2-category $V Cat$ doesn't natively supply any information about the $V$-valued hom-functors in a 2-category.  (In $Cat$ these hom-functors can be recovered by looking at [[comma categories]], which can be interpreted internally as [[comma objects]]---in some sense this is what all the above internalizations are secretly doing.)  Thus, all of these problems can be remedied by equipping a 2-category with extra structure which describes these hom-functors, or more generally describes a notion of [[profunctor]].

There are several not-quite-equivalent ways to describe this extra structure.  One due to Street and Walters, called a [[Yoneda structure]], involves assigning to each object $X$ a "presheaf object" $P X$ and a "Yoneda arrow" $X\to P X$; a profunctor $X\to Y$ is then identified with an arrow $Y \to P X$.  The notion of *equipment*, due to Wood, instead postulates an additional bicategory of "proarrows" and specifies their relationship to the ordinary arrows.  One can then define fully faithful morphisms, pointwise Kan extensions, weighted limits, etc. relative to this structure, in a way which specializes to the correct notions in $V Cat$.

# Definition #

An **equipment** (or *proarrow equipment*) consists of:

* a 2-category $K$,
* a 2-category $M$, whose arrows are called *proarrows*, and
* a functor $(-)_\bullet: K\to M$ which is the identity on objects and locally fully faithful, such that
* for each arrow $f:X\to Y$ in $K$, the proarrow $f_\bullet:X\to Y$ has a right adjoint $f^\bullet$ in $M$.

As usual on the nLab, here by [[2-category]] we mean a weak 2-category (aka [[bicategory]]) and by [[functor]] we mean a weak 2-functor (aka [[pseudofunctor]]).  However, in many or most examples, $K$ is in fact a [[strict 2-category]].

For example, if $V$ is a [[cosmos]], we define an equipment where $K= V Cat$ is the 2-category of $V$-enriched categories, $M=V Mod$ is the bicategory of $V$-enriched profunctors, and $f_\bullet$ and $f^\bullet$ are the two ways of regarding a $V$-functor $f:A\to B$ as a profunctor, namely $B(f-,-)$ and $B(-,f-)$.  Composition of $V$-profunctors is by [[tensor product]], i.e. [[coends]]; note that we require $V$ to be [[cocomplete category|cocomplete]] with colimist preserved by $\ten$ on both sides in order to form such associative tensor products.

