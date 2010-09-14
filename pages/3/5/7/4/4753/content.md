
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Type-theoretic definition of category
* table of contents
{: toc}

## Motivation

There are two broad definitions of [[category]] in the literature: one which immediately generalises to the usual definition of [[internal category]] and one which immediately generalises to the usual definition of [[enriched category]].

Here we consider the latter definition and show how it may naturally be expressed in [[dependent type theory]].  In a [[type theory]] where [[types]] are [[presets]] (without an inherent [[equality predicate]]), it is not manifestly possible to express so-called [[evil]] ideas in category theory.


## Definition

In a [[dependent type theory]] with [[dependent record type|dependent record types]] we can define a type of categories as follows (using a two-dimensional syntax):
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
Here, $\mathrm{Type}$ is a type of types, and $\mathrm{Type}_=$ is a type of types with equality predicates (we may or may not have $\mathrm{Type}=\mathrm{Type}_=$).

The two-dimensional syntax is convenient to allow inference of [[implicit parameter|implicit parameters]], and to signify notation. We read the horizontal line as a rule, so for instance the second line means that whenever $a$ and $b$ have type $\mathrm{Obj}$, then we have a type $\hom(a,b)$ (with equality).

The notation $p\coloneq P$ signifies that $p$ is a proof of the [[proposition]] $P$ (under [[propositions as types]], this may be the same as $p\colon P$, but many type theories treat propositions as distinct from types).

So the above defines that a category is a record consisting of a type of objects, and for each pair of objects a type of homomorphisms between them, and also identity and composition operations satisfying unit laws and associativity.


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
