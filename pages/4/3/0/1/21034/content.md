For the Definition \ref{KnizhnikZamolodchikovConnection} of the [[Knizhnik-Zamolodchikov connection]] we need the following notation:

1. **[[configuration spaces of points]]**

   For $N_{\mathrm{f}} \in \mathbb{N}$ write 

   \[
     \label{OrderedConfigurationSpaceofnPointsinC}
     \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{R}^2)
     \;\coloneqq\;
     (\mathbb{R}^2)^n \backslash FatDiagonal
   \]

   for the [[ordered configuration space of n points]] in the [[plane]], regarded as a [[smooth manifold]].

   Identifying the plane with the [[complex plane]] $\mathbb{C}$, we have canonical [[holomorphic function|holomorphic]] [[coordinate functions]]

   \[
     \label{CoordinateFunctionsOnConfC}
     (z_1, \cdots, z_{N_{\mathrm{f}}})
     \;\colon\;
     \underset{{}^{\{1,\cdots,n\}}}{Conf}(\mathbb{R}^2)
     \longrightarrow
     \mathbb{C}^{N_{\mathrm{f}}}
     \,.
   \]

1. **[[horizontal chord diagrams]]**

   \[
     \label{HorizontalChordDiagrams}
     \mathcal{A}^{{}^{pb}}_{N_{\mathrm{f}}}
     \;\coloneqq\;
     Span\big(\mathcal{D}^{{}^{pb}}_{N_{\mathrm{f}}}\big)/4T
   \]

   for the [[quotient vector space]] of the [[linear span]] of [[horizontal chord diagrams]] on $n$ strands by the [[4T relations]] ([[infinitesimal braid relations]]), regarded as an [[associative algebra]] under [[concatenation]] of strands ([here](horizontal+chord+diagram#AlgebraOfHorizontalChordDiagrams)).

+-- {: .num_defn #KnizhnikZamolodchikovConnection}
###### Definition
**([[Knizhnik-Zamolodchikov form]])**

The _universal [[Knizhnik-Zamolodchikov form]]_ is the [[horizontal chord diagram]]-[[Lie algebra valued differential form|algebra valued differential form]] (eq:HorizontalChordDiagrams) on the [[configuration space of points]]  (eq:OrderedConfigurationSpaceofnPointsinC)

\[
  \label{UniversalKnizhnikZamolodchikovForm}
  \omega_{KZ}
  \;\in\;
  \Omega
  \big(
    \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{C})
    \,,
    \mathcal{A}^{{}^{pb}}_{N_{\mathrm{f}}}
  \big)
\]

given in the canonical [[coordinates]] (eq:CoordinateFunctionsOnConfC) by:

\[
  \label{DefineUniversalKnizhnikZamolodchikovForm}
  \omega_{KZ}
  \;\coloneqq\;
  \underset{ i \lt j \in \{1, \cdots, n\} }{\sum}
  d_{dR} log\big( z_i - z_j \big)
  \otimes t_{i j}
  \,,
\]

where 

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordGenerator.jpg" width="500>
</center>

is the horizontal chord diagram with exactly one chord, which stretches between the $i$th and the $j$th strand.

Regarded as a connection form for a [[connection on a vector bundle]], this defines the universal _[[Knizhnik-Zamolodchikov connection]]_ $\nabla_{KZ}$, with [[covariant derivative]]

$$
  \nabla \phi
  \;\coloneqq\;
  d \phi + \omega_{KV} \wedge \phi
$$

for any [[smooth function]]

$$
  \phi \;\colon\;
    \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{C})
  \longrightarrow
  \mathcal{A}^{{}^{pb}}_{N_{\mathrm{f}}} Mod 
$$

with values in [[modules]] over the algebra of [[horizontal chord diagrams]] [[quotient space|modulo]] [[4T relations]].

The condition of covariant constancy

$$
  \nabla_{KZ} \phi \;=\; 0
$$

is called the _Knizhnik-Zamolodchikov equation_.

Finally, given a [[metric Lie algebra]] $\mathfrak{g}$ and a [[tuple]] of [[Lie algebra representations]] 

$$
  (
    V_1, 
      \cdots,
    V_{N_{\mathrm{f}}}
  ) 
  \;\in\; (\mathfrak{g} Rep_{/\sim})^{N_{\mathrm{f}}}
  \,,
$$

the corresponding [[endomorphism]]-valued [[Lie algebra weight system]]

$$
  w_{V} 
  \;\colon\;
  \mathcal{A}^{{}^{pf}}_{N_{\mathrm{f}}}
  \longrightarrow
  End_{\mathfrak{g}}\big( V_1 \otimes \cdots V_{N_{\mathrm{f}}}  \big) 
$$

turns the universal [[Knizhnik-Zamolodchikov form]] (eq:UniversalKnizhnikZamolodchikovForm) into a [[endomorphism ring]]-[[Lie algebra valued differential form|valued differential form]]

\[
  \label{LieKnizhnikZamolodchikovForm}
  \omega_{KZ}
  \;\coloneqq\;
  \underset{ i \lt j \in \{1, \cdots, n\} }{\sum}
  d_{dR} log\big( z_i - z_j \big)
  \otimes w_V(t_{i j})
  \;\in\;
  \Omega
  \big(
    \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{C})
    \,,
    End\big(V_1 \otimes \cdot V_{N_{\mathrm{f}}} \big)
  \big)

  \,.
\]

=--

The universal formulation (eq:UniversalKnizhnikZamolodchikovForm) is highlighted for instance in [Bat-Natan 95, Section 4.2](Vassiliev+invariant#BarNatan95), 
[Lescop 00, p. 7](Kontsevich+integral#Lescop00). Most authors state the version after evaluation in a [[Lie algebra weight system]], e.g. [Kohno 14, Section 5](Kontsevich+integral#Kohno14).

+-- {: .num_prop #KnizhnikZamolodchikovConnectionIsFlat}
###### Proposition
**([[Knizhnik-Zamolodchikov connection]] is [[flat connection|flat]])**

The [[Knizhnik-Zamolodchikov connection]] $\omega_{ZK}$ (Def. \ref{KnizhnikZamolodchikovConnection}) is [[flat connection|flat]]:

$$
  d \omega_{ZK} + \omega_{ZK} \wedge \omega_{ZK}
  \;=\;
  0
  \,.
$$

=--

+-- {: .num_prop #KontsevichIntegralForBraids}
###### Proposition
**([[Kontsevich integral]] for [[braids]])**

The [[Dyson formula]] for the [[holonomy]] of the [[Knizhnik-Zamolodchikov connection]] (Def. \ref{KnizhnikZamolodchikovConnection}) is called the _[[Kontsevich integral]] on [[braids]]_.

=--

(e.g. [Lescop 00, side-remark 1.14](Kontsevich+integral#Lescop00))
