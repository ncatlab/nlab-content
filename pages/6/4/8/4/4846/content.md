
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
* table of contents
{:toc}

## Idea

The _supergravity Lie 6-algebra_ is a [[super L-∞ algebra]] such that [[connection on an ∞-bundle|∞-connections]] with values in it encode

* a [[vielbein]] field and a [[spin connection]], hence the [[first order formulation of gravity]] for a [[graviton]] field in 11-[[dimension]]s;

* a [[gravitino]] field;

* the [[supergravity C-field]] in degree 3 _and_ its [[electric-magnetic duality|magnetic dual]].

This is such that the [[field strength]]s and [[Bianchi identities]] of these fields are governed by certain fermionic [[L-∞ algebra cohomology|super L-∞ algebraic cocycles]] as suitable for [[11-dimensional supergravity]].

## Definition

+-- {: .num_prop #TheSevenCocycle}
###### Proposition

The [[supergravity Lie 3-algebra]] $\mathfrak{sugra}_3(10,1)$ carries an [[L-∞ algebra cohomology|L-∞ algebra cocycle]] $\mu_7 \in CE(\mathfrak{sugra}_3(10,1))$ of degree 7, given in the standard generators $\{e^a\}$ ([[vielbein]]), $\{\omega^{a b}\}$ ([[spin connection]]) $\{\psi^\alpha\}$ ([[gravitino]]) and $\{c_3\}$ ([[supergravity C-field]]) by

$$
  \mu_7
   := 
  - \frac{1}{2} \bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
  -
  \frac{13}{2} \bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2} \wedge c_3
  \,.
$$

=--

This appears on page 18 of ([DAuriaFre](#DAuriaFre)).

+-- {: .num_def #TheDefinition}
###### Definition


The _supergravity Lie 6-algebra_ $\mathfrak{sugra}_{7}(10,1)$ is the [[super L-∞ algebra|super Lie 7-algebra]] that is the $b^6 \mathbb{R}$-[[L-∞ algebra cohomology|extension]] of $\mathfrak{sugra}_3(10,1)$ classified by the cocycle $\mu_7$ from def. \ref{TheSevenCocycle}.

$$
  b^5 \mathbb{R} \to \mathfrak{sugra}_6 \to \mathfrak{sugra}_3
  \,.
$$


=--


+-- {: .num_note #InTermsOfGenerators}
###### Note


This means that the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{sugra}_6)$ is generated from 

* $\{e^a\}$ ([[vielbein]]) in degree $(1,even)$

* $\{\omega^{a b}\}$ ([[spin connection]]) in degree $(1,even)$;

* $\{\psi^\alpha\}$ ([[gravitino]]) in degree $(1,odd)$ 

* $\{c_3\}$ ([[supergravity C-field]]) in degree $(3,even)$

* $\{c_6\}$ (magnetic dual [[supergravity C-field]]) in degree $(6,even)$

with [[differential]] defined by

$$
  d_{CE}  : \omega^{a b} \mapsto \omega^{a c} \wedge \omega_c{}^b
$$

$$
  d_{CE} : e^a = -\omega^{a b} e_b  - \frac{1}{2}i \bar \psi \wedge  \Gamma^a \psi
$$

$$
  d_{CE} : \psi \mapsto - \frac{1}{4}\omega^{a b} \Gamma^{a b} 
$$

$$
  d_{CE} : c_3 \mapsto \frac{1}{2} \bar \psi \wedge \Gamma^{a b} \psi \wedge e_a \wedge e_b
$$

$$
  d_{CE} 
   : 
  c_6 
  \mapsto
  - \frac{1}{2} \bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
  -
  \frac{13}{2} \bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2} \wedge c_3
  \,.
$$


=--


## Applications

The maximal 11-dimensional [[supergravity]] is [[schreiber:∞-Chern-Simons theory]] for a degree 11 [[Chern-Simons element]] in $\mathfrak{sugra}_6$.
See [[D'Auria-Fre formulation of supergravity]] for details.

## Related concepts

**supergravity Lie 6-algebra** $\to$ [[supergravity Lie 3-algebra]] $\to$ [[super Poincaré Lie algebra]]


## References

The supergravity Lie 6-algebra appears first on page 18 of

* R. D'Auria, P. Fr&#233; _[[GeometricSupergravity.pdf:file]]_
{#DAuriaFre} 

A textbook discussion is in section III.8.3 of 

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], 

  _[[Supergravity and Superstrings - A Geometric Perspective]]_
{#CastellaniDAuriaFrre}
