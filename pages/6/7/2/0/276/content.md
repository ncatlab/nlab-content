#Idea#

A _crossed complex_ (of groupoids) is a nonabelian and [[horizontal categorification|many object]] generalization of a chain complex of abelian groups.

Crossed complexes were defined by Blakers in 1948 (following a suggestion of Eilenberg) and developed by Whitehead in 1949 and 1950 (but these authors used different terminology). They were applied by Huebschmann to group cohomology in 1980. They were further developed in  series of articles by Ronnie Brown and collaborators in the context of [[nonabelian algebraic topology]], and partly because they were found equivalent to form of (strict) cubical $\omega$-groupoid with _connections_. This equivalence enabled a number of new results, including van Kampen type theorems and monoidal closed structures for crossed complexes. 

Crossed complexes are an equivalent way to encode the information contained in [[strict omega-groupoid]]s: the groups appearing in the crossed complex in degree $n \geq 2$ are the source-fibers of the collection of $n$-morphisms of the $\omega$-groupoid.

See also [[homotopy n-type]]. 

One way to think of a crossed complex is as a chain complex in which the bottom part is a crossed module and the rest is a chain complex of modules over the fundamental group of the crossed complex (that is its cokernel).  This is easy to think of in the case where there is a single object (crossed complex of groups), and it is a simple step to extend to the many object case.

##Examples##

If $X_*$ is a [[filtered space]], then there is a crossed complex $\Pi X_*$ which in dimension 0 is $X_0$, in dimension 1 is the [[fundamental groupoid]] $\pi_1(X_1,X_0)$ and   in dimension $n \gt 1$ is the family of relative homotopy groups $\{\pi_n(X_n,X_{n-1},p) : p\in X_0\}$.  This gives a functor $\Pi$ from filtered spaces to crossed complexes, which may be used to construct the generalisation of the [[Dold-Kan correspondence]], which in this case goes between crossed complexes and [[simplicial T-complex]]es.  


#Remarks#

* In low degrees crossed complexes are the following:
  * A crossed complex of length 0 is a [[Set|set]].
  * A crossed complex of length 1 is a [[groupoid]].
  * A crossed complex of length 2 is a [[crossed module]], which is equivalent to a strict kind of [[2-group]] by the Brown-Spencer Theorem,
(R. Brown and C.B. Spencer, _G-groupoids, crossed modules and the fundamental groupoid of a 
topological group_, Proc. Kon. Ned. Akad. v. Wet, 79, (1976), 296 &#8211; 302.)

A survey of the use of crossed complexes is in 
R. Brown _Crossed complexes and homotopy groupoids as non commutative tools for higher dimensional local-to-global problems_,  to appear in Michiel Hazewinkel (ed.), Handbook of Algebra, volume 6, Elsevier, 2008/2009. (available as math.AT/0212274 v7).

+--{.query}
[[Tim Porter|Tim]]: One of many terminological problems that arise in this stuff is whether 'length' of a chain complex or crossed complex refers to the number of transitions/arrows or the number of nodes /groups or whatever?
=--

A discussion of the kind of homotopy types modelled by crossed complexes, namely a _linear_ model, and a conjecture as to how to extend this, is in [[homotopy n-type]]. 