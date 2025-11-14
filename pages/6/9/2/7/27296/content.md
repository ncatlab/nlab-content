

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[physics]], specifically in [[field theory]], a *gauge field* is a type of [[field (physics)|field]] in [[gauge theory]]. In the [[standard model of particle physics]], gauge fields are the *[[force]]* fields whose [[quanta]] are [[bosons]], in contrast to [[matter]]-fields whose [[quanta]] are [[fermions]].

The eponymous property of gauge fields is that they are identified only up to [[equivalences]] called *[[gauge transformations]]*.

The archetypical example of a gauge field is the [[electromagnetic field]] in ([[classical field theory|classically]]) [[electromagnetism]] and ([[quantum field theory|quantumly]]) in [[quantum electrodynamics]].

The most widely considered kind of gauge field, often the one understood by default, is a [[non-abelian cohomology|non-abelian]] generalization of electromagnetism, generally called the *[[Yang-Mills field]]*, of which specific instances are the [[gluon]]-[[field (physics)|field]] in [[quantum chromodynamics]] carrying the [[strong nuclear force]], and a similar field carrying the [[weak nuclear force]].

Mathematically, [[field configurations]] of such "ordinary" gauge fields are: 

* *locally* identified with [[Lie algebra-valued differential forms]], whose [[curvature 2-form]] (just the [[de Rham differential]] in the abelian case) is to be understood as the [[flux density]] that the gauge fields imprints on [[spacetime]],

* *globally* identified with [[connection on a principal bundle|connections]] on [[principal bundles]], whose [[structure group]] is then called the *[[gauge group]]* of the field. 

The eponymous [[gauge transformations]] between gauge fields are thereby identified with [[isomorphisms]] between these [[connection on a principal bundle|connections]]. 

The [[isomorphism class]] of the [[underlying]] [[principal bundles]], hence its class in [[nonabelian cohomology]], reflects the "topological charge" carried by the gauge field, attributed to [[soliton|solitonic]] field configurations such as [[Abrikosov vortices]], [[magnetic monopoles]] and [[instantons]].

(To some extent also the [[gravitational field]] behaves like a gauge field with [[structure group|structure]]/[[gauge group]] a [[Poincaré group]], but a further [[soldering form|soldering]]-[[constraint]] makes gravity be described more specifically by [[Cartan connections]] which are often not counted under "gauge fields" -- see at *[[first-order formulation of gravity]]* for more on this.)

Much technology in [[variational calculus]] for [[Lagrangian field theory]] and subsequent [[quantization]]-procedures has been and is being developed already for handling gauge fields with their [[gauge transformations]] just locally -- common machinery is known as "[[BRST complex|BRST]]-[[BV-formalism]]" or variants thereof.

Comparatively less attention has traditionally been paid to the global aspects of gauge fields (for instance available BRST-BV formalism does not really reflect or handle them). But realizing that connections on [[principal U(1)-bundles]] globally describing the [[electromagnetic field]] are equivalently 2-[[cocycles]] in [[ordinary differential cohomology]], and that connections on general [[principal bundles]] may still be understood as cocycles in [[nonabelian differential cohomology]], it is helpful to understand the global nature of gauge fields generally as reflected by notions of [[cohomology]]:

[[!include cohomology and gauge fields -- table]]

This cohomological perspective is particularly apt for generalizations of gauge fields such as to (hypothetical) [[higher gauge fields]]. For instance, the [[RR-fields]] of [[type II supergravity]]/[[type II string theory]] have famously been [[D-brane charge quantization in K-theory|conjectured]] to be [[cocycles]] in ([[twisted equivariant differential K-theory|twisted equivariant differential]]) [[topological K-theory]] instead of [[ordinary cohomology]].


## Related concepts

* [[gauge theory]]

* [[gauge transformation]]

* [[gauge fixing]]

* [[gauge invariance]]

* [[higher gauge field]]


## References

For the time being see the references at *[[gauge theory]]*.


[[!redirects gauge fields]]
