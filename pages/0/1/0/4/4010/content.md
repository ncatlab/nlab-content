

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##
The Schr&#246;dinger equation (named after [[Erwin Schrödinger]]) is the [[evolution equation]] of [[quantum mechanics]] in the [[Schrödinger picture]]. Its simplest version results from replacing the classical expressions in the nonrelativistic, mechanical equation for the energy of a pointparticle, by [[operators]] on a [[Hilbert space]]:

We start with a point particle with mass $m$, impulse $p$ moving in the space $\mathbb{R}^3$ with a given potential function $V$, the energy of it is the sum of kinetic and potential energy: 
$$
   E = \frac{p^2}{2 m} + V
$$

Quantizing this equation means replacing the coordinate $x \in \mathbb{R}^3$ with the [[Hilbert space]] $L^2(\mathbb{R}^3)$ and 
$$
E \to i \hbar  \frac{\partial}{\partial t}
$$

$$
p \to -i  \hbar \nabla
$$


with the [[Planck constant]] $h$ and
$$
\hbar = \frac{h}{2 \pi}
$$
the reduced Planck constant.

This results in the Schr&#246;dinger equation for a single particle in a potential:
$$
i \hbar  \frac{\partial}{\partial t} \psi(t, x) = - \frac{\hbar^2}{2 m} \nabla^2 \psi(t, x) + V(t, x) \psi(t, x)
$$
The last term is the multiplication of the functions $V$ and $\psi$.

The right hand side is called the [[Hamilton operator]] $H$, the Schr&#246;dinger equation is therefore mostly stated in this form:
$$
i \hbar \psi_t = H \psi
$$ 

## Abstract ##
...

## Definition ##
...

## Properties ##
...

## Examples ##
...

## References ##
Any introductory textbook about [[quantum mechanics]] will explain the Schr&#246;dinger equation (from the viewpoint of physicists mostly).

* Wikipedia: [Schr&#246;dinger equation] (http://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation)