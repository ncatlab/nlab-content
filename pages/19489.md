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

$E$ is a **trifibration** if both $E \to B$ and $E^{op} \to B$ are [[bifibrations]], where the category $E^{op}$, fibered over $B$, is obtained by changing the direction of all the vertical arrows in $E$. The arrows of $E^{op}$ are the equivalence classes of spans with a vertical arrow (i.e., those above an identity morphism in $B$) pointing at the source, and a cartesian arrow pointing at the target ([Pavlovic90, p. 315](#Pavlovic90)).

A fibration $E \to B$ is a bifibration if and only if for every $t: I \to J$ in $B$, the [[inverse image functor]]  $t^{\ast}: E_{J} \to E_{I}$ has a [[left adjoint]] $t^{!}: E_{I} \to E_{J}$. It is a trifibration if and only if there is also a [[right adjoint]] $t_{\ast}: E_{I} \to E_{J}$.

## References

* {#Pavlovic90} [[Dusko Pavlovic|Duško Pavlović]], _Categorical Interpolation: Descent and the Beck-Chevalley Condition without Direct Images_ , pp.306-325  in _Category theory Como 1990_, LNM **1488** Springer Heidelberg 1991. ([pdf](http://www.isg.rhul.ac.uk/dusko/papers/1990-BCDE-Como.pdf))