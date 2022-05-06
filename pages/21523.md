
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Tate sphere_, in the strict sense, is the [[object]] in a [[sheaf topos]] (or [[(∞,1)-sheaf (∞,1)-topos]], or its [[stabilization]]) over a [[gros site]] of [[algebraic varieties]], which is one of the following: $\mathbb{P}^{1}$ (the [[projective line]]); the quotient

$$ 
  S^1_{Tate}
  \;\coloneqq\;
  \mathbb{A}^1 / (\mathbb{A}^1 \setminus \{0\})
  \,,
$$

which denotes the ([[homotopy cofiber|homotopy]]-)[[cofiber]] of the inclusion morphism into the [[sheaf]] [[representable functor|represented]] by the [[affine line]] $\mathbb{A}^1$ from the [[subobject]] $\mathbb{A}^1 \setminus \{0\}$ [[representable functor|represented]] by the affine line with origin removed (equivalently the object underlying the [[multiplicative group]] $\mathbb{G}_m$); or $S^{1} \wedge \mathbb{G}_{m}$.

These constructions are understood by default in the context of [[motivic homotopy theory]] working over the [[Nisnevich site]] ([VRO 07, Remark 2.22](#VRO07)), where they are all $\mathbb{A}^{1}$-homotopy equivalent.
But the construction principle, especially that of the homotopy cofibre definition, is clearly more general.

In formal constructions of categories of [[motive|motives]], one typically 'inverts the Tate sphere' in some sense in order to represent [[Tate twist|Tate twists]] correctly in [[Weil cohomology theory|Weil cohomology theories]] such as [[étale cohomology]], or in [[motivic cohomology|motivic cohomology theories]]. This is the case, for example, both for the [[stable motivic homotopy category|stable motivic homotopy categories]] à la [[Vladimir Voevodsky|Voevodsky]], where one more precisely inverts the operation of smashing with the Tate sphere, and for the category of [[pure motive|pure motives]], where one inverts the [[Lefschetz motive]]. 

To be more precise, we have the following, which is Theorem 10.2 in [MazzaVoevodskyWeibel2006](#MazzaVoevodskyWeibel2006).

\begin{thm} Let $X$ be a smooth, separated [[scheme]] over a [[field]] $k$. Let $n$ be an integer prime to the characteristic of $k$. Then for every integer $p$ and every integer $q \geq 0$, we have that $H^{p,q}_{L}(X, \mathbb{Z} / n)$, the étale (or Lichtenbaum) motivic cohomology of $X$, is isomorphic to $H^{p}_{et}\left(X, \mathbb{Z}/n(q) \right)$, the [[étale cohomology]] of $X$ with coefficients in the $q$-th [[Tate twist]] of $\mathbb{Z}/n$. \end{thm}

The inverting of smashing with the Tate sphere as opposed to just with $S^{1}$ in the construction of the stable motivic homotopy category allows the $q$ part of motivic cohomology to be represented in it (by the motivic Eilenberg-MacLane spectrum), as opposed to just the $(p,0)$ part. Combining this with the above theorem, we see that inverting the Tate sphere as opposed to just $S^{1}$ allows the Tate twists of étale cohomology to be represented.   

## Related concepts

* [[motivic homotopy theory]]

* [[n-sphere]]

* [[Tate twist]]

## References

* {#MazzaVoevodskyWeibel2006} Mazza, [[Vladimir Voevodsky|Voevodsky]], [[Chuck Weibel|Weibel]], _Lecture notes on motivic cohomology_, Clay Mathematics Monographs 2. Providence, RI: American Mathematical Society (AMS); Cambridge, MA: Clay Mathematics Institute. xiv, 216 p. (2006). [zentralblatt](https://zbmath.org/?q=an%3A1115.14010) [pdf](http://www.claymath.org/library/monographs/cmim-2-voevodsky-cov1.pdf)

* {#VRO07} [[Vladimir Voevodsky]], [[Oliver Röndigs]], [[Paul Arne Østvær]], _Voevodsky’s Nordfjordeid Lectures: Motivic Homotopy Theory_, In:  [[Bjørn Ian Dundas]], [[Marc Levine]], [[Paul Arne Østvær]], [[Oliver Röndigs]], [[Vladimir Voevodsky]] (eds.), _Motivic Homotopy Theory_,  Springer 2007 ([doi:10.1007/978-3-540-45897-5_7](https://doi.org/10.1007/978-3-540-45897-5_7), [pdf](https://www.math.ias.edu/vladimir/sites/math.ias.edu.vladimir/files/Nordfjordeid_lectures_published.pdf))

[[!redirects Tate spheres]]

