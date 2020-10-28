
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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

What is known as _Born-Infeld theory_ ([Born-Infeld 34](#BornInfeld34), often also attributed to [Dirac 62](#Dirac62) and abbreviated "DBI theory") is a [[deformation]] of  the [[theory (physics)|theory]] of [[electromagnetism]] which coincides with ordinary [[electromagnetism]] for small excitations of the [[electromagnetic field]] but is such that there is a maximal value for the [[field strength]] which can never be reached in a physical process.

Just this theory happens to describe the [[Chan-Paton gauge field]] on single [[D-branes]] at low [[energy]], as deduced from [[open string|open]] [[string scattering amplitudes]] ([Fradkin-Tseytlin 85](#FradkinTseytlin85), [Abouelsaood-Callan-Nappi-Yost 87](#AbouelsaoodCallanNappiYost87), [Leigh 89](#Leigh89)).

In this context the [[action functional]] corresponding to Born-Infeld theory arises as the low-energy [[effective action]] on the [[D-branes]], and this is referred to as the _DBI-action_. This is part of the full [[Green-Schwarz action functional]] for super [[D-branes]], being a deformation of the [[Nambu-Goto action]]-summand by the [[field strength]] of the [[Chan-Paton gauge fields]].

On [[intersecting brane|coincident]] [[D-branes]], where one expects [[gauge enhancement]] of the [[Chan-Paton gauge field]] to a [[non-abelian group|non-abelian]] [[gauge group]], a further generalization of the DBI-action to non-abelian [[gauge fields]] is expected to be an analogous [[deformation]] of that of non-abelian [[Yang-Mills theory]].
A widely used proposal is due to [Tseytlin 97](#Tseytlin97), [Myers 99](#Myers99), but a derivation from [[string theory]] of this non-abelian DBI action is lacking; and it is in fact known to be in conflict, beyond the first few orders of correction terms, with effects argued elsewhere in the string theory literature ([Hashimoto-Taylor 97](#HashimotoTaylor97), [Bain 99](#Bain99), [Bergshoeff-Bilal-Roo-Sevrin 01](#BergshoeffBilalRooSevrin01)). The issue remains open.

When the [[D-branes]] in question are interpreted as [[flavor branes]], then the maximal/critical value of the [[electric field]] which arises from the [[DBI-action]] has been argued ([Semenoff-Zarembo 11](#SemenoffZarembo11)) to reflect, via [[holographic QCD]], the [[Schwinger limit]] beyond which the [[vacuum polarization]] caused by the [[electromagnetic field]] leads to [[deconfinement]] of [[quarks]].


## Definition
 {#Definition}

### On $4$-dimensional Minkowski spacetime
  {#On4dMinkowski}

In the simplest situation of flat 4-dimensional [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ and no other [[field (physics)|fields]] besides that of [[electromagnetism]], encoded in a [[Faraday tensor]] [[differential 2-form]]

$$
  F \;=\; F_{a b} d x^a \wedge d x^b
$$

the [[Lagrangian density]] of the Born-Infeld [[action functional]] is

\[
  \label{PlainMinkowskiDBIAction}
  \mathbf{L}_{BI}
  \;=\;
  \sqrt{ 
    - 
    det
    \big( 
      (\eta_{\mu\nu}) 
      + 
      \tfrac{1}{T}
      (F_{\mu\nu})
    \big) 
  } 
  \, dvol
  \,.
\]

Here 

* $\eta$ denotes the [[metric tensor]] of [[Minkowski spacetime]], regarded as a $4 \times 4$ [[matrix]]

  $$
    \eta \;=\; (\eta_{a b}) \;=\; diag(-1,1,1,1)
    \,,
  $$

* $F$ is the [[Faraday tensor]], regarded as a $4 \times 4$ [[matrix]]

  $$
    F = (F_{a b})
    \,,
  $$

* $T = \frac{1}{2\pi \, \alpha'} = \frac{1}{2\pi \, \ell_2^2}$ is the [[string tension]],

* $det(\cdots)$ denotes the [[determinant]] of the [[sum]] of these [[matrices]],

* $\sqrt{}$ denotes the [[positive number|positive]] [[square root]],

* $dvol$ denotes a [[volume form]] on [[Minkowski spacetime]], which after a choice of global [[coordinates]] may be taken to be

  \[
    \label{VolumeForm}
    dvol \;=\; d t \wedge d x^1 \wedge d x^2 \wedge d x^3
  \]

In the following, for $\omega_4$ any [[differential 4-form]] on $\mathbb{R}^{3,1}$ we write $\omega_4 / dvol$ for the unique [[smooth function]] $\mathbb{R}^{3,1} \to \mathbb{R}$ such that

$$
  (\omega_4 / dvol) \cdot dvol \;=\; \omega_4
  \,.
$$


+-- {: .num_lemma}
###### Lemma

The [[determinant]] in (eq:PlainMinkowskiDBIAction) evaluates to

\[
  \label{TheDeterminant}
  det( \eta + F )
  \;=\;
  - 1 
  -  
 \tfrac{1}{2} 
 \underset{
   \mathclap{
   {\color{blue}\text{Lagrangian of}}
   \atop
   {\color{blue}\text{electromagnetism}}   
   }
 }{
   \underbrace{
     (F \wedge \star F) 
  }
  }
  / dvol 
  +
    \underset{
      {\color{blue}\text{correction}}
      \atop
      {\color{blue}\text{term}}
    }{
    \underbrace{
      \big( 
        \tfrac{1}{2}
        (F\wedge F) 
        / \mathrm{dvol} 
      \big)^2
    }
    }
  \,,
\]

where 

* $F \wedge \star F$ is the 4-form [[wedge product]] of $F$ with its  [[Hodge duality|Hodge dual]], hence is the [[Lagrangian density]] of ordinary [[electromagnetism]],

* $F \wedge F$ is the [[wedge product]] of $F$ with itself.

=--

+-- {: .proof} 
###### Proof 

We compute as follows:

$$
  \begin{aligned}
  \mathrm{det}
  \big( 
    (\eta_{a b})
    +
    (F_{a b})
  \big)
  & 
  \; = \phantom{+}
  \tfrac{1}{4!}
  \epsilon^{a_1 a_2 a_3 a_4}
  (\eta_{a_1 b_1} + F_{a_1 b_1})  
  (\eta_{a_2 b_2} + F_{a_2 b_2})
  (\eta_{a_3 b_3} + F_{a_3 b_3})
  (\eta_{a_4 b_4} + F_{a_4 b_4})
  \epsilon^{b_1 b_2 b_3 b_4}
  \\
  &
  \; = \phantom{+}
  \underset{
    = \mathrm{det}(\eta) = -1
  }{
  \underbrace{
  \tfrac{1}{4!}
  \epsilon^{a_1 a_2 a_3 a_4}
  \eta_{a_1 b_1}
  \eta_{a_2 b_2}
  \eta_{a_3 b_3}
  \eta_{a_4 b_4}
  \epsilon^{b_1 b_2 b_3 b_4}
  }
  }
  \\
  &
  \phantom{\; =} +
  \underset{
    = 0
  }{
  \underbrace{
  \tfrac{3}{4!}
  \epsilon^{a_1 a_2 a_3 a_4}
  \eta_{a_1 b_1}
  \eta_{a_2 b_2}
  \eta_{a_3 b_3}
  F_{a_4 b_4}
  \epsilon^{b_1 b_2 b_3 b_4}
  }
  }
  \\
  &
  \phantom{\; =} +
  \underset{
    = -\tfrac{2\cdot 6}{4!} F_{a b} F^{a b}
  }{
  \underbrace{
  \tfrac{6}{4!}
  \epsilon^{a_1 a_2 a_3 a_4}
  \eta_{a_1 b_1}
  \eta_{a_2 b_2}
  F_{a_3 b_3}
  F_{a_4 b_4}
  \epsilon^{b_1 b_2 b_3 b_4}
  }
  }
  \\
  &
  \phantom{\; =} +
  \underset{
    = 0
  }{
  \underbrace{
  \tfrac{3}{4!}
  \epsilon^{a_1 a_2 a_3 a_4}
  \eta_{a_1 b_1}
  F_{a_2 b_2}
  F_{a_3 b_3}
  F_{a_4 b_4}
  \epsilon^{b_1 b_2 b_3 b_4}
  }
  }
  \\
  &
  \phantom{\; =} +
  \underset{
    = 
    \big(  
      \tfrac{1}{2}
      (F \wedge F) / \mathrm{dvol} 
    \big)^2
  }{
  \underbrace{
  \tfrac{1}{4!}
  \epsilon^{a_1 a_2 a_3 a_4}
  F_{a_1 b_1}
  F_{a_2 b_2}
  F_{a_3 b_3}
  F_{a_4 b_4}
  \epsilon^{b_1 b_2 b_3 b_4}
  }
  }
  \\
  & \; = \phantom{+}
  -1 
    - 
  \tfrac{1}{2} (F \wedge \star F) / \mathrm{dvol}
    +
  \big( 
    \tfrac{1}{2} (F\wedge F) / \mathrm{dvol}
  \big)^2
  \end{aligned}
$$

In the first line we used the expression of the [[determinant]] via the [[Levi-Civita symbol]] ([here](determinant#eq:DeterminantInTermsOfLCSymbols)) with the [[Einstein summation convention]] being understood throughout.
Then we multiplied out the terms, collecting those with the same number of factors of $\eta$ (of $F$), using that under exchange of the order of factors both [[Levi-Civita symbols]] give a sign, which hence cancel. Of the five terms that appear, the first and the last are themselves the plain [[determinants]] of $\eta$ and of $F$, respectively (again by [that formula](determinant#eq:DeterminantInTermsOfLCSymbols)).

We discuss the identifications of the resulting four summands shown under the braces:

* (first summand) The determinant of $\eta$ equals -1 by definition.

* (second summand) If we exchange indices $(a_i \leftrightarrow b_i)$ the form of this summand remains unchanged, also the factors $\eta_{a_i b_i}$ do not change, since $\eta$ is a [[symmetric matrix]], by definition. But the single factor of $F$ changes by a sign, since the components of a [[differential 2-form]] constitute a [[skew-symmetric matrix]]. In summary this says that the second term is equal to minus itself, and hence has to be [[zero]].

* (third summand) Consider this term first with $\eta$ relaced by the [[identity matrix]] (to be indicated by a [[Kronecker delta]] $(\delta_{a b})$). Observe then that the contraction not involving any factor of $F$ yields

  $$
    \epsilon^{a_1 a_2 a_3 a_4} 
      \delta_{a_1 b_1} \delta_{a_2 b_2}
    \epsilon^{b_1 b_2 b_3 b_4}
    \;=\;
    2 \delta^{a_3 a_4}_{b_3 b_4}
    \,,
  $$

  where the symbol on the right is defined to be

  \[
    \label{TheRelativeLCTensor}
    \delta^{a_3 a_4}_{b_3 b_4}
    \;\coloneqq\;
    \left\lbrace
    \array{
      +1 &\vert& a_3 \neq a_4 \;\text{and}\; a_3 = b_3 \;\text{and}\; a_4 = b_4
      \\
      -1 &\vert& a_3 \neq a_4 \;\text{and}\; a_3 = b_4 \;\text{and}\; a_4 = b_3
      \\
      \phantom{+}0 &\vert& \text{otherwise}      
    }
    \right.
  \]

  Hence the full expression (with $\eta$ still replaced by $\delta$) is

  $$
    \tfrac{2\cdot 2}{4!} 
    \delta^{a_3 a_4}_{b_3 b_4} 
    F_{a_3 b_3} F_{a_4 b_4}
    \;=\;
    - \sum_{a, b} F_{a b} F_{a b}
  $$

  where we used that due to the [[skew-symmetric matrix|skew-symmetry]] of $F$ the first case in (eq:TheRelativeLCTensor) does not contribute, only the second case does.

  Now it just remains to translate this back to the situation at hand where we use $\eta$ instead of $\delta$: This just differs by a minus sign in the component with both indices corresponding to the temporal direction, while this is also the case for which raising an index on $F$ picks up a minus sign. Since _either_ of these cases contributes in each summand, there is a global minus sign.

 
* (fourth summand) Since this involves three factors of $F$ which jointly pick up one minus sign when the indices on each of them are exchanged simultaneously, this vanishes by the same kind of skew-symmetry argument as for the second term.

* (fifth summand) Since this is the [[determinant]] of a [[skew-symmetric matrix]], the [[Pfaffian]]-theorem ([here](Pfaffian#eq:DeterminantIsPfaffianSquared)) says that this term equals the square of the [[Pfaffian]] of $F$, which is (by [this](Pfaffian#eq:PfaffianInTermsOfLCTensor) formula)

  $$
    Pf(F)
    \;=\;
    \tfrac{1}{4 \cdot 4!}
    \epsilon^{a_1 b_1 a_2 b_2} F_{a_1 b_1} F_{a_2 b_2}
  $$

  This is proportial to the coefficient of the [[wedge product]]
  of $F$ with itself, relative to the [[volume form]]:

  $$
    \begin{aligned}
      F \wedge F
      & = \;
      \big(
        \tfrac{1}{2}F_{a_1 b_1} d x^{a_1} \wedge d x^{b_1}
      \big)
      \wedge
      \big(
        \tfrac{1}{2}F_{a_2 b_2} d x^{a_2} \wedge d x^{b_2}
      \big)
      \\
      & = \;
      \tfrac{1}{4} F_{a_1 b_1} F_{a_2 b_2} d x^{a_1} \wedge d x^{b_1} \wedge d x^{a_2} \wedge d x^{b_2}
      \\
      & = \;
      \tfrac{1}{4} F_{a_1 b_1} F_{a_2 b_2} 
      \epsilon^{a_1 b_1 a_2 b_2}
      \,
      dvol   
      \\
      & = 
      4! Pf(F)
      \,
      dvol   
    \end{aligned}
  $$

=--

The expression (eq:PlainMinkowskiDBIAction) is supposed to be exact for [[constant function|constant]] [[field strength]] (e..g. [Bachas-Bain-Green 99, above (1.9)](#BachasBainGreen99)), and to pick up [[higher curvature corrections]] for non-constant field strength. The first derivative correction to (eq:PlainMinkowskiDBIAction) is supposed to arise at order $(\partial F)^4$. The explicit expression is given in [Garousi 15 (7)](#Garousi15) (argued there by appealing to [[T-duality]] and [[S-duality]] applied to earlier results on higher curvature corrections in other fields involved).

\linebreak


Consider now the [[Faraday tensor]] $F$ expressed in terms of the [[electric field]] $\vec E$ and [[magnetic field]] $\vec B$ as

$$
  \begin{aligned}
    F_{0 i} & = \phantom{+} E_i
    \\
    F_{i 0} & = - E_i
    \\
    F_{i j} & = \epsilon_{i j k} B^k
  \end{aligned}
$$

Then the general expression (eq:TheDeterminant) for the [[DBI-Lagrangian]] reduces to ([Born-Infeld 34, p. 437](#BornInfeld34), review in [Gibbons 97, (56)](#Gibbons97), [Savvidy 99, (22)](#Savvidy99), [Nastase 15, 9.4](#Nastase15)):

\[
  \label{InTermsOfElectricAndMagneticField}
  \mathbf{L}_{BI}
  \;=\;
  \sqrt{
    - det\left( \eta + \tfrac{1}{T} F \right)
  }
  \,
  dvol_4
  \;=\;
  \sqrt{
    1 
    -
    \tfrac{1}{T^2}
    ( 
    \vec E \cdot \vec E 
      - 
    \vec B \cdot \vec B 
    )
    - 
    \tfrac{1}{T^4}
    (\vec B \cdot \vec E)^2
  }
  \,
  dvol_4
\]

### Critical field strength
  {#CriticalFieldStrength}

For the DBI-action (eq:InTermsOfElectricAndMagneticField) to be well-defined, in that the [[square root]] is a [[real number]], hence its argument a non-[[negative number]], requires that

$$
  \begin{aligned}
    &
    -
    \mathrm{det}
    \big(
      (\eta_{\mu \nu})
      +
      \tfrac{1}{T}
      (F_{\mu \nu})
    \big)
    \geq  0
    \\
    & \Leftrightarrow
    \;
  1
  \;-\;
  \tfrac{1}{T^2}
  (E \cdot E - B \cdot B)
  \;-\;
  \tfrac{1}{T^4}
  (B \cdot E)^2
  \;\geq\;
  0
  \\
  & \Leftrightarrow
  \;
  \tfrac{1}{T^2}
  E^2 
  -
  \tfrac{1}{T^2} 
  B^2 
  +
  \tfrac{1}{T^4} 
  E^2 B_{\parallel}^2
  \;\leq 1\;
  \\
  & \Leftrightarrow
  \;
  \tfrac{1}{T^2}
  E^2
  \;\leq\;
  \frac{
    1 + \tfrac{1}{T^2} B^2
  }{
    1 + \tfrac{1}{T^2} B_{\parallel}^2
  }
  \\
  & \Leftrightarrow
  \;
  E
  \;\leq\;
  T
  \sqrt{
  \frac{
    T^2 + B^2
  }{
    T^2 + B_{\parallel}^2
  }
  }
  \end{aligned}
$$

where 

$$
  B_{\parallel} \coloneqq  \tfrac{1}{\sqrt{E\cdot E}} B \cdot E
$$

is the component of the [[magnetic field]] which is parallel to the [[electric field]].

The resulting maximal electric field strength

$$
  E_{crit}
  \;\coloneqq\;
  T
  \sqrt{
    \frac{
      T^2 + B^2
    }{
      T^2 + B_{\parallel}^2
    }
  }
$$

turns out to be the [[Schwinger limit]] (see [there](Schwinger+effect#CriticalFieldStrength)) beyond which the electric field would cause [[deconfinement|deconfining]] [[quark]]-pair creation ([Hashimoto-Oka-Sonoda 14b, (2.17)](#HashimotoOkaSonoda14b)). 



## Related concepts

* [[Myers effect]]

## References

### General

As a proposal for a modification of [[electromagnetism]] in [[spacetime]], the (Dirac-)Born-Infeld (DBI) action originates in

* {#BornInfeld34} [[Max Born]], [[Leopold Infeld]], _Foundations of the New Field Theory_,  Proceedings of the Royal Society of London. Series A, Containing Papers of a Mathematical and Physical Character, Vol. 144, No. 852 (Mar. 29, 1934), pp. 425-451 ([jstor:2935568](https://www.jstor.org/stable/2935568))

The article by Dirac which came to be commonly cited in this context is

* {#Dirac62} [[Paul Dirac]], _An Extensible Model of the Electron_, Proc. Roy. Soc. A268, (1962) 57-67 ([jstor:2414316](https://www.jstor.org/stable/2414316))

  (which proposes a [[membrane]]-model as a unification of the [[electron]] and the [[muon]])


### For single (abelian) D-branes

As the low energy [[action functional]] for single [[D-branes]] the DBI action is due to

* {#FradkinTseytlin85} [[Efim Fradkin]], [[Arkady Tseytlin]], _Non-linear electrodynamics from quantized strings_, Physics Letters B Volume 163, Issues 1–4, 21 November 1985 (<a href="https://doi.org/10.1016/0370-2693(85)90205-9">doi:10.1016/0370-2693(85)90205-9</a>)

* {#AbouelsaoodCallanNappiYost87} A. Abouelsaood, [[Curtis Callan]], [[Chiara Nappi]], S. A. Yost, _Open strings in background gauge fields_, Nuclear Physics B Volume 280, 1987, Pages 599-624 (<a href="https://doi.org/10.1016/0550-3213(87)90164-7">doi:10.1016/0550-3213(87)90164-7</a>)

* {#Leigh89} [[Robert Leigh]], _Dirac-Born-Infeld Action from Dirichlet Sigma Model_, Mod. Phys. Lett. A4 (1989) 2767 ([spire:26399](http://inspirehep.net/record/26399), [doi:10.1142/S0217732389003099](https://doi.org/10.1142/S0217732389003099))

and a full $\kappa$-symmetric [[Green-Schwarz sigma-model]] for [[D-branes]]:

* {#CGNSW96} [[Martin Cederwall]], Alexander von Gussich, [[Bengt Nilsson]], Per Sundell, Anders Westerberg, _The Dirichlet Super-p-Branes in Ten-Dimensional Type IIA and IIB Supergravity_, Nucl.Phys. B490 (1997) 179-201 ([arXiv:hep-th/9611159](http://arxiv.org/abs/hep-th/9611159))

* {#APPS97b} [[Mina Aganagic]], Jaemo Park, Costin Popescu, [[John Schwarz]], _Dual D-Brane Actions_, Nucl. Phys. B496 (1997) 215-230 ([arXiv:hep-th/9702133](https://arxiv.org/abs/hep-th/9702133))

Review:

* {#Gibbons97} [[Gary Gibbons]], _Born-Infeld particles and Dirichlet p-branes_, Nucl. Phys. B514:603-639, 1998 ([arXiv:hep-th/9709027](https://arxiv.org/abs/hep-th/9709027))

* {#Savvidy99} Konstantin G. Savvidy, _Born-Infeld Action in String Theory_, 1999 ([arXiv:hep-th/9906075](https://arxiv.org/abs/hep-th/9906075), [spire:501510](https://inspirehep.net/literature/501510))

* [[Arkady Tseytlin]], _Born-Infeld action, supersymmetry and string theory_, in: [[Mikhail Shifman]] (ed.)  _[[The many faces of the superworld]]_, pp. 417-452, World Scientific (2000) ([arXiv:hep-th/9908105](https://arxiv.org/abs/hep-th/9908105), [doi:10.1142/9789812793850_0025](https://doi.org/10.1142/9789812793850_0025))

* {#Schwarz01} [[John Schwarz]], _Comments on Born-Infeld Theory_, in: [[Atish Dabholkar]], [[Sunil Mukhi]], Spenta R. Wadia (eds.) _[Strings 2001: Proceedings, Strings 2001 Conference](http://inspirehep.net/record/944370)_, Tata Institute of Fundamental Research, Mumbai, India, January 5-10, 2001 ([arXiv:hep-th/0103165](https://arxiv.org/abs/hep-th/0103165), [spire:554347](http://inspirehep.net/record/554347))

* Paul Koerber, _Abelian and Non-abelian D-brane Effective Actions_, Fortsch. Phys. 52 (2004) 871-960 ([arXiv:hep-th/0405227](https://arxiv.org/abs/hep-th/0405227))

* {#Nastase15} [[Horatiu Nastase]], Section 9.2 and 9.4 of: _Introduction to AdS/CFT correspondence_, Cambridge University Press, 2015 ([cds:1984145](http://cds.cern.ch/record/1984145), [doi:10.1017/CBO9781316090954](https://doi.org/10.1017/CBO9781316090954))


Detailed discussion of the relation to the [[Polyakov action]] and the [[Nambu-Goto action]] is in

* {#Nieto01} J. A. Nieto, _Remarks on Weyl invariant p-branes and Dp-branes_ ([arXiv:hep-th/0110227](http://arxiv.org/abs/hep-th/0110227))


Discussion in terms of D-branes as [[leaves]] of [[Dirac structures]] on [[Courant Lie 2-algebroids]] of [[type II geometry]] is in

* {#AsakawaSasaWatamura} Tsuguhiko Asakawa, Shuhei Sasa, Satoshi Watamura, _D-branes in Generalized Geometry and Dirac-Born-Infeld Action_ ([arXiv:1206.6964](http://arxiv.org/abs/1206.6964))

See also

* [[Martin Cederwall]], Alexander von Gussich, Aleksandar Mikovic, [[Bengt Nilsson]], Anders Westerberg, _On the Dirac-Born-Infeld Action for D-branes_,  Phys.Lett.B390:148-152, 1997 ([arXiv:hep-th/9606173](https://arxiv.org/abs/hep-th/9606173))

* Ian I. Kogan, Dimitri Polyakov, _DBI Action from Closed Strings and D-brane second Quantization_, Int. J. Mod. Phys. A18 (2003) 1827 ([arXiv:hep-th/0208036](https://arxiv.org/abs/hep-th/0208036))

Discussion of [[loop order|one-loop corrections]]:

* Garrett Goon, Scott Melville, Johannes Noller, _Quantum Corrections to Generic Branes: DBI, NLSM, and More_ ([arXiv:2010.05913](https://arxiv.org/abs/2010.05913))

Derivation of the first DBI-correction from an [[M5-brane]] model via [super-exceptional geometry](exceptional+generalized+geometry#SuperExceptionalGeometryReferences):

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:super-exceptional M5 flavor|Super-exceptional M5-brane model: Emergence of SU(2)-flavor sector]]_ ([arXiv:2006.00012](https://arxiv.org/abs/2006.00012))



### For coincident (non-abelian) D-branes

Proposals for the generalization of the DBI action to  [[non-abelian group|non-abelian]] [[Chan-Paton gauge fields]] (hence: for [[intersecting branes|coincident]] [[D-branes]]) includes the following:

Via a plain [[trace]]:

* T. Hagiwara, _A non-abelian Born-Infeld Lagrangian_, J. Phys., A14:3059, 1981 ([doi:10.1088/0305-4470/14/11/027](https://iopscience.iop.org/article/10.1088/0305-4470/14/11/027))

Via an antisymmetrized [[trace]]:

* [[Philip Argyres]], [[Chiara Nappi]], _Spin-1 effective actions from open strings_, Nuclear Physics B Volume 330, Issue 1, 22 January 1990, Pages 151-173 Nuclear Physics B (<a href="https://doi.org/10.1016/0550-3213(90)90305-W">doi:10.1016/0550-3213(90)90305-W</a>)

Via a combination of spacetime and gauge indices:

* Jeong-Hyuck Park, _A Study of a Non-Abelian Generalization of the Born-Infeld Action_, Phys. Lett. B458 (1999) 471-476 ([arXiv:hep-th/9902081](https://arxiv.org/abs/hep-th/9902081))

The now widely accepted proposal via a symmetrized [[trace]] is due to

* {#Tseytlin97} [[Arkady Tseytlin]], _On non-Abelian generalization of Born-Infeld action in string theory_, Nucl.Phys. B501 (1997) 41-52 ([spire:439767](http://inspirehep.net/record/439767))

followed by

* {#Myers99} [[Robert Myers]], _Dielectric-Branes_, JHEP 9912 (1999) 022 ([arXiv:hep-th/9910053](https://arxiv.org/abs/hep-th/9910053))

  (introducing the [[Myers effect]])

The symmetrized trace proposal has become widely accepted.

Review includes:

* {#Chemissany04} W. Chemissany, _On the way of finding the non-Abelian Born-Infeld theory_, 2004 ([spire:1286212](http://inspirehep.net/record/1286212) [[ChemissanyNonAbelianDBI04.pdf:file]])

Issues with this proposal at higher order have been found in


* {#HashimotoTaylor97} [[Akikazu Hashimoto]], [[Washington Taylor]], _Fluctuation Spectra of Tilted and Intersecting D-branes from the Born-Infeld Action_, Nucl. Phys. B503: 193-219, 1997 ([arXiv:hep-th/9703217](https://arxiv.org/abs/hep-th/9703217))

* {#Bain99} P. Bain, _On the non-abelian Born-Infeld action_, In: L. Baulieu , [[Michael Green]], Picco M., Windey P. (eds.) _Progress in String Theory and M-Theory_. NATO Science Series (Series C: Mathematical and Physical Sciences), vol 564. Springer, Dordrecht ([arXiv:hep-th/9909154](https://arxiv.org/abs/hep-th/9909154), [doi:10.1007/978-94-010-0852-5_12](https://doi.org/10.1007/978-94-010-0852-5_12))

* {#BergshoeffBilalRooSevrin01} [[Eric Bergshoeff]], [[Adel Bilal]], M. de Roo and A. Sevrin, _Supersymmetric non-abelian Born-Infeld revisited_, JHEP 0107, 029 (2001) ([arXiv:hep-th/0105274](https://arxiv.org/abs/hep-th/0105274))


Correction terms have been proposed in

* {#TaylorVanRaamsdonk99} [[Washington Taylor]], [[Mark Van Raamsdonk]], _Multiple D$p$-branes in Weak Background Fields_, Nucl. Phys. B573:703-734, 2000 ([arXiv:hep-th/9910052](https://arxiv.org/abs/hep-th/9910052))

A completely different approach via [[TT deformation]] of the abelian DBI action is proposed in


* T. Daniel Brennan, Christian Ferko, [[Savdeep Sethi]], _A Non-Abelian Analogue of DBI from $T \bar T$ ([arXiv:1912.12389](https://arxiv.org/abs/1912.12389))

For actual derivation of [[gauge enhancement]] on coincident D-branes see the references [there](enhanced+gauge+symmetry#ReferencesOnCoincidentDBranes).


### On flavor branes for holographic QCD

Discussion of the [[DBI-action]] for [[flavor brane|flavor branes]] in [[holographic QCD]]:


* [[Vadim Kaplunovsky]], [[Jacob Sonnenschein]], Section 6 of: _Searching for an Attractive Force in Holographic Nuclear Physics_, JHEP 05 (2011) 058 ([arXiv:1003.2621](https://arxiv.org/abs/1003.2621))


[[!include holographic Schwinger effect -- references]]


[[!include DBI-action higher curvature corrections -- references]]



### Single trace observables as weight systems on chord diagrams

Relation of [[single trace observables]] in the [[non-abelian DBI action]] on [[Dp-D(p+2)-brane bound states]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] computing [[radii]] averages of [[fuzzy spheres]]:

* {#RamgoolamSpenceThomas04} [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* {#McNamaraPapageorgakis05} [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* {#McNamara06} [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])


### Brane intersections as DBI-spikes/BIons

On [[D1-D3 brane intersections]] as spikes/BIons in the [[D3-brane]] [[DBI action|DBI-theory]]:

* [[Curtis Callan]], [[Juan Maldacena]], _Brane Dynamics From the Born-Infeld Action_, Nucl. Phys. B513 (1998) 198-212 ([arXiv:hep-th/9708147](https://arxiv.org/abs/hep-th/9708147))

* [[Paul Howe]], [[Neil Lambert]], [[Peter West]], _The Self-Dual String Soliton_, Nucl. Phys. B515 (1998) 203-216 ([arXiv:hep-th/9709014](https://arxiv.org/abs/hep-th/9709014))

* [[Gary Gibbons]], _Born-Infeld particles and Dirichlet p-branes_,  	Nucl. Phys. B514: 603-639, 1998 ([arXiv:hep-th/9709027](https://arxiv.org/abs/hep-th/9709027))

* [[Neil Constable]], [[Robert Myers]], Oyvind Tafjord, _The Noncommutative Bion Core_, Phys. Rev. D61 (2000) 106009 ([arXiv:hep-th/9911136](https://arxiv.org/abs/hep-th/9911136))


From the [[M5-brane]]

* {#HoweLambertWest97} [[Paul Howe]], [[Neil Lambert]], [[Peter West]], _The Self-Dual String Soliton_, Nucl. Phys. B515 (1998) 203-216 ([arXiv:hep-th/9709014](https://arxiv.org/abs/hep-th/9709014))



[[!redirects Dirac-Born-Infeld actions]]

[[!redirects Born-Infeld theory]]
[[!redirects Born-Infeld theories]]

[[!redirects DBI action]]
[[!redirects DBI-action]]
[[!redirects DBI actions]]
[[!redirects DBI-actions]]

[[!redirects non-abelian DBI action]]
[[!redirects non-abelian DBI-action]]
[[!redirects non-abelian DBI actions]]
[[!redirects non-abelian DBI-actions]]


[[!redirects DBI Lagrangian]]
[[!redirects DBI-Lagrangian]]
[[!redirects DBI Lagrangians]]
[[!redirects DBI-Lagrangians]]


[[!redirects DBI field theory]]
[[!redirects DBI field theories]]
[[!redirects DBI-field theory]]
[[!redirects DBI-field theories]]

[[!redirects DBI model]]
[[!redirects DBI-model]]
[[!redirects DBI models]]
[[!redirects DBI-models]]


[[!redirects nonabelian DBI model]]
[[!redirects nonabelian DBI-model]]
[[!redirects nonabelian DBI models]]
[[!redirects nonabelian DBI-models]]


[[!redirects nonabelian DBI field theory]]
[[!redirects nonabelian DBI field theories]]
[[!redirects non-abelian DBI field theory]]
[[!redirects non-abelian DBI field theories]]

[[!redirects nonabelian Born-Infeld action]]
[[!redirects nonabelian Born-Infeld actions]]
[[!redirects non-abelian Born-Infeld action]]
[[!redirects non-abelian Born-Infeld actions]]

[[!redirects nonabelian DBI action]]
[[!redirects nonabelian DBI-action]]

[[!redirects Dirac-Born-Infeld action functional]]
[[!redirects DBI action functional]]


