
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _Lindenbaum number_ of a [[set]] $X$ is the smallest [[well-ordered set]] that is not a quotient of $X$ (as a bare set). It is a 'surjective analogue' of the [[Hartogs number]].

## Definition

Given a set $X$, denote by $\aleph^*(X)$ the set of [[ordinals]] $\alpha$ that admit a [[surjection]] $X\to \alpha$. Equivalently, it is the set of order isomorphism classes of well-orderings of quotients of $X$.

## Properties

By construction, if there were a surjection function $X \to \aleph^*(X)$, then $\aleph^*(X)$ would be order isomorphic to one of its own elements, and hence to a proper initial segment of itself, which is impossible.

If $\aleph(X)$ denotes the [[Hartogs number]] of $X$, then we also have:

* there is an injection $\aleph(X) \to \aleph^*(X)$

* for well-orderable $X$, then $\aleph(X) \simeq \aleph^*(X)$

* for non-well-orderable $X$, it's consistent that the gap can be arbitrarily large ([Karagila 2012, Section 1.2](#Karagila12)).

* there is an injection $\aleph^*(X) \to \aleph(P(X))$ ([Diener 1992](#Diener92)).



## Related entries

* [[Hartogs number]]
* [[successor]]
* [[diagonal argument]]

# References

The concept appeared as exercise 7.1.6 in 

* Karel Hrdacek and Thomas Jech, _Introduction to Set Theory_, 3rd Edition, Marcel Dekker (1999)

[Note: the exercise is also in chapter 8 in the 1984 2nd edition, not sure about the 1st edition]

And is mentioned in

* {#Diener92} Karl‐Heinz Diener, _On the transitive hull of a $\kappa$-narrow relation_, Math. Logic Quarterly, Volume 38, Issue1 (1992) pp 387-398, doi:[10.1002/malq.19920380137](https://doi.org/10.1002/malq.19920380137)

The name appears to be due to 

* Asaf Karagila, _Embedding Posets Into Cardinals With $DC_\kappa$_, arXiv:[1212.4396v1](https://arxiv.org/abs/1212.4396v1) (published as _Embedding Orders Into The Cardinals With $DC_\kappa$_ Fund. Math. 226 (2014), 143-156. and omitting the Lindenbaum number)

note: version 1 of the arXiv paper!

* {#Karagila12} Asaf Karagila, _Vector spaces and antichains of cardinals in models of set theory_, Master’s thesis, Ben-Gurion University of the Negev, 2012.