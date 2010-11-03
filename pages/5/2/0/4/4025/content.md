
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Functional is used in two meanings: either a $k$-valued, usually linear, function on a $k$-vector space, where $k$ is a [[field]] (or even [[skewfield]]), or, more generally, a function on some space of functions, paths or alike. The two meanings overlap as sometimes one considers linear spaces of functions; then the two concepts of a functional agree.

Physicists and engineers usually talk about functions in terms of (real or complex) variables; and when the variables, i.e. [[domain]] are spaces of functions itself they are usually warned; hence word functional emphasises a function on [[domain]] which is a [[space]]  "of the size of [[mapping space]]", so that the functional is a "a function of functions".

Some special cases include

* in linear [[functional analysis]] one most often studies continuous _linear_ functionals: linear [[function]]s on [[topological vector space]]s. This includes for instance [[distribution]]s.

* in [[variational calculus]] one studies functions on spaces of [[section]]s of [[jet bundle]]s. For example, they appear in [[physics]] as [[action functional]]s.
 
* various discretised versions are interesting in finite geometries as well as numerical analysis

## In linear algebra and functional analysis

### Definition

A **functional** is a map $V \to k$ in $Vect_k$ from a [[vector space]] to the ground [[field]] $k$. In the case that $V$ is a [[TVS]], this is usually required to be a _continuous_ map (and so a map in an appropriate category of topological vector spaces).

### Remarks

In a sense, functional are co-probes for vector spaces. If the vector space $V$ in question is finite dimensional and is equipped with a basis, then all functionals are linear combinations of the coordinate projections. These projections are known as the _dual basis_. 

In infinite dimensional topological vector spaces over complex numbers, the notion of dual basis breaks down once (topological) vector spaces more general than Hilbert spaces are considered. In this case, the [[Hahn-Banach theorem]] ensures the existence of 'enough' (continuous) functionals. Note that for a non-locally convex TVS the Hahn-Banach theorem may fail. There are even examples of TVS such that the only continuous functional is the constant map onto $0\in k$.



## In variational calculus

See 

* [[variational calculus]].

[[!redirects functionals]]

[[!redirects linear functional]]
[[!redirects linear functionals]]

