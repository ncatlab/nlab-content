
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[topological group]], there exists a [[model category]]-[[mathematical structure|structure]] on the [[category]] of [[topological G-spaces]] whose [[weak equivalences]] and [[fibrations]] are those morphisms whose [[underlying]] [[continuous functions]] between $H$-[[fixed loci]], for all [[closed subgroups]] $H \subset_{clsd} G$, are weak equivalences or fibrations, respectively, in the [[classical model structure on topological spaces]], hence [[weak homotopy equivalences]] or [[Serre fibrations]], respectively. Hence the weak equivalences are the [[equivariant weak homotopy equivalences]].

In the case that $G$ is a [[compact Lie group]], the corresponding [[homotopy theory]] coincides with that of [[G-CW complexes]] [[localization|localized]] at $G$-[[equivariant function|equivariant]] [[homotopy equivalences]]. 

For general $G$, [[Elmendorf's theorem]] asserts that the fine equivariant model structure is [[Quillen equivalence|Quillen equivalent]] to the [[model category of simplicial presheaves]] on the [[orbit category]] of $G$.

All this makes the fine model structure serve as a foundation for [[equivariant homotopy theory]] and for [[equivariant cohomology]] in its refined form subsuming [[Bredon cohomology]].

This is in contrast to the "coarse" or *[[Borel model structure]]* whose [[weak equivalences]] are simply the underlying [[weak homotopy equivalences]] (which need not restrict to weak homotopy equivalences on all [[fixed loci]]). The coarse Borel model structure instead presents the [[slice (infinity,1)-category|slice]] homotopy theory over the [[classifying space]] $B G$. The intrinsic [[cohomology]] of this coarse [[equivariant homotopy theory]] is just "Borel equivariant", hence computes cohomology of [[Borel constructions]].

While one may, therefore, think of the fine model structure as exhibiting "genuine" equivariance (e.g. [Guillou, May & Rubin 13, p. 14-15](#GuillouMayRubin13)), beware that the term "genuine equivariant homotopy theory" has come to be adopted for something yet a little richer, namely to [[equivariant stable homotopy theory]] whose [[G-spectra]] are in addition equipped with "transfer maps".

However, when the [[closed subgroups]] of $G$ that enter the definition of the fine model structure are taken to be [[compact groups]], then it is not wrong to speak of *[[proper equivariant homotopy theory]]* (conflating two usages of the term "proper", but in a sensible way).

## Definition

Throughout, we write

* [[TopologicalSpaces|TopSp]] for the [[conventient category of topological spaces|convenient category]] of [[compactly generated weak Hausdorff spaces]];

* $TopSp_{Qu}$ for its [[classical model structure on topological spaces]] ([here](classical+model+structure+on+topological+spaces#ModelStructureOnCompactlyGeneratedTopologicalSpaces));

* $G \,\in\, Grp(CptSmthMfd) \xrightarrow{\;} Grp(TopSp)$ for the [[underlying]] [[topological group]] of a [[compact Lie group]]

  (most of the following statements hold for general [[topological groups]], at least if some further qualifications are added)

* $G Act(TopSp)$ for the [[category]] of [[continuous function|continuous]] $G$-[[group action|actions]], hence for the category of [[topological G-spaces]] with [[continuous function|continuous]] [[equivariant functions]] between them.



\begin{proposition}\label{FineModelStructureOnGSpaces}
**(fine model structure on $G$-spaces)**
\linebreak
  There is a [[model category]]-[[mathematical structure|structure]] 
$G Act\big(TopSp_{Qu}\big)_{fine}$ on [[topological G-spaces]] whose [[weak equivalences]] and [[fibrations]] are those [[morphisms]] $f \,\colon\, X \xrightarrow{\;} Y$ such that for each [[closed subgroup]] $H \,\underset{clsd}{\subset}\, G$ their ([[corestriction|co-]])[[restriction]] $f^H \,\colon\, X^H \xrightarrow{\;} Y^H$ to the  $H$-[[fixed loci]] is, respectivelhy, a [[weak equivalence]] or [[fibration]] in the [[classical model structure on topological spaces]], hence a [[weak homotopy equivalence]] or [[Serre fibration]].
\end{proposition}

([Dwyer & Kan 1984, 1.2](#DwyerKan84))


## Properties

### Cofibrant generation, enrichment and properness

\begin{prop}\label{BasicPropertiesOfTheFineModelStructure}
  The model category $G Act\big( TopSp_{Qu}\big)_{fine}$ (Prop. \ref{FineModelStructureOnGSpaces}) is:

1. {#CofibrantGeneration} [[proper model category|proper]] and [[cofibrantly generated model category]] with generating (acyclic) cofibrations the images under forming [[products]] ([[k-ification|k-ified]] [[product topological spaces]]) of [[coset spaces]] $G/H$ with the classical generating cofibrations ([here](classical+model+structure+on+topological+spaces#TopologicalGeneratingCofibrations) and [here](classical+model+structure+on+topological+spaces#TopologicalGeneratingAcyclicCofibrations)):

   \[
     \label{GeneratingCofibrations}
     \begin{aligned}
     I_{G Top} 
       &\;\coloneqq\;
     \big\{
       G/H \times S^{n-1} \xhookrightarrow{\;} G/H \times D^n 
     \big\}_{n \in \mathbb{N}, H \underset{clsd}{\subset} G}
     \\
     I_{G Top} 
       &\;\coloneqq\;
     \big\{
       G/H \times D^n \xhookrightarrow{\;} G/H \times D^n \times I
     \big\}_{n \in \mathbb{N}, H \underset{clsd}{\subset} G}
     \end{aligned}
   \]

   ([Guillou 2006, Prop. 3.12](#Guillou06); [Fausk 2008, Prop. 2.11](#Fausk08); [Stephan 2013, Prop. 2.6](#Stephan13))

1. in addition an [[enriched model category]] over [[classical model structure on topological spaces|$TopSp_{Qu}$]] with [[hom-objects]] given by the $G$-[[fixed loci]] of the [[conjugation action]] on the [[mapping spaces]], hence such that
   \[
     \label{EnrichmentOverTopologicalSpaces}
     Maps(-,-)^G 
       \;\colon\;
     G Act\big(TopSp_{Qu}\big)_{fine}^{op}
       \times
     G Act\big(TopSp_{Qu}\big)_{fine}^{op}
      \xrightarrow{\;}
     TopSp_{Qu}
   \]
   is a [[Quillen bifunctor]].

   ([Guillou, May & Rubin 2013, Thm 3.7](#GuillouMayRubin13); [Schwede 2018, Prop. B.7](#Schwede18); [DHLPS 2019, Prop. 1.1.3 (i-ii) ](#DHLPS19))

\end{prop}

\begin{remark}\label{SpecializationToBorelModelStructure}
**(specialization to [[Borel model structure]])**
\linebreak
The direct analog of Prop. \ref{FineModelStructureOnGSpaces}, Prop. \ref{BasicPropertiesOfTheFineModelStructure} holds for any choice of family of closed subgroups of $G$. In the case that the family contains only the [[trivial group]] $1 \subset G$ the result is the topological [[Borel model structure]]. 
\end{remark}

\begin{corollary}\label{GCWComplexesAreCofibrant}
  Evey [[G-CW complex]] (being, by definition, a special [[cell complex]] in the generating cofibrations (eq:GeneratingCofibrations)) is a [[cofibrant object]] in the fine equivariant model structure.
\end{corollary}

The $TopSp_{Qu}$ enrichment of Prop. \ref{BasicPropertiesOfTheFineModelStructure} in fact underlies a model enrichment of $G Act(TopSp_{Qu})_{fine}$ over itself:

\begin{prop}\label{MonoidalModelCategoryStructure}
**([[cartesian monoidal category|cartesian]] [[monoidal model category]] structure)** \linebreak
  The model category $G Act\big( TopSp_{Qu}\big)_{fine}$ (Prop. \ref{FineModelStructureOnGSpaces}) is a [[cartesian monoidal category|cartesian]] [[monoidal model category]] in that it satisfies the [[pushout-product axiom]] with respect to [[Cartesian product]] of ([[compactly generated topological space|cgwh]]) $G$-spaces.
\end{prop}
(Observe that the [[unit axiom]] is automatic, by [this Prop.](monoidal+model+category#CaseOfCofibrantTensorUnit), since the [[tensor unit]] -- which here is the [[point space]] equipped with the [[trivial action]] -- is clearly a [[G-CW complex]], $\ast \simeq G/G$, and hence [[cofibrant object|cofibrant]], by Cor. \ref{GCWComplexesAreCofibrant}.)
\begin{proof}
Prop. \ref{MonoidalModelCategoryStructure} seems to have been [[folklore]] statement, based on the fact that the [[equivariant triangulation theorem]] implies that [[products]] of [[coset spaces]] $G/H_2 \,\times\, G/H_2$ admit an [[G-CW complex]]-structure (crucially using here that $G$ is assumed to be a [[Lie group]], so that its [[coset spaces]] have the structure of [[smooth manifolds]] with [[smooth function|smooth]] [[group actions]].) The required argument to make this into a proof of monoidal model category structure is spelled out as [DHLPS 2019, Prop. 1.1.3 (iii)](#DHLPS19), there in the further generality of [[proper equivariant homotopy theory]]. (Under the above assumption that $G$ is not just a Lie group but a [[compact Lie group]], the classes of "$\mathcal{Com}$-cofibrations" and of "$G$-cofibrations" in [DHLPS 19, Def. 1.1.2](#DHLPS19) agree, since [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]).
\end{proof}

Prop. \ref{MonoidalModelCategoryStructure} immediately implies (by [this general Prop.](monoidal+model+category#InternalHomQuillenAdjunction)):
\begin{proposition}
  \label{InternalHomQuillenAdjunction}
**([[internal hom]] [[Quillen adjunction]])**
\linebreak
  For $X \,\in\, G Act\big(TopSp_{Qu}\big)_{fine}$ a [[cofibrant object]], the [[functor]] which assigns [[mapping spaces]] out of $X$ equipped with the [[conjugation action]], is a [[right Quillen functor]], hence makes a [[Quillen adjunction]] together with the [[functor]] of taking the [[product]] with $X$ (the [[k-ification|k-ified]] [[product topological space]]) equipped with the [[diagonal action]]:
\[
  G Act\big( TopSp_{Qu}\big)_{fine}
    \underoverset
    {\underset{Maps(X,-)}{\longrightarrow}}
    {\overset{X \times (-)}{\longleftarrow}}
    {\bot_{\mathrlap{Qu}}}
  G Act\big( TopSp_{Qu}\big)_{fine}
  \mathrlap{\,.}
\]
\end{proposition}


## Related concepts

* [[Borel model structure]]

* [[equivariant homotopy theory]]

* [[Elmendorf's theorem]]

## References


The model structure itself was first discussed in:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]], Section 1.2 of: _Singular functors and realization functors_, Indagationes Mathematicae (Proceedings) Volume 87, Issue 2, 1984, Pages 147-153 (<a href="https://doi.org/10.1016/1385-7258(84)90016-7">doi:10.1016/1385-7258(84)90016-7</a>)



Further properties, such as cofibrant generation, properness, and topological enrichment and are established in:

* {#Guillou06} [[Bert Guillou]], Prop. 3.12 in: _A short note on models for equivariant homotopy theory_, 2006 ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouEquivariantHomotopy.pdf:file]])


* {#Fausk08} [[Halvard Fausk]], Prop. 2.11 in: *Equivariant homotopy theory for pro-spectra*,  Geom. Topol. 12 (2008) 103-176 ([doi:10.2140/gt.2008.12.103](http://dx.doi.org/10.2140/gt.2008.12.103), [arXiv:math/0609635](https://arxiv.org/abs/math/0609635))

* {#GuillouMayRubin13} [[Bertrand Guillou]], [[Peter May]], [[Jonathan Rubin]], Theorem 1.6 in: _Enriched model categories in equivariant contexts_, Homology, Homotopy and Applications 21 (1), 2019 ([arXiv:1307.4488](https://arxiv.org/abs/1307.4488), [doi:10.4310/HHA.2019.v21.n1.a10](https://dx.doi.org/10.4310/HHA.2019.v21.n1.a10))

* {#Stephan13} [[Marc Stephan]], _On equivariant homotopy theory for model categories_, Homology Homotopy Appl. 18(2) (2016) 183-208 ([arXiv:1308.0856](http://arxiv.org/abs/1308.0856), [doi:10.4310/HHA.2016.v18.n2.a10](https://dx.doi.org/10.4310/HHA.2016.v18.n2.a10))


* {#Schwede18} [[Stefan Schwede]], Prop. B.7 in: _[[Global homotopy theory]]_, New Mathematical Monographs **34** Cambridge University Press, 2018 ([doi:10.1017/9781108349161](https://doi.org/10.1017/9781108349161), [arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

In addition, the monoidal model category structure is made explicit (in the generality of [[proper equivariant homotopy theory]]) in:

* {#DHLPS19} [[Dieter Degrijse]], [[Markus Hausmann]], [[Wolfgang Lück]], [[Irakli Patchkoria]], [[Stefan Schwede]], Prop. 1.1.3 in: _Proper equivariant stable homotopy theory_, Memoirs of the AMS ([arXiv:1908.00779](https://arxiv.org/abs/1908.00779))

For more see [the references](Elmendorf's+theorem#References) at *[[Elmendorf's theorem]]*.



