
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In an [[Ab-enriched category]], it is natural to produce an [[image]] factorization of a morphism by first forming its [[kernel]] and then the [[cokernel]] of the kernel.  Similarly, in a [[regular category]] we can produce an image factorization by first forming the [[kernel pair]] and then the [[coequalizer]] of the kernel pair.  Several similar situations arise in the study of [[2-categories]] as well.  The theory of **generalized kernels** in [[enriched categories]] subsumes all of these examples.

## Generalized kernels and their quotients

Let $V$ be a [[cosmos]] and let $\mathbf{2}$ denote the [[interval category]] regarded as a $V$-category, i.e. it has two objects $0$ and $1$, with $hom(0,0) = hom(1,1) = hom(0,1) = I$ (the unit object of $V$) and $hom(1,0) = \emptyset$ (the initial object of $V$).  Let $H$ be a $V$-category which contains $\mathbf{2}$ as a full subcategory, and let $J$ be the full subcategory of $H$ containing all the objects except $1$.  Then the inclusions of $J$ and $\mathbf{2}$ into $H$ induce a [[profunctor]] $K\colon \mathbf{2} &#8696; J$.  This is the input data for a notion of kernels.

Now suppose that $C$ is a $V$-category with sufficiently many limits and colimits, and that $f\colon x\to y$ is a morphism in $C$.  Then $f$ can be identified with a $V$-functor $\ulcorner f \urcorner \colon \mathbf{2}\to C$.  The **kernel** of $f$ is defined to be the $K$-[[weighted limit]] of $\ulcorner f \urcorner$, which is a $V$-functor $ker(f)\colon J\to C$.  By construction of $K$, it can equivalently be described as the (enriched, pointwise) right [[Kan extension]] of $\ulcorner f \urcorner$ from $\mathbf{2}$ into $H$, followed by restriction to $J$.  Since the inclusion of $\mathbf{2}$ into $H$ is fully faithful, it follows that $ker(f)(0) = \ulcorner f \urcorner (0) = x$.

Similarly, let $M$ be a $V$-functor $J\to C$; we call such a functor **kernel data**.  The **quotient** of $M$ defined to be its $K$-weighted colimit. This is a functor $\mathbf{2}\to C$, i.e. a single morphism in $C$.  Again, by construction of $K$, the quotient of $M$ can equivalently be described by the left Kan extension of $M$ to $H$, followed by restriction to $\mathbf{2}$, and since $J\to H$ is fully faithful, the source of the quotient of $M$ is the object $M(0)$.

Since colimits and limits weighted by a fixed profunctor are adjoint to each other (or equivalently, since left and right Kan extension are left and right adjoint to restriction), we obtain an adjunction
$$ quot: [J,C] \;\rightleftarrows\; [\mathbf{2},C] :ker $$
Moreover, by the remarks above, for any object $x\in C$ this adjunction restricts to an adjunction
$$ quot: [J,C]_x \;\rightleftarrows\; x/C :ker $$
where $[J,C]_x$ denotes the subcategory of $[J,C]$ on those functors $M$ such that $M(0)=x$.  Of course the analogous subcategory $[\mathbf{2},C]_x$ is just the [[coslice category]] $x/C$.

Of particular interest is the [[counit]] of this adjunction at a morphism $f\colon x\to y$, which is a morphism $quot(ker(f)) \to f$ in $x/C$.  In other words, it is a *factorization* of $f$.  Often the factorizations produced in this way are familiar.

## Examples

1. With $V=Set$, let $H$ be the category
   $$ z \;\rightrightarrows\; 0 \to 1 $$
   with the two composites $z\to 1$ being equal.  That is, $H$ is the "[[walking structure|walking]] fork."  Then kernel data is a pair of parallel arrows, the kernel of a morphism is its [[kernel pair]], and the quotient of a parallel pair is their [[coequalizer]].  In a [[regular category]], the factorization produced in this way is the usual [[image]] factorization.

   Note that since coequalizers are epic, the full image of $quot\colon [J,C] \to [\mathbf{2},C]$ is a preorder, and thus in this case the adjunction is [[idempotent adjunction|idempotent]].  This yields the familiar fact that a morphism is a coequalizer iff it is the coequalizer of its kernel pair, and a parallel pair is a kernel pair iff it is the kernel pair of its coequalizer.

1. Again with $V=Set$, let $H$ be the category
   $$ \array{ 0 \\ & \searrow \\ z & \to & 1 } $$
   Then kernel data is just a pair of objects, the kernel of a morphism $f\colon x\to y$ is the pair $(y,x)$, and the quotient of a pair $(y,x)$ is the [[coproduct]] injection $x \to (x\sqcup y)$.  The factorization of $f\colon x\to y$ obtained in this way is $x \to (x\sqcup y) \overset{[f,id]}{\to} y$.

