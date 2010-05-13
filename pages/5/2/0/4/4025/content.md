
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The term **functional** is used to denote [[function]]s whose [[domain]] is a [[space]] that itself is or has the typical size of a [[mapping space]], so that the functional is a "a function of functions".

Two (at least) special cases of this have achieved precise mathematical formulation with a rich theory:

1. in  [[functional analysis]] one studies _linear_ functionals: linear [[function]]s on [[topological vector space]]s. This includes for instance [[distribution]]s.

1. in [[variational calculus]] one studies certain functions on spaces of [[section]]s of [[jet bundle]]s. These are the kind of functionals that appear in [[physics]] as [[action functional]]s.
 
## In functional analysis

### Definition

A **functional** is a map $V \to k$ in $Vect_k$ from a [[vector space]] to the ground [[field]] $k$. In the case that $V$ is a [[TVS]], this is usually required to be a _continuous_ map (and so a map in an appropriate category of topological vector spaces).

### Remarks

In a sense, functional are co-probes for vector spaces. If the vector space $V$ in question is finite dimensional and is equipped with a basis, then all functionals are linear combinations of the coordinate projections. These projections are known as the _dual basis_. 

In infinite dimensional topological vector spaces over complex numbers, the notion of dual basis breaks down once (topological) vector spaces more general than Hilbert spaces are considered. In this case, the [[Hahn-Banach theorem]] ensures the existence of 'enough' (continuous) functionals. Note that for a non-locally convex TVS the Hahn-Banach theorem may fail. There are even examples of TVS such that the only continuous functional is the constant map onto $0\in k$.



## In variational calculus

See 

* [[variational calculus]].