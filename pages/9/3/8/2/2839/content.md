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

## Ideas

In [[algebraic topology]] and [[homotopy theory]], a **cocylinder** is a dual construction to a [[cylinder]].  In contexts where spatial intuition is involved, it is perhaps more often called a [[path space]]  $X^I$ or a [[path space object]]. In general, however, a cocylinder, $X^I$, may not involve any object $I$ nor use a mapping space in its construction, see [[cylinder functor]] for the discussion of the dual point.

## Definition (cocylinders and cocylinder functors)

These are the duals of [[cylinders]] and [[cylinder functors]] so can safely be left as an exercise.

## Ideas continued
 
Similarly, the **mapping cocylinder**, which is dual to the [[mapping cylinder]], is equally called the **mapping path space** or **mapping path fibration**.  It provides a canonical way to factor any map as a [[homotopy equivalence]] followed by a [[fibration]].


## Definition (mapping cocylinders)

### In category theory

For a [[topological space]] $X$, its **cocylinder** is simply the path space $X^{[0,1]}$.  More generally, in a [[cartesian closed category]] with an [[interval object]] $I$, the **cocylinder** of an object $X$ is the [[exponential object]] $X^I$.  Even more generally, in a [[model category]] the **cocylinder** of any object is the [[path space object]] --- the factorization of the [[diagonal morphism]] $X\to X\times X$ as an [[acyclic cofibration]] followed by a [[fibration]].

In any of these cases: 

+-- {: .num_defn }
###### Definition

Given a [[morphism]] $f\colon X\to Y$, its **mapping cocylinder** (or **mapping path space** or **mapping path fibration**) is the [[pullback]]
$$
 \array{
   Cocyl(f)&\to& X\\
    \downarrow&&\downarrow f \\
    Y^I&\stackrel{ev_0}{\to}&Y
    \\
    \downarrow^{\mathrlap{ev_1}}
    \\
    Y
 }$$
where $Y^I$ is the cocylinder. 

=--

The mapping cocylinder is sometimes denoted $M_f Y$ or $N f$.

+-- {: .num_remark }
###### Remark

If we interchange $ev_0$ and $ev_1$ then we have an upside-down version of a cylinder, sometimes called inverse (or inverted) mapping cocylinder; but usually it is clear just from the context which version is used.  They are homotopy equivalent, so usually it does not matter.

=--

### In type theory

In [[homotopy type theory]] the mapping cocylinder $Cocyl(f) \to Y$ is expressed as

$$
  y : Y \vdash \sum_{x  \in X} (f(x) = y)
$$

being the [[dependent sum]] over $x$ of the [[substitution]] of $f(x)$ for $y_1$ in the [[dependent type|dependent]] [[identity type]] $(y_1 = y)$. Equivalently this is the $y$-[[dependent type|dependent]] [[homotopy fiber]] of $f$ at $y$

$$
  y : Y \vdash hfiber(f,y)
  \,.
$$

## Examples

* In the case of [[topological spaces]], the mapping cocylinder is the subspace $Cocyl(f)\subset Y^I\times X$ whose elements are pairs $(s,x)$ such that $s(0)=f(x)$.

* In [[homotopy type theory]], cocylinders represent [[identity types]], and the mapping cocylinder represents the [[dependent type]] $y\colon Y \vdash hfiber(f,y)\colon Type$.  This is used crucially in the definition of [[equivalence in homotopy type theory]].

## Applications

* The mapping cocylinder is the central ingredient in the [[factorization lemma]].

* One usage is discussed at _[[Hurewicz connection]]_.

* The mapping path fibration is used in the construction of the [[Strøm model structure]] on topological spaces.

* The [[homotopy fiber]] can be constructed as the strict [[fiber]] of the mapping cocylinder.


## Related concepts

[[!include universal constructions of topological spaces -- table]]


## References

* [[George Whitehead]],  _Elements of homotopy theory_ 

Peter May's books use the terminology *mapping path space*.

[[!redirects cocylinder]]
[[!redirects cocylinders]]
[[!redirects mapping cocylinder]]
[[!redirects mapping cocylinders]]
[[!redirects mapping path space]]
[[!redirects mapping path spaces]]
[[!redirects mapping path fibration]]
[[!redirects mapping path fibrations]]
