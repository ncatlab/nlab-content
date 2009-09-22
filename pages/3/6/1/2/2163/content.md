<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>


#Idea#

The notion of cobordism category is an abstract one intended to capture important features of (many variants of) the [[category]] of [[cobordism]]s and include in the same formalism cobordisms for closed manifolds with various kinds of structure. 

#Motivation#

The passage from a [[manifold]] $M$ to its [[boundary]] $\partial M$ has some formal properties which are preserved in the presence of [[orientation]], for manifolds with additional structure and so on. The category of [[compact space|compact]] smooth manifolds with boundary $D = Diff_c$ has finite [[coproducts]] and the boundary operator $\partial:D\to D$, $M\mapsto \partial M$ is an endofunctor commuting with coproducts. (Often these coproducts are referred to as [[direct sums]], and some say that $\partial$ is an [[additive functor]], but $D$ is not actually an [[additive category]]). The inclusions $i_M:\partial M\to M$ form a [[natural transformation]] of functors $i:\partial\to Id$. Finally, the isomorphism classes of objects in $D$ form a set, so $D$ is [[essentially small category|essentially small]] (svelte).


#Definition#

A __cobordism category__ is a triple $(D,\partial,i)$ where $D$ is a [[svelte category]] with finite coproducts (called direct sums, often denoted by $+$), including an [[initial object]] $0$ (also often denoted by $\emptyset$), $\partial:D\to D$ is an additive (direct-sum-preserving) functor and $i:\partial\to Id_D$ is a natural transformation such that $\partial\partial M = 0$ for all objects $M\in D$.

Note that $i$ is *not* required to be a *[[subfunctor]]* of the identity, i.e. the components $i_M$ are not required to be [[monomorphism|monic]], which is however often the case in examples.

Two objects $M$ and $N$ in a cobordism category $(D,\partial,i)$ are said to be __cobordant__, written $M\sim_{cob} N$, if there are objects $U,V\in D$ such that $M+\partial U \cong N+\partial V$ where $\cong$ denotes the relation of being [[isomorphism|isomorphic]] in $D$. In particular, isomorphic objects are cobordant. Being cobordant is an [[equivalence relation]] and for any object $M$ in $D$, one has $\partial M\sim_{cob} 0$. Objects of the form $\partial M$ where $M$ is an object in $D$ are said to be *boundaries* and the objects $V$ such that $\partial V = 0$ are said to be *closed*. In particular, every boundary is closed. A direct sum of closed objects (resp. boundaries) is a closed object (resp. a boundary). If an object $M$ is a boundary and $M\cong N$ then $N$ is also a boundary. To summarize, the relation of being cobordant is compatible with the direct sum, in the sense that the direct sum induces an associative commutative operation on the set of equivalence classes, which hence becomes a commutative [[monoid]] $\Omega(D,\partial,i)$, which is called the __cobordism semigroup__ (although it is a monoid) of the cobordism category $(D,\partial,i)$. The [[Thom group]] $\mathcal{N}_*$ of cobordism classes of unoriented compact smooth manifolds is an example where $D=Diff_c$.


#Literature#

* Robert E. Stong, _Notes on cobordism theory_, Princeton University Press 1968 (Russian transl., Mir 1973)

#Related $n$Lab entries#

Compare also some other nlab entries on cobordism theory: 


* [[cobordism]]

  * [[extended cobordism]]

  * [[(∞,n)-category of cobordisms]]

* [[cobordism hypothesis]]

  * [[generalized tangle hypothesis]]


* [[cospan]]

  * [[Cospans in Algebraic Topology]]