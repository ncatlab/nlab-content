
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


For a [[linear operator]] $A$ on a [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]] $V$, the *spectrum* of $A$ is simply the [[subset]] of the [[complex numbers]] consisting of the [[eigenvalues]] of $A$. 

In the case that $V$ is an infinite-dimensional complex [[separable Hilbert space]], the ([[normal eigenvalue|normal]]) eigenvalues only form the *discrete spectrum*.  Instead, the full spectrum is the set of all $\lambda \in \mathbb{C}$ for which the [[resolvent]] $(A-\lambda I)^{-1}$ is not a [[bounded operator]]. 

In other words, the spectrum is the [[complement]] of the subset of complex numbers for which the resolvent is a [[bounded operator]].

## Properties

If $A$ is a [[bounded linear operator]] on a complex separable Hilbert space, then the spectrum $\sigma(A)$ is a [[compact subset]] of $\mathbb{C}$. 

The set $\sigma_d(A)$ of ordinary [[normal eigenvalues|normal]] [[eigenvalues]] of $A$ is a subset of $\sigma(A)$ called the *discrete spectrum* of $A$. In particular case when $A$ is a [[compact operator]] the spectrum consists of the discrete spectrum only, except for possible addition of point $0$.

## Related concepts

* [[essential spectrum]], [[Calkin algebra]]

* [[spectral gap]]

* [[spectral flow]]

* [[spectral theory]]

* [[min-entropy]]

## References


* {#Müller2003} [[Vladimir Müller]]: *Spectral Theory of Linear Operators and Spectral Systems in Banach Algebras*, Operator Theory: Advances and Applications **139**, Birkhäuser (2003, 2007) &lbrack;[doi:10.1007/978-3-7643-8265-0](https://doi.org/10.1007/978-3-7643-8265-0)&rbrack;


See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Spectrum_(functional_analysis)">Spectrum (functional_analysis)</a>*

[[!redirects operator spectrum]]
[[!redirects spectrum of operator]]
[[!redirects spectrum of a linear operator]]
[[!redirects spectrum of linear operator]]

[[!redirects discrete spectrum]]
[[!redirects discrete spectra]]
