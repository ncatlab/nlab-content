
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

An _iso-inserter_ is a particular kind of [[2-limit]] in a [[2-category]], which universally inserts an [[isomorphism|invertible]] [[2-morphism]] between a pair of parallel 1-morphisms.

## Definition

Let $f,g\colon A\rightrightarrows B$ be a pair of parallel 1-morphisms in a 2-category.  The **iso-inserter** of $f$ and $g$ is a universal object $V$ equipped with a morphism $v\colon V\to A$ and an invertible 2-morphism $\alpha\colon f v \xrightarrow{\cong} g v$.

More precisely, universality means that for any object $X$, the induced functor
$$Hom(X,V) \to IsoIns(Hom(X,f),Hom(X,g)) $$
is an equivalence, where $IsoIns(Hom(X,f),Hom(X,g))$ denotes the category whose objects are pairs $(u,\beta)$ where $u\colon X\to A$ is a morphism and $\beta\colon f u \xrightarrow{\cong} g u$ is an invertible 2-morphism.  If this functor is an *isomorphism* of categories, then we say that $V\xrightarrow{v} A$ is a **strict iso-inserter**.

Iso-inserters and strict iso-inserters can be described as a certain sort of [[weighted limit|weighted]] 2-limit, where the diagram shape is the [[walking structure|walking]] parallel pair $P = (\cdot \rightrightarrows\cdot)$ and the weight $P\to Cat$ is the diagram
$$1 \;\rightrightarrows\; Iso$$
where $1$ is the [[terminal category]] and $Iso$ is the walking [[isomorphism]].

An iso-inserter in $K^{op}$ (see [[opposite 2-category]]) is called a **co-iso-inserter** in $K$.

## Properties

* Any iso-inserter is a [[faithful morphism]], and also a [[conservative morphism]], but not in general a [[fully faithful morphism]].

* Any strict iso-inserter is, in particular, an iso-inserter.  (This is not true for all strict 2-limits.)

* Since $Iso$ is [[equivalence of categories|equivalent]] to $1$, iso-inserters (but not strict iso-inserters) can equivalently be described as the [[conical limit]] of a diagram of shape $P$, which might be called a (non-strict) *pseudo-equalizer*.  A strict pseudo-equalizer---that is, a [[strict pseudolimit]] of a diagram of shape $P$---is not the same as a strict isoinserter, but if it exists, a strict pseudo-equalizer is also, in particular, a (non-strict) iso-inserter.  The relationship between isoinserters and pseudoequalizers is analogous to the relationship between [[iso-comma-objects]] and [[pseudo-pullbacks]].

* Iso-inserters can be constructed as an [[inserter]] followed by an [[inverter]] (for both the strict and non-strict versions).  In particular, it follows that strict iso-inserters are a type of [[PIE-limit]].

[[!redirects isoinserters]]
[[!redirects strict isoinserter]]
[[!redirects strict isoinserters]]
[[!redirects co-isoinserter]]
[[!redirects co-isoinserters]]
[[!redirects strict co-isoinserter]]
[[!redirects strict co-isoinserters]]
[[!redirects iso-inserter]]
[[!redirects iso-inserters]]
[[!redirects strict iso-inserter]]
[[!redirects strict iso-inserters]]
[[!redirects co-iso-inserter]]
[[!redirects co-iso-inserters]]
[[!redirects strict co-iso-inserter]]
[[!redirects strict co-iso-inserters]]
[[!redirects pseudo-equalizer]]
[[!redirects strict pseudo-equalizer]]
[[!redirects biequalizer]]
