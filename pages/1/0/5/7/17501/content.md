# 2-categories with contravariance

* table of contents
{:toc}

## Idea

A *2-category with contravariance* is a [[2-category]]-like structure that contains a basic notion of [[contravariant functor|contravariant morphism]].  There are multiple ways to make this precise, depending on what sort of natural transformations we include.

## No mixed-variance transformations

The simplest case is when we include only natural transformations between functors of the same variance.  In this case, for any two objects $x$ and $y$ we will have two disjoint hom-categories $hom^+(x,y)$ and $hom^-(x,y)$ whose objects are called "covariant" and "contravariant" respectively, and composition functors

$$ \begin{aligned}
hom^+(y,z) \times hom^+(x,y) &\to hom^+(x,z)\\
hom^+(y,z) \times hom^-(x,y) &\to hom^-(x,z)\\
hom^-(y,z) \times hom^+(x,y)^{op} &\to hom^-(x,z)\\
hom^-(y,z) \times hom^-(x,y)^{op} &\to hom^+(x,z)
\end{aligned} $$

Note that the variances behave like a $\mathbb{Z}/2$-[[graded category|grading]], with covariant functors considered "even" and contravariant functors "odd".  Moreover, postcomposing with a contravariant functor is a contravariant operation.

This sort of 2-category with contravariance can be described more abstractly in two ways:

* It is a [[generalized multicategory]] relative to the [[2-monad]] on [[2-Cat]] defined by $ob(T A) = ob(A)$ and $T A(x,y) = A(x,y) + A(x,y)^{op}$.

* It is an [[enriched category]] over the category $V = Cat \times Cat$ with the non-standard (and non-[[symmetric monoidal category|symmetric]]) monoidal structure
  $$(A^+,A^-)\otimes (B^+,B^-) = (A^+\times B^+ + A^-\times (B^-)^{op}, A^+\times B^- + A^- \times (B^+)^{op}). $$

The operation "$op$" can then be characterized by a [[universal property]], using the [[representable multicategory|representability]] property of a generalized multicategory or the notion of [[copowers]] in an enriched category.  See [Shulman 2016](#Shulman2016) for more details.

### Examples

* Of course, [[Cat]] with its usual notion of [[contravariant functor]].

* If $V$ is any [[symmetric monoidal category]], then $V$-categories have opposites and so we can define contravariant $V$-functors in the usual way.

* 2-categories of [[indexed categories]] and [[fibrations]] have "fiberwise" opposites and hence fiberwise contravariant morphisms.

* More generally, any 2-category with a [[duality involution]] has an underlying 2-category with contravariance, and conversely a 2-category with contravariance that has all "opposites" (characterized by a universal property as above) has a duality involution.

* For instance, if $B$ is a [[compact closed bicategory]], then its sub-bicategory of "maps" ([[left adjoint]] morphisms) has a duality involution given by the duals in $B$, and hence is a "bicategory with contravariance".


## With mixed-variance transformations

It is also possible to define natural transformations from a covariant functor to a contravariant functor or vice versa, as a special case of [[dinatural transformations]]; thus we might ask for a sort of 2-category with contravariance that includes these as well.  (This will include many of the examples above, but not $V$-enriched categories unless $V$ is cartesian monoidal, and thus also not the bicategory of maps in $B$ unless $B$ is not just compact closed but a [[cartesian bicategory]].)

Now our hom-objects will not decompose into two disjoint categories $hom^+$ and $hom^-$.  Instead we have only one hom-category, but with gradings of "even" (covariant) or "odd" (contravariant) assigned to its objects (the morphisms of our 2-category-like structure).  In the example of [[Cat]], the objects of these hom-categories will be all functors, covariant and contravariant alike, with covariant ones considered even and contravariant ones odd.

The $2$-morphisms $F\stackrel{\alpha}{\Rightarrow}G\colon C\to D$ in $Cat$ are as usual $\ob(C)$-indexed families of morphisms $FX\stackrel{\alpha_X}{\to} GX$, but the commutative diagram they will have to satisfy for each $X\stackrel{f}{\to} Y$ in $C$ depends on the combination of variances of $F$ and $G$:
$$
\array{
FX&\stackrel{Ff}{\rightarrow}&FY&&FX&\stackrel{Ff}{\rightarrow}&FY&&FX&\stackrel{Ff}{\leftarrow}&FY&&FX&\stackrel{Ff}{\leftarrow}&FY
\\\alpha_X\downarrow&&\alpha_Y\downarrow&&
\alpha_X\downarrow&&\alpha_Y\downarrow&&
\alpha_X\downarrow&&\alpha_Y\downarrow&&
\alpha_X\downarrow&&\alpha_Y\downarrow
\\GX&\stackrel{Gf}{\rightarrow}&GY&&GX&\stackrel{Gf}{\leftarrow}&GY&&GX&\stackrel{Gf}{\rightarrow}&GY&&GX&\stackrel{Gf}{\leftarrow}&GY
}$$
Note that these are the special cases of [[dinatural transformations]] between functors $C^{op}\times C\to D$ when both functors depend only on one of $C$ or $C^{op}$.  It is clear that "vertical" composition of $2$-morphisms makes sense, so we do have hom-categories whose objects are functors of both variances.  Note that if we consider transformations between functors of different variance to be graded odd and natural transformation between functors of the same variance to be graded even, then vertical composition is appropriately additive on the grading (the composition of two even morphisms, or two odd ones, is even; while the composition of an even and an odd morphism is odd).

Horizontal composition is trickier to describe.  Of course, we can compose functors of both sorts, and this is also additive on the grading.  Moreover, we can [[whisker]] a transformation of any sort by a functor of either sort on either side, and postwhiskering by an odd functor reverses the direction of a transformation.  There is an appropriate [[interchange law]] (it is just the "naturality square" for the second transformation involved), so we have something that looks sort of like a 2-category.

+--{:.standout}
**Conjecture:** Let $W$ be the category whose objects are categories with $\mathbb{Z}/2$-gradings assigned to their objects, and whose morphisms are functors preserving grading.  Then there is a [[closed monoidal category|biclosed]] (non-[[symmetric monoidal category|symmetric]]) [[monoidal category|monoidal structure]] on $W$ (or at least a [[closed category]] or [[multicategory]] structure) such that the above structure on categories, functors of both variances, and transformations assembles into a $W$-enriched category.
=--

## References

For **categories with contravariance**, see Example 4.2.9 of:

* [[Higher Operads, Higher Categories]]

For 2-categories, see:

* [[Mike Shulman]], *Contravariance through enrichment*, [arXiv](https://arxiv.org/abs/1606.05058), 2016
 {#Shulman2016}

[[!redirects 2-categories with contravariance]]
