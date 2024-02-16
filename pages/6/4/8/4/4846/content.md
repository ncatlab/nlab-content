
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
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _supergravity Lie 6-algebra_ ([D'Auria & Fré 1982, p. 18](#DauriaFre82)) is (with hindsight, following [FSS15](#FSS15)) a [[super L-∞ algebra]] such that [[L-infinity algebra valued differential forms|$L_\infty$-algebra valued differential forms]] (local [[connection on an ∞-bundle|∞-connections]]) with values in it encode [[field history|field histories]] of

1. the [[vielbein]] field with a [[spin connection]], 

   hence the [[first order formulation of gravity]] for a [[graviton]] field 

   in 10+1 dimensions;

1. the [[gravitino]] field;

1. the [[supergravity C-field]] 

   _and_ its [[electric-magnetic duality|magnetic dual]].

This is such that the [[field strengths]] and [[Bianchi identities]] of these fields are governed by certain fermionic [[L-∞ algebra cohomology|super L-∞ algebraic cocycles]] as suitable for [[11-dimensional supergravity]].


## Definition

> Our normalization conventions entirely follow [Castellani, D'Auria & Fré 1991, §III.8.3](#CastellaniDAuriaFre), but we denote the [[super-vielbein]] 1-forms by $\big\{e^a\big\}_{a=0}^{10}$ instead of by $\big\{V^a\big\}_{a=0}^{10}$.

+-- {: .num_prop #TheSevenCocycle}
###### Proposition

The [[supergravity Lie 3-algebra]] $\mathfrak{sugra}_3(10,1)$ carries an [[L-∞ algebra cohomology|L-∞ algebra cocycle]] $\mu_7 \in CE\big(\mathfrak{sugra}_3(10,1)\big)$ of degree 7, given in the standard generators $\{e^a\}$ ([[vielbein]]), $\{\omega^{a b}\}$ ([[spin connection]]) $\{\psi^\alpha\}$ ([[gravitino]]) and $\{c_3\}$ ([[supergravity C-field]]) by

$$
  \mu_7
   \;\coloneqq\;
   \frac{i}{2}\bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
   +
   15 \mu_4 \wedge c_3
  \,,
$$

where

$$
  \mu_4 
  \;=\; 
  \frac{1}{2} 
  \overline{\psi} 
    \Gamma^{a_1 a_2} 
  \psi \wedge e_{a_1} \wedge e_{a_2}
$$

is the 4-cocycle which defines $\mathfrak{sugra}_3(10,1)$ as an extension of $\mathbb{R}^{10,1\vert \mathbf{32}}$, and where $c_3$ is the generator that cancels the class of this cocycle, $d_{CE} c_3 \,=\, \mu_4$.

=--

In other words, we have

$$
  \begin{array}{l}
    \mathrm{d}
    \,
    \mu_4 \;=\; 0
    \\
    \mathrm{d}
    \,
    \mu_7
    \;=\;
    15\,
    \mu_4 \wedge \mu_4
    \mathrlap{\,.}
  \end{array}
$$

which has the same structure as the [[equations of motion]] of the [[field strength]] $G_4$ of the [[supergravity C-field]] and its [[Hodge dual]] $G_7 = \ast G_4$ in [[11-dimensional supergravity]] (to which it is related [below](#eq:SuperMaxwellEquation))

This appears (in the dual language of [[Chevalley-Eilenberg algebras]]) in [DAuria & FrFré 1982, page 18](#DAuriaFre) and 
[Castellani, D'Auria & Fré 1991, §III.8.3](#CastellaniDAuriaFre).

+-- {: .proof}
###### Proof

One computes

$$
  \begin{aligned}
    d_{{}_{CE}} \mu_7 
    \;=\;
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
  \Gamma^{a_1 \cdots a_4 b} \psi \wedge \bar \psi \wedge \Gamma_b \psi 
  \;=\; 
  3 \bar \psi \wedge \Gamma^{[a_1 a_2} \psi \wedge \bar \psi \wedge \Gamma^{a_3 a_4 ]} \psi
$$

and

$$
  \bar \psi \wedge \Gamma^{a b} \psi \wedge \bar \psi \wedge \Gamma_b \psi 
  \;=\; 0 
  \,.
$$

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
  \begin{array}{ccl}
  \omega^{a b} 
  &\mapsto& 
  \omega^{a c} \wedge \omega_c{}^b
  \\
  e^a 
    &\mapsto&
  -\omega^{a b} e_b  - \frac{1}{2}i \bar \psi \wedge  \Gamma^a \psi
  \\
  \psi &\mapsto& 
   - \frac{1}{4}\omega^{a b} \Gamma^{a b} 
  \\
  c_3 
  &\mapsto& 
  \frac{1}{2} \bar \psi \wedge \Gamma^{a b} \psi \wedge e_a \wedge e_b
  \\
  c_6 
  &\mapsto&
  - \frac{1}{2} \bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
  -
  \frac{13}{2} \bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2} \wedge c_3
  \,.
  \end{array}
$$


=--

This appears in [Castellani, D'Auria & Fré, (III.8.18)](#CastellaniDAuriaFre).

+-- {: .num_remark}
###### Remark

According to [Castellani, D'Auria & Fré 1991, comment below (III.8.18)](#CastellaniDAuriaFre): "no further extension is possible".

=--



## Relation to $D = 11$ supergravity
  {#RelationToSupergravity}

The supergravity Lie 6-algebra is something like the gauge $L_\infty$-algebra of [[11-dimensional supergravity]], in the sense discussed at _[[D'Auria-Fré formulation of supergravity]]_ .


\begin{definition}
\label{ModifiedWeilAlgebra}

Write $W\big(\mathfrak{sugra}_6(10,1)\big)$ for the [[Weil algebra]] of the supergravity Lie 6-algebra.

Write $g_4$ and $g_7$ for the shifted generators of the Weil algebra corresponding to $c_3$ and $c_6$, respectively.

Define an [[adjusted Weil algebra]] $\tilde W(\mathfrak{sugra}_6(10,1))$ by declaring it to have the same generators and differential as before, except that the differential for $c_6$ is modified to

$$
  d_{\tilde W} \, c_6 
    \coloneqq
  d_{W} \, c_6  
    + 
  15 \, g_4 \wedge c_3  
$$

and hence the differential of $g_7$ is accordingly modified in the unique way that ensures $d_{\tilde W}^2 = 0$ (yielding the modified [[Bianchi identity]] for $g_7$).

\end{definition}

This ansatz appears in [Castellani, D'Auria & Fré 1991 (III.8.24)](#CastellaniDAuriaFre).

Note that this amounts simply to a redefinition of [[curvatures]]

$$
  \tilde g_7 
    \;\coloneqq\; 
  g_7 + 15 g_4 \wedge c_3
  \,.
$$

\begin{proposition}
\label{SugraEOM}

A field configuration of [[11-dimensional supergravity]] is given by [[∞-groupoid of ∞-Lie algebra valued forms|L-∞ algebra valued differential forms]] with values in $\mathfrak{sugra}_6$. Among all of these the solutions to the equations of motion (the points in the [[covariant phase space]]) can be characterized as follows:

A field configuration

$$
  \Omega^\bullet(X) 
     \leftarrow 
  \tilde W(\mathfrak{sugra}_6)  
  \;\colon\; 
  \Phi
$$

solves the equations of motion precisely if

1. all [[curvatures]] sit in the ideal of differential forms spanned by the 1-form fields $E^a$ ([[vielbein]]) and $\Psi$ ([[gravitino]]); 

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

\end{proposition}

This is, in paraphrase, the content of [Castellani, D'Auria & Fré, section III.8.5](#CastellaniDAuriaFre).

\begin{remark}
\label{EOMOfSuperCField}

In particular, the [[Bianchi identity]] for the super-form enhancement of the [[supergravity C-field]] [[flux density]] is (by [III.8.23j, 34, 35, 36](#CastellaniDAuriaFre) and using hupf):

\[
  \label{SuperMaxwellEquation}
  \begin{array}{l}
  \mathrm{d}
  \big(
    \underset{
      G_7^{super}
    }{
      \underbrace{
        F_{a_1 \cdots a_4}
        e^{a_1} \wedge \cdots \wedge e^{a_4}
        \,+\,
        \mathrm{i}
        \overline{\psi} \Gamma_{a_1 \cdots a_5} \psi
        \,
        e^{a_1} \wedge \cdots \wedge e^{a_5}
      }
    }
  \big)
  \\
  \;=\;
  -15
  \big(
    \underset{G_4^{super}}{
    \underbrace{
      F_{a_1 \cdots a_4} 
      e^{a_1} \wedge \cdots \wedge e^{a_4}
      +
      \tfrac{1}{2}
      \overline{\psi}\Gamma_{a_1 a_2}\psi
      \,
      e^{a_1} \wedge e^{a_2}
    }
    }
  \big)
  \wedge
  \big(
    \underset{G_4^{super}}{
    \underbrace{
      F_{a_1 \cdots a_4} 
      e^{a_1} \wedge \cdots \wedge e^{a_4}
      +
      \tfrac{1}{2}
      \overline{\psi}\Gamma_{a_1 a_2}\psi
      \,
      e^{a_1} \wedge e^{a_2}
    }
    }
  \big)
  \mathrlap{\,}
  \end{array}
\]

and its rheonomic solution implies for the "actual" [[flux densities]] $F_4 \coloneqq F_{a_1 \cdots a_4} e^{a_1} \wedge \cdots \wedge e^{a_4}\vert_{\psi=0}$ and $G_4 \coloneqq  G_{a_1 \cdots a_7} e^{a_1} \wedge \cdots e^{a_7} \vert_{\psi = 0}$ that

1. the CJS [[higher gauge theory|higher]] [[Maxwell equation]] holds

   $$
     \mathrm{d}\, G_7 \;=\; - 15 \, F_4 \wedge F_4
   $$

   ([III.8.53](#CastellaniDAuriaFre))


1. the [[Hodge duality|Hodge duality]] holds

   $$
     G_7 \;=\; \star F_4
   $$

   ([III.8.52](#CastellaniDAuriaFre))

\end{remark}

## Related concepts

**supergravity Lie 6-algebra** $\to$ [[supergravity Lie 3-algebra]] $\to$ [[super Poincaré Lie algebra]]

* [[4d supergravity Lie 2-algebra]]

* [[type II supergravity Lie 2-algebra]]

* [[M-theory super Lie algebra]]

* [[adjusted Weil algebra]]


## References

The supergravity Lie 6-algebra originates in:

* {#DAuriaFre82} [[Riccardo D'Auria]], [[Pietro Fré]], p. 18 of: _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 &lbrack;<a href="https://doi.org/10.1016/0550-3213(82)90376-5">doi:10.1016/0550-3213(82)90376-5</a>,  [[GeometricSupergravityErrata.pdf:file]]&rbrack;

Brief review is in:

* {#CFGPN83} [[Leonardo Castellani]], [[Pietro Fré]], F. Giani, [[Krzysztof Pilch]], [[Peter van Nieuwenhuizen]], §4 of: *Gauging of $d = 11$ supergravity?*, Annals of Physics **146** 1 (1983) 35-77 &lbrack;[spire:11998](https://inspirehep.net/literature/11998), <a href="https://doi.org/10.1016/0003-4916(83)90052-0">doi:10.1016/0003-4916(83)90052-0</a>&rbrack;

* [[Pietro Fré]], [[Pietro Antonio Grassi]], §3 of: *Free Differential Algebras, Rheonomy, and Pure Spinors* &lbrack;[arXiv:0801.3076](http://arxiv.org/abs/0801.3076), [inspire:777785](https://inspirehep.net/literature/777785)&rbrack;

* [[Pietro Fré]], §6.4.1 in: *Gravity, a Geometrical Course*, Volume 2: *Black Holes, Cosmology and Introduction to Supergravity*, Springer (2013) &lbrack;[doi:10.1007/978-94-007-5443-0](https://doi.org/10.1007/978-94-007-5443-0)&rbrack;

A monograph account is in:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], vol 2, III.8.3 of: *[[Supergravity and Superstrings - A Geometric Perspective]]*, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), [epdf](https://epdf.pub/supergravity-and-superstrings-a-geometric-perspective-vol-2-supergravity.html), ch III.8: [[CastellaniDAuriaFre-ChIII8.pdf:file]]&rbrack;
 
It was (apparently) rediscovered in:  

* {#CAIB99} C. Chrysso‌malakos, [[José de Azcárraga]], [[José M. Izquierdo]], C. P&#233;rez Bueno, around equation (8.8) in: _The geometry of branes and extended superspaces_, Nucl. Phys. B **567** (2000) 293-330  &lbrack;[arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137), <a href="https://doi.org/10.1016/S0550-3213(99)00512-X">doi:10.1016/S0550-3213(99)00512-X</a>&rbrack;

where a detailed discussion is given.

These authors all consider the [[Chevalley-Eilenberg algebra]] ("FDA") of the actual [[super L-infinity algebra|super $L_\infty$-algebra]]. The latter and its relation to [[smooth super ∞-groupoids]] is considered in:

* {#FSS15} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, Int. J. Geom. Meth. Modern Physics **12** 02 (2015) 1550018 &lbrack;[arXiv:1308.5264](http://arxiv.org/abs/1308.5264), [doi:10.1142/S0219887815500188](http://www.worldscientific.com/doi/abs/10.1142/S0219887815500188)&rbrack;

* [[Urs Schreiber]], last section of: _[[schreiber:differential cohomology in a cohesive topos]]_


