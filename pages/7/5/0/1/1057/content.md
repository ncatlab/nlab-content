
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##  Definition 

A **strong monomorphism** in a [[category]] $C$ is a [[monomorphism]] which is right [[orthogonality|orthogonal]] to any [[epimorphism]].  The dual notion is, of course, [[strong epimorphism]].


## Remarks 

* If $C$ has [[coequalizers]], then any morphism which is right orthogonal to epimorphisms must automatically be a monomorphism.

* Every [[regular monomorphism]] is strong.

* Every strong monomorphism is [[extremal monomorphism|extremal]]; the converse is true if $C$ has [[pushouts]].


## Examples 

* A nice example of strong monomorphisms in a category are the subspace inclusions in the category of [[diffeological spaces]].  In this setting, any subset $Y$ of a diffeological space $X$ is again a diffeological space.  If smooth, the inclusion $\iota:Y \rightarrow X$ is always a monomorphism, but it is a strong monomorphism if and only if $Y$ has "enough" plots, that is if $\varphi: U\rightarrow Y$ is a plot if and only if the composite $\iota\varphi: U\rightarrow X$ is a plot.

[[!redirects strong monomorphisms]]