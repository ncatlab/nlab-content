
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _$(\infty,1)$-quasitopos_ is the [[(∞,1)-topos]]-analog of the notion of [[quasitopos]].

## Definition

Let $C$ be an [[(∞,1)-site]]. Say an [[(∞,1)-presheaf]] $F$ on $C \in (\infty,1)PSh_C$ is **separated** if for every covering [[sieve]] $U \to X$ in $C$ we have that the induced morphism

$$
  (\infty,1)PSh_C(X,F) \hookrightarrow (\infty,1)PSh_C(U,F)
$$

in [[∞Grpd]] is a [[full and faithful (∞,1)-functor]].

A **(Grothendieck) $(\infty,1)$-quasitopos** is an [[(∞,1)-category]] that is [[equivalence of quasi-categories|equivalent]] to the full [[sub-(∞,1)-category]] of some $(\infty,1)PSh_C$ on the separated $(\infty,1)$-presheaves.


## Examples

For $\mathbf{H}$ a [[local (∞,1)-topos]]

$$
  \mathbf{H} \stackrel{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}}{\underset{Codisc}{\leftarrow}}
  \infty Grpd
$$

a $C$ be a site of definition for $\mathbf{H}$, the $(\infty,1)$-quasitopos on $C$ that factors the [[geometric embedding]] $Codisc \infty Grpd \hookrightarrow \mathbf{H}$

$$
  \infty Grpd
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc(\mathbf{H})
   \stackrel{\overset{concretization}{\leftarrow}}{\underset{}{\hookrightarrow}}
  \mathbf{H}
$$

is that of **concrete objects** in $\mathbf{H}$, the analog of [[concrete sheaves]].


## Related concepts

* [[quasitopos]]

* **$(\infty,1)$-quasitopos**


[[!redirects (∞,1)-quasitopos]]
[[!redirects (∞,1)-quasitoposes]]
[[!redirects (∞,1)-quasitopoi]]
[[!redirects Grothendieck (∞,1)-quasitopos]]
[[!redirects Grothendieck (∞,1)-quasitoposes]]
[[!redirects Grothendieck (∞,1)-quasitopoi]]
[[!redirects (infinity,1)-quasitoposes]]
[[!redirects (infinity,1)-quasitopoi]]
[[!redirects Grothendieck (infinity,1)-quasitopos]]
[[!redirects Grothendieck (infinity,1)-quasitoposes]]
[[!redirects Grothendieck (infinity,1)-quasitopoi]]



