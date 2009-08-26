##Motivation##

The passage from a manifold $M$ to its boundary $\partial M$ has some formal properties which are preserved in the presence of orientation, for manifolds with additional structure and so on. The category of compact smooth manifolds with boundary $D = Diff_c$ has finite [[direct sums]] and the boundary operator $\partial:D\to D$, $M\mapsto \partial M$, is an endofunctor commuting with finite sums (some say it is an additive functor). The inclusions $i_M:\partial M\to M$ form a natural transformation of functors $i:\partial\to Id$. Finally, the isomorphism classes of objects in $D$ form a set.

##Definition##

A __cobordism category__ is a triple $(D,\partial,i)$ where $D$ is a [[svelte category]] with finite direct sums and an initial object $0$ (often denoted by $\emptyset$ in this context), $\partial:D\to D$ is an additive functor and $i:\partial\to Id_D$ is a natural transformation such that $\partial\partial M = 0$ for all objects $M\in D$.

Note that $i$ is *not* required to be a *subfunctor* of the identity, i.e. the components $i_M$ are not required to be [[monomorphism|monic]], what is however often the case in examples. In this context, the direct sum is often denoted by $+$.  

Two objects $M$ and $N$ in a cobordism category $(D,\partial,i)$ are said to be __cobordant__ and write $M\sim_{cob} N$ if there are objects $U,V\in D$ such that $M+\partial U \cong N+\partial V$ where $\cong$ denotes the relation of being isomorphic. In particular, the isomorphic objects are cobordant. Being cobordant is an [[equivalence relation]] and for any object $M$ in $D$, one has $\partial M\sim_{cob} 0$. Objects of the form $\partial M$ where $M$ is an object in $D$ are said to be *boundaries* and the objects $V$ such that $\partial V = 0$ are said to be *closed*. In particular, every boundary is closed. A direct sum of closed objects (resp. boundaries) is a closed object (resp. a boundary). If an object $M$ is a boundary and $M\cong N$ then $N$ is also a boundary. To summarize, the relation of being cobordant compatible with the direct sum, in the sense that the direct sum induces an associative commutative operation on the set of equivalence classes, which hence becomes a commutative [[semigroup]] $\Omega(D,\partial,i)$, which is called the __cobordism semigroup__ of the cobordism category $(D,\partial,i)$. The Thom group $\mathcal{N}_*$ of cobordism classes of unoriented compact smooth manifolds is an example where $D=Diff_c$.

##Literature##

* Robert E. Stong, _Notes on cobordism theory_, Princeton University Press 1968 (Russian transl., Mir 1973)

Compare also some other nlab entries on cobordism theory: [[extended cobordism]], [[cobordism]], [[cobordism hypothesis]], [[generalized tangle hypothesis]], [[(infinity,n)-category of cobordisms]]. 