
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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
   \coloneqq
   \frac{i}{2}\bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
   +
  15 \mu_4 \wedge c_3
  \,,
$$

where

$$
  \mu_4 = \frac{i}{2}\bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2}
$$

is the 4-cocycle which defines $\mathfrak{sugra}_3(10,1)$ as an extension of $\mathbb{R}^{10,1\vert \mathbf{32}}$m and where $c_3$ is the generator that cancels the class of this cocycle, $d_{CE} c_3 \propto \mu_4$.

=--

This appears in ([DAuria-Fre, page 18](#DAuriaFre)) and 
[Castellani-DAuria-Fre, III.8.3](#CastellaniDAuriaFre).

+-- {: .proof}
###### Proof

One computes

$$
  \begin{aligned}
    d_{CE} \mu_7 = 
    & 
     - \frac{5}{4} \bar \psi \wedge \Gamma^{a_1 \cdots a_4 b} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_4} \wedge \bar \psi \wedge \Gamma_b \psi
  \\
  & - i 15 \wedge \Gamma^{a b} e_a \wedge \bar \psi \wedge \Gamma_b \psi \wedge c_3
   \\
   & +
    \frac{15}{4} \bar \psi \wedge \Gamma_{a b} \psi \wedge e^a \wedge e^b \wedge \bar \psi \wedge \Gamma_{c d} \psi \wedge e^c \wedge e^d 
  \end{aligned}
  \,.
$$

This expression vanishes due to the [[Fierz identities]]

$$
  \bar \psi \wedge 
  \Gamma^{a_1 \cdots a_4 b} \psi \wedge \bar \psi \wedge \Gamma_b \psi = 
  3 \bar \psi \wedge \Gamma^{[a_1 a_2} \psi \wedge \bar \psi \wedge \Gamma^{a_3 a_4 ]} \psi
$$

and

$$
  \bar \psi \wedge \Gamma^{a b} \psi \wedge \bar \psi \wedge \Gamma_b \psi = 0 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Hence if we write

$$
  g_4 \coloneqq \mu_4 = \bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2}
$$

and

$$
  g_7 
  \coloneqq
  \bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
$$

then 

$$
  d g_7 \propto g_4 \wedge g_4
  \,.
$$

This is the structure of the [[equations of motion]] of the [[field strength]] $G_4$ of the [[supergravity C-field]] and its [[Hodge dual]] $G_7 = \ast G_4$ in [[11-dimensional supergravity]].

=--



+-- {: .num_def #TheDefinition}
###### Definition


The _supergravity Lie 6-algebra_ $\mathfrak{sugra}_{7}(10,1)$ is the [[super L-∞ algebra|super Lie 7-algebra]] that is the $b^6 \mathbb{R}$-[[L-∞ algebra cohomology|extension]] of $\mathfrak{sugra}_3(10,1)$ classified by the cocycle $\mu_7$ from def. \ref{TheSevenCocycle}.

$$
  b^5 \mathbb{R} \to \mathfrak{sugra}_6 \to \mathfrak{sugra}_3
  \,.
$$


=--


+-- {: .num_remark #InTermsOfGenerators}
###### Remark

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
   \colon
  c_6 
  \mapsto
  - \frac{1}{2} \bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
  -
  \frac{13}{2} \bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2} \wedge c_3
  \,.
$$


=--

This appears as ([Castellani-DAuria-Fre, (III.8.18)](#CastellaniDAuriaFre)).

+-- {: .num_remark}
###### Remark

According to ([Castellani-DAuria-Fre, comment below (III.8.18)](#CastellaniDAuriaFre)): "no further extension is possible".

=--



## Relation to $D = 11$ supergravity
  {#RelationToSupergravity}

The supergravity Lie 6-algebra is something like the gauge $L_\infty$-algebra of [[11-dimensional supergravity]], in the sense discussed at _[[D'Auria-Fre formulation of supergravity]]_ .

+-- {: .num_defn #ModifiedWeilAlgebra}
###### Definition

Write $W(\mathfrak{sugra}_6(10,1))$ for the [[Weil algebra]] of the supergravity Lie 6-algebra.

Write $g_4$ and $g_7$ for the shifted generators of the Weil algebra corresponding to $c_3$ and $c_6$, respectively.

Define a modified Weil algebra $\tilde W(\mathfrak{sugra}_6(10,1))$ by declaring it to have the same generators and differential as before, except that the differential for $c_6$ is modified to

$$
  d_{\tilde W} c_6 := d_{W} c_6  + 15 g_4 \wedge c_3  
$$

and hence the differential of $g_7$ is accordingly modified in the unique way that ensures $d_{\tilde W}^2 = 0$ (yielding the modified [[Bianchi identity]] for $g_7$).

=--

This ansatz appears as ([CastellaniDAuriaFre, (III.8.24)](#CastellaniDAuriaFre)).

Note that this amounts simply to a redefinition of [[curvature]]s

$$
  \tilde g_7 := g_7 + 15 g_4 \wedge c_3
  \,.
$$

+-- {: .num_note #SugraEOM}
###### Claim

A field configuration of [[11-dimensional supergravity]] is given by [[∞-groupoid of ∞-Lie algebra valued forms|L-∞ algebra valued differential forms]] with values in $\mathfrak{sugra}_6$. Among all of these the solutions to the equations of motion (the points in the [[covariant phase space]]) can be characterized as follows:

A field configuration

$$
  \Omega^\bullet(X) \leftarrow \tilde W(\mathfrak{sugra}_6) : \Phi
$$

solves the equations of motion precisely if

1. all [[curvature]]s sit in the ideal of differential forms spanned by the 1-form fields $E^a$ ([[vielbein]]) and $\Psi$ ([[gravitino]]); 

   more precisely if we have

   * $\tau = 0$ 
 
     (super-[[torsion]]);

   * $G_4 = (G_4)_{a_1, \cdots a_4} E^{a_1} \wedge \cdots E^{a_4}$ 

     ([[field strength]] of [[supergravity C-field]])

   * $G_7 = (G_7)_{a_1, \cdots a_7} E^{a_1} \wedge \cdots E^{a_7}$

     ([[electric-magnetic duality|dual]] field strength)
  
   * $\rho = \rho_{a b} E^a \wedge E^b  + H_a \Psi \wedge E^a$

     ([[Dirac operator]] applied to [[gravitino]])

   * $R^{a b} = R^{a b}_{c d} E^c \wedge E^d + \bar \Theta^{a b}{}_c \Psi \wedge E^c + \bar \Psi \wedge K^{a b} \Psi$

     ([[Riemann tensor]]: [[field strength]] of [[gravity]])

1. such that the coefficients of terms containing $\Psi$s are polynomials in the coefficients of the terms containing no $\Psi$s. ("rheonomy").

=--

This is the content of ([CastellaniDAuriaFre, section III.8.5](#CastellaniDAuriaFre)).

In particular this implies that on-shell the 4- and 7-field strength are indeed dual of each other

$$
  G_7 \propto \star G_4
  \,.
$$

This is the content of ([CastellaniDAuriaFre, equation (III.8.52)](#CastellaniDAuriaFre)).

## Related concepts

**supergravity Lie 6-algebra** $\to$ [[supergravity Lie 3-algebra]] $\to$ [[super Poincaré Lie algebra]]

* [[4d supergravity Lie 2-algebra]]

* [[type II supergravity Lie 2-algebra]]

* [[M-theory super Lie algebra]]

## References

The supergravity Lie 6-algebra appears first on page 18 of

* {#DAuriaFre}  [[Riccardo D'Auria]], [[Pietro Fré]]; _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140
 

and is recalled in section 4 of

* {#CFGPN83} [[Leonardo Castellani]], [[Pietro Fré]], F. Giani, K. Pilch, [[Peter van Nieuwenhuizen]], _Gauging of $d = 11$ supergravity?_, Annals of Physics
Volume 146, Issue 1, March 1983, Pages 35&#8211;77


A textbook discussion is in section III.8.3 of 

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], 

  _[[Supergravity and Superstrings - A Geometric Perspective]]_
 

The same is being recalled for instance in section 3 of

* [[Pietro Fré]], Pietro Antonio Grassi, _Free Differential Algebras, Rheonomy, and Pure Spinors_ ([arXiv:0801.3076](http://arxiv.org/abs/0801.3076))

Then it is rediscovered around equation (8.8) in 

* {#CAIB99} C. Chrysso&#8204;malakos, [[José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_ ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))
 

which gives a detailed and comprehensive discussion.

A discussion in the context of [[smooth super ∞-groupoids]] is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_


in the last section of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_