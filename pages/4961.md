[[!redirects discrete and codiscrete topology]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The [[forgetful functor]] $\Gamma : Top \to Set$ from [[Top]] to [[Set]] that sends any [[topological space]] to its underlying [[set]] has a [[left adjoint]] $Disc : Set \to Top$ and a [[right adjoint]] $Codisc : Set \to Top$.
$$
  (Disc \dashv \Gamma \dashv Codisc) : 
  Top
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  Set
  \,.
$$


For $S \in Set$

* $Disc(S)$ is the [[topological space]] on $S$ in which every subset is an [[open set]],

  this is called the **discrete topology** on $S$, it is the [[finer topology|finest topology]] on $S$; $Disc(S)$ is called a [[discrete space]];

* $Codisc(S)$ is the topological space on $S$ whose only open sets are the [[empty set]] and $S$ itself, which is called the **indiscrete topology** on $S$ (rarely also __antidiscrete topology__ or __codiscrete topology__ or __trivial topology__ or __chaotic topology__ ([[SGA4|SGA4-1, 1.1.4]])), it is the [[coarser topology|coarsest topology]] on $S$; $Codisc(S)$ is called a __indiscrete space__ (rarely also __antidiscrete space__, even more rarely __codiscrete space__).

For an axiomatization of this situation see _[[codiscrete object]]_.

## Properties


+-- {: .num_example}
###### Example

Let $S$ be a [[set]] and let $(X,\tau)$ be a [[topological space]]. Then 

1. every [[continuous function]] $(X,\tau) \longrightarrow Disc(S)$ is [[locally constant function|locally constant]];

1. every [[function]] (of sets) $X \longrightarrow CoDisc(S)$ is [[continuous function|continuous]].

=--

### The left adjoint of the discrete space functor

The functor $Disc$ does not [[preserved limit|preserve]] [[infinite products]]
because the infinite [[product topological space]] of discrete spaces may be nondiscrete.
Thus, $Disc$ does not have a [[left adjoint functor]].

However, if we restrict the [[codomain]] of $Disc$
to [[locally connected spaces]], then the [[left adjoint functor]]
of $Disc$ does exist and it computes the set of [[connected components]] of a given [[locally connected space]], i.e., is the $\pi_0$ functor.

This is discussed at _[locally connected spaces -- cohesion over sets](locally+connected+topological+space#CohesionOverSets)_
and [[cosheaf of connected components]].

## References

The terminology _chaotic topology_ is motivated (see also at _[[chaos]]_) in

* {#Lawvere84} [[William Lawvere]], _Functorial remarks on the general concept of chaos_ IMA preprint #87, 1984 ([pdf](http://www.ima.umn.edu/sites/default/files/87s.pdf)) 

and via footnote 1 (page 3) in

* [[William Lawvere]],  _Categories of spaces may not be generalized spaces, as exemplified by directed graphs_, preprint, State University of New York at Buffalo, (1986) Reprints in Theory and Applications of Categories, No. 9, 2005, pp. 1&#8211;7 ([tac:tr9](http://www.tac.mta.ca/tac/reprints/articles/9/tr9abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/9/tr9.pdf)).

In the context of [[Grothendieck topologies]], this appears for instance in 

* [[The Stacks Project]], _[Example 7.6.6](https://stacks.math.columbia.edu/tag/07GE)_

following [[SGA4|SGA4-1, 1.1.4]].

[[!redirects discrete topology]]

[[!redirects discrete topologies]]
[[!redirects discrete topological structure]]
[[!redirects discrete topological structures]]
[[!redirects discrete topological space]]
[[!redirects discrete topological spaces]]

[[!redirects codiscrete topology]]
[[!redirects codiscrete topologies]]
[[!redirects codiscrete topological structure]]
[[!redirects codiscrete topological structures]]

[[!redirects codiscrete topological space]]
[[!redirects codiscrete topological spaces]]

[[!redirects co-discrete topological space]]
[[!redirects co-discrete topological spaces]]

[[!redirects chaotic topology]]
[[!redirects chaotic topologies]]
[[!redirects chaotic topological space]]
[[!redirects chaotic topological spaces]]

[[!redirects indiscrete topology]]
[[!redirects indiscrete topologies]]
[[!redirects antidiscrete topology]]
[[!redirects antidiscrete topologies]]
[[!redirects indiscrete space]]
[[!redirects indiscrete spaces]]
[[!redirects antidiscrete space]]
[[!redirects antidiscrete spaces]]