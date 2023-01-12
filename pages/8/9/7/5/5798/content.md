
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $R$ a [[commutative ring]], its **nilradical** $I \subset R$ is the [[ideal]] of [[nilpotent elements]]: the collection of those elements $a \in R$ such that there is $n \in \mathbb{N}$ with $a^n = 0$.

The [[quotient]] $R/I$ is also called the _[[reduced object|reduced]]_ part of $R$.

(If $R$ is not [[commutative ring|commutative]] there are different generalization of the notion of nilradical. See Wikipedia, for the moment.) 

## Examples

Every [[local Artinian ring]] is a commutative ring whose set of non-invertible elements is a [[nilradical]]. 

With rings regarded as [[Isbell duality|formal dual]]s of [[affine scheme]]s, the canonical inclusion

$$
  Spec R/I \to Spec R
$$

is to be thought of as exhibiting the inclusion of $Spec R/I$ into an [[infinitesimal object|infinitesimal thickening]] of itself.

For $X : CRing \to Set$ a [[presheaf]] on the [[category]] of [[commutative rings]], the presheaf

$$
  X_{dR} : Spec R \mapsto X(Spec R/I)
$$

is called the [[de Rham space]] of $X$.

## Reduced rings and trivial nilradicals

Given a [[commutative ring]] $R$, $R$ is **reduced** or has a **trivial nilradical** if $x \cdot x = 0$ implies that $x = 0$ for all $x \in R$. This implies that for every natural number $n$, $x^{n + 1} = 0$ implies that $x = 0$ for all $x \in R$. Let the function $f:\mathbb{N} \to \mathbb{N}$ be defined as the [[ceiling]] of half of $n$, $f(n) \coloneqq \lceil n/2 \rceil$. Then $x^{n + 1} = 0$ implies that $x^{f(n + 1)} = 0$, and for every natural number $n$, the $(n + 1)$-th iteration of the function $f$ evaluated at $n + 1$ is always equal to $1$, $f^{n + 1}(n + 1) = 1$, thus resulting in $x^{f^{n + 1}(n + 1)} = x = 0$. Thus, the nilradical of $R$ is trivial. 

As a result, the theory of a reduced ring is a [[coherent theory]]. 

## Related concepts

* [[infinitesimal extension]]

## References

See also:

* Wikipedia, *[Nilradical](https://en.m.wikipedia.org/wiki/Nilradical_of_a_ring)*

[[!redirects nilradical]]
[[!redirects nilradicals]]

[[!redirects trivial nilradical]]
[[!redirects trivial nilradicals]]

[[!redirects reduced ring]]
[[!redirects reduced rings]]

[[!redirects reduced algebra]]
[[!redirects reduced algebras]]


