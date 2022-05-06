
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea

This construction 'probes' a space $X$ by mapping geometric simplices into it. It is one of the classical approaches to determining invariants of the homotopy type of the space.  

## Definition

The _singular simplicial complex_ $S_\bullet(X)$ of a [[topological space]] $X$ is the [[nerve]] of $X$ with respect to the standard [[cosimplicial object|cosimplicial]] topological space $\Delta_{Top} : \Delta \to Top$.  It is thus the [[simplicial set]], $S_\bullet(X)$, having
$$
  S_n(X) = Hom_{Top}(\Delta_{Top}^n, X)
  \,.
$$
as its set of $n$-simplices, and fairly obvious faces and degeneracy mappings obtains by restriction along the structural maps of $\Delta_{Top} : \Delta \to Top$.  This is always a [[Kan complex]] and as such has the interpretation of the [[fundamental ∞-groupoid]] $\Pi(X)$ of $X$.

The $n$-simplices of this are just _[[singular simplex|singular n-simplices]]_ generalising paths in $X$. (The term _singular_ is used because there is no restriction that the continuous function used should be an embedding, as would be the case in, for instance, a [[triangulation]] where a simplex in the underlying [[simplicial complex]] corresponds to an embedding of a simplex.)


## Properties

### Preservation of model structure

The singular complex functor preserves all five classes
of maps in a [[model category]]: [[weak equivalences]], [[cofibrations]], [[acyclic cofibrations]],
[[fibrations]], and [[acyclic fibrations]].

* [[weak equivalences|Weak equivalences]] are preserved by definition of the [[model structure]] on topological spaces, which is [[transferred model structure|transferred]] from [[simplicial sets]].

* [[Cofibrations]] (and hence [[acyclic cofibrations]]) are preserved because all cofibrations of topological spaces are [[injective functions]], injective maps are preserved, and all injective maps of simplicial sets are cofibrations.

* [[fibrations|Fibrations]] and [[acyclic fibrations]] are preserved because the singular complex functor is a [[right Quillen functor]].


### Relation to geometric realization

Together with its [[adjoint functor|adjoint]]—[[geometric realization]] $|-| : sSet \to Top$—the functor $Sing : Top \to sSet$ is part of the [[Quillen equivalence]] between the [[model structure on topological spaces]] and the [[model structure on simplicial sets]] that is sometimes called the [[homotopy hypothesis]]-theorem.

### Relation to ordinary (co)homology

Forming from the singular simplicial complex $Sing(X)$ first the free [[simplicial abelian group]] $\mathbb{Z}[Sing(X)]$ and then under the [[Dold-Kan correspondence]] the corresponding [[normalized chain complex]] yields the [[chain complex]] of (normalized!) singular chains, which computes the [[singular homology]] of $X$. 

## Related concepts

* [[singular simplex]]

* [[fundamental infinity-groupoid]]

* [[singular homology]]

[[!redirects singular complex]]

[[!redirects singular simplicial complexes]]

