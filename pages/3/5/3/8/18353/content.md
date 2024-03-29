
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

The Kahn-Priddy theorem characterizes a comparison map between [[cohomology]] with [[coefficients]] in the [[suspension spectrum]] of the infinite [[real projective space]] $\mathbb{R}P^\infty \simeq B \mathbb{Z}/2$ and [[stable cohomotopy]].

## Statement

Write $\mathbb{R}P^\infty \in Ho(Top)$ for the [[homotopy type]] of [[real projective space]] (an object in the [[classical homotopy category]]), and write $\Sigma^\infty \mathbb{R}P^\infty_+ \in Ho(Spectra)$ for its [[suspension spectrum]] regarded as an [[H-group ring spectrum]] in the [[stable homotopy category]]. 

For each $n$ there is a canonical inclusion (see [Whitehead 83, p. 20](#Whitehead83)).

$$
  \mathbb{R}P^{n-1}
     \hookrightarrow
  O(n)^+
$$

due to Hopf 35, which is compatible with the inclusions as $n$ varies

$$
  \array{
    \mathbb{R}P^{n-1}
      &\hookrightarrow&
    O(n) 
    \\
    \downarrow && \downarrow
    \\
    \mathbb{R}P^n 
       &\hookrightarrow&
    O(n+1)
  }
$$

and hence induces an inclusion

$$
  \mathbb{R}P^\infty \hookrightarrow O
$$

> check

Composing this with the [[J-homomorphism]] gives a map 

$$
  \phi \;\colon\; \Sigma^\infty \mathbb{R}P^\infty \longrightarrow \mathbb{S}
$$ 

from the [[H-group ring spectrum]] of infnite [[real projective space]] to the [[sphere spectrum]].

Then for $X$ a connected 2-primary finite [[CW-complex]], the function that takes stable maps into this H-group ring spectrum to maps to the [[sphere spectrum]], hence to the [[stable cohomotopy]] of $X$

$$
  \phi_X
    \;\colon\;
  [\Sigma^\infty X_+ , \Sigma^\infty \mathbb{R}P^\infty_+ ]
    \overset{surj.}{\longrightarrow}
  [\Sigma^\infty X_+, \mathbb{S}]
$$

is [[surjective function|surjective]].

In this form this is stated in [Adams 73, lemma 3.1](#Adams73) (see the notation introduced below lemma 2.2: for $p = 2$ then Adams's $L$ is $\mathbb{R}P^\infty$).

## Analog for complex projective space 

The statement was announced in the above  form in [Segal 73, prop. 2](#Segal73), where the analogous statement for [[complex projective space]] and [[topological K-theory]] is proven (see [this prop.](complex+projective+space#HGroupRingSpectrumSurjectsOntoTopologicalKTheory)):

$$
  [\Sigma^\infty X_+ , \Sigma^\infty \mathbb{C}P^\infty_+ ]
    \overset{surj.}{\longrightarrow}
  K_{\mathbb{C}}(X)
  \,.
$$

Notice that [[Snaith's theorem]] asserts that this map becomes in fact an [[isomorphism]] to [[reduced K-theory]] after quotienting out the [[Bott generator]] $\beta \in \Sigma^\infty \mathbb{C}P^\infty_+$.



## References

The original formulation is due to 

* {#KahnPriddy72} [[Daniel Kahn]], [[Stewart Priddy]], _Applications of the transfer to stable homotopy theory_, Bull. Amer. Math. Soc. Volume 78, Number 6 (1972), 981-987 ([Euclid](https://projecteuclid.org/euclid.bams/1183534135))

A strengthening was obtained in

* {#Adams73} [[John Frank Adams]], _The Kahn-Priddy theorem_, Mathematical Proceedings of the Cambridge Philosophical Society, Mathematical Proceedings of the Cambridge Philosophical Society 55, 1973

Review is in 

* {#Whitehead83} [[George Whitehead]], pages 20, 21 of _Fifty years of homotopy_, Bulletin of the AMS, Volume 8, Number 1, 1983 ([pdf](http://www.ams.org/journals/bull/1983-08-01/S0273-0979-1983-15072-3/S0273-0979-1983-15072-3.pdf))


The analogous statement for [[complex projective space]] and complex [[topological K-theory]] is due to

* {#Segal73} [[Graeme Segal]], _The stable homotopy of complex of projective space_, The quarterly journal of mathematics (1973) 24 (1): 1-5. ([[Segal72.pdf:file]], [doi:10.1093/qmath/24.1.1]( https://doi.org/10.1093/qmath/24.1.1))

