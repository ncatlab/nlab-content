
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

## Definition

In a [[finitely complete category]] $C$, a **cartesian monoidal preordered object** $X$ is a [[preordered object]] with internal preorder $R\stackrel{(s,t)}\hookrightarrow X \times X$ and a [[monoid object]] in $C$ with multiplication $(-)\wedge(-):X \times X \to X$ and a [[global element|global]] unit $\top:* \to X$, where $*$ is the [[terminal object]] in $C$, with

* a function $\tau:(* \to X) \to (* \to R)$ such that for all [[global elements]] $a:* \to X$, $s \circ \tau(a) = a$ and $t \circ \tau(a) = \top$. 

* functions 
$$\lambda_l:((* \to X) \times (* \to X)) \to (* \to R)$$ 
$$\lambda_r:((* \to X) \times (* \to X)) \to (* \to R)$$ 
such that for all [[global elements]] $a:* \to X$ and $b:* \to X$, $s \circ \lambda_l(a,b) = a \wedge b$, $t \circ \lambda_l(a,b) = a$, $s \circ \lambda_r(a,b) = a \wedge b$, and $t \circ \lambda_r(a,b) = b$. 

## See also

* [[preordered object]]

* [[monoid object]]

* [[cocartesian monoidal preordered object]]

* [[bicartesian preordered object]] 

* [[cartesian monoidal category]]

* [[meet-semilattice]]

[[!redirects cartesian monoidal preordered objects]]