
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #AccessibleMonad}
###### Definition

An _[[accessible monad]]_ is a [[monad]] on an [[accessible category]] whose underlying [[functor]] is an [[accessible functor]].

=--

## Properties

### Category of algebras over an accessible monad
 {#CategoryOfAlgebras}

+-- {: .num_prop}
###### Proposition

The Eilenberg-Moore category of a $\kappa$-accessible monad, def. \ref{AccessibleMonad}, is a  $\kappa$-[[accessible category]]. If in addition the category on which the monad acts is a $\kappa$-[[locally presentable category]] then so is the EM-category.


=--

([Adamek-Rosicky, 2.78](#AdamekRosicky))

Moreover, let $C$ be a [[topos]]. Then

* if a [[monad]] $T : C \to C$ has a [[right adjoint]] then $T Alg(C)= C^T$ is itself a topos;

* if a [[comonad]] $T : C \to C$ is [[exact functor|left exact]], then $T CoAlg(C) = C_T$ is itself a topos.

See at _[[topos of algebras over a monad]]_ for details.


## References

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}
