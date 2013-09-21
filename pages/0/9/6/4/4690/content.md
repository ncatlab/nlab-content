
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents
* table of contents
{:toc}

## Idea

The _Einstein-Hilbert action_ is the [[action functional]] that defines the dynamics of [[gravity]] in [[general relativity]]. It is a canonical invariant of [[pseudo-Riemannian manifold]]s.

## Definition

For $(X,g)$ a [[Riemannian manifold]] or [[pseudo-Riemannian manifold]], its **vacuum Einstein-Hilbert action** is the number

$$
  (X,g) \mapsto \int_X R(g) dvol(g)
  \,,
$$

where

* $R(g) : X\to \mathbb{R}$ is the [[scalar curvature]] function of the [[metric]] $g$;

* $dvol(g)$  is the [[volume form]] defined by the metric

* $\int_X$ is [[integration of differential forms]] over $X$.

If the metric is instead encoded in terms of an [[Poincare group]]-[[connection on a bundle|connection]] $\nabla$ (the [[first-order formulation of gravity]]) then (for $dim X = 4$ and assuming for simplicity that the underlying bundle is trivial) this is equivalently

$$
  (X,\nabla) \mapsto \int_X \langle R \wedge e \wedge e \rangle
  \,,
$$

where now

* $R$ denotes the [[curvature]] 2-form of the [[orthogonal group]]-connection part of $\nabla$;

* $e$ denotes the [[vielbein]], (the translation part of the connection 1-form);

* $\langle -\rangle$ is the [[invariant polynomial]] which in terms of the canonical basis has components $(\epsilon_{a b c d})$.

This extends to an [[action functional]] for gravity coupled to "matter" (which in the context of [[general relativity]] conventionally means every other field, for instance the [[electromagnetic field]]) by simply adding the matter action on a given gravitational background

$$
  (X,g,\phi) \mapsto \int_X (L_{EH}(g) + L_\phi(g)) d vol(g)
  \,.
$$


The [[critical point]]s of the Einstein-Hilbert action define the physically realized [[spacetime]]s. This are [[Einstein's equations]] (the [[Euler-Lagrange equation]]s of this action)

$$
  \delta S_{EH}(g) = 0
  \,.
$$

(...)

## History
 {#History}

Historically, Einstein had been working towards what today are called [[Einstein's equations]] over some time. What is today called the [[Einstein tensor]] in the equation had been missing the trace term in one of hist first publications, and other things remained unclear. Einstein was working with the 10 coordinate components of these [[tensors]] and trying to make the theory match classical [[Newtonian physics]] in the right limit. The "[[general covariance]]" of the equations made this a subtle problem, at least at the times back then when these issues were just beginning to be appreciated.

Hilbert was following these developments, also hearing Einstein talk about them. Apparently at some point Hilbert, who believed in the axiomatic foundation of physics -- the [[Hilbert's sixth problem]] -- decided that whatever the correct equations of motion are, they ought to follow from an [[action principle]], hence that they characterize the [[critical points]] of an [[action functional]] on the space of [[pseudo-Riemannian metrics]] on some [[smooth manifold]]. Second he observed that the most obvious such functional with the right [[symmetry]] properties  is the [[integral]] over the [[Riemann scalar curvature]] times the [[volume form]] of the given metric (hence the "Einstein-Hilbert action"). He computed the [[variational calculus|variational derivative]] of this and thereby found [[Einstein's equations]] apparently around the same time if not a little bit before Einstein published the final version of his theory.

In ([Sauer-Majer, from p. 402](#SauerMajer)) a talk of Hilbert  is reproduced reviewing Einstein's work, from the point of view of Hilbert having known the right answer all along from the variational principle (hence from the axioms). Einstein's struggle (until a few days before the lecture was given!) with finding the right equations of gravity. This comment culminates on ([Sauer-Majer, from p. 405](#SauerMajer)) with the curious remark, paraphrasing just a little: that the fact that Einstein after his "colossal detour" ends up with the same equations of motion as Hilbert already had is a "nice consistency check" ( _sch&#246;ne Gew&#228;hr_ )


In Constance Reid's biography of Hilbert here, it says in Chapter XVII the following

> In G&#246;ttingen, in the weekly Hilbert-Debye seminars, it seemed to those few students who were left $[$ due to WWI $]$ that the "living pulse" of physical research was at their finger tips. The work of Einstein as he pressed forward toward a general theory of relativity was followed with great interest. Also followed was the work of others who were trying to reach the same goal. Hilbert was especially fascinated by the ideas of Gustav Mie, then in Greifswald, who was attempting to develop a theory of matter on the fundamentals of the relativity principle; and in his own investigations he was able to bring together Mie's program of pure field theory and Einstein's theory of gravitation. At the same time, while Einstein was attempting in a rather roundabout way to develop the binding laws for the 10 coefficients of the differential form which determines gravitation, Hilbert independantly solved the problem in a different, more direct way. Both men arrived at almost the same time at the same goal. As the western front settled down for the winter, Einstein presented his two papers, "On general relativity theory" to the Berlin Academy on November 11 and 25; Hilbert presented his first note on "The foundations of physics" to the Royal Society of Science in Gottingen on November 20, 1915. It was a remarkable coincidence ... but even more remarkable, according to $[$Max$]$ Born (who was now in Berlin with Einstein), was the fact that it led, not to a controversy over priority, but to a series of friendly encounters and letters. Hilbert freely admitted, and frequently stated in lectures, that the great idea was Einstein's. 

The success of the Einstein-Hilbert [[action principle]] in the formulation of [[gravity]] probably had a considerable influence on the theoretical physics to follow and led some physcist to explore more systematically the space of action functionals invariant under prescribed symmetries and their [[critical points]]. This way notably at some point the [[supergravity]] variant of Einstein-gravity in the context of Riemannian [[supergeometry]] was found, a theory developing which eventually leads to [[superstring theory]]. These variants of course remain speculative as [[theory (physics)|theories]] of [[phenomenology|phenomenological physics]], but to some extent their development does follow Hilbert's attitude in the discovery of [[general relativity]].


## Related concepts

* [[Einstein-Maxwell theory]]

* [[Einstein-Yang-Mills theory]]

* [[Einstein-Yang-Mills-Dirac theory]]

* [[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]]

[[!include standard model of fundamental physics - table]]

## References

### General

Section _[Prequantum gauge theory and Gravity](geometry+of+physics#ActionFunctionalsForChernSimonsTypeGaugeTheories)_ at

* _[[geometry of physics]]_

### History
 {#History}

* Sauer, Majer, _David Hilbert's "Lectures on the foundations of physics"_
  {#SauerMajer}

[[!redirects Einstein-Hilbert action functional]]
