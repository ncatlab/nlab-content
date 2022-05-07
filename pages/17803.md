
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _smooth Serre-Swan theorem_ ([Nestruev 03, 11.33](#Nestruev03)) states that over a connected [[smooth manifold]] $X$, 

1. the [[section]] [[functor]]

   $$
     \Gamma_X(-)
      \;\colon\;
     SmoothVectorBundles_{/X} 
       \hookrightarrow
     C^\infty(X) Mod
   $$

   that sends [[smooth vector bundles]] over $X$ of [[finite number|finite]] [[rank]] to their [[spaces of sections|spaces of]] smooth [[sections]], regarded as [[modules]] over the [[algebra of functions|algebra of]] [[smooth functions]] on $X$, is a [[fully faithful functor]]
   
   ([Nestruev 03, theorem 11.29](#Nestruev03));

1. its [[essential image]] consists precisely of the [[finitely generated object|finitely generated]] [[projective modules]] 

   ([Nestruev 03, 11.32](#Nestruev03)).

This is the variant for [[differential geometry]] of what the [[Serre-Swan theorem]] asserts in [[algebraic geometry]] and in [[topology]]. 


+-- {: .num_remark #BaseManifoldNotRequiredToBeCompact}
###### Remark
**(base [[smooth manifold]] not required to be [[compact space|compact]])

Contrary to the original theorem of [Swan 62](Serre-Swan+theorem#Swan) for [[topological vector bundles]], here in the smooth case the base [[smooth manifold]] $X$ of the [[smooth vector bundle]] is _not required_ to be [[compact space|compact]]. While for [[topological spaces]] [[compact space|compactness]] is needed to deduce that every [[topological vector bundle]] is a [[direct sum|direct summand]] of a [[trivial vector bundle]] ([this prop.](topological+vector+bundle#TopologicalVectorbundleOverCompactHausdorffSpaceIsDirectSummandOfTrivialBundle)) for [[smooth vector bundles]] this conclusion follows without assuming compactness, by [[embedding of smooth manifolds]] into [[Cartesian spaces]] ([this prop.](embedding+of+differentiable+manifolds#ManifoldEmbedsIntoLargeDimensionalEuclideanSpace)).

=--


+-- {: .num_remark}
###### Remark
**(other algebraic apects of differential geometry)**

Together with the [[embedding of smooth manifolds into formal duals of R-algebras]], the smooth Serre-Swan theorem states that that differential geometry is "more algebraic" than it may superficially seem.
A third fact in this vein is that _[[derivations of smooth functions are vector fields]]_.

=--

## Related theorems

* the [[Hadamard lemma]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[derivations of smooth functions are vector fields]]


## References

* {#Nestruev03} [[Jet Nestruev]], _Smooth manifolds and observables_, Graduate texts in mathematics, 220, Springer-Verlag, ISBN 0-387-95543-7 (2003)

[[!redirects smooth Serre–Swan theorem]]