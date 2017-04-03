

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

## Definition

An **isofibration** is a [[functor]] $p:E\to B$ such that for any [[object]] $e\in E$ and any [[isomorphism]] $\phi:p(e) \cong b$, there exists an isomorphism $\psi:e \cong e'$ such that $p(\psi)=\phi$.  

$$
  \array{
    e &\stackrel{\exists \psi \in p^{-1}(\phi)}{\to} & \exists e'&&& E 
    \\
     &&&&&  \downarrow^p
    \\
    p(e) &\stackrel{\phi}{\to} & b &&& B
  }
  \,.
$$

If $p$ is a [[forgetful functor]], then being an isofibration says that whatever stuff $p$ forgets can be "transported along isomorphisms."

{#NotInvariantUnderEquivalence} Notice that this definition of isofibration violates the 1-categorical [[principle of equivalence]] where it demands that $p(\psi)=\phi$ (which includes the requirement that $p(e') = b$): this condition is not invariant under [[equivalence of categories]]. If one changed the definition to involve just an [[isomorphism]] $p(\psi)\cong\phi$, then of course, any functor would qualify. But the point of isofibrations is rather to help present the [[(2,1)-category]] of categories/groupoids in terms of 1-categorical data. For more on this see below at _[As fibrations in canonical model structures](#AsFibrationsInCanonicalModelStructures)_.



## Properties

### General

Isofibrations have a number of good properties.  For example, any [[strict 2-limit|strict pullback]] of an isofibration is also a [[2-limit|weak pullback]]. (This is also explained by the role of isofibrations as the fibrations in the [[canonical model structures]], see [below](#AsFibrationsInCanonicalModelStructures).)

Any [[Grothendieck fibration]] or opfibration is an isofibration, but not conversely (unless $B$ is a [[groupoid]]).

### As fibrations in canonical model structures
 {#AsFibrationsInCanonicalModelStructures}

The isofibrations are the _fibrations_ in the [[canonical model structure on categories]] and the [[canonical model structure on groupoids]].  More generally, the fibrations in [[canonical model structures]] on various types of higher categories are usually some generalization of isofibrations.  For example, the fibrations in the Lack model structure on 2-Cat have "equivalence lifting" and "local isomorphism lifting," and the fibrations in the Joyal model structure for [[quasi-category|quasicategories]] have "equivalence lifting" at all levels.

Generalizing in another direction, internalized isofibrations are the fibrations in the [[2-trivial model structure]] on any finitely complete and cocomplete [[strict 2-category]].


## References

For groupoids the definition appears (called "star surjectivity" there) on p. 105 (3 of 30) in

* {#Brown70} [[Ronnie Brown]], _Fibrations of groupoids_, Journal of Algebra
Volume 15, Issue 1, May 1970, Pages 103-132


[[!redirects isofibrations]]
