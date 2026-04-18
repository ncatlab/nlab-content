
> This is about the [[topological space]] of the [[set of truth values]] equipped with the [[Scott topology]]. For the set of Sierpinski semi-decidable truth values, which is sometimes called *Sierpi&#324;ski space* in [[predicative]] [[constructive mathematics]], see at [[semi-decidable proposition]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn }
###### Definition

The __Sierpi&#324;ski space__ $\Sigma$ is the [[topological space]] 

1. whose underlying set has two elements, say $\{0,1\}$,

1. whose set of [[open subsets]] is $\left\{ \emptyset, \{1\}, \{0,1\}  \right\}$.

(We could exchange "0" and "1" here, the result would of course be [[homeomorphism|homeomorphic]]).

Equivalently we may think of the underlying [[set]] as the set of [[classical mathematics|classical]] [[truth values]]  $\{\bot, \top\}$, equipped with the [[specialization topology]], in which $\{\bot\}$ is [[closed subset|closed]] and $\{\top\}$ is an [[open subset|open]] but not conversely.

The corresponding [[locale]] is given by the three-element frame $\{\bot \lt \omega \lt \top\}$.

=--


+-- {: .num_remark }
###### Remark

In [[constructive mathematics]], the Sierpi&#324;ski locale is given by the free frame over one element. More concretely, its opens are $O_{p \le q}$ indexed by pairs of truth values $(p, q)$ such that $p \le q$. The partial order is given by $O_{p \le q} \le O_{p' \le q'}$ iff $p \le p'$ and $q \le q'$. This is also the [[specialization topology|Alexandroff locale]] over the poset of *classical* truth values.

The corresponding topological space however, has the point set given by *all* truth values. The open subsets are $O_{p \le q} = \{\varphi \mid p \vee (q \wedge \varphi)\}$. Importantly, it is not homeomorphic to the Alexandroff topology on the set of truth values, or classical truth values.

=--

## Properties

### As a topological space

This Sierpinski space 

* is a [[contractible space]];

* is a [[locally contractible space]];

* has a [[focal point]];

* is a [[sober topological space]] (but not [[separation axiom|T1]]).

According properties are inherited by the [[Sierpinski topos]] and the [[Sierpinski (∞,1)-topos]] over $Sierp$.


### As a classifier for open/closed subspaces

The Sierpinski space $S$ is a classifier for [[open subspaces]] of a [[topological space]] $X$ in that for any open subspace $A$ of $X$ there is a unique [[continuous function]] $\chi_A: X \to S$ such that $A = \chi_A^{-1}(\top)$.  

Dually, it classifies [[closed subsets]] in that any closed subspace $A$ is $\chi_A^{-1}(\bot)$.  Note that the closed subsets and open subsets of $X$ are related by a [[bijection]] through [[complement|complementation]]; one gets a topology on the set of either by identifying the set with $\Top(X,\Sigma)$ for a suitable [[function space]] topology.  (This part does not work as well in [[constructive mathematics]].)

## Related concepts

* [[empty space]], [[point space]]

* [[Cantor space]]

* [[Sierpinski topos]], [[Sierpinski (∞,1)-topos]]

* [[Stone duality]]

* [[separation axioms in terms of lifting properties]]

* In [[synthetic topology]], an analogue of the Sierpinski space is called a [[dominance]]. 

  * [[Sierpinski dominance]]

## References

* Wikipedia, _[Sierpinski space](https://en.wikipedia.org/wiki/Sierpi%C5%84ski_space)_

* [[Paul Taylor]],  _Foundations for computable topology -- 7 The Sierpinski space_ ([html](http://www.paultaylor.eu/ASD/foufct/sierpinski.html))

* [[Andrej Bauer]], [[Davorin Lešnik]], *Metric spaces in synthetic topology* Annals of Pure and Applied Logic, Volume 163, Issue 2, February 2012, Pages 87-100 ([doi:10.1016/j.apal.2011.06.017](https://doi.org/10.1016/j.apal.2011.06.017))

[[!redirects Sierpinski space]]
[[!redirects Sierpiński space]]
[[!redirects Sierpinski topology]]
[[!redirects Sierpiński topology]]