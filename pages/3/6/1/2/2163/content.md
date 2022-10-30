
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and Cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Functorial Quantum Field Theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The notion of cobordism category is an abstract one intended to capture important features of (many variants of) the [[category]] of [[cobordism]]s and include in the same formalism cobordisms for closed manifolds with various kinds of structure. 


The passage from a [[manifold]] $M$ to its [[boundary]] $\partial M$ has some formal properties which are preserved in the presence of [[orientation]], for manifolds with additional structure and so on. The category of [[compact space|compact]] smooth manifolds with boundary $D = Diff_c$ has finite [[coproducts]] and the boundary operator $\partial:D\to D$, $M\mapsto \partial M$ is an endofunctor commuting with coproducts. (Often these coproducts are referred to as [[direct sums]], and some say that $\partial$ is an [[additive functor]], but $D$ is not actually an [[additive category]]). The inclusions $i_M:\partial M\to M$ form a [[natural transformation]] of functors $i:\partial\to Id$. Finally, the isomorphism classes of objects in $D$ form a set, so $D$ is [[essentially small category|essentially small]] (svelte).


## Definition

### Axiomatization

+-- {: .un_def }
###### Definition

A __cobordism category__ is a triple $(D,\partial,i)$ where 

* $D$ is a [[svelte category]] 

  * with finite [[coproduct]]s (called [[direct sum]]s, often denoted by $+$), 

  * including an [[initial object]] $0$ (also often denoted by $\emptyset$), 

* $\partial:D\to D$ is an additive (direct-sum-preserving) [[functor]] 

* and $i:\partial\to Id_D$ is a [[natural transformation]] such that $\partial\partial M = 0$ for all [[object]]s $M\in D$.

=--

Note that $i$ is *not* required to be a *[[subfunctor]]* of the identity, i.e. the components $i_M$ are not required to be [[monomorphism|monic]], which is however often the case in examples.


+-- {: .un_def }
###### Definition

Two objects $M$ and $N$ in a cobordism category $(D,\partial,i)$ are said to be __cobordant__, written $M\sim_{cob} N$, if there are objects $U,V\in D$ such that $M+\partial U \cong N+\partial V$ where $\cong$ denotes the relation of being [[isomorphism|isomorphic]] in $D$. 

=--

+-- {: .un_remark }
###### Remark

In particular, isomorphic objects are cobordant. Being cobordant is an [[equivalence relation]] and for any object $M$ in $D$, one has $\partial M\sim_{cob} 0$. 

=--


+-- {: .un_def }
###### Definition

Objects of the form $\partial M$ where $M$ is an object in $D$ are said to be *boundaries* and the objects $V$ such that $\partial V = 0$ are said to be *closed*. 

=--


+-- {: .un_remark }
###### Remark

In particular, every boundary is closed. A direct sum of closed objects (resp. boundaries) is a closed object (resp. a boundary). If an object $M$ is a boundary and $M\cong N$ then $N$ is also a boundary. 

=--


+-- {: .un_def }
###### Definition

By the above, the relation of being cobordant is compatible with the direct sum, in the sense that the direct sum induces an associative commutative operation on the set of equivalence classes, which hence becomes a commutative [[monoid]] called the __cobordism semigroup__ 

$$
  \Omega(D,\partial,i)
  \,,
$$ 

of the cobordism category $(D,\partial,i)$. 


=--



## Properties


### The homotopy type of the cobordism category
 {#GMTWTheorem}

#### Topological case



+-- {: .num_theorem}
###### Theorem

There is a [[weak homotopy equivalence]]

$$
  \Omega |Cob_d|
  \simeq
  \Omega^\infty(MTSO(d))
$$

between the [[loop space]] of the [[geometric realization]] of the $d$-cobordism category and the [[Thom spectrum]]-kind spectrum 

$$
  \Omega^\infty MTSO(d)
   :=
  {\lim_\to}_{n \to \infty}  \Omega^{n+d} Th(U_{d,n}^\perp)
$$

where

$$
  U_{d,n}^\perp = 
  \{
   ...
  \}
$$

=--

This is ([GalatiusTillmannMadsenWeiss, main theorem](#GMWT)).


#### Geometric case

* ([Ayala](#Ayala))

The [[Thom group]] $\mathcal{N}_*$ of cobordism classes of unoriented compact smooth manifolds is the cobordism semigroup for $D=Diff_c$.



## Related concepts


* [[cobordism]], [[extended cobordism]]

* **category of cobordisms**

  * [[cobordism ring]]

  * [[Thom spectrum]]

  * [[(∞,n)-category of cobordisms]]

* [[cobordism hypothesis]]


## References

A classical reference is

* Robert E. Stong, _Notes on cobordism theory_, Princeton University Press 1968 (Russian transl., Mir 1973)

The [GMTW theorem](#GMTWTheorem) about the [[homotopy type]] of the cobordisms category with topological structures on the cobordisms appears in 

* [[Søren Galatius]], [[Ib Madsen]], [[Ulrike Tillmann]], and [[Michael Weiss]], _The homotopy type of the cobordism category_ 	Acta Math. 202 (2009), no. 2, 195--239 ([arXiv:math/0605249](http://arxiv.org/abs/math/0605249))
{#GMWT}

A generalization to geometric structure on the cobordisms is discussed in

* [[David Ayala]], _Geometric cobordism categories_ thesis (2009) ([arXiv:0811.2280](http://arxiv.org/abs/0811.2280))
 {#Ayala}


[[!redirects category of cobordisms]]

[[!redirects Galatius-Madsen-Tillmann-Weiss theorem]]
[[!redirects Galatius-Tillmann-Madsen-Weiss theorem]]
[[!redirects GMWT theorem]]

[[!redirects cobordism categories]]