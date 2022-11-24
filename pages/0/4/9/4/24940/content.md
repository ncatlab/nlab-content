# Contents
* table of contents
{: toc}

## Idea

A _p-adic modular form_ is a limit of [[modular forms]] under a topology that encodes congruences between its Fourier coefficients.

## Definition

The original definition is due to Serre. Consider the space of [[modular forms]] over $\mathbb{Q}$, and recall that they are fully determined by their q-expansions, therefore we may write them as [[power series]] $f=\sum_{n=0}^{\infty}{a_{n}}q^{n}\in\mathbb{Q}[[q]]$. Since $\mathbb{Q}$ embeds into the [[p-adic numbers ]] $\mathbb{Q}_{p}$, we may consider these modular forms as elements of $\mathbb{Q}_{p}[[q]]$ as well. We define a [[valuation]] $v_{p}$ on this space by

$$v_{p}(f):=\inf_{n}( v_{p}(a_{n}))$$

where the $v_{p}$ on the right-hand side is the p-adic valuation on $\mathbb{Q}_{p}$ with $v_{p}(p)=1$.

A _p-adic modular form_ is a power series $f=\sum_{n=0}^{\infty}{a_{n}}q^{n}\in\mathbb{Q}_{p}[[q]]$ such that there exists a sequence of modular forms $f_{1},f_{2},\ldots$ with $f_{i}\to f$.

Another different definition was later formulated by Katz.

## Related concepts

* [[modular form]]

* [[eigenvariety]]

## References

* {#Calegari13} Frank Calegari, _Congruences Between Modular Forms_, 2013 ([pdf](https://swc-math.github.io/aws/2013/2013CalegariLectureNotes.pdf))

* {#Eischen21} Ellen Eischen, _An Introduction to Eisenstein Measures_, 2021 ([arxiv:2101.01879](https://arxiv.org/abs/2101.01879))