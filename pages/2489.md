+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

The notion of _differential crossed module_ (or crossed module of/in [[Lie algebras]]) is a way to encode the structure of a [[strict Lie 2-algebra]] in terms of two ordinary [[Lie algebra]]s.


This is the [[infinitesimal object|infinitesimal]] version of how a smooth [[crossed module]] encodes a smooth [[strict 2-group]].


## Definition

### As crossed modules of Lie algebras

A **differential crossed module** $\mathfrak{g}$ is 

* a pair of [[Lie algebra]]s $\mathfrak{g}_0$ and $\mathfrak{g}_1$

* equipped with two Lie algebra homomorphisms

  * $\partial : \mathfrak{g}_1 \to \mathfrak{g}_0$

  * $ \rho : \mathfrak{g}_0 \to Der(\mathfrak{g}_1)$
  
    (to the [[Lie algebra]] of Lie [[derivation]]s)

* such that for all $x \in \mathfrak{g}_0, b,b' \in \mathfrak{g}_1$ we have

  * $\partial  ( \rho(x)(b) ) = [x, \partial(b)]$

  * $\rho(\partial b)(b') = [b, b']$.

Notice that the Lie algebra structure on $\mathfrak{g}_1$ is already fixed by the rest of the data. So a differential crossed module may equivalently be thought of as extra structure on a Lie module $\mathfrak{g}_1$ of $\mathfrak{g}_0$. This leads over to the following perspective.

### As dg-Lie algebras

Equivalently, a  differential crossed module is a [[dg-Lie algebra]] structure on a [[chain complex]] $(\mathfrak{g}_1 \stackrel{\partial}{\to} \mathfrak{g}_0)$ concentrated in degrees 0 and 1.

The components of the dg-Lie bracket are

* the given bracket $[-,-] : \mathfrak{g}_0 \otimes \mathfrak{g}_0 \to \mathfrak{g}_0$;

* the mixed bracket

  $$
    [-,-] : \mathfrak{g}_0 \otimes \mathfrak{g}_1 \to \mathfrak{g}_1
  $$

  identifies with the action:

  $$
    [x,b] := \rho(x)(b)
    \,.
  $$

This way the respect of the dg-bracket for the differential

$$
  \partial [x,b] = [\partial x, b ] + [x, \partial b] = [x,\partial b]
$$

is equivalently the above condition

$$
  \partial \rho(x)(b) = \rho(x)(\partial b)
  \,.
$$

### As strict Lie 2-algebras

By the discussion there, [[dg-Lie algebra]]s are _strict_ [[L-∞ algebra]]s (those for which all the brackets of higher arity vanish). Therefore the above identification of differential crossed modules with 2-term [[dg-Lie algebra]]s identifies these also with [[strict Lie 2-algebra]]s.

## Related concepts

* [[Lie algebra]], [[Lie group]]

* [[Lie 2-algebra]], [[Lie 2-group]]

* [[L-infinity algebra]], [[smooth ∞-group]]

* [[Lie algebroid]], [[Lie groupoid]]

* [[L-∞ algebroid]], [[smooth ∞-groupoid]]


## References

The [[crossed modules]] (in groups or Lie groups) and the differential crossed modules are examples of the [[internal crossed module]]s. A good theory of them is developed in [[semiabelian categories]]. 

* [[George Janelidze]], _Internal crossed modules_, Georgian Math. J. 10 (2003) 99114 ([journal](http://www.heldermann.de/GMJ/GMJ10/GMJ101/gmj1008.htm)).

[[!redirects differential crossed modules]]
[[!redirects crossed module in Lie algebras]]
[[!redirects Lie algebra crossed module]]