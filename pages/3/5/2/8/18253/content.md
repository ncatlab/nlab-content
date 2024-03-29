
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement


+-- {: .num_lemma #RegularSpacesWherOpenCoveringIsRefinedbyCountableLocallyFiniteConnectionsofOpensAreParacompact}
###### Lemma
**([[Michael's theorem]], [Michael 53, theorem 1](#Michael53))**

Let $X$ be a [[topological space]] such that

1. $X$ is [[regular topological space|regular]];

1. every [[open cover]] of $X$ has a [[refinement]] by a union of a [[countable set]] of [[locally finite sets of subsets|locally finite]] sets of open subsets (not necessarily covering). 

Then $X$ is [[paracompact topological space]].

=--

Note that while in Michael's paper he assumes that paracompact spaces are Hausdorff, the assumption is not necessary, and the proof goes through for regular non-Hausdorff spaces.  See Kelley, p. 156.

+-- {: .num_prop }
###### Proposition
**(second-countable regular spaces are paracompact)**

Let $X$ be a [[topological space]] which is

1. [[second-countable topological space|second-countable]];

1. [[regular topological space|regular]].

Then $X$ is [[paracompact topological space]].

=--

+-- {: .proof}
###### Proof

Let $\{U_i \subset X\}_{i \in I}$ be an open cover. By [[Michael's theorem]] (lemma \ref{RegularSpacesWherOpenCoveringIsRefinedbyCountableLocallyFiniteConnectionsofOpensAreParacompact}) it is sufficient that we find a [[refinement]] by a [[countable cover]].

But second countability implies precisely that every open cover has a countable subcover:


Every open cover has a refinement by a cover consisting of [[base for the topology|base]] elements, and if there is only a countable set of these, then the resulting refinement necessarily contains at most this countable set of distinct open subsets.


=--

## Related statements

* [[locally compact and sigma-compact spaces are paracompact]]

* [[locally compact and second-countable spaces are sigma-compact]]

* [[CW-complexes are paracompact Hausdorff spaces]]

## References

* Kelley, _General Topology_, 1955.

* {#Michael53} [[Ernest Michael]], _A note on paracompact spaces_, Proc. Amer. Math. Soc. 1953 ([jstor](http://www.jstor.org/stable/2032419), [pdf](http://www.renyi.hu/~descript/papers/Michael_parakompakt.pdf))


* [[Akhil Mathew]], _[A theorem of Michael on paracompactness](https://amathew.wordpress.com/2010/08/19/a-theorem-of-michael-on-paracompactness/)_

