
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Curves
* table of contents
{: toc}

## In differential geometry

For $X$ a [[smooth manifold]], a (parametrized oriented) __smooth curve__ in $X$ is a [[smooth function]] $\gamma\colon \mathbb{R} \to X$ from the [[real line]] (or an [[interval]] therein) to $X$.  (Compare [[path]].)

For most purposes in [[differential geometry]] one needs to work with a __regular curve__, which is a parametrized smooth curve whose [[velocity]], i.e. the [[derivative]] with respect to the parameter, is never zero. For example, this is important if one wants to split curve into segments which have no self-intersections, which is important. 

In the foundations of [[differential topology]], it is possible to define a [[tangent vector]] as an equivalence class of smooth curves at a given point in the image of the curve, effectively identifying a curve with its derivative at (say) $0$.

See also the [[fundamental theorem of differential geometry of curves]].

### Open and closed curves

In a [[Cartesian space]] $\mathbb{R}^n$, an __open smooth curve__ is a smooth curve $\gamma:\mathbb{R} \to \mathbb{R}^n$ which does not intersect itself: For every real number $a \in \mathbb{R}$ and $b \in \mathbb{R}$, the [[distance]] between the two points on the curve parameterized by $a$ and $b$ is greater than zero: $\rho(\gamma(a),\gamma(b)) \gt 0$. Equivalently, an open smooth curve is a smooth curve such that the [[shape]] of the [[image]] of $\gamma$ is [[contractible]]: $\esh \mathrm{im}(\gamma) \simeq *$. 

A __closed smooth curve__ is a smooth curve $\gamma:\mathbb{R} \to \mathbb{R}^n$ which does intersect itself: for every real number $a \in \mathbb{R}$, there is a real number $b \in \mathbb{R}$, such that $\gamma(a) = \gamma(a + b)$. Equivalently, a closed smooth curve is a smooth curve such that the [[shape]] of the [[image]] of $\gamma$ is [[equivalent]] to the [[circle type]]: $\esh \mathrm{im}(\gamma) \simeq S^1$. 

In classical mathematics, every smooth curve $\gamma:\mathbb{R} \to \mathbb{R}^n$ is either open or closed. In [[constructive mathematics]], there are smooth curves where it cannot be proved to be either open or closed, due to the failure of [[trichotomy]]. 

## In algebraic geometry

In [[algebraic geometry]], an [[algebraic curve]] is a $1$-dimensional [[algebraic variety]] over a field.

An example: [[elliptic curve]].

## Related concepts

* [[surface]]

* [[differential geometry of curves and surfaces]]

* [[singular point of a curve]]

* [[torsion of a curve]]

* [[surface]], [[hypersurface]]

* [[velocity]], [[acceleration]], [[jerk]]

## References 

See also 

+ Wikipedia, _[Curve](https://en.wikipedia.org/wiki/Curve)_

[[!include infinitesimal and local - table]]

[[!redirects curve]]
[[!redirects curves]]

[[!redirects smooth curve]]
[[!redirects smooth curves]]

[[!redirects open curve]]
[[!redirects open curves]]

[[!redirects closed curve]]
[[!redirects closed curves]]