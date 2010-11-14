
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

The notion of _$(\infty,1)$-quasitopos is the [[(∞,1)-topos]]-analog of the notion of [[quasitopos]].


## Definition
An **(∞,1)-bisite** is an [[(∞,1)-category]] $C$ together with two [[(∞,1)-Grothendieck topologies]], $J$ and $K$ such that $J \subseteq K$. 

## Definition

Let $C$ be an [[(∞,1)-bisite]]. Say an [[(∞,1)-presheaf]] $F$ on $C \in (\infty,1)PSh_C$ is $\left(J,K\right)$-**biseparated** if it an $(\infty,1)$-sheaf for $J$ for every $K$-covering [[sieve]] $U \to X$ in $C$ we have that the induced morphism

$$
  (\infty,1)PSh_C(X,F) \hookrightarrow (\infty,1)PSh_C(U,F)
$$

in [[∞Grpd]] is a [[full and faithful (∞,1)-functor]].

We say it is $n-\left(J,K\right)$-**biseparated** if 

the induced morphism

$$
  (\infty,1)PSh_C(X,F) \hookrightarrow (\infty,1)PSh_C(U,F)
$$

is an [[n-truncated object in an (∞,1)-category|(n-1)-truncated object]] in the [[over quasi-category|(∞,1)-overcategory]] $\left(\infty-Gpd\right)/(\infty,1)PSh_C(U,F)$.

A **(Grothendieck) $(\infty,1)$-quasitopos** is an [[(∞,1)-category]] that is [[equivalence of quasi-categories|equivalent]] to the full [[sub-(∞,1)-category]] of some $(\infty,1)PSh_C$ on the $n-\left(J,K\right)$-**biseparated** $(\infty,1)$-presheaves, on some (∞,1)-bisite $\left(C,J,K\right)$.


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

The definition as it stands, originated out of a discussion between [[Urs Schreiber]] and [[David Carchedi]]. The suggestion to rephrase the definition in terms of bisites came from [[Mike Shulman]].

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
[[!redirects (∞,1)-bisite]]



