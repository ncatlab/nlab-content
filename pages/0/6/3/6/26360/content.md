
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Set truncation is an operation in [[type theory]] which turns a [[type]] into an [[h-set]]. 

## Definition

### With propositional truncations and quotient sets

Suppose that the [[dependent type theory]] has [[propositional truncations]] and [[quotient sets]]. Then given a type $T$, the [[type family]] $R(x, y)$ indexed by $x:T$ and $y:T$ defined by the [[propositional truncation]] of the [[identity type]] of $T$, $R(x, y) \equiv [\mathrm{Id}_T(x, y)]_{-1}$ is an [[equivalence relation]]. The **set truncation** of $T$ is the quotient set of $T$ by $R$: $[T]_0 \equiv T / R$. 

### With localizations and the circle type

Suppose that [[dependent type theory]] has [[localization of a type|localizations of types]] and the [[circle type]] $S^1$. Then the **set truncation** of a type $T$ is the localization of $T$ at $S^1$: $[T]_0 \equiv L_{S^1}(T)$

### As a higher inductive type

to be done; for the time being see section 6.9 of the [[HoTT Book]]. 

## Related concepts

* [[propositional truncation]], [[quotient set]]

* [[localization of a type]], [[circle type]]

* [[axiom of set truncation]]

* [[n-truncation modality]]

## References

For set truncations in [[dependent type theory]], see section 18.5 of:

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects set truncation]]
[[!redirects set truncations]]

[[!redirects set-truncation]]
[[!redirects set-truncations]]