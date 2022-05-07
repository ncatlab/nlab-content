+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Synthetic topology**, like [[synthetic domain theory]], [[synthetic differential geometry]], and [[synthetic computability]], are part of [[synthetic mathematics]]. It uses the internal logic of a topos to develop a part of mathematics. In this case topology. This is closely related to topology via logic and [[abstract Stone duality]].

The formal system of [[type theory]] has semantics in many [[categories]], and in particular in many categories of "spaces".  Thus types may be regarded not just as [[sets]] but as [[general topology|topological objects]].  Interestingly, a good deal of this "topology" can be detected intrinsically in type theory, often corresponding to the possible failure of principles of [[classical mathematics]].

## Dictionary

[[Martín Escardó]] has given the following translations between the two fields;

| general topology | type theory |
|--|--|
| [[topological space|space]] | [[type]] |
| [[continuous function]] | [[function]] |
| [[clopen set]] | [[decidable object|decidable]] set |
| [[open set]] | semi-decidable set |
| [[closed set]] | set with semi-decidable [[complement]] |
| [[discrete space]] | type with [[decidable equality]] |
| [[Hausdorff space]] | type with semi-decidable [[inequality relation|inequality]] |
| [[convergent sequence]] | map out of $\mathbb{N}_\infty$ (see below) |
| [[compact set]] | exhaustively searchable set, in a finite number of steps |

It should be stressed that the concepts on the right are not the *only* ways to represent the topological concepts on the left in type theory.  For instance, in [[cohesive homotopy type theory]] there is a notion of "discrete space" that has nothing to do with decidable equality (in particular, in homotopy type theory a type with decidable equality is necessarily an [[h-set]], whereas discrete spaces don't need to be h-sets).

## Semantics

There are many different topological semantics for type theory, but one which seems especially closely related to the above dictionary is the [[topological topos]].  For instance, in that case the internally defined set $\mathbb{N}_\infty$ (the set of infinity non-decreasing binary sequences) really does get interpreted semantically as the "generic convergent sequence".

## Implementation

Many of the results that have originated from this view have been implemented in an [[Agda]] [library](http://www.cs.bham.ac.uk/~mhe/agda/)

## Related pages

* [[dominance]]
* [[open subset]]
* [[overt space]]

##References

* [[Martín Escardó]], _Synthetic topology of data types and classical spaces_, ([pdf](http://www.cs.bham.ac.uk/~mhe/papers/barbados.pdf))

* [[Martín Escardó]], {#EscardoPopl2012} _The topology of Seemingly impossible functional programs_, ([pdf](http://www.cs.bham.ac.uk/~mhe/.talks/popl2012/escardo-popl2012.pdf))

* [[Andrej Bauer]], [[Davorin Lešnik]], _Metric Spaces in Synthetic Topology_, ([pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf))

* [[Davorin Lešnik]], _Synthetic Topology and Constructive Metric Spaces_,[PhD](http://www.fmf.uni-lj.si/storage/19160/PhD_Davorin.pdf)

* [[Davorin Lešnik]], _Unified Approach to Real Numbers in Various Mathematical Settings_, [1402.6645](https://arxiv.org/abs/1402.6645)

* [[Steven Vickers]], _Locales and toposes as spaces, [PDF](https://www.cs.bham.ac.uk/~sjv/LocTopSpaces.pdf) 

[[!redirects relation between type theory and topology]]