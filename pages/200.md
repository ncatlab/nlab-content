
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

_Ring_ is the [[category]] of [[rings]] (with [[unital ring|unit]]) and ring [[homomorphisms]] (that preserve the unit).

A _ring_ is a [[monoid]] [[internalization|in]] [[Ab]], where $Ab$ is the category of [[abelian group|abelian groups]].  So, $Ring$ is an example of a category of [[internal monoids]].

## Properties

### Epi/Monomorphisms


For more see at [[Stacks Project]], _[10.106 Epimorphisms of rings](http://stacks.math.columbia.edu/tag/04VM)_.

Every [[surjective function|surjective]] [[homomorphism]] of rings is an [[epimorphism]] in $Ring$, but not every epimorphism is surjective. 

A counterexample:

\begin{proposition}
  \label{InclusionOfIntegersIntoRationalsIsEpimorphismOfRings}
  
In [[unital ring|unital]] [[Rings]], the canonical inclusion $\mathbb{Z} \overset{i}{\hookrightarrow} \mathbb{Q}$ of the [[integers]] into the [[rational numbers]] is an [[epimorphism]].

\end{proposition}

\begin{proof}

Since every [[rational number]] is the product of an [[integer]] with the multiplicative inverse of an integer

$$
  \frac{a}{b} \,=\,  a \cdot b^{-1}
  \;\;
  \in
  \;
  \mathbb{Q}
$$

and since [[unital ring|unital]] [[ring homomorphism]]

$$
  \mathbb{Z}
  \overset{\;\; i \;\;}{\hookrightarrow}
  \mathbb{Q}
  \underoverset
  {\;\;g\;\;}
  {\;\;f\;\;}
  {\rightrightarrows}
  R
  \,.
$$ 

preserve multiplicative inverses, $f\left( a/b \right) = f(a) \cdot \big(f(b)\big)^{-1}$, it follows that any pair $(f,g)$ of [[parallel morphisms]] on $\mathbb{Q}$ are equal as soon as they take equal value on the integers.

\end{proof}


## Related categories

* [[Mod]]

* [[CRing]]

* [[Rng]]

* [[Mon]], [[CMon]]

## References

* [[Stacks Project]], _[10.106 Epimorphisms of rings](http://stacks.math.columbia.edu/tag/04VM)_

[[!redirects category of rings]]

[[!redirects Rings]]

category: category