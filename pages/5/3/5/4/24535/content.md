## Idea

While a [[ring]] is a set with two operations, (Abelian) group with respect to one and semigroup with respect to another with a standard two-sided distributivity law, there are also interesting examples of a "brace-like" distributivity law instead. Truss is a formalization/generalization of the usage of the alternative distributivity which uses a [[heap]] as a weakening of a concept of a group. Trusses appear in a number of subjects including the study of solutions to [[quantum Yang-Baxter equation]], ideal ring extensions, [[Hopf-Galois extension]]s, [[inverse semigroup]]s etc. 

If we drop Abelianess of the "additive" group then we talk about a more general notion of a skew truss (which is therefore to [[near-ring]] roughly what a truss is to a ring).

## Definition

A __left truss__ is a [[heap]] $(A,[.,.,.])$ together with another "multiplicative" operation which distributes with the ternary operation of the heap from the left
$$
a\cdot [b,c,d] = [a\cdot b,a\cdot c,a\cdot d]
$$
A [[truss]] is a left and right truss.

A left truss is a __left [[brace]]__ if it is Abelian group under the multiplicative operation. 

Alternatively, we can use the binary operations only, together with some sort of a cocycle (measuring nonstandardness of distributive law). So let $(A,+)$ be a group (though additive, not necessarily commutative!) and $(A,\cdot)$ a [[semigroup]].
As usually, consider the associated heap operation of $(A,+)$, 
$$
[b,c,d] = b - c + d
$$
(where $-$ means adding, in this order, the additive inverse).
Then the following are equivalent:

1. $(A,[.,.,.])$ is a truss 

2. $\exists \sigma: A\to A$ such that $a\cdot(b+c) = (a\cdot b)-\sigma(a)+(a\cdot c)$

3. $\exists\lambda : A\times A\to SA$ such that
$a\cdot(b+c) = (a\cdot b) + \lambda(a,c)$

4. $\exists\mu : A\times A\to SA$ such that
$a\cdot(b+c) = \mu(a,b)+(a\cdot c)$

5. $\exists\kappa,\tilde\kappa$ such that $a\cdot(b+c) = \kappa(a,b)+\tilde\kappa(a,c)$


## Examples

* All even numbers form a (nonunital) subring of the ring of integers. Another coset, the class $2\mathbb{Z}+1$ of all odd numbers is closed under multiplication, but not under addition. However, if we introduce the new addition $a\oplus b = a - 1 + b$ then
$2\mathbb{Z}+1$ is closed under both operation and the brace-like distributive law holds $a\cdot(b \oplus c) = a\cdot b \ominus a \oplus a\cdot c$. 

## Properties

## Literature

* [[Tomasz Brzeziński]], _Trusses: Between braces and rings_, Trans. Amer. Math. Soc. __372__ (2019), 4149-4176 [doi](https://doi.org/10.1090/tran/7705); preprint  [pdf](https://core.ac.uk/download/pdf/187088098.pdf)

* T. Brzeziński, _Enter truss_, Northatlantic NCG seminar 2021 (video 2hr [yt](https://www.youtube.com/watch?v=F0MiZMxjQlk))

* Tomasz Brzeziński, Bernard Rybołowicz, _Modules over trusses vs modules over rings: direct sums and free modules_, Algebra and Representation Theory 25, 1–23 (2022) [doi](https://doi.org/10.1007/s10468-020-10008-8)

* Ryszard R. Adruszkiewicz, Tomasz Brzeziński, Bernard Rybołowicz, _Ideal ring extensions and trusses_, [arXiv:2101.09484](https://arxiv.org/abs/2101.09484)

category: algebra

    