
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _numerable open cover_ (alias _normal cover_) is an [[open cover]] of a [[topological space]] that admits a subordinate [[partition of unity]]. 

## Definition

Let $\{U_i\}$ be an open [[cover]] of the [[topological space]] $X$ (actually [Dold 1963](#Dold63) doesn't always require open, see discussion below). It is said to be **numerable** if there is a collection of [[continuous functions]] $\phi_i \colon X \to [0,1]$ (to the [[closed interval]]) such that:

1. the [[support]] of the $i$th function is contained in the $i$th subset:

   $Supp(\phi_i) \subset U_i$;

1. at each point $x\in X$, only a [[finite number]] of the $\phi_i$ are non-zero;

1. $\underset{x \in X}{\forall}  \sum_i \phi_i(x) \equiv 1  $.

(The functions $\{\phi_i\}$ are a [[partition of unity]].)

The collection of [[preimages]] $\phi_i^{-1}(0,1]$ then constitute a [[locally finite cover]] that [[refinement|refines]] $\{U_i\}$. 



## Alternative characterizations

\begin{proposition}
**([[Ernest Michael]], [[Kiiti Morita]], [[Arthur H. Stone]], see [Morita 1962, Thm. 1.2](#Morita62))**
\linebreak                         
For an [[open cover]] $\{U_i\}_{i\in I}$ of a [[topological space]] $X$ the following properties are equivalent.                      

* $U$ is a numerable cover, i.e., it admits a compatible positive partition;

* ([Michael 1953, Prop. 2](#Michael53)) $U$ admits a subordinate locally finite [[partition of unity]];

* ([Stone, Thms. 1, 2](#Stone).) $U$ is a normal cover, meaning there is a sequence $W_0=U$, $W_1$, $W_2$, $\ldots$ of open covers of $X$ such that $W_{n+1}$ is a [[star refinement]] of $W_n$ for all $n\ge0$;

* $U$ can be refined by the [[inverse image]] of an open cover of $Y$ under some continuous map $X\to Y$, where $Y$ is a [[metrizable topological space]];

* ([Mardešić & Segal 1982, Lemma I.6.1](#MardesicSegal82)) $U$ can be refined by the inverse image of an open cover of $Y$ under some continuous map $X\to Y$, where $Y$ is an absolute neighborhood retract, i.e., a metrizable topological space $Y$ such that any closed embedding $Y\to Z$ into a metrizable topological space $Z$ factors through an open subset $U\subset Z$ such that there is a map $U\to Y$ for which the composition $Y\to U\to Y$ is identity;

* $U$ can be refined by a locally finite normal open cover;

* $U$ can be refined by a locally finite open cover consisting of cozero sets;

* ([Michael 1953, Thm. 1](#Michael53), [Morita 1964, Thm. 1.2](#Morita64).) $U$ can be refined by an open cover given by the union of a countable collection of locally finite families of cozero sets.

* ([Michael 1953, Proposition 1](#Michael53), [Hoshina 1989, Theorem 1.1 and 1.2](#Hoshina89)) $U$ can be refined by an open cover given by the union of a countable collection of discrete families of cozero sets.

\end{proposition}

## Properties

### As a coverage, as a site

Numerable open covers form a [[site]] called the **numerable site**. More precisely, numerable open covers are a [[coverage]] on the category [[Top]] of topological spaces (this is essentially given in [Dold's lectures, A.2.17](#DoldLectures), but not using this terminology).


For [[paracompact topological spaces]], numerable covers are [[cofinal functor|cofinal]] in open covers, so that the numerable site is equivalent to the open cover site for such spaces.

There is also a 1944 result by Dieudonnne that numerable covers are cofinal in [[locally finite open cover|locally finite covers]] of [[normal spaces]] — need to add this! See, eg, Theorem 6.3 of Howes' _Modern analysis and topology_.

### Relation to numerable bundles

Many classical theorems concerning [[fiber bundles]] are stated for the numerable site. For example, the [[classifying space]] $\mathcal{B}G$ actually classifies [[bundles]] which trivialise over a numerable cover. (References? Dold for [[Milnor's classifying space]], and tom Dieck I think for Segal's) These are called [[numerable bundles]]. This is because the standard constructions of the universal bundle by Minor and Segal both are trivialisable over a numerable cover.


## References ##

* {#Stone} [[Arthur H. Stone]], _Paracompactness and product spaces_, Bulletin of the American Mathematical Society 54:10 (1948), 977–983 $[$[doi:10.1090/S0002-9904-1948-09118-2](https://doi.org/10.1090/S0002-9904-1948-09118-2)$]$

* {#Michael53} [[Ernest Michael]], _A note on paracompact spaces_, Proceedings of the American Mathematical Society 4:5 (1953) 831–838  $[$[doi:10.1090/S0002-9939-1953-0056905-8](https://doi.org/10.1090/S0002-9939-1953-0056905-8)$]$

* {#Morita62} [[Kiiti Morita]], _Paracompactness and product spaces_, Fundamenta Mathematicae 50:3 (1962), 223–236 $[$[doi:10.1090/S0002-9939-1991-1054165-6](https://doi.org/10.1090/S0002-9939-1991-1054165-6)$]$

* {#Dold63} [[Albrecht Dold]], _Partitions of unity in the theory of fibrations_, Ann. of Math. **78** 2 (1963) 223–255 $[$[MR0155330](http://www.ams.org/mathscinet-getitem?mr=155330) [jstor:1970341](http://www.jstor.org/stable/1970341) [doi:10.2307/1970341](http://dx.doi.org/10.2307/1970341)$]$


* {#Morita64} [[Kiiti Morita]], _Products of normal spaces with metric spaces_, Mathematische Annalen 154:4 (1964), 365–382 $[$[doi:10.1007/BF01362570](https://doi.org/10.1007/BF01362570)$]$


* {#MardesicSegal82} [[Sibe Mardešić]], [[Jack Segal]], _Shape Theory_,  North-Holland Mathematical Library 26 (1982).

* {# Hoshina89} Takao Hoshina, _Extensions of mappings II_, Topics in General Topology, Elsevier (1989).

The appendix of

* {#DoldLectures} [[Albrecht Dold]], _Lectures on algebraic topology_

talks about "stacked covers": these are useful for 'decomposing' numerable covers of products to a sort of parameterised version depending on a numerable cover of the first factor. This is important in looking at concordance of numerable bundles.

Detailed review of numerable covers and discussion of [[descent]] over them for [[simplicial presheaves]] via a [[Brown-Gersten property]]:

* [[Dmitri Pavlov]], *Numerable open covers and representability of topological stacks* &#x5B;[arXiv:2203.03120](https://arxiv.org/abs/2203.03120)]



[[!redirects numerable open covers]]

[[!redirects numerable cover]]
[[!redirects numerable covers]]
