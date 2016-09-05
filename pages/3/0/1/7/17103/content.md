
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


The notion of _CW-spectrum_ is the analogue for [[sequential spectra]] in [[Top]] of the concept of [[CW-complex]] for [[topological spaces]].

Just like [[CW-complexes]] are cofibrant objects in the [[classical model structure on topological spaces]], so CW-spectra are cofibrant objects in the [[stable model category|stable]] [[model structure on topological sequential spectra]], see [below](#Cofibrancy).

## Definition

### In components

+-- {: .num_defn #CWSpectrum}
###### Definition

A **CW-spectrum** $X_\bullet\in SeqSpec(Top)$ is a [[sequential spectrum]] in [[Top]] such that

1. all component spaces $X_n$ are [[CW-complexes]], 

1. all structure maps $\Sigma X_n \longrightarrow X_{n+1}$ are inclusions of subcomplexes 

=--

e.g. ([Adams 74, p. 139](#Adams74)) Beware that for instance ([Switzer 75, def. 8.1](#Switzer75)) says just "spectrum" for "CW-spectrum".

For a CW-spectrum $X$ there is a concept of "cell of a spectrum": 

+-- {: .num_defn #CellOfACWSpectrum}
###### Definition

A **cell** of a CW-spectrum, def. \ref{CWSpectrum} is a cell of one of the components CW-complexes $X_n$, together with all its suspensions in all the higher component spaces $X_{\gt n}$, subject to the condition that the first cell itself is not itself the suspension of a cell in $X_{n-1}$.

=--

This way every CW-spectrum is the union of all its cells in the sense of def. \ref{CellOfACWSpectrum}. (e.g. [Switzer 75, 8.4](Switzer75)).

+-- {: .num_defn }
###### Definition

A CW-spectrum, def. \ref{CWSpectrum}, is called a _[[finite spectrum]]_ (or countable spectrum, etc.) if it has [[finite number|finitely many]] cells (countably many cells) according to def. \ref{CellOfACWSpectrum}.

=--


### Via spectrum attaching maps


+-- {: .num_defn #SphereSpectrumOfIntegerDimension}
###### Definition

For $n \in \mathbb{Z}$ (possibly negative) define $\mathbb{S}^n$ to be the [[sequential prespectrum]] with component spaces

$$
 (\mathbb{S}^{n})_k
   \coloneqq
 \left\{
   \array{
     S^{k+n} & if \; k + n \geq 0
     \\
     \ast & otherwise
   }
 \right.
$$

and with structure maps the canonical isomorphisms. 

=--
 
([Lewis-May-Steinberger 86, def. 4.3](#LewisMaySteinberger86))

+-- {: .num_defn}
###### Remark

In def. \ref{SphereSpectrumOfIntegerDimension} 

* for $n = 0$ then $\mathbb{S}^0 = \mathbb{S} = \Sigma^\infty S^0$ is standard sequential incarnation of the [[sphere spectrum]];

* for $n \geq n$ then $\mathbb{S}^n \simeq \Sigma^\infty S^n$ is the [[suspension spectrum]] on the [[n-sphere]];

* for general $n$ then $\mathbb{S}^n \simeq F_{-n} S^0$ is also known as the $(-n)$th [[free spectrum]] on $S^0$.

=--

+-- {: .num_defn }
###### Definition

A **[[cell spectrum]]** is a topological [[sequential spectrum]] $X$ realized as the [[colimit]] over a sequence of spectra $\ast = X_0 \to X_1 \to X_2 \to X_3 \to \cdots$ such that there are morphisms

$$
  j_n 
   \;\colon\; 
   \left(
      \underset{i \in I_n}{\sqcup} \mathbb{S}^{q_n}
   \right)
   \longrightarrow
   X_n
$$

with $X_{n+1}= Cone(j_n)$ (the [[mapping cone]]).

([rmk.](Introduction+to+Stable+homotopy+theory+--+1-1#StrictModelStructureCellAttachmentToSpectra))

A cell spectrum is a **CW-spectrum** if each attaching map $\Sigma^\infty S^{q_n}\to X_n$ factors through a $X_k \to X_n$ with $k \lt q$.

=--

(e.g. [Lewis-May-Steinberger 86, def. 5.1, def. 5.2](#LewisMaySteinberger86), [Weiss](#Weiss))

### Category of CW-spectra
There is an obvious category of CW-spectra given as the full subcategory $CWSpec'$ of $SeqSpec(Top)$ consisting of the CW-spectra, ie. a morphism of CW-spectra $f: X \to Y$ is given by levelwise maps $f_n: X_n \to F_n$ that are compatible with the structure maps. In accordance with [Switzer 75, 8.9](Switzer75), we call morphisms in this sense **functions**.

However, often there is a more useful notion of morphisms between CW-spectra. 

+-- {: .num_defn}
###### Definition
Let $E$ be a CW-spectrum. A **subspectrum** is a CW spectrum $F$ such that each $F_n$ is a subcomplex of $E_n$. A subspectrum is **cofinal** if for each cell $e_n \in E_n$, there is some $m$ such that $\Sigma^m e_n \in F_{n + m}$.
=--

We can then construct the category $CWSpec$ as the [[localization]] of $CWSpec'$ at the cofinal inclusions. Since the class of cofinal inclusions admit a [[calculus of right fractions]], the cateogry $CWSpec$ has the following concrete description - a morphism $X \to Y$ in $CWSpec$ is given by a function $\tilde{X} \to Y$, where $\tilde{X}$ is some cofinal subspectrum of $X$, quotiented by the relation that two such morphisms $f: \tilde{X} \to Y$ and $f': \tilde{X}' \to Y$ are considered equivalent if there is some further cofinal subspectrum $\tilde{X}'' \subseteq \tilde{X} \cap \tilde{X'}$ such that $f|_{\tilde{X}'} = f'|_{\tilde{X}''}$.

## Properties

### Cofibrancy
 {#Cofibrancy}

+-- {: .num_prop}
###### Proposition

A [[sequential spectrum]] $X\in SeqSpec(Top)_{stable}$ is cofibrant in the stable [[model structure on topological sequential spectra]] in particular if all component spaces are [[cell complexes]] and all its structure morphisms $S^1 \wedge X_n \to X_{n+1}$ are [[relative cell complexes]]. In particular [[CW-spectra]], def. \ref{CellOfACWSpectrum}, are cofibrant in $SeqSpec(Top)_{stable}$.

=--

For the proof see [there](model+structure+on+topological+sequential+spectra#CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra).

+-- {: .num_prop}
###### Proposition

For $X\in SeqSpec(Top)_{stable}$ a [[CW-spectrum]], then its standard [[cylinder spectrum]] $X \wedge (I_+)$ is a _good_ [[cylinder object]], in that the inclusion

$$
  X \vee X \longrightarrow X \wedge (I_+)
$$

is a cofibration in $SeqSpec(Top)_{stable}$.

=--

See [this prop.](model+structure+on+topological+sequential+spectra#CylinderSpectrumOverCWSpectrumIsGood).

### CW-approximation
 {#CWApproximation}

The analog of [[CW-approximation]] for [[topological spaces]] holds true for topological [[sequential spectra]]:

+-- {: .num_prop}
###### Proposition

For $X \in SeqSpec(Top)$ a topological [[sequential spectrum]], there exists a CW-spectrum $\hat X$ and a [[stable weak homotopy equivalence]]

$$
 \hat X \longrightarrow X
 \,.
$$

=--

(e.g. [Elmendorf-Kriz-May 95, theorem 1.5](#ElmendorfKrizMay95))

+-- {: .proof}
###### Proof 1

First let $\hat X_0 \longrightarrow X_0$ be a CW-approximation of the component space in degree 0, via [this prop.](CW+approximation#CWApproximationForContinuousFunctions). Then proceed by [[induction]]: suppose that for $n \in \mathbb{N}$ a [[CW-approximation]] $\phi_{k \leq n} \colon  \hat X_{k \leq n} \to X_{k \leq n}$ has been found such that all the structure maps are respected. Consider then the continuous function

$$
  \Sigma \hat X_n \overset{\Sigma \phi_n}{\longrightarrow} \Sigma X_n \overset{\sigma_n}{\longrightarrow} X_{n+1}
  \,.
$$

Applying [that prop.](CW+approximation#CWApproximationForContinuousFunctions) to this function factors it as

$$
  \Sigma X_n \hookrightarrow \hat X_{n+1} \overset{\phi_{n+1}}{\longrightarrow} X_{n+1}
  \,.
$$

Hence we have obtained the next stage of the CW-approximation. The respect for the structure maps is just this factorization property:

$$
  \array{  
    \Sigma \hat X_n 
      &\overset{\Sigma \phi_n}{\longrightarrow}& 
    \Sigma X_n
    \\
    {}^{incl}\downarrow && \downarrow^{\mathrlap{\sigma_n}}
    \\
    \hat X_{n+1} &\underset{\phi_{n+1}}{\longrightarrow}& X_{n+1}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof 2

A high-powered way to see this is to use the [[Quillen equivalence]] between the stable [[model structure on topological sequential spectra]] and the stable [[Bousfield-Friedlander model structure]] (see there) on sequential spectra in [[simplicial sets]]. This implies that a CW-approximation is given by

$$
  {\vert Q Sing X\vert}
  \overset{\in W_{stable}}{\longrightarrow}
  X
  \,,
$$ 

where ${\vert - \vert} \dashv Sing$ is degreewise the adjunction between [[geometric realization]] and forming [[singular simplicial complex]], and $Q$ denotes any cofibrant replacement in the BF-model structure.

=--


## References

* {#Adams74} [[Frank Adams]], section III.2 and III.3 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 1 of _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_,  1995 Amsterdam: North-Holland, pp. 213&#8211;253,   ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#Weiss} [[Michael Weiss]], around pages 43-46 of _Homotopy theory and bordism theory_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/abdnbordism.pdf))
 
Discussion in the generality of [[equivariant spectra]] is in 

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and M. Steinberger (with contributions by J.E. McClure), section I.5 of _Equivariant stable homotopy theory_ Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))


[[!redirects CW spectra]]

[[!redirects CW-spectrum]]
[[!redirects CW-spectra]]

[[!redirects CW spectrum]]
