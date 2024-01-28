
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

A weak notion of [[local ring]] in the context of [[constructive mathematics]]. 

## Definition

A **weak local ring** is a [[commutative ring]] such that 

* $0 \neq 1$; and

* the sum of two non-invertible elements is non-invertible

These are the same as [[local rings]] in classical mathematics, but are a weaker (and thus more general) notion than local rings in [[constructive mathematics]]. 

## Properties

The non-invertible elements in a weak local ring form an [[ideal]]. Thus, the quotient of a weak local ring by its ideal of non-invertible elements form a [[weak Heyting field]] (cf. [Richman 2020](#Richman20)) or a [[Johnstone residue field]] (cf. [Johnstone 1977](#Johnstone77)). 

Every weak local ring has an [[equivalence relation]] $\approx$, defined as $x \approx y$ if and only if $x - y$ is non-invertible. Then weak Heyting fields are precisely the weak local rings for which $\approx$ implies [[equality]]. 

## Examples

* Every [[weak Heyting field]] is an weak local ring where every non-invertible element is equal to zero. 

* The dual algebra $\mathbb{R}[\epsilon]/\epsilon^2$ of the [[MacNeille real numbers]] $\mathbb{R}$ is a weak local ring where the [[nilpotent]] [[infinitesimal]] $\epsilon \in \mathbb{R}[\epsilon]/\epsilon^2$ is a non-zero non-invertible element. 

* For any prime number $p$ and any positive natural number $n$, the [[prime power local ring]] $\mathbb{Z}/p^n\mathbb{Z}$ is an weak local ring, whose ideal of non-invertible elements is the ideal $p(\mathbb{Z}/p^n\mathbb{Z})$. The quotient of $\mathbb{Z}/p^n\mathbb{Z}$ by its ideal of non-invertible elements is the [[finite field]] $\mathbb{Z}/p\mathbb{Z}$. 

* Every [[local ring]] is a weak local ring with an [[apartness relation]] $\#$ such that for all $a \in R$ and $b \in R$, $a \# b$ if and only if $a - b$ is invertible. The negation of $a \# b$ is an [[equivalence relation]] which holds if and only if $a - b$ is non-invertible, making every local ring a weak local ring. 

## Weakly ordered local rings

A weakly ordered local ring is a weak local ring $R$ with a [[preorder]] $\leq$ such that 

* for all $a \in R$ and $b \in R$, $a \approx b$ if and only if $a \leq b$ and $b \leq a$
* for all $a \in R$, $b \in R$, and $c \in R$, if $a \leq b$, then $a + c \leq b + c$
* for all $a \in R$ and $b \in R$, if $0 \leq a$ and $0 \leq b$, then $0 \leq a \cdot b$

If additionally, for all $a \in R$ and $b \in R$, $a \approx b$ implies that $a = b$, then a weakly ordered local ring becomes a weakly ordered Heyting field, and the preorder becomes a [[partial order]]. 

Every [[ordered local ring]] and thus every [[ordered field]] is a weakly ordered local ring. 

## See also

* [[local ring]]

* [[ordered local ring]]

## References

* {#Johnstone77} [[Peter Johnstone]], *Rings, Fields, and Spectra*, Journal of Algebra **49** (1977) pp 238-260. doi:[10.1016/0021-8693(77)90284-8](https://doi.org/10.1016/0021-8693%2877%2990284-8)

* {#Richman20} [[Fred Richman]], *Laurent series over $\mathbb{R}$*. Communications in Algebra, Volume 48, Issue 5, 11 Jan 2020 Pages 1982-1984 &lbrack;[doi:10.1080/00927872.2019.1710166](https://doi.org/10.1080/00927872.2019.1710166)&rbrack;

[[!redirects weak local ring]]
[[!redirects weak local rings]]