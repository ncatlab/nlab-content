
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

An _inserter_ is a particular kind of [[2-limit]] in a [[2-category]], which universally inserts a [[2-morphism]] between a pair of parallel 1-morphisms.

## Definition

Let $f,g\colon A\rightrightarrows B$ be a pair of parallel 1-morphisms in a 2-category.  The **inserter** of $f$ and $g$ is a universal object $V$ equipped with a morphism $v\colon V\to A$ and a 2-morphism $\alpha\colon f v \to g v$.

More precisely, universality means that for any object $X$, the induced functor
$$Hom(X,V) \to Ins(Hom(X,f),Hom(X,g)) $$
is an equivalence, where $Ins(Hom(X,f),Hom(X,g))$ denotes the category whose objects are pairs $(u,\beta)$ where $u\colon X\to A$ is a morphism and $\beta\colon f u \to g u$ is a 2-morphism.  If this functor is an *isomorphism* of categories, then we say that $V\xrightarrow{v} A$ is a **strict inserter**.

Inserters and strict inserters can be described as a certain sort of [[weighted limit|weighted]] 2-limit, where the diagram shape is the [[walking structure|walking]] parallel pair $P = (\cdot \rightrightarrows\cdot)$ and the weight $P\to Cat$ is the diagram
$$1 \;\rightrightarrows\; I$$
where $1$ is the [[terminal category]] and $I$ is the [[interval category]].  Note that inserters are not equivalent to any sort of [[conical limit|conical]] 2-limit.

## Properties

* Any inserter is a [[faithful morphism]], but not in general fully faithful.

* Any strict inserter is, in particular, an inserter.  (This is not true for all strict 2-limits.)

* Strict inserters are (by definition) a particular class of [[PIE-limits]].

[[!redirects inserters]]
[[!redirects strict inserter]]
[[!redirects strict inserters]]
