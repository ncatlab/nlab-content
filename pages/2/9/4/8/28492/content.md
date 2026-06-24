
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
| [[clopen set]] | [[decidable subset]] |
| [[open set]] | semi-decidable subset |
| [[closed set]] | subset with semi-decidable [[complement]] |
| [[discrete space]] | type with [[decidable equality]] |
| [[Hausdorff space]] | type with semi-decidable [[inequality relation|inequality]] |
| [[convergent sequence]] | map out of $\mathbb{N}_\infty$ (see [below](#Semantics)) |
| [[compact set]] | exhaustively searchable set, in a finite number of steps |

This dictionary has been used in some approaches to [[synthetic topology]], such as [[synthetic Stone duality]] ([Cherubini, Coquand, Geerligs & Moeneclaey 2024](#CCGM24)), where the set of [[semidecidable propositions]] is a [[dominance]]. 

However, not all approaches to [[synthetic topology]] use Smyth's dictionary as defined above, in terms of [[semidecidability]]. In general, the set of semidecidable propositions cannot be proven to be a dominance in [[constructive mathematics]] without assuming an axiom that implies the constructive [[taboo]] [[Rosolini dominance axiom]], such as [[countable choice]] or [[dependent choice]]. In this case, the [[quasidecidable propositions]] are usually used instead of semidecidable propositions, since the set of quasidecidable propositions is always an $\mathbb{N}$-overt [[dominance]] ([Bidlingmaier, Faissole & Spitters 2019](#BFS19), [Escardo 2020](#Escardo20)). In the presence of the [[Rosolini dominance axiom]], the semidecidable propositions coincide with the quasidecidable propositions. 

Moreover, other approaches to [[synthetic topology]] use [[dominances]] other than the set of [[semidecidable propositions]] or [[quasidecidable propositions]] to define topological concepts, such as [Lešnik 2021](#Lešnik21) and [Bakke, Sterling, Williams & Ye 2026](#BSWY26). 

## Semantics {#Semantics}

One [[categorical semantics]] which seems especially closely related to Smyth's dictionary in [[synthetic topology]] is the [[topological topos]]. For instance, in that case the internally defined set $\mathbb{N}_\infty$ (the set of infinite decreasing binary sequences) really does get interpreted semantically as "the generic convergent sequence". 

Another [[categorical semantics]] related to Smyth's dictionary is provided by the [[topos]] of [[light condensed sets]] in [[condensed mathematics]], as [[synthetic Stone duality]] uses Smyth's dictionary and is supposed to be the [[internal logic]] of said topos ([Cherubini, Coquand, Geerligs & Moeneclaey 2024](#CCGM24)). 

## Implementation

Many of the results that have originated from the viewpoint of Smyth's dictionary in [[synthetic topology]] have been implemented in an [[Agda]] library called TypeTopology (see [Escardo 2010](#Escardo10)).

## Related concepts

* [[synthetic topology]]

## References

* {#Escardo04} [[Martín Escardó]], *Synthetic topology of data types and classical spaces*, Electronic Notes in Theoretical Computer Science (ENTCS), Volume 87, Pages 21 - 156, 01 November 2004 &lbrack;[doi:10.1016/j.entcs.2004.09.017](https://doi.org/10.1016/j.entcs.2004.09.017), [pdf](http://www.cs.bham.ac.uk/~mhe/papers/barbados.pdf)&rbrack;

* {#Escardo10} [[Martín Escardó]]. *TypeTopology*. [[Agda]] code with comments, 2010. ([URL](https://www.cs.bham.ac.uk/~mhe/TypeTopology/)).

* [[Martín Escardó]], _Topology for functional programming_, EWSCS, Palmse, Estonia, 26 Feb – 2 Mar 2012 &lbrack;[slides](https://cs.ioc.ee/ewscs/2012/escardo/slides.pdf)&rbrack;

* [[Martín Escardó]], *The topology of seemingly impossible functional programs*, POPL TutorialFest, Philadelphia, 28 November 2012 &lbrack;[slides](http://www.cs.bham.ac.uk/~mhe/.talks/popl2012/escardo-popl2012.pdf)&rbrack;

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

* {#Escardo20} [[Martin Escardo]]. *Quasidecidable propositions*. [[Agda]] code with comments, 2020. ([URL](https://martinescardo.github.io/TypeTopology/NotionsOfDecidability.QuasiDecidable.html)).

* {#Lešnik21} [[Davorin Lešnik]], *Synthetic Topology and Constructive Metric Spaces* &lbrack;[arXiv:2104.10399](https://arxiv.org/abs/2104.10399)&rbrack;

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* &lbrack;[arXiv:2412.03203](https://arxiv.org/abs/2412.03203)&rbrack;

* {#BSWY26} [[Fredrik Bakke]], [[Jonathan Sterling]], [[Mark Damuni Williams]], [[Lingyuan Ye]], *The Synthetic Sierpiński Cone* &lbrack;[arXiv:2605.00773](https://arxiv.org/abs/2605.00773)&rbrack;

[[!redirects relation between type theory and topology]]
