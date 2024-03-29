
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Given a point in 4-dimensional [[Minkowski spacetime]], its _celestial_ (or _heavenly_) _sphere_ is the  space of lines in its [[light cone]], hence the [[projective space]] of its [[light cone]].

We can equivalently speak of rays in the past light cone (or rays in the future light cone); then your celestial sphere (the one around the point where your head is) is the sphere of which you directly perceive a portion when you look. (Since our eyes face forward, we actually see only a small portion of this sphere, but some birds see the entire sphere.) If you take the point to be Earth, then this celestial sphere is the sphere of the heavens as it appeared to the ancients.

## Properties

### Spinorial coordinates

By the [exceptional spin isomorphism](spin+group#ExceptionalIsomorphisms) 

$$
  Spin(3,1) \simeq SL(2,\mathbb{C})
$$

one may identify points $(x^i) = (x^0, x^1, x^2, x^3)$ in [[Minkowski spacetime]] with [[Hermitean matrices]]

$$
  \left(x^{\alpha \beta}\right)
  \coloneqq
  (x^i \gamma_i^{\alpha \beta})
  =
  \tfrac{1}{\sqrt{2}}
  \left(
    \array{
       x^0 + x^3 & x^1 + i x^2
       \\
       x^1 - i x^2 & x^0 - x^3
    }
  \right)
$$

(where $\gamma_i$ denote the generators of the [[Clifford algebra]] given by the [[Pauli matrices]]). This is such that the [[Lorentz metric]] [[norm]] is just the [[determinant]] of this [[matrix]]

$$
  \Vert \left(x^i\right) \Vert 
   = 
   2 det\left(\left(x^{\alpha \beta} \right)\right)
  \,.
$$

From this one finds that $\left(x^i\right)$ is [[lightlike]] precisely if there is a [[spinor]] $\kappa$, hence a pair of [[complex numbers]] $\xi, \eta \in \mathbb{C}$ 

$$
  \left(\kappa^a\right) = 
  \left(
    \array{
      \xi
      \\
      \eta
    }
  \right)
  \,,
$$

such that

$$
  x^{\alpha \beta} = \kappa^\alpha \overline{\kappa}^{\beta}
  \,.
$$

Therefore the celestial sphere is equivalently the space of such pairs of complex numbers, modulo rescaling $\kappa \mapsto c \kappa$ for $0 \neq c \in \mathbb{C}$. This identifies the celestial sphere with the [[complex projective space]] 

$$
  CelestialSphere \simeq \mathbb{C}P^1
  \,,
$$

the [[Riemann sphere]].

### As a coset space of the Lorentz group

The celestial sphere may be given as a [[coset space]] of the [[Lorentz group]]. For the moment see [here](sphere#AsQuotientsOfLorentzGroups) at *[[n-sphere]]*.


## Related concepts

* [[twistor space]] 

* [[Moebius transformation]] 

* [[celestial amplitude]]

## References

* Blagoje Oblak, _From the Lorentz Group to the Celestial Sphere_ ([arXiv:1508.00920](http://arxiv.org/abs/1508.00920))

See also:

* Wikipedia, *[Celestial sphere](https://en.wikipedia.org/wiki/Celestial_sphere)*

[[!redirects celestial sphere]]
[[!redirects celestial spheres]]
[[!redirects heavenly sphere]]
[[!redirects heavenly spheres]]

