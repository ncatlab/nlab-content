
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The generalization of a [[slice category]] to [[2-categories]].

## Definition

Let $C$ be a (non-strict) [[2-category]], and $X\in C$ an [[object]].  Then the **slice 2-category** $C/X$ has:

* as objects, the 1-[[morphisms]] $a\colon A\to X$ in $C$;

* as 1-morphisms from $a\colon A\to X$ to $b\colon B\to X$, the pairs $(f,\phi)$ where $f\colon A\to B$ is a 1-morphism in $C$ and $\phi\colon a \cong b f$ is a 2-isomorphism in $C$.

* as 2-morphisms from $(f,\phi)$ to $(g,\psi)$, the 2-morphisms $\xi\colon f \to g$ such that $(b \xi) . \phi = \psi$.

If $C$ is a [[strict 2-category]], then so is $C/X$.  Moreover, in this case, we can also define the **strict-slice 2-category** to be the subcategory $C/_s X$ of $C/X$ containing all the objects, only those morphisms $(f,\phi)$ such that $\phi$ is an identity, and all 2-morphisms between these.

If, on the other hand, we do not require $\phi : a \to b f$ to be invertible, then we obtain the **lax-slice 2-category** $C\sslash X$.  This can be regarded as an [[F-category]] whose tight morphisms are those where $\phi$ *is* invertible (or an identity).

Dually, the morphisms in the **colax-slice 2-category** involve a $\phi : b f \to a$.  It is not clear whether there is a universally accepted convention as to which is the lax-slice and which is the colax-slice; the one adopted here is that used by [Johnson-Yau](#JohnsonYau) and is such that for the lax-slice $C\sslash X$, the canonical transformation
\begin{tikzcd} C/\!/ X \ar[r] \ar[d] \ar[dr,phantom,"\Downarrow"] & C \ar[d,equals] \\ 1 \ar[r,"X"'] & C \end{tikzcd}
is a [[lax natural transformation]].

Finally, the subcategory of $C/X$ whose objects are the [[fibration in a 2-category|fibrations]] and whose morphisms are the maps of fibrations is denoted $Fib(X) = Fib_C(X)  = Fib_C/X$, and may be called the **fibrational-slice 2-category**.  Similarly we have the **opfibrational-slice** $Opf(X)$.

## Remarks

When $C$ is a 1-category, the slice, strict-slice, lax- and colax-slice, and fibrational- and opfibrational-slice 2-categories all coincide with the usual [[slice category]].  When $C$ is a [[(2,1)-category]], then all of them coincide except the strict one.  Thus, when generalizing a concept involving slice categories from categories to 2-categories, it can sometimes be a little subtle to decide on the correct version of slice category to use.

## Related concepts

* [[michaelshulman:fibrational slice]]

* [[slice category]]

* [[slice (∞,1)-category]]

## References

* {#JohnsonYau} [[Niles Johnson]], [[Donald Yau]], _2-Dimensional Categories_ ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055))

[[!redirects slice 2-category]]
[[!redirects slice 2-categories]]
[[!redirects over 2-category]]
[[!redirects over 2-categories]]
[[!redirects strict slice 2-category]]
[[!redirects strict slice 2-categories]]
[[!redirects strict over 2-category]]
[[!redirects strict over 2-categories]]
[[!redirects lax slice 2-category]]
[[!redirects lax slice 2-categories]]
[[!redirects colax slice 2-category]]
[[!redirects colax slice 2-categories]]
[[!redirects oplax slice 2-category]]
[[!redirects oplax slice 2-categories]]
[[!redirects lax over 2-category]]
[[!redirects lax over 2-categories]]
[[!redirects colax slice 2-category]]
[[!redirects colax slice 2-categories]]
[[!redirects colax over 2-category]]
[[!redirects colax over 2-categories]]
[[!redirects strict-slice 2-category]]
[[!redirects strict-slice 2-categories]]
[[!redirects strict-over 2-category]]
[[!redirects strict-over 2-categories]]
[[!redirects lax-slice 2-category]]
[[!redirects lax-slice 2-categories]]
[[!redirects lax-over 2-category]]
[[!redirects lax-over 2-categories]]
[[!redirects colax-slice 2-category]]
[[!redirects colax-slice 2-categories]]
[[!redirects colax-over 2-category]]
[[!redirects colax-over 2-categories]]
[[!redirects fibrational-slice 2-category]]
[[!redirects fibrational-slice 2-categories]]
[[!redirects opfibrational-slice 2-category]]
[[!redirects opfibrational-slice 2-categories]]
[[!redirects fibrational slice]]
[[!redirects opfibrational slice]]