1. With $V=Ab$, let $H$ be the [[Ab-enriched category]] with three objects $z,0,1$ and $H(z,z) = H(0,0) = H(1,1) = H(z,0) = H(0,1) = \mathbb{Z}$ and all other hom-groups being $0$.  Then a diagram of shape $H$ in an Ab-category consists of a pair of composable arrows whose composite is zero.  Then kernel data is also just a single morphism, the kernel of a morphism is its [[kernel]] in the usual sense, and the quotient of a morphism (considered as kernel data) is its [[cokernel]] in the usual sense.  The resulting factorization is again the usual image factorization, and the adjunction is again idempotent.

1. With $V=Cat$, let $H$ be the (strict) [[2-category]] with three objects $z,0,1$ and $H(0,1) = *$, $H(z,1) = \mathbf{2}$, and $H(z,0)$ the "[[walking structure|walking]] [[parallel pair]]" $(\cdot \rightrightarrows \cdot)$.  Then kernel data in a 2-category consists of a pair of parallel 2-cells, and the quotient of such a pair is their [[coequifier]].  In $Cat$ at least, the kernel $f\colon x\to y$ of a functor is the category of parallel pairs in $x$ which become equal in $y$, and the resulting factorization of $f$ consists of an bijective-on-objects-and-full functor followed by a faithful one.  Since bijective-on-objects-and-full functors are epic in $Cat$, the adjunction is again idempotent.

1. Again with $V=Cat$, let $H$ be the 2-category with three objects $y,0,1$ and $H(0,1)=*$, $H(y,0)$ the discrete category with two objects, and $H(y,1)=\mathbf{2}$.  Then kernel data is a pair of parallel 1-morphisms, and the quotient of such a pair is their [[coinserter]].  The kernel of a morphism $f\colon x\to y$ is the [[comma object]] $(f/f)$.

1. Once again with $V=Cat$, let $H$ be the 2-category
   $$ \array{ && 0\\ & \nearrow & \cong & \searrow \\ z && \to && 1} $$
   Then kernel data is again a single arrow, its quotient is its pseudocolimit, and the kernel of a morphism is its pseudolimit.  The resulting factorization is one of the ones arising in the [[canonical model structure]] on any 2-category.

1. Continuing with $V=Cat$, let $H$ be the 2-category on $z,0,1$ with $H(0,1)=*$, $H(z,0) = \mathbf{2}$, and $H(z,1)$ the [[walking structure|walking]] [[isomorphism]].  Then kernel data is a 2-cell, and its quotient is its [[coinverter]].  The kernel of a morphism is sometimes called its [[invertee]].  Since coinverters are epic, the adjunction is idempotent: thus a morphism is a coinverter iff it is the coinverter of its invertee, and a 2-cell is an invertee iff it is the invertee of its coinverter.

1. Finally with $V=Cat$, let $H$ be the 3-truncated augmented [[simplex category]] with additional 2-cells added, in such a way that kernel data is *codescent data* and the quotient of such data is a [[codescent object]].  Then the factorization produced in $Cat$ consists of a bijective-on-objects functor followed by a fully faithful one.


## Factorization systems

In some of the above examples, the resulting factorization of a morphism is not what one would hope for.  In particular, it need not give a [[factorization system]] of any kind.  However, the adjunction does induce a [[comonad]] $Q_1 = quot \circ ker$ on $[\mathbf{2},C]$ such that $dom(Q_1(f)) = dom(f)$.  This is the "left half" of the factorization obtained in this way; the "right half" $R_1$ is merely a [[pointed endofunctor]] such that $cod(R_1(f)) = cod(f)$.  The [[algebra for an endofunctor|algebras]] for $R_1$ are usually what one would hope for as the "right class" of the (weak) factorization systems intuitively associated to the above examples.

Now this data is exactly the required input for the construction of a *free* [[algebraic weak factorization system]].  If $C$ is sufficiently well-behaved (such as [[locally presentable category|locally presentable]]), then this free nwfs exists, and gives the factorizations we would hope for in most cases.  It is constructed by (possibly transfinite) iteration, i.e. we take the quotient of the kernel, then take the quotient of the kernel of the right half of the resulting factorization, and so on.  The resulting monad $R$ is usually [[free monad|algebraically-free]] on $R_1$, and thus the $R$-[[algebra for a monad|algebras]] are again just what we would expect.

For example, in the coinverter-invertee example above, the right clas of the factorization system produced in this way consists of [[conservative functor|conservative]] functors.


## Related concepts

* [[kernel]], [[cokernel]]

* **generalized kernel**

## References

This sort of idea has been thought of by various people at various times.  The above version, especially the view of factorization systems, is a slight modification of one presented by [[Richard Garner]] to the Sydney category seminar in February 2010.  Other references include

* Betti, Schumacher, and [[Ross Street|Street]], "Factorizations in bicategories" (unpublished)

* Betti, "Adjointness in descent theory", JPAA

* [[Mathieu Dupont]], *Abelian categories in dimension 2*, [arXiv:0809.1760](http://arxiv.org/abs/0809.1760), section 1.2.2


[[!redirects generalized kernels]]
[[!redirects generalized cokernel]]
[[!redirects generalized cokernels]]
