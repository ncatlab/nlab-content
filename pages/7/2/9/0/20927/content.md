

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
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

In the construction of the [[Lagrangian density]] for the [[supersymmetry|supersymmetric]] [[worldvolume]] [[gauge field|gauge]] [[quantum field theory]] on [[intersecting brane|coincident]] [[M2-branes]] (the [[BLG model]]/[[ABJM model]], a [[conformal field theory|conformal]] [[supersymmetry|super]]-[[Chern-Simons theory]] coupled to  [[matter]]-[[field (physics)|fields]]) a certain [[algebra|algebraic]] structure appears -- and at least in the [[BLG model]] it appears at a pivotal stage in the [[proof]] of [[supersymmetry]] -- which is given by a  [[multilinear map|trilinear map]] on an [[inner product space]] $V$

$$
  V \otimes V \otimes V 
  \overset{ 
    \overset{
       \color{blue} 
       \;\;
       {
        \text{3-bracket}
        \atop
        \phantom{-}
       }
       
       \;\;
    }{
      [-,-,-] 
    }
  }{\longrightarrow} V
$$

that is subject to some [[axioms]] which are different from but clearly reminiscent to the [[axioms]] on the [[Lie bracket]] of a [[Lie algebra]], (which is of course a bilinear map).

In special cases, but not generally, this algebraic structure is a special case of a structure introduced by Filippov, which could be called a [[Filippov algebra]], but which mostly came to alternatively be called a _3-Lie algebra_ or a _Lie 3-algebra_ or often just a _3-algebra_.  

Unfortunately, in [[homotopy theory]] and [[higher algebra]], these terms refer to something different, namely to [[L-infinity algebras]] or [[categorification|categorifications]] of [[associative algebras]] to [[n-algebras]] -- but the structure seen in the [[BLG model]] on [[M2-branes]] is _none_ of these.

Hence to be on the safe side, one may want to speak of _M2-brane 3-algebras_ or maybe _M-brane algebras_, for definiteness

Moreover, while this "M2-brane 3-algebra" appeared to be a central ingredient in the [[BLG model]], it makes _no_ appearance in the [[ABJM model]], which however generalizes and hence subsumes the BLG model, up to slight re-identifications of terms.

Indeed, inspection reveals that "M2-brane 3-algebras" give rise to and may be re-constructed from data in ordinary [[Lie theory]], namely from [[pairs]] consisting of a [[metric Lie algebra]] and a [[dualizable object|dualizable]] [[Lie algebra representation]]. 

$$
  \big\{
    \text{M2-brane 3-algebras}
  \big\}
  \;\;\overset{\simeq}{\leftrightarrow}
  \left\{
    {
    \text{faithful orthogonal representations} 
       \atop
    \text{of metric Lie algebras}
    }
  \right\}
$$

