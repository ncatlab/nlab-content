

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The generalization of the [[Artin representability theorem]] from [[algebraic geometry]] to [[spectral algebraic geometry]].

## Statement

Write $CAlg^{cn}$ for the [[(∞,1)-category]] of [[connective]] [[E-∞ rings]], and [[∞Grpd]] for that of [[∞-groupoids]].

+-- {: .num_theorem}
###### Theorem

Necessary and sufficient conditions for an [[(∞,1)-presheaf]] 

$$
  \mathcal{F} \;\colon\; CAlg^{cn}\longrightarrow \infty Grpd
$$

over some $Spec R$, on the [[opposite (∞,1)-category]] of [[connective]] [[E-∞ rings]] to be [[representable functor|represented]] by a  [[spectral Deligne-Mumford stack|spectral Deligne-Mumford n-stack]] locally of almost finite presentation over $R$:

1. For every discrete commutative ring, $\mathcal{F}(A)$ is [[n-truncated object in an (infinity,1)-topos|n-truncated]].

1. $\mathcal{F}$ is an [[∞-stack]] for the [[étale (∞,1)-site]].

1. $\mathcal{F}$ is nilcomplete, integrable, and an [[infinitesimally cohesive (∞,1)-presheaf on E-∞ rings]].

1. $\mathcal{F}$ admits a [[connective]] [[cotangent complex]].

1. the natural transformation to $Spec R$ is locally almost of finite presentation.

=--

([Lurie Rep, theorem 2](#LurieRep))


+-- {: .num_remark}
###### Remark

The condition that $\mathcal{F}$ be [[infinitesimally cohesive (∞,1)-presheaf on E-∞ rings|infinitesimally cohesive]] implies that the [[Lie differentiation]] around any point, given by restriction to [[local Artin rings]] ([[formal duals]] of [[infinitesimally thickened points]]), is a [[formal moduli problem]], hence equivalently an [[L-∞ algebra]].

=--

## Applications 

The motivating example of the Artin-Lurie representability theorem is the re-proof of the _[[Goerss-Hopkins-Miller theorem]]_. See there for more. 

## Related concepts

* [[Grothendieck existence]]

* [[Artin representability theorem]]

## References

* {#LurieRep} [[Jacob Lurie]], _[[Representability theorems]]_