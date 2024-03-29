
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

For $p$ a [[prime number]], the _Fermat quotient_ of any [[integer]] $a$ is the quotient

$$
  \partial_p a \coloneqq
  \frac{a - a^p}{p}
$$

of the difference between the $p$th power of $a$ and $a$ itself by $p$. By [[Fermat's little theorem]] this is indeed an [[integer]], i.e. conversely one has for all $a\in \mathbb{Z}$ that

$$
  a^p = a + p (\partial_p a)
$$

for a uniquely defined integer $\partial_p a$.

(The $p$-power operation $(-)^p$ here is the one that restricts to the [[Frobenius homomorphism]] after [[p-localization]] and the one which is a shadow of the [[power operations]] in [[E-infinity arithmetic geometry]] ([Lurie, remark 2.2.7](#Lurie)).)

As the notation is meant to suggest, the Fermat quotient as a map $\mathbb{Z} \to \mathbb{Z}$ from the (underlying set of the) [[ring]] of [[integers]] to itself is [[analogy|analogous]] to a [[derivation]]. It is not quite an ordinary derivation, but satisfies conditions of what has been called a __$p$-[[p-derivation|derivation]].

In view of this, in the context of [[arithmetic differential equations]] the Fermat quotient is interpreted as an analog in [[arithmetic geometry]] of actual [[derivations]] in [[algebraic geometry]]/[[complex analytic geometry]]. For more on this see also at _[[Borger's absolute geometry]]_ the section _[Motivation](Borger's%20absolute%20geometry#Motivation)_.

## Related concepts

* [[p-derivation]]

* [[arithmetic differential equation]]

* [[Borger's absolute geometry]]

* [[arithmetic differential geometry]]

## References

* Wikipedia, _[Fermat quotient](http://en.wikipedia.org/wiki/Fermat_quotient)_

* {#Lurie} [[Jacob Lurie]], _[[Rational and p-adic Homotopy Theory]]_


[[!redirects Fermat quotients]]

