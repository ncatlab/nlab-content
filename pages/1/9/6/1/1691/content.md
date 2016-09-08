
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Hochschild-Serre spectral sequence_ is a [[spectral sequence]] that expresses [[group cohomology]] by a special case of the [[Grothendieck spectral sequence]].

## Statement

Let $G$ be a [[group]], $K\subset G$ a [[normal subgroup]] and $A$ a left 
$G$-[[module]]. The [[group cohomology]] groups $H^n(G,A)$ form the [[derived functor in homological algebra|derived functors]] of the [[invariants]] functor $A\mapsto A^G = \{ a\in A | g a = a, g\in G\}$. 

The invariants can be computed in two stages, hence as the [[composition|composite]] of two [[functors]] as 

$$
  A^G = (A^K)^{G/K}
  \,.
$$ 

The _Hochschild--Serre spectral sequence_
is the [[Grothendieck spectral sequence]] for the composition of these functors. Its $E_2$-page is

$$
  E^{p,q}_2 = H^p(G/K,H^q(K,A))
$$ 

and it is converging to the [[group cohomology]] $E^n_\infty = H^n(G,A)$.  

There is a similar spectral sequence for [[group homology]] obtained as a Grothendieck spectral sequence for the two-stage computation of [[coinvariants]].  

## References

* [[James Milne]], section 14 of _[[Lectures on Étale Cohomology]]_


[[!redirects Hochschild–Serre spectral sequence]]
[[!redirects Hochschild--Serre spectral sequence]]