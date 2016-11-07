
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

The _Helmholtz operator_ (going back to [Helmholtz 87](#Helmholtz87), [Sonin](#Sonin), with modern version due to [Vinogradov 78](#Vinogradov78), [Tulczyjew 80](#Tulczyjew80)) is a map from [[partial differential equations]] (on [[sections]] of some [[bundle]]) to [[differential operators]] (on sections of that bundle) with the property that locally its [[kernel]] consists precisely of those [[PDEs]] which are _variational_ in that there is a [[local Lagrangian density]] such that the PDE is the [[Euler-Lagrange equation]] which says that the variational of this Lagrangian (equivalently: of the [[action functional]] that it induces) vanishes.

In modern terminology this says that together with the [[Euler-Lagrange operator]] the Helmholtz operator constitutes a [[chain complex]] of [[abelian sheaves]] (namely of [[differential forms]] on a [[jet bundle]]) which is locally [[long exact sequence|exact]]. In fact this extends in both directions to a locally [[long exact sequence]] of forms on the jet bundle, called the [[Euler-Lagrange complex]]. See there for more.

## Details

A quick way to write the Helmholtz operator $H$ is as follows: If $\mathcal{E}$ denotes a [[partial differential equation]] and $L\mathcal{E}$ its linearization, and $(L\mathcal{E}^\ast$ its [[formal adjoint differential operator]], as a [[differential operator]] then

$$
  H[\mathcal{E}]
    =
  L\mathcal{E}
   -
  (L\mathcal{E})^\ast
  \,.
$$ 

This means that the PDE $\mathcal{E}$ is locally variational precisely if its linearization is formally self-adjoint.

## References

The Helmholtz operator originates in

* {#Helmholtz87} [[Hermann von Helmholtz]], _&#220;ber die physikalische Bedeutung des Princips der kleinsten Wirkung_, Journal f&#252;r reine und angewandte Mathematik 100 (1887), 137&#8211;166

* {#Sonin} Sonin, ...

where it is considered for linear [[ordinary differential equations]]. The modern general incarnation of the Helmholtz condition is due to 

* {#Vinogradov78} [[Alexandre Vinogradov]], _A spectral sequence associated with a non-linear differential equation, and the algebro-geometric foundations of Lagrangian field theory with constraints_, Soviet Math. Dokl. 19 (1978), 144&#8211;148.

* {#Tulczyjew80} W. M. Tulczyjew, _The Euler-Lagrange resolution_, in Lecture Notes in Mathematics No. 836, Springer-Verlag, New York, 1980, pp. 22&#8211;48.


Review includes

* [[Ian Anderson]],  _Aspects of the inverse problem to the calculus of variations_.
Archivum Mathematicum, vol. 24 (1988), issue 4, pp. 181-202 ([web](http://dml.cz/dmlcz/107326))

* {#Anderson89} [[Ian Anderson]], _The variational bicomplex_, Utah State University 1989 ([[AndersonVariationalBicomplex.pdf:file]]) 
