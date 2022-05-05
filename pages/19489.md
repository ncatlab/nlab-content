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

$E$ is a **trifibration** if both $E \to B$ and $E^{d} \to B$ are [[bifibrations]], where the category $E^{d}$, fibered over $B$, is the [[dual fibration]] obtained by changing the direction of all the vertical arrows in $E$. The arrows of $E^{d}$ are the equivalence classes of spans with a vertical arrow pointing at the source, and a cartesian arrow pointing at the target ([Pavlovic90, p. 315](#Pavlovic90)).

A fibration $E \to B$ is a bifibration if and only if for every $t: I \to J$ in $B$, the [[inverse image functor]]  $t^{\ast}: E_{J} \to E_{I}$ has a [[left adjoint]] $t_{!}: E_{I} \to E_{J}$. It is a trifibration if and only if there is also a [[right adjoint]] $t_{\ast}: E_{I} \to E_{J}$.

Since a trifibration is _not_ a fibration in three ways as its name suggests, alternative terminology has been used, including $\ast$-bifibration in ([FBMF](#FBMF)).

## References

* {#Pavlovic90} [[Dusko Pavlovic|Duško Pavlović]], _Categorical Interpolation: Descent and the Beck-Chevalley Condition without Direct Images_ , pp.306-325  in _Category theory Como 1990_, LNM **1488** Springer Heidelberg 1991. ([pdf](http://www.isg.rhul.ac.uk/dusko/papers/1990-BCDE-Como.pdf))

* {#FBMF} [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, Theory and Applications of Categories, Vol. 20, No. 18, 2008, pp.  650–738, ([tac](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))