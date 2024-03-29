
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is known as the _prime geodesic theorem_ is a result that descrives the [[asymptotic]] distribution of [[prime geodesics]] on a [[hyperbolic manifold]]. 

The prime geodesic theorem is [[analogy|analogous]] to the [[prime number theorem]]. Just as the zeros of the [[Riemann zeta function]] control the error term in the prime number theorem, so the zeros of the [[Selberg zeta function]] control the error term in the prime geodesic theorem.

## Statement

Let $X$ be a [[hyperbolic manifold]] of [[dimension]] $d + 1$. Let

$$
  \Gamma \coloneqq \pi_1(X)
$$

be its [[fundamental group]]. 

For each element $\gamma \in \Gamma$ there exists one closed [[geodesic]] in $X$ representing it. By standard convenient abuse of notation we write $\gamma$ also for that geodesic. Write

* $l(\gamma)$ for the [[length]] of the geodesic $\gamma$;

* $N(\gamma) \coloneqq e^{l(\gamma)}$ for what is called its _norm_;

* $\pi_\Gamma(x)$ for the number of primitive elements $\gamma \in \Gamma$ such that $N(\gamma) \leq x$.

The _prime geodesic theorem_ is a statement of the form that this number $\pi_\Gamma(x)$ satisfies

$$
  \pi_\Gamma(x)
  =
  li(x^d)
  + 
  \underoverset{n = 0}{N}{\sum} li(x^{s_n}) + (error\;term)
$$

where 

* $li(x) = \underoverset{0}{x}{\int}\frac{d t}{ln t}$ is the [[logarithmic integral function]];

* $\{s_1, \cdots, s_N\}$ are the zeros of the [[Selberg zeta function]] in the interval $(d/2,d)$

* $(error\;term)$ is some term, estimates of which are the main content of this class of theorems.

## References

The original estimates are due to [[Atle Selberg]], Hejhal, Huber, and [[Peter Sarnak]].

* [[Peter Sarnak]], _Prime Geodesic Theorems_, Stanford University, 1980

Further developments include

* Koyama _Prime geodesic theorem for arithmetic compact surfaces_, Int Math Res Notices (1998) 1998 ([web](http://imrn.oxfordjournals.org/content/1998/8/383.extract))

* Maki Nakasuji, _Prime Geodesic Theorem for Higher-Dimensional Hyperbolic Manifold_, Transactions of the AMS, Vol. 358, No. 8, 2006 ([JSTOR](http://www.jstor.org/stable/3845331), [pdf](http://www.ams.org/journals/tran/2006-358-08/S0002-9947-06-04122-5/S0002-9947-06-04122-5.pdf))

* {#SoundararajanYoung13} K. Soundararajan, Matthew P. Young, _The Prime Geodesic Theorem_,J. Reine Angew. Math. 676 (2013), 105-120 ([arXiv:1011.5486](http://arxiv.org/abs/1011.5486))

Discussion for the case of simple geodesics in hyperbolic surfaces contains

* [[Igor Rivin]], _Simple Curves on Surfaces_, Geometriae Dedicata August 2001, Volume 87, Issue 1-3, pp 345-360 ([web](http://link.springer.com/article/10.1023%2FA%3A1012010721583))

* [[Maryam Mirzakhani]], _Growth of the number of simple closed geodesics on hyperbolic surfaces_, Pages 97-125 from Volume 168 (2008), Issue 1 ([web](http://annals.math.princeton.edu/2008/168-1/p03))

