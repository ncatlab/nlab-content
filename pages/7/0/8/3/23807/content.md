
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

For a [[commutative ring]] $R$, where $\mathrm{Can}(R)$ is the [[multiplicative submonoid of cancellative elements]], the corresponding [[commutative localization]] $D\to (\mathrm{Can}(R))^{-1} R$ is an injective homomorphism of rings and $Q(R) = (\mathrm{Can}(R))^{-1} R$ is a [[prefield]], called the **ring of fractions** or the fraction ring of $R$. 

Its elements are fractions $a/b$ where $a\in R$ and $b\in \mathrm{Can}(R)$ which are by the definition the equivalence classes of pairs $(a,b) \in R\times \mathrm{Can}(R)$ and $(a,b)\sim (c,d)$ iff $a d = b c$. The addition is given by the formula
$$
\frac{a}{b}+\frac{c}{d} = \frac{ad+bc}{bd}
$$
and multiplication by $(a/b)(c/d) = (ac)/(bd)$. 

## Related concepts

* [[Grothendieck group]]

* [[localization]]

* [[prefield]]

* [[multiplicative submonoid of cancellative elements]]

## References

* [[Frank Quinn]], *Proof Projects for Teachers* ([pdf](https://personal.math.vt.edu/fquinn/education/pfs4teachers0.pdf))

[[!redirects rings of fractions]]

[[!redirects fraction ring]]
[[!redirects fraction rings]]

[[!redirects prefield of fractions]]
[[!redirects prefields of fractions]]

[[!redirects quotient prefield]]
[[!redirects quotient prefields]]

[[!redirects fraction prefield]]
[[!redirects fraction prefields]]

