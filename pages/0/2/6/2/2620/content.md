
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

"Harmonic oscillator" is a fancy name for a rock on a spring: 

* in [[classical mechanics]] it is the [[physical system]] given by a point mass in a parabolic potential, feeling [[forces]] driving it back to a specified origin that are propertional to the distance of the [[mass]] from that origin.

* in [[quantum mechanics]] and in particular [[quantum field theory]] the quantum harmonic oscillator governs not just the dynamics of idealized point masses but crucially appears in the dynamics of all free massive quantum fields. 

To quote the field theorist Sidney Coleman,
> The career of a young theoretical physicist consists of treating the harmonic oscillator in ever-increasing levels of abstraction.

## Classical oscillator

First the harmonic oscillator in [[classical mechanics]].

The [[force]] exerted by a spring is proportional to how far you stretch it:
\[F = k x.\]
The [[potential energy]] stored in a stretched spring is the integral of that:
\[V_0 = \frac{1}{2}k x^2 + C,\]
and to make things work out nicely, we're going to choose $C = -1/2.$  The total [[energy]] $H_0$ is the sum of the potential and the kinetic energy:
\[H_0 = V_0 + T = \frac{1}{2}k x^2 + \frac{1}{2}m v^2 - \frac{1}{2}.\]
By choosing units so that $k = m = 1,$ we get
\[H_0 = \frac{x^2}{2} + \frac{p^2}{2} - \frac{1}{2},\]
where $p$ is momentum.

## Quantum harmonic oscillator

Now the harmonic oscillator in [[quantum mechanics]].

We [[quantization|quantize]], getting a quantum harmonic oscillator, or QHO.  We set $p = -i \frac{\partial}{\partial x},$ taking units where $\hbar = 1.$  Now 
\[\array{ [x, p]x^n & = & (x p - p x)x^n \\ & = &(- x i \frac{\partial}{\partial x} + i \frac{\partial}{\partial x} x)x^n \\ & = & -i(n x^n - (n+1)x^n) \\ & = & i x^n. }\]

If we define a new [[observable]] $z = \frac{p + ix}{\sqrt{2}},$ then 
\[\array{ z z^* & = & \frac{(p + i x)}{\sqrt{2}} \frac{(p - i x)}{\sqrt{2}} \\ & = & \frac{1}{2}(p^2 + i(x p - p x) + x^2) \\ & = & \frac{1}{2}(p^2 -1 + x^2) \\ & = & H_0. }\]
We can think of $z^*$ as $\frac{d}{dz}$ and write the energy [[eigenvector]]s as [[polynomial]]s in $z:$
\[H_0 z^n = z \frac{d}{dz} z^n = n z^n.\]  
The creation operator $z$ adds a photon to the mix; there's only one way to do that, so $z\cdot z^n = 1 z^{n+1}.$  The annihilation operator $\frac{d}{dz}$ destroys one of the photons; in the state $z^n$, there are $n$ [[photon]]s to choose from, so $\frac{d}{dz} z^n = n z^{n-1}.$

[[Schrodinger equation|Schrödinger's equation]] says $i \frac{d}{dt} \psi = H_0 \psi,$ so 
\[\psi(t) = \sum_{n=0}^{\infty} e^{-itn} a_n z^n.\]
This way of representing the state of a QHO is known as the _Fock basis_.

## Related concepts

* [[hydrogen atom]]

* [[quantum lattice system]]

## References

### General

* [[Howard Georgi]], Section 1 of: *The Physics of Waves*, Prentice Hall (1993) $[$[web](https://www.people.fas.harvard.edu/~hgeorgi/new.htm), [pdf](https://www.people.fas.harvard.edu/~hgeorgi/onenew.pdf)$]$

### Geometric quantization

Discussion of [[geometric quantization]] of the harmonic oscillator is in 

* Adrian Lim, _A non-standard geometric quantization of the harmonic oscillator_ ([pdf](http://www.math.cornell.edu/~pclim/Docs/papers/oscillator6.pdf))

* G. Sherry, _Geometric quantization of the 3-dimensional harmonic oscillator_, Quaestiones Mathematicae, 8 (1986)

* Sergey V. Zuev, _Geometric quantization of generalized oscillator_ ([arXiv:math-ph/9902024](http://arxiv.org/abs/math-ph/9902024))

### Categorification

A program initiated by [[John Baez]] aims to identify a [[categorification]] of sorts of the quantum harmonic oscillator

The notes

* [[John Baez]]'s [Fall '03](http://math.ucr.edu/home/baez/qg-fall2003/) Quantum gravity seminar 

relate wavefunctions expressed in the Fock basis to [[structure types]].

This originates in

* [[John Baez]], [[James Dolan]], _From finite sets to Feynman diagrams_ ([arXiv](http://arxiv.org/abs/math/0004133)).

For more along these lines see

* [[Jeffrey Morton]], _Categorified Algebra and Quantum Mechanics_ ([arXiv](http://arxiv.org/abs/math/0601458))


[[!redirects quantum harmonic oscillators]]

[[!redirects harmonic oscillator]]
[[!redirects harmonic oscillators]]

