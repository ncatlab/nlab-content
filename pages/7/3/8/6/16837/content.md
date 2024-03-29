## Definition

There is a [[Waldhausen S-construction]] $w_\bullet S_\bullet C$ for [[stable (infinity,1)-categories]].
One defines the [[algebraic K-theory]] of $C$ as
  $$ K(C) = \Omega | w_\bullet S_\bullet C | $$
in the usual way.

## Properties

There is a universal characterization of the construction of the K-theory spectrum $K(A)$ of a stable $(\infty,1)$-category $A$:

there is an $(\infty,1)$-functor

$$
  U : (\infty,1)StabCat \to N
$$

to a stable $(\infty,1)$-category which is universal with the property that it respects [[filtered colimits]] and exact sequences in a suitable way. Given any stable $(\infty,1)$-category $A$, its (connective or non-connective, depending on details) algebraic K-theory spectrum is the hom-object

$$
  K(A) \simeq Hom(U(Sp), U(A))
  \,,
$$

where $Sp$ denotes the stable $(\infty,1)$-category of compact [[spectra]]. 

See ([Blumberg-Gepner-Tabuada 10](#BlumbergGepnerTabuada10)).

## References

* {#BlumbergGepnerTabuada10} [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282)).

[[!redirects K-theory of a stable (infinity,1)-category]]
[[!redirects K-theory of a stable infinity-category]]