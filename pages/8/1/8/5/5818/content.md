
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $V$ a [[vector space]], the **general linear Lie algebra** or **[[endomorphism Lie algebra]]** $\mathfrak{gl}(V)$ of $V$ is the [[Lie algebra]] whose elements are [[linear map|linear]] [[endomorphisms]] $V \to V$ and whose Lie bracket is given by the [[commutator]] of endomorphisms.

This is also the [[endomorphism L-∞ algebra]] of $V$

If $V$ is a real vector space that carries an [[inner product]] there are the sub-Lie algebras

$$
  \mathfrak{so}(V) \hookrightarrow \mathfrak{o}(V) \hookrightarrow \mathfrak{gl}(V)
$$

the 

* [[orthogonal Lie algebra]]

* and [[special orthogonal Lie algebra]].

If $V$ is a complex vector space with an inner product there is 

$$
  \mathfrak{so}(V) \hookrightarrow \mathfrak{o}(V) \hookrightarrow \mathfrak{gl}(V)
$$

the 

* [[unitary Lie algebra]]

* and [[special unitary Lie algebra]].


## Properties

### Loday-Quillen-Tsygan theorem

The _[[Loday-Quillen-Tsygan theorem]]_ ([Loday-Quillen 84](#LodayQuillen84), [Tsygan 83](#Tsygan83)) states that for any [[associative algebra]], $A$ in [[characteristic zero]], the [[Lie algebra homology]] $H_\bullet(\mathfrak{gl}(A))$  of the infinite [[general linear Lie algebra]] $\mathfrak{gl}(A)$ with [[coefficients]] in $A$ is, up to a degree shift, the [[exterior algebra]] $\wedge(HC_{\bullet - 1}(A))$ on the [[cyclic homology]] $HC_{\bullet - 1}(A)$ of $A$:

$$
  H_\bullet(\mathfrak{gl}(A))
  \;\simeq\;
  \wedge( HC_{\bullet - 1}(A) )
$$

(see e.g [Loday 07, theorem 1.1](#Loday07)).


## References

The [[Loday-Quillen-Tsygan theorem]] is originally due, independently, to

* {#LodayQuillen84} [[Jean-Louis Loday]], [[Daniel Quillen]], _Cyclic homology and the Lie algebra homology of matrices_ Comment. Math. Helv., 59(4):569–591, 1984.

and

* {#Tsygan83} [[Boris Tsygan]], _Homology of matrix algebras over rings and the Hochschild homology_, Uspeki Math. Nauk., 38:217–218, 1983.

Lecture notes include

* {#Loday07} [[Jean-Louis Loday]], _Cyclic Homology Theory, Part II_, notes taken by Pawe l Witkowsk (2007) ([pdf](https://www.impan.pl/swiat-matematyki/notatki-z-wyklado~/loday_cht_2.pdf))

[[!redirects general linear Lie algebras]]

