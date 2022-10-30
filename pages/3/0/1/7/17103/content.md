
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

+-- {: .num_defn #CWSpectrum}
###### Definition

A **CW-spectrum** $X_\bullet\in SeqSpec(Top)$ is a [[sequential spectrum]] in [[Top]] such that

1. all component spaces $X_n$ are [[CW-complexes]], 

1. all structure maps $\Sigma X_n \longrightarrow X_{n+1}$ are inclusions of subcomplexes 

=--

e.g. ([Adams 74, p. 139](#Adams74)) Beware that for instance ([Switzer 75, def. 81](#Switzer75)) says just "spectrum" for "CW-spectrum".

For a CW-spectrum $X$ there is a concept of "cell of a spectrum": 

+-- {: .num_defn #CellOfACWSpectrum}
###### Definition

A **cell** of a CW-spectrum, def. \ref{CWSpectrum} is a cell of one of the components CW-complexes $X_n$, together with all its suspensions in all the higher component spaces $X_{\gt n}$, subject to the condition that the first cell itself is not itself the suspension of a cell in $X_{n-1}$.

=--

This way every CW-spectrum is the union of all its cells in the sense of def. \ref{CellOfACWSpectrum}. (e.g. [Switzer 75, 8.4](Switzer75)).

More abstractly:

+-- {: .num_defn }
###### Definition

A **[[cell spectrum]]** is a topologicl [[sequential spectrum]] $X$ realized as the [[colimit]] over a sequence of spectra $\ast = X_0 \to X_1 \to X_2 \to X_3 \to \cdots$ such that there are morphisms

$$
  j_n 
   \;\colon\; 
   \left(
      \underset{i \in I_n}{\sqcup} \Sigma^\infty S^{q_n}
   \right)
   \longrightarrow
   X_n
$$

with $X_{n+1}= Cone(j_n)$ (the [[mapping cone]]).

A cell spectrum is a **CW-spectrum** if each attaching map $\Sigma^\infty S^{q_n}\to X_n$ factors through a $X_k \to X_n$ with $k \lt q$.

=--

(e.g. [Lewis-May-Steinberger 86, def. 5.1, def. 52](#LewisMaySteinberger86))


+-- {: .num_defn #CellOfACWSpectrum}
###### Definition

A CW-spectrum, def. \ref{CWSpectrum}, is called a _[[finite spectrum]]_ (or countable spectrum, etc.) if it has [[finite number|finitely many]] cells (countably many cells) according to def. \ref{CellOfACWSpectrum}.

=--

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

Discussion in the generality of [[equivariant spectra]] is in 

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and M. Steinberger (with contributions by J.E. McClure), section I.5 of _Equivariant stable homotopy theory_ Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))


[[!redirects CW spectra]]

[[!redirects CW-spectrum]]
[[!redirects CW-spectra]]

[[!redirects CW spectrum]]
