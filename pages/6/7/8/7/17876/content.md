
# Locally decomposable spaces
* table of contents
{: toc}

## Idea

*Local decomposability* is a sort of [[separation axiom]], like a weak sort of [[regular space|regularity]], that is trivial in [[classical mathematics]], but interesting in [[constructive mathematics]].


## Definition

A [[topological space]] $X$ is **locally decomposable** if for any open set $U\subseteq X$ and point $x\in X$, there exists an open set $V$ with $x\in V$ such that for all $y\in X$ we have either $y\in U$ or $y\notin V$.  If [[excluded middle]] holds, of course, we can take $V = U$.

For [[point-set apartness spaces]], which are equivalent to certain topological spaces, the condition can be rephrased as: if $x\bowtie A$, then there is a set $B$ such that $x\bowtie B$ and for all $y$ we have either $y\bowtie A$ or $y\in B$.

For [[uniform spaces]], the notion of [[uniformly regular space|uniform regularity]] is really a notion of "uniform local decomposability"; but since in the uniform case it is sufficient to imply full regularity, we generally call it "uniform regularity" instead.  For [[quasi-uniform spaces]] this is no longer true (since after all, there are non-regular quasi-uniform spaces classically), so we should speak of uniform local decomposability instead.


## References

* [[Douglas Bridges]], Peter Schuster, and Luminita Vita, *Apartness, Topology, and Uniformity: a Constructive View*, [doi](http://dx.doi.org/10.1002/1521-3870%28200210%2948:1%2B%3C16::AID-MALQ16%3E3.0.CO;2-7)
 {#BSV}


[[!redirects locally decomposable space]]
[[!redirects locally decomposable spaces]]
[[!redirects locally decomposable topological space]]
[[!redirects locally decomposable topological spaces]]
[[!redirects locally decomposable apartness space]]
[[!redirects locally decomposable apartness spaces]]
[[!redirects local decomposability]]
