
#Contents#
* automatic table of contents goes here
{:toc}


## Definitions


### Derivations on an algebra

For $A$ an [[nonassociative algebra|algebra]] (over some [[ring]] $k$), a **derivation** on $A$ is a $k$-linear morphism

$$
  d : A \to A
$$

such that for all $a,b \in A$ we have

$$ 
  d(a b) = d(a) b + a d (b) 
  \,,
$$

This identity is called the __Leibniz rule__; compare it to the product rule in ordinary calculus (first written down by [[Gottfried Leibniz]]).


### Derivations with values in a bimodule

For $A$ an [[nonassociative algebra|algebra]] (over some [[ring]] $k$) and $N$ a [[bimodule]] over $A$, a **derivation** of $A$ with values in $N$ is a $k$-linear morphism

$$
  d : A \to N
$$

such that for all $a,b \in A$ we have

$$ 
  d(a b) = d(a) \cdot b + a \cdot d (b) 
  \,,
$$

where on the dot on the right-hand side denotes the right (first term) and left (second term) [[action]] of $A$ on the bimodule $N$. 

The previous definition is a special case of this one, where the bimodule is $N = A$, the algebra itself with its canonical left and right action on itself.


### Graded derivations

A __graded derivation__ of degree $p$ on a [[graded object|graded]] algebra $A$ is a degree-$p$ graded-module homomorphism $d: A \to A$ such that
$$ d(a b) = d(a) b + (-1)^{pq} a d(b) $$
whenever $a$ is homogeneous of degree $q$.  (By default, the grade is usually $1$, or sometimes $-1$.)


### Augmented derivations

An __augmented derivation__ on an algebra $A$, augmented by an algebra homomorphism $\epsilon: A \to B$, is a module homomorphism $d: A \to B$ such that
$$ d(a b) = d(a) \epsilon(b) + \epsilon(a) d(b) .$$

If you think about it, you should be able to figure out the definition of an __augmented graded derivation__.


### Further variations

There are many further extensions, for examples derivations with values in an $A$-[[bimodule]] $M$ forming $Der_k(A,M) \subset Hom_k(A,M)$ (see also [[double derivation]]), skew-derivations in ring theory (with a twist in the Leibniz rule given by an endomorphism of a ring) and the dual notion of a [[coderivation]] of a coalgebra.  The latter plays role in Koszul-dual definitions of $A_\infty$-[[A-infinity-algebra|algebras]] and $L_\infty$-[[L-infinity-algebra|algebras]].  See also [[derivation on a group]], which uses a modified Leibniz rule: $d(a b) = d(a) + a d(b)$.


## Examples


### Derivations on an algebra

*  Let $A$ consist of the smooth real-valued functions on an [[interval]] in the [[real line]].  Then differentiation is a derivation; this is the motivating example.
*  Let $A$ consist of the [[holomorphic function]]s on a region in the [[complex plane]].  Then differentiation is a derivation again.
*  Let $A$ consist of the [[meromorphic function]]s on a region in the [[complex plane]].  Then differentiation is still a derivation.
*  Let $A$ consist of the smooth functions on a [[manifold]] (or [[generalized smooth space]]) $X$.  Then any [[tangent vector field]] on $X$ defines a derivation on $A$; indeed, this serves as one definition of tangent vector field.
*  Let $A$ consist of the [[germ]]s of differentiable functions near a point $p$ in a smooth space $X$.  Then any [[tangent vector]] at $a$ on $X$ defines a derivation on $A$ augmented by evaluation at $a$; again, this serves to define tangent vectors.
*  Let $A$ consist of the smooth [[differential form]]s on a smooth space $X$.  Then [[exterior differentiation]] is a graded derivation (of degree $1$).
*  In any of the above examples containing the adjective 'smooth', replace it with $C^k$ and augment $A$ by the inclusion of $C^k$ into $C^{k-1}$.  Then we have an augmented derivation.

There should be some more clearly algebraic examples (other than obvious things like restricting the above to polynomials), but I don\'t know how to state them.


### Derivations with values in a bimodule

The standard example of a derivation not on an algebra, but with values in a [[bimodule]] is a restriction of the above case of the exterior differential acting on the [[deRham complex|deRham algebra]] of differential forms. Restricting this to 0-fomrs yields a morphism

$$
  d : C^\infty(X) \to \Omega^1(X)
$$ 

where $\Omega^1(X)$ is the space of 1-forms on $X$, regarded as a bimodule over the algebra of functions in the obvious way. 

A variation of this example is given by the [[Kähler differential]]s. These provide a **universal derivation** in some sense.


[[!redirects derivations]]
[[!redirects Leibniz rule]]
[[!redirects Leibniz identity]]