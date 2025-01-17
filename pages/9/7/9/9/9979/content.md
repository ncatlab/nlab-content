
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

An **irreflexive symmetric relation** or sometimes **inequality relation** is a [[binary relation]] that is [[irreflexive relation|irreflexive]] and [[symmetric relation|symmetric]]. 

## Examples

* Every [[apartness relation]] is an irreflexive symmetric relation which is also a [[comparison]]. 

* The negation of a [[reflexive symmetric relation]] is an irreflexive symmetric relation. 

* Every [[denial inequality]] is a [[weakly tight relation|weakly tight]] irreflexive symmetric relation. 

## In constructive mathematics
 {#ConstructiveMathematics}

In constructive mathematics, not ever tight irreflexive symmetric relation is a denial inequality, and not every denial inequality is tight. Instead, every [[denial inequality]] is only [[weakly tight]]. Indeed, since excluded middle cannot be proven, we could distinguish between the following irreflexive symmetric relations in constructive mathematics:

* [[denial inequality]], an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg(a = b)$ implies $(a \neq b)$

* [[tight]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg(a \neq b)$ implies $(a = b)$

* [[weakly tight relation|weakly tight]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg(a \neq b)$ implies $\neg \neg (a = b)$

* [[stable relation|stable]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg \neg (a \neq b)$ implies $(a \neq b)$

* [[decidable relation|decidable]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $(a \neq b)$ or $\neg (a \neq b)$

* [[apartness relation]], an irreflexive symmetric relation $\neq$ which additionally satisfies $a \neq b$ implies that $a \neq c$ or $c \neq b$

or any combination of the above, such as [[tight apartness relation]]. 

The notion of "[[inequality relation]]" in constructive mathematics usually refers to either the [[denial inequality]] or a [[tight apartness relation]]. On the other hand, some authors have used "inequality relation" to refer to general irreflexive symmetric relations. 

### Irreflexive symmetric relations and equality of sets

In [[classical mathematics]], every set $S$ comes with an irreflexive symmetric relation $\neq$ such that for all $x$ and $y$ in $S$, $x = y$ [[disjunction|or]] $x \neq y$. 

However, in constructive mathematics, the usual classical notion of [[disjunction]] bifurcates into multiple notions which are not equivalent to each other. Here is a Hasse diagram of some of them, applied to the equality and irreflexive symmetric relation, with the strongest statement at the bottom and the weakest at the top (so that each statement entails those above it):

$$ \array {           &          & \neg(\neg(x = y) \wedge \neg(x \neq y)) \\
                      & &#x21d7; &          & &#x21d6; \\
\neg(x = y) \rightarrow x \neq y &          &          &          & x = y \leftarrow \neg(x \neq y) \\
                      & &#x21d6; &          & &#x21d7; \\
                      &          & (\neg(x = y) \rightarrow x \neq y) \wedge (x = y \leftarrow \neg(x \neq y)) \\
                      &          & \Uparrow \\
                      &          & x = y \vee x \neq y } $$

## Related concepts

* [[apartness relation]]
* [[inequality relation]]
* [[reflexive symmetric relation]]
* [[antithesis partial order]]
* [[antithesis interpretation]]
* [[inequality ring]]
* [[affine set]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects irreflexive symmetric relation]]
[[!redirects irreflexive symmetric relations]]

[[!redirects tight irreflexive symmetric relation]]
[[!redirects tight irreflexive symmetric relations]]

[[!redirects weakly tight irreflexive symmetric relation]]
[[!redirects weakly tight irreflexive symmetric relations]]

[[!redirects stable irreflexive symmetric relation]]
[[!redirects stable irreflexive symmetric relations]]

[[!redirects decidable irreflexive symmetric relation]]
[[!redirects decidable irreflexive symmetric relations]]

[[!redirects weak inequality]]
[[!redirects weak inequalities]]
[[!redirects weak inequality structure]]
[[!redirects weak inequality structures]]
[[!redirects weak inequality relation]]
[[!redirects weak inequality relations]]

[[!redirects strict inequality]]
[[!redirects strict inequalities]]
[[!redirects strict inequality structure]]
[[!redirects strict inequality structures]]
[[!redirects strict inequality relation]]
[[!redirects strict inequality relations]]

[[!redirects stable inequality]]
[[!redirects stable inequalities]]
[[!redirects stable inequality structure]]
[[!redirects stable inequality structures]]
[[!redirects stable inequality relation]]
[[!redirects stable inequality relations]]

[[!redirects decidable inequality]]
[[!redirects decidable inequalities]]
[[!redirects decidable inequality structure]]
[[!redirects decidable inequality structures]]
[[!redirects decidable inequality relation]]
[[!redirects decidable inequality relations]]
