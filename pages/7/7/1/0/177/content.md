> This entry is meant to be a **disambiguation page**, plus some **commentary** that would not fit well on either of the pages [[digraph]] and [[quiver]]. 
The term "directed graph" is somewhat intermediate between two rather precisely delineated terms: [[digraph]] and [[quiver]].
In a sense, "directed graph" is an undefined term, but the latter two both are defined. 
Every digraph is a quiver, not every quiver is a [[digraph]]. 
This page also briefly treats the related technical terms **oriented graph**,  **bidirected graph**, and **signed graph**, the latter of which  can hardly be regarded as a directed graph. Each of the latter three terms  has a standard meaning in modern combinatorics.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}






The term _directed graph_ is used in both [[graph theory]] and [[category theory]].
The definition varies---even within *one* of the two theories.

In [[graph theory]], _directed graph_ (often abbreviated to the contraction _digraph_) nowadays usually means a [[digraph]], while in [[category theory]], directed graph/digraph means and always has meant a [[quiver]]. 
The basic the difference is: [[quivers]] may have multiple arrows in the *same* direction (often called "parallel"), and also *loops*, while [[digraphs]] may not have any of those.

## Overview of usual technical terms 


> We see one family, in the same room but hardly together. The family of signed, gain, and biased graphs is a lot like that. The Bibliography and Glossary are supposed to lead the family members to talk to one another. May they do so!  ([Thomas Zaslavsky: front page](#HomePageOfSignedGraphs))

The following table is meant to have *pragmatic* value. I has little *epistomological* value. 
It should go without saying for thinking readers that the table does not, like e.g. [[periodic table]] does, describe objective *connections between things*, but merely *conventional connections between language and things*. 
The table describes a clear-enough reality, yet is bound to read dated in the future, even *in substance* rather than style. 


| technical term | distinctive feature |  short verbal definition  | [[signature]]; and axioms, of the [[theory]] (in a narrow sense of "theory")| comments |  
|---------------------|-------------|---------------|---------------|---------------|
|  directed graph |   n/a (context-dependent umbrella-term)       |  n/a |  n/a | n/a   |  
|  [[quiver]] |     loops allowed, parallel arcs allowed     | presheaf on the walking quiver | [[equality| = ]], two function symbols; more than one axioms (how many is up to interpretation)  |  |
|  [[digraph]] |    no loops, no parallel arcs, but 2-cycles allowed     | binary [[irreflexive relation]]  | [[equality| = ]], one relation symbol; one axiom expressing irreflexivity; if [[constructive logic]] is required, signature might be larger, requiring an [[apartness relation]] expressing irreflexivity    |  |
|  oriented [[graph]] |   looks essentially like oriented one-dimensional [[simplicial complex]]   | undirected simple graph whose edges were replaced by one arrow each | dependent on the chosen formalization of [[graph]]; if [[graph]] is formalized as a [[relation|relation]], and the orientedness by [[antisymmetry]], then the signature is: [[equality| = ]], one relation symbol; and the axioms then are: one axiom expressing irreflexivity, one axiom expressing antisymmetry; if [[constructive logic]] is required, the signature might be larger, requiring an [[apartness relation]] expressing irreflexivity |  |
|  signed [[graph]] | undirected [[graph]] with a sign on each edge    | undirected simple [[graph]] together with a function $\{$edges$\}$ $\rightarrow$ $\{-,+\}$,not subject to any axioms | dependent on the chosen formalization of [[graph|undirected simple graph]]; if [[graph|undirected simple graph]] is formalized in one of the usual ways as a [[relation|symmetric irreflexive relation]], and the signs in the usual way as two [[signature|constant symbols]], then the signature is:  [[equality| = ]], one relation symbol, two constant symbols; and the axioms then are: one axiom expressing irreflexivity, one axiom expressing symmetry; note that no axiom to express distinctness of the two constant symbols is necessary, as this, in the usual approach, is built into the signature; if [[constructive logic]] is required, the signature might be larger, requiring an [[apartness relation]] to express irreflexivity  | beware that this should *not* in a natural way be regarded a "directed graph", though they *are* often used in *contexts* together with directed graphs and thus belong on this page; in a sense, "signed graphs" are a non-example, an *odd-one-out*, in particular in that they seem tricky to categorically construct |
|  bidirected [[graph]] |  [[quiver]] with a sign on each vertex-arrow-*[[incidence|incidence relation]]*   | quiver together with function $\{$vertices$\}$ $\times$ $\{$arrows$\}$ $\rightarrow$ $\{-,+\}$, subject to axioms |   |  |

Note that there are two points of view in model theory, one regards [[equality| = ]] as a [[logic|logical symbol]] of a meta-language, the other regards  [[equality| = ]] as a binary relation symbol within the language under investigation. 
In the table, as a reminder that equality plays an important roles in these theories, the latter view was taken. 

## Table of definitions of directed graphs in various references

This is to give a compressed look-up table, quickly usable, telling you what definition of directed graph is being used in the reference you happen to be working with.



| reference | kind of directed graph emphasized in the reference | formalization used; and exact reference to place in reference  | *word* used in reference | miscellaneous further comments |
|---------------------|---|-----|---------------|----------------------|
|  [BangJensenGutin2nd](#DG2nd) |    [[digraph]]               | the one in [[digraph]], except for a needless assumption of a vertex-set being non-empty: an empty vertex-set implies that the binary relation is the empty relation, but this *is* a [[digraph]] |  *digraph*  | beware that that book sometimes treats [[quivers]], but calls them *directed pseudographs* and formalizes those using [[multisets]] of ordered pairs |
| [BondyMurtyt1st](#BondyMurtyFirstEdition) | [[quiver]] | unusually hybrid functional-relational formalization via *families of ordered pairs* | *digraph*; beware that Bondy-Murty-digraphs are *not* [[digraphs]] | aversion to the void: needless assumption of vertex-sets being non-empty; essentially, Bondy-Murty-digraphs$\simeq$Schrijver-digraphs|
| [ChartrandLesniakZhang6th](#CLZ2016) | [[digraph]] | the one in [[digraph]], except for a needless assumption of a digraph being non-empty set: the empty set *is* a [[digraph]] | *digraph* | beware that what the authors call "The First Theorem of Digraph Theory" is a *not* a theorem of "Digraph Theory" in the strictest technical sense of "Digraph Theory"($=$the first-order theory of irreflexive binary relations) since it *uses the language of arithmetic*|
|  [CsabaEtAl2016](#DecompositionProof) |    [[digraph]]               | the one in [[digraph]] |  *digraph*  | |
|  [DiestelGraphTheory4th](#Diestel2010) |    [[quiver]]               | the usual one: cf. [Section 1.10](#Diestel2010), which is the "nuts-and-bolts-definition" in [[quiver]] | *directed graph*; wisely, the contraction *digraph* is used but once in main text, avoiding a clash with [[digraph]] | beware that *directed path* in the book means something different, type-theoretically at least, from *path in a [[digraph]]*: in the book, a *directed path* is itself a [[digraph]], not a sequence of vertices |
|  [HararyGraphTheory1969](#HararyGraphTheory1969) |   [[digraph]]               | the one in [[digraph]]; cf. [Chapter 16](#HararyGraphTheory1969), provided the word "collection" is read "set", which, as is abundantly clear from the context, is what Harary means; Harary is unambiguous that he does not allow digraphs to have loops; so Harary-digraphs are [[digraphs]] |  *digraph* | Harary uses [p. 199, second paragraph](#HararyGraphTheory1969) the unusual term "semiwalk" what is called "wealk walk" in [[digraph]]; note [p. 198, last paragraph](#HararyGraphTheory1969) that Harary's "path" is (modulo "paths" in [[digraph]] not being digraphs but only vertex-sequences) precisely the usual meaning of "path", although he only mentions that there be no point-repetitions: this evidently implies that there are no arc-repetitions; in summary, Harary-paths are [[digraph|paths]] |
|  [FlajoletSedgewick1st](#AnalyticCombinatorics2009) |   [[binary relation]]               | [[binary relations]], formalized in [[material set theory]]-style, cf. [V.5.1](#AnalyticCombinatorics2009) | both  *digraph* and *directed graph* used interchangeably | beware that Flajolet-Sedgwewick-digraphs are just [[binary relations]], *not* [[digraphs]] |
|  [SchrijverComOpt1st](#Schriver2003) |    [[quiver]]               | unusually hybrid formalization via *families of ordered pairs*; Bondy-Murty formalise Schrijver's *family* using a function called $\psi_D$ | *digraph*; beware that Schrijver-digraphs are *not* [[digraphs]] | no aversion to the void here; moreover, note that SchrijverDigraphs$\simeq$Bondy-Murty-digraphs  |
|  [West2002](#West2002) |    [[quiver]]           | unusually hybrid functional-relational formalization via *families of ordered pairs*: cf. [Definition 1.4.2](#West2002); West is very explicit about allowing both loops and multiple directed edges | *digraph* | beware that, as usual in the combinatorial literature, a "path" in [Definition 1.4.6](#West2002) is *itself* a quiver, i.e. does not carry any parametrization-information, i.e. is not a map like [[paths]] are  |



Note that "kind of directed graph" is a used in a loose, undefined sense, sufficiently clear from the context. 


## Signed graphs

A *signed graph* is a [[simple undirected graph|graph]] *each of whose edges has  been assigned one element of a specified two-element set*. 
The latter's elements are customarily interpreted as "signs", and *sometimes* the sign-set is also equipped with arithmetical structure, though this is *not* part of the definition.  

Signed graphs should *not* be regarded to be *directed graphs*. Signs on undirected edges are not the same as directional information. 
Of course, upon *arbitarily specifying a [[total order]] on the vertex set*, the signs *can* be interpreted to contain directional information, but this extraneous choice of total order is not natural.

Signed graphs (and the basic theorems of their theory) are notorious for being rediscovered over and over again; a critically annotated bibliography on signed graphs and their various guises is [Zaslavsky](#ZaslavskyBibliography).


In a sense, the [[theory]] of signed graphs has a [[[model theory|signature]] which contains at least two [[model theory|constant symbols]], whereas e.g. the theory of undirected simple graphs (in the narrowest sense) has none. 

A *signed graph* should *not* be regarded a "directed graph", though they *are* often used in *contexts* together with directed graphs and thus belong on this page; in a sense, "signed graphs" are a non-example, an odd-one-out, in particular in that they seem tricky to categorically construct.  




## Oriented graphs

An *oriented graph* is a [[simple undirected graph|graph]] *each of whose edges has  been given one of the two orientations*. 
As such, *no* multiplicities whatsoever are possible, not even *directed 2-cycles*($=$antiparallel arcs). 
This is the standard meaning of *oriented graph* in combinatorics, the term generally being perceived to signal that even 2-cycles are forbidden, in contrast to [[digraphs]] which may have them. 
There are several ways to formalize "oriented graph", and here we do not describe any of them. 




## Bidirected graphs

Roughly speaking, bidirected graphs are quivers in which *each non-loop arrow gets decorated with _two_ elements drawn from a two-element set fixed in advanced, one thought to be attached to the arrow's tail, the other to its head*. 
Like for signed graphs, the elements of this two-element set are *sometimes* interpreted to be *signs* and equipped with arithmetical structure (essentially, the two-element set is taken to be a two-element [[group]]). 
 
(The treatment of *loops* is slightly controversial in the combinatorical literature, prompting some ad-hoc-ery, and this is explicitly commented on at least once in the literature.)
The category-theoretic literature seems not to have picked up on this so far, and could clarify the issue. 

Bidirected graphs are important in the theory of [[flows]] on [[graphs]]. 





## Connections to category theory

Herein some evident aspects are pointed out explicitly.

### Underlying quivers

A basic connection is that for any category, its [[forgetful functor|underlying]] [[quiver]] is a directed graph. 

Another aspect is that a *nonempty* [[digraph]] never is isomorphic to the [[quiver]] [[forgetful functor|underlying]] any category: such a quiver *always* has a loop at each vertex, which is already enough to rule out any isomorphism. 


### An application of directed graphs to category theory

Briefly, and from a slightly [[model theory|model theoretical]] point of view, the charm of this application is that [[pasting scheme|A. J. Power's pasting theorem]] is an example of a *transfer* of knowledge from a *theory without [[signature (in logic)|function symbols]]* to a *theory with [[signature (in logic)|function symbols]]*. 
(The theory of [[digraphs]], strictly construed, is *purely relational*, while [[higher category theory]] makes essential use of several [[signature (in logic)|function symbols]]).

An example of a use of digraph theory in category theory is giving a rigorous justification of the  notational practice of [[pasting diagrams]]. 
This was achieved in the late 1980s (cf. e.g. [Johnson 1987](#Johnson1987), [Johnson 1989](#Johnson1989), [Power 1990](#Power1990)). 
In this approach, parallel arcs or loops are of secondary importance, and sometimes expressly forbidden, so the work of Johnson and Power can be seen as a genuine application of graph theory to category theory. 


### *All* quivers deemed irreflexive by Lawvere


There is an article of [[William Lawvere]] which is relevant in one precise respect to a disambiguation page such as the present one: *an unusual use of the adjective "irreflexive"*. 
Therein, one reads (cf. ([Lawvere 1989](#GeneralizedGraphs), page 272)) 

> [..] the elementary "parallel process" $E= \bullet\overset{\rightarrow}{\rightarrow}\bullet$ is a reflexive graph which happens to admit only one definition of composition making it into a category $\mathbf{P}$. [..] Its [[actions]] $S^{\mathbf{P}^{\mathrm{op}}}$ are the **irreflexive** graphs (the negative is in a way appropriate even for those objects which happen to have loops at some point $p$, for morphisms are allowed to interchange *any* two such loops).

With "the negative is in a way appropriate" Lawvere explains the use of the strong negation *irr-*, despite such an "irreflexive graph" being permitted to contain loops at *some* of its vertices, which is obviously different from what one would expect from the usual sense of [[irreflexive relation]]. 
This is a usage in need of explanation, all the more against the backdrop of contemporary teaching where the term "simple undirected graph" is often literally defined as symmetric irreflexive relation (on the vertex set).

Some authors have adopted this interesting variant sense of "irreflexive", prompting an additional use of the a modifier "strict" to form a composite "strict irreflexive graph". (cf. ([Brown et al 2008](#GraphsOfMorphismsOfGraphs)), which uses "digraph" as a synonym for "strict irreflexive graph", and this sense of "digraph" is precisely the one in [[digraph]]). 
In a sense, a [[digraph]] is a "strictly-Lawvere-irreflexive graph".



From a graph-theoretical point of view, every digraph is a quiver, but not every quiver is a digraph (again, in the sense of [Gutin and Bang-Jensen 2009](#DG2nd)).

## Cultural differences of style and correctness

### Lawvere's Como comments  

> The subjects of mathematics, like civilizations of mankind, have finite lifespans, which historians are expected to record. (...) Finally, there are the young subjects---combinatorics for instance. Wild-eyed researchers pick from mountains of intractable problems, childishly babbling the first words of what may turn into a new language. Childhood will end with the first S&#233;minaire Bourbaki.
Gian-Carlo Rota: Indiscrete Thoughts. Modern Birkh&#228;user Classics. Chapter "Book Reviews"



At the [[Como]] conference in 1990, [[William Lawvere]] gave a videotaped lecture, in which he makes thoughtful remarks, relevant to the present article and section: 


> I have great problems reading books on graph theory, books and papers on graph theory, because they never tell you exactly what they are talking about. 
Sometimes the graphs are [word inaudible, even when played slower], sometimes they are absolutely reflexive, sometimes they are not. 
Even if they go so far as talking about homomorphisms, I still don't know exactly what that is, i.e., which category are we in? 
What they should do is admit that they are working in three or four *different* categories and they don't know how to pass from one to the other, and so on, and [inaudible words] to simplify.  
But no, they prefer to talk in a vague way and smushing these together. [inaudible] tried to understand some of the problems of graph theorists and get [bogged? locked?] in the first page. 
Does anybody actually know what a graph minor is? 
[some interjection from the audience] Graph minor. Big problem. 
(..) you see, this famous [inaudible works] problem on graph minors. 
Looks like that that might be interesting. 
But I can't determine *exactly* what it is, because, if you read the first parts of the paper, they waffle, you see, they don't give you a *property* (...)
([William Lawvere] in his 1990 lecture at [[Como]], Italy, Villa Olmo)

The above should be understood *in its historical context*, in particular one should be aware that in 1990 several of the textbooks in graph theory now in use had not yet been written, and the [[Graph Minor Theorem]] had not been proved, rather being chipped away at, using ad hoc methods, in pioneering reasearch papers since the early 1980s. 

And yet, [[Lawvere]] touches differences in style, presentation, verifiability and *preservability* that are important to this day, and similar concerns have been voiced by other mathematicians, for example by  [[William Thurston]] and [[Jean-Pierre Serre]].


Concerns about mathematics written in the more semantic, or geometric, style, in particular its *preservation in the minds of people* are known for long, and have been voiced about other fields than [[graph theory]], most notably about [[topology]]. 


[[William Thurston|Thurston]] said:

> It's very hard to do, you know, a brain dump. 
It's very hard to do that. 
William Thurston, Lecture _The Mystery of 3-Manifolds_ at the Clay Research Conference 2010

and

> ... many, many questions about three-manifolds are probably algorithmically doable, it is just a question of whether they are sort-of-humanly-comprehensible. 
I want to say one thing, which is that you can get the software. 
If you really want to look at examples of three-manifolds, it's good to get the software    that I am using on my [machine]. There's a program called [[SnapPea]], it's written mainly by [[Jeff Weeks]], with some other collaborators, and you can get it from [outdated], the best version is for [outdated technical comments], but there are also versions that run on the garden-variety machine with a C-compiler. 
With it, you can do a lot. 
And I think, ultimately, you know, how do you *conserve a theory of mathematics*, I mean, it's a hard thing to do, but, hopefully, I think, there's a chance that somehow the computers will become the experts, down the line, when the current experts are all, senile, or dead, or whatever.
William Thurston, Lecture _Three-dimensional geometry and topology_, Landau Lectures, 1995/6, Part 3, Hebrew University of Jerusalem


There are two interrelated aspects of this concern: 

* How to preserve the insights of mathematicians writing in the semantic style for posterity?

* How to communicate mathematics written in the semantic styles to learners? 


[[Jean-Pierre Serre|Serre]], who is often praised for the clarity and arithmeticality of his style, made remarks similar to Lawvere's and Thurston's, with (pioneering) topology corresponding to (pioneering) graph theory:

> Some theories get simplified. 
Some just drop out of sight. 
For instance, in 1949, I remember I was depressed because every issue of the Annals of Mathematics would contain another paper on topology which was more difficult to understand than the previous ones. 
But nobody looks at these papers any more; they are forgotten (...)
C. T. Chong and Y. K. Leong: _An Interview with Jean-Pierre Serre_. Mathematical Conversations. Selections from The Mathematical Intelligencer. Springer. 2001. pp. 32--38


Again, the above ought to be understood *in its historical context*, in particular with an awareness of the state  mathematics was in in 1949, at a time when [[homotopy groups of sphere]], to which Serre first applied a calculating [[spectral sequence|method]] developed about a decade earlier by [[Jean Leray]], were still being chipped away at in pioneering reasearch papers, using ad hoc methods, and a systematizing theory like [[category theory]] was in its [[General Theory of Natural Equivalences|infancy|]]. 



### To say no, or not to say no: what is simpler? 

The convention of formalising directed graphs like in [[digraph]] is widespread in modern combinatorics, but it is mostly just that: conventional. 
In particular, forbidding parallel arcs, and in particular, forbidding loops by yaking the  [[relative complement]] of $V\times V$ and the diagonal $\{(v,v)\colon v\in V\}$ is sometimes[^1] regarded to be a negative complication. 

This aspect looms large in the context of [[constructive mathematics]].
 
This is a matter of opinion and culture; similar comparisons can be found in what is perhaps the earliest article reviewing graph theory from a category theoretic perspective (cf. [Bumby-Latch 1986](#BumbyLatch1986)).

[^1]: T. Leinster: " ...  the irreflexivity condition tastes strange on a category theorist's tongue. We're suspicious of negatives. " In: [The n-Category Caf&#233;: April 12, 2013](https://golem.ph.utexas.edu/category/2013/04/colouring_a_graph.html)



Some reasonably distinct aspects are:

* While arguably the *simplest nontrivial limit of all*, the definition of [[digraphs]] uses a [[limit]] of the [[category of sets]], the [[cartesian product]] of the vertex set with itself, while the definition of [[quivers]] avoids doing so, and can therefore be interpreted in categories which do not have all binary products. 

* It is a fact that [[quivers]] are more general than [[digraph]]s: to have [[digraph]] offer multiple arcs or loops requires adhocery, like *weight-functions* or hybrid definitions like the use of *families of ordered pairs* (e.g. [Section 10.1](#BondyMurtyFirstEdition)). 
Many references in the combinatorial literature are aware of that,  of course, e.g. ([Diestel 2010](#Diestel2010)) defines a "directed graph" precisely to be a [[quiver]], without mentioning the word.  
The use of [[digraphs]] is not amiss, of course, if *questions* are being analyzed which would make one talk about [[quivers]] *as if they were* [[digraphs]], which is the case for many combinatorial questions, such as about [[tournaments]]; then one might just as well use [[digraphs]] from the outset. 

* The restriction, within modern combinatorics, to [[digraphs]] ($\simeq$ loopless quivers without any parallel arcs) is mostly a result of 

1. the kind *questions* that are answered in the combinatorial literature, which are often of a counting or decomposing kind,
1. a definite tendency in combinatorics to no shy away from *formalizing  multiplicities* by *attaching weights* of some "alien" type (mostly [[number]]s) to the single arc of a graph. 
Model-theoretically speaking, [[combinatorics]] rather uninhibitedly [[model theory|expands the signature]] if the need arises, while [[category theory]]  is reluctant to do so, and hardly ever does. 
Category theory prefers to have its constructions preplanned for a given purpose,  and carried out by a more uniform method. 


The difference between the two formalizations, given in [[digraph]] and [[quiver]], can be seen to be similar to the differences between [[material set theory]] and [[structural set theory]].

The material point of view makes the decision of how to represent the connections loom large (examples are the various different data structures for digraphs, such as signed adjacency matrices, signed incidence matrices, linked lists for adjacency *lists*, one often vastly more efficient than the other).  

The structural point of view, exemplified by [[quivers]], in a way already fixes the formalizing concept: functions. 
It then only remains to be decided how to represent function. 

All these points of view have disadvantages and advantages and it depends on what one is trying to do what one should use.

## Related concepts

* [[digraph]] 
* [[graph]]
* [[quiver]]
* [[n-quiver]]
* [[ribbon graph]]



## References


* A. Bondy, U.S.R. Murty: Graph Theory with Applications. Fifth Printing. North Holland 1982.
{#BondyMurtyFirstEdition}

* Andr&#233; Bouchet: _Nowhere-Zero Integral Flows on a Bidirected Graph_. Journal of Combinatorial Theory, Series B 34, 279--292(1983) 
{#Bouchet1983}

* Gary Chartrand, Linda Lesniak, Ping Zhang: _Graphs & Digraphs_. Sixth edition. CRC Press. 2016
{#CLZ2016}


* B. Csaba, D. K&#252;hn, A. Lo, D. Osthus, A. Treglown: Proof of the 1-factorization and Hamilton decomposition conjectures. Memoirs of the American Mathematical Society, 244 (2016), monograph 1154, 170 pages
{#DecompositionProof}


* [[Ronald Brown]], I. Morris, J. Shrimpton, C.D. Wensley: _Graphs of morphisms of graphs_, The Electronic Journal of Combinatorics 15 (2008), A1
{#GraphsOfMorphismsOfGraphs}

* R. Diestel: _Graph Theory_. Fourth Edition. Springer (2010)
{#Diestel2010}


* [[Philippe Flajolet]], Robert Sedgewick, _Analytic Combinatorics_, 2009 ([pdf](http://algo.inria.fr/flajolet/Publications/book.pdf))
{#AnalyticCombinatorics2009}

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}


* [[Frank Harary]]: _Graph Theory_. Addison Wesley. First Edition. (1969)
{#HararyGraphTheory1969}


* [[Frank Harary]]: _The notion of balance of a signed graph_. 

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}

* [[William Lawvere]]: _Qualitative Distinctions Between Some Toposes of Generalized Graphs_, Contemporary Mathematics 92 (1989) 
{#GeneralizedGraphs}


* [[Eugene L. Lawler]]: _Combinatorial Optimization: Networks and Matroids_, Holt, Rinehart and Winston. (1976)
{#Lawler1976}


* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990}

* [[Alexander Schrijver]]: _Combinatorial Optimization_. Volume A. Springer. First  Edition (2003)
{#Schrijver2003}


* Douglas B. West: _Introduction to Graph Theory_. Second Edition. Pearson Education. (2002)
{#West2002}


* Thomas Zaslavsky: _A Mathematical Bibliography of Signed and Gain Graphs and Allied Areas_, Electronic Journal of Combinatorics, Dynamic Surveys in Combinatorics, #DS8.
{#ZaslavskyBibliography}

* Thomas Zaslavsky: [The Home Page of Signed, Gain, and Biased Graphs](http://people.math.binghamton.edu/zaslav/Bsg/index.html)
{#HomePageOfSignedGraphs}

[[!redirects bidirected graph]]
[[!redirects directed graphs]]
[[!redirects Directed graph]]
[[!redirects Directed graphs]]