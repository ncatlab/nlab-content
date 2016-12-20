

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
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

### Decomposition into phase and amplitude


Consider for simplicity, the [[mechanical system]] of a [[particle]] of [[mass]] $m$ propagating on the [[real line]] $\mathbb{R}$ and subject to a [[potential]] $V \in C^\infty(\mathbb{R})$, so that the Schr&#246;dinger equation is the [[differential equation]] on [[complex number|complex]]-valued [[functions]] $\Psi \colon \mathbb{R}\times \mathbb{R} \to \mathbb{C}$ given by

$$
  i \hbar
  \frac{\partial}{\partial t}
  \Psi
  =
  \frac{\hbar^2}{2m}
  \frac{\partial^2}{\partial^2 x} \Psi
  + 
  V \Psi
  \,,
$$

where $\hbar$ denotes [[Planck's constant]].

By the nature of [[complex numbers]] and by the discussion at _[[phase and phase space in physics]]_, it is natural to parameterize $\Psi$ -- away from its [[zero locus]] -- by a [[complex phase]] function

$$
  S \;\colon\; \mathbb{R}\times \mathbb{R} \longrightarrow \mathbb{R}
$$

and an [[absolute value]] function $\sqrt{\rho}$

$$
  \sqrt{\rho} \;\colon\; \mathbb{R}\times \mathbb{R} \longrightarrow \mathbb{R}
$$

which is positive, $\sqrt{\rho} \gt 0$, as

$$
  \Psi 
    \coloneqq 
  \exp\left(\frac{i}{\hbar} S / \hbar\right) \sqrt{\rho}
  \,.
$$

Entering this Ansatz into the above Schr&#246;dinger equation, that [[complex number|complex]] equation becomes equivalent to the following two [[real number|real]] equations:

$$
  \frac{\partial}{\partial t} S
  = 
  - 
  \frac{1}{2m} \left(\frac{\partial}{\partial x}S\right)^2
  - 
  V
  + 
  \frac{\hbar^2}{2m} \frac{1}{\sqrt{\rho}}\frac{\partial^2}{\partial^2 x} \sqrt{\rho}
$$

and

$$
  \frac{\partial}{\partial t} \rho
  = 
  -
  \frac{\partial}{\partial x}
  \left(
    \frac{1}{m} \left(\frac{\partial}{\partial x}S\right) \rho
  \right)
  \,.
$$

Now in this form one may notice a similarity of the form of these two equations with other equations from [[classical mechanics]] and [[statistical mechanics]]:

1. The first equation is similar to the [[Hamilton-Jacobi equation]] that expresses the classical [[action functional]] $S$ and the [[canonical momentum]]

   $$
     p \coloneqq \frac{\partial}{\partial x} S
   $$

   except that in addition to the ordinary [[potential energy]] $V$ there is an additional term

   $$
    Q 
      \coloneq
    \frac{\hbar^2}{2m} \frac{1}{\sqrt{\rho}}\frac{\partial^2}{\partial^2 x} \sqrt{\rho}
   $$

   which is unlike what may appar in an ordinary [[Hamilton-Jacobi equation]]. The perspective of Bohmian mechanics is to regard this as a correction of [[quantum physics]] to classical [[Hamilton-Jacobi theory]], it is then called the _quantum potential_. Notice that unlike ordinary potentials, this "quantum potential" is a function of the density that is subject to the potential. (Notice that this works only away from the [[zero locus]] of $\rho$.)

1. The second equation has the form of the [[continuity equation]] of the [[flow]] expressed by $\frac{1}{m}p$.

(In the context of _[[Bohmian mechanics]]_ one regard this equivalent rewriting of the [[Schrödinger equation]] as providing a [[hidden variable theory]] formulation of [[quantum mechanics]].)





## Examples ##
...

## Related concepts

* [[Tomonaga-Schwinger equation]]

* [[Schrödinger picture]]


## References ##

Any introductory textbook about [[quantum mechanics]] will explain the Schr&#246;dinger equation (from the viewpoint of physicists mostly).

* Wikipedia: [Schr&#246;dinger equation] (http://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation)

[[!redirects Schrödinger's equation]]

[[!redirects Schroedinger equation]]
[[!redirects Schroedinger's equation]]
