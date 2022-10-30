
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


## References

* {#Adams74} [[Frank Adams]], section III.2 and III.3 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


* {#ElmendorfKrizMay} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 1 of _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_,  1995 Amsterdam: North-Holland, pp. 213&#8211;253,   ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

[[!redirects CW spectra]]

[[!redirects CW-spectrum]]
[[!redirects CW-spectra]]

[[!redirects CW spectrum]]
