
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], **Coquand universes** or **universes à la Coquand** are an alternative to [[Russell universes]] and [[Tarski universes]] in presenting [[types]] and the hierarchy of [[type universes]]. Unlike type theories with Russell universes, which usually have either no separate type judgment, like that found in the *[[HoTT book]]*, or one type judgment, or type theories with Tarski universe, which are required to have one type judgment, type theories with Coquand universes have a type judgment for every universe in the type theory. 

## Formal definition

One formal definition of a type theory with Coquand universes is as follows:

The type theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $i \; \mathrm{index}$, that $i$ is a universe index, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are [[linearly ordered]] with strict order $\lt$ and upwardly unbounded, where $i \lt s(i)$ is true for all indices $i$. 

This allows us to add an infinite number of [[type]] [[judgments]], one type judgment $A \; \mathrm{type}_i$ for every index $i$, indicating that $A$ is a type with level $i$, as well as [[term]] judgments $a:A$. Then, one has the following [[inference rules]] for Coquand universes: 

$$\frac{\Gamma \vdash i \; \mathrm{index}}{\Gamma \vdash U_i \; \mathrm{type}_{s(i)}} \quad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{Lift}_i(A) \; \mathrm{type}_{s(i)}}$$

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{Code}(A):U_i} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{El}(B) \; \mathrm{type}_i}$$

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{El}_i(\mathrm{Code}_i(A)) \equiv A \; \mathrm{type}_i} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{Code}_i(\mathrm{El}(B)) \equiv B:U_i}$$

There are also weak versions of Coquand universes, where one uses [[identifications]] and [[equivalences of types]] instead of [[judgmental equality]]:

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \beta_{U_i}^A:\mathrm{El}_i(\mathrm{Code}_i(A)) \simeq A} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash B:U_i}{\Gamma \vdash \eta_{U_i}(B):\mathrm{Code}_i(\mathrm{El}(B)) =_{U_i} B}$$

The [[univalence axiom]] for Coquand universes states that for all $A:U_i$ and $B:U_i$, [[type transport|transport]] across $\mathrm{Lift}_i(\mathrm{El}_i(-))$ is an [[equivalence of types]]

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{ua}_{U_i}(A, B):\mathrm{isEquiv}(\mathrm{transport}_{x:U_i.\mathrm{Lift}_i(\mathrm{El}_i(x))}(A, B))}$$

## Related concepts

* [[type universe]]

  * [[Russell universe]]

  * [[Tarski universe]]

## References

Universes à la Coquand are described in section 2.1 of

* [[Daniel Gratzer]], [[G. Alex Kavvos]], [[Andreas Nuyts]], [[Lars Birkedal]]: _Multimodal Dependent Type Theory_, Logical Methods in Computer Science **17** 3 (2021) lmcs:7713 &lbrack;[arXiv:2011.15021](https://arxiv.org/abs/2011.15021), <a href="https://doi.org/10.46298/lmcs-17(3:11)2021">doi:10.46298/lmcs-17(3:11)2021</a>&rbrack;

[[!redirects Coquand universe]]
[[!redirects Coquand universes]]

[[!redirects à la Coquand]]

[[!redirects universe à la Coquand]]
[[!redirects universes à la Coquand]]


[[!redirects strict Coquand universe]]
[[!redirects strict Coquand universes]]

[[!redirects strictly à la Coquand]]

[[!redirects universe strictly à la Coquand]]
[[!redirects universes strictly à la Coquand]]

[[!redirects strict universe à la Coquand]]
[[!redirects strict universes à la Coquand]]


[[!redirects weak Coquand universe]]
[[!redirects weak Coquand universes]]

[[!redirects weakly à la Coquand]]

[[!redirects universe weakly à la Coquand]]
[[!redirects universes weakly à la Coquand]]

[[!redirects weak universe à la Coquand]]
[[!redirects weak universes à la Coquand]]