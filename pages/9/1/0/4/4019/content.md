
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
* the following line creates the automatic table of contents
{:toc}


## Idea ##
Linear operators on [[Hilbert spaces]] are continuous precisely iff they are bounded. A bornological space retains this property by definition.

+-- {: .standout}
The discussion below is about bornological CVSes, but there is a more general notion of [[bornological space]].
=--

## Definition ##

A [[locally convex]] [[topological vector space]] $E$ is **bornological** if every circled, convex subset $A \subset E$ that absorbs every [[bounded set]] in $E$ is a neighbourhood of $0$ in $E$. Equivalently every [[seminorm]] that is bounded on bounded sets is continuous.

The **bornology** of a given [[TVS]] is the family of bounded subsets.

Given a locally convex [[TVS]] $E$ with initial topology $T_0$, there is a finest topology $T$ such that the family of bounded subsets of $T$ coincides with $T_0$. The space $E$ equipped with the topology $T$ is called the **bornologification** of $E$, or the **bornological space associated with** $(E, T_0)$

## Properties ##
+-- {: .un_theorem}
###### Theorem
Let $U$ be a linear map from a bornological space $E$ to any locally convex [[TVS]], then the following statements are equivalent:

* $U$ is continuous,

* $U$ is bounded on bounded sets,

* $U$ maps [[null sequence|null sequences]] to null sequences.
=--

## Examples ##
Every metrizible locally convex space is bornological, that is every [[Fréchet space]] and thus every [[Banach space]].

## References ##

* Wikipedia about [bornological spaces] (http://en.wikipedia.org/wiki/Bornological_space)

* Helmut Sch&#228;fer: _Topological Vector Spaces_, chapter 8. 

  
[[!redirects bornologification]]

[[!redirects bornological vector space]]
[[!redirects bornological vector spaces]]
[[!redirects bornological topological vector spaces]]
[[!redirects Bornological topological vector space]]


