
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In the same vein that [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]], rings of fractions are to [[field of fractions]]. 

## Definition ##

Let $R$ be a [[commutative ring]]. A multiplicative submonoid of $R$ is a subset $S \subseteq R$ with an injection $m:S \hookrightarrow R$, an element $1_S \in S$ and a function $(-)\cdot_S(-):S \times S \to S$, such that $m(1_S) = 1$ and for all elements $a \in S$ and $b \in S$, $s(a \cdot_S b) = s(a) \cdot s(b)$. The [[localization of a commutative ring|localization]] of $R$ away from a multiplicative submonoid $S$ is the [[initial object|initial]] commutative ring $R[S^{-1}]$ with a commutative ring homomorphism $h:R \to R[S^{-1}]$ and a function $(-)^{-1}:S \to R[S^{-1}]$, such that for all $a \in S$, $h(m(a)) \cdot a^{-1} = 1$. 

The **ring of fractions** $R[\mathrm{Reg}(R)^{-1}]$ is the localization of $R$ away from the [[multiplicative subset of regular elements]] $\mathrm{Reg}(R)$. Its elements are fractions $\frac{a}{b}$ where $a\in R$ and $b\in \mathrm{Reg}(R)$ which are by the definition the equivalence classes of pairs $(a,b) \in R\times \mathrm{Reg}(R)$ and $(a,b)\sim (c,d)$ iff $a \cdot d = b \cdot c$. The addition is given by the formula
$$\frac{a}{b}+\frac{c}{d} = \frac{a \cdot d+b \cdot c}{b \cdot d}$$
and multiplication by 
$$\frac{a}{b} \cdot \frac{c}{d} = \frac{a \cdot c}{b \cdot d}$$

For $a \in R$, $b \in \mathrm{Reg}(R)$, $c \in \mathrm{Reg}(R)$, and $d \in \mathrm{Reg}(R)$, division is given by
$$\frac{a}{b} \div \frac{c}{d} = \frac{a \cdot d}{b \cdot c}$$

## Examples

* The ring of fractions of the [[integers]] is the [[rational numbers]] $\mathbb{Q} \coloneqq \mathbb{Z}[\mathrm{Reg}(\mathbb{Z})^{-1}]$. 

* The ring of fractions of a [[Heyting integral domain]] is a [[Heyting field]]. 

* The ring of fractions of a [[strict approximate integral domain]] is a [[local ring]]. 

* The ring of fractions of any [[commutative ring]] is a [[prefield ring]]. 

## Related concepts

* [[Grothendieck group]]

* [[localization]]

* [[prefield ring]]

* [[multiplicative submonoid of cancellative elements]]

## References

* [[Frank Quinn]], *Proof Projects for Teachers* ([pdf](https://personal.math.vt.edu/fquinn/education/pfs4teachers0.pdf))

[[!redirects rings of fractions]]

[[!redirects fraction ring]]
[[!redirects fraction rings]]

[[!redirects prefield ring of fractions]]
[[!redirects prefield rings of fractions]]

[[!redirects quotient prefield ring]]
[[!redirects quotient prefield rings]]

[[!redirects fraction prefield ring]]
[[!redirects fraction prefield rings]]

