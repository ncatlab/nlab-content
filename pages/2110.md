
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _solution set condition_ appears as part of the hypothesis in Freyd's [[adjoint functor theorem|General Adjoint Functor Theorem]].


## Statement

A [[functor]] $F : C \to D$ satisfies the **solution set condition** if for every [[object]] $Y$ of $D$ there exists a [[small set]] $I$, an $I$-indexed family $(X_i)_{i \in I}$ of objects of $C$ and an $I$-indexed family $(f_i\colon Y \to F(X_i))_{i \in I}$ of morphisms in $D$ such that each morphism $h\colon Y \to F(X)$ in $D$ can be factored, for some index $i$ and some morphism $t\colon X_i \to X$ in $C$, as 

$$
  F(t) \circ f_i
  \colon
  Y \stackrel{f_i}{\to}
  F(X_i)
  \stackrel{F(t)}{\to}
  F(X).
$$

This is a smallness condition in that the family is required to be indexed by a [[small set]].

A restatement of this condition is that the comma categories $(Y \downarrow F)$ all admit weakly initial families of objects.

Here is the connection with the adjoint functor theorem: when small products exist in those comma categories, this is equivalent to saying that they all admit weakly initial objects. When small equalizers exist in those comma categories also, this is equivalent to saying that they all admit initial objects, and this is equivalent to $F$ being a right adjoint.


## Examples

* To define the [[projective tensor product]] of [[Banach spaces]] using the [[adjoint functor theorem]], let $C$ and $D$ each be [[Ban]] (the category of Banach spaces and [[short linear maps]]), fix a Banach space $B$, and let $F(X)$ be $BdLin(B,X)$, the Banach space of [[bounded linear maps]] from $B$ to $X$.

  If $f\colon X_1 \to X_2$ is a short linear map and $\phi\colon B \to X_1$ is a bounded linear map, then $BdLin(B,f)(\phi) \coloneqq f \circ \phi\colon B \to X_2$ is a bounded linear map with norm ${\|BdLin(B,f)(\phi)\|} \leq {\|f\|} {\|\phi\|}$, which proves that ${\|BdLin(B,f)\|} \leq {\|f\|} \leq 1$, so that $BdLin(B,f)$ is also a short map, as it must be for $F$ to be a functor.  (That $F$ is linear and preserves identities and composition is trivial.)

  The solution set condition now states:  For every Banach space $Y$ there exists a small set $I$, an $I$-indexed family $(X_i)_{i \in I}$ of Banach spaces and an $I$-indexed family $(f_i\colon Y \to BdLin(B,X_i))_{i \in I}$ of short linear maps such that each short linear map $h\colon Y \to BdLin(B,X)$ can be factored, for some index $i$ and some short linear map $t\colon X_i \to X$, as $h = BdLin(B,t) \circ f_i$.

  (to be completed)

## Related pages

The solution set condition weakens the notion of adjoint functor by allowing a family of objects rather than a single one, and also by removing the uniqueness of the factorization.  If we weaken the definition in only one of these ways, we obtain a [[multi-adjoint]] or a [[weak adjoint]] respectively.


[[!redirects solution set condition]]
[[!redirects solution set conditions]]
[[!redirects small solution set condition]]
[[!redirects small solution set conditions]]