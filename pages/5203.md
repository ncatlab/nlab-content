
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

An inserter in $K^{op}$ (see [[opposite 2-category]]) is called a **coinserter** in $K$.

## Example: the strict 2-category of categories

In the strict 2-category of categories, inserters can be concretely described as follows.

The input data is two categories, $A$ and $B$,
and two functors, $F,G\colon A\to B$.
The objects of the inserter are pairs $(X,b)$, where $X\in A$
and $b\colon F(A)\to G(A)$.
Morphisms $(X,b)\to(X',b')$ are morphisms $f\colon X\to X'$ such that
$b'\circ F(f)=G(f)\circ b$.
The functor from the inserter to $A$ discards the data of $b$.

## Properties

* Any inserter is a [[faithful morphism]], and also a [[conservative morphism]], but not in general a [[fully faithful morphism]].

* Any strict inserter is, in particular, an inserter.  (This is not true for all strict 2-limits.)

* Strict inserters are (by definition) a particular class of [[PIE-limits]].

## Examples

* Let $C$ denote a category and $F : C \rightarrow C$ denote a functor. Then the notion of an [[algebra for an endofunctor]] of $F$ corresponds to the inserter of $F$ and $\mathrm{id}_C$, and the notion of a [[coalgebra for an endofunctor]] of $F$ corresponds to the inserter of $\mathrm{id}_C$ and $F$.

## References

* G.J. Bird, G.M. Kelly, A.J. Power, R.H. Street, _Flexible limits for 2-categories_, J. Pure and Applied Algebra __61__:1, 1-27, 1989, <a href="https://doi.org/10.1016/0022-4049(89)90065-0">doi:10.1016/0022-4049(89)90065-0</a>
* Fernando Lucatelli Nunes, _Freely generated $n$-categories, coinserters and presentations of low dimensional categories_, [arxiv/1704.04474](https://arxiv.org/abs/1704.04474)

[[!redirects inserters]]
[[!redirects strict inserter]]
[[!redirects strict inserters]]
[[!redirects coinserter]]
[[!redirects coinserters]]
[[!redirects strict coinserter]]
[[!redirects strict coinserters]]
