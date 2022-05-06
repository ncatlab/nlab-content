
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The 3 classical _Euler angles_ furnish a global parametrization and a smooth [[coordinate system]] on a big dense cell of the [[Lie group]] [[special orthogonal group|SO(3)]] of [[rotation]]s in 3 dimensions, or on its double cover, $SU(2)$ group. Its essential feature is that it supplies a multiplicative decomposition of arbitrary rotation into 3 elements belonging to distinguished 1-parametric subgroups of rotations $SO(2) = U(1)$ around 2 coordinate axes, where the classical choices are z-x-z and the angular parameters for the elements in distinguished $SO(2)$ are the Euler angles. 

Generalized constructions apply to some other [[Lie groups]].

## Construction for $SU(2)$

(Following Vilenkin) Every $SU(2)$ matrix can be written in a form

$$
      u = \left(\array{ a & b \\ - \overline{b} & \overline{a} }\right)
$$
where $a,b\in\mathbf{C}$, $det(u) = 1$ and $|a|^2 + |b|^2 = 1$. The simplest parametrization is to take $|i|, arg(a)$ and $arg(b)$ as independent parameters. 
If $a b \neq 0$ then there are unique parameters $\phi,\theta,\psi$ called Euler angles such that
$$
|a| = cos\frac{\theta}{2} ,
\,\,\,\,\,\,
arg(a) = \frac{\phi+\psi}{2},
\,\,\,\,\,\,
arg(b) = \frac{\phi-\psi+\pi}{2}
$$
and we can take $O\leq \phi\lt 2\pi$, $0\lt\theta\lt\pi$, $-2\pi\leq\psi\lt 2\pi$.
If $a=0$ or $b = 0$ then we can find triples $(\phi,\theta,\psi)$ satisfying the above system but the choice is not necessarily unique. In any case, the matrix $u$ is now

$$
u(\phi,\theta,\psi):= u = \left(\array{ 
cos\frac{\theta}{2} e^{i\frac{\phi+\psi}{2}}& i sin\frac\theta{2}e^{i\frac{\phi-\psi}{2}} 
\\ i sin\frac\theta{2}e^{i\frac{\psi-\phi}{2}} & cos\frac\theta{2} e^{i\frac{\phi+\psi}{2}} 
}\right)
$$

There is a decomposition

$$
u(\phi,\theta,\psi) = \left(\array{
e^{\frac{i\phi}{2}}&0\\0&e^{-\frac{i\phi}{2}}
}\right)
\left(\array{
cos\frac\theta{2}&i sin\frac\theta{2}\\
i sin\frac\theta{2}&cos\frac\theta{2}
}\right)
\left(\array{
e^{\frac{i\psi}{2}}&0\\0&e^{-\frac{i\psi}{2}}
}\right) 
$$

The standard homomorphism $SU(2)\to SO(3)$ sends this Euler angles to classical Euler angles for $SO(3)$; the map is surjective if we restrict to values
$\theta\in[0,2\pi]$ as the classical Euler angle bounds suggests. 


## Related concepts

* [[Pauli matrix]]

## References

* Wikipedia, _[Euler angles](https://en.wikipedia.org/wiki/Euler_angles)_

* WolframMath, _[Euler angles](http://mathworld.wolfram.com/EulerAngles.html)_

* N. Ja. Vilenkin, _Special functions and representation theory of groups $SO(n)$_

* L. C. Biedenharn, J. D. Louck, _The angular momentum in quantum physics_, Enc. Math Appl. __8__, Addison-Wesley 1981

* S. Bertini, S. L. Cacciatori, B. L. Cerchiai, _On the Euler angles for $SU(N)$_, J. Math. Phys. __47__:4, id.043510 (2006) [doi](https://doi.org/10.1063/1.2190898) [arxiv:math-ph/0510075](https://arxiv.org/math/abs/0510075)

[[!redirects Euler angles]]