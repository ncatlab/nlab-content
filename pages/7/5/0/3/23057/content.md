\tableofcontents

## Idea

In general, in the [[additively idempotent semiring|idempotent semiring]] $(max,+)$, an equation of form $A x = b$ has no solution, but the [[inequality]] $A x \leq b$ does by taking $x=\mathbb{0}$.  (Here recall that in any idempotent semiring, there is a natural [[partial order]] on its elements.)  It is natural to relax [[equality]] in the search for solutions, and study instead the set of its 'subsolutions'. One way forward in this approach is to use the notion of [[residuated mapping]] from the theory of [[posets]].

## Definition

An idempotent semiring, $S$ is *residuated* if the right and left multiplication maps

$$
  \lambda_a \colon x\mapsto a x
$$

and

$$
  \rho_a \colon x\mapsto x a
$$

from $S$ to itself are [[residuated mapping|residuated]].

## Example

Any complete idempotent semiring is automatically residuated.  We set

$
  a \backslash b 
  \coloneqq 
  \lambda^\#_a (b) 
  = 
  max \{x \mid a x \leq b\}
$

and 

$
  b / a
  \coloneqq 
  \rho_a^\# (b) 
  = 
  max \{ x \mid x a \leq b\}
  \,.
$

In the completed $(max,+)$ semiring, $\overline{\mathbb{R}}_{max}$, $a\backslash b$ and $b/a$ are equal and both equal $b-a$, provided that $a\neq \mathbb{0}$, in which case they equal $+\infty$.

## References

* [[Stéphane Gaubert]], _Methods and Applications of $(max,+)$ Linear Algebra,_ [Report 3088](https://hal.inria.fr/inria-00073603/document), January 1997, INRIA.


[[!redirects residuated idempotent semirings]]