This is due to [dMFFMER 08, Theorem 11](#dMFFMER08), recalled as Prop. \ref{M2Brane3AlgebrasEquivalentToMetricLieRepresentation} below.

(...)

## Definition

+-- {: .num_defn #AxiomsOnM2Brane3Algebra}
###### Definition
**([[M2-brane 3-algebra]])**

An _M2-brane 3-algebra_ is

1. a [[real vector space|real]] [[finite-dimensional vector space]] $V$;

1. a _metric_ $\langle -,-\rangle$ on $V$, hence a non-degenerate [[inner product space]]  (not required to be positive definite);

1. a [[multilinear map|trilinear function]], the _3-bracket_

   $$
     V \otimes V \otimes V \overset{[-,-,-]}{\longrightarrow} V
   $$

such that the following three [[axioms]] hold, for all [[elements]] $w,x,y,z \in V$:

1. (**unitarity**) 

   $$
     \big\langle [x,y,z],w \big\rangle
      \;=\;
     -\big\langle z, [x,y,w]\big\rangle
   $$

1. (**symmetry**)

   $$
     \big\langle [x,y,z],w \big\rangle
      \;=\;
     -\big\langle [z,w,x], y \big\rangle
   $$

1. (**fundamental identity**)

   $$
     \begin{aligned}
       \big[x,y, [v,w,z]  \big]
       & 
         = \phantom{+}\;
        \big[  [x,y,v], w, z \big]
       \\
       &
       \phantom{=\;} +
        \big[ v, [x,y, w] , z \big]
       \\
       &
       \phantom{=\;} +
        \big[ v, w , [x,y, z ] \big]
     \end{aligned}
   $$

=--

In this generality, and under the name "generalized metric Lie 3-algebras", this is due to [Cherkis-Saemann 08, 41](#CherkisSaemann08), see [dMFFMER 08, Def. 1](#dMFFMER08)

## Properties 

### Equivalence to metric Lie representations

For the following, let the [[ground field]] be the [[real numbers]] and take all [[vector spaces]] involved to be [[real vector space|real]] and [[finite-dimensional vector spaces|finite-dimensional]].

For definiteness, we make the following explicit:

+-- {: .num_defn #ModulesOfMetricLieAlgebras}
###### Definition
**([[metric Lie representation]])**

An _orthogonal representation of a metric Lie algebra_ is

1. a [[metric Lie algebra]]

   $$
     \big((\mathfrak{g},[-,-]), g \big)
   $$

1. a metric [[vector space]] 

   $$
     (V,k)
     \,,
   $$ 

   hence a non-degenerate real [[inner product space]];

1. an [[orthogonal Lie algebra|orthogonal]] [[Lie algebra representation]] 

   $$
     \mathfrak{g} \otimes V \overset{\rho}{\to} V
   $$

  of $\mathfrak{g}$ on $(V,k)$.

=--

+-- {: .num_remark #LinearDualsAndAdjuncts}
###### Remark
**(linear duals and adjuncts/transposition)**

Given an orthogonal representation of a metric Lie algebra as in Def. \ref{ModulesOfMetricLieAlgebras}, 
the non-degenerate [[inner products]] $g$  on $\mathfrak{g}$ and $k$ on $V$ exhibit these as [[self-dual objects]] in the [[monoidal category]] of [[finite-dimensional vector spaces]] (with respect to the [[tensor product of vector spaces]]).

This means that by passsing to [[adjuncts]] we may regard [[linear maps]] of the form

$$
  V \otimes W \overset{f}{\longrightarrow} Z
$$

equivalently as linear maps of the form

$$
  W \overset{\overline{f}}{\longrightarrow} Z \otimes V^\ast
  \,,
$$

where $V^\ast$ is the [[dual vector space]]; and similarly for $\mathfrak{g}$.

Once we choose a [[linear basis]] $\{v_i\}_{i \in \{1, \cdots, dim(V)\}}$ of $V$, with respect to which the metric tensor $k$ has components

\[
  \label{ComponentsOfMetricOnV}
  k_{i j} \;\coloneqq\; k(v_i, v_j)
\]

this forming of adjuncts is equivalently the yoga of "raising and lowering of indices via the metric". Similarly for a choice of [[linear basis]] $\{t_a\}_{a \in \{1,\cdots, dim(\mathfrak{g})\}}$ for the Lie algebra, and the induced components

\[
  \label{ComponentsOfMetricOng}
  g_{a b} \;\coloneqq\; g(t_a, t_b) \,.
\]

Specifically, given the basis component $(\rho_a{}^{i}{}_j)_{a,i,j}$ of the [[Lie algebra representation|Lie action]] $\mathfrak{g} \otimes V \overset{\rho}{\longrightarrow} V$, defined by

\[
  \label{ComponentsOfLieAction}
  \rho(t_a, v_i)
  \;\coloneqq\;
  \rho_a{}^{i}{}_j v_i
\]

we get the components $(\tilde \rho^a{}_{i j})_{a,i,j}$ of the [[adjunct]]

\[
  \label{AdjunctOfLieAction}
  V \otimes V \overset{ \tilde \rho }{\longrightarrow} \mathfrak{g}
\]

by contracting the original component (eq:ComponentsOfLieAction) with the components (eq:ComponentsOfMetricOnV) (eq:ComponentsOfMetricOng)  of the metric tensors:

\[
  \label{ComponentsOfAdjunctOfLieAction}
  (\tilde \rho^a{}_{i j})_{a,i,j}
  \;=\;
  g_{l j} k^{a b} \, \rho_b{}^l{}_i
\]



=--


+-- {: .num_defn #TrilinearMapInducedFromOrthogonalRepOfMetricLieAlgebra}
###### Definition
**(trilinear map induced from [[metric Lie representation]] -- [[Faulkner construction]])**

Given an orthogonal representation $\mathfrak{g} \otimes V \overset{\rho}{\to} V$ of a metric Lie algebra as in Def. \ref{ModulesOfMetricLieAlgebras}, define

1. a [[bilinear map]]

   $$
     V \otimes V 
       \overset{
          \;\;D\;\;
       }{\longrightarrow}
     \mathfrak{g}
   $$  

   given by

   \[
     \label{DefiningEquationForD}
     (X, D(x,y))
     \;=\;
     \langle \rho(X,x), y \rangle
     \;\;\;\;
     \mathrlap{
       \text{for all}\; X \in \mathfrak{g}\,, x, y \in V
     }
   \]

1. a [[multilinear map|trilinear map]]

   $$
     \label{DefiningEquationForInducedTrilinearBracket}
     V \otimes V \otimes V
       \overset{
          [-,-,-]_{\rho} \coloneqq \rho(D(-,-),-)
       }{\longrightarrow}
     V
    \,,
   $$ 

   hence

   $$
     [x, y, z]_\rho
     \;\coloneqq\;
     \rho\big(  D(x, y), z \big)
   $$

=--


In this form and with this notation  this is [dMFFMER 08, equation (9) and over Prop. 10](#dMFFMER08) (except that we write "$\rho(X,x)$" for their "$X \cdot x$"). The construction itself, up to one dualization of $V$, was introduced in [Faulkner 73](#Faulkner73).


+-- {: .num_remark}
###### Remark
**(component expression of trilinear bracket)**

After a choice of [[linear bases]] as in Remark \ref{LinearDualsAndAdjuncts}, in terms of which Lie algebra elements $X \in \mathfrak{g}$
are expanded as $X \coloneqq X^a t_a$ and representation vectors $x \in V$ are expanded as $x \coloneqq x^i v_i$, the defining equation (eq:DefiningEquationForD)

$$
  (X, D(x,y))
  \;=\;
  \langle \rho(X,x), y \rangle
  \;\;\;\;
  \text{for all arguments}
$$

reads

$$
  k_{a b} X^a \, D_{i j}{}^b \, x^i y^j
  \;=\;
  g_{l j} \, \rho_a{}^l{}_i \,  X^a x^i y^j
  \;\;\;\;
  \text{for all components}
$$

(where here and in the following we use the [[Einstein summation convention]]), hence reads

$$
  k_{a b} D_{i j}{}^b
  \;=\;
  g_{l j} \rho_a{}^l{}_i
  \;\;\;\;
  \text{for all indices}
$$

hence equivalently reads

$$
  D_{i j}{}^a
  \;=\;
  g_{l j} k^{a b} \, \rho_b{}^l{}_i
  \;\;\;\;
  \text{for all indices}
$$

hence says that the [[tensor]] $D$ is equal to the adjunct (eq:AdjunctOfLieAction) of the Lie action tensor $\rho$, given in components by the evident "raising and lowering of indices via the metrics" as in (eq:ComponentsOfAdjunctOfLieAction):

$$
  D_{i j}{}^a
  \;=\;
  \rho^a{}_{i j}
  \;\;\;\;
  \text{for all indices}
  \,.
$$


With this, the induced trilinear bracket (eq:DefiningEquationForInducedTrilinearBracket)

$$
     V \otimes V \otimes V
       \overset{
          [-,-,-]_{\rho} \coloneqq \rho(D(-,-),-)
       }{\longrightarrow}
     V
$$

is given in components as

$$
  \begin{aligned}
  [v_i, v_j, v_k]_\rho
  & =\;
  \rho(D(v_i, v_j), v_k)
  \\
  & =\;
  \rho( D_{i j}{}^a t_a , v_k )
  \\
  & =
  \rho_{a}{}^m{}_k  
  \underset{
    = 
    g_{l j} k^{a b} \, \rho_b{}^l{}_i
  }{
    \underbrace{D_{i j}{}^a}
  } 
  v_m
  \\
  & =
  \rho_{a}{}^m{}_k   g_{l j} k^{a b} \, \rho_b{}^l{}_i     v_m
  \\
  & = 
  \big( \rho_{a}{}^m{}_k \rho^a{}_j{}_i \big)  v_m
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #M2Brane3AlgebrasEquivalentToMetricLieRepresentation}
###### Proposition
**([[M2-brane 3-algebras]] are equivalent to [[metric Lie representations]])**

Given an orthogonal representation $\mathfrak{g} \otimes V \overset{\rho}{\to} V$ of a metric Lie algebra as in Def. \ref{ModulesOfMetricLieAlgebras}, its induced trilinear map $[-,-,-]_\rho$ (Def. \ref{TrilinearMapInducedFromOrthogonalRepOfMetricLieAlgebra}) satisfies the axioms of an M2-brane 3-algebra (Def. \ref{AxiomsOnM2Brane3Algebra}). 

Hence this assignment defines a [[function]] from [[isomorphism classes]] of orthogonal representations of metric Lie algebras to [[isomorphism classes]] of M2-brane 3-algebras

$$
  \left\{
    {
    {\text{orthogonal representations}}
    \atop
    {\text{metric Lie algebras}}
    }
  \right\}_{/\sim}
  \underoverset
  {}
  {
     \;\;\;\;
     \rho \;\mapsto\; [-,-,-]_\rho
     \;\;\;\;
  }{\longrightarrow}
  \left\{
    {
    {\text{M2-brane}}
    \atop
    {\text{3-algebras}}
    }
  \right\}_{/\sim}
  \,.
$$

Moreover, restricted to [[faithful representations]], this function is a [[bijection]]:

$$
  \left\{
    {
    {
    {\text{faithful}}
    \atop
    {\text{orthogonal representations}}
    }
    \atop
    {\text{metric Lie algebras}}
    }
  \right\}_{/\sim}
  \underoverset
  {\simeq}
  {
     \;\;\;\;
     \rho \;\mapsto\; [-,-,-]_\rho
     \;\;\;\;
  }{\longrightarrow}
  \left\{
    {
    {\text{M2-brane}}
    \atop
    {\text{3-algebras}}
    }
  \right\}_{/\sim}
  \,.
$$


=--

This is [dMFFMER 08, Prop. 10 and Theorem 11](#dMFFMER08).

### Relation to Lie algebra weight systems on chord diagrams
 {#RelationToLieAlgebraWeightSystemsOnChordDiagrams}

In [[Penrose notation]] ([[string diagram]]-notation), the trilinear bracket induced by a [[metric Lie representation]] according to Def. \ref{TrilinearMapInducedFromOrthogonalRepOfMetricLieAlgebra} looks as follows:

<center>
<img src="https://ncatlab.org/nlab/files/MBrane3AlgebraFromMetricLieRepresentationII.jpg" width="600">
</center>

With Prop. \ref{M2Brane3AlgebrasEquivalentToMetricLieRepresentation} this shows that M2-brane 3-algebras are equivalently the datum that [[Lie algebra weight systems]] on ([[horizontal chord diagram|horizontal]]) [[chord diagrams]] assign to a single chord.

> from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


## Related entries

* [[Nambu mechanics]]

* [[BLG model]]

* [[Nambu-Poisson M5-brane model]]

## References

### Appearance in M2-brane theory

The idea that some higher-arity version of the Lie bracket may be relevant for [[M2-M5 brane intersections]] originates with attempts of generalizing [[Nahm's equations]] for [[fuzzy funnels]] of [[D2-D4 brane intersections]] in 

* [[Anirban Basu]], [[Jeffrey Harvey]], _The M2-M5 Brane System and a Generalized Nahm's Equation_, Nucl.Phys. B713 (2005) 136-150 ([arXiv:hep-th/0412310](https://arxiv.org/abs/hep-th/0412310))

Motivated by this, the M2-brane 3-algebra appears in the construction of the [[BLG model]] for the [[worldvolume]] [[quantum field theory]] on 2 coincident [[M2-branes]] in

* {#BaggerLambert06} [[Jonathan Bagger]], [[Neil Lambert]], _Modeling Multiple M2's_, Phys. Rev. D75, 045020 (2007). ([hep-th/0611108](http://arxiv.org/abs/hep-th/0611108))

* {#BaggerLambert07} [[Jonathan Bagger]], [[Neil Lambert]], _Gauge Symmetry and Supersymmetry of Multiple M2-Branes_, Phys. Rev. D77, 065008 (2008). ([arXiv:0711.0955](http://arXiv.org/abs/0711.0955))

further highlighted as such in 

* {#Gustavsson07} [[Andreas Gustavsson]], _Algebraic structures on parallel M2-branes_ Nucl. Phys. B811, 66-76 (2009) ([arXiv:0709.1260](https://arxiv.org/abs/0709.1260))

(whence the "BLG" of the [[BLG model]])

and further explored in

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Elena Méndez-Escobar]], _Metric Lie 3-algebras in Bagger-Lambert theory_, JHEP 0808 : 045, 2008 ([arXiv:0806.3242](https://arxiv.org/abs/0806.3242))

From here on a myriad of references followed up. Review includes:

(...)



### Equivalence to metric Lie representations

The full generalized axioms on the M2-brane 3-algebra and first insights into their relation to [[Lie algebra representations]] of [[metric Lie algebras]] is due to

* {#CherkisSaemann08} [[Sergey Cherkis]], [[Christian Saemann]], Section 4 of: _Multiple M2-branes and Generalized 3-Lie algebras_, Phys. Rev. D78:066019, 2008 ([arXiv:0807.0808](https://arxiv.org/abs/0807.0808))

The full identification of M2-brane 3-algebras with dualizable [[Lie algebra representations]] over [[metric Lie algebras]] is due to

* {#dMFFMER08} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Elena Méndez-Escobar]], [[Patricia Ritter]], _On the Lie-algebraic origin of metric 3-algebras_, Commun. Math. Phys. 290:871-902, 2009 ([arXiv:0809.1086](http://arxiv.org/abs/0809.1086))

reviewed in

* [[José Figueroa-O'Farrill]], slide 145 onwards in: _Triple systems and Lie superalgebras_ in _M2-branes, ADE and Lie superalgebras_, talk at IPMU 2009 ([pdf](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/Hongo.pdf), [[FigueroaOFarrillM2Branes02.pdf:file]])

further explored in 

* [[José Figueroa-O'Farrill]], _Simplicity in the Faulkner construction_,  Journal of Physics A: Mathematical and Theoretical, Volume 42, Number 44 ([arXiv:0905.4900](https://arxiv.org/abs/0905.4900))

and putting to use the [[Faulkner construction]] that was previously introduced in 

* {#Faulkner73} [[John Faulkner]], _On the geometry of inner ideals_, Journal of Algebra, Volume 26, Issue 1, July 1973, Pages 1-9 (<a href="https://doi.org/10.1016/0021-8693(73)90032-X">doi:10.1016/0021-8693(73)90032-X</a>)

See also:

* Sam Palmer, [[Christian Saemann]], section 2 of _M-brane Models from Non-Abelian Gerbes_, JHEP 1207:010, 2012 ([arXiv:1203.5757](http://arxiv.org/abs/1203.5757))

* {#SaemannRitter13} [[Patricia Ritter]], [[Christian Saemann]], section 2.5 of _Lie 2-algebra models_, JHEP 04 (2014) 066 ([arXiv:1308.4892](http://arxiv.org/abs/1308.4892))

* {#Saemann16} [[Christian Saemann]], appendix A of _Lectures on Higher Structures in M-Theory_ ([arXiv:1609.09815](https://arxiv.org/abs/1609.09815))

and

* {#Palmkvist09} [[Jakob Palmkvist]], _Three-algebras, triple systems and 3-graded Lie superalgebras_, J. Phys. A43:015205, 2010 ([arXiv:0905.2468](https://arxiv.org/abs/0905.2468))


[[!redirects M-brane 3-algebras]]

[[!redirects M2-brane 3-algebra]]
[[!redirects M2-brane 3-algebras]]

[[!redirects Faulkner construction]]
[[!redirects Faulkner constructions]]

[[!redirects BLG 3-algebra]]
[[!redirects BLG 3-algebras]]

