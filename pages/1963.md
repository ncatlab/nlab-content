A __derivation__ on an [[nonassociative algebra|algebra]] $A$ is a module homomorphism $d: A \to A$ such that
$$ d(a b) = d(a) b + a d(b) .$$
This identity is called the __Lebiniz rule__; compare it to the product rule in ordinary calculus (first written down by [[Gottfried Leibniz]]).

A __graded derivation__ of degree $p$ on a [[graded object|graded]] algebra $A$ is a degree-$p$ graded-module homomorphism $d: A \to A$ such that
$$ d(a b) = d(a) b + (-1)^{pq} a d(b) $$
whenever $a$ is homogeneous of degree $q$.  (By default, the grade is usually $1$, or sometimes $-1$.)

An __augmented derivation__ on an algebra $A$, augmented by an algebra homomorphism $\epsilon: A \to B$, is a module homomorphism $d: A \to B$ such that
$$ d(a b) = d(a) \epsilon(b) + \epsilon(a) d(b) .$$

If you think about it, you should be able to figure out the definition of an __augmented graded derivation__.

There are many further extensions, for examples derivations with values in an $A$-[[bimodule]] $M$ forming $Der_k(A,M) \subset Hom_k(A,M)$ (see also [[double derivation]]), skew-derivations in ring theory (with a twist in the Leibniz rule given by an endomorphism of a ring) and the dual notion of a [[coderivation]] of a coalgebra.  The latter plays role in Koszul-dual definitions of $A_\infty$-[[A-infinity-algebra|algebras]] and $L_\infty$-[[L-infinity-algebra|algebras]]. 


## Examples

*  Let $A$ consist of the smooth real-valued functions on an [[interval]] in the [[real line]].  Then differentiation is a derivation; this is the motivating example.
*  Let $A$ consist of the [[holomorphic function]]s on a region in the [[complex plane]].  Then differentiation is a derivation again.
*  Let $A$ consist of the [[meromorphic function]]s on a region in the [[complex plane]].  Then differentiation is still a derivation.
*  Let $A$ consist of the smooth functions on a [[manifold]] (or [[generalized smooth space]]) $X$.  Then any [[tangent vector field]] on $X$ defines a derivation on $A$; indeed, this serves as one definition of tangent vector field.
*  Let $A$ consist of the [[germ]]s of differentiable functions near a point $p$ in a smooth space $X$.  Then any [[tangent vector]] at $a$ on $X$ defines a derivation on $A$ augmented by evaluation at $a$; again, this serves to define tangent vectors.
*  Let $A$ consist of the smooth [[differential form]]s on a smooth space $X$.  Then [[exterior differentiation]] is a (degree-$1$) graded derivation.
*  In any of the above example containing the adjective 'smooth', replace it with $C^k$ and augment $A$ by the inclusion of $C^k$ into $C^{k-1}$.  Then we have an augmented derivation.


[[!redirects derivations]]
[[!redirects Leibniz rule]]
[[!redirects Leibniz identity]]