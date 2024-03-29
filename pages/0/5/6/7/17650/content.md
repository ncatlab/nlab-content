+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[formal dual]] to the [[pushout product]] (frequently considered in the context of [[enriched model category]] theory) does not have a widely established name, but plausibly deserves to be called the _pullback powering_ operation. Note that it sometimes called _pullback hom_.

More precisely, a pushout product is defined with respect to a functor of the form $E_1\times E_2 \to E_3$, while a pullback power is defined with respect to a functor of the form $E_2^{op} \times E_3\to E_1$ or $E_1^{op}\times E_3 \to E_2$, of the sort that would be the right adjoints in a [[two-variable adjunction]].

Pullback powers and pushout products are related to [[factorization systems]] by the [[Joyal-Tierney calculus]].


## Definition

Let $\mathcal{C}$ be [[category]] with [[finite limits]] and let


$$
  [-,-]
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
  \longrightarrow
   \mathcal{C}
$$

a [[functor]] (out of the [[product category]] of the [[opposite category]] of $\mathcal{C}$ with $\mathcal{C}$ itself). Then for 

$$
  g \;\colon\; X \to Y
$$

and

$$
  f \;\colon\; A \to B
$$

two [[morphisms]] in $\mathcal{C}$, their _pullback powering_ $g^f$ is the morphism

$$
   [B,X] \stackrel{[i , p]}{\to} [A,X] \times_{[A,Y]} [B,Y]
$$ 

into the evident [[fiber product]] on the right.

## Related concepts

* [[pullback power axiom]]

* [[powering]]

* [[Joyal-Tierney calculus]]

* [[enriched model category]]

[[!redirects pullback-power]]
[[!redirects pullback-powers]]


[[!redirects pullback powering]]
[[!redirects pullback powerings]]

[[!redirects pullback-powering]]
[[!redirects pullback-powerings]]

[[!redirects pullback powers]]

[[!redirects Leibniz cotensor]]

[[!redirects pullback hom]]
[[!redirects pullback-hom]]