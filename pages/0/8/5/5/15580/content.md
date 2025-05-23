
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

For $G$ an [[abelian group]], then the _Moore spectrum_ $S G$ (often $M G$) of $G$ is the [[spectrum]] characterized by having the following [[homotopy groups]]:

1. $\pi_{\lt 0} S G = 0$;

1. $\pi_0(S G) = G$;

1. $H_{\gt 0}(S G,\mathbb{Z}) = 0$.

Here $H \mathbb{Z}$ is the [[Eilenberg-MacLane spectrum]] of the [[integers]] and $H_\ast(S G,\mathbb{Z})= \pi_{\ast}(S G \wedge H \mathbb{Z})$.

## Properties

### Bousfield localization at Moore spectra

A basic special case of $E$-[[Bousfield localization of spectra]] is given by $E = S A$ the Moore spectrum of an [[abelian group]] $A$. For $A = \mathbb{Z}_{(p)}$ this is [[p-localization]] and for $A = \mathbb{F}_p$ this is [[p-completion]].

+-- {: .num_prop}
###### Proposition

For $A_1$ and $A_2$ two [[abelian groups]] then the following are equivalent

1. the [[Bousfield localization of spectra|Bousfield localizations]] at their Moore spectra are equivalent 

   $$
     L_{S A_1} \simeq L_{S A_2}
     \,;
   $$

1. $A_1$ and $A_2$ have the same _type of acyclicity_, meaning that 
 
   1. every [[prime number]] $p$ is invertible in $A_1$ precisely if it is in $A_2$;

   1. $A_1$ is a [[torsion group]] precisely if $A_2$ is.

=--

([Bousfield 79, prop. 2.3](#Bousfield79)) recalled e.g. in ([VanKoughnett 13, prop. 4.2](#VanKoughnett13)).

This means that given an abelian group $A$ then 

* either $A$ is not torsion, then 

  $$
    L_{S A} \simeq L_{S \mathbb{Z}[I^{-1}]}
    \,,
  $$ 

  where $I$ is the set of primes invertible in $A$ and $\mathbb{Z}[I^{-1}] \hookrightarrow \mathbb{Q}$ is the [[localization of a ring|localization]] at these primes of the [[integers]];

* or $A$ is torsion, then 
    
  $$
   L_{S A }\simeq L_{S(\oplus_q \mathbb{F}_q )  }
   \,,
  $$

  where the [[direct sum]] is over all [[cyclic groups]] of order $q$ for $q$ a prime not invertible in $A$.



### Serre's theorem
  {#SerreTheorem}

* For $\mathbb{Q}$ the [[rational numbers]] there is an equivalence $S \mathbb{Q} \stackrel{\simeq}{\longrightarrow} H \mathbb{Q}$ between the Moore spectrum and the [[Eilenberg-MacLane spectrum]]. (e.g. [Banagl 10, p. 6](#Banagl10))

## Related concepts

* [[Eilenberg-MacLane spectrum]]

* [[Bousfield localization of spectra]]

## References

* [[Frank Adams]], Part III.6 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Schwede12} [[Stefan Schwede]], section II.6.3 of _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/people/schwede/SymSpec-v3.pdf))

Lecture notes:

* {#Strickland} [[Neil Strickland]], p. 9 of _An introduction to the category of spectra_ ([pdf](https://neil-strickland.staff.shef.ac.uk/research/stableintro.pdf))

* [[Neil Strickland]], section 14 of: *A Bestiary of Topological Objects* \[<a href="https://strickland1.org/courses/bestiary/bestiary.pdf">pdf</a>, [[Strickland-BestiaryTopological.pdf:file]]\]


* {#VanKoughnett13} [[Paul VanKoughnett]], _Spectra and localization_, 2013 ([[VanKoughnettLocalization.pdf:file]])

* {#Rognes12} [[John Rognes]], section 4.6 of _The Adams spectral sequence_, 2012 ([pdf](https://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/notes.050612.pdf))


Discussion in the context of [[Bousfield localization of spectra]] is in 

* {#Bousfield79} [[Aldridge Bousfield]], section 2 of _The localization of spectra with respect to homology_ , Topology vol 18 (1979) ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))
 
See also 

* {#Banagl10} [[Markus Banagl]], *Rational generalized intersection homology theories*, Homology, Homotopy and Applications, **12** 1 (2010) 157-185  &lbrack;[pdf](http://www.mathi.uni-heidelberg.de/~banagl/pdfdocs/spectrumqih.pdf), [euclid](https://projecteuclid.org/journals/homology-homotopy-and-applications/volume-12/issue-1/Rational-generalized-intersection-homology-theories/hha/1296223826.full)&rbrack;

[[!redirects Moore spectra]]
