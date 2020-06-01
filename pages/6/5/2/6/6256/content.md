
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

## Idea

There are several theorems of [[Ernest Michael]] from the 1950s about [[paracompactness]]. There is also Michael's 1972 characterization of paracompact [[locally compact spaces]] under certain class of quotient maps.  

## Statement

+-- {: .num_prop #RegularSpacesWherOpenCoveringIsRefinedbyCountableLocallyFiniteConnectionsofOpensAreParacompact}
###### Proposition
**(detection of paracompactness, [Michael 53, theorem 1](#Michael53))**

Let $X$ be a [[topological space]] such that

1. $X$ is [[regular topological space|regular]];

1. every [[open cover]] of $X$ has a [[refinement]] by a union of a [[countable set]] of 

   [[locally finite sets of subsets|locally finite]] sets of open subsets (not necessarily covering). 

Then $X$ is [[paracompact topological space]].

=--

Prop. \ref{RegularSpacesWherOpenCoveringIsRefinedbyCountableLocallyFiniteConnectionsofOpensAreParacompact} immediately implies that 

* [[second-countable regular spaces are paracompact]],

* [[locally compact and sigma-compact spaces are paracompact]].


+-- {: .num_prop }
###### Proposition
**(on the closed image of a paracompact space, [Michael 57, corollary 1](#Michael57))**

The [[image]] of a [[paracompact Hausdorff space]] under a [[closed maps|closed]] [[continuous function]] is also paracompact Hausdorff.

=--

+-- {: .num_prop }
###### Proposition
**(Michael [[selection theorem]])** 

A [[lower semicontinuous map]] from a [[paracompact topological space]] $X$ to a [[Banach space]] $E$ with convex closed values has a continuous subrelation which is a function. If this is true for a given topological space $Y$ instead of $E$ and all such functions and codomains $E$, then $Y$ is paracompact. 

=--

## Related entries

* [[selection theorem]]


## References

The original articles are the following:

* {#Michael53} [[Ernest Michael]], _A note on paracompact spaces_, Proc. Amer. Math. Soc. 1953 ([jstor](http://www.jstor.org/stable/2032419), [pdf](http://www.renyi.hu/~descript/papers/Michael_parakompakt.pdf))

* {#Michael57} [[Ernest Michael]], _Another note on paracompactness_, 1957, ([pdf](krein.unica.it/~cornelis/private/PDF/AMS/PAMS_8_822.pdf), [pdf](http://www.ams.org/journals/proc/1957-008-04/S0002-9939-1957-0087079-9/S0002-9939-1957-0087079-9.pdf))

* [[Ernest Michael]], _Continuous selections. I_, Annals of Math. __63__ (2): 361&#8211;382 ([doi:10.2307/1969615](http://dx.doi.org/10.2307/1969615), MR0077107)


* [[Ernest Michael]], _A quintuple quotient test_, Gen. Topol. Appl. __2__ (1972) 91&#8211;138, [link](www.sciencedirect.com/science/article/pii/0016660X729004021972)

* discussion at A. Mathew's [blog](http://amathew.wordpress.com/2010/08/19/a-theorem-of-michael-on-paracompactness) and also on an application to metric spaces [here](http://amathew.wordpress.com/2010/08/19/a-metric-space-is-paracompact)

See also:

* R. Engelking, _General topology_

* [[Kenneth Kunen]], _Paracompactness of box products of compact spaces_, Trans. Amer. Math. Soc. __240__, (1978) 307-316, [jstor](http://www.jstor.org/stable/1998822)

* [[Akhil Mathew]], _[A theorem of Michael on paracompactness](https://amathew.wordpress.com/2010/08/19/a-theorem-of-michael-on-paracompactness/)_


* wikipedia [Michael selection theorem](http://en.wikipedia.org/wiki/Michael_selection_theorem)

[[!redirects Michael theorem]]

[[!redirects Michael's theorems]]
