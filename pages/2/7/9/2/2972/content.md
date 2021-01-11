
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Generally in a context of [[Kaluza-Klein compactification]] a _dilaton_ is a [[field (physics)|field]]  on a lower-dimensional [[spacetime]] which is a component of the field of [[gravity]] on a higher dimensional spacetime, in that it is part of the [[pseudo-Riemannian metric|metric]] of the [[fiber]]-spaces on which the KK-compactification takes place. Specifically for KK-compactification on a [[circle]] fiber "the dilaton" (or "radion") is the lowest [[Fourier series|Fourier]] mode of the metric of the circle, hence is the [[length]] (circumference) (or [[radius]], up to a factor) of the circle fiber.

The subtlety in [[Kaluza-Klein theory]] is that the dilaton should have small but approximately constant value in order to yields [[effective field theory]] gravity coupled to [[gauge theory]] in lower dimensions from pure gravity in higher dimensions. This is the problem of _[[moduli stabilization]]_.

Specifically in [[string theory]], together with the field of [[gravity]] and the [[Kalb?Ramond field]], the _dilaton field_ is one of the three massless [[boson|bosonic fields]] that appears in [[effective QFT|effective background]] [[quantum field theory|quantum field theories]]. For [[type IIA string theory]] this may be interpreted as the Kaluza-Klein dilaton in the above sense, arising from [[11-dimensional supergravity]] ([[M-theory]]) compactified on a circle. Similarly for [[heterotic string theory]] and [[Horava-Witten theory]].

## Details

### Action functional of dilaton gravity

Let $X$ be a [[compact space|compact]] [[smooth manifold]]. Write $Conf$ for the [[configuration space]] of [[pseudo-Riemannian metric]]s $g$ (the [[graviton]]) and of [[smooth function]]s $f$ (the _dilaton_ ) on $X$.

The [[action functional]] for [[dilaton gravity]] is

$$
  S : Conf \to \mathbb{R}
$$

$$
  S : (g,f) \mapsto \int_X e^{-f}(R_g dvol_g+ d f \wedge \star_g d f) 
  \,,
$$

where $R_g$ is the [[Riemann curvature]] scalar of $g$ and $\star_g$ the [[Hodge star operator]] and $dvol_g$ is the [[volume form]] of $g$.

For $f = 0$ this reduces to the [[Einstein-Hilbert action]]. For $f = const$ it is still a multiple of the Einstein-Hilbert action functional.

The [[gradient flow]] of this functional is [[Ricci flow]].

### Global cohomological description

The global nature of the gravitational field and the Kalb--Ramond field are well understood conceptually: the gravitational field is a [[pseudo-Riemannian metric]] and the Kalb--Ramond field is a cocycle in third integral [[differential cohomology]] (for instance realized by a cocycle in [[Deligne cohomology]] or by a [[bundle gerbe]] with connection). 

In [[generalized complex geometry]], both these fields are shown to be unified as one single [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued]] form field: a connection on a [[standard Courant algebroid]] (as described in more detail there). 

While it was clear that the diaton field is locally just a real-valued function, is formal global identification has not been understood in an analogous manner for a long time.

But a proposal for a precise conceptual identification of the dilaton as a structure appearing in the context of [[generalized complex geometry]] is in

* Mariana Gra&#241;a, Ruben Minasian, Michela Petrini, Daniel Waldram, _T-duality, generalized geometry and non-geometric backgrounds_ ([arXiv](http://arxiv.org/abs/0807.4527))

## Applications

The [[gradient flow]] of the [[action functional]] for [[dilaton gravity]] is essentially [[Ricci flow]].

## Related concepts

* [[JT-gravity]]

[[!include fields and quanta - table]]


## References

The derivation of dilaton gravity as part of the [[effective QFT]] of [[string theory]] is discussed for instance aroung page 911 of

* [[Eric D'Hoker]], _String theory_ in [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], (eds.) _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


[[!redirects dilaton field]]

[[!redirects dilaton gravity]]