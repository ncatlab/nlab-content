
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents goes here
{:toc}

## Idea

The _Poincar&#233; Lie algebra_ $\mathfrak{iso}(d-1,1)$ is the [[semidirect product]] of the [[special orthogonal Lie algebra]] $\mathfrak{so}(d-1,1)$ and the abelian translation Lie algebra $\mathbb{R}^{d-1,1}$. 

The corresponding [[Lie group]] is the [[Poincaré group]].

## Definition

### The CE-algebra

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{iso}(d-1,1))$ is generated from $\mathbb{R}^{d,1}$ and $\wedge^2 \mathbb{R}^{d,1}$. For $\{t_a\}$ the standard basis of $\mathbb{R}^{d-1,1}$ we write $\{\omega^{a b}\}$ and $\{e^a\}$ for these generators. With $(\eta_{a b})$ the components of the [[Minkowski metric]] we write

$$
  \omega^{a}{}_b := \omega^{a c}\eta_{c b}
  \,.
$$

In terms of this the CE-differential that defines the Lie algebra structure is

$$
  d_{CE} : \omega^{a b} = \omega^a{}_c \wedge \omega^{c b}
$$

$$
  d_{CE} : e^a \mapsto \omega^{a}{}_b  \wedge t^b
$$


## Properties

### Cohomology

We discuss some elements in the [[Lie algebra cohomology]] of $\mathfrak{iso}(d-1,1)$.

The canonical degree-3 $\mathfrak{so}(d-1,1)$-cocycle is

$$
  \omega^a{}_b \wedge \omega^b{}_c \wedge \omega^c{}_a
  \in 
  CE(\mathfrak{iso}(d-1,1))
  \,.
$$

The _volume cocycle_ is 

$$
  vol = \epsilon_{a_1 \cdots a_{d}} e^{a_1} \wedge \cdots \wedge e^{a_d} \in CE(\mathfrak{iso}(d-1,1))
  \,.
$$
{#VolumeCocycle}

### Invariant polynomials and Chern-Simons elements

With the basis elements $(e^a, \omega^{a b})$ as above, denote the shifted generators of the [[Weil algebra]] $W(\mathfrak{iso}(d-1,1))$ by $\theta^a$ and $r^{a b}$, respectively.

We have the [[Bianchi identity]]

$$
  d_W : r^{a b} 
   \mapsto
   \omega^{a c} \wedge R_c{}^d
   - 
   R^{a c} \wedge \omega_c{}^b
$$

and

$$
  d_W : \theta^a 
   \mapsto
    \omega^a{}_b \theta^b
    - 
    R^{a}{}_b e^b
   \,.
$$


The element $\eta_{a b} \theta^a \wedge \theta^b \in W(\mathfrak{iso}(d-1,1))$ is an [[invariant polynomial]]. A [[Chern-Simons element]] for it is $cs = \eta_{a b} e^a \wedge \theta^b$. So this transgresses to the trivial cocycle.

Another invariant polynomial is $r^{a b} \wedge r_{a b}$. This is the [[Killing form]] of $\mathfrak{so}(d-1,1)$. Accordingly, it transgresses to a multiple of $\omega^a{}_b \wedge \omega^b{}_c \wedge \omega^c{}_a$.

This is the first in an infinite series of Pontryagin invariant polynomials

$$
  P_n 
  :=
  r^{a_1}{}_{a_2} \wedge r^{a_2}{}_{a_3}
  \wedge \cdots \wedge r^{a_n}{}_{a_1}
  \,.
$$

There is also an infinite series of mixed invariant polynomials

$$
  C_{2n + 2}
  :=
  \theta_{a_1} \wedge r^{a_1}{}_{a_2} \wedge r^{a_2}{}_{a_3}
  \wedge \cdots \wedge r^{a_{n-1}}{}_{a_n} \wedge \theta^{a_n}
  \,.
$$

[[Chern-Simons element]]s for these are

$$
  B_{2n + 1}
  :=
  \theta_{a_1} \wedge r^{a_1}{}_{a_2} \wedge r^{a_2}{}_{a_3}
  \wedge \cdots \wedge r^{a_{n-1}}{}_{a_n} \wedge e^{a_n}
  \,.
$$



### Lie algebra valued forms

A [[Lie algebra-valued form]] with values in $\mathfrak{iso}(d-1,1)$

$$
  \Omega^\bullet(X) \leftarrow W(\mathfrak{iso}(d-1,1)) : (E,\Omega)
$$

is

* a [[vielbein]] $E$ on $X$;

* a "[[spin connection]]" $\Omega$ on $X$.

The [[curvature]] 2-form $(T, R)$ consists of

* the [[torsion]] $T$;

* the ordinary curvature 2-form $R$.

If the torsion vanishes, then $\Omega$ is a [[Levi-Civita connection]] for the [[metric]] $E^a \otimes E^b \eta_{a b}$ defined by $E$.

The volume form is the image of the [volume cocycle](#VolumeCocycle) 

$$
  \Omega^\bullet(X)
  \stackrel{(E,\Omega)}{\leftarrow}
  W(\mathfrak{iso}(d-1,1))
  \stackrel{vol}{\leftarrow}
  W(b^{d-1} \mathbb{R})
  :
  vol(E)
  \,.
$$

We have

$$
  vol(E) = \epsilon_{a_1 \cdots a_d} E^{a_1} \wedge \cdots \wedge E^{a_d}
  \,.
$$

If the torsion vanishes, this is indeed a closed form.

## Related structures

* [[special orthogonal Lie algebra]]

* [[super Poincaré Lie algebra]]



[[!redirects Poincare Lie algebra]]
[[!redirects Poincaré Lie algebra]]
