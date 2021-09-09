##Idea

In general, in the [[idempotent semiring]] $(max,+)$, an equation of form $Ax=b$ has no solution, but the inequality $Ax\leq b$ does by taking $x=\mathbb{0}$.  (Here recall that in any idmepotent semiring, there is a natural partial order on the elements.)  It is natural to relax equality in the search for somultions, and study instead the set of its 'subsolutions'.  One way forward in this approach is to use the notion of [[residuated mapping]] from the theory of [[posets]].

## Definition

An idempotent semiring, $S$ is residuated if the right and left multiplication maps

$$\lambda_a:x\mapsto ax$$

and

 $$\rho_a:x\mapsto xa$$

from $S$ to itself are [[residuated mapping|residuated]].

## Example

Any complete idempotent semiring is automatically residuated.  We set

$a \backslash b:= \lambda^\#_a (b) = max \{x \mid ax \leq b\}$

and 

$b / a:= \rho_a^\# (b) = max \{ x \mid xa \leq b\}.$

In the completed $(max,+)$ semiring, $\overline{\mathbb{R}}_{max}$, $a\backslash b$ and $b/a$ are equal and both equal $b-a$, provided that $a\neq \mathbb{0}$, in which case they equal $+\infty$.

##References

* [[Stéphane Gaubert]], _Methods and Applications of $(max,+)$ Linear Algebra,_ [Report 3088](https://hal.inria.fr/inria-00073603/document), January 1997, INRIA.

