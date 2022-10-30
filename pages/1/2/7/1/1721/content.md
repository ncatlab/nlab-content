
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called generalized Eilenberg-Steenrod cohomology is really the general _fully abelian_ subcase of [[cohomology]]. 

This means that generalized Eilenberg-Steenrod cohomology is the [[cohomology]] in an [[(∞,1)-category]] $\mathbf{H}$ that happens to be a [[stable (∞,1)-category]].

The archetypical example of this is $\mathbf{H} = Sp(Top)$, the [[stable (∞,1)-category of spectra]] and this is the context in which generalized Eilenberg-Steenrod cohomology is usually understood. So


+-- {: .standout}

Generalized Eilenberg-Steenrod cohomology is 
[[cohomology]] $H(X,A)$ with coefficient object $A$ a [[spectrum]].

=--

## The Eilenberg-Steenrod axioms 

**remark** Originally Eilenberg and Steenrod had written down axioms that characterized the behaviour of ordinary integral cohomology, what is now understood to be cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]. Generalized Eilenberg-Steenrod cohomology is originally defined as anything that satisfies this list of axioms except the first one. Later it was proven, by the [[Brown representability theorem]], that all the models for these axioms arise in terms of homotopy classes of maps into a [[spectrum]]. In our revisionist perspective above, we take this historically secondary point of view as the conceptually primary one.

The Eilenberg-Steenrod axioms are this:


+-- {: .num_defn}
###### Definition

A [[cohomology theory]] is a collection $\{A^n\}_{n \in \mathbb{Z}}$ of [[functor]]s

$$
  A^n : Top^{op} \to Ab
$$

from the category [[Top]] of [[topological space]]s to the category [[Ab]] of abelian groups, that satisfies the following axioms, for all $n \in \mathbb{Z}$:

1. if $f : X \to Y$ is a [[weak homotopy equivalence]] then $A^n(f) : A^n(Y) \to A^n(X)$ is an [[isomorphism]];

   i.e. $A^n$ is a [[homotopical functor]] with respect to the standard structure of a [[homotopical category]] on [[Top]],

1. ...

1. ...

1. ...

1. ...

=--

## Examples 


* [[ordinary cohomology]]: [[Eilenberg?Mac Lane spectrum]]
* [[K-theory]]: [[K-theory spectrum]]
* [[tmf]]

* [[cobordism cohomology theory]]

* [[Morava K-theory]], [[integral Morava K-theory]]

* [[Morava E-theory]]

## Related concepts

* [[Brown representability theorem]]

* [[homology theory]]

* [[bivariant cohomology theory]]

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]

## References 

A pedagogical introduction to [[spectrum|spectra]] and generalized (Eilenberg-Steenrod) cohomology is in

* [[John Baez]], [TWF 149](http://math.ucr.edu/home/baez/twf_ascii/week149) 

A comprehensive account is in 

* _Generalized cohomology_ ([[GeneralizedCohomology.pdf:file]])


More references relating to the [[nPOV]] on cohomology include:

* [[Mike Hopkins]], _Complex oriented cohomology theories and the language of stacks_ course notes ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* [[Jacob Lurie]],  _[[A Survey of Elliptic Cohomology - cohomology theories]]_


[[!redirects generalized (Eilenberg?Steenrod) cohomology]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg?Steenrod) cohomology theory]]

[[!redirects generalized (Eilenberg--Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology theories]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theories]]

[[!redirects generalised (Eilenberg-Steenrod) cohomology]]
[[!redirects generalised (Eilenberg?Steenrod) cohomology]]
[[!redirects generalised (Eilenberg--Steenrod) cohomology]]
[[!redirects generalised (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalised (Eilenberg?Steenrod) cohomology theory]]
[[!redirects generalised (Eilenberg--Steenrod) cohomology theory]]
[[!redirects Eilenberg-Steenrod cohomology]]
[[!redirects Eilenberg?Steenrod cohomology]]
[[!redirects Eilenberg--Steenrod cohomology]]
[[!redirects Eilenberg-Steenrod cohomology theory]]
[[!redirects Eilenberg?Steenrod cohomology theory]]
[[!redirects Eilenberg--Steenrod cohomology theory]]

[[!redirects Eilenberg-Steenrod axioms]]

[[!redirects generalized cohomology theory]]
[[!redirects generalized cohomology theories]]
[[!redirects generalised cohomology theory]]
[[!redirects generalised cohomology theories]]
[[!redirects cohomology theories]]
[[!redirects cohomology theory]]