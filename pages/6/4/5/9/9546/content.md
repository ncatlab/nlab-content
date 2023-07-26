
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
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

[[K-theory]] as a [[generalized homology theory]].

In terms of [[KK-theory]], the $K$-homology of a [[C*-algebra]] $A$ is $KK(A,\mathbb{C})$.

## Presentations

There are various useful ways to present K-homology classes.

### By geometric cycles

See at _[[Baum-Douglas geometric cycle]]_.

### By Fredholm modules and Dirac operators

Let $(X,g)$ be a [[Riemannian manifold]]. Let 

$$
  C_\tau(X) \coloneqq \Gamma_0(\wedge^\bullet T^\ast X)
$$

be the algebra of continuous [[sections]] of the [[exterior bundle]] [[vanishing at infinity]], and let

$$
  \mathcal{H} \coloneqq L^2(\wedge^\bullet T^\ast X)
$$

be the space of [[square integrable function|square integrable]] [[sections]] of the [[exterior bundle]]. Write $\mathcal{D} = d + d^\ast$ for the [[Kähler-Dirac operator]] and $\mathcal{F} = \mathcal{D} (1 + \mathcal{D}^2)^{-1/2}$. Then $(\mathcal{H}, \mathcal{F})$ is a [[Fredholm module|Fredholm]]-[[Hilbert module]] which hence represents an element

$$
  [d_X + d^\ast_X] \in KK(C_\tau(X), \mathbb{C})
  \,.
$$ 

Now assume that $X$ carries a [[spin^c structure]]. Then there exists a [[vector bundle]] $S \to X$ such that $C_\tau(X) = End(S)$ and hence a [[Morita equivalence]] $C_\tau(X) \simeq_{Morita} C_0(X)$ with the algebra of [[continuous functions]] [[vanishing at infinity]].

Let then 

$$
  H \coloneqq L^2(S)
$$

and write $D$ for the [[Spin^c Dirac operator]] and $F \coloneqq D (1+ D^2)^{-1/2}$. 

Then under the above Morita equivalence these two [[Fredholm module|Fredholm]]-[[Hilbert modules]] represent the same element in K-homology

$$
  [d_X + d^\ast_X] = [D] \in KK(C_0(X), \mathbb{C})
  \,.
$$

## Related concepts

* [[K-cohomology]]

* [[Baum-Douglas geometric cycles]]

## References

The "geometric model" of K-homology (cf. *[[Baum-Douglas geometric cycle]]*) is due to:

* [[Paul Baum]], R. Douglas, *K-homology and index theory*, in: R. Kadison (ed.), *Operator Algebras and Applications, Proceedings of Symposia in Pure Math. **38** AMS (1982) 117-173 &lbrack;[ams:pspum-38-1](https://bookstore.ams.org/pspum-38-1)&rbrack;

* [[Paul Baum]], R. Douglas. _Index theory, bordism, and K-homology_, Contemp. Math. **10** (1982) 1-31

Analytic formulation via [[KK-theory]]:

* {#KK} [[Gennady Kasparov]], _Equivariant KK-theory and the Novikov conjecture_, Inventiones Mathematicae, **91** (1988) 147 &lbrack;[doi:10.1007/BF01404917](https://doi.org/10.1007/BF01404917), [web](http://adsabs.harvard.edu/abs/1988InMat..91..147K)&rbrack;


An expository account of the analytic model:

* [[Nigel Higson]], [[John Roe]], _Analytic K-homology_, Oxford Mathematical Monographs. Oxford University Press, Oxford (2000) &lbrack;[ISBN: 9780198511762](https://global.oup.com/academic/product/analytic-k-homology-9780198511762?cc=nl&lang=en&)&rbrack;

Twisted K-homology:

* [[Christopher Douglas]], _On the Twisted K-Homology of Simple Lie Groups_, Topology 45 (2006), 955-988 ([arXiv:math/0402082](https://arxiv.org/abs/math/0402082))

[[!redirects K-homology theory]]
