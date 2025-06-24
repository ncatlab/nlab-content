
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

The _smooth Serre-Swan theorem_ ([Nestruev 03, 11.33](#Nestruev03)) states that over a [[smooth manifold]] $X$, 

1. the [[section]] [[functor]]

   $$
     \Gamma_X(-)
      \;\colon\;
     SmoothVectorBundles_{/X} 
       \hookrightarrow
     C^\infty(X) Mod
   $$

   that sends [[smooth vector bundles]] (with fibers of uniformly bounded dimension) over $X$ of [[finite number|finite]] [[rank]] to their [[spaces of sections|spaces of]] smooth [[sections]], regarded as [[modules]] over the [[algebra of functions|algebra of]] [[smooth functions]] on $X$, is a [[fully faithful functor]]
   
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

* {#Nestruev03} [[Jet Nestruev]]: *Smooth manifolds and Observables*, Graduate Texts in Mathematics **220** Springer (2002, 2020) &lbrack;[doi:10.1007/978-3-030-45650-4](https://doi.org/10.1007/978-3-030-45650-4), ISBN:0-387-95543-7, <a href="https://nzdr.ru/data/media/biblio/kolxoz/M/MD/MDdg/Nestruev%20J.%20Smooth%20Manifolds%20and%20Observables%20(ISBN%200387955437)(Springer,%202003)(224s)_MDdg_.pdf">pdf</a>&rbrack;

Variant for [[Hilbert space]]-bundles over [[Riemannian manifolds]]:

* Jens Kaad: *A Serre–Swan theorem for bundles of bounded geometry*, Journal of Functional Analysis **265** 10 (2013) 2465-2499 &lbrack;[doi;10.1016/j.jfa.2013.06.005](https://doi.org/10.1016/j.jfa.2013.06.005)&rbrack;


[[!redirects smooth Serre–Swan theorem]]