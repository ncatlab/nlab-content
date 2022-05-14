
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

In a [[finitely complete category]] $C$, a **cocartesian monoidal preordered object** $X$ is a [[preordered object]] with internal preorder $R\stackrel{(s,t)}\hookrightarrow X \times X$ and a [[monoid object]] in $C$ with multiplication $(-)\vee(-):X \times X \to X$ and a [[global element|global]] unit $\bot:* \to X$, where $*$ is the [[terminal object]] in $C$, with

* a function $\beta:(* \to X) \to (* \to R)$ such that for all [[global elements]] $a:* \to X$, $s \circ \beta(a) = \bot$ and $t \circ \beta(a) = a$. 

* functions 
$$\kappa_l:((* \to X) \times (* \to X)) \to (* \to R)$$ 
$$\kappa_r:((* \to X) \times (* \to X)) \to (* \to R)$$ 
such that for all [[global elements]] $a:* \to X$ and $b:* \to X$, $s \circ \kappa_l(a,b) = a$, $t \circ \kappa_l(a,b) = a \vee b$, $s \circ \kappa_r(a,b) = b$, and $t \circ \kappa_r(a,b) = a \vee b$. 

## See also

* [[preordered object]]

* [[monoid object]]

* [[cartesian monoidal preordered object]]

* [[bicartesian preordered object]] 

* [[join-semilattice object]]

* [[cocartesian monoidal category]]

[[!redirects cocartesian monoidal preordered objects]]