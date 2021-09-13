
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

> under construction

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[topological group]], there exists a [[model category]]-[[mathematical structure|structure]] on the [[category]] of [[topological G-spaces]] whose [[weak equivalences]] and [[fibrations]] are those morphisms whose [[underlying]] [[continuous functions]] between $H$-[[fixed loci]], for all [[closed subgroups]] $H \subset_{clsd} G$, are weak equivalences or fibrations, respectively, in the [[classical model structure on topological spaces]], hence [[weak homotopy equivalences]] or [[Serre fibrations]], respectively.

In the case that $G$ is a [[compact Lie group]], the corresponding [[homotopy theory]] coincides with that of [[G-CW complexes]] [[localization|localized]] at $G$-equivariant [[homotopy equivalences]].

For general $G$, [[Elmendorf's theorem]] asserts that this is [[Quillen equivalence|Quillen equivalent]] to the [[model category of simplicial presheaves]] on the [[orbit category]] of $G$ (...).

## Definition

Throughout, we write

* [[TopologicalSpaces|TopSp]] for the [[conventient category of topological spaces|convenient category]] of [[compactly generated weak Hausdorff spaces]];

* $TopSp_{Qu}$ for its [[classical model structure on topological spaces]] ([here](classical+model+structure+on+topological+spaces#ModelStructureOnCompactlyGeneratedTopologicalSpaces));

* $G \,\in\, Grp(CptSmthMfd) \xrightarrow{\;} Grp(TopSp)$ for the [[underlying]] [[topological group]] of a [[compact Lie group]];

* $G Act(TopSp)$ for the [[category]] of [[continuous function|continuous]] $G$-[[group action|actions]], hence for the category of [[topological G-spaces]] with [[continuous function|continuous]] [[equivariant functions]] between them.


\begin{proposition}\label{FineModelStructureOnGSpaces}
**(fine model structure on $G$-spaces)**
\linebreak
  There is a [[model category]]-[[mathematical structure|structure]] 
$G Act\big(TopSp_{Qu}\big)_{fine}$ in [[topological G-spaces]] whose [[weak equivalences]] and [[fibrations]] are those [[morphisms]] $f \,\colon\, X \xrightarrow{\;} Y$ such that for each [[closed subgroup]] $H \,\underset{clsd}{\subset}\, G$ their ([[corestriction|co-]])[[restriction]] $f^H \,\colon\, X^H \xrightarrow{\;} Y^H$ to the  $H$-[[fixed loci]] is, respectivelhy, a [[weak equivalence]] or [[fibration]] in the [[classical model structure on topological spaces]], hence a [[weak homotopy equivalence]] or [[Serre fibration]].
\end{proposition}


## Properties


\begin{prop}\label{TheFineModelStructure}
  The model category $G Act\big( TopSp_{Qu}\big)_{fine}$ (Prop. \ref{FineModelStructureOnGSpaces}) is 

1. {#CofibrantGeneration} a [[cofibrantly generated model category]] with generating (acyclic) cofibrations the images under forming [[products]] ([[k-ification|k-ified]] [[topological product spaces]]) of [[coset spaces]] $G/H$ with the classical generating cofibrations ([here](classical+model+structure+on+topological+spaces#TopologicalGeneratingCofibrations) and [here](classical+model+structure+on+topological+spaces#TopologicalGeneratingAcyclicCofibrations)):

   \[
     \label{GeneratingCofibrations}
     \begin{aligned}
     J_{G Top} 
       &\;\coloneqq\;
     \big\{
       G/H \times D^n \xhookrightarrow G/H \times D^n \times I
     \big\}
     \\
     I_{G Top} 
       &\;\coloneqq\;
     \big\{
       G/H \times D^n \xhookrightarrow G/H \times D^n \times I
     \big\}
     \end{aligned}
   \]

1. an [[enriched model category]] over $TopSp_{Qu}$ with [[hom-objects]] given by the $G$-[[fixed loci]] of the [[conjugation action]] on the [[mapping spaces]], hence such that
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
\end{prop}
This is part of a special case of [Guillou, May & Rubin 2013, Thm 3.7](#GuillouMayRubin13).


\begin{proposition}
  For $X \,\in\, G Act\big(TopSp_{Qu}\big)_{fine}$ a [[G-CW complex]], the [[functor]] which assigns [[mapping spaces]] out of $X$ equipped with the [[conjugation action]], is a [[right Quillen functor]], hence make a [[Quillen adjunction]] together with the [[functor]] of taking [[product]] with $X$ (the [[k-ification|k-ified]] [[topological product space]]) equipped with the [[diagonal action]]:
$$
  G Act\big( TopSp_{Qu}\big)_{fine}
    \underoverset
    {\underset{Maps(X,-)}{\longrightarrow}}
    {\overset{X \times (-)}{\longleftarrow}}
    {\bot_{\mathrlap{Qu}}}
  G Act\big( TopSp_{Qu}\big)_{fine}
  \mathrlap{\,.}
$$
\end{proposition}
\begin{proof}
  Let $f \,\colon\, A \xrightarrow{\;} B$ be a ([[acyclic fibration|acyclic]]) [[fibration]]. It is sufficient to to show that $Maps(X,f)$ is an (acyclic) fibration in $G Act\big( TopSp_{Qu}\big)_{fine}$, hence that $Maps(X,f)^H$ is an (acyclic) fibration in $TopSp_{Qu}$ for every $H \underset{clsd}{\subset} G$. But the latter may be identified with
$$
  Maps(X,f) \,=\, Maps\big( G/H \,\times\, X  \big)^{ G }
  \,.
$$
It is now sufficient to see that $G/H \times X$ is cofibrant, because then (eq:EnrichmentOverTopologicalSpaces) implies that the right hand side is an (acyclic) fibration.

Since [[G-CW complexes]] are cofibrant by (eq:GeneratingCofibrations), and since $G/H$ is a $G$-CW-complex (evidently) as is $X$ (by assumption), it is sufficient to observe that taking products preserves $G$-CW complexes. This is true for $G$ a [[compact Lie group]], by the [[equivariant triangulation theorem]] for [[G-manifolds]].
\end{proof}


## Related concepts

* [[Borel model structure]]

* [[equivariant homotopy theory]]

* [[Elmendorf's theorem]]

## References

For the moment, see the references and discussion at *[[Elmendorf's theorem]]* for more.

The original article:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]], Section 1.2 of: _Singular functors and realization functors_, Indagationes Mathematicae (Proceedings) Volume 87, Issue 2, 1984, Pages 147-153 (<a href="https://doi.org/10.1016/1385-7258(84)90016-7">doi:10.1016/1385-7258(84)90016-7</a>)

Further discussion:

* {#GuillouMayRubin13} [[Bertrand Guillou]], [[Peter May]], [[Jonathan Rubin]], Theorem 1.6 in: _Enriched model categories in equivariant contexts_, Homology, Homotopy and Applications 21 (1), 2019 ([arXiv:1307.4488](https://arxiv.org/abs/1307.4488), [doi:10.4310/HHA.2019.v21.n1.a10](https://dx.doi.org/10.4310/HHA.2019.v21.n1.a10))


