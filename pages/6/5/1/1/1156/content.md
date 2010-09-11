

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

* [[sheaf]]

* [[2-sheaf]] / [[stack]]

* **$(\infty,1)$-sheaf** / [[∞-stack]]

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **$(\infty,1)$-sheaf** is the analog in [[(∞,1)-category]] theory of the notion of [[sheaf]] in ordinary [[category theory]].

See [[(∞,1)-category of (∞,1)-sheaves]] for more.

## Definition


Given an [[(∞,1)-site]] $C$, legt $S$ be the class of [[monomorphism in an (∞,1)-category|monomorphisms]] in the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ that correspond to [[covering]] [[(∞,1)-sieve]]s

$$
  \eta : U \hookrightarrow j(c)
$$

on objects $c \in C$, where $j$ is the [[(∞,1)-Yoneda embedding]]. 

Then an [[(∞,1)-presheaf]] $A \in PSh_{(\infty,1)}(C)$ is an **$(\infty,1)$-sheaf** if it is an $S$-[[local object]]. That is, if for all such $\eta$ the morphism

$$
  A(c) \simeq Psh_C(j(c),A) \stackrel{PSh_C(\eta,,A)}{\to}
  PSh(U,A)
$$

is an [[equivalence in a quasi-category|equivalence]].

This is the analog of the ordinary sheaf condition. The [[∞-groupoid]] $PSh_C(U,A)$ is also called the [[descent]]-[[∞-groupoid]] of $A$ relative to the covering encoded by $U$.




## Terminology

An **($\infty$,1)-sheaf** is also called an [[∞-stack]] with values in [[∞-groupoid]]s. 

The practice of writing "$\infty$-sheaf" instead of [[∞-stack]] is a rather reasonable one, since a [[stack]] is nothing but a _2-sheaf_. 

Notice however that there is ambiguity in what precisely one may mean by an $\infty$-stack: it can be an $(\infty,1)$-sheaf or more specifically a [[hypercomplete]] $(\infty,1)$-sheaf. This is a distinction that only appears in [[(∞,1)-topos]] theory, not in [[(n,1)-topos]] theory for finite $n$.

## References

Section 6.2.2 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects (infinity,1)-sheaves]]
[[!redirects (∞,1)-sheaf]]
[[!redirects (∞,1)-sheaves]]