
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

Informally, a **free functor** is a [[left adjoint]] to a [[forgetful functor]]. (This is informal because the concept of forgetful functor is informal; *any* functor might be viewed as forgetful, so *any* left adjoint might be viewed as free, while in practice only some are.)


## Examples

* the [[free monoid]] functor $Set \to Mon$

* the [[free module]] functor $Set \to K Mod$ for a [[rig]] $K$

* the [[free group]] functor $Set \to Grp$

* the [[free abelian group]] functor $Set \to Ab$

* the [[free category]] functor $Quiv \to Cat$

One formal sort of free functor is the left adjoint $C\to C^T$, where $T$ is a [[monad]] on the category $C$ and $C^T$ is its [[Eilenberg-Moore category]] (the category of $T$-algebras).  This includes all of thee examples above and many others.


## Free objects

In general, if $U: C \to D$ is thought of as a forgetful functor and $F: D \to C$ is its left adjoint, then $F(x)$ is the __free $C$-object__ on an object $x$ of $D$.

More generally, even if the entire left adjoint $F$ doesn't exist, a [[free object]] on $x$ can be defined using a universal property, as "what the value of $F(x)$ would be if $F$ existed."  Conversely, if a free object on $x$ exists for *all* $x\in D$, then the left adjoint $F$ can be assembled from them.


## Cofree functors

Dually, a __cofree functor__ is a [[right adjoint]] to a forgetful functor; these seem to be less common.  As a political joke (which works best for someone who associates political freedom with the left wing), cofree functors are sometimes called __fascist functors__.


[[!redirects free functor]]
[[!redirects free functors]]
[[!redirects free construction]]
[[!redirects free constructions]]

[[!redirects cofree functor]]
[[!redirects cofree functors]]
[[!redirects co-free functor]]
[[!redirects co-free functors]]
[[!redirects fascist functor]]
[[!redirects fascist functors]]
