+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Cocylinders and mapping cocylinders
* table of contents
{: toc}

## Idea

In [[algebraic topology]] and [[homotopy theory]], a **cocylinder** is a dual construction to a [[cylinder]].  However, it is more commonly called a [[path space]]  $X^I$ or a [[path object]].

Similarly, the **mapping cocylinder**, which is dual to the [[mapping cylinder]], is equally called the **mapping path space** or **mapping path fibration**.  It provides a canonical way to factor any map as a [[homotopy equivalence]] followed by a [[fibration]].

## Definition

For a [[topological space]] $X$, its **cocylinder** is simply the path space $X^{[0,1]}$.  More generally, in a [[cartesian closed category]] with an [[interval object]] $I$, the **cocylinder** of an object $X$ is the [[exponential object]] $X^I$.  Even more generally, in a [[model category]] the **cocylinder** of any object is the [[path object]] --- the factorization of the [[diagonal morphism]] $X\to X\times X$ as an [[acyclic cofibration]] followed by a [[fibration]].

In any of these cases, given a [[morphism]] $f\colon X\to Y$, its **mapping cocylinder** (or **mapping path space** or **mapping path fibration**) is the [[pullback]]
$$\array{
Cocyl(f)&\to& X\\
\downarrow&&\downarrow f \\
Y^I&\stackrel{ev_0}{\to}&Y
}$$
where $Y^I$ is the cocylinder.  The mapping cocylinder is sometimes denoted $M_f Y$ or $N f$.

## Examples

* In the case of [[topological spaces]], the mapping cocylinder is the subspace $Cocyl(f)\subset Y^I\times X$ whose elements are pairs $(s,x)$ such that $s(0)=f(x)$.

* In [[homotopy type theory]], cocylinders represent [[identity types]], and the mapping cocylinder represents the [[dependent type]] $y\colon Y \vdash hfiber(f,y)\colon Type$.  This is used crucially in the definition of [[equivalence in homotopy type theory]].

## Applications

* For a usage see [[Hurewicz connection]].

* In Brown's theory of [[higher stack]]s via categories of fibred objects, mapping cocylinders take a role of total spaces of a relative version of [[universal bundle|universal principal bundles]] associated to a map $f$; the projection of such a bundle is the composition $Cocyl(f)\to Y^I\stackrel{ev_1}\to Y$.  Note that the other leg $ev_1$ is used here. 

* The mapping path fibration is used in the construction of the [[Strøm model structure]] on topological spaces.

* The [[homotopy fiber]] can be constructed as the strict [[fiber]] of the mapping cocylinder.

## Remarks

* If we interchange $ev_0$ and $ev_1$ then we have an upside-down version of a cylinder, sometimes called inverse (or inverted) mapping cocylinder; but usually it is clear just from the context which version is used.  They are homotopy equivalent, so usually it does not matter.

## References

* George Whitehead in his old book "Elements of homotopy theory" uses the terminology *mapping path space*.

[[!redirects cocylinder]]
[[!redirects cocylinders]]
[[!redirects mapping cocylinder]]
[[!redirects mapping cocylinders]]
[[!redirects mapping path space]]
[[!redirects mapping path spaces]]
[[!redirects mapping path fibration]]
[[!redirects mapping path fibrations]]
