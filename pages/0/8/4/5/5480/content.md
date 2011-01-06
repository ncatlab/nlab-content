

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

A *totally $\infty$-connected site* is a [[site]] satisfying sufficient conditions to make the [[(∞,1)-sheaf (∞,1)-topos]] over it a [[totally ∞-connected (∞,1)-topos]].


## Definition

+-- {: .un_prop}
###### Proposition


Let $C$ be an [[∞-connected site]]; we say it is a **strongly $\infty$-connected site** if it is also a [[cofiltered (∞,1)-category]].

=--

## Properties


+-- {: .un_prop}
###### Proposition

If $C$ is a totally $\infty$-connected site, then the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over it is a [[totally ∞-connected (∞,1)-topos]]. 

=--


+-- {: .proof}
###### Proof

We need to check that the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]-functor $\Pi : Sh_{(\infty,1)}(C) \to \infty Grpd$ preserves [[finite limit|finite]] [[(∞,1)-limit]]s.

By the discussion at [[∞-connected site]] we have that $\Pi$ is given by the [[(∞,1)-colimit]] [[(∞,1)-functor]] $\lim_\to : Func(C^{op}, \infty Grpd) \to \infty Grpd$. On the [[opposite (∞,1)-category|opposite]] and therefore [[filtered (∞,1)-category]] $C^{op}$ these preserve finite [[(∞,1)-limit]]s.

=--

## Examples

* [[CartSp]], [[ThCartSp]].

## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / **totally ∞-connected site**

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]





[[!redirects totally ∞-connected site]]

[[!redirects totally ∞-connected sites]]
[[!redirects totally infinity-connected sites]]
