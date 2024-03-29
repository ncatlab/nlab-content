
> This entry is about operators in the sense of [[higher-order logic]], which is the original sense and which has only that name.  For operators in the sense of [[functional analysis]], see _[[linear operator]]_.  For the relation between these, see under Examples [below](#Examples). For yet other kinds of operators see at _[[operation]]_.


# Operators
* table of contents
{: toc}




## Definition

In a [[type theory]] with [[function types]], given a [[type]] $X$, an __operator__ of base type $X$ is a [[term]] of type $(X^X)^{X^X}$ aka $(X \to X) \to (X \to X)$.  This should be distinguished from a [[functional]], which is a term of type $X^{X^X}$ aka $(X \to X) \to X$, and a [[endofunction|function]], which (in this context) is a term of type $X^X$ aka $X \to X$.

More generally, any term whose type has the form $(A^B)^{C^D}$ aka $(D \to C) \to (B \to A)$ may be called an operator, although usually not if any of these types is very trivial (since any type has this form, up to equivalence, if $B,C,D \coloneqq 1$).

Although one typically interprets type theory within [[set theory]] so that operations between types become [[functions]], one may also use [[partial functions]], which is necessary for the connection to [[linear operators]] in [[functional analysis]].

An operator could also be interpreted within [[category theory]] as a [[globe|globular]] [[2-morphism]] in the [[2-category|2-]][[category of sets]]. 

## Examples
 {#Examples}

The [[Church numeral]]s are operators in the (possibly typed) [[lambda-calculus]]:

* $0 \coloneqq (f \mapsto (x \mapsto x))$,
* $1 \coloneqq (f \mapsto (x \mapsto f x))$,
* $2 \coloneqq (f \mapsto (x \mapsto f f x))$,
* etc.


If we interpret $X$ as the [[real line]], then $X^X$ consists of real-valued maps of a real variable, which form a [[vector space]].  The [[partial function|partially defined]] [[linear maps]] from $X^X$ to itself are the original [[linear operators]].  In [[functional analysis]], we now replace $X^X$ with an arbitrary [[topological vector space]] $V$ (originally but no longer necessarily taken to be a [subspace](subspace#vector_subspaces) of $X^X$) and consider partial linear maps from $V$ to itself instead; so these linear operators are actually functions (meaning [[endofunctions]]) in a type-theoretic sense.  In [[operator theory]], we go further and replace $V^V$ with an arbitrary [[operator algebra]] (originally but no longer necessarily taken to be a [[subalgebra]] of $V^V$); so these operators are unstructured terms in a type-theoretic sense.


A [[differential operator]] is a good example of something that is both an operator in the logical sense (since it turns functions into functions) and a linear operator in the sense of functional analysis (since [[differentiable functions]] form a vector space and [[differentiation]] acts linearly).

## Related concepts

* [[operator product]]

[[!redirects operator]]
[[!redirects operators]]
