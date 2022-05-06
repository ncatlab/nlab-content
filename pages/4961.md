
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

* $Codisc(S)$ is the topological space on $S$ whose only open sets are the [[empty set]] and $S$ itself,

  this is called the **codiscrete topology** on $S$ (also _indiscrete topology_ or _trivial topology_ or _chaotic topology_), it is the [[coarser topology|coarsest topology]] on $S$; $Codisc(S)$ is called a _[[codiscrete space]]_.

For an axiomatization of this situation see _[[codiscrete object]]_.

## Properties


+-- {: .num_example}
###### Example

Let $S$ be a [[set]] and let $(X,\tau)$ be a [[topological space]]. Then 

1. every [[continuous function]] $(X,\tau) \longrightarrow Disc(S)$ is [[locally constant function|locally constant]];

1. every [[function]] (of sets) $X \longrightarrow CoDisc(S)$ is [[continuous function|continuous]].

=--

## References

The terminology _chaotic topology_ is motivated (see also at _[[chaos]]_) in

* {#Lawvere84} [[William Lawvere]], _Functorial remarks on the general concept of chaos_ IMA preprint #87, 1984 ([pdf](http://www.ima.umn.edu/sites/default/files/87s.pdf)) 

via footnote 3 in

* [[William Lawvere]],  _Categories of spaces may not be generalized spaces, as exemplified by directed graphs_, preprint, State University of New York at Buffalo, (1986) Reprints in Theory and Applications of Categories, No. 9, 2005, pp. 1&#8211;7 ([tac:tr9](http://www.tac.mta.ca/tac/reprints/articles/9/tr9abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/9/tr9.pdf))

and appears for instance in 

* [[The Stacks Project]], _[Example 7.6.6](https://stacks.math.columbia.edu/tag/07GE)_

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