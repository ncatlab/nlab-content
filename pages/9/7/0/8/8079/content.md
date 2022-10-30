
# Preduals
* table of contents
{: toc}

## Idea

In any context in which one speaks of [[duals]], $x$ is a __predual__ of $a$ if $a$ is the dual of $x$.  If there is more than one sort of dual (left and right, algebraic and topological, etc), then the same goes for preduals. 

The term is most commonly encountered when "dual" is meant in the sense of [[dual object in a closed category]]. In particular, it is common parlance in the context of [[Banach spaces]]; see also the discussion below on von Neumann algebras.


## Definitions

The Idea section above gives a fine definition, except for the word 'is' in the phrase '$x$ is the dual of $a$'. One ought to say: given an [[object]] $a$, a __predual__ of $a$ is an object $x$ and an [[isomorphism]] $i\colon a \to x^*$, where $x^*$ is the dual (whatever that means in the appropriate context) of $x$.  (Or if the objects in question form some kind of [[higher category]], then $i$ is an [[equivalence]].)

Similarly, given a [[morphism]] $f\colon a \to b$ and isomorphisms $i\colon x^* \to a$ and $j\colon y^* \to b$, a __predual__ of $f$ (relative these preduals of $a$ and $b$) is a morphism $u\colon y \to x$ making this [[commutative diagram]] (or in a higher category, with a $2$-equivalence filling it):
$$ \array {
   x^*                  & \overset{i}\to  & a \\
   \llap{u^*}\downarrow &                 & \rlap{f}\downarrow \\
   y^*                  & \underset{j}\to & b
   } $$
(We may continue to preduals of $2$-morphisms etc, if appropriate.)

One can, of course, apply the term "predual" to any of the contexts of "dual" listed in [[category with duals]] (before the examples of [[star-autonomous category]] and [[closed category]], which were said not to really belong). But this is less commonly encountered in practice, since it reduces to a concept with some other standard name, e.g., a left predual of an object is the same as its right dual.


## Of von Neumann algebras

Preduals are particularly studied for [[von Neumann algebras]].  Indeed, a von Neumann algebra may be defined as a $C^*$-[[C-star-algebra|algebra]] with a predual of its underlying [[Banach space]].  We have the nice theorem that this predual is essentially unique, so we speak of [[the]] predual of a von Neumann algebra.  Similarly, a [[morphism]] of von Neumann algebras is a morphism of $C^*$-algebras with a predual (relative to the algebras\' unique preduals) of its underlying morphism of Banach spaces; this is again unique.

Since the preduals are unique, we may give them symbols; if the dual of $A$ is denoted $A^*$, then we use $A_*$ for the predual of $A$.  (If one uses a different symbol for duals, then preduals follow that.)


[[!redirects predual]]
[[!redirects preduals]]
