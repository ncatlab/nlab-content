
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _equifier_ is a particular kind of [[2-limit]] in a [[2-category]], which universally renders a pair of parallel [[2-morphism]] equal.

## Definition

Let $f,g\colon A\rightrightarrows B$ be a pair of parallel 1-morphisms in a 2-category and let $\alpha,\beta\colon f\rightrightarrows g$ be a pair of parallel 2-morphisms.  The **equifier** of $\alpha$ is a universal object $V$ equipped with a morphism $v\colon V\to A$ such that $\alpha v = \beta v$.

More precisely, universality means that for any object $X$, the induced functor
$$Hom(X,V) \to Hom(X,A)$$
is fully faithful, and its [[replete image]] consists precisely of those morphisms $u\colon X\to A$ such that $\alpha u=\beta u$.  If the above functor is additionally an *isomorphism* of categories onto the exact subcategory of such $u$, then we say that $V\xrightarrow{v} A$ is a **strict equifier**.

Equifiers and strict equifiers can be described as a certain sort of [[weighted limit|weighted]] 2-limit, where the diagram shape is the [[walking structure|walking]] parallel pair of 2-morphisms $P$, and the weight $P\to Cat$ is the diagram
$$\array{ & \to \\ 1 & \Downarrow\Downarrow & Ppr\\ & \to } $$
where $1$ is the [[terminal category]] and $Ppr$ is the walking [[parallel pair]] of arrows.  Note that this cannot be re-expressed as any sort of [[conical limit|conical]] 2-limit.

An equifier in $K^{op}$ (see [[opposite 2-category]]) is called a **coequifier** in $K$.

## Properties

* The above explicit definition makes it clear that any equifier is a [[fully faithful morphism]].

* Any strict equifier is, in particular, an equifier.  (This is not true for all strict 2-limits.)

* Strict equifiers are, by definition, a particular case of [[PIE-limits]].


[[!redirects equifiers]]
[[!redirects strict equifier]]
[[!redirects strict equifiers]]
[[!redirects coequifier]]
[[!redirects coequifiers]]
[[!redirects strict coequifier]]
[[!redirects strict coequifiers]]
