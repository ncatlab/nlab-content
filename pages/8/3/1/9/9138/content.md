
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[quantum mechanics]] a [[self-adjoint operator]] $A$ on the given [[Hilbert space]] such that its [[spectrum]] lies between 0 and 1 is sometimes called an _effect_ or _quantum effect_ (see e.g. ([Ludwig](#Ludwig), ([Kraus](#Kraus))). These operators generalize [[projection operators]] and may be thought of as [[quantum observables]] with "unsharp" or "fuzzy" value. 

The notion of _effect algebra_ (due to ([Foulis-Bennet 94](#FoulisBennet))) is an abstraction of the structure exhibited by the collection of such effect operators. 

## Definition

+-- {: .num_defn}
###### Definition

A [[partial monoid|partial commutative monoid]] (PCM) consists of a set $M$ with a zero element $0 \in  M$ and a partial binary operation $\vee : M \times M \to M$ satisfying the three requirements below. They involve the notation $x \perp y$ for: $x \vee y$ is defined; in that case $x, y$ are called orthogonal.

1. Commutativity: $x\perp y$ implies $y\perp x$ and $x\vee y=y\vee x$.

1. Associativity: $y\perp z$ and $x\perp(y\vee z)$ implies $x\perp y$ and $(x\vee y)\perp z$ and $x\vee (y\vee z)=(x\vee y)\vee z$.

1. Zero: $0\perp x$ and $0\vee x=x$

(p.22)
=--

+-- {: .num_defn}
###### Definition
An *effect algebra* is a PCM $(E,0,\vee)$ with an orthocomplement. The latter is a unary operation $(-)^\perp :E\to E$ satisfying:

1.  $x^\perp\in E$ is the unique element in $E$ with $x\vee x^\perp=1$, where $1=0^\perp$.

1. $x\perp 1\Rightarrow x=0$.

For such an effect algebra one defines:

$$x\wedge y:=(x^\perp\vee y^\perp)^\perp$$

and

$$x\le y:\Leftrightarrow \exists_z.x\vee z=y$$

and


$$y\ominus x=z:\Leftrightarrow y=x\vee z$$
 (p. 23)
=--


+-- {: .num_remark}
###### Remark
If we consider

$$(-)\ominus y:up(y)\to down(y^\perp)$$

and

$$(-)\vee y:down(y^\perp)\to up$$

as functors between [[posets]] we have [[adjunctions]]

$$((-\wedge y)\dashv (-\ominus y)\dashv (-\wedge y)$$

Hence these functors are a [[Frobenius functor|frobenius pair]].

 (p.25)
=--

## Examples

(...)

## Application

In ([Jacobs 12](#Jacobs)) the approach to categorical logic where the substrate carrying the logical notions are [[Heyting algebras]] of [[subobjects]] in a [[topos]] is replaced by a new one where the substrate is [[effect algebra of predicates]] in [[extensive categories]].

## Reference

Quantum effect operators are discussed for instance in 

* G. Ludwig, _Foundations of Quantum Mechanics I_ Springer Verlag, New York, (1983)
 {#Ludwig}

* K. Kraus, _States, Effects, and Operations_ Springer Verlag, Berlin, (1983)
 {#Kraus}

The notion of effect algebra is due to

* D. J. Foulis, M. K. Bennet, _Effect algebras and unsharp quantum logics_, Found. Phys. 24 (1994), 1 331&#8211;1 352.
 {#FoulisBennet}

Discussion of effect algebras in the context of [[categorical logic]] is in

* [[Bart Jacobs]], _New Directions in Categorical Logic, for Classical, Probabilistic and Quantum Logic_, (2012) ([arXiv:1205.3940 ](http://arxiv.org/abs/1205.3940))
 {#Jacobs}
