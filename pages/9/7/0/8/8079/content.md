
# Preduals
* table of contents
{: toc}

## Idea

In any context in which one speaks of [[duals]], $x$ is a __predual__ of $a$ if $a$ is the dual of $x$.  If there is more than one sort of dual (left and right, algebraic and topological, etc), then the same goes for preduals.


## Definitions

The paragraph above is a fine definition, except for the word 'is' in the phrase '$b$ is the dual of $a$'.  Most generally, we may consider an $(\infty,n)$-[[(infinity,n)-category with duals|category with duals]] $C$.  This includes the case of a [[category with duals]], which includes the well-known duals of [[vector spaces]], [[Banach spaces]], etc.

Given an [[object]] $a$, a __predual__ of $a$ is an object $x$ and an [[equivalence]] (which is an [[isomorphism]] if $C$ is a category) $i\colon x^* \to a$, where $x^*$ is the dual of $x$.

Given a [[morphism]] $f\colon a \to b$ and equivalences $i\colon x^* \to a$ and $j\colon y^* \to b$, a __predual__ of $f$ (relative these preduals of $a$ and $b$) is a morphism $u\colon y \to x$ and a $2$-equivalence (which is an [[equality]] if $C$ is a category) filling this diagram:
$$ \array {
   x^*                  & \overset{i}\to  & a \\
   \llap{u^*}\downarrow &                 & \rlap{f}\downarrow \\
   y^*                  & \underset{j}\to & b
   } $$

We may continue to preduals of $2$-morphisms etc.


## Of von Neumann algebras

Preduals are particularly studied for [[von Neumann algebras]].  Indeed, a von Neumann algebra may be defined as a $C^*$-[[C-star-algebra|algebra]] with a predual of its underlying [[Banach space]].  We have the nice theorem that this predual is essentially unique, so we speak of [[the]] predual of a von Neumann algebra.  Similarly, a [[morphism]] of von Neumann algebras is a morphism of $C^*$-algebras with a predual (relative to the algebras\' unique preduals) of its underlying morphism of Banach spaces; this is again unique.

Since the preduals are unique, we may give them symbols; if the dual of $A$ is denoted $A^*$, then we use $A_*$ for the predual of $A$.  (If one uses a different symbol for duals, then preduals follow that.)


[[!redirects predual]]
[[!redirects preduals]]
