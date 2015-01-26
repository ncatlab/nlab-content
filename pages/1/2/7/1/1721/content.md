
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

One may conceptualize the axioms as ensuring that certain nice properties that hold in the category Top will be preserved by our cohomology functor.

The Eilenberg-Steenrod axioms are this:


+-- {: .num_defn}
###### Definition

A [[cohomology theory]] is a collection $\{A^n\}_{n \in \mathbb{Z}}$ of [[functor]]s

$$
  A^n : Top^{op} \to Ab
$$

from the category [[Top]] of [[topological space]]s to the category [[Ab]] of abelian groups, that satisfies the following axioms, for all $n \in \mathbb{Z}$.

It may also be defined as a functor from pairs of topological spaces, if only one space is listed, the subspace is assumed to be the empty set.

Let U and X be topological spaces, such that U is a subspace of X. Notation: $(X,A) := A \hookrightarrow X$ 

1. *Additivity*: If $\coprod_i X_i = X$, then $\coprod_i A^n(X_i) = A^n(X)$.

1. *Weak homotopy equivalence*: if $f : X \to Y$ is a [[weak homotopy equivalence]] then $A^n(f) : A^n(Y) \to A^n(X)$ is an [[isomorphism]];

1. *Excision*: Let S be a subspace of U, the natural inclusion of the pair $i:(X-U, A-U) \hookrightarrow (X, A)$ induces an isomorphism $A^n(i): A^n(X-U, A-U) \to A^n(X, A)$.

1. *Exactness*: Preserves exact sequences, in other words $(A, \emptyset) \to (X, \emptyset) \to (X, A)$ ...

=--

Ordinary cohomology theories require and additional axiom, the dimension axiom $A^n(pt) = 0$.

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

**remark** Originally Eilenberg and Steenrod had written down axioms that characterized the behaviour of ordinary integral cohomology, what is now understood to be cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]. Generalized Eilenberg-Steenrod cohomology is originally defined as anything that satisfies this list of axioms except the first one. Later it was proven, by the [[Brown representability theorem]], that all the models for these axioms arise in terms of homotopy classes of maps into a [[spectrum]]. In our revisionist perspective above, we take this historically secondary point of view as the conceptually primary one.


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

[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theories]]

[[!redirects generalized (Eilenberg-Steenrod) cohomlogy theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomlogy theories]]