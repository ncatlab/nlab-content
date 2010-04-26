The **solution set condition** appears as part of the hypothesis in Freyd's [[adjoint functor theorem|General Adjoint Functor Theorem]] and can be stated as follows:

A [[functor]] $F : C \to D$ satsifies the condition if for every object $Y$ of $D$ there exists a [[small set]] $I$ and an $I$-indexed family of morphisms $\{f_i : Y \to F(X_i)\}_{i \in I}$ such that any morphism $h : Y \to F(X)$ can be factored as 

$$
  F(t) \circ f_i
  : 
  Y \stackrel{f_i}{\to}
  F(X_i)
  \stackrel{F(t)}{\to}
  F(X)
$$ 

for some $t : X_i \to X$ and some $i$.

This is a smallness condition in that the family is required to be indexed by a set.