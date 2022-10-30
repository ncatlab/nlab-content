
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Chern classes_ are the [[integral cohomology|integral]] [[characteristic class]]es 

$$
  c_i : B U \to B^{2 i} \mathbb{Z}
$$

of the [[classifying space]] $B U$ of the [[unitary group]].

Accordingly these are characteristic classes of $U$-[[principal bundle]]s and hence of [[complex numbers|complex]] [[vector bundle]]s.

The first Chern class is the unique characteristic class of [[circle group]]-principal bundles.

The analogous classes for the [[orthogonal group]] are the [[Pontryagin class]]es.

## Definition

+-- {: .num_defn}
###### Definition

For $n \geq 1$ the Chern universal [[characteristic classes]] $c_i \in H^{2i}(B U(n), \mathbb{Z})$ of the [[classifying space]] $B U(n)$ of the [[unitary group]] are characterized as follows:

1. $c_0 = 1$ and $c_i = 0$ if $i \gt n$;

1. for $n = 1$, $c_1$ is the canonical generator of $H^2(B U(1), \mathbb{Z})\simeq \mathbb{Z}$;

1. under pullback along the inclusion $i : B U(n) \to B U(n+1)$ we have $i^* c_i^{(n+1)} = c_i^{(n)}$;

1. under the inclusion $B U(k) \times B U(l) \to B U(k+l)$ we have $i^* c_i = \sum_{j = 0}^i c_i \cup c_{j-i}$.

=--

## Properties

### General 

+-- {: .num_prop}
###### Proposition

The [[cohomology ring]] of $B U(n)$ is the [[polynomial]] algebra on the Chern classes:

$$
  H^\bullet(B U(n), \mathbb{Z})
  \simeq
  \mathbb{Z}(c_1, \cdots, c_n)
  \,.
$$

=--


### First Chern class

* The First Chern class of a bundle $P$ is the class of its [[determinant line bundle]] $det P$

  $$
    c_1(P) = [det P]
    \,.
  $$

  See [[determinant line bundle]] for more.

## Related concepts 

* [[Pontryagin class]]

* [[Stiefel-Whitney class]]

* [[Chern character]]

In [[Yang-Mills theory]] field configurations with non-vanishing second Chern-class (and minimal energy) are called [[instanton]]s. The second Chern class is the _instanton number_ .

## References

Standard textbook references include

* [[John Milnor]], [[Jim Stasheff|James D. Stasheff]], _Characteristic Classes_, Annals of Mathematics Studies 76, Princeton University Press (1974). 


or chapter IX of volume II of

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)


* [[A. Grothendieck]], _La th&#233;orie des classes de Chern_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __86__ (1958), p. 137--154, [numdam](http://www.numdam.org/item?id=BSMF_1958__86__137_0)

A brief introduction is in chapter 23, section 7 

* [[Peter May]], _A concise course in algebraic topology_ ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))


[[!redirects Chern classes]]