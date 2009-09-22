<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

What is called generalized Eilenberg-Steenrod cohomology is really the general _fully abelian_ subcase of [[cohomology]]. 

This means that generalized Eilenberg-Steenrod cohomology is the [[cohomology]] in an [[(∞,1)-category]] $\mathbf{H}$ that happens to be a [[stable (∞,1)-category]].

The archetypical example of this is $\mathbf{H} = Sp(Top)$, the [[stable (∞,1)-category of spectra]] and this is the context in which generalized Eilenberg-Steenrod cohomology is usually understood. So


+-- {: .standout}

Generalized Eilenberg-Steenrod cohomology is 
[[cohomology]] $H(X,A)$ with coefficient object $A$ a [[spectrum]].

=--

## the Eilenberg-Steenrod axioms ##

**remark** Originally Eilenberg and Steenrod had written down axioms that characterized the behaviour of ordinary integral cohomology, what is now understood to be cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]. Generalized Eilenberg-Steenrod cohomology is originally defined as anything that satisfies this list of axioms except the first one. Later it was proven, by the [[Brown representability theorem]], that all the models for these axioms arise in terms of homotopy classes of maps into a [[spectrum]]. In our revisionist perspective above, we take this historically secondary point of view as the conceptually primary one.

The Eilenberg-Steenrod axioms are this:


**Definition**

A [[cohomology theory]] is a collection $\{A^n\}_{n \in \mathbb{Z}}$ of [[functor]]s

$$
  A^n : Top^{op} \to Ab
$$

from the category [[Top]] of [[topological space]]s to the category [[Ab]] of abelian groups, that satisfies the following axioms, for all $n \in \mathbb{Z}$:

1. if $f : X \to Y$ is a [[weak homotopy equivalence]] then $A^n(f) : A^n(Y) \to A^n(X)$ is an [[isomorphism]];

   i.e. $A^n$ is a [[homotopical functor]] with respect to the standard structure of a [[homtopical category]] on [[Top]],

1. ...

1. ...

1. ...

1. ...

# Examples #


* [[Eilenberg?Mac Lane spectrum]]
* [[K-theory spectrum]]
* [[tmf]]


# References #

A pedagogical introduction to [[spectrum|spectra]] and generalized (Eilenberg-Steenrod) cohomology is in

* [[John Baez]], [TWF 149](http://math.ucr.edu/home/baez/twf_ascii/week149) .

A general discussion of cohomology with an emphasis on [[nonabelian cohomology]] and on [[Postnikov system]]s is in

* [[John Baez]], [[Mike Shulman]], _Lectures on n-Categories and Cohomology_ ([pdf](http://math.ucr.edu/home/baez/cohomology.pdf), [[Lectures on n-Categories and Cohomology|nLab]])

In particular a remark on the relation between [[Postnikov system]]s and [[Eilenberg?MacLane spectrum|Eilenberg-MacLane cohomology]] is in the discussion beginning at the bottom of page 24.



[[!redirects generalized (Eilenberg?Steenrod) cohomology]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg?Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology theory]]
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