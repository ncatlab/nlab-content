
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Type-theoretic definition of category
* table of contents
{: toc}

## Motivation

There are two main styles of definition of [[category]] in the literature: one which immediately generalises to the usual definition of [[internal category]] and one which immediately generalises to the usual definition of [[enriched category]].  Here we consider the latter definition, and show how it may naturally be expressed in [[dependent type theory]].

Note that in a [[type theory]] without [[identity types]], where [[types]] are [[presets]] (without an inherent [[equality predicate]]), it is not manifestly possible to express concepts that violate the [[principle of equivalence]]; in that categories are not necessarily [[strict category|strict]].  In [[homotopy type theory]], we have identity types, but they are not [[extensional type theory|extensional]]; thus it is also possible to define non-strict categories there (but there is a subtlety; see below).


## Definition

In a [[dependent type theory]] with [[dependent record type|dependent record types]] we can define a type of categories as follows.

We use a two-dimensional syntax, which is convenient to allow inference of [[implicit parameter|implicit parameters]], and to signify notation. We read the horizontal line as a rule, so for instance the second line means that whenever $a$ and $b$ have type $\mathrm{Obj}$, then we have a type $\hom(a,b)$ (with equality).

The notation $p\coloneq P$ signifies that $p$ is a proof of the [[proposition]] $P$ (under [[propositions as types]] or [[propositions as some types]], this may be the same as $p\colon P$, but many type theories treat propositions as distinct from types).

\[\begin{aligned}
  \biggl\{&\mathrm{Obj}\colon\mathrm{Type}, \\
    &\frac{a,b\colon\mathrm{Obj}}{\hom(a,b)\colon\mathrm{Type}_=}, \\
    &\frac{a\colon\mathrm{Obj}}{1_a\colon\hom(a,a)}, \\
    &\frac{f\colon\hom(b,c) \quad g\colon\hom(a,b)}{f\circ g\colon\hom(a,c)}, \\
    &\frac{g\colon\hom(a,b)}{\mathrm{left}\text{-}\mathrm{unit}\coloneq 1_b\circ g=g}, \\
    &\frac{f\colon\hom(a,b)}{\mathrm{right}\text{-}\mathrm{unit}\coloneq f\circ 1_a=f}, \\
    &\frac{f\colon\hom(c,d) \quad
        g\colon\hom(b,c) \quad h\colon\hom(a,b)}{\circ\text{-}\mathrm{assoc}\coloneq f\circ(g\circ h) =
        (f\circ g)\circ h} \\
  &\!\biggr\}
\end{aligned}\]
Here, $\mathrm{Type}$ is a type of types, and $\mathrm{Type}_=$ is a type of types with equality predicates (we may or may not have $\mathrm{Type}=\mathrm{Type}_=$).  Specifically:

* In [[extensional type theory]] (with extensional [[identity types]]), we have $\mathrm{Type} = \mathrm{Type}_=$, and the above definition simply makes no use of the equality predicate on the type of objects.  In this case we obtain [[strict categories]], although that is not immediately visible from the definition.

* In dependent type theory without identity types, basically the only option for $\mathrm{Type}_=$ is the type of [[setoids]].  In this case we obtain a notion of non-strict category, since the type of objects has no equality predicate at all.

* In [[homotopy type theory]], it is natural to take $\mathrm{Type}_=$ to be the type of [[h-sets]]: types whose identity/path types behave extensionally.  We should also restrict the [[homotopy level]] of the type of objects, however, since a true 1-category should have no more than a 1-groupoid of objects; thus $\mathrm{Type}$ in the definition above is really the type of [[h-groupoids]] instead of the type of *all* small types.  That is, we should take $\mathrm{Obj}$ to be $1$-truncated in addition to taking each $\hom(a,b)$ to be $0$-truncated.

  This gives a notion of non-strict category (since there is no equality predicate on a $1$-truncated type other than isomorphism).  However, it is not quite the right definition of "$1$-category" in homotopy type theory, because nothing requires that the paths in $\mathrm{Obj}$ are the same as the isomorphisms defined categorically.  We need to impose a version of the "completeness" condition on a [[complete Segal space]]; in other words, we require that the [[core]] of the category be the [[equivalence of groupoids|equivalent]] as a [[groupoid]] to the original type of objects.

\begin{remark}
The defined type of categories cannot itself be a member of $\mathrm{Type}$, otherwise we run into [[Girard's paradox]]. This is related to the size issues for categories. 
\end{remark}

## Related concepts

* [[fully formal definition of ETCS]]

* [[internal category in homotopy type theory]]

[[!redirects type-theoretic definition of category]]
[[!redirects type-theoretic definition of a category]]
[[!redirects type-theoretic definition of categories]]
[[!redirects type-theoretic definitions of category]]
[[!redirects type-theoretic definitions of a category]]
[[!redirects type-theoretic definitions of categories]]
[[!redirects preset-theoretic definition of category]]
[[!redirects preset-theoretic definition of a category]]
[[!redirects preset-theoretic definition of categories]]
[[!redirects preset-theoretic definitions of category]]
[[!redirects preset-theoretic definitions of a category]]
[[!redirects preset-theoretic definitions of categories]]
