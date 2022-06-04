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
{:toc}

## Idea 

The notion of *coexponential objects* is [[abstract duality|dual]] to that of *[[exponential objects]]*. 

## Definition 

Let $X$ and $Y$ be objects of a [[category]] $C$ such that all binary [[coproducts]] with $Y$ exist.  (Usually, $C$ actually has all binary coproducts.)  Then an __coexponential object__ is an object $Coexp(Y, X)$ equipped with a coevaluation map $\eta \colon X \to Coexp(Y, X) \coprod Y$ which is universal in the sense that, given any object $Z$ and map $e\colon X \to Z \coprod Y$, there exists a unique map $u\colon Coexp(Y, X) \to Z$ such that $e = (u, id_Y) \circ \eta$.

## See also

* [[cocartesian coclosed category]]

* [[locally cocartesian coclosed category]]

* [[exponential object]]

[[!redirects coexponential objects]]