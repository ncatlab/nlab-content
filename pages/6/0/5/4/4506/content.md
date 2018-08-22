

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Dual to [[Lie algebra cohomology]]. See there for more.

## Definition 

The abelian [[homology]] of a $k$-[[Lie algebra]] $\mathfrak{g}$ with coefficients in the left $\mathfrak{g}$-module $M$ is defined as $H_*^{Lie}(\mathfrak{g},M) = Tor^{U\mathfrak{g}}_*(k,M)$ where $k$ is the ground field understood as a trivial module over the universal enveloping algebra $U\mathfrak{g}$. In particular it is a [[derived functor]]. It can be computed using [[Chevalley-Eilenberg chain complex]] $V(\mathfrak{g})$ as the homology of the chain complex

$$ M \otimes_{U\mathfrak{g}} V(\mathfrak{g}) = M\otimes_{U\mathfrak{g}} U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g} = M\otimes_k \Lambda^* \mathfrak{g}. $$

## Properties

### Loday-Quillen-Tsygan theorem


The _[[Loday-Quillen-Tsygan theorem]]_ ([Loday-Quillen 84](#LodayQuillen84), [Tsygan 83](#Tsygan83)) states that for any [[associative algebra]], $A$ in [[characteristic zero]], the [[Lie algebra homology]] $H_\bullet(\mathfrak{gl}(A))$  of the infinite [[general linear Lie algebra]] $\mathfrak{gl}(A)$ with [[coefficients]] in $A$ is, up to a degree shift, the [[exterior algebra]] $\wedge(HC_{\bullet - 1}(A))$ on the [[cyclic homology]] $HC_{\bullet - 1}(A)$ of $A$:

$$
  H_\bullet(\mathfrak{gl}(A))
  \;\simeq\;
  \wedge( HC_{\bullet - 1}(A) )
$$

(see e.g [Loday 07, theorem 1.1](#Loday07)).


Lecture notes include

* {#Loday07} [[Jean-Louis Loday]], _Cyclic Homology Theory, Part II_, notes taken by Paweł Witkowski (2007) ([pdf](https://www.impan.pl/swiat-matematyki/notatki-z-wyklado~/loday_cht_2.pdf))


## References

* C. Chevalley, S. Eilenberg, _Cohomology theory of Lie groups and Lie algebras_, Trans. Amer. Math. Soc. 63, (1948). 85&#8211;124.


The [[Loday-Quillen-Tsygan theorem]] is originally due, independently, to

* {#LodayQuillen84} [[Jean-Louis Loday]], [[Daniel Quillen]], _Cyclic homology and the Lie algebra homology of matrices_ Comment. Math. Helv., 59(4):569–591, 1984.

and

* {#Tsygan83} [[Boris Tsygan]], _Homology of matrix algebras over rings and the Hochschild homology_, Uspeki Math. Nauk., 38:217–218, 1983.
