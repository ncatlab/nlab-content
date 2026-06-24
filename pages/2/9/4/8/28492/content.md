
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
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

In one branch of [[synthetic topology]], there is a translation between the concepts of [[topology]] and those of [[data types]], [[sequences]], and [[semidecidability]] in [[type theory]] called **Smyth's dictionary** ([Escardó 2004](#Escardo04)), named after [[Michael B. Smyth]]:

| general topology | type theory |
|--|--|
| [[topological space|space]] | [[type]] / [[data type]] |
| [[point]] | [[term]] / [[element]] / piece of data | 
| [[continuous function]] | [[function]] |
| [[clopen set]] | [[decidable object|decidable]] set |
| [[open set]] | semi-decidable property |
| [[closed set]] | set with semi-decidable [[complement]] |
| [[discrete space]] | type with [[decidable equality]] |
| [[Hausdorff space]] | type with semi-decidable [[inequality relation|inequality]] |
| [[convergent sequence]] | map out of $\mathbb{N}_\infty$ (see [below](#Semantics)) |
| [[compact set]] | exhaustively searchable set, in a finite number of steps |

Not all approaches to [[synthetic topology]] use Smyth's dictionary, since it defines topological concepts in terms of [[semidecidability]]. Many approaches to [[synthetic topology]] use sets other than the set of [[semidecidable propositions]] to define topological concepts. Most commonly, [[dominances]] are used, and the set of semidecidable propositions cannot be proven to be a dominance in [[constructive mathematics]] without assuming an axiom that implies the constructive [[taboo]] [[Rosolini dominance axiom]], such as [[countable choice]]. 

## Semantics {#Semantics}

One [[categorical semantics]] which seems especially closely related to Smyth's dictionary in [[synthetic topology]] is the [[topological topos]]. For instance, in that case the internally defined set $\mathbb{N}_\infty$ (the set of infinite decreasing binary sequences) really does get interpreted semantically as "the generic convergent sequence".

## Implementation

Many of the results that have originated from the viewpoint of Smyth's dictionary in [[synthetic topology]] have been implemented in an [[Agda]] library called TypeTopology (see [Escardo 2010](#Escardo10)).

## Related concepts

* [[synthetic topology]]

## References

* {#Escardo04} [[Martín Escardó]], _Synthetic topology of data types and classical spaces_, 2004 ([pdf](http://www.cs.bham.ac.uk/~mhe/papers/barbados.pdf))

* {#Escardo10} [[Martín Escardó]]. *TypeTopology*. [[Agda]] code with comments, 2010. ([URL](https://www.cs.bham.ac.uk/~mhe/TypeTopology/)).

* {#EscardoPopl2012} [[Martín Escardó]], _The topology of seemingly impossible functional programs_, 2012 ([pdf](http://www.cs.bham.ac.uk/~mhe/.talks/popl2012/escardo-popl2012.pdf), almost same presentation with minor changes [pdf](https://cs.ioc.ee/ewscs/2012/escardo/slides.pdf))