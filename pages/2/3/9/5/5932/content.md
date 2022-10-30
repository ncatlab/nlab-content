

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[homomorphism]] of [[schemes]] $f \colon Y\to X$ is 

1. __finitely presented at__ $x\in X$ if there is an affine 
[[open neighborhood]] $U\ni x$ and an affine open set $V\subset Y$, $f(V)\subset U$ such that $\mathcal{O}_Y(V)$ is [[finitely presented algebra|finitely presented]] as an $\mathcal{O}_X(U)$-[[associative algebra|algebra]]. 

1. __locally finitely presented__ if it is finitely presented at each $x\in X$. 

1. __finitely presented__ if it is locally finitely presented, [[quasicompact morphism|quasicompact]] and [[quasiseparated morphism|quasiseparated]].  

1. __essentially finitely presented__ if it is a localization of a finitely presented morphism.  

## Example

A standard open $Spec(R[\{s\}^{-1}]) \longrightarrow Spec(R)$ ([[Zariski topology]]) is of finite presentation. More generally, an [[étale morphism of schemes]] is of finite presentation (though essentially by definition so).

## Related concepts

* [[morphism of finite type]]

## References

* [[The Stacks Project]], section 28.22 _Morphism of finite presentation_

* [wikipedia: Finite, quasi-finite, finite type, and finite presentation morphisms](http://en.wikipedia.org/wiki/Glossary_of_scheme_theory#Finite.2C_quasi-finite.2C_finite_type.2C_and_finite_presentation_morphisms)

* [[David Rydh]], _Why are unramified maps not required to be locally of finite presentation?_, [MO/206333/2503](http://mathoverflow.net/a/206333/2503).

[[!redirects finitely presented morphism]]
[[!redirects locally of finite presentation]]