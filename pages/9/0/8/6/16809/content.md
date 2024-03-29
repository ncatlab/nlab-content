

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given a smooth [[bundle]] $E \to \Sigma$ over a [[smooth manifold]] $\Sigma$, then its _Euler-Lagrange complex_ is a [[resolution]] of the [[constant sheaf]] of [[locally constant functions]] on the [[jet bundle]] $J^\infty E$ by a [[chain complex]] of sheaves of certain [[differential forms]]. The Euler-Lagrange complex starts out as the complex of [[horizontal differential forms]] up to degree $n \coloneqq dim(\Sigma)$ the [[dimension]] of $\Sigma$, the following [[differential]] is 

1. the [[Euler-Lagrange operator]] $\delta_{El}$

1. followed by the [[Helmholtz operator]] $\delta_{Helm}$

$$
 0 \to \mathbb{R}
 \to
  \Omega^{0,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \Omega^{1,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \cdots 
  \stackrel{d_H}{\to}
  \Omega^{n,0}(J^\infty E)
  \stackrel{\delta_{EL}}{\to}
  \mathcal{F}^1(J^\infty E)
  \stackrel{\delta_{Helm}}{\to}
  \mathcal{F}^2(J^\infty E)
  \stackrel{\delta_V}{\to}
  \cdots
$$

Hence the elements in the Euler-Lagrange complex have the following interpretation

* in degree $dim(\Sigma)$: [[local Lagrangians]];

* in degree $dim(\Sigma)+1$: [[Euler-Lagrange equations of motion]];

* in degree $dim(\Sigma)-1$: trivial local Lagrangians;

* in degree $dim(\Sigma)+2$: [[obstructions]] for [[equations of motion]] to be variational, i.e. to be the Euler-Lagrange equations of a local Lagrangian.

## Properties

+-- {: .num_prop #ELComplexHasSameCohomologyAsDeRhamComplex}
###### Proposition

The [[cochain cohomology]] of the [[Euler-Lagrange complex]]

$$
 0 \to \mathbb{R}
 \to
  \Omega^{0,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \Omega^{1,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \cdots 
  \stackrel{d_H}{\to}
  \Omega^{n,0}(J^\infty E)
  \stackrel{E}{\to}
  \mathcal{F}^1(J^\infty E)
  \stackrel{\delta_V}{\to}
  \mathcal{F}^2(J^\infty E)
  \stackrel{\delta_V}{\to}
  \cdots
$$

is [[isomorphism|isomorphic]] to the [[de Rham cohomology]] of the total space $E$ of the given fiber bundle.

=--

([Anderson 89, theorem 5.9](#Anderson89)).

## Related concepts

* [[variational sequence]]

## References

The Euler-Lagrange complex was recognized in

* {#Vinogradov78} [[Alexandre Vinogradov]], _A spectral sequence associated with a non-linear differential equation, and the algebro-geometric foundations of Lagrangian field theory with constraints_, Soviet Math. Dokl. 19 (1978), 144&#8211;148.

* {#Tulczyjew80} W. M. Tulczyjew, _The Euler-Lagrange resolution_, in Lecture Notes in Mathematics No. 836, Springer-Verlag, New York, 1980, pp. 22&#8211;48.

Review includes

* {#VinogradovKrasilshchik99} [[Alexandre Vinogradov]], I. S. Krasilshchik (eds.) _Symmetries and Conservation Laws for Differential Equations of Mathematical Physics_, vol. 182 of Translations of Mathematical Monographs. American Mathematical Society, Providence, RI, 1999. ([pdf](ftp://softbank.iust.ac.ir/MathBooks/V/Vinogradov%20-%20Symmetries%20and%20Conservation%20Laws%20for%20Differential%20equations%20of%20mathematical%20physics.pdf))

* {#Anderson89} [[Ian Anderson]], _The variational bicomplex_, Utah State University 1989 ([[AndersonVariationalBicomplex.pdf:file]]) 


[[!redirects Euler complex]]
[[!redirects Euler complexes]]

[[!redirects Euler-Lagrange operator]]
[[!redirects Euler-Lagrange operators]]

[[!redirects Euler-Lagrange variational derivative]]
[[!redirects Euler-Lagrange variational derivatives]]


[[!redirects Euler-Lagrange derivative]]
[[!redirects Euler-Lagrange derivatives]]
