
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

Given a [[commutative ring]] $R$, an [[element]] $e \in R$ is *left cancellative* if $e \cdot a = e \cdot b$ for all $a \in R$ and $b \in R$, then $a = b$. 

$$\mathrm{isLeftCancellative}(e) \coloneqq \forall a,b \in R.(e \cdot a = e \cdot b) \implies (a = b)$$

An element $e \in R$ is *right cancellative* if $a \cdot e = b \cdot e$ for all $a \in R$ and $b \in R$, then $a = b$. 

$$\mathrm{isRightCancellative}(e) \coloneqq \forall a,b \in M.(a \cdot e = b \cdot e) \implies (a = b)$$

An element $e \in R$ is *cancellative* if it is both left cancellative and right cancellative.

$$\mathrm{isCancellative}(e) \coloneqq \mathrm{isLeftCancellative}(e) \wedge \mathrm{isRightCancellative}(e)$$

The **multiplicative submonoid of cancellative elements in $R$** is the subset of all cancellative elements in $R$

$$\mathrm{Can}(R) \coloneqq \{e \in M \vert \mathrm{isCancellative}(e)\}$$

## See also ##

* [[cancellative monoid]]

* [[GCD ring]]

* [[prefield]]

* [[group of units]]

[[!redirects multiplicative submonoids of cancellative elements]]
