
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

The notion of *cobordism categories* in the original sense of [Stong 1968](#Stong68)
abstracts basic properties of (variants of) [[categories]] whose [[objects]] are [[compact topological space|compact]] [[manifolds with boundary]], with the [[concept with an attitude|intent]] of regarding these as [[cobordisms]] between their boundary components.

A closely related but nominally different notion are categories whose *[[morphisms]]* are taken to be cobordisms between their boundary components. 

Beware that the use of terminology not always brings out this distinction; but these days this second meaning is more prevalent, in particular in discussion of [[cobordism cohomology]] and of [[topological field theory]].





## Definition


The axiomatization below is motivated as capturing the following familiar situation:

The category $D$ of [[compact space|compact]] [[smooth manifolds]] with [[boundary]], has finite [[coproducts]] and the boundary operator $\partial \colon D\to D$, $M\mapsto \partial M$ is an [[endofunctor]] commuting with [[coproducts]]. (Often these coproducts are referred to as [[direct sums]]. Notice that $D$ is similar to but not actually an [[additive category]]. The inclusions $i_M \colon \partial M\to M$ form a [[natural transformation]] of functors $i \colon \partial\to Id$. Finally, the [[isomorphism classes]] of objects in $D$ form a set, so $D$ is [[essentially small category|essentially small]] (svelte).

### Axiomatization

\begin{definition}

A __Stong cobordism category__ is a triple $(D,\partial,i)$ where 

* $D$ is a [[svelte category]] (i.e. an [[essentially small category]])

  * with finite [[coproduct]]s (called [[direct sum]]s, often denoted by $+$), 

  * including an [[initial object]] $0$ (also often denoted by $\emptyset$), 

* $\partial:D\to D$ is an additive (direct-sum-preserving) [[functor]] 

* and $i:\partial\to Id_D$ is a [[natural transformation]] such that $\partial\partial M = 0$ for all [[object]]s $M\in D$.

\end{definition}

[Stong 1968, p. 4](#Stong68).


\begin{remark}
Note that $i$ is *not* required to be a *[[subfunctor]]* of the identity, i.e. the components $i_M$ are not required to be [[monomorphism|monic]], which is however often the case in examples.
\end{remark}


\begin{definition}

Two objects $M$ and $N$ in a cobordism category $(D,\partial,i)$ are said to be __cobordant__, written $M\sim_{cob} N$, if there are objects $U,V\in D$ such that $M+\partial U \cong N+\partial V$ where $\cong$ denotes the relation of being [[isomorphism|isomorphic]] in $D$. 

\end{definition}

\begin{remark}
In particular, isomorphic objects are cobordant. Being cobordant is an [[equivalence relation]] and for any object $M$ in $D$, one has $\partial M\sim_{cob} 0$. 

\end{remark}


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

This is ([Galatius-Tillmann-Madsen-Weiss 06, main theorem](#GMWT)).

+-- {: .num_remark}
###### Remark

This statement may be thought of as a limiting case, of the [[cobordism hypothesis]]-theorem. See there for more.

=--


#### Geometric case

* ([Ayala](#Ayala))

The [[Thom group]] $\mathcal{N}_*$ of cobordism classes of unoriented compact smooth manifolds is the cobordism semigroup for $D=Diff_c$.


## Examples
 {#Examples}

Examples of cobordism categories besides those of manifolds with [[(B,f)-structure|$(B,f)$-structure]]:

* "foams" used in [[link homology]] following [Khovanov 2004](Khovanov+homology#Khovanov04)

See also [MO:q/59677](https://mathoverflow.net/q/59677/381).


## Related concepts


* [[cobordism]], [[extended cobordism]]

* **category of cobordisms**

  * [[cobordism ring]]

  * [[Thom spectrum]]

  * [[(∞,n)-category of cobordisms]]

* [[conformal cobordism category]]

* [[cobordism hypothesis]]

* [[cobordism cohomology theory]]

## References

### General

A classical reference is

* {#Stong68} [[Robert Stong]], _Notes on cobordism theory_, Princeton University Press 1968 (Russian transl., Mir 1973) &lbrack;[toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html)&rbrack;

The [GMTW theorem](#GMTWTheorem) about the [[homotopy type]] of the cobordisms category with topological structures on the cobordisms appears in 

* {#GMWT} [[Søren Galatius]], [[Ib Madsen]], [[Ulrike Tillmann]], and [[Michael Weiss]], _The homotopy type of the cobordism category_, Acta Math. 202 (2009), no. 2, 195--239 ([arXiv:math/0605249](http://arxiv.org/abs/math/0605249))


A generalization to geometric structure on the cobordisms is discussed in

* {#Ayala} [[David Ayala]], _Geometric cobordism categories_ thesis (2009) ([arXiv:0811.2280](http://arxiv.org/abs/0811.2280))
 

### Embedded cobordism category


* [[Oscar Randal-Williams]], _Embedded Cobordism Categories and Spaces of Manifolds_, 	Int. Math. Res. Not. IMRN 2011, no. 3, 572-608 ([arXiv:0912.2505](https://arxiv.org/abs/0912.2505))

On the [[homotopy groups]] of the [[embedded cobordism category]]:


* [[Marcel Bökstedt]], [[Anne Marie Svane]], _A geometric interpretation of the homotopy groups of the cobordism category_, Algebr. Geom. Topol. 14 (2014) 1649-1676 ([arXiv:1208.3370](https://arxiv.org/abs/1208.3370))

* [[Marcel Bökstedt]], [[Johan Dupont]], [[Anne Marie Svane]], _Cobordism obstructions to independent vector fields_, Q. J. Math. 66 (2015), no. 1, 13-61 ([arXiv:1208.3542](https://arxiv.org/abs/1208.3542))





[[!redirects cobordism categories]]

[[!redirects category of cobordisms]]
[[!redirects categories of cobordisms]]

[[!redirects Galatius-Madsen-Tillmann-Weiss theorem]]
[[!redirects Galatius-Tillmann-Madsen-Weiss theorem]]
[[!redirects GMWT theorem]]

[[!redirects embedded cobordism category]]
[[!redirects embedded cobordism categories]]
