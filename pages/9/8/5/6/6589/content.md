
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum field theory
+-- {: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# The Zamolodchikov $c$-theorem
* table of contents
{: toc}

## Idea

The fixed point of a [[renormalization]]-group (RG) transform applied to a [[field theory]] should, intuitively, be described by a theory which is scale-invariant.  The **Zamolodchikov $c$-theorem** makes this precise:  for any renormalizable 2D field theory, there exists a function $c(g)$ of its coupling constants $g = (g_1,g_2,\ldots)$ which

* decreases monotonically with successive RG transforms, and
* at the fixed point of the RG, is equal to the [[Virasoro algebra|central charge]] of the [[conformal field theory]] which describes that critical point.

[Cardy (1996)](#Cardy1996) observes,

: The $c$-theorem has the interpretation that renormalization group flows go 'downhill'.  In particular, it rules out the existence (for systems satisfying reflection positivity) of limit cycles and other esoteric behaviour in renormalization group flows.  It also severely restricts the possible fixed points to which unstable directions at a given fixed point may flow. ... An appealing physical interpretation of the $[c(g)]$-function is as a kind of entropy of information about the critical system.  Under renormalization, information is lost about the short distance behaviour of the correlation functions.  However, this cannot be taken too literally---for example, even at infinite temperature a block spin transformation results in loss of information about the microstates of the system, yet no renormalization group flow takes place.  Presumably, a more complete interpretation along these lines needs to account for the fact that the central charge is sensitive to only the effectively gapless degrees of freedom.

Attempts to find analogues for the 2D $c$-theorem in higher [[dimensions]] have involved versions of [[holographic principle|holographic duality]] such as the [[AdS/CFT correspondence]].  See [Myers and Sinha (2010)](#Myers2010), [(2011)](#Myers2011).


## Proof

We follow the original proof given by [Zamolodchikov (1986)](#Zamolodchikov).

We start with a field theory whose action functional is an integral of a local [[Lagrangian]] density:

$$ S = \int \mathcal{L}(g,a,x) d x, $$

where $a$ is the ultraviolet cutoff of the theory.  The basic assumption of RG is that there exists a single-parameter family of transformations on $Q$, the space of coupling constants,

$$ R_t: Q \rightarrow Q,$$

which has the property that a field theory with the action $S(R_t g, e^t a)$ is equivalent to the original theory with action $S(g, a)$.  Here, _equivalence_ means that the [[correlation function]]s of the two theories agree, as long as we consider scales larger than the renormalized UV cutoff, $x \gg e^t a$.  The RG flow is described by the [[beta function]]s:

$$  d g^i = \beta^i(g) \,d t. $$

At the fixed points, $\beta^i(g) = 0$.  (The beta functions in RG theory should not be confused with the [[Euler beta function]]).  Here, we are using the term in the same sense as when people say, "The beta function in [[QCD]] is negative."

The local energy-momentum tensor $T_{\mu\nu}(x) = T_{\nu\mu}(x)$ satisfies the conservation equation $\partial_\mu T_{\mu\nu} = 0$.  Define the complex coordinates

$$ (z, \bar{z}) = (x^1 + i x^2, x^1 - i x^2) $$

and define $T = T_{zz}$, $\Theta = T_{z\bar{z}}$.  The local scalar fields are given by

$$\Phi_i(g,x) = \frac{\partial}{\partial g^i} \mathcal{L}(g,a,x).$$

If the field theory is renormalizable, we can expand the field $\Theta$ in the basis given by the $\Phi_i$:

$$\Theta = \beta^i(g) \Phi_i.$$

Take a convenient distance scale $x_0$, significantly larger than the UV cutoff of the theory.  This arbitrary value is the "normalization point".  Define

$$ C(g) = 2z^4 \left.\langle T(x) T(0) \rangle\right|_{x^2 = x_0^2} $$

$$ H_i(g) = z^2 x^2 \left.\langle T(x) \Phi_i(0) \rangle\right|_{x^2 = x_0^2} $$

$$ G_{i j}(g) = x^4 \left.\langle \Phi_i(x) \Phi_j(0) \rangle\right|_{x^2 = x_0^2} $$

The positivity condition of the field theory implies that the symmetric [[matrix]] $G_{i j}(g)$ is positive definite, and that we can use it as the [[metric space|metric]] in the space of coupling constants.  

The **Callan--Symanzik equation** describes how the $n$-point [[correlation function]]s vary under the RG transform.  For our purposes, the scaling matrix $\gamma$ which appears in the Callan-Symanzik equation is given by

$$ \gamma_i^{\,j} (g) \Phi_j = \left(\frac{a}{2} \frac{\partial}{\partial a} - \beta^k \frac{\partial}{\partial g^k}\right) \Phi_i = (\partial_i \beta^j) \Phi_j.$$

We combine our expansion of the field $\Theta$ with the conservation condition $\partial_\mu T_{\mu\nu} = 0$ and the Callan--Symanzik equation to get

$$ \frac{1}{2} \beta^i\partial_i C = -3\beta^i H_i + \beta^i\beta^k\partial_k H_i + \beta^k(\partial_k \beta^i) H_i, $$

and

$$ \beta^k \partial_k H_i + (\partial_i \beta^k)H_k - H_i = -2\beta^k G_{i k} + \beta^j \beta^k G_{i j} + \beta^j (\partial_i \beta^k) G_{j k} + \beta^j (\partial_j \beta^k) G_{i k}, $$

where we have written $\partial_i$ for the derivative in the coupling-constant space, $\partial/\partial g^i$.

For the function

$$c(g) = C(g) + 4\beta^i H_i = 6\beta^i \beta^j G_{i j},$$

we have that

$$\beta^i \partial_i c(g) = -12 \beta^i \beta^j G_{i j}.$$

This verifies that

$$ \frac{d c}{d t} = \beta^i(g) \partial_i c(g) \leq 0, $$

establishing that the function $c(g)$ decreases monotonically as we apply the RG transform.

Consider a fixed point $g_*$, and choose a coordinate system centered on that point, so that the metric becomes

$$ G_{i j}(g) = \delta_{i j} + \mathcal{O}(g^2). $$

Near the fixed point, we can calculate $c(g)$ using [[perturbation theory]].  This calculation results in

$$ c(g) = \tilde{c}(g_*) - 3(2 - d_i) g^i g^i + 2C_{i j k} g^i g^j g^k + \mathcal{O}(g^4). $$

We have written $d_i$ for the [[anomalous dimension]]s of the vectors $\Phi_i(g_*, x)$, which at the fixed point are conformal fields.  It then follows that the 2D field theory at the fixed point has conformal symmetry, with an infinite set of generators

$$\{L_n | n = 0, \pm 1, \pm 2, \ldots \}$$

which satisfy the [[Virasoro algebra]]

$$ [L_n, L_m] = (n - m)L_{n+m} + \frac{\tilde{c}}{12}(n^3 - n) \delta_{n+m,0}. $$

The fixed-point value of the $c$-function becomes the central charge of the Virasoro algebra.  The central charge is the numerical coefficient in the correlation function

$$\langle T(z) T(0) \rangle = z^{-4} \tilde{c}(g_*) / 2.$$

Near the fixed point, we can also compute the beta functions in perturbation theory.

$$ \beta^i(g) = \frac{2 - d_i}{2} g^i - \frac{1}{2} C_{i j k} g^j g^k + \mathcal{O}(g^3).$$

Note that to maintain consistency of indices across both sides of this equation, we do not sum over $i$ in the first term.  If the perturbations are "soft", satisfying $|2 - d_i| \ll 1$, then the coefficients $C_{i j k}$ form the structure constants of a [[CFT]] operator algebra.  Raising the indices on $G_{i j}$ by $G^{i k}G_{k j} = \delta^i_{\,j}$, we can write
 
$$\beta^i(g) = -\frac{1}{12} G^{i j}(g) \partial_j c(g).$$


## References

* A. B. Zamolodchikov (1986), _"Irreversibility" of the Flux of the Renormalization Group in a 2-D Field Theory_, JETP Lett. **43**: 730--732. ([pdf](http://www.jetpletters.ac.ru/ps/1413/article_21504.pdf))
  {#Zamolodchikov}
* J. Cardy (1996), _Scaling and Renormalization in Statistical Physics._ Cambridge Lecture Notes in Physics.
  {#Cardy1996}
* J. Cardy (2010), _The Ubiquitous 'c': From the Stefan--Boltzmann Law to Quantum Information_, J.Stat.Mech. **2010**: P10004, ([arXiv:1008.2331](http://arxiv.org/abs/1008.2331))
  {#Cardy2010}
* R. C. Myers and A. Sinha (2010), _Seeing a $c$-theorem with holography_, Physical Review D **82**: 046006, ([arXiv:1006.1263](http://arxiv.org/abs/1006.1263))
  {#Myers2010}
* R. C. Myers and A. Sinha (2011), _Holographic $c$-theorems in arbitrary dimensions_, Journal of High Energy Physics **2011**, 1: 1--53, ([arXiv:1011.5819](http://arxiv.org/abs/1011.5819))
  {#Myers2011}
* Z. Komargodski and A. Schwimmer (2011), _On renormalization group flows in four dimensions_, ([arXiv:1107.3987](http://arxiv.org/abs/1107.3987))
  {#Komargodski2011}
* Wikipedia, [Callan--Symanzik equation](http://en.wikipedia.org/wiki/Callan%E2%80%93Symanzik_equation)
