
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *compactly supported mapping space* is a [[subspace]] of a [[mapping space]] on those [[maps]] that have [[compact support]].

## Definition


Let $X$ be a [[topological space]]. For $C \subset X$ a [[compact subset]], write $cof(X\setminus C \to X)$ for the [[cofiber]] of the inclusion of its [[complement]], hence for the result of collapsing the [[complement]] to a [[base point]].

For a [[pointed topological space]] $A$, the *[[compactly supported mapping space]]* from $X$ to $A$ is the following [[colimit]] of [[pointed mapping spaces]]:
\[
  \label{CompactlySupportedMappingSpace}
  Map^c(X,A)
  \,\coloneqq\,
  \underset{\underset{C}{\longrightarrow}}{\lim} 
  \,
  Map^\ast\big(
    cof(X \setminus C \to X)
    ,
    A
  \big)
  \mathrlap{\,.}
\]

## Properties

### Relation to one-point compactification

Now let $X$ be a [[locally compact topological space]] with [[one-point compactification]] $X_{cpt}$. Then we have a canonical [[homeomorphism]]
$$
  cof\big(
    X_{cpt} \setminus C
    \to 
    X_{cpt}
  \big)
  \simeq
  cof\big(
    X \setminus C 
    \to 
    X
  \big)
$$
and hence a system of comparison maps, [[natural transformation|natural]] in $C$, of the form:
\[
  \label{CollapsingComplementOfCompactinOnePointCompactification}
  X_{cpt} 
    \longrightarrow
  cof(X \setminus C \to X)
  \mathrlap{\,.}
\]
which induces a comparison map from the [[compactly supported mapping space]] (eq:CompactlySupportedMappingSpace) to the [[pointed mapping space]] out of the [[one-point compactification]]:

\[
  \label{ComparisonMapFromCompactToPointedMappingSpace}
  Map^c(X,A)
  \longrightarrow
  Map^\ast\big(
    X_{cpt} , A
  \big)
\]

\begin{proposition}
  A sufficient condition for the comparison map (eq:ComparisonMapFromCompactToPointedMappingSpace) to be a [[weak homotopy equivalence]] is that

* $X$ is a [[manifold]] which is finitary in that it is the [[complement]] of some [[faces]] ([[codimension]]=1 [[stratified space|strata]]) of a [[compact topological space|compact]] [[manifold with corners]].

\end{proposition}

([Mazel-Gee 2016 §2.5](#Mazel-Gee2016), [Ayala & Francis 2025 p 6](#AyalaFrancis2025))


## Related concepts

* [[compactly supported cohomology]]

## References

* {#Mazel-Gee2016} [[Aaron Mazel-Gee]]; §2.5 in: *Locally Constant Factorization Algebras*, lecture notes (2016) &lbrack;[pdf](https://etale.site/teaching/s16-lcfa/locally-constant.pdf), [[MazelGee-FactorizationHomology.pdf:file]]&rbrack;

* {#AyalaFrancis2025} [[David Ayala]], [[John Francis]]; p. 6 of: *A parametrized Pontryagin-Thom theorem* \[<a href="https://arxiv.org/abs/2512.10274">arXiv:2512.10274 math.AT</a>\]

In the generality of [[G-spaces]]:

* Jeremy Hahn, Asaf Horev, Inbar Klang, [[Dylan Wilson]], Foling Zou; Prop. 4.4.2 in: *Equivariant nonabelian Poincaré duality and equivariant factorization homology of Thom spectra* \[<a href="https://arxiv.org/abs/2006.13348">arXiv:2006.13348</a>\]

[[!redirects compactly supported mapping spaces]]

