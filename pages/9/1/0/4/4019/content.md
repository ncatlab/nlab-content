
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea ##

Linear operators on [[normed space|normed spaces]] are continuous precisely iff they are bounded. A bornological space retains this property by definition.

+-- {: .standout}
The discussion below is about bornological CVSes, but there is a more general notion of [[bornological space]].
=--

## Definition ##

A [[locally convex]] [[topological vector space]] $E$ is **bornological** if every circled, convex subset $A \subset E$ that absorbs every [[bounded set]] in $E$ is a neighbourhood of $0$ in $E$. Equivalently every [[seminorm]] that is bounded on bounded sets is continuous.

The **bornology** of a given [[TVS]] is the family of bounded subsets.

Given a locally convex [[TVS]] $E$ with initial topology $T_0$, there is a finest topology $T$ such that the family of bounded subsets of $T$ coincides with $T_0$. The space $E$ equipped with the topology $T$ is called the **bornologification** of $E$, or the **bornological space associated with** $(E, T_0)$

## Properties ##

### Maps on bornological spaces

+-- {: .num_theorem}
###### Theorem
Let $U$ be a linear map from a bornological space $E$ to any locally convex [[TVS]], then the following statements are equivalent:

* $U$ is continuous,

* $U$ is bounded on bounded sets,

* $U$ maps [[null sequence|null sequences]] to null sequences.
=--

### Relation to Banach spaces

Every [[inductive limit]] of [[Banach spaces]] is a bornological vector space. ([Alpay-Salomon 13, prop. 2.3](#AlpaySalomon13))

Conversely, every bornological vector space is an inductive limit of [[normed spaces]], and of [[Banach spaces]] if it is quasi-complete ([Schaefer-Wolff 99](#SchaeferWolff99))


## Examples ##

Every metrizible locally convex space is bornological, that is every [[Fréchet space]] and thus every [[Banach space]].

## Related concepts

* [[bornological set]]

* [[bornological group]]

* [[bornological space]]

## References ##

* Wikipedia about [bornological spaces] (http://en.wikipedia.org/wiki/Bornological_space)

* {#SchaeferWolff99} H. H. Schaefer with M. P. Wolff, section 8 of _Topological vector spaces_, Springer 1999

* {#AlpaySalomon13} Daniel Alpay, Guy Salomon, _On algebras which are inductive limits of Banach spaces_ ([arXiv:1302.3372](http://arxiv.org/abs/1302.3372))


Discussion of bornological vector spaces forming a [[quasi-abelian category]] is in 

* {#ProsmansSchneiders} [[Fabienne Prosmans]], [[Jean-Pierre Schneiders]], _A homological study of bornological spaces_, December 2000, Prepublications Mathematiques de l'Universite Paris 13, 46 ([pdf](http://www.analg.ulg.ac.be/jps/rec/hsbs.pdf))

with review and generalization to [[bornological abelian groups]] in 

* {#Bambozzi14} [[Federico Bambozzi]], section 1 of _On a generalization of affinoid varieties_ ([arXiv:1401.5702](http://arxiv.org/abs/1401.5702))



  
[[!redirects bornologification]]

[[!redirects bornological vector space]]
[[!redirects bornological vector spaces]]
[[!redirects bornological topological vector spaces]]
[[!redirects Bornological topological vector space]]


