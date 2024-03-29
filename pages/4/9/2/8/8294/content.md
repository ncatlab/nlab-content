
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

An _equation_ is a [[proposition]] of [[equality]].

For 

$$
  x : X \vdash \phi(x) : Z
$$ 

and 

$$
  y : Y \vdash \psi(y) : Z
$$

two [[terms]] of some [[type]] $Z$ [[dependent type|dependent]] on [[variables]] $x$ of type $X$ and $y$ of type $Y$, respectively, the equation asserting that these two formulas are [[equality|equal]] is as a [[proposition]] the [[bracket type]] 

$$
 x : X, y : Y \vdash [\phi(x) = \psi(y)] : Type
$$

and as a not-neccessarily [[(-1)-truncated object|(-1)-truncated]] type just the [[identity type]]

$$
 x : X, y : Y \vdash (\phi(x) = \psi(y)) : Type
$$

itself.

The **space of [[solutions]]** of this equation is the [[dependent sum]] over all pairs of terms for which [[equality]] holds

$$
  \vdash \sum_{{x : X} \atop {y : Y}} (\phi(x) = \psi(y)) : Type
  \,.
$$

Hence a particular **[[solution]]** $sol$ is a [[term]] of this type

$$
  \vdash sol : \sum_{{x : X} \atop {y : Y}} (\phi(x) = \psi(y))
  \,,
$$

which means that it is a triple consisting of an $x \in X$, a $y \in Y$ and a witness $eq : (\phi(x) = \psi(y))$ that these indeed solve the equation.

In [[categorical semantics]] this means that the space of solutions to an equation between expression $\phi(x) : Z$ and $\psi(y) : Z$ of [[type]] $Z$ depending on [[variables]] of type $X$ and $Y$, respectively is the  [[pullback]]

$$
  \array{
    \sum_{{x : X} \atop {y : Y}} (\phi(x) = \psi(y))
    &\to& Y
    \\
    \downarrow && \downarrow^{\mathrlap{\psi}}
    \\
    X &\stackrel{\phi}{\to}& Z
  }
  \,,
$$

the [[fiber product]] of $\phi$ with $\psi$. In the context of [[homotopy type theory]] this is the [[homotopy pullback]]/[[homotopy fiber product]].

See at _[homotopy pullback -- concrete constructions -- In homotopy type theory](http://ncatlab.org/nlab/show/homotopy+pullback#ConstructionInHomotopyTypeTheory)_ for more on this.


## Examples

* [[linear equation]]

* [[algebraic equation]]

* [[Diophantine equation]]

* [[trigonometric identity]]

* [[differential equation]]

* [[Euler-Lagrange equation]], [[equation of motion]]

* [[master equation]]

* [[equation of state]]

[[!redirects equations]]