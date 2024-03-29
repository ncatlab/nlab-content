
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[field strength]] of the [[electromagnetic field]].

## Details

Over [[Minkowski space]] $\mathbb{R}^{4}$:

the [[electromagnetic potential]]

$$
  A = \phi \mathbf{d}t + A_1 \mathbf{d}x^1 + A_2 \mathbf{d}x^2 + A_3 \mathbf{d}x^3
$$

then [[field strength]] is the [[de Rham differential]]

$$
  F 
    \coloneqq
  \mathbf{d}A 
    = 
   E_1 \mathbf{d}t \wedge \mathbf{d}x^1 
    + 
   E_2 \mathbf{d}t \wedge \mathbf{d}x^2 
    + 
   E_3 \mathbf{d}t \wedge \mathbf{d}x^3
    + 
    B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3 
    + 
    B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1 
    + 
    B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2 
$$

with 

$$
  E_i = \frac{\partial \phi}{\partial x^i}
$$

the _electric field strength_

and

$$
  B_1 = \frac{\partial A_2}{\partial x^3} - \frac{\partial A_3}{\partial x^2}
$$

etc

the _magnetic field strength_.

The field strength is closed, $\mathbf{d} F = 0$

this are the first 2 of 4 [[Maxwell equations]]

## Related concepts

* [[electromagnetic potential]]

* [[Aharonov-Bohm effect]]

* [[Dirac charge quantization]]
