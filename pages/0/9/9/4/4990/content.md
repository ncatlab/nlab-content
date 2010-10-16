
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A *locally connected site* is a [[site]] satisfying sufficient conditions to make its [[topos of sheaves]] into a [[locally connected topos]].

## Definition

Let $C$ be a small [[site]]; we say it is a **locally connected site** if all covering [[sieves]] of any object $U\in C$ are [[connected category|connected]], as full subcategories of the [[slice category]] $C/U$.  (In particular, this means that all covering families are [[inhabited set|inhabited]].)

## Locally connected topoi from sites

If $C$ is a locally connected site, then we claim that $Sh(C)$ is a [[locally connected topos]], i.e. that the [[inverse image functor]] $L Const\colon Set \to Sh(C)$ has a left adjoint $\Pi_0$.  To see this, observe that the constant *presheaf* functor $Const \colon Set \to Psh(C)$ has a left adjoint given by taking colimits along $C^{op}$.  But if $C$ is locally connected, then every constant presheaf is a sheaf.  So $L Const$ is just a factorization of $Const$ through $Sh(C)$, and thus it also has a left adjoint.

If $C$ furthermore has a [[terminal object]], then colimits along $C^{op}$ preserve the terminal object, so that $Sh(C)$ is moreover a [[connected topos]].

Note that a non-locally-connected site can still give rise to a locally connected topos of sheaves, but every locally connected topos can be defined by *some* locally connected site.

## Related concepts

* [[locally contractible site]] / [[locally contractible (∞,1)-topos]]

* **locally connected site** / [[locally ∞-connected site]]

* [[cohesive site]] / [[(∞,1)-cohesive site]]




[[!redirects locally connected sites]]
