

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

A *strongly $\infty$-connected site* is a [[site]] satisfying sufficient conditions to make the [[(∞,1)-sheaf (∞,1)-topos]] over it a [[strongly ∞-connected (∞,1)-topos]].


## Definition

+-- {: .un_def}
###### Definition


Let $C$ be a locally and globally [[∞-connected site]]; we say it is a **strongly $\infty$-connected site** if it is also a [[cosifted (∞,1)-category]].

=--

+-- {: .un_remark}
###### Remark

If $C$ is in addition an [[∞-local site]] then it is an [[∞-cohesive site]].

=--

## Properties


+-- {: .un_prop}
###### Proposition

If $C$ is a strongly $\infty$-connected site, then the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over it is a [[strongly ∞-connected (∞,1)-topos]]. 

=--


+-- {: .proof}
###### Proof

We need to check that the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]-functor $\Pi : Sh_{(\infty,1)}(C) \to \infty Grpd$ preserves finite [[(∞,1)-product]]s.

By the discussion at [[∞-connected site]] we have that $\Pi$ is given by the [[(∞,1)-colimit]] [[(∞,1)-functor]] $\lim_\to : Func(C^{op}, \infty Grpd) \to \infty Grpd$. On the [[opposite (∞,1)-category|opposite]] and therefore [[sifted (∞,1)-category]] $C^{op}$ these preserve finite [[(∞,1)-product]]s.

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

  * [[strongly connected site]] / **strongly ∞-connected site**

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]], [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]





[[!redirects strongly ∞-connected site]]

[[!redirects strongly ∞-connected sites]]
[[!redirects strongly infinity-connected sites]]
