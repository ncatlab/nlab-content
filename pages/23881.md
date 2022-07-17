
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of a *bicartesian closed preordered object* or *Heyting prealgebra object* is the generalization of that of *[[bicartesian closed preordered set]]* or *[[Heyting prealgebra]]* as one passes from the ambient [[category of sets]] [[internalization|into]] more general ambient  [[categories]] with suitable properties.

## Definition

In a [[finitely complete category]] $C$, a **bicartesian closed preordered object** or **Heyting prealgebra object** is a [[bicartesian preordered object]] 
$$(X, R, s, t, \rho, \tau_p \wedge, \top, \tau, \lambda_l, \lambda_r, \vee, \bot, \beta, \kappa_l, \kappa_r)$$ 
with a morphism $(-)\Rightarrow(-):X \times X \to X$ and functions
$$\epsilon_l:((* \to X) \times (* \to X)) \to (* \to R)$$ 
$$\epsilon_r:((* \to X) \times (* \to X)) \to (* \to R)$$ 
such that for all global elements $a:* \to X$ and $b:* \to X$, 

* $s \circ \epsilon_l(a, b) = (a \Rightarrow b) \wedge a$
* $t \circ \epsilon_l(a, b) = b$ 
* $s \circ \epsilon_r(a, b) = a$ 
* $t \circ \epsilon_r(a, b) = b \Rightarrow (a \wedge b)$

## See also 

* [[Heyting prealgebra]]

* [[bicartesian preordered object]]

* [[bicartesian closed category]]

* [[Boolean prealgebra object]]

* [[Heyting algebra object]]

[[!redirects bicartesian closed preordered objects]]
[[!redirects Heyting prealgebra object]]
[[!redirects Heyting prealgebra objects]]