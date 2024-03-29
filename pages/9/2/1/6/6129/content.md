
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In the context of a [[manifold structure of mapping spaces|mapping space]], an important family of [[smooth maps]] are the 
[[evaluation maps]].  That is, for a [[sequentially compact]] [[Froelicher space|Frölicher space]] $S$ and a [[manifold]] $M$, we pick a [[point]] $p \in S$ and consider the map $ev_p \colon C^\infty(S,M) \to M$ given by $ev_p(\alpha) = \alpha(p)$.  This is [[smooth function|smooth]] (see [[smooth maps of mapping spaces]]).  At $q \in M$, the [[fibre]] is the space of smooth maps $S \to M$ which take $p$ to $q$.  This is again a smooth manifold (as shown in [[manifold structure of mapping spaces]]).  Providing $M$ has enough diffeomorphisms, this is the projection of a [[fibre bundle]].  That is to say, the sequence:
\[
C^\infty(S,p;M,q) \to C^\infty(S,M) \to M
\]
is a fibre bundle.

The remark about "enough diffeomorphisms" is the key to proving this.  To prove that this is a fibre bundle, we need to show that if $\beta \colon S \to M$ nearly takes $p$ to $q$ then we can deform $\beta$ to a map which takes $p$ to $q$ on the nose.  Knowing that $M$ has the structure of a manifold, we can interpret the statement "$\beta(p)$ is close to $q$" as meaning that we have fixed a [[coordinate chart|chart]] near $q$ and require that $\beta(p)$ be in the [[codomain]] of that chart.  We therefore have a good choice of deformation for $\beta(p)$ itself: deform it along the "straight line" from $q$ to $\beta(p)$ as defined by the chart.  The problem with this is that it only tells us what to do with $\beta(p)$, not with the rest of $\beta$.  So we need to drag the rest of $\beta$ along with $\beta(p)$.  This is where the diffeomorphisms come in: instead of moving $\beta(p)$ along a path, we deform the entire manifold using a diffeomorphism so that $\beta(p)$ is taken to $q$.  We do this using the methods of [[propagating flows]].
