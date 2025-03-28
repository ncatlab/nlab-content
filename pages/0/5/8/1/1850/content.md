
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

In [[electromagnetism]] the [[electromagnetic field]] is modeled by a degree 2 [[differential cohomology|differential cocycle]] $\hat F \in H(X, \mathbb{Z}(2)_D^\infty)$ (see [[Deligne cohomology]]) with curvature characteristic 2-form $F \in \Omega^2(X)$.

With $\star$ denoting the [[Hodge star]] operator with respect to the corresponding pseudo-Riemannian metric on $X$, the right hand of

$$
  d \star F = j_{el} \in \Omega^3(X)
$$

is the [[conserved current]] called the **electric current** on $X$. Conversely, with $j_{el}$ prescribed this equation is one half of [[electromagnetic field|Maxwell's equations]] for $F$.


If $X$ is globally hyperbolic and $\Sigma \subset X$ is any spacelike hyperslice, then

$$
  Q_{el} := \int_\Sigma j_{el}
$$

is the [[charge]] of this current: the **electric charge**  encoded by this configuration of the [[electromagnetic field]].

Notice that due to the above equation $d j_{el} = 0$, so that $Q$ is independent of the choice of $\Sigma$. When unwrapped into separate space and time components, the expression $d j_{el} = 0$ may be expressed as

$$div j + \frac{\partial\rho}{\partial t} = 0$$

which is a statement of the physical phenomenon of _charge conservation_ .

## Remarks 

* While electric current is modeled by just a differential form, magnetic charge has a more subtle model. See [[magnetic charge]] .

* The above has a straightforward generalization to higher abelian [[gauge field]]s such as the [[Kalb-Ramond field]] and the [[supergravity C-field]]: for a field modeled by a degree $n$ [[Deligne cohomology|Deligne cocycle]] $\hat F$ the electric current $j_{el}$ is the right hand of
  $$
    d \star F = f_{el} \in \Omega^{n+1}(X)
    \,.
  $$

## Related concepts

* [[Gauss law]]

* [[hypercharge]]

* [[conserved current]], [[charge]]

* [[magnetic charge]]

* [[Ohm's law]]

* [[color charge]]

* [[flux]]

* [[dyon]]

* [[Hodge-Maxwell theorem]]

* [[higher electric background charge coupling]]


[[!redirects electric charges]]



[[!redirects electric current]]
[[!redirects electric currents]]

