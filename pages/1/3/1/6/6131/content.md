+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

## Idea ##

As shown in [[evaluation fibration of mapping spaces]] and [[tubular neighbourhoods of mapping spaces]], if we carve out a submanifold of a mapping space by specifying "coincidences", we often get a tubular neighbourhood.  On this page, we shall give an example of a submanifold with no tubular neighbourhood.  The example is simple to describe.  To make it concrete, we shall fix as our source space the circle, $S^1$.  For our target space, we shall take a finite dimensional smooth manifold, $M$.  The full smooth mapping space, $C^\infty(S^1, M)$ is known as the [[smooth loop space]].  For simplicity, let us take _based_ loops within this, which we write as $\Omega M$.  Within that, we consider the space of based smooth maps $S^1 \to M$ which are infinitely flat at the point $1 \in S^1$.  Let us write this as $\Omega_&#9837; M$.  As we are using based loops, we can identify the tangent space of $M$ at the basepoint with $\mathbb{R}^n$ and so we have a sequence, which is exact by [[Borel's theorem]]:
\[
\Omega_&#9837; M \to \Omega M \to \prod_{j = 1}^\infty \mathbb{R}^n
\]

It is easy to show that this does not admit a tubular neighbourhood.  If it did, there would be a splitting of the induced map on tangent spaces:
\[
T_\alpha \Omega_&#9837; M \to \Omega_\alpha M \to \prod_{i = 1}^\infty \mathbb{R}^n
\]
but as the second map is surjective, this cannot split as a splitting map would induce a continuous injection from $\prod_{i=1}^\infty \mathbb{R}^n$ to a normed vector space and that is impossible.