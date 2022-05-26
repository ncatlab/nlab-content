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

The [[quotient]] of a [[bimodule]] by an [[subbimodule]].

## Definition

Given [[rings]] $R$ and $S$, a $R$-$S$-bimodule $B$, and an sub-$R$-$S$-bimodule $I$ with a $R$-$S$-[[bimodule monomorphism]] $i:I \hookrightarrow B$, the quotient of $B$ by $I$ is the [[initial object|initial]] $R$-$S$-bimodule $B/I$ with canonical $R$-$S$-[[bimodule homomorphism]] $h:B \to B/I$ such that for every element $a \in I$, $h(i(a)) = 0$: for any other $R$-$S$-[[bimodule]] $A$ with canonical $R$-$S$-bimodule homomorphism $k:B \to A$ such that for every element $a \in I$, $k(i(a)) = 0_A$, there is a $R$-$S$-bimodule homomorphism $l:B/I \to A$ such that $l \circ h = k$. 

## Related concepts

* [[quotient group]]

* [[quotient module]]

* [[quotient ring]]

[[!redirects quotient bimodules]]
