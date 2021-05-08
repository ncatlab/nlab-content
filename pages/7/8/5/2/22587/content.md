
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[ODE]]/[[PDE]]-theory, the *homtopy analysis method* ([Liao 92](#Liao92)) is a method for solving a *non-linear* [[differential equation]] $N_x u(x) = 0$ by considering a [[homotopy]] of PDEs to a [[linear differential equation]] $L_x \big(u(x) - u_0(x)\big) = 0$

$$
  q 
  \;\mapsto
  \;\;\;
  q \cdot N_x u(x,q)
  \;+\;
  (1-q) \cdot L_x\big(u(x,q) - u_0(x,q)\big)
$$

and then solving this in terms of a [[Taylor series]]-expansion of the desired solution $u$ in the new parameter $q$ ("homotopy Maclaurin series"), which  transforms the original non-linear differential equation into an infinite sequence of [[linear differential equations]], that can (apparently) often be solved more readily.


## References

Original articles:

* {#Liao92} Shijun Liao, *The proposed homotopy analysis technique for the solution of nonlinear problems*, PhD thesis, Shanghai Jiao Tong University (1992)

* Shijun Liao, *Notes on the homotopy analysis method: Some definitions and theorems*, Communications in Nonlinear Science and Numerical Simulation, Volume 14, Issue 4, April 2009, Pages 983-997 ([doi:10.1016/j.cnsns.2008.04.013](https://doi.org/10.1016/j.cnsns.2008.04.013))

* Binfeng Pan, Yangyang Ma, Yang Ni, *A new fractional homotopy method for solving nonlinear optimal control problems*, Acta Astronautica, Volume 161, August 2019, Pages 12-23 ([doi:10.1016/j.actaastro.2019.05.005](https://doi.org/10.1016/j.actaastro.2019.05.005))

But see:

* Cheng-shi Liu, *The essence of the homotopy analysis method*, Applied Mathematics and Computation Volume 216, Issue 4, 15 April 2010, Pages 1299-1303 ([doi:10.1016/j.amc.2010.02.022](https://doi.org/10.1016/j.amc.2010.02.022))

Introduction and review:

* Shijun Liao, *Beyond Perturbation -- Introduction to the Homotopy Analysis Method*, CRC Press 2003 ([ISBN:9781584884071](https://www.routledge.com/Beyond-Perturbation-Introduction-to-the-Homotopy-Analysis-Method/Liao/p/book/9781584884071))

* Shijun Liao, *Homotopy Analysis Method in Nonlinear Differential Equations* Springer 2012 ([pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-642-25132-0.pdf))

* V.G. Gupta, Sumit Gupta, *Application of the Homotopy Analysis Method for solving nonlinear Cauchy Problem*, Surveys in Mathematics and its Applications, Volume 7 (2012), 105 – 116 ([ISSN:1842-6298](https://www.emis.de/journals/SMA/v07/a08.html), [pdf](https://www.emis.de/journals/SMA/v07/p08.pdf))

See also

* Wikipedia, *[Homotopy analysis method](https://en.wikipedia.org/wiki/Homotopy_analysis_method)*



Further development:

* M. Turkyilmazoglu, *A note on the homotopy analysis method*, Applied Mathematics Letters Volume 23, Issue 10, October 2010, Pages 1226-1230 ([doi:10.1016/j.aml.2010.06.003](https://doi.org/10.1016/j.aml.2010.06.003))



