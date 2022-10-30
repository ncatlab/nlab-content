
# Contents
* automatic table of contents goes here
{: toc}

## Idea

Functional is used in two meanings: either a $k$-valued, usually linear, [[function]] on a $k$-[[vector space]] (or [[module]]), where $k$ is a [[field]] (or any [[rig]]); or a function on some [[mapping space|space of functions]], [[path space|paths]] or the like. The two meanings overlap as sometimes one considers [[function space|linear spaces of functions]]; then the two concepts of a functional agree.

Physicists and engineers usually talk about 'functions' in terms of (real or complex) variables; and when the variables are themselves functions (i.e., the [[domain]] is a space of functions itself), they are usually warned; hence the word 'functional' emphasises a function on a domain which is "of the size of [[mapping space]]", so that the functional is a "a function of functions".

Some special cases include

* in linear [[functional analysis]] one most often studies continuous _linear_ functionals: linear [[function]]s on [[topological vector space]]s. This includes for instance [[distribution]]s.

* in [[variational calculus]] one studies functions on spaces of [[section]]s of [[jet bundle]]s. For example, they appear in [[physics]] as [[action functional]]s.
 
* various discretised versions are interesting in finite geometries as well as numerical analysis


## In linear algebra and functional analysis

### Definition

A **functional** is a [[function]] $V \to k$ from a [[vector space]] to the [[ground field]] $k$.  A __linear functional__ is a [[linear map|linear]] such function, that is a [[morphism]] $V \to k$ in $k$-[[Vect]].  In the case that $V$ is a [[topological vector space]], a __continuous linear functional__ is a [[continuous map|continuous]] such map (and so a morphism in the category [[TVS]]).  When $V$ is a [[Banach space]], we speak of __[[bounded operator|bounded]] linear functionals__, which are the same as the continuous ones.


### Remarks

In a sense, linear functionals are co-probes for vector spaces. If the vector space $V$ in question has finite [[dimension]] and is equipped with a [[basis]], then all linear functionals are [[linear combinations]] of the [[coordinate projection]]s. These projections are known as the _[[dual basis]]_.

In infinite-dimensional [[topological vector spaces]], the notion of dual basis breaks down once spaces more general than [[Hilbert spaces]] are considered. But for [[locally convex spaces]], the [[Hahn–Banach theorem]] ensures the existence of 'enough' continuous linear functionals.  Among non-LCSes, however, there are examples such that the only continuous linear functional is the constant map onto $0 \in k$.


## In variational calculus

See 

* [[variational calculus]].


[[!redirects functional]]
[[!redirects functionals]]

[[!redirects linear functional]]
[[!redirects linear functionals]]

[[!redirects continuous linear functional]]
[[!redirects continuous linear functionals]]
[[!redirects bounded linear functional]]
[[!redirects bounded linear functionals]]
