+-- {: .num_defn}
###### Definition
A monad in [[Haskell]] is defined to be a type class with two methods:

> $\mathbf{class}\;Monad\;m\;\mathbf{where}$

> $\gt\gt =::ma\to(a\to mb)\to mb$

> $return::a\to ma$

such that

> $x\gt\gt=f\equiv fx$

> $a\gt\gt=return\equiv a$

> $(a\gt\gt=f)\gt\gt=g\equiv a\gt\gt =(\lambda x\to fx\gt\gt =g)$

=--

+-- {: .num_remark}
###### Remark
$m$ being a [[monad]] $(m:a\to a, \mu:m^2\to m,\epsilon:id_a\to m)$ on some object $a$ in a [[2-category]] can be expressed in [[Haskell]] by

> $\mathbf{class}\;Monad\;m\;\mathbf{where}$

> $map::(a\to b)\to ma\to mb$

> $return::a\to ma$

> $join:: m(ma)\to ma$

We have the following translation of Haskell and [[category theory, language and library specification|category theoretical language]]:

> $join:=\mu$

> $return :=\epsilon$

Then from the category theoretical properties of $(m,\mu,\epsilon)$ we obtain (mixing the two languages)

> $map\; g\circ \epsilon\equiv \epsilon\circ g$

> $map \; \circ \mu\equiv \mu\circ map(map\; g)$

> $\mu\circ map\; \mu \equiv \mu\circ \mu$

> $\mu\circ \epsilon\equiv \mu\circ map\;\epsilon =id$


And with the following definitions

> $map\; f :=(\lambda\to a\gt\gt=(return\circ f))$

> $ join \; a=a\gt\gt id$

or alternatively

> $a\gt\gt =f:=join (map\;fa)$

one can verify that the two given definitions of a monad are equivalent.
=--

## References

category theory/monads, haskellwiki, [wiki](http://www.haskell.org/haskellwiki/Category_theory/Monads)
