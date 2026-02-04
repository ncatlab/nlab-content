
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


\tableofcontents


### Definition

Consider 

* [[open subsets]]$\;D, D' \subset \mathbb{C}$ of the [[complex plane]],

* a [[differentiable function|differentiable]] [[homeomorphism]] $f \colon D \longrightarrow D'$.

The [[ratio]] 
\[
  \label{ComplexDilatation}
  \mu_f 
    \coloneqq
  \frac   
    { \bar\partial f }
    { \partial f }
\]
of the function's (anti-)holomorphic derivatives
$$
  \partial f 
  \,\coloneqq\,
  \frac{\partial f}{\partial z}
  \;\coloneqq\;
  \tfrac{1}{2}\big(
    \tfrac{\partial f}{\partial x}
    -\mathrm{i}
    \tfrac{\partial f}{\partial y}
  \big)
  \,,\;\;\;
  \bar\partial f 
  \,\coloneqq\,
  \frac{\partial f}{\partial \bar z}
$$ 
is called the *complex dilatation* $\mu_f$ of $f$, a measure for the function's failure to be a [[conformal map]] or [[holomorphic map]].

The actual *dilatation* of $f$ is defined to be the [[ratio]]
\[
  \label{Dilatation}
  D_f
  \;\coloneqq\;
  \frac
    { 1 + d_f }
    { 1 - d_f }
\]
for
$$
  d_f 
  \;\coloneqq\;
  \left\vert\mu_f\right\vert
  =
  \frac
    { \left\vert \bar\partial f\right\vert }
    { \left\vert \partial f\right\vert }
$$
the [[absolute value]] of the complex dilation (eq:ComplexDilatation).

The function $f$ is called *quasi-conformal* if its dilatation $D_f \colon \mathbb{C} \longrightarrow \mathbb{R}$ (eq:Dilatation) is a [[bounded function]].


### References

* [[Lars V. Ahlfors]]; pp. 4 of: *Lectures on quasiconformal mappings*, Van Nostrand, Princeton (1966), University Lecture Series **38** AMS (2006) &lbrack;[ams:ULECT/38](https://bookstore.ams.org/view?ProductCode=ULECT/38), [pdf](https://zr9558.com/wp-content/uploads/2013/11/lectures-on-quasiconformal-mappings-ahlfors.pdf)&rbrack;

* Davoud Cheraghi; sections 7.1-2 in: *Geometric Complex Analysis* (2016) &lbrack;[pdf](https://www.ma.imperial.ac.uk/~dcheragh/Teaching/2016-F-GCA/2016-F-GCA.pdf), [[Cheraghi-ComplexAnalysis.pdf:file]]&rbrack;

* [[Nikolai V. Ivanov]]: *The geometric meaning of the complex dilatation* &lbrack;[arXiv:1701.06259](https://arxiv.org/abs/1701.06259)&rbrack;

See also:

* Wikipedia: *[Quasiconformal map](https://en.wikipedia.org/wiki/Quasiconformal_mapping)*


[[!redirects quasiconformal maps]]

[[!redirects quasiconformal mapping]]
[[!redirects quasiconformal mappings]]

[[!redirects quasi-conformal map]]
[[!redirects quasi-conformal map]]


[[!redirects quasi-conformal mapping]]
[[!redirects quasi-conformal mappings]]


