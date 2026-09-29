
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

\tableofcontents

## Idea

A weak first-order [[theory]] of [[arithmetic]], *Presburger arithmetic* is notable for being [[decidable]] and thus is most commonly used to define the universe levels of the [[universe hierarchy]] in [[dependent type theories]] such as used in the [[proof assistants]] [[Rocq]] or [[Lean]]. 

However, because Presburger arithmetic is not a [[second-order logic|second-order]] theory, it admits non-standard models; the [[natural numbers]] are only the [[initial object|initial]] model of Presburger arithmetic. 

## Axioms

The language of Presburger arithmetic consists of a binary operation $ +\colon N \times N \to N$ and constants $0,1\in N$.

1. $\neg(0=x+1)$
2. $x+1=y+1 \to x=y$
3. $x+0=x$
4. $x+(y+1)=(x+y)+1$
5. Let $P(x)$ be a first-order formula in the language of Presburger arithmetic where $x$ is among the free variables in $P$. Then:
$$
(P(0) \wedge \forall x(P(x) \to P(x+1))) \to \forall y\, P(y).
$$

The last item is an axiom scheme, one axiom per formula $P$.

## Related concepts

* [[Peano arithmetic]]

* [[Heyting arithmetic]]

## References

* Wikipedia, *[Presburger arithmetic](https://en.wikipedia.org/wiki/Presburger_arithmetic)*