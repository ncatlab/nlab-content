
#Contents#
* table of contents
{:toc}

## Idea

A _Hecke correspondence_ is a certain [[correspondence]] between a [[moduli stacks of bundles]]. The [[integral transform]] induced by a [[Hecke correspondence]] is called a _Hecke transform_. The objects preserves by such a transform up to a tensor multiple are called [[Hecke eigensheaves]].

These are central objects of interest in [[geometric Langlands duality]].

## For modular curves

The reference for this is section 1.4 of [Calegari13](#Calegari13).


Let $X_{0}(p)$ be the moduli space of pairs $(E,E')$ where $E$ and $E'$ are $p$-isogenous elliptic curves. This has maps $\pi_{1}$ and $\pi_{2}$ to the moduli space of elliptic curves $X$, sending $(E,E')$ to $E$ and $E'$ respectively:

$$
  \array{
     && X_{0}(p)     \\
     & {}_{\mathllap{\pi_{1}}}\swarrow && \searrow_{\mathrlap{\pi_{2}}}
     \\
     X && && X
  }
$$

We can think of the Hecke correspondence as the multivalued function $\pi_{2 *}\circ\pi_{1}^{*}$. Although this is a multivalued function, upon linearizing (by, say, passing to [[modular forms]] i.e. global sections of the sheaf $\omega^{k}$) we get a legitimate function

$$pT_{p}:H^{0}(X(\Gamma),\omega^{k})\to H^{0}(X(\Gamma),\omega^{k})$$

where $T_{p}$ is the $p$-th _Hecke operator_.

Alternatively, we can embed $X_{0}(p)$ inside $X\times X$ as the graph of the above-mentioned multivalued function. In this way it is more properly seen as a correspondence.

## For moduli stacks of bundles

A reference for this is section 3.7 of [Frenkel05](#Frenkel05). A discussion can also be found in [Lafforgue18](#Lafforgue18).

Hecke correspondences for moduli stacks of bundles follow roughly the same idea but instead of $X$ we have $Bun_{G}$ and instead of $X_{0}$ we have the Hecke stack $Hck$, which parametrizes pairs of bundles $\mathcal{E}_{1}$, $\mathcal{E}_{2}$ together with a _modification_ which is an isomorphism between $\mathcal{E}_{1}$ and $\mathcal{E}_{2}$ away from some points:

$$
  \array{
     && Hck     \\
     & {}_{\mathllap{\pi_{1}}}\swarrow && \searrow_{\mathrlap{\pi_{2}}}
     \\
     Bun_{G} && && Bun_{G}
  }
$$

## Properties

### Relation to S-duality in super Yang-Mills theory

[[!include geometric Langlands QFT -- table]]

## Related concepts

* [[modular form]]

* [[Hecke algebra]]

* [[Hecke eigensheaf]]

* [[Hecke category]]

## References

* {#Frenkel05} [[Edward Frenkel]], section 3.7 in _Lectures on the Langlands Program and Conformal Field Theory_ ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))

* {#Calegari13} Frank Calegari, _Congruences between modular forms_, 2013 [pdf](https://swc-math.github.io/aws/2013/2013CalegariLectureNotes.pdf)

* {#Lafforgue18} [[Vincent Lafforgue]], _Shtukas for reductive groups and Langlands correspondence for function fields_, [arXiv:1803.03791](https://arxiv.org/abs/1803.03791)

[[!redirects Hecke correspondences]]

[[!redirects Hecke transformation]]
[[!redirects Hecke transformations]]


[[!redirects Hecke transform]]
[[!redirects Hecke transforms]]
