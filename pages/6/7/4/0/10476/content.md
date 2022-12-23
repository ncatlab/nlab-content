
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Elmendorf's theorem_ states that for $G$ a [[topological group]], the [[(∞,1)-category of (∞,1)-presheaves]] on the [[orbit category]] $Orb_G$ of $G$, naturally regarded as an [[(∞,1)-site]], is [[equivalence of (∞,1)-categories|equivalent]] to the classical $G$-[[equivariant homotopy theory]], namely the [[localization of an (∞,1)-category|localization]] of [[topological spaces]] with $G$-[[action]] ([[G-spaces]]) at the _[[weak homotopy equivalences]] on all [[fixed point spaces]]_ of [[closed subset|closed]] [[subgroups]] (the [[equivariant weak homotopy equivalences]]).

This is due to [Elmendorf 83](#Elmendorf83) and [Dwyer-Kan 84, Sec. 1.2, 1.7 & Thm. 3.1](#DwyerKan84); with alternative proofs in various stages of refinement (see Remark \ref{AssumptionsAndRefinementsInTheLiterature} below) given by [Piacenza 91, Sec. 6](#Piacenza91), [May 96, Sec. V.3](#May96), [Cordier-Porter 96, Thm. 3.11](#CordierPorter96), [Guillou 06, Prop. 3.15](#Guillou06), [Stephan 13, Cor. 3.20](#Stephan13), [Guillou-May-Rubin 13, Thm. 1.8 & 5.6](#GuillouMayRubin13). Exposition is in [Blumberg 17, Sec. 1.3](#Blumberg17).

In particular this means that the $G$-[[equivariant homotopy theory]], thus identified with an [[(∞,1)-category of (∞,1)-presheaves]], is an [[(∞,1)-topos]] and in fact (since $Orb_G$ has [[finite products]]) a [[cohesive (∞,1)-topos]]; a point expanded on in [Rezk 14](#Rezk14), [Sati-Schreiber 20](#SatiSchreiber20) (for more on this see at _[[orbifold cohomology]]_).


More in detail, write $Top^G$ for the [[category]] of [[compactly generated topological spaces]] which are equipped with a [[continuous function|continuous]] $G$-[[action]] ([[G-spaces]]). Say that a $G$-[[equivariant function|equivariant]] [[continuous function]] $f \colon X \longrightarrow Y$ between $G$-spaces is a **weak $G$-homotopy equivalence** if for all [[closed subgroups]] $H \hookrightarrow G$ the induced function on $H$-[[fixed point spaces]] $f^H \colon X^H \longrightarrow Y^H$ is an ordinary [[weak homotopy equivalence]]. Write 

$$
  L_{G whe} Top^G
  \;\in\; 
  (\infty,1)Cat
$$

for the corresponding [[simplicial localization]].

Next, write $Orb_G$ for the [[full subcategory]] of $Top^G$ on the $G$-[[homogeneous spaces]] of the form $G/H$, but regarded as an [[(∞,1)-category]] by regarding each [[compact-open topology|hom-space]] as its [[homotopy type]]. Write moreover $Top^{Orb_G}$ for the category of [[continuous function|continuous]] [[functors]] $Orb_G^{op} \longrightarrow Top$. Write finally

$$
  PSh_\infty(Orb_G)
   \in 
 (\infty,1)Cat
  \,.
$$

Then Elmendorf's theorem asserts that there is an [[equivalence of (∞,1)-categories]]

$$
 L_{G whe}
  Top^G
  \;\simeq\;
  PSh_\infty(Orb_G)
  \,.
$$

\begin{remark}\label{AssumptionsAndRefinementsInTheLiterature}
(**survey of available proofs.**)

Elmendorf's theorem is stated in [Elmendorf 83](#Elmendorf83) as an [[equivalence of categories|equivalence]] of [[homotopy categories]]; and is enhanced in [Dwyer-Kan 84, Sec. 1.2, 1.7 & Thm. 3.1](#DwyerKan84) to a [[simplicial Quillen adjunction|simplicial]] [[Quillen equivalence]] of [[model categories]] [[presentable (infinity,1)-category|presenting]] (in hindsight) the [[equivalence of (∞,1)-categories]] stated above (e.g. [Blumberg 17. Thm. 1.3.8](#Blumberg17)).

Moreover, while [Elmendorf 83](#Elmendorf83) assumes $G$ to be a [[compact Lie group]], [Dwyer-Kan 84](#DwyerKan84) allow $G$ to be *any* [[topological group]]. But beware that invoking the [[equivariant Whitehead theorem]] to identify the fixed-locus-wise weak homotopy equivalences, used in the theorem, with the $G$-homotopy equivalences, typically used in practice, again requires $G$ to be a [[compact Lie group]].

Later [Piacenza 91, Sec 6](#Piacenza91) and [May 96, Sec. V.3](#May96) re-prove the equivalence of [[homotopy categories]] for $G$ any [[topological group]]; while [Cordier-Porter 96, Thm. 3.11](#CordierPorter96) and [Guillou 06, Prop. 3.15](#Guillou06) re-prove a ([[simplicial Quillen adjunction|simplicial]]) [[Quillen equivalence]] assuming $G$ to be a [[discrete group|discrete]] or even [[finite group]], respectively; and [Stephan 13, Cor. 3.20](#Stephan13), [Guillou-May-Rubin 13, Thm. 1.8](#GuillouMayRubin13) re-prove the Quillen equivalence for $G$ again any topological group.

([Stephan 13](#Stephan13) credits [Piacenza 91](#Piacenza91) with proving a [[Quillen equivalence]]. While this is not what [Piacenza 91, Thm. 6.3](#Piacenza91) actually states, the conclusion follows with hindsight.)

These results are all based on the [[classical model structure on topological spaces]].  The analogous Quillen equivalence based on the [[classical model structure on simplicial sets]] is proven in [Guillou-May-Rubin 13, Thm. 5.6](#GuillouMayRubin13), assuming $G$ to be a [[discrete group]].
\end{remark}


\begin{remark}\label{AsAStatementAboutEquivariantConcordance}
**(as a statement about [[concordance]] of [[equivariant maps]])**
\linebreak
  One way to understand Elmendorf's theorem (in its full $\infty$-category theoretic version) is as translating [[concordance]] of [[equivariant maps]] into actual [[homotopies]] in another [[(infinity,1)-category|$\infty$-category]]. Namely, if we think of sending a [[topological space]] $\mathrm{X}$ to its underlying [[homotopy type]] presented by its [[path infinity-groupoid|path $\infty$-groupoid]] (we follow the notation at *[[shape via cohesive path ∞-groupoid]]*)
$$
  \array{
    Top 
      &\longrightarrow&
    Grpd_\infty
    \\
    \mathrm{X}
    &\overset{\phantom{--}}{\mapsto}&
    \esh \mathrm{X}
  }
$$
then it says that got each [[G-CW complex|$G$-CW complex]] $X$ we have:
$$
  \esh
  \Big(
    Maps
    \big(
      \mathrm{X}
      ,\,
      \mathrm{Y}
    \big)^G
  \Big)
  \;\;
  \simeq
  \;\;
  G Grpd_\infty
  \Big(
    \esh \big(\mathrm{X}^{(-)}\big)
    ,\,
    \esh \big(\mathrm{Y}^{(-)}\big)
  \Big)
  \,,
$$
where $Map(-,-)$ denotes the [[compact-open topology|mapping space]].

In this form the statement holds for *every* choice of [[topological group]] $G$ and *every* choice of family $\big\{H_i 
\subset G\big\}_{i \in I}$ of [[subgroups]]: This choice affects what counts as a $G$-CW complex on the left and what the [[orbit category]]-site $Orb(G,\{H_i\}_{i \in I})$ is on the right
(in both cases the [[coset spaces]] involved must be $G/H_i$ for $H_i$ in the given family) -- but with that understood, the above equivalence holds, by [Dwyer-Kan 84, Sec. 1.2, 1.7 & Thm. 3.1](#DwyerKan84).

To bring this out, write

* $Orb(G,\mathcal{F}) \hookrightarrow G Top$ for the [[full subcategory]] on the [[coset spaces]] $G/H$ for $H \in \mathcal{F}$ in the family of subgroups,

* $(G, \mathcal{F})CWCplx \hookrightarrow G Top$ for the [[full subcategory]] of [[G-CW complexes]] build via these coset spaces, then

$$
  X \,\in\,
  (G,\mathcal{F})CWCplx
  \;\;\;\;
  \vdash
  \;\;\;\;
  \esh
  \Big(
    Maps
    \big(
      \mathrm{X}
      ,\,
      \mathrm{Y}
    \big)^G
  \Big)
  \;\;
  \simeq
  \;\;
  Psh_\infty\big(Orb(G,\mathcal{F})\big)
  \Big(
    \esh \big(\mathrm{X}^{(-)}\big)
    ,\,
    \esh \big(\mathrm{Y}^{(-)}\big)
  \Big)
  \,.
$$


\end{remark}




## Statement

### Classical version in topological spaces
 {#ClassicalVersionInTopologicalSpaces}

Write 

* $kTop$ for the category of [[compactly generated topological spaces]];

\begin{assumption}\label{GeneralInputData}
**(general input data)**
\linebreak
Let 

* $G \,\in\, Grp(kTop)$ be *any* [[topological group]],

* $\mathcal{F} \,\subset\,  Sub(G)$ be *any* [[set]] of [[subgroups]] of $G$.

\end{assumption}

\begin{remark}\label{FixedLociAsEquivariantMappingSpaces}
**([[fixed loci]] as [[equivariant function|equivariant]] [[mapping spaces]])**
\linebreak
For $H \subset G$ any [[subgroup]], notice the usual identification of $H$-[[fixed loci]] $X^H \subset X$ inside [[topological G-spaces|topological $G$-spaces]] $X$ with the $G$-[[equivariant function|equivariant]] [[compact-open topology|mapping space]] out of the [[orbit]]/[[coset space]] $G/H$:

$$
  Map(G/H,\, -)
  \;\simeq\;
  (-)^H
  \,.
$$

\end{remark}

\begin{proposition}\label{FProjectiveModelStructureOnGSpaces}
**($\mathcal{F}$-projective model structure on $G$-spaces)**
\linebreak
  In the generality of Assumption \ref{GeneralInputData},
  the category of [[topological G-spaces|topological $G$-spaces]] carries the [[mathematical structure|structure]] of a  [[simplicial model category]] $G Act(kTop)_{\mathcal{F} proj}$ whose

* [[hom-objects]] are the [[singular simplicial complexes]] of [[compact-open topology|mapping spaces]]:

  \[
    \label{SimplicialHomComplexBetweenGTopologicalSpaces}
    [X,Y] 
      \,\coloneqq\,
    Sing
    \big(
      Map(X,Y)^G
    \big)
    \;\;\;
    \in
    \;
    sSet
  \]

* [[weak equivalences]] and [[fibrations]] $X \xrightarrow{f} Y$ are $H \in \mathcal{F}$-[[fixed point space]]-wise ($[G/H, X] \xrightarrow{\;[G/H, f]\;} [G/H, Y]$, see Rem. \ref{FixedLociAsEquivariantMappingSpaces})
those of the [[classical model structure on topological spaces]], 

* [[cofibrations]] include the relative [[G-CW complexes|$G$-CW complexes]] which are build (only) from [[orbits]] of the form $G/H$ for $H \,\in\, \mathcal{F} \subset Sub(G)$.

\end{proposition}
([Dwyer & Kan 1984, §1.2 and Thm. 2.2](#DwyerKan84))

\begin{remark}
**(relation to classical $G$-equivariant homotopy theory)**
\linebreak
In the special case of Assumption \ref{GeneralInputData} that
 
1. $G$ is a [[compact Lie group]];

1. $\mathcal{F} \coloneqq ClsSub(G)$ is the set of all [[closed topological space|closed]] subgroups

1. $X$ is a [[G-CW-complex|$G$-CW complex]]

the [[equivariant Whitehead theorem]] says that weak equivalence $X \longrightarrow{Y}$ in $G Act(kTop)_{ClsSub(G)}$ (from Prop. \ref{FProjectiveModelStructureOnGSpaces}) are exactly the $G$-[[equivariant map|equivariant]] [[homotopy equivalences]].

More generally there may be more weak equivalences in $G Act(KTop)_{\mathcal{F}}$ than there are $G$-[[homotopy equivalences]]:

$$
  G Heq 
  \hookrightarrow
  W_{\mathcal{F}}
  \,.
$$

However, observe that the simplicial hom-complex (eq:SimplicialHomComplexBetweenGTopologicalSpaces) is always the classical one, in particular its [[connected components]] are always (no matter the choice of $G$ and $\mathcal{F}$) the plain $G$-[[homotopy classes]]:

$$
  \pi_0
  [X,Y]
  \,=\,
  G Heq(X,\,Y)
  \,.
$$

\end{remark}


\begin{definition}\label{SimplicialPresheavesOnFTypeGOrbits}
**(simplicial presheaves over $\mathcal{F}$-type $G$-orbits)**
\linebreak
Given data as in Assumption \ref{GeneralInputData}, write

\[
  \label{CategoryOfFTypeGOrbits}
  Orb(G,\mathcal{F})
  \hookrightarrow
  G Act(kTop)
\]

for the [[orbit category|category of $\mathcal{F}$-type $G$ orbits]], namely the [[full subcategory|full sub]]-[[sSet-enriched category]] of [[topological G-spaces]] (eq:SimplicialHomComplexBetweenGTopologicalSpaces) on the [[coset spaces]] $G/H$ for $H \,\in\, \mathcal{F} \subset Sub(G)$.

Moreover, write

$$
  sPSh
  \big(
    Orb(G,\mathcal{F})
  \big)_{proj}
$$


for the projective [[model structure on sSet-presheaves]] 
over (eq:CategoryOfFTypeGOrbits), 
hence that whose [[weak equivalences]] and [[fibrations]] 
are object-wise those in the [[classical model structure on simplicial sets]].

\end{definition}


\begin{proposition}\label{DwyerKanTheorem}
**(Dwyer-Kan theorem)**
\linebreak
In the generality of Assumption \ref{GeneralInputData}, there is a [[Quillen equivalence]]
$$
  G Act(kTop)
  \underoverset
    {
      \underset{
        X \mapsto 
        \big(
          G/H \mapsto
          [G/H, X]
        \big)
      }{\longrightarrow}
    }
    {\longleftarrow}
    {\simeq_{\mathrlap{Qu}}}
  sPSh(
    Orb(G,\mathcal{F})
  )
$$
between 

1. the $\mathcal{F}$-projective model structure on  topological $G$-spaces  
 
    (Prop. \ref{FProjectiveModelStructureOnGSpaces}) 
 
1. the projective model structure on simplicial presheaves over the $\mathcal{F}$-type $G$-orbits 

   (Def. \ref{SimplicialPresheavesOnFTypeGOrbits})


\end{proposition}
This is [Dwyer & Kan 1984, Thm. 3.1](#DwyerKan84), formulated here as a simplicial Quillen adjunction in view of the recognition principle for simplicial Quillen adjunctions (from [this Prop.](simplicial+Quillen+adjunction#RecognitionOfSimplicialQuillenAdjunctions)).



### General model category presentation 
 {#ModelCategoryPresentation}

A version of the theorem that applies fairly generally for ([[discrete group|discrete]]) [[group objects]] in suitable [[cofibrantly generated model categories]] is in ([Guillou 06](#Guillou06), [Stephan 10](#Stephan10), [Stephan 13](#Stephan13)).

+-- {: .num_defn}
###### Definition

For $\mathcal{C}$ a [[cofibrantly generated model category]]
and for $G$ a [[discrete group]] (canonically regarded as a [[group object]] of $\mathcal{C}$ via its [[tensoring]] over [[Set]]) write $G \mathcal{C}$ for the category of $G$-[[actions]] in $\mathcal{C}$.

=--

+-- {: .num_defn #CellularFixedPointFunctor}
###### Definition

A _cellular fixed point functor_ on $\mathcal{C}$ is ...

=--

([Guillou 06, def. 3.7](#Guillou06))

+-- {: .num_example}
###### Example

The [[fixed point spaces]]-functors on the following kinds of model categories are cellular

* the [[classical model structure on topological spaces]];

* the [[classical model structure on simplicial sets]];

* the global [[model structure on simplicial presheaves]] over any small category;

* (...)

=--

([Guillou 06, section 4](#Guillou06))


+-- {: .num_defn}
###### Proposition

For $\mathcal{C}$ a [[cofibrantly generated model category]] with cellular fixed point functor, def. \ref{CellularFixedPointFunctor}, then the category $G \mathcal{C}$ of $G$-actions in $\mathcal{C}$ carries a [[cofibrantly generated model category]] structure $G \mathcal{C}_{fine}$ whose weak equivalences and fibrations are those morphisms whose [[underlying]] maps of 
$H$-[[fixed loci]], for all [[subgroups]] $H$ of $G$, are equivalences or fibrations in $\mathcal{C}$, respectively.

=--

([Guillou 06, theorem 3.12](#Guillou06))

For the case that $\mathcal{C}$ is the [[classical model structure on topological spaces]] this yields the [[fine model structure on topological G-spaces]].

Write $Orb_G$ for the [[orbit category]] of $G$.

Write $(\mathcal{C}^{Orb_G^{op}})_{proj}$ for the projective global [[model structure on functors]] from the $G$-[[orbit category]] to $\mathcal{C}$. 


+-- {: .num_defn}
###### Proposition

There is a pair of [[adjoint functors]]

$$
  (\Theta, \Phi)
    \;\colon\;
  G\mathcal{C}
   \stackrel{\overset{\Theta}{\longleftarrow}}{\underset{\Phi}{\longrightarrow}}
  \mathcal{C}^{Orb_G^{op}}
$$

where $\Phi X \colon G/H \mapsto X^H$ assigns fixed-point objects and where $\Theta S$ has as underlying object $S(G/1)$.

This constitutes a [[Quillen equivalence]] between the above model structures

$$
  (\Theta, \Phi)
    \;\colon\;
  G\mathcal{C}_{fine}
    \underset{Quillen}{\simeq}
  \mathcal{C}^{Orb_G^{op}}_{proj}
 \,.
$$

=--

([Guillou 06, prop. 3.15](#Guillou06), [Stephan 13, Theorem 3.17](#Stephan13))


## Generalizations

1. Elmendorf's theorem may be generalized to the case where only a sub-family $\mathcal{H}$ of the closed subgroups of $G$ is considered ([Stephan 10](#Stephan10), also [May 96](#May96)).

1. There is an evident generalization of the [[orbit category]] of a fixed group $G$ to the _[[global orbit category]]_. Under this generalization an analog of Elmendorf's theorem plays a central role in [[global equivariant homotopy theory]] ([Rezk 14](#Rezk14)).

1. The orbit category for $G$ can also be generalized to the orbit category generated by any small category, $I$, where the $I$-orbits are $I$-diagrams in $Top$ whose strict colimit is equal to a point. If the orbits are either small or complete, then the $I$-equivariant model structure is Quillen-equivalent to a presheaf category (see pt. 11 of p. 8 of [PHCTIntro](Parametrized+Higher+Category+Theory+and+Higher+Algebra#PHCTIntro) and [Chorny13](#Chorny13)).





## Related concepts

* [[G-CW approximation]]

* [[equivariant Whitehead theorem]]

* [[tom Dieck splitting]]

* [[global equivariant homotopy theory]]

* [[Bredon cohomology]]

* [[equivariant rational homotopy theory]]

  * [[model structure on equivariant connective dgc-algebras]]

  * [[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]]

  * [[fundamental theorem of dg-algebraic equivariant rational homotopy theory]]

## References
 {#References}

Lecture notes on Elmendorf's theorem:

* {#Blumberg17} [[Andrew Blumberg]], Section 1.3 of: _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


The "fine" homotopical structure on [[G-spaces]] (with fixed-point-wise weak equivalences) is originally due to

* {#Bredon67} [[Glen Bredon]], _[[Equivariant cohomology theories]]_, Springer Lecture Notes in Mathematics Vol. 34. 1967.

The equivalence of its [[homotopy category]] to that of presheaves over the orbit category is then due to:

* {#Elmendorf83} [[Anthony Elmendorf]], _Systems of fixed point sets_, Trans. Amer. Math. Soc., 277(1):275&#8211;284, 1983 ([jstor:1999356](https://www.jstor.org/stable/1999356))



Enhancement of Elmendorf's equivalence of homotopy categories to an [[sSet]]-[[enriched adjunction]] and/or to a [[Quillen equivalence]] of [[model categories]] based on the [[classical model structure on topological spaces]] and/or the [[classical model structure on simplicial sets]]:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]], _Singular functors and realization functors_, Indagationes Mathematicae (Proceedings) Volume 87, Issue 2, 1984, Pages 147-153 (<a href="https://doi.org/10.1016/1385-7258(84)90016-7">doi:10.1016/1385-7258(84)90016-7</a>)

* {#CordierPorter96} [[Jean-Marc Cordier]], [[Timothy Porter]], Thm. 3.11 of: _Categorical Aspects of Equivariant Homotopy_, Applied Cat. Structures, **4** (1996) 195 - 212 ([doi:10.1007/BF00122252](https://doi.org/10.1007/BF00122252)) (Proceedings of the European Colloquium of Category Theory, 1994)

* {#Guillou06} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_, 2006 ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouEquivariantHomotopy.pdf:file]])

* {#Stephan10} [[Marc Stephan]], 

  _Elmendorf’s Theorem via Model Categories_,  2010 ([pdf](http://web.math.ku.dk/~jg/students/stephan.msproject.2010.pdf)) 

  _Elmendorf’s Theorem for Cofibrantly Generated Model Categories_, MS thesis, Z&uuml;rich 2010 ([pdf](http://web.math.ku.dk/~jg/students/stephan.msthesis.2010.pdf))

* {#Stephan13} [[Marc Stephan]], _On equivariant homotopy theory for model categories_, Homology Homotopy Appl. 18(2) (2016) 183-208 ([arXiv:1308.0856](http://arxiv.org/abs/1308.0856), [doi:10.4310/HHA.2016.v18.n2.a10](https://dx.doi.org/10.4310/HHA.2016.v18.n2.a10))

* {#GuillouMayRubin13} [[Bertrand Guillou]], [[Peter May]], [[Jonathan Rubin]], Sections 1 and 5.2 in: _Enriched model categories in equivariant contexts_, Homology, Homotopy and Applications 21 (1), 2019 ([arXiv:1307.4488](https://arxiv.org/abs/1307.4488), [doi:10.4310/HHA.2019.v21.n1.a10](https://dx.doi.org/10.4310/HHA.2019.v21.n1.a10))

Other discussions generalizing [Elmendorf 83](#Elmendorf83) (i.e. the equivalence of homotopy categories)  to general topological equivariance groups:

* {#Piacenza91} [[Robert Piacenza]], Section 6 of: _Homotopy theory of diagrams and CW-complexes over a category_, Can. J. Math. Vol 43 (4), 1991 ([doi:10.4153/CJM-1991-046-3](https://doi.org/10.4153/CJM-1991-046-3), [[Piazenza91.pdf:file]])

* {#May96} [[Peter May]] et al., Section V.3 of: _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics Volume: 91; 1996 ([ISBN:978-0-8218-0319-6](https://bookstore.ams.org/cbms-91), [pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf), [pdf](https://ncatlab.org/nlab/files/MayEtAlEquivariant96.pdf))

More on the approach of [Dwyer-Kan 84](#DwyerKan84):

* [[Emmanuel Dror Farjoun]], Prop. 1.3 in: _Homotopy Theories for Diagrams of Spaces_, Proceedings of the AMS, Vol. 101, No. 1 (Sep., 1987), pp. 181-189 ([jstor:2046572 ](https://www.jstor.org/stable/2046572 ))

* {#Chorny13} [[Boris Chorny]], _Homotopy  theory  of  relative  simplicial  presheaves_,  Israel J. Math. 205 (2015), no. 1, 471–484, ([arXiv:1310.2932](https://arxiv.org/abs/1310.2932))

These Elmendorf-theorem [[Quillen equivalences]] (as in [Stephan 13](#Stephan13)) apply to other [[model categories]], and yield Elmendorf-like equivalences in other contexts:

* [[Jonathan Rubin]], _Elmendorf constructions for G-categories and G-posets_ ([arXiv:2006.08876](https://arxiv.org/abs/2006.08876))

See also related discussion of "[[orbispaces]]", starting with:

* [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916)),

relating to [[global equivariant homotopy theory]]:

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

and then to [[orbifolds]]:

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))



An n-cat café discussion initiated by [[John Huerta]] and probing some of its uses in Mathematical Physics, can be found [here](https://golem.ph.utexas.edu/category/2018/06/elmendorfs_theorem.html#more), following

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, Comm. Math. Phys. 371: 425. (2019 ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987), [doi:10.1007/s00220-019-03442-3](https://doi.org/10.1007/s00220-019-03442-3))

Some generalization to [[monoid]]-[[actions]]:

* Mehmet Akif Erdal, *Homotopy theory of monoid actions via group actions and an Elmendorf style theorem*, Collectanea Mathematica (2022) &lbrack;[arXiv 1609.06785](https://arxiv.org/abs/1609.06785), [doi:10.1007/s13348-022-00388-z](https://doi.org/10.1007/s13348-022-00388-z)&rbrack;



[[!redirects Elmendorf theorem]]

[[!redirects model structure on equivariant simplicial sets]]
[[!redirects model structures on equivariant simplicial sets]]

[[!redirects model structure on topological G-spaces]]
[[!redirects model structures on topological G-spaces]]
