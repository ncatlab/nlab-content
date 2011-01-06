
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

An [[(∞,1)-site]] is **locally $\infty$-connected** if it has properties that ensure that  the [[(∞,1)-category of (∞,1)-sheaves]] over it is a [[locally ∞-connected (∞,1)-topos]]


## Definition

+-- {: .un_def}
###### Definition

Call an [[(∞,1)-site]] $C$ **locally contractible** if every constant [[(∞,1)-presheaf]] on it is an [[(∞,1)-sheaf]].

=--

## Properties

+-- {: .un_def}
###### Proposition

By the general notion of [[(∞,1)-colimit]] the constant $(\infty,1)$-presheaf functor has a left [[adjoint (∞,1)-functor]] given by taking colimits

$$
  PSh_{(\infty,1)}(C)
    \stackrel{\overset{\lim_\to}{\to}}{\underset{Const}{\leftarrow}}}
  \infty Grpd
  \,.
$$

Since the [[(∞,1)-category of (∞,1)-sheaves]] sits by a [[full and faithful (∞,1)-functor]] inside presheaves and by assumption that every constant $(\infty,1)$-presheaf is an $(\infty,1)$-sheaf, this implies that we have also [[natural transformation|natural]] [[equivalence in an (∞,1)-category|equivalences]]

$$
  Sh(X, Const S) \simeq PSh(C, Const S) \simeq \infty Grpd(\lim_\to C , S)
  \,.
$$

=--

## Related concepts



* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / **locally ∞-connected (∞,1)-site**

  * [[connected site]] / [[∞-connected (∞,1)-site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]


[[!redirects locally ∞-connected (∞,1)-site]]
[[!redirects locally ∞-connected (∞,1)-sites]]
[[!redirects locally infinity-connected (infinity,1)-sites]]

[[!redirects locally ∞-connected site]]
[[!redirects locally infinity-connected site]]

[[!redirects locally ∞-connected sites]]
[[!redirects locally infinity-connected sites]]


