+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The [[quotient]] of a [[ring]] by an [[ideal]].

## Definition

### Quotient by two-sided ideals

Given a [[ring]] $R$ and a [[two-sided ideal]] $I$ with canonical $R$-$R$-[[bimodule monomorphism]] $i:I \hookrightarrow R$, the quotient of $R$ by $I$ is the [[initial object|initial]] two-sided $R$-[[associative unital algebra|algebra]] $R/I$ with canonical [[ring homomorphism]] $h:R \to R/I$ such that for every element $a \in I$, $h(i(a)) = 0$: for any other $R$-algebra $S$ with canonical ring homomorphism $k:R \to S$ such that for every element $a \in I$, $k(i(a)) = 0_S$, there is a unique ring homomorphism $l:R/I \to S$ such that $l \circ h = k$. 

### Quotient by left ideals

Given a [[ring]] $R$ and a [[left ideal]] $I$ with canonical left $R$-[[module]] [[monomorphism]] $i:I \hookrightarrow R$, the quotient of $R$ by $I$ is the [[initial object|initial]] left $R$-[[associative unital algebra|algebra]] $R/I$ with canonical [[ring homomorphism]] $h:R \to R/I$ such that for every element $a \in I$, $h(i(a)) = 0$: for any other $R$-algebra $S$ with canonical ring homomorphism $k:R \to S$ such that for every element $a \in I$, $k(i(a)) = 0_S$, there is a unique ring homomorphism $l:R/I \to S$ such that $l \circ h = k$. 

### Quotient by right ideals

Given a [[ring]] $R$ and a [[right ideal]] $I$ with canonical right $R$-[[module]] [[monomorphism]] $i:I \hookrightarrow R$, the quotient of $R$ by $I$ is the [[initial object|initial]] right $R$-[[associative unital algebra|algebra]] $R/I$ with canonical [[ring homomorphism]] $h:R \to R/I$ such that for every element $a \in I$, $h(i(a)) = 0$: for any other $R$-algebra $S$ with canonical ring homomorphism $k:R \to S$ such that for every element $a \in I$, $k(i(a)) = 0_S$, there is a unique ring homomorphism $l:R/I \to S$ such that $l \circ h = k$. 

## Related concepts

* [[associative unital algebra]]

* [[quotient group]]

* [[quotient module]]

* [[quotient bimodule]]

* [[localization of a ring]]

* [[completion of a ring]]

* [[Koszul complex]]

## References

See also

* Wikipedia, _[Quotient ring](https://en.wikipedia.org/wiki/Quotient_ring)_

[[!redirects quotient rings]]

[[!redirects quotient algebra]]
[[!redirects quotient algebras]]
