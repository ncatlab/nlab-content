


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

## Definition


+-- {: .num_defn #CellSpectrum}
###### Definition

A **cell spectrum** is a topological [[sequential spectrum]] $X$ realized as the [[colimit]] over a sequence of spectra $\ast = X_0 \to X_1 \to X_2 \to X_3 \to \cdots$ such that there are morphisms

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

A cell spectrum is a **[[CW-spectrum]]** if each attaching map $\Sigma^\infty S^{q_n}\to X_n$ factors through a $X_k \to X_n$ with $k \lt q$.

=--

(e.g. [Lewis-May-Steinberger 86, def. 5.1, def. 52](#LewisMaySteinberger86))


+-- {: .num_defn #CellOfACWSpectrum}
###### Definition

A CW-spectrum, def. \ref{CellSpectrum}, is called a _[[finite spectrum]]_ (or countable spectrum, etc.) if it has [[finite number|finitely many]] cells (countably many cells) according to def. \ref{CellOfACWSpectrum}.

=--


## Related concepts

* [[cell complex]]

## References


Discussion in the generality of [[equivariant spectra]] is in 

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and M. Steinberger (with contributions by J.E. McClure), section I.5 of _Equivariant stable homotopy theory_ Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))


[[!redirects cell spectra]]

