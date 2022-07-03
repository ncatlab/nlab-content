
> This entry is about regular elements in [[ring theory]] and [[commutative algebra]]. For regular elements in [[formal logic]] and [[topology]], see [[regular element]]. For regular elements in [[physics]]/[[quantum field theory]] see at _[[regularization (physics)]]_. 

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

Given a [[commutative ring]] $R$, an [[element]] $e \in R$ is *left cancellative* or *left regular* if $e \cdot a = e \cdot b$ for all $a \in R$ and $b \in R$, then $a = b$. 

$$\mathrm{isLeftCancellative}(e) \coloneqq \forall a,b \in R.(e \cdot a = e \cdot b) \implies (a = b)$$

An element $e \in R$ is *right cancellative* or *right regular* if $a \cdot e = b \cdot e$ for all $a \in R$ and $b \in R$, then $a = b$. 

$$\mathrm{isRightCancellative}(e) \coloneqq \forall a,b \in M.(a \cdot e = b \cdot e) \implies (a = b)$$

An element $e \in R$ is *cancellative* or *regular* if it is both left cancellative and right cancellative.

$$\mathrm{isCancellative}(e) \coloneqq \mathrm{isLeftCancellative}(e) \wedge \mathrm{isRightCancellative}(e)$$

The **multiplicative subset of cancellative elements** in $R$ is the [[multiplicative subset]] of all cancellative elements in $R$

$$\mathrm{Can}(R) \coloneqq \{e \in M \vert \mathrm{isCancellative}(e)\}$$

If the synonym 'regular element' is used in place of 'cancellative element', such as in [LombardiQuitté2010](LombardiQuitté2010), then this multiplicative subset is typically written as $\mathrm{Reg}(R)$. 

Since the multiplicative identity element $1$ is always cancellative, the multiplicative subset of all cancellative elements forms a [[cancellative monoid]]. 

## See also ##

* [[multiplicative subset]]

* [[filter of a ring]]

* [[cancellative monoid]]

* [[torsion-free module]]

* [[GCD ring]]

* [[prefield]]

* [[ring of fractions]]

* [[group of units]]

## References

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects cancellative element]]
[[!redirects cancellative elements]]
[[!redirects regular element]]
[[!redirects regular elements]]

[[!redirects multiplicative subsets of cancellative elements]]
[[!redirects multiplicative subset of regular elements]]
[[!redirects multiplicative subsets of regular elements]]

[[!redirects filter of cancellative elements]]
[[!redirects filters of cancellative elements]]
[[!redirects filter of regular elements]]
[[!redirects filters of regular elements]]

[[!redirects multiplicative submonoid of cancellative elements]]
[[!redirects multiplicative submonoids of cancellative elements]]
[[!redirects multiplicative submonoid of regular elements]]
[[!redirects multiplicative submonoids of regular elements]]
